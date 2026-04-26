World Geography Quiz

Aplikacja webowa typu quiz zbudowana w Django, Pythonie i JavaScript. Umożliwia rozwiązywanie testów z geografii świata, wybór poziomu trudności oraz śledzenie wyników w systemie rankingowym.

Aplikacja działa w modelu sesyjnym i zapisuje wyniki użytkowników w bazie danych.

📌 Funkcjonalności
Quiz z losowo wybieranymi pytaniami
Trzy poziomy trudności (łatwy / średni / trudny)
System punktacji i wynik końcowy
Ranking graczy
Zapis wyników do bazy danych
Historia wyników użytkowników
Interaktywny feedback po odpowiedzi
Dynamiczne przejścia między pytaniami
🧩 Jak działa aplikacja
Aplikacja wykorzystuje sesje Django do przechowywania stanu quizu
Każda sesja śledzi:
aktualne pytanie
wynik użytkownika
postęp quizu
Pytania są losowane z bazy danych na podstawie poziomu trudności
Po zakończeniu quizu wynik zapisywany jest w bazie danych
Ranking generowany jest na podstawie zapisanych wyników
JavaScript obsługuje interakcje użytkownika i feedback wizualny
🛠️ Technologie
Python
Django
JavaScript
HTML
CSS
SQLite
📁 Główne elementy
models.py – definicja pytań i wyników graczy
views.py – logika quizu i sesji
templates/ – widoki (start, pytania, wyniki)
static/ – JavaScript i stylowanie
🚀 Architektura
Django + sesje do zarządzania stanem quizu
Model oparty na bazie danych (pytania + wyniki)
Frontend wzbogacony o JavaScript (interakcja i UX)
System rankingowy oparty o zapisane wyniki graczy
