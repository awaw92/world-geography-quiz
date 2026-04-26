📄 World Geography Quiz

World Geography Quiz to pełnostackowa aplikacja webowa zbudowana w Django, Pythonie i JavaScript. Aplikacja pozwala użytkownikom rozwiązywać quizy z geografii świata, wybierać poziom trudności oraz śledzić swoje wyniki w rankingu.

Projekt został zaprojektowany jako interaktywny system edukacyjny z elementami grywalizacji, łączący backend, bazę danych oraz dynamiczny frontend.

🧠 O projekcie

Aplikacja skupia się na:

zarządzaniu stanem quizu w sesjach użytkownika
dynamicznym generowaniu pytań
systemie punktacji i rankingów
interaktywnej obsłudze odpowiedzi w JavaScript
przechowywaniu wyników w bazie danych

W przeciwieństwie do klasycznych aplikacji CRUD, projekt symuluje logikę gry / quizu z progresją i feedbackiem użytkownika.

⚙️ Kluczowe funkcjonalności
Quiz z losowo wybieranymi pytaniami
Trzy poziomy trudności: łatwy, średni, trudny
System punktacji oraz wynik końcowy
Ranking graczy zapisany w bazie danych
Historia wyników użytkowników
Interaktywne odpowiedzi z natychmiastowym feedbackiem
Dynamiczne przejścia między pytaniami
🧩 Logika działania aplikacji
📌 Zarządzanie quizem
Stan quizu przechowywany jest w sesji Django
Sesja kontroluje:
aktualne pytanie
wynik użytkownika
postęp quizu
📌 Generowanie pytań
Pytania są losowane z bazy danych
Filtrowane według wybranego poziomu trudności
Każda sesja quizu zawiera ograniczoną liczbę pytań
📌 System wyników
Wyniki zapisywane są w modelu PlayerScore
Każdy wynik zawiera:
imię gracza
kraj i wiek
poziom trudności
wynik punktowy
datę
Wyniki są używane do generowania rankingu
📌 Interakcja (JavaScript)

JavaScript odpowiada za:

wybór odpowiedzi
wizualne oznaczenie poprawnych / błędnych odpowiedzi
blokadę wielokrotnego wyboru
płynne przejścia między pytaniami
poprawę UX bez przeładowywania strony
🧠 Struktura projektu
🗄️ models.py
Question – pytania, odpowiedzi, poprawna odpowiedź, poziom trudności
PlayerScore – dane gracza oraz wynik quizu
🧠 views.py
start_quiz – inicjalizacja quizu, wybór poziomu trudności i zapis sesji
question_view – obsługa logiki pytań i aktualizacja wyniku
result_view – wyświetlenie wyników i zapis do bazy danych
🖥️ Frontend
ekran startowy (dane gracza + wybór trudności)
widok pytań z interaktywnymi odpowiedziami
ekran wyników z podsumowaniem
ranking graczy
🌐 Routing (urls.py)
start quizu
kolejne pytania
ekran wyników
🛠️ Technologie
Python
Django
JavaScript
HTML / CSS
SQLite
🏁 Podsumowanie

World Geography Quiz to rozbudowana aplikacja webowa łącząca:

backend Django z logiką sesji
bazę danych i system rankingowy
dynamiczny frontend w JavaScript
mechanikę quizu z elementami grywalizacji

Projekt pokazuje umiejętność budowania aplikacji złożonych, które wymagają zarządzania stanem użytkownika, logiki biznesowej oraz interaktywnego UI.
