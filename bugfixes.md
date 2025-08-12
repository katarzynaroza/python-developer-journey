# 🐞 Bugfixes

This file documents bugs I encountered and how I solved them.  
Each entry includes the module, the issue, the reaseon, the fix, and a short reflection.  
It's part of my learning process and helps me track progress and mistakes.

---
  ## 🐞 Błąd: [Nazwa błędu lub krótki opis]

- 🎓 Moduł kursu: [Nazwa modułu, np. "Obsługa plików", "Flask – routing"]
- ❌ Problem: [Co dokładnie się działo? Jak objawiał się błąd?]
- 🔍 Przyczyna: [Dlaczego wystąpił błąd? Co było źródłem?]
- ✅ Rozwiązanie: [Jak go naprawiłaś? Co zmieniłaś w kodzie?]
- 💡 Lekcja: [Czego się nauczyłaś? Jakie wnioski na przyszłość?]

example:
## 🐞 Błąd: TypeError przy dodawaniu do listy

- 🎓 Moduł kursu: Podstawy Pythona – struktury danych
- ❌ Problem: Próba dodania `None` do listy powodowała wyjątek
- 🔍 Przyczyna: Funkcja zwracała `None`, bo brakowało `return`
- ✅ Rozwiązanie: Dodano `return new_item` na końcu funkcji
- 💡 Lekcja: Funkcja bez `return` zwraca `None` – warto zawsze sprawdzać, co funkcja zwraca
