# 🐞 Bugfixes

This file documents bugs I encountered and how I solved them.  
Each entry includes the module, the issue, the reaseon, the fix, and a short reflection.  
It's part of my learning process and helps me track progress and mistakes.

---

## 🐞 Błąd: JSONDecodeError

- 🎓 Moduł kursu: API i obsługa danych JSON
- ❌ Problem: Próba wczytania pustego stringa przez `json.loads()`
- 🔍 Przyczyna: Brak walidacji danych wejściowych
- ✅ Rozwiązanie: Dodano warunek `if data:` przed parsowaniem
- 💡 Lekcja: `json.loads()` wymaga poprawnego formatu – warto zawsze sprawdzać dane przed parsowaniem

---

Szablon:
  ## 🐞 Błąd: [Nazwa błędu lub krótki opis]

- 🎓 Moduł kursu: [Nazwa modułu, np. "Obsługa plików", "Flask – routing"]
- ❌ Problem: [Co dokładnie się działo? Jak objawiał się błąd?]
- 🔍 Przyczyna: [Dlaczego wystąpił błąd? Co było źródłem?]
- ✅ Rozwiązanie: [Jak go naprawiłaś? Co zmieniłaś w kodzie?]
- 💡 Lekcja: [Czego się nauczyłaś? Jakie wnioski na przyszłość?]
