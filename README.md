📄 World Geography Quiz

World Geography Quiz to pełnostackowa aplikacja webowa stworzona w Django, Pythonie i JavaScript.

Aplikacja umożliwia rozwiązywanie quizów z geografii świata, wybór poziomu trudności oraz śledzenie wyników w systemie rankingowym.

Projekt łączy backend, bazę danych oraz interaktywny frontend.

🧠 O projekcie

Aplikacja koncentruje się na:

zarządzaniu stanem quizu w sesji użytkownika
dynamicznym generowaniu pytań
systemie punktacji i rankingów
interakcji użytkownika w czasie rzeczywistym
przechowywaniu wyników w bazie danych

Projekt nie jest typowym CRUD-em — działa jak system quizowy z logiką gry i progresją użytkownika.

⚙️ Kluczowe funkcjonalności
quiz z losowo wybieranymi pytaniami
poziomy trudności: łatwy / średni / trudny
system punktacji i wynik końcowy
ranking graczy
zapis wyników w bazie danych
natychmiastowy feedback po odpowiedzi
płynna nawigacja między pytaniami
🧩 Logika działania aplikacji
📌 Sesje (Django)

Stan quizu przechowywany jest w sesji:

aktualne pytanie
wynik użytkownika
postęp quizu
📌 Generowanie pytań
pytania pobierane z bazy danych
filtrowanie według poziomu trudności
losowy wybór zestawu pytań
📌 System wyników

Model PlayerScore przechowuje:

dane gracza (imię, kraj, wiek)
wynik końcowy
poziom trudności
datę

Na tej podstawie tworzony jest ranking graczy.

📌 Interakcja (JavaScript)

JavaScript odpowiada za:

wybór odpowiedzi
wizualne oznaczenie poprawnych i błędnych odpowiedzi
blokadę wielokrotnego kliknięcia
płynne przejścia między pytaniami
poprawę UX bez przeładowania strony
🧠 Struktura projektu
🗄️ models.py
Question – pytania, odpowiedzi, poprawna odpowiedź, poziom trudności
PlayerScore – wyniki graczy
🧠 views.py
start_quiz – inicjalizacja quizu
question_view – logika pytań i wyników
result_view – zapis wyniku i ekran końcowy
🖥️ Frontend
ekran startowy (formularz gracza)
widok pytań z interakcją
ekran wyników
ranking
🛠️ Technologie
Python
Django
JavaScript
HTML / CSS
SQLite
🏁 Podsumowanie

Projekt pokazuje umiejętność budowy pełnej aplikacji webowej obejmującej:

backend w Django
zarządzanie sesją użytkownika
bazę danych i ranking
interaktywny frontend w JavaScript
