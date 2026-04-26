📄 World Geography Quiz

World Geography Quiz to pełnostackowa aplikacja webowa zbudowana w Django, Pythonie i JavaScript.

Aplikacja pozwala użytkownikom rozwiązywać quizy z geografii świata, wybierać poziom trudności oraz śledzić wyniki w rankingu.

Projekt został zaprojektowany jako interaktywny system edukacyjny z elementami grywalizacji, łączący backend, bazę danych oraz dynamiczny frontend.

🧠 O projekcie

Aplikacja koncentruje się na:

zarządzaniu stanem quizu w sesjach użytkownika
dynamicznym generowaniu pytań
systemie punktacji i rankingów
interakcji w czasie rzeczywistym (JavaScript)
przechowywaniu wyników w bazie danych

W przeciwieństwie do klasycznych aplikacji CRUD, projekt symuluje logikę gry z progresją i feedbackiem użytkownika.

⚙️ Kluczowe funkcjonalności
quiz z losowo wybieranymi pytaniami
poziomy trudności (łatwy / średni / trudny)
system punktacji i wynik końcowy
ranking graczy
zapis wyników w bazie danych
natychmiastowy feedback po odpowiedzi
interaktywne przejścia między pytaniami
🧩 Logika działania
📌 Sesje (Django)

Stan quizu przechowywany jest w sesji:

aktualne pytanie
wynik użytkownika
postęp quizu
📌 Generowanie pytań
pytania losowane z bazy danych
filtrowanie po poziomie trudności
limit pytań na sesję
📌 Wyniki i ranking

Model PlayerScore przechowuje:

dane gracza (imię, kraj, wiek)
wynik końcowy
poziom trudności
datę

Na tej podstawie tworzony jest ranking graczy.

📌 Interakcja (JavaScript)

JavaScript odpowiada za:

wybór odpowiedzi
wizualne oznaczanie poprawnych i błędnych odpowiedzi
blokadę wielokrotnego klikania
płynne przejścia między pytaniami
poprawę UX bez przeładowania strony
🧠 Struktura projektu
🗄️ models.py
Question – pytania, odpowiedzi, poprawna odpowiedź, poziom trudności
PlayerScore – wyniki graczy
🧠 views.py
start_quiz – inicjalizacja quizu i ustawień
question_view – obsługa logiki pytań i wyniku
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

Projekt pokazuje umiejętność budowy pełnej aplikacji webowej, łączącej:

backend w Django
logikę sesji i stanu użytkownika
bazę danych i ranking
interaktywny frontend w JavaScript
