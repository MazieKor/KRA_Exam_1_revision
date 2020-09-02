![Coders-Lab-1920px-no-background](https://user-images.githubusercontent.com/152855/73064373-5ed69780-3ea1-11ea-8a71-3d370a5e7dd8.png)


### Zadanie 1 (4pkt)
 
1. Nazwa bazy danych to  `exam1`.
2. Utwórz tabelę o nazwie **students**.
Tabela ma zawierać następujące pola:
- id - typu INT - ma być kluczem głównym z atrybutem AUTO_INCREMENT,
- email - VARCHAR, długość 80 - z atrybutem UNIQUE,
- firstName - VARCHAR, długość 80,
- lastName - VARCHAR, długość 80.

3. Utwórz tabelę o nazwie **exercises**.
4. Tabela ma zawierać następujące pola:
- id - typu INT - ma być kluczem głównym z atrybutem AUTO_INCREMENT,
- title - VARCHAR, długość 80,
- points - INT,
- created - DATETIME,
- description - TEXT.
5. Stwórz relację wiele do wielu między tabelami `students` a `exercises`.
   Tabela łącząca ma się nazywać `student_exercises`. Klucze obce nazwij `student_id` i `exercise_id`. 
Tabela nie powinna zawierać własnego dodatkowego identyfikatora.
6. Zapytania umieść w zmiennych w pliku `Main01`. 

**Wywołaj wszystkie zapytania w metodzie `main` programu.**

### Zadanie 2 (4pkt)

Zapytania wpisz w odpowiednie zmienne w przygotowanym pliku `Main02.java`, np. `QUERY1`.

**Nie musisz wywoływać zapytań w kodzie Javy.**
     
1. Pobierz studenta, którego imię to `Jan` a nazwisko `Kowalski`.
2. Pobierz zadanie, które ma największą wartość atrybutu `points`.
3. Pobierz zadanie, którego tytuł rozpoczyna się od `W pli`.
4. Pobierz studentów, którzy mają przypisane przynajmniej jedno zadanie, jeżeli student ma przypisanych więcej zadań ma się pojawiać tylko raz.
5. Pobierz wszystkie dane o studentach oraz ilość przypisanych do nich zadań.
6. Pobierz trzech studentów, którzy mają przypisane zadania z sumaryczną największą ilością punktów, posortowaną od największej do najmniejszej.
7. Pobierz wszystkich studentów, którzy nie mają przypisanego żadnego zadania.
8. Pobierz wszystkie zadania, które zostały utworzone między **2020-01-01** a **2020-12-31**. 

### Zadanie 3 (3pkt)

Utwórz klasę `BaseEntity` - klasa ta będzie zawierać:
- id — typu `long`
- utwórz gettery i settery dla atrybutu `id` 
- konstruktor ustawiający `id`

1. Utwórz klasę `Book`, która dziedziczy po `BaseEntity`.
Klasa ta reprezentuje dane z tabeli `books` i zawiera prywatne pola:
  - `title` (String),
  - `author` (String),
  - `isbn` (String).
2. Utwórz gettery i settery do pól klasy.
3. Utwórz konstruktor przyjmujący wszystkie parametry oraz konstruktor bezparametrowy.
4. W konstruktorze przyjmującym wszystkie parametry wykorzystaj konstruktor klasy nadrzędnej.

### Zadanie 4 (4 pkt)

Dla tego zadania dostępne jest zapytanie tworzące tabelę:
```sql
CREATE TABLE `books` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(45) DEFAULT NULL,
  `author` varchar(45) DEFAULT NULL,
  `isbn` varchar(45) DEFAULT NULL,
PRIMARY KEY (id)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```
wczytaj zapytanie do bazy danych.

W pliku `Main04.java` napisz program, który spełni następujące założenia:

1. z linii komend pobierze następujące parametry:
  - `title` (String),
  - `author` (String),
  - `isbn` (String).
4. Zapisze te dane do bazy danych do tabeli `books`.

### Zadanie 5 (5pkt)

1. W `Main05.java` utwórz metodę o sygnaturze `public static Book[] getAllBooks()`.
2. W ciele metody pobierz wiersze z tabeli `books`, utwórz z nich obiekty typu `Book`. 
3. Kolejne wiersze dodawaj do tablicy, za każdym razem zwiększaj jej rozmiar.
4. Zwróć tak utworzoną tablicę.
