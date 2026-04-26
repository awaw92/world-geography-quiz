📄 World Geography Quiz

World Geography Quiz to pełnostackowa aplikacja webowa zbudowana w Django, Pythonie oraz JavaScript. Jest to interaktywna platforma edukacyjna służąca do sprawdzania i rozwijania wiedzy z geografii świata.

Użytkownicy rozwiązują quiz składający się z losowo wybranych pytań, wybierają poziom trudności oraz otrzymują natychmiastową informację zwrotną, wynik końcowy oraz ranking graczy.

Projekt został stworzony jako projekt końcowy CS50 Web Programming with Python and JavaScript i demonstruje integrację logiki backendowej, modeli bazy danych, zarządzania sesjami oraz dynamicznego frontendu.

🧠 Odrębność i złożoność projektu

Projekt spełnia wymagania odrębności i złożoności projektu końcowego CS50W w następujący sposób:

📌 Charakter aplikacji

Aplikacja jest interaktywnym systemem quizowym, który łączy:

trwałe przechowywanie wyników użytkowników,
filtrowanie treści według poziomu trudności,
progresję quizu opartą o sesje,
interaktywność po stronie klienta (JavaScript),
ranking oparty o bazę danych.

W przeciwieństwie do wcześniejszych projektów kursowych skupionych na operacjach CRUD lub prostych interakcjach użytkownika, ten projekt koncentruje się na stanowej interakcji użytkownika, progresji gry oraz pętli edukacyjnej (feedback learning loop).

⚙️ Kluczowe elementy złożoności
📌 Quiz oparty o sesje

Aplikacja przechowuje stan quizu w sesji Django, śledząc:

aktualne pytanie,
wybrane odpowiedzi,
wynik użytkownika,
stan zakończenia quizu.

Zapewnia to wieloetapowy przebieg bez konieczności logowania użytkownika.

📌 Poziomy trudności

Pytania podzielone są na:

Łatwe
Średnie
Trudne

Każda sesja quizu losuje do 10 pytań z wybranego poziomu trudności.

📌 Ranking i wyniki

Wyniki graczy są zapisywane w modelu bazy danych PlayerScore, co umożliwia:

ranking według poziomu trudności,
porównywanie wyników między graczami,
analizę historii prób.
📌 Interaktywność JavaScript

JavaScript odpowiada za:

wybór odpowiedzi,
wizualne oznaczanie poprawnych i błędnych odpowiedzi,
opóźnienie wysyłki formularza (animacje),
poprawę UX ponad standardowe formularze Django.
📌 Separacja logiki

Projekt jest podzielony na:

modele danych,
logikę widoków,
szablony HTML,
logikę po stronie klienta (JavaScript).
📁 Struktura projektu i pliki
🗄️ quiz/models.py

Definiuje strukturę bazy danych:

Question – pytania quizowe, odpowiedzi, poprawna odpowiedź, poziom trudności
PlayerScore – dane gracza, wynik, poziom trudności, data
🧠 quiz/views.py

Główna logika aplikacji:

start_quiz – inicjalizacja quizu, ustawienie sesji
question_view – obsługa pytań, walidacja odpowiedzi, aktualizacja wyniku
result_view – wyświetlanie wyników i zapis do bazy
🖥️ start.html
formularz wejściowy do quizu
dane gracza (imię, kraj, wiek, poziom trudności)
walidacja danych
responsywny interfejs
❓ question.html
wyświetlanie pytań quizowych
obsługa JavaScript
animacje odpowiedzi
blokada wielokrotnego wyboru
🏁 result.html
wynik końcowy quizu
szczegółowe podsumowanie odpowiedzi
ranking graczy
podświetlenie aktualnego gracza
🌐 quiz/urls.py

Routing aplikacji:

start quizu
pytania
wyniki
⚙️ quiz/admin.py

Rejestracja modeli w panelu administracyjnym Django

⚙️ quizproject/settings.py

Konfiguracja Django:

aplikacje
middleware
baza danych SQLite
ustawienia szablonów
pliki statyczne
🗃️ db.sqlite3

Baza danych zawierająca:

przykładowe pytania
przykładowe wyniki graczy
📦 requirements.txt

Zależności projektu (m.in. Django)

🚀 Uruchomienie projektu
📌 Wymagania
Python 3.8+
Django 3.2 – 4.x
📥 Instalacja
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
🌐 Dostęp
Aplikacja: http://127.0.0.1:8000/
Panel admina: http://127.0.0.1:8000/admin/
📌 Dodatkowe informacje
Cała logika quizu i scoringu działa po stronie backendu (Django sessions)
JavaScript służy tylko do poprawy interakcji użytkownika
Aplikacja jest responsywna (mobile + desktop)
Projekt został wykonany wyłącznie w celach edukacyjnych
🏁 Podsumowanie

Projekt przedstawia kompletną aplikację Django, łączącą:

logikę backendową,
bazę danych,
zarządzanie sesjami,
interaktywny frontend.

