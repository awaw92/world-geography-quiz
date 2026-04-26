📄 World Geography Quiz

World Geography Quiz to pełnostackowa aplikacja webowa zbudowana w Django, Pythonie oraz JavaScript. Jest to interaktywna platforma edukacyjna służąca do sprawdzania i rozwijania wiedzy z geografii świata.

Użytkownicy rozwiązują quiz składający się z losowo wybranych pytań, wybierają poziom trudności, a następnie otrzymują natychmiastową informację zwrotną, wynik końcowy oraz ranking graczy.

Projekt został stworzony jako projekt końcowy CS50 Web Programming with Python and JavaScript i demonstruje integrację logiki backendowej, modeli bazy danych, zarządzania sesjami oraz dynamicznego frontendu.

🧠 Odrębność i złożoność projektu

Projekt spełnia wymagania odrębności i złożoności projektu końcowego CS50W w następujących obszarach:

📌 Charakter aplikacji

Aplikacja jest interaktywnym systemem quizowym, który łączy:

trwałe przechowywanie wyników użytkowników
filtrowanie treści według poziomu trudności
progresję quizu opartą o sesje
interaktywność po stronie klienta (JavaScript)
ranking oparty o bazę danych

W przeciwieństwie do wcześniejszych projektów kursowych skupionych na CRUD lub prostych formularzach, ten projekt koncentruje się na stanowej interakcji użytkownika oraz mechanice gry edukacyjnej.

⚙️ Kluczowe elementy złożoności
📌 Quiz oparty o sesje

Aplikacja przechowuje stan quizu w sesjach Django, śledząc:

aktualne pytanie
wybrane odpowiedzi
wynik użytkownika
stan zakończenia quizu

Dzięki temu quiz działa jako wieloetapowy proces bez konieczności logowania.

📌 Poziomy trudności

Pytania są podzielone na:

Łatwe
Średnie
Trudne

Każda sesja losuje do 10 pytań z wybranego poziomu trudności.

📌 Ranking i wyniki

Wyniki graczy są zapisywane w modelu PlayerScore, co umożliwia:

ranking według poziomu trudności
porównywanie wyników między graczami
analizę historii prób
📌 Interaktywność JavaScript

JavaScript odpowiada za:

wybór odpowiedzi
wizualne oznaczanie poprawnych i błędnych odpowiedzi
opóźnienie wysyłki formularza (animacje)
poprawę doświadczenia użytkownika
📌 Separacja logiki

Projekt jest podzielony na:

modele danych
logikę widoków
szablony HTML
logikę frontendową (JavaScript)
📁 Struktura projektu
🗄️ quiz/models.py

Definiuje strukturę bazy danych:

Question – pytania, odpowiedzi, poprawna odpowiedź, poziom trudności
PlayerScore – dane gracza, wynik, poziom trudności, data
🧠 quiz/views.py

Główna logika aplikacji:

start_quiz – inicjalizacja quizu i ustawienie sesji
question_view – obsługa pytań i aktualizacja wyniku
result_view – wyświetlenie wyników i zapis do bazy
🖥️ start.html
formularz rozpoczęcia quizu
dane gracza (imię, kraj, wiek, poziom trudności)
walidacja danych
responsywny interfejs
❓ question.html
wyświetlanie pytań
obsługa JavaScript
animacje odpowiedzi
blokada wielokrotnego wyboru
🏁 result.html
wynik końcowy
szczegółowe podsumowanie odpowiedzi
ranking graczy
podświetlenie aktualnego gracza
🌐 quiz/urls.py

Routing aplikacji:

start quizu
pytania
wyniki
⚙️ quiz/admin.py

Panel administracyjny Django:

zarządzanie pytaniami
zarządzanie wynikami
⚙️ settings.py

Konfiguracja Django:

aplikacje
middleware
baza danych SQLite
pliki statyczne
🗃️ db.sqlite3

Baza danych zawiera:

przykładowe pytania
przykładowe wyniki graczy
📦 requirements.txt

Zależności projektu (w tym Django)

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
🌐 Uruchomienie
Aplikacja: http://127.0.0.1:8000/
Panel admina: http://127.0.0.1:8000/admin/
📌 Dodatkowe informacje
logika quizu działa po stronie backendu (Django sessions)
JavaScript odpowiada tylko za UX
aplikacja działa na desktop i mobile
projekt ma charakter edukacyjny
🏁 Podsumowanie

Projekt przedstawia kompletną aplikację Django łączącą:

backend
bazę danych
sesje użytkownika
interaktywny frontend
