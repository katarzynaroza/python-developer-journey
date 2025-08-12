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

## 🐞 Błąd: TypeError: 'NoneType' object is not subscriptable

- 🎓 Moduł kursu: Flask – routing
- 📁 Plik źródłowy: app.py
- ❌ Problem: Po uruchomieniu aplikacji i wejściu na stronę /user/Anna, pojawiał się błąd zamiast danych użytkownika.
- 🔍 Przyczyna: Funkcja `get_user()` zwracała `None`, bo użytkownik nie był znaleziony w bazie, a mimo to próbowałam odczytać `user['name']`.
- ✅ Rozwiązanie: Dodałam warunek `if user is None:` i przekierowanie na stronę błędu.
- 💡 Lekcja: Zawsze sprawdzaj, czy obiekt istnieje, zanim spróbujesz go użyć. Python nie wybacza nadziei 😉
