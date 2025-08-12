📘 glossary.md – Bugfix Log Glossary

This glossary helps me write bugfix logs and documentation in English.  
It includes common terms from frontend, backend, testing, GitHub, DevOps, security, and AI/ML.

---

🎨 Frontend

| 🇬🇧 Term               | 🇵🇱 Translation             | 💡 Notes / Example                              |
|------------------------|-----------------------------|-------------------------------------------------|
| DOM (Document Object Model) | model obiektowy dokumentu | Manipulating the DOM with JavaScript            |
| Element                | element                     | Clicked element didn't trigger event            |
| Event listener         | nasłuchiwacz zdarzeń        | Added a click event listener                    |
| CSS selector           | selektor CSS                | Wrong selector caused styling bug               |
| Responsive design      | projekt responsywny         | Bug on mobile view due to missing media query   |
| Viewport               | obszar widoczny             | Viewport too small for layout                   |
| Render                 | renderowanie                | Component didn't render correctly               |
| State                  | stan                        | Incorrect state caused UI glitch                |
| Props                  | właściwości (React)         | Passed wrong props to component                 |
| Component              | komponent                   | Component didn't update on state change         |

---

⚙️ Backend

| 🇬🇧 Term               | 🇵🇱 Translation             | 💡 Notes / Example                              |
|------------------------|-----------------------------|-------------------------------------------------|
| Endpoint               | punkt końcowy API           | GET /users endpoint returned 500 error          |
| Request                | żądanie                     | Request body was missing required field         |
| Response               | odpowiedź                   | Response status was 404                         |
| Status code            | kod statusu                 | Fixed incorrect 403 status                      |
| Middleware             | pośrednik / middleware      | Bug in authentication middleware                |
| Database               | baza danych                 | Query returned empty result                     |
| Query                  | zapytanie                   | SQL query had syntax error                      |
| Model                  | model danych                | Model validation failed                         |
| Serializer             | serializator                | Serializer didn't include all fields            |
| Authentication         | uwierzytelnianie            | Login failed due to token error                 |

---

🧪 Testing

| 🇬🇧 Term               | 🇵🇱 Translation             | 💡 Notes / Example                              |
|------------------------|-----------------------------|-------------------------------------------------|
| Unit test              | test jednostkowy            | Added unit test for login function              |
| Integration test       | test integracyjny           | Tested API and database together                |
| Mock                   | obiekt pozorowany / mock    | Used mock for external API call                 |
| Assertion              | asercja / sprawdzenie       | Assertion failed: expected 200, got 500         |
| Test coverage          | pokrycie testami            | Improved coverage to 85%                        |
| Failing test           | test zakończony błędem      | Test failed due to missing setup                |
| Setup / teardown       | przygotowanie / sprzątanie  | Forgot to teardown database after test          |
| CI (Continuous Integration) | ciągła integracja       | Bug in CI pipeline blocked deployment           |

---

🗂️ Git & GitHub

| 🇬🇧 Term               | 🇵🇱 Translation             | 💡 Notes / Example                              |
|------------------------|-----------------------------|-------------------------------------------------|
| Commit                 | commit / zatwierdzenie      | Commit message was unclear                      |
| Branch                 | gałąź                       | Bug only on feature/login branch                |
| Merge                  | scalanie                    | Merge conflict caused syntax error              |
| Pull request (PR)      | żądanie scalenia            | PR failed tests due to typo                     |
| Conflict               | konflikt                    | Resolved merge conflict manually                |
| Push / Pull            | wypchnięcie / pobranie      | Forgot to push latest changes                   |
| Repository             | repozytorium                | Bugfix log added to repository                  |
| Issue                  | zgłoszenie / problem        | Created GitHub issue for broken layout          |
| Tag                    | tag / etykieta              | Tagged release v1.0.1                           |

---

🚀 DevOps

| 🇬🇧 Term               | 🇵🇱 Translation             | 💡 Notes / Example                              |
|------------------------|-----------------------------|-------------------------------------------------|
| Pipeline               | potok / pipeline            | CI pipeline failed on test stage                |
| Deployment             | wdrożenie                   | Deployment broke due to missing env variable    |
| Environment variable   | zmienna środowiskowa        | Used ENV_SECRET in config                     |
| Container              | kontener                    | Bug in Docker container setup                   |
| Dockerfile             | plik Dockerfile             | Dockerfile missing CMD instruction            |
| Kubernetes             | Kubernetes                  | Pod crashed due to misconfigured volume         |
| YAML                   | plik YAML                   | Syntax error in deployment.yaml                 |
| Monitoring             | monitorowanie               | No alerts triggered during outage               |
| Rollback               | cofnięcie wdrożenia         | Performed rollback to previous version          |
| Infrastructure as Code (IaC) | infrastruktura jako kod | Used Terraform to provision resources           |

---

🔐 Security

| 🇬🇧 Term               | 🇵🇱 Translation             | 💡 Notes / Example                              |
|------------------------|-----------------------------|-------------------------------------------------|
| Authentication         | uwierzytelnianie            | Login failed due to invalid credentials         |
| Authorization          | autoryzacja                 | User not authorized to access admin panel       |
| Token                  | token                       | Expired JWT token caused error                  |
| Encryption             | szyfrowanie                 | Data encrypted using AES                        |
| Hashing                | haszowanie                  | Passwords hashed with bcrypt                    |
| Vulnerability          | podatność                   | Fixed XSS vulnerability in form input           |
| XSS (Cross-Site Scripting) | atak XSS              | Sanitized user input to prevent XSS             |
| CSRF (Cross-Site Request Forgery) | fałszywe żądanie | Added CSRF token to form                        |
| Rate limiting          | ograniczenie liczby żądań   | API rate limit exceeded                         |
| Security headers       | nagłówki bezpieczeństwa     | Configured Content-Security-Policy            |

---

🧠 AI / Machine Learning

| 🇬🇧 Term               | 🇵🇱 Translation             | 💡 Notes / Example                              |
|------------------------|-----------------------------|-------------------------------------------------|
| Model                  | model                       | Trained model on 10k samples                    |
| Training               | trenowanie                  | Bug in training loop caused NaN loss            |
| Dataset                | zbiór danych                | Missing labels in dataset                       |
| Feature                | cecha / zmienna             | Selected top 10 features for prediction         |
| Label                  | etykieta / wynik            | Incorrect label mapping                         |
| Loss function          | funkcja straty              | Loss didn't decrease during training            |
| Overfitting            | przeuczenie                 | Model overfitted on training data               |
| Inference              | wnioskowanie / predykcja    | Slow inference on large batch                   |
| Hyperparameter         | hiperparametr               | Tuned learning rate and batch size              |
| Evaluation             | ewaluacja / ocena           | Used accuracy and F1 score for evaluation       |

---

📌 This glossary will grow as I learn more. It's a tool to help me write clearly and confidently in English while documenting bugs and fixes.

---
