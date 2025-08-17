# 📝 Task - The find_max() function is supposed to find and return the largest number from a list of integers. However, it returns incorrect results due to an error:

def find_max(numbers):  
    max_num = None  
    for num in numbers:  
        if max_num < num:  
            max_num = num  
    return max_num  

Step-by-step task:  
Find and fix the error in the find_max() function.  
Make sure the function returns the correct results. Consider edge cases, such as empty lists—in these cases, None should be returned.
💡 Examine how the max_num variable is initialized and compared within the loop. Use PyCharm's debugging tools.

RESULT:
def find_max(numbers):  
    if not numbers:  
        return None  
    max_num = numbers[0]  
    for num in numbers:  
        if max_num <= num:  
            max_num = num              
    return max_num
      
# 💭 Technical reflection:
- if not numbers:  
        return None  -> this part is helpful (when I want check if the list is empty)
- when I want to bugfix, i need to call the function at the end

# 📝 Task - The function should reverse a string (e.g., "Python" → "nohtyP"). For some reason, it only returns the first letter.

def reverse_string(text):
----reversed_text = ""  
____for char in text:
--------reversed_text = char
----return reversed_text

👉 Test it on "Ala has a cat".


RESULT:
def reverse_string(text):
    reversed_text = ""
    for i in range(len(text) - 1, -1, -1):
        reversed_text += text[i]
    return reversed_text

print(reverse_string("Ala ma kota"))

# 💭 Technical reflection: 
Zasada działania
Funkcja range() generuje sekwencję liczb.

Pętla for...in działa na obiekcie, który jest "iterowalny", czyli takim, z którego można po kolei pobierać elementy.

range(len(text) - 1, -1, -1) tworzy w pamięci sekwencję liczb całkowitych, np. [10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0].

Ta sekwencja nie wie nic o zmiennej text. Jej jedynym zadaniem jest wygenerowanie liczb, które podałeś.

Pętla for używa tych liczb jako indeksów.

W każdej iteracji pętli, zmienna i (zamiast char jak w poprzednich przykładach, bo teraz to jest indeks) przyjmuje kolejną wartość z sekwencji wygenerowanej przez range().

W pierwszej iteracji i będzie równe 10, w drugiej 9 i tak dalej.

Następnie, wewnątrz pętli, używasz tej liczby do indeksowania zmiennej text za pomocą nawiasów kwadratowych [].

To właśnie ta linijka: print(text[i]) łączy liczbę wygenerowaną przez range() z konkretnym znakiem w zmiennej text.

# 🔖 Tags / topics:
`TAG: bugfix | TAG: none | TAG: range`  
