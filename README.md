📄 World Geography Quiz

World Geography Quiz to pełnostackowa aplikacja webowa zbudowana w Django, Pythonie i JavaScript. Aplikacja umożliwia rozwiązywanie quizów z geografii świata, wybór poziomu trudności oraz śledzenie wyników w rankingu.

Projekt koncentruje się na interaktywnej rozgrywce, zarządzaniu stanem użytkownika oraz przechowywaniu wyników w bazie danych.

🧠 Główne funkcjonalności
Quiz z losowo wybieranymi pytaniami
Poziomy trudności (łatwy / średni / trudny)
System punktacji i wynik końcowy
Ranking graczy według poziomu trudności
Historia wyników zapisywana w bazie danych
Interaktywne odpowiedzi z wykorzystaniem JavaScript
⚙️ Jak działa aplikacja
Stan quizu przechowywany jest w sesji Django
Każda sesja śledzi aktualne pytanie, odpowiedzi i wynik
Pytania są losowane na podstawie wybranego poziomu trudności
Wyniki są zapisywane w bazie danych i wykorzystywane do rankingu
JavaScript odpowiada za interakcje i wizualną informację zwrotną
🧩 Struktura projektu
🗄️ Models
Question – pytania, odpowiedzi, poprawna odpowiedź, poziom trudności
PlayerScore – dane gracza, wynik, poziom trudności, data
🧠 Views
start_quiz – inicjalizacja quizu i wybór ustawień
question_view – obsługa pytań i aktualizacja wyniku
result_view – wyświetlenie wyników i zapis do bazy
🖥️ Frontend
formularz startowy z danymi gracza
widok pytań z interaktywnym wyborem odpowiedzi
ekran wyników z podsumowaniem i rankingiem
dynamiczne efekty i walidacja w JavaScript
🛠️ Technologie
Python
Django
JavaScript
HTML / CSS
SQLite (baza danych)
🏁 Podsumowanie

Projekt przedstawia kompletną aplikację quizową, która łączy backend Django, bazę danych oraz interaktywny frontend.

Najważniejsze elementy:

zarządzanie stanem użytkownika (sessions)
logika gry i progresji quizu
ranking i analiza wyników
dynamiczna interakcja w JavaScript
