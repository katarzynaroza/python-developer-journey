# 🐞 Bugfixes

This file documents bugs I encountered and how I solved them.  
Each entry includes the module, the issue, the reaseon, the fix, and a short reflection.  
It's part of my learning process and helps me track progress and mistakes.

---

## 🐞 Błąd: [Nazwa błędu lub krótki opis]

- 🎓 Moduł kursu: [np. "Flask – routing"]
- 📁 Plik źródłowy: [np. "app.py"] *(opcjonalnie)*
- ❌ Problem: [Co się działo?]
- 🔍 Przyczyna: [Dlaczego wystąpił błąd?]
- ✅ Rozwiązanie: [Jak go naprawiłaś?]
- 💡 Lekcja: [Czego się nauczyłaś?]

example:

## 🐞 Bug: TypeError when adding to list

- 🎓 Course module: Python Basics – Data Structures  
- 📁 Source file: list_utils.py  
- ❌ Problem: Attempting to add `None` to a list caused a TypeError  
- 🔍 Cause: The function returned `None` because it was missing a `return` statement  
- ✅ Fix: Added `return new_item` at the end of the function  
- 💡 Lesson: A function without `return` returns `None` — always check what your function gives back
