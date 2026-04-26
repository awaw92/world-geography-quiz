# World Geography Quiz

Aplikacja webowa typu quiz zbudowana w Django, Pythonie i JavaScript. Umożliwia rozwiązywanie testów z geografii świata, wybór poziomu trudności oraz śledzenie wyników w systemie rankingowym.

Aplikacja działa w modelu sesyjnym i zapisuje wyniki użytkowników w bazie danych.

---

## 📌 Funkcjonalności

- Quiz z losowo wybieranymi pytaniami  
- Trzy poziomy trudności (łatwy / średni / trudny)  
- System punktacji i wynik końcowy  
- Ranking graczy  
- Zapis wyników do bazy danych  
- Historia wyników użytkowników  
- Interaktywny feedback po odpowiedzi  
- Dynamiczne przejścia między pytaniami  

---

## 🧩 Jak działa aplikacja

- Aplikacja wykorzystuje sesje Django do przechowywania stanu quizu  
- Każda sesja śledzi:
  - aktualne pytanie  
  - wynik użytkownika  
  - postęp quizu  

- Pytania są losowane z bazy danych na podstawie poziomu trudności  
- Po zakończeniu quizu wynik zapisywany jest w bazie danych  
- Ranking generowany jest na podstawie zapisanych wyników  
- JavaScript odpowiada za interakcje i wizualny feedback  

---

## 🗄️ Modele danych

- **Question** – pytania, odpowiedzi i poprawna odpowiedź  
- **PlayerScore** – dane gracza oraz wynik quizu  

---

## 🧠 Logika backendu

- `start_quiz` – inicjalizacja quizu i ustawień gracza  
- `question_view` – obsługa pytań i aktualizacja wyniku  
- `result_view` – zapis wyniku i ekran końcowy  

---

## 🖥️ Frontend

- ekran startowy (formularz gracza i wybór trudności)  
- widok pytań z interaktywnymi odpowiedziami  
- ekran wyników z podsumowaniem  
- ranking graczy  

---

## 🛠️ Technologie

- Python  
- Django  
- JavaScript  
- HTML  
- CSS  
- SQLite  

---

## 🚀 Architektura

- Django + sesje do zarządzania stanem quizu  
- Model oparty na bazie danych (pytania + wyniki)  
- Frontend wzbogacony o JavaScript (interakcja i UX)  
- System rankingowy oparty o zapisane wyniki graczy  
