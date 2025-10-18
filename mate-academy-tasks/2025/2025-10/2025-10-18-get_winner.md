# 📝 Task - During the Computer Science Olympiad, the server responsible for selecting the winner from among the finalists, Max and Roman, malfunctioned. It was supposed to return the number of tasks completed by Max and Roman, but instead returned—randomly—both numbers and strings.

Help us! Create a function get_winner that:  
Takes the number of problems solved by Max (max_solved) and Roman (roman_solved) as the first and second parameters, respectively. The function should be able to accept both strings and numbers.  
  
Returns:  
Max winner!!! if Max solved more problems.  
Roman winner!!! if Roman solved more problems.  
Roman and Maxim are the winners!!! if both finalists solved the same number of problems.  
  
Examples:  
<pre>
get_winner(45, "42") == "Max winner!!!"
get_winner("34", 35) == "Roman winner!!!"
get_winner(24, 28) == "Roman winner!!!"
get_winner("13", "11") == "Max winner!!!"
get_winner(15, "15") == "Roman and Maxim are the winners!!!"
</pre> 
WARNING: here I need polish commments, because a I want to undestand the code properly, if You want in English, please, use Google translator ;)  
  
RESULT:  
<pre>
# rules: odrzuca spacje wewnętrzne, minusy, kropki/przecinki a akceptuje „+” i spacje zewnętrzne (bo to obsłuży)
WRONG = "wrong data"
def parse_nonneg_int(x):
    if x is None: #  # odrzucam brak wartości; nie próbuję zgadywać liczby → zwracam WRONG. None nie jest liczbą ani poprawnym stringiem liczby, więc zwrot WRONG ma sens i upraszcza logikę.
        return WRONG
    if isinstance(x, bool): # Bool: chcesz je traktować jako WRONG czy jako 1/0? Jeśli WRONG, dodaj if isinstance(x, bool): return WRONG przed tą linią.
        return WRONG
    s = str(x) # dalej waliduję jako tekst: ujednolicam wejście (liczby/bool/str) do stringa, by sprawdzić znaki i format. Dlaczego 10a może “wyskoczyć błędem” przed s = str(x)?
    #Jeśli wpiszesz w kodzie literal 10a bez cudzysłowów, to Python nie uruchomi programu (błąd składni przy parsowaniu pliku), zanim w ogóle dojdzie do s = str(x).
    #Jeśli przyjdzie jako string, np. "10a", to s = str("10a") działa (zwraca "10a"). Błąd nie wystąpi tu, tylko dopiero później w walidacji/konwersji. Wpisując po prostu roman_solved = 10a bez cudzysłowów to błąd składni — Python nie potrafi tego zinterpretować ani jako liczbę, ani jako string.

    s = s.strip() # dopuszczam, żeby użytkownik mógł wstawiać spacje (i taby) na brzegach. Program to obsłuży, nie wywalając WRONG
    if s.startswith("+"): # jeśli wstawione dane zaczynają się od znaku "+", to usuwam go, liczbę po prostu traktuję jako zwykłą dodatnią
        s = s[1:]
    if not s: # ten test powinien być bezpośrednio pod powyższym. Korzyści: 1. Czytelność: “zdejmij plus → jeśli pusto, to błąd”.
# 2. Unikasz sprawdzania kolejnych reguł na pustym stringu.
        return WRONG
    if s[0] == "-": # nie przyjmuję wartośći ujemnej, z założenia wstawiona liczba miała wskazywać ilość liczbę zrobionych zadań, wartość ujemna byłaby nie logiczna
        return WRONG
    if any(ch.isspace() for ch in s): # Generator ch.isspace() for ch in s zwraca True/False dla każdego znaku - dzięki funkcji any().
# any(...) zatrzymuje się na pierwszym True (krótkie spięcie).
# Jeśli w s jest jakikolwiek biały znak (spacja, tab, newline), warunek wejdzie i zwróci wrong, jeśli jest jakikolwiek biały znak
        return WRONG
    if "_" in s:
        return WRONG
    if any(ch in ".," for ch in s): # tutaj oczywiście warunek any() sprawdza True/ False, jeśli True, czyli są jakieś znaki typu . albo , to program wejdzie i wykona, czyli zwróci wrong
        return WRONG
    if not s.isdigit(): # ten warunek sprawdza, czy to co zostało jest cyfrą
        return WRONG
    return int(s)


def get_winner(
        max_solved: str | int, roman_solved: str | int
) -> str:
    max_solved = parse_nonneg_int(max_solved)
    roman_solved = parse_nonneg_int(roman_solved)


    if max_solved == WRONG or roman_solved == WRONG:
        return WRONG
    if max_solved > roman_solved:
        return "Max winner!!!"
    elif max_solved < roman_solved:
        return "Roman winner!!!"
    else:
        return "Roman and Maxim are the winners!!!"

print(get_winner(max_solved = "xyz", roman_solved = "2"))
</pre>
  
# 💭 Technical reflection: 
- None is not a number or a valid number string, so the return WRONG makes sense and simplifies the logic.
- Why is if any(ch.isspace() for ch in s or "_" in s) /as a single line incorrect and it's better to split it into two separate if conditions:
The or operator has higher precedence here: s or "" in s first evaluates "" in s (bool), then does s or (this bool).  
When s is non-empty, the expression becomes any(ch.isspace() for ch in s) (OK), but when s is empty, it becomes any(ch.isspace() for ch in True), meaning you're iterating over bool (TypeError).  
Furthermore, I'd logically mix two different checks.

# 🔖 Tags / topics:
`TAG: isdigit | TAG: isspace` 
