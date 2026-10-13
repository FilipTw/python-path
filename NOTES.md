<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>

---

<div align="center">

# Whetting Your Appetite

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Interpreter](https://img.shields.io/badge/język-interpretowany-3776AB?style=for-the-badge)

</div>

---

Python to język programowania, który daje wiele możliwości w perspektywie rozwoju na rok 2026+.

Pythona można używać w wielu obszarach m.in.:

> ⌲ Automatyzacji *(Selenium, Scrapy, Beautiful Soup, Playwright, ...)*
>
> ⌲ Aplikacji webowych *(Django, DRF, FastAPI, Flask, Reflex, ...)*
>
> ⌲ AI *(TensorFlow, PyTorch, Keras, Scikit-learn, Streamlit(Web UI ), Pydantic AI, ...)*
>
> ⌲ Analizy danych i Data science *(Pandas/Polars, NumPy, Matplotlib, Seaborn, ...)*
>
> ⌲ Programowania gier, aplikacji mobilnych i obszarów związanych z DevOps i administracją systemami ...

---

## Ważne pojęcia

---

### 1. Python jako język interpretowany

**a)** Interpreter jest podstawowym narzędziem umożliwiającym wykonywanie kodu w językach skryptowych.

**b)** Działa jak tłumacz symultaniczny – na bieżąco przekłada kod napisany przez człowieka na język "zer i jedynek", który rozumie komputer (tłumaczy kod źródłowy języka wysokiego poziomu na sekwencję instrukcji, które mogą być wykonane przez komputer w czasie rzeczywistym).

**c)** Interpreter vs Kompilator - interpreter nie generuje pliku binarnego, lecz odczytuje i wykonuje kod linia po linii.

> 💡 Wyobraź sobie, że kompilator to tłumacz, który najpierw przekłada całą książkę, a dopiero potem daje Ci gotowy tekst. Interpreter z kolei czyta i tłumaczy "na żywo", zdanie po zdaniu.
>
> Python korzysta właśnie z tego drugiego rozwiązania.
> Dlatego zrozumienie, jak działa ten "tłumacz na żywo", jest kluczem do pisania naprawdę szybkiego kodu w Pythonie.

---

#### Działanie Interpretera w Python'ie

Tak Python przetwarza Twój program od momentu jego uruchomienia:

| # | Etap | Opis |
|---|---|---|
| ☞ | **Dzielenie na słowa** *(Analiza leksykalna)* | Python tnie Twój kod na najmniejsze sensowne kawałki (tzw. tokeny). Oddziela od siebie komendy, nazwy zmiennych, liczby i nawiasy, żeby wiedzieć, z czym ma do czynienia. |
| ☞ | **Układanie mapy logiki** *(Analiza składniowa)* | Z tych małych kawałków tworzony jest schemat programu (drzewo AST). Na tym etapie Python uczy się zaleceń – np. rozumie, że konkretna grupa słów to pętla, a inna to definicja funkcji. |
| ☞ | **Tworzenie uniwersalnego półproduktu** *(Kompilacja do bytecode'u)* | Schemat programu jest tłumaczony na bytecode – wewnętrzny, uproszczony język Pythona. Dzięki temu Twój program zadziała na każdym komputerze, niezależnie od tego, czy to Windows, Mac, czy Linux. |
| ☞ | **Właściwe działanie** *(Wykonanie przez PVM)* | Do akcji wkracza "silnik" Pythona (czyli maszyna wirtualna PVM). Odczytuje on gotowy bytecode instrukcja po instrukcji i po prostu wykonuje Twoje polecenia, zarządzając przy tym pamięcią komputera. |

---

### 2. Python a wysoko-poziomowe typy danych

**❖ Zgadywanie typów "w locie":**

W Pythonie nie musisz z góry określać, czy zmienna przechowuje tekst, czy liczbę. Interpreter sam to rozpoznaje w trakcie działania programu i w razie potrzeby automatycznie dopasowuje formaty.

**❖ Automatyczne sprzątanie pamięci:**

Python sam dba o porządek w pamięci komputera. Działa to jak system "liczników popularności" – system liczy, w ilu miejscach w kodzie dany element jest używany. Gdy dany obiekt przestaje być komukolwiek potrzebny (licznik spada do zera), Python automatycznie go usuwa.

**❖ Radzenie sobie z zapętleniami:**

Czasami dwa niepotrzebne obiekty wskazują nawzajem na siebie. Python ma specjalny mechanizm (moduł gc), który wykrywa takie "zamknięte kółka" i też je usuwa, by nie blokowały pamięci.

**❖ Koszty wygody:**

Chociaż takie automatyczne rozpoznawanie typów jest wygodne i bezpieczne, może zwalniać działanie programu (szczególnie przy dużych ilościach danych). Dlatego Python stosuje w tle różne sztuczki optymalizacyjne – np. trzyma często używane rzeczy w szybkiej pamięci podręcznej.

---

### 3. Dodatkowe informacje

> **Zarządzanie funkcjami (Stos wywołań):** kiedy program uruchamia funkcję, dodaje ją na szczyt specjalnej listy (tzw. stosu). Każda funkcja otrzymuje tam swoją własną, odizolowaną przestrzeń na tymczasowe zmienne. Gdy skończy zadanie, jest natychmiast usuwana z listy, dzięki czemu jej dane są bezpieczne i nie mieszają się zresztą programu.

> **Ładowanie modułów:** Python doczytuje dodatkowe pliki z kodem w locie. Aby przyspieszyć ten proces w przyszłości, od razu tłumaczy je na szybszy format (pliki .pyc) i zachowuje w pamięci podręcznej. Dodatkowo każdy moduł działa w swojej własnej, zamkniętej strefie, co zapobiega konfliktom nazw (np. gdy dwie różne wtyczki mają funkcję o tej samej nazwie).

> **Obsługa błędów:** gdy w kodzie wystąpi niespodziewany błąd, Python zaczyna cofać się krok po kroku po wspomnianym "stosie wywołań". Szuka po drodze instrukcji ratunkowej (bloku try-except). Jeśli ją znajdzie, wykonuje plan awaryjny. Jeśli przeszuka wszystko i nic nie znajdzie – zatrzymuje program i wyświetla komunikat o błędzie.

---

## Ciekawostki

### Autorzy

> *" Swoją drogą, nazwa języka pochodzi od programu BBC „Latający Cyrk Monty Pythona" i nie ma nic wspólnego z gadami. Tworzenie odniesień do skeczy Monty Pythona w dokumentacji jest nie tylko dozwolone, wręcz do tego zachęcamy!"*

---

[![Obejrzyj demo](https://img.youtube.com/vi/EcgH1QPSiS4/maxresdefault.jpg)](https://www.youtube.com/watch?v=EcgH1QPSiS4)

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>

---

<div align="center">

# Using The Interpreter

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Interpreter](https://img.shields.io/badge/temat-interpreter-3776AB?style=for-the-badge)

</div>

---

Interpreter Pythona to „silnik", który czyta i uruchamia Twój kod. Wiedza o tym, jak go wywoływać i jak się zachowuje, jest fundamentem codziennej pracy z Pythonem.

---

## Ważne pojęcia

---

### 1. Wywoływanie Interpretera

**a)** Standardowe uruchomienie w terminalu:

```bash
python3.15         # Linux / macOS
py                 # Windows (launcher py.exe)
```

**b)** Zamknięcie interpretera:

| Skrót | System |
|---|---|
| `Ctrl + D` | Unix / macOS |
| `Ctrl + Z` | Windows |
| `quit()` | wszędzie |

**c)** Przydatne flagi wywołania:

| Składnia | Co robi |
|---|---|
| `python -c "kod"` | Wykonuje jednolinijkowy kod bez pliku |
| `python -m moduł` | Uruchamia moduł Pythona jak skrypt |
| `python -i skrypt.py` | Po wykonaniu skryptu wchodzi w tryb interaktywny |

> 💡 Flaga `-m` jest szczególnie użyteczna – np. `python -m http.server` uruchamia od razu wbudowany serwer HTTP bez pisania ani jednej linii kodu.

---

### 2. Przekazywanie argumentów (`sys.argv`)

**❖ Jak to działa:**

Gdy uruchamiasz skrypt z argumentami, Python pakuje je do listy `sys.argv` dostępnej po `import sys`.

```python
# uruchomienie: python skrypt.py hello world
import sys
print(sys.argv)   # ['skrypt.py', 'hello', 'world']
```

**❖ Zasady dotyczące `sys.argv[0]`:**

| Sposób uruchomienia | Wartość `sys.argv[0]` |
|---|---|
| Bez skryptu | `''` *(pusty string)* |
| `python skrypt.py` | `'skrypt.py'` |
| `python -` *(stdin)* | `'-'` |
| `python -c "kod"` | `'-c'` |
| `python -m moduł` | Pełna ścieżka do modułu |

> 💡 Argumenty podane **za** `-c` lub `-m` trafiają do `sys.argv`, ale **nie** są przetwarzane przez interpreter – to Twój kod je obsługuje.

---

### 3. Tryb interaktywny

**a)** Interpreter wchodzi w tryb interaktywny, gdy jest uruchamiany bez pliku – wtedy czyta komendy bezpośrednio z klawiatury.

**b)** Dwa rodzaje promptów:

| Prompt | Znaczenie |
|---|---|
| `>>>` | Gotowy na nową instrukcję |
| `...` | Oczekuje na kontynuację (np. ciało pętli lub bloku `if` lub inne) |

**c)** Przykład wieloliniowej konstrukcji:

```python
>>> the_world_is_flat = True
>>> if the_world_is_flat:
...     print("Uważaj, żeby nie spaść!")
...
Uważaj, żeby nie spaść!
```

> 💡 Tryb interaktywny świetnie sprawdza się do szybkiego testowania pomysłów i eksperymentowania z kodem – działa jak kalkulator dla programisty.

---

### 4. Kodowanie plików źródłowych

**❖ Domyślne kodowanie:**

Python domyślnie traktuje pliki `.py` jako **UTF-8**, co oznacza pełne wsparcie dla polskich znaków, emoji i znaków z większości języków świata.

**❖ Zmiana kodowania:**

Jeśli musisz użyć innego kodowania (np. przy starych plikach Windows), dodaj specjalny komentarz jako **pierwszą linię** pliku:

```python
# -*- coding: cp1252 -*-
```

**❖ Wyjątek – linia shebang:**

Gdy plik zaczyna się od shebangu (linia `#!`), deklaracja kodowania wędruje na **drugą** linię:

```python
#!/usr/bin/env python3
# -*- coding: cp1252 -*-
```

> 💡 W praktyce 2026+ rzadko zmienia się kodowanie – UTF-8 obsługuje wszystko. Wiedza o `# -*- coding: -*-` przydaje się głównie przy pracy ze starym kodem lub systemami legacy.

---

## Ciekawostki

### Skąd `>>>` jako prompt?

> Trzy znaki `>` nawiązują do tradycji uniksowych powłok. Podwójny `>>` w bashu oznacza dopisywanie do pliku – Python dodał trzeci, żeby się odróżnić. Ten sam symbol `>>>` zobaczysz w przykładach kodu w całej oficjalnej dokumentacji Pythona.
---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>


<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>



---

<div align="center">

# An Informal Introduction to Python

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Podstawy](https://img.shields.io/badge/poziom-podstawy-3776AB?style=for-the-badge)

</div>

---

Python potrafi działać jak prosty kalkulator, ale kryje w sobie znacznie więcej. Ten rozdział to solidny fundament — liczby, tekst, listy i pierwsza prawdziwa pętla.

Poznasz tutaj trzy kluczowe typy danych:

> ⌲ **Liczby** *(int, float, complex, Decimal, Fraction)*
>
> ⌲ **Tekst / Stringi** *(str — niemutowalny typ sekwencyjny)*
>
> ⌲ **Listy** *(list — mutowalny, wielofunkcyjny typ złożony)*

---

## Ważne pojęcia

---

### 1. Liczby

**a)** Python obsługuje kilka typów liczbowych: 
- `int` (całkowite), 
- `float` (zmiennoprzecinkowe), 
- `complex` (zespolone z sufiksem `j`), 
- a także `Decimal` i `Fraction` z biblioteki standardowej.

**b)** Dzielenie `/` **zawsze** zwraca `float`. 
- Do dzielenia całkowitego służy `//`, 
- reszta z dzielenia to `%`, 
- a potęgowanie to `**`.

**c)** W operacjach mieszanych (`int` z `float`) Python automatycznie rzutuje `int` na `float`.

> 💡 Wyobraź sobie, że `//` to dzielenie "na podłogę" — wynik jest zawsze zaokrąglony w dół do najbliższej liczby całkowitej.
>
> `17 // 3` daje `5`, bo `5 * 3 = 15`, a reszta `2` jest odrzucana.
> Operator `%` zwraca właśnie tę resztę.

---

#### Operatory liczbowe

| Operator | Działanie | Przykład | Wynik |
|----------|-----------|---------|-------|
| `+` `-` `*` | Podstawowa arytmetyka | `50 - 5*6` | `20` |
| `/` | Dzielenie (zawsze float) | `8 / 5` | `1.6` |
| `//` | Dzielenie całkowite | `17 // 3` | `5` |
| `%` | Reszta z dzielenia | `17 % 3` | `2` |
| `**` | Potęgowanie | `5 ** 2` | `25` |

---

#### Zmienna `_` w konsoli interaktywnej

W trybie interaktywnym `_` automatycznie przechowuje wynik ostatniej operacji:

```python
>>> price = 100.50
>>> price * 0.125
12.5625
>>> price + _      # _ = 12.5625
113.0625
>>> round(_, 2)
113.06
```

> ⚠️ Nie przypisuj do `_` ręcznie — stworzysz lokalną zmienną, która zablokuje to magiczne zachowanie.

---

### 2. Tekst (Stringi)

**a)** Stringi to typ `str` — niezmienialny (niemutowalny) ciąg znaków. 
Można je zapisać w `'...'` lub `"..."` — oba zapisy są równoważne.

**b)** Znaki specjalne jak `\n` (nowa linia) czy `\t` (tabulator) są interpretowane. 
Aby tego uniknąć, używa się **raw stringów** z przedrostkiem `r`.

**c)** Stringi obsługują indeksowanie i wycinanie (slicing) tak jak listy, ale **nie można ich modyfikować** — każda zmiana tworzy nowy string.


---

#### Tworzenie i formatowanie

```python
'spam eggs'              # pojedynczy cudzysłów
"Paris :)"               # podwójny cudzysłów — ten sam efekt
'Powiedzieli \'tak\'.'   # znak ucieczki \'
r'C:\this\name'          # raw string — \ nie jest interpretowany
```

#### Stringi wieloliniowe

```python
print("""\
Użycie: program [OPCJE]
     -h    Pomoc
     -v    Wersja
""")
```

#### Operacje na stringach

| Operacja | Przykład | Wynik |
|----------|---------|-------|
| Łączenie `+` | `'Py' + 'thon'` | `'Python'` |
| Powtarzanie `*` | `3 * 'un'` | `'ununun'` |
| Auto-łączenie literałów | `'Py' 'thon'` | `'Python'` |
| Długość | `len('Python')` | `6` |

#### Indeksowanie i slicing

```
 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
   0   1   2   3   4   5
  -6  -5  -4  -3  -2  -1
```

```python
word = 'Python'
word[0]    # → 'P'    pierwszy znak
word[-1]   # → 'n'    ostatni znak
word[0:2]  # → 'Py'   od 0 (włącznie) do 2 (wyłącznie)
word[2:]   # → 'thon' od 2 do końca
word[:2]   # → 'Py'   od początku do 2
```

> ⚠️ String jest **niemutowalny** — `word[0] = 'J'` wyrzuci `TypeError`. 
> Twórz nowy: `'J' + word[1:]`.

---

### 3. Listy

**a)** Lista (`list`) to najbardziej wszechstronny złożony typ danych w Pythonie. Przechowuje elementy różnych typów, oddzielone przecinkami, w nawiasach kwadratowych `[]`.

**b)** W przeciwieństwie do stringów — listy są **mutowalne**: można zmieniać, dodawać i usuwać elementy.

**c)** Przypisanie listy do zmiennej **nie kopiuje danych** — obie zmienne wskazują na ten sam obiekt w pamięci. Aby uzyskać kopię, użyj `lista[:]`.

> 💡 Lista to jak notatnik z ponumerowanymi stronami. Możesz dopisywać, wyrywać kartki i zamieniać ich zawartość. 
> String to natomiast wyryta w kamieniu inskrypcja — tylko do odczytu.

---

#### Podstawowe operacje

```python
squares = [1, 4, 9, 16, 25]

squares[0]          # → 1             indeksowanie
squares[-1]         # → 25            ostatni element
squares[-3:]        # → [9, 16, 25]   slicing — nowa lista
squares + [36, 49]  # → [1,4,...,49]  łączenie
len(squares)        # → 5             długość
```

#### Modyfikowanie list

```python
cubes = [1, 8, 27, 65, 125]
cubes[3] = 64           # zmiana elementu
cubes.append(216)       # dodanie na koniec
cubes[2:5] = ['C','D']  # zamiana przez slice
cubes[2:4] = []         # usunięcie przez slice
cubes[:] = []           # wyczyszczenie całej listy
```

#### Pułapka referencji

```python
rgb  = ["czerwony", "zielony", "niebieski"]
rgba = rgb           # ⚠️ to samo miejsce w pamięci!
rgba.append("alfa")
print(rgb)           # → ['czerwony', 'zielony', 'niebieski', 'alfa']

kopia = rgba[:]      # ✅ płytka kopia — niezależny obiekt
```

#### Zagnieżdżone listy

```python
a = ['a', 'b', 'c']
n = [1, 2, 3]
x = [a, n]
x[0][1]   # → 'b'
```

---

### 4. Pierwsze kroki w programowaniu

**a)** Pętla `while` wykonuje blok kodu tak długo, jak warunek pozostaje prawdziwy. Ciało pętli **musi być wcięte** — Python używa wcięć zamiast nawiasów klamrowych do grupowania kodu.

**b)** Wielokrotne przypisanie pozwala nadać wartości kilku zmiennym jednocześnie. Prawa strona jest zawsze obliczana w całości przed przypisaniem.

**c)** Funkcja `print()` przyjmuje wiele argumentów i domyślnie kończy wypisywanie znakiem nowej linii. Można to zmienić argumentem `end=`.

> 💡 Wcięcia w Pythonie to nie kwestia estetyki — to składnia. Blok kodu należący do pętli lub warunku **musi** być wcięty o tę samą liczbę spacji. Brak wcięcia = `IndentationError`.

---

#### Przykład: Ciąg Fibonacciego

```python
a, b = 0, 1          # wielokrotne przypisanie
while a < 10:        # pętla while
    print(a)         # ciało pętli — wcięte!
    a, b = b, a + b  # zamiana wartości (prawa strona obliczana najpierw)
```

**Wynik:** `0 1 1 2 3 5 8`

#### Operatory porównania

| Operator | Znaczenie |
|----------|-----------|
| `<` | mniejsze niż |
| `>` | większe niż |
| `==` | równe |
| `<=` | mniejsze lub równe |
| `>=` | większe lub równe |
| `!=` | różne |

#### `print()` z argumentem `end`

```python
while a < 1000:
    print(a, end=',')
    a, b = b, a + b
# → 0,1,1,2,3,5,8,13,21,34,55,89,...
```

---

## Ciekawostki

### Tryb interaktywny

> *"Interpreter Pythona działa jak kalkulator na sterydach — wpisujesz wyrażenie, natychmiast widzisz wynik. 
> Zmienna `_` automatycznie zapamiętuje ostatnią wartość, więc możesz budować obliczenia krok po kroku bez przypisywania czegokolwiek do zmiennych."*


---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>


<div align="center">

# Control Flow

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Flow](https://img.shields.io/badge/temat-control--flow-3776AB?style=for-the-badge)

</div>

---

## 🐍  Instrukcja `if` 

> Jedna z podstawowych konstrukcji sterujących przepływem programu w języku Python.

---

### 📌 Czym jest instrukcja `if`?

Instrukcja `if` pozwala wykonać określony blok kodu **tylko wtedy**, gdy spełniony jest podany warunek. To fundament logiki warunkowej — bez niej programy działałyby zawsze tak samo, niezależnie od danych wejściowych.

---

### 🧩 Składnia 

```python
if warunek:
    # kod wykonywany gdy warunek jest prawdziwy
elif inny_warunek:
    # kod wykonywany gdy inny_warunek jest prawdziwy
else:
    # kod wykonywany gdy żaden warunek nie jest spełniony
```

|Element|Wymagany?|Opis|
|---|:-:|---|
|`if`|✅ Tak|Główny warunek — zawsze wymagany|
|`elif`|❌ Nie|Dodatkowe warunki — można dodać dowolną ich liczbę|
|`else`|❌ Nie|Gałąź domyślna — wykonywana gdy nic nie pasuje|

---

### 💡 Przykład praktyczny

```python
x = int(input("Wprowadź liczbę całkowitą: "))

if x < 0:
    x = 0
    print('Wartość ujemna zmieniona na zero')
elif x == 0:
    print('Zero')
elif x == 1:
    print('Jeden')
else:
    print('Więcej niż jeden')
```

#### ▶️ Przykładowe wyniki

```
Wprowadź liczbę całkowitą: -5   →   Wartość ujemna zmieniona na zero
Wprowadź liczbę całkowitą: 0    →   Zero
Wprowadź liczbę całkowitą: 1    →   Jeden
Wprowadź liczbę całkowitą: 42   →   Więcej niż jeden
```

---

### 🔑 Kluczowe informacje

#### Słowo kluczowe `elif`

`elif` to skrót od **else if**. Jego użycie:

- ✔️ poprawia **czytelność** kodu
- ✔️ eliminuje **nadmierne zagnieżdżanie** wcięć
- ✔️ zastępuje instrukcje `switch` / `case` znane z innych języków

#### Porównanie z innymi językami

```
Java / C++ / C#          Python
─────────────────        ──────────────────
switch (x) {             if x == 1:
  case 1: ...                ...
  case 2: ...            elif x == 2:
  default: ...               ...
}                        else:
                             ...
```

---

## 🔁 Instrukcja `for`

> Iteruj po elementach dowolnej sekwencji — prosto, czytelnie i po pythonowemu.

---

### 📌 Czym jest instrukcja `for` w Pythonie?

Instrukcja `for` w Pythonie działa **inaczej** niż jej odpowiedniki w C czy Pascalu:

|Język|Sposób działania|
|---|---|
|**Pascal**|Iteracja od liczby do liczby|
|**C**|Ręczna kontrola kroku i warunku zakończenia|
|**Python**|✅ Iteracja po **elementach sekwencji** w ich naturalnej kolejności|

Python nie wymaga liczników ani indeksów — pętla przechodzi po kolejnych elementach listy, łańcucha znaków lub innej sekwencji, tak jak są one ułożone.

---

### 🧩 Składnia

```python
for zmienna in sekwencja:
    # kod wykonywany dla każdego elementu
```

---

### 💡 Przykład podstawowy

```python
# Zmierz długość kilku napisów
words = ['kot', 'okienko', 'defenestracja']

for w in words:
    print(w, len(w))
```

#### ▶️ Wynik

```
kot             3
okienko         7
defenestracja  13
```

---

### ⚠️ Modyfikowanie kolekcji podczas iteracji

Zmiana kolekcji **w trakcie** iterowania po niej może prowadzić do nieoczekiwanych błędów i trudnych do wykrycia bugów.

```python
# ❌ Niebezpieczne — modyfikacja kolekcji podczas iteracji
for user, status in users.items():
    if status == 'nieaktywny':
        del users[user]  # RuntimeError: dictionary changed size during iteration
```

#### ✅ Dwie bezpieczne strategie

```python
users = {
    'Hans':     'aktywny',
    'Éléonore': 'nieaktywny',
    '景太郎':    'aktywny'
}
```

---

#### 🔹 Strategia 1 — Iteracja po kopii kolekcji

```python
for user, status in users.copy().items():
    if status == 'nieaktywny':
        del users[user]

# Wynik: users zawiera tylko aktywnych użytkowników
```

> `users.copy()` tworzy płytką kopię słownika — oryginał można bezpiecznie modyfikować, bo iterujemy po kopii.

---

#### 🔹 Strategia 2 — Budowanie nowej kolekcji

```python
active_users = {}

for user, status in users.items():
    if status == 'aktywny':
        active_users[user] = status

# Wynik: active_users = {'Hans': 'aktywny', '景太郎': 'aktywny'}
```

> Zamiast usuwać elementy ze starej kolekcji, budujemy nową — to podejście jest zazwyczaj **czytelniejsze i bezpieczniejsze**.

---

### ⚡ Porównanie strategii

|Kryterium|Kopia (`.copy()`)|Nowa kolekcja|
|---|---|---|
|Modyfikuje oryginał|✅ Tak|❌ Nie|
|Zużycie pamięci|Umiarkowane|Nieco wyższe|
|Czytelność|Dobra|✅ Bardzo dobra|
|Ryzyko błędów|Niskie|✅ Minimalne|

---
## 🔢  Funkcja `range()`

> Generuj sekwencje liczb bez zużywania pamięci — wydajnie i elegancko.

---

### 📌 Czym jest `range()`?

`range()` to wbudowana funkcja Pythona służąca do generowania **ciągów arytmetycznych**. Jest niezbędna wszędzie tam, gdzie trzeba iterować po sekwencji liczb — bez ręcznego tworzenia list.

---

### 🧩 Składnia

```python
range(stop)
range(start, stop)
range(start, stop, step)
```

|Parametr|Opis|Domyślnie|
|---|---|---|
|`start`|Pierwsza wartość sekwencji|`0`|
|`stop`|Wartość końcowa — **nie jest włączona**|wymagany|
|`step`|Krok (może być ujemny)|`1`|

> ⚠️ **Ważne:** punkt końcowy (`stop`) nigdy nie należy do generowanej sekwencji.

---

### 💡 Przykłady użycia

#### 🔹 Podstawowe użycie

```python
for i in range(5):
    print(i)
```

```
0  1  2  3  4
```

`range(5)` generuje dokładnie **5 wartości** — poprawne indeksy dla sekwencji o długości 5.

---

#### 🔹 Własny punkt startowy

```python
list(range(5, 10))
```

```
[5, 6, 7, 8, 9]
```

---

#### 🔹 Własny krok

```python
list(range(0, 10, 3))   # co 3
```

```
[0, 3, 6, 9]
```

---

#### 🔹 Krok ujemny (odliczanie wstecz)

```python
list(range(-10, -100, -30))
```

```
[-10, -40, -70]
```

---

### 🔗 `range()` + `len()` — iteracja po indeksach

```python
a = ['Wyszły', 'w', 'pole', 'kurki', 'trzy']

for i in range(len(a)):
    print(i, a[i])
```

```
0 Wyszły
1 w
2 pole
3 kurki
4 trzy
```

> 💡 W większości przypadków zamiast `range(len(...))` wygodniej jest użyć wbudowanej funkcji `enumerate()` — opisanej szczegółowo w rozdziale **Techniki pętli**.

---

### 🧠 `range()` to nie lista — to iterable

Wydrukowanie zakresu daje zaskakujący wynik:

```python
print(range(10))
```

```
range(0, 10)
```

`range()` **nie tworzy listy** — zwraca specjalny obiekt, który generuje kolejne wartości **na żądanie**, podczas iteracji. Dzięki temu:

- ✅ nie zajmuje pamięci proporcjonalnie do rozmiaru sekwencji
- ✅ działa wydajnie nawet dla bardzo dużych zakresów
- ✅ nadaje się wszędzie tam, gdzie wymagany jest **iterable**

Aby otrzymać prawdziwą listę, wystarczy jawna konwersja:

```python
list(range(5))   # [0, 1, 2, 3, 4]
```

---

### 🔄 Co to jest iterable?

**Iterable** to dowolny obiekt, z którego można pobierać kolejne elementy aż do wyczerpania. Instrukcja `for` oraz wiele funkcji wbudowanych przyjmuje iterable jako argument:

```python
sum(range(4))   # 0 + 1 + 2 + 3
```

```
6
```

|Konstrukcja / Funkcja|Przyjmuje iterable|
|---|---|
|`for`|✅|
|`sum()`|✅|
|`list()`|✅|
|`min()` / `max()`|✅|
|`enumerate()`|✅|

---
## ⛔ Instrukcje `break` i `continue`

> Przejmij pełną kontrolę nad przepływem pętli — zatrzymaj ją lub przeskocz do następnej iteracji.

---

### 📌 Przegląd

|Instrukcja|Działanie|
|---|---|
|`break`|**Przerywa** pętlę natychmiast i wychodzi z niej całkowicie|
|`continue`|**Pomija** resztę bieżącej iteracji i przechodzi do następnej|

Obie instrukcje działają na **najbardziej wewnętrznej** aktywnej pętli `for` lub `while`.

---

### ⛔ Instrukcja `break`

Używana gdy znalezienie danego elementu sprawia, że dalsza iteracja jest zbędna — np. przy wyszukiwaniu lub sprawdzaniu warunków.

```python
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(f"{n} równa się {x} * {n//x}")
            break  # ← przerywa wewnętrzną pętlę po pierwszym znalezieniu dzielnika
```

#### ▶️ Wynik

```
4 równa się 2 * 2
6 równa się 2 * 3
8 równa się 2 * 4
9 równa się 3 * 3
```

> 💡 Pętla zewnętrzna (`for n`) działa dalej — `break` przerywa tylko tę pętlę, w której się bezpośrednio znajduje.

#### 🔍 Jak to działa krok po kroku?

```
n=4 → sprawdzamy x=2 → 4 % 2 == 0 → BREAK  ✅ znaleziono dzielnik
n=5 → sprawdzamy x=2 → 5 % 2 != 0
      sprawdzamy x=3 → 5 % 3 != 0
      sprawdzamy x=4 → 5 % 4 != 0 → brak break (5 jest pierwsze)
n=6 → sprawdzamy x=2 → 6 % 2 == 0 → BREAK  ✅ znaleziono dzielnik
...
```

---

### ⏭️ Instrukcja `continue`

Używana gdy chcemy **pominąć** pewne elementy, ale kontynuować pętlę dla pozostałych.

```python
for num in range(2, 10):
    if num % 2 == 0:
        print(f"Znaleziono liczbę parzystą {num}")
        continue  # ← pomija print poniżej dla liczb parzystych
    print(f"Znaleziono liczbę nieparzystą {num}")
```

#### ▶️ Wynik

```
Znaleziono liczbę parzystą   2
Znaleziono liczbę nieparzystą 3
Znaleziono liczbę parzystą   4
Znaleziono liczbę nieparzystą 5
Znaleziono liczbę parzystą   6
Znaleziono liczbę nieparzystą 7
Znaleziono liczbę parzystą   8
Znaleziono liczbę nieparzystą 9
```

> 💡 `continue` sprawia, że dla liczb parzystych Python **nie wykonuje** instrukcji `print(f"Znaleziono liczbę nieparzystą...")` — wraca od razu na początek pętli.

---

### ⚖️ Porównanie `break` vs `continue`

```
Pętla iteruje po elementach [A, B, C, D, E]:

─────────────────────────────────────────────────
Bez instrukcji:   A → B → C → D → E  (koniec)

break przy C:     A → B → [STOP]
                           ↑ wychodzi z pętli

continue przy C:  A → B → (pomija C) → D → E
                                ↑ wraca na start pętli
─────────────────────────────────────────────────
```

---

### ⚠️ Pułapki i dobre praktyki

|Sytuacja|Zalecenie|
|---|---|
|`break` w zagnieżdżonych pętlach|Przerywa tylko **wewnętrzną** — zewnętrzna działa dalej|
|Zbyt wiele `break` / `continue`|Może utrudnić czytanie kodu — rozważ refaktoryzację|
|`continue` jako pierwsza instrukcja w pętli|Zbędne — warunek można odwrócić w `if`|

---

## 🔚 Klauzula `else` w pętlach

> Mało znana, a niezwykle przydatna — `else` w pętli wykonuje się tylko wtedy, gdy `break` nigdy nie zadziałał.

---

### 📌 Czym jest `else` w pętli?

Zarówno pętla `for`, jak i `while` mogą posiadać opcjonalną klauzulę `else`. Jej działanie jest proste:

|Sytuacja|Czy `else` się wykona?|
|---|:-:|
|Pętla zakończyła się naturalnie|✅ Tak|
|Pętla przerwana przez `break`|❌ Nie|
|Pętla przerwana przez `return`|❌ Nie|
|Pętla przerwana przez wyjątek|❌ Nie|

---

### 🧩 Składnia

#### Pętla `for`

```python
for element in sekwencja:
    if warunek:
        break
else:
    # wykona się tylko jeśli pętla NIE została przerwana przez break
```

#### Pętla `while`

```python
while warunek:
    if inny_warunek:
        break
else:
    # wykona się gdy warunek pętli stał się fałszywy (bez break)
```

---

### 💡 Przykład — szukanie liczb pierwszych

```python
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(n, 'równa się', x, '*', n//x)
            break
    else:
        # wewnętrzna pętla przeszła całość nie znajdując dzielnika
        print(n, 'jest liczbą pierwszą')
```

> ⚠️ **Uwaga na wcięcia!** Klauzula `else` należy do pętli `for`, **nie** do instrukcji `if`.

#### ▶️ Wynik

```
2 jest liczbą pierwszą
3 jest liczbą pierwszą
4 równa się 2 * 2
5 jest liczbą pierwszą
6 równa się 2 * 3
7 jest liczbą pierwszą
8 równa się 2 * 4
9 równa się 3 * 3
```

---

### 🔍 Jak to działa krok po kroku?

```
n=2 → wewnętrzna pętla pusta → brak break → ELSE ✅ → "2 jest liczbą pierwszą"
n=3 → x=2: 3%2≠0 → koniec bez break → ELSE ✅ → "3 jest liczbą pierwszą"
n=4 → x=2: 4%2==0 → BREAK ⛔ → else pominięte → "4 równa się 2 * 2"
n=5 → x=2,3,4: brak dzielnika → ELSE ✅ → "5 jest liczbą pierwszą"
...
```

---

### 🧠 Jak o tym myśleć?

Klauzula `else` przy pętli działa analogicznie do klauzuli `else` przy instrukcji `try`:

```
Instrukcja try:
    try:      → wykonaj kod
    except:   → gdy wystąpił wyjątek
    else:     → gdy NIE wystąpił wyjątek      ← analogia

Pętla for/while:
    for/while → wykonaj iteracje
    break     → gdy znaleziono / warunek spełniony
    else:     → gdy NIE użyto break           ← to samo myślenie
```

Można też wyobrazić sobie działanie pętli jako wielokrotne `if/if/if/…/else`:

```
Iteracja 1: if warunek → break
Iteracja 2: if warunek → break
Iteracja 3: if warunek → break
...
(żaden if nie zadziałał) → else ✅
```

---

### ⚖️ `else` w pętli vs `else` w `if`

Choć słowo kluczowe jest to samo, semantyka jest zupełnie inna:

|Konstrukcja|`else` wykonuje się gdy…|
|---|---|
|`if / else`|warunek `if` był **fałszywy**|
|`for / else`|pętla **nie** została przerwana przez `break`|
|`try / else`|**nie** wystąpił żaden wyjątek|

---

### ✅ Kiedy używać `else` w pętli?

Klauzula `else` przy pętli jest szczególnie przydatna gdy:

- 🔍 **szukasz** czegoś w sekwencji i chcesz wiedzieć, czy wyszukiwanie zakończyło się sukcesem
- ✔️ **walidacja** — sprawdzasz, czy wszystkie elementy spełniają warunek
- 🔢 **algorytmy matematyczne** — np. sprawdzanie pierwszości, jak w przykładzie powyżej

---
## 🤫 Instrukcja `pass`

> Nic nie rób — ale zrób to składniowo poprawnie.

---

### 📌 Czym jest `pass`?

`pass` to instrukcja, która **dosłownie nic nie robi**. Służy jako wypełniacz syntaktyczny — wszędzie tam, gdzie Python wymaga obecności instrukcji, ale program nie wymaga żadnego działania.

```python
pass  # Python widzi instrukcję, akceptuje ją i... idzie dalej
```

---

### 🧩 Kiedy używać `pass`?

|Przypadek użycia|Opis|
|---|---|
|Aktywne oczekiwanie|Pętla nieskończona czekająca na zdarzenie zewnętrzne|
|Pusta klasa|Minimalna definicja klasy jako punkt startowy|
|Placeholder funkcji|Szkielet kodu do późniejszej implementacji|
|Pusty warunek / blok|Tymczasowe zignorowanie gałęzi logicznej|

---

### 💡 Przykłady użycia

#### 🔹 Aktywne oczekiwanie w pętli

```python
while True:
    pass  # Aktywne oczekiwanie na przerwanie z klawiatury (Ctrl+C)
```

> ⚠️ Pętla nieskończona z `pass` zużywa 100% CPU — stosuj tylko gdy celowo czekasz na sygnał zewnętrzny (np. `KeyboardInterrupt`).

---

#### 🔹 Minimalna definicja klasy

```python
class MyEmptyClass:
    pass
```

Przydatne gdy chcesz zdefiniować klasę jako **punkt startowy** lub **marker typu** — bez implementacji metod.

---

#### 🔹 Placeholder dla funkcji

```python
def initlog(*args):
    pass   # Pamiętaj, aby to zaimplementować!
```

Pozwala pisać kod na **wyższym poziomie abstrakcji** — najpierw definiujesz strukturę, potem wypełniasz szczegóły. Python zaakceptuje taką funkcję i nie zgłosi błędu.

---

### ✏️ Alternatywa — wielokropek `...`

W roli placeholdera coraz częściej spotyka się literał **wielokropka** (`Ellipsis`):

```python
def initlog(*args):
    ...   # konwencjonalny odpowiednik pass jako placeholder
```

#### Porównanie `pass` vs `...`

|Cecha|`pass`|`...`|
|---|---|---|
|Część definicji języka|✅ Tak|⚠️ Nie (stałe wyrażenie)|
|Użycie jako placeholder|✅ Tak|✅ Tak (konwencja)|
|Czytelność intencji|Neutralna|Sugeruje "do uzupełnienia"|
|Użycie w type hints / stubbach|Rzadko|✅ Standardowe (pliki `.pyi`)|

> 💡 Oba są akceptowane przez Pythona — wybór to kwestia stylu i konwencji zespołu. `...` bywa czytelniejszy jako sygnał "tu jeszcze nic nie ma".

---

### 🔍 `pass` vs inne puste konstrukcje

```python
# pass — nic nie zwraca, nic nie robi
def f():
    pass
print(f())   # None

# ... — też nic nie robi jako instrukcja
def g():
    ...
print(g())   # None

# Funkcja bez ciała → SyntaxError!
def h():
# ↑ IndentationError: expected an indented block
```

---

### ✅ Dobre praktyki

- Zostaw komentarz przy `pass` — np. `# TODO: zaimplementować` — żeby intencja była jasna
- Preferuj `...` w plikach `.pyi` (type stubs) — to tam jest standardem
- Unikaj `pass` w finalnym kodzie produkcyjnym — jego obecność zazwyczaj sygnalizuje niezakończoną pracę

---
## 🎯  Instrukcja `match`

> Pattern matching — sprawdzaj nie tylko **czy** coś pasuje, ale też **co** w tym jest.

---

### 📌 Zacznijmy od podstaw — po co w ogóle `match`?

Wyobraź sobie, że dostajesz kod błędu HTTP i chcesz wyświetlić odpowiedni komunikat. Możesz to zrobić przez `if`:

```python
if status == 400:
    return "Niewłaściwe żądanie"
elif status == 404:
    return "Nie znaleziono"
elif status == 418:
    return "Jestem czajniczkiem"
else:
    return "Coś jest nie tak z internetem"
```

`match` robi dokładnie to samo — ale czytelniej i z dużo większymi możliwościami:

```python
match status:
    case 400:
        return "Niewłaściwe żądanie"
    case 404:
        return "Nie znaleziono"
    case 418:
        return "Jestem czajniczkiem"
    case _:
        return "Coś jest nie tak z internetem"
```

#### Jak to działa?

```
match status:          ← "weź tę wartość..."
    case 400:          ← "...czy to 400?"  → tak → wykonaj i STOP
    case 404:          ← "...czy to 404?"  → tak → wykonaj i STOP
    case _:            ← "cokolwiek innego" → zawsze pasuje
```

> ✅ **Wykonywany jest tylko pierwszy pasujący wzorzec** — reszta jest pomijana.  
> ✅ `_` to **dzika karta** — pasuje do wszystkiego, ale niczego nie zapamiętuje.

---

### 🔗 Łączenie kilku wartości w jeden `case`

Zamiast pisać dwa bloki `case` z tym samym kodem, połącz je operatorem `|`:

```python
# Zamiast tego:
case 401:
    return "Niedozwolone"
case 403:
    return "Niedozwolone"
case 404:
    return "Niedozwolone"

# Napisz tak:
case 401 | 403 | 404:
    return "Niedozwolone"
```

---

### 📦 Wzorce sekwencji — wyciąganie wartości ze środka

Tu zaczyna się magia. `match` potrafi nie tylko sprawdzić **czy** coś pasuje, ale też **wyciągnąć wartości ze środka** dopasowanego obiektu.

Wyobraź sobie punkt na płaszczyźnie zapisany jako para `(x, y)`:

```python
match point:
    case (0, 0):
        print("Początek układu współrzędnych")
    case (0, y):
        print(f"Na osi Y, y wynosi {y}")
    case (x, 0):
        print(f"Na osi X, x wynosi {x}")
    case (x, y):
        print(f"Gdzieś na płaszczyźnie: X={x}, Y={y}")
    case _:
        raise ValueError("To nie jest punkt!")
```

#### Co się tu dzieje krok po kroku?

```
point = (0, 5)

case (0, 0)  → czy to (0, 0)?           → NIE (drugi element to 5)
case (0, y)  → czy pierwszy element to 0? → TAK
               → y = 5                  ✅ DOPASOWANO
               → wypisuje: "Na osi Y, y wynosi 5"
```

```
point = (3, 7)

case (0, 0)  → NIE
case (0, y)  → NIE (pierwszy element to 3, nie 0)
case (x, 0)  → NIE (drugi element to 7, nie 0)
case (x, y)  → TAK → x = 3, y = 7      ✅ DOPASOWANO
               → wypisuje: "Gdzieś na płaszczyźnie: X=3, Y=7"
```

> 💡 **Kluczowa zasada:** samodzielna nazwa we wzorcu (jak `x` lub `y`) to **zmienna, która przechwyci wartość**. Literał (jak `0`) to **konkretna wartość do sprawdzenia**.

---

### 🏗️ Wzorce klas — dopasowywanie obiektów

Jeśli używasz klas do reprezentowania danych, `match` potrafi dopasować **typ obiektu** i jednocześnie **wyciągnąć jego atrybuty**:

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

def where_is(point):
    match point:
        case Point(x=0, y=0):
            print("Początek")
        case Point(x=0, y=y):
            print(f"Na osi Y, y={y}")
        case Point(x=x, y=0):
            print(f"Na osi X, x={x}")
        case Point():
            print("Jakiś inny punkt")
        case _:
            print("To nie jest punkt")
```

#### Jak czytać `case Point(x=0, y=y):`?

```
Point(...)    ← czy obiekt jest klasy Point?
x=0           ← czy atrybut x wynosi dokładnie 0?
y=y           ← jeśli tak, przypisz atrybut y do zmiennej y
```

#### Zapis pozycyjny — skrót dzięki `__match_args__`

Żeby nie pisać `x=`, `y=` za każdym razem, zdefiniuj kolejność atrybutów w klasie:

```python
class Point:
    __match_args__ = ('x', 'y')   # ← definiuje kolejność pozycyjną
    def __init__(self, x, y):
        self.x = x
        self.y = y
```

Wtedy wszystkie poniższe wzorce są **równoważne** — każdy przechwytuje `y` do zmiennej `var`:

```python
Point(1, var)        # pozycyjnie: x=1, y=var
Point(1, y=var)      # mix: pozycyjny + nazwany
Point(x=1, y=var)    # czysto nazwany
Point(y=var, x=1)    # kolejność nie ma znaczenia
```

---

### 🧱 Wzorce zagnieżdżone — wzorce wewnątrz wzorców

Wzorce można dowolnie łączyć i zagnieżdżać. Poniżej `match` dopasowuje **listę obiektów Point**:

```python
class Point:
    __match_args__ = ('x', 'y')
    def __init__(self, x, y):
        self.x = x
        self.y = y

match points:
    case []:
        print("Brak punktów")
    case [Point(0, 0)]:
        print("Jeden punkt — w początku układu")
    case [Point(x, y)]:
        print(f"Jeden punkt: ({x}, {y})")
    case [Point(0, y1), Point(0, y2)]:
        print(f"Dwa punkty na osi Y: {y1} i {y2}")
    case _:
        print("Coś innego")
```

Każdy `case` opisuje inną **strukturę** listy — nie tylko jej zawartość:

```
[]                        ← pusta lista
[Point(0, 0)]             ← lista z jednym punktem w początku
[Point(x, y)]             ← lista z dokładnie jednym dowolnym punktem
[Point(0, y1), Point(0, y2)] ← lista z dokładnie dwoma punktami na osi Y
```

---

### 🛡️ Guard — dodatkowy warunek z `if`

Czasem sam wzorzec nie wystarczy — chcesz dopasować strukturę, ale tylko jeśli spełniony jest dodatkowy warunek logiczny. Służy do tego klauzula `if` zwana **guardem**:

```python
match point:
    case Point(x, y) if x == y:
        print(f"Punkt leży na przekątnej: ({x}, {y})")
    case Point(x, y):
        print(f"Punkt poza przekątną: ({x}, {y})")
```

#### Kolejność działania

```
1. Sprawdź wzorzec → czy to Point z dwoma wartościami?
2. Jeśli tak       → przypisz x i y ze środka obiektu
3. Sprawdź guard   → czy x == y?
4. Jeśli NIE       → odrzuć dopasowanie, idź do następnego case
```

> ⚠️ Zmienne są przypisywane **przed** sprawdzeniem guarda. Jeśli guard jest fałszywy, wartości są odrzucane i szukanie trwa dalej.

---

### 🗺️ Wzorce słownikowe — dopasowywanie po kluczach

`match` potrafi dopasowywać słowniki i wyciągać konkretne klucze:

```python
match config:
    case {"tryb": "debug", "poziom": poziom}:
        print(f"Tryb debug, poziom: {poziom}")
    case {"tryb": "produkcja"}:
        print("Tryb produkcji")
    case _:
        print("Nieznana konfiguracja")
```

Ważna różnica: słownik może zawierać **więcej kluczy** niż wzorzec — nadmiarowe są po prostu **ignorowane**. W sekwencjach tak nie jest:

|Cecha|Sekwencja (`[]`, `()`)|Słownik (`{}`)|
|---|---|---|
|Nadmiarowe elementy|❌ Wzorzec nie pasuje|✅ Są ignorowane|
|Rozpakowywanie reszty|`*rest`|`**rest`|
|Kolejność|Ma znaczenie|Nie ma znaczenia|

```python
# Przechwycenie pozostałych kluczy do zmiennej
case {"bandwidth": b, **rest}:
    print(f"Bandwidth: {b}, reszta konfiguracji: {rest}")
```

---

### 🏷️ Przechwytywanie podwzorców — słowo kluczowe `as`

Chcesz dopasować wzorzec i jednocześnie zachować całą dopasowaną wartość w zmiennej? Użyj `as`:

```python
match dane:
    case (Point(x1, y1), Point(x2, y2) as drugi_punkt):
        print(f"Drugi punkt jako obiekt: {drugi_punkt}")
        print(f"Jego współrzędne: x={x2}, y={y2}")
```

Czytaj to jako: _„dopasuj parę dwóch punktów, wyciągnij współrzędne z obu, a cały drugi punkt zapisz dodatkowo jako `drugi_punkt`"_.

---

### 🎨 Stałe i Enum — uważaj na nazwy!

`match` traktuje **samodzielne nazwy** jako zmienne do przechwycenia, nie jako stałe. Żeby użyć nazwanej stałej (np. z Enum), musisz napisać ją **z kropką**:

```python
from enum import Enum

class Color(Enum):
    RED = 'red'
    GREEN = 'green'
    BLUE = 'blue'

match color:
    case Color.RED:            # ✅ z kropką = stała Enum
        print("Widzę czerwone!")
    case Color.GREEN:
        print("Zielono mi")
    case Color.BLUE:
        print("Niebo jest niebieskie")
```

> ❌ **Pułapka:** gdybyś napisał `case RED:` (bez `Color.`), Python potraktowałby `RED` jako zmienną — wzorzec **zawsze** by pasował i przechwytywał wartość, nigdy nie sprawdzając czy to rzeczywiście czerwony!

---

### 🔁 Rozpakowywanie reszty sekwencji — `*rest`

Wzorzec sekwencji obsługuje gwiazdkę `*` tak samo jak przy rozpakowywaniu list:

```python
match punkty:
    case [pierwszy, *reszta]:
        print(f"Pierwszy: {pierwszy}")
        print(f"Pozostałe: {reszta}")

    case [pierwszy, drugi, *_]:   # *_ ignoruje resztę bez przypisania
        print("Mamy co najmniej dwa punkty")
```

---

### ⚠️ Rzeczy, o których łatwo zapomnieć

```python
# ✅ Z kropką = stała, sprawdzana przez tożsamość
case Color.RED:

# ❌ Bez kropki = zmienna — ZAWSZE pasuje i przechwytuje wartość!
case RED:

# ✅ Wzorce sekwencji działają dla list i krotek
case [x, y]:        # pasuje do [1, 2] i (1, 2)

# ❌ Ale NIE dla łańcuchów znaków ani iteratorów
# "ab" NIE pasuje do case [x, y]:

# ✅ True, False, None porównywane są przez TOŻSAMOŚĆ
case True:          # pasuje tylko do True, nie do 1
case None:          # pasuje tylko do None
```

---

### 📋 Ściąga — wszystkie rodzaje wzorców

| Typ wzorca           | Przykład                 | Co robi                                          |
| -------------------- | ------------------------ | ------------------------------------------------ |
| **Literał**          | `case 404:`              | Sprawdza równość wartości                        |
| **Alternatywa**      | `case 401 \| 403:`       | Pasuje do jednej z kilku wartości                |
| **Dzika karta**      | `case _:`                | Zawsze pasuje, nic nie przypisuje                |
| **Zmienna**          | `case x:`                | Zawsze pasuje, przypisuje wartość do `x`         |
| **Sekwencja**        | `case (0, y):`           | Rozpakowuje krotkę/listę, wyciąga elementy       |
| **Klasa**            | `case Point(x=0, y=y):`  | Sprawdza typ i wyciąga atrybuty                  |
| **Guard**            | `case (x, y) if x == y:` | Dodaje warunek logiczny do wzorca                |
| **Słownik**          | `case {"klucz": val}:`   | Wyciąga wartości ze słownika (reszta ignorowana) |
| **Przechwycenie**    | `case Point(...) as p:`  | Wiąże cały dopasowany obiekt do zmiennej         |
| **Stała (Enum)**     | `case Color.RED:`        | Porównuje przez tożsamość, nie równość           |
| **Reszta sekwencji** | `case [x, *rest]:`       | Przechwytuje pozostałe elementy listy            |

---
## 🧩 Funkcja

> Funkcja to nazwany blok kodu, który możesz wywołać wielokrotnie — z różnymi danymi, za każdym razem.

---

### 📌 Zacznijmy od przykładu

Napiszmy funkcję, która wypisuje elementy ciągu Fibonacciego mniejsze niż podana liczba `n`:

```python
def fib(n):
    """Wypisz elementy ciągu Fibonacciego mniejsze niż n."""
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a+b
    print()
```

Wywołanie:

```python
fib(2000)
```

Wynik:

```
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597
```

---

### 🧩 Anatomia definicji funkcji

```python
def fib(n):
    """Wypisz elementy ciągu Fibonacciego mniejsze niż n."""
    a, b = 0, 1
    while a < n:
        ...
```

Rozbijmy to na części:

```
def         ← słowo kluczowe oznaczające definicję funkcji
fib         ← nazwa funkcji (możesz ją potem wywołać jako fib(...))
(n)         ← lista parametrów — tu funkcja oczekuje jednego argumentu
:           ← koniec nagłówka, zaraz zaczyna się ciało
    """...""" ← docstring — opis funkcji (opcjonalny, ale zalecany)
    a, b = 0, 1
    ...      ← ciało funkcji — musi być wcięte!
```

---

### 📝 Docstring — opis funkcji

Pierwszy wiersz ciała funkcji może być gołym napisem zwanym **docstringiem**:

```python
def fib(n):
    """Wypisz elementy ciągu Fibonacciego mniejsze niż n."""
    ...
```

Docstring to nie zwykły komentarz — jest on **częścią obiektu funkcji** i można go odczytać w każdej chwili:

```python
help(fib)
# Wypisz elementy ciągu Fibonacciego mniejsze niż n.
```

Narzędzia do generowania dokumentacji (jak Sphinx) i środowiska IDE automatycznie korzystają z docstringów. **Dobry nawyk: pisz docstring zawsze, gdy definiujesz funkcję.**

---

### 🗂️ Jak Python zarządza zmiennymi w funkcji?

Każde wywołanie funkcji tworzy swoją **własną tablicę symboli** — oddzielną przestrzeń dla zmiennych lokalnych. Gdy Python szuka wartości zmiennej, przeszukuje kolejno:

```
1. Lokalna tablica symboli tej funkcji
        ↓ nie znaleziono?
2. Lokalne tablice funkcji otaczających (jeśli są)
        ↓ nie znaleziono?
3. Globalna tablica symboli modułu
        ↓ nie znaleziono?
4. Tablica nazw wbudowanych (built-ins: print, len, range...)
        ↓ nie znaleziono?
5. NameError — zmienna nie istnieje
```

#### Co to oznacza w praktyce?

```python
x = 10          # zmienna globalna

def funkcja():
    x = 99      # to jest INNA zmienna — lokalna kopia!
    print(x)    # wypisze 99

funkcja()
print(x)        # wypisze 10 — globalna x się nie zmieniła!
```

> ⚠️ **Ważne:** wewnątrz funkcji możesz **czytać** zmienne globalne, ale nie możesz ich **nadpisywać** bez użycia słów kluczowych `global` lub `nonlocal`.

---

### 📨 Jak przekazywane są argumenty?

Argumenty przekazywane są **przez wartość — ale tą wartością jest referencja do obiektu**, nie sam obiekt.

```python
# Dla typów niezmiennych (int, str, tuple) — oryginał jest bezpieczny
def podwoj(x):
    x = x * 2       # lokalna kopia — oryginał bez zmian
    return x

a = 5
podwoj(a)
print(a)             # nadal 5

# Dla typów zmiennych (list, dict) — funkcja MOŻE zmodyfikować oryginał!
def dodaj_element(lista):
    lista.append(99)  # modyfikuje oryginalną listę!

moja_lista = [1, 2, 3]
dodaj_element(moja_lista)
print(moja_lista)    # [1, 2, 3, 99]
```

---

### 🔗 Funkcja to obiekt

W Pythonie funkcja jest pełnoprawnym obiektem — można ją przypisać do zmiennej i wywołać pod nową nazwą:

```python
fib               # → <function fib at 0x10042ed0>

f = fib           # f wskazuje na ten sam obiekt funkcji
f(100)            # wywołanie przez nową nazwę
```

Wynik:

```
0 1 1 2 3 5 8 13 21 34 55 89
```

---

### 🔄 `return` — zwracanie wartości

Instrukcja `return` kończy funkcję i zwraca wartość do miejsca wywołania:

```python
def fib2(n):
    """Zwróć listę zawierającą ciąg Fibonacciego do n."""
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a, b = b, a+b
    return result

f100 = fib2(100)
print(f100)
```

Wynik:

```
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
```

#### Co jeśli funkcja nie ma `return`?

Każda funkcja **zawsze zwraca coś** — jeśli brakuje `return`, Python cicho zwraca `None`:

```python
fib(0)             # wypisuje nic (pusta linia), zwraca None
print(fib(0))      # wypisze: None
```

|Sytuacja|Zwracana wartość|
|---|---|
|`return wartość`|podana wartość|
|`return` (bez wyrażenia)|`None`|
|Dojście do końca ciała funkcji|`None`|

---

### 📋 Metody a funkcje — krótkie wyjaśnienie

W przykładzie `fib2` pojawia się `result.append(a)`. To nie jest zwykła funkcja — to **metoda**:

```
result.append(a)
  ↑       ↑
obiekt  metoda — funkcja "należąca" do obiektu
```

Metoda działa jak funkcja, ale jest przypisana do konkretnego typu obiektu. `append()` jest metodą listy — dodaje element na jej końcu:

```python
result.append(a)          # wydajne — modyfikuje listę w miejscu
result = result + [a]     # równoważne, ale tworzy nową listę za każdym razem
```

---

### 🔍 Porównanie — funkcja wypisująca vs zwracająca

```python
# Wersja 1: wypisuje wynik (nie możesz go dalej używać)
def fib(n):
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a+b

fib(10)             # wypisuje: 0 1 1 2 3 5 8
wynik = fib(10)     # wynik == None  ← nic nie możesz z tym zrobić!

# Wersja 2: zwraca listę (możesz jej używać dalej)
def fib2(n):
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a, b = b, a+b
    return result

wynik = fib2(10)    # wynik == [0, 1, 1, 2, 3, 5, 8]
print(sum(wynik))   # możesz sumować, filtrować, sortować...
```

> 💡 **Zasada ogólna:** jeśli chcesz używać wyników funkcji dalej w kodzie — użyj `return`. Jeśli funkcja służy tylko do wypisywania — `print` wewnątrz wystarczy.

---

## ⚙️ Funkcje i Domyślne wartości argumentów

> Zdefiniuj funkcję raz — wywołuj ją na wiele sposobów.

---

### 📌 Czym są domyślne wartości argumentów?

Domyślna wartość argumentu to wartość, którą Python użyje **automatycznie**, jeśli wywołasz funkcję bez podania tego argumentu. Dzięki temu funkcja może być wywoływana z różną liczbą argumentów — od minimalnej do pełnej.

```python
def ask_ok(prompt, retries=4, reminder='Spróbuj ponownie!'):
    while True:
        reply = input(prompt)
        if reply in {'t', 'ta', 'tak'}:
            return True
        if reply in {'n', 'ni', 'nie'}:
            return False
        retries = retries - 1
        if retries < 0:
            raise ValueError('Niepoprawna odpowiedź użytkownika')
        print(reminder)
```

#### Anatomia definicji

```
def ask_ok(prompt,   retries=4,              reminder='Spróbuj ponownie!'):
            ↑            ↑                          ↑
         wymagany    opcjonalny                opcjonalny
         (zawsze      (domyślnie 4)         (domyślnie 'Spróbuj ponownie!')
         podawany)
```

---

### 🎛️ Sposoby wywołania tej samej funkcji

```python
# Tylko wymagany argument — retries=4, reminder='Spróbuj ponownie!' z domyślnych
ask_ok('Czy na pewno chcesz wyjść?')

# Dwa argumenty — reminder='Spróbuj ponownie!' z domyślnego
ask_ok('OK nadpisać plik?', 2)

# Wszystkie argumenty — żadna wartość domyślna nie jest użyta
ask_ok('OK nadpisać plik?', 2, 'No coś ty, tylko tak lub nie!')
```

Trzy wywołania, ta sama funkcja — Python sam uzupełnia brakujące argumenty wartościami domyślnymi.

---

### 🔍 Przy okazji — operator `in`

W przykładzie pojawia się słowo kluczowe `in`:

```python
if reply in {'t', 'ta', 'tak'}:
    return True
```

`in` sprawdza, czy dana wartość **należy do sekwencji lub zbioru**:

```python
'tak' in {'t', 'ta', 'tak'}   # True
'nie' in {'t', 'ta', 'tak'}   # False
3 in [1, 2, 3, 4]             # True
'a' in 'nazywam'              # True — działa też na napisach!
```

Użycie zbioru `{...}` zamiast listy `[...]` jest tu celowe — sprawdzanie przynależności do zbioru jest **szybsze** niż przeszukiwanie listy.

---

### ⏱️ Kiedy wyliczana jest wartość domyślna?

> **Wartości domyślne są wyliczane dokładnie raz — w momencie definiowania funkcji.**

To ważna subtelność. Spójrzmy na przykład:

```python
i = 5

def f(arg=i):   # ← wartość domyślna wyliczana TUTAJ, gdy Python czyta tę linię
    print(arg)

i = 6           # zmiana i po definicji funkcji
f()             # wypisze 5, nie 6!
```

```
i = 5  →  def f(arg=i)  →  domyślna wartość arg = 5  →  zapamiętana na stałe
i = 6  →  nie ma żadnego wpływu na już zdefiniowaną funkcję
f()    →  arg = 5  ✅
```

Myśl o tym tak: Python "sfotografował" wartość `i` w momencie definiowania funkcji. Późniejsze zmiany `i` na zdjęciu już nie zmieniają.

---

### 🚨 Pułapka — mutowalne wartości domyślne

Tu kryje się jeden z najsłynniejszych błędów początkujących w Pythonie.

Ponieważ wartość domyślna jest wyliczana **tylko raz**, mutowalny obiekt (lista, słownik) jako wartość domyślna jest **współdzielony między wszystkimi wywołaniami** funkcji:

```python
def f(a, L=[]):    # ← ta lista [] tworzona jest RAZ, przy definicji
    L.append(a)
    return L

print(f(1))   # [1]
print(f(2))   # [1, 2]  ← lista pamięta poprzednie wywołanie!
print(f(3))   # [1, 2, 3]  ← i to też!
```

#### Dlaczego tak się dzieje?

```
Definicja funkcji:  L = []          ← jeden obiekt listy, stworzony raz
                        ↑
f(1) wywołane:      L.append(1)     → L = [1]
f(2) wywołane:      L.append(2)     → L = [1, 2]   ← ta sama lista!
f(3) wywołane:      L.append(3)     → L = [1, 2, 3] ← nadal ta sama lista!
```

Lista nie jest tworzona na nowo przy każdym wywołaniu — jest **jedna wspólna lista** dla całego życia funkcji.

---

### ✅ Rozwiązanie — użyj `None` jako wartości domyślnej

Standardowy, idiomatyczny wzorzec w Pythonie:

```python
def f(a, L=None):       # None jest niemutowalny — bezpieczny jako domyślny
    if L is None:
        L = []          # nowa lista tworzona przy każdym wywołaniu
    L.append(a)
    return L

print(f(1))   # [1]
print(f(2))   # [2]     ← własna, świeża lista!
print(f(3))   # [3]     ← i znowu świeża!
```

#### Porównanie zachowania

```
❌ def f(a, L=[]):          ✅ def f(a, L=None):
      f(1) → [1]                  f(1) → [1]
      f(2) → [1, 2]               f(2) → [2]
      f(3) → [1, 2, 3]            f(3) → [3]

   Jedna wspólna lista          Nowa lista przy każdym wywołaniu
```

Ale co jeśli chcesz **celowo** przekazać istniejącą listę?

```python
moja_lista = [10, 20]
f(30, moja_lista)     # [10, 20, 30] — działa, lista przekazana wprost
```

---

### 📋 Zasady dotyczące kolejności argumentów

Argumenty z wartościami domyślnymi muszą zawsze stać **po** argumentach wymaganych:

```python
# ✅ Poprawnie
def f(wymagany, opcjonalny=10):
    ...

# ❌ SyntaxError — wymagany argument po opcjonalnym
def f(opcjonalny=10, wymagany):
    ...
```

---

### 🔑 Podsumowanie kluczowych zasad

|Zasada|Opis|
|---|---|
|Wartość domyślna wyliczana jest **raz**|W momencie definiowania funkcji, nie wywołania|
|Argumenty wymagane zawsze **przed** opcjonalnymi|Inaczej `SyntaxError`|
|Mutowalne domyślne (`[]`, `{}`) są **współdzielone**|To zazwyczaj błąd — używaj `None`|
|`None` jako domyślny + tworzenie w ciele|Standardowy, bezpieczny wzorzec|

---

## 🏷️ Funkcje i Argumenty nazwane

> Wywołuj funkcje czytelniej — podawaj argumenty po nazwie, w dowolnej kolejności.

---

### 📌 Czym są argumenty nazwane?

Normalnie argumenty podajesz **pozycyjnie** — Python dopasowuje je do parametrów po kolejności:

```python
def parrot(voltage, state='jest sztywna', action='fru', type='norweska błękitna'):
    print("-- Ta papuga nie zrobi", action, end=' ')
    print("nawet jeśli podłączę ją do", voltage, "woltów.")
    print("-- Śliczne upierzenie,", type)
    print("-- Ona", state, "!")
```

Możesz jednak podać dowolny argument **po nazwie** — wtedy kolejność przestaje mieć znaczenie:

```python
parrot(voltage=1000000, action='FRUUUUU')   # kolejność dowolna
parrot(action='FRUUUUU', voltage=1000000)   # identyczny efekt!
```

---

### 🎛️ Wszystkie poprawne sposoby wywołania

```python
parrot(1000)
# voltage=1000, pozostałe z domyślnych

parrot(voltage=1000)
# to samo co wyżej — voltage podane po nazwie

parrot(voltage=1000000, action='FRUUUUU')
# dwa argumenty nazwane

parrot(action='FRUUUUU', voltage=1000000)
# kolejność nie ma znaczenia — wynik identyczny

parrot('miliona', 'wyzionęła ducha', 'hop')
# trzy argumenty pozycyjne: voltage, state, action

parrot('tysiąca', state='wącha kwiatki')
# mix: pierwszy pozycyjny, drugi nazwany
```

---

### ❌ Wywołania niepoprawne — i dlaczego

```python
parrot()
# TypeError: brakuje wymaganego argumentu 'voltage'
# → voltage nie ma wartości domyślnej, trzeba go zawsze podać

parrot(voltage=5.0, 'zdechła')
# SyntaxError: argument pozycyjny za argumentem nazwanym
# → po argumencie nazwanym nie można już użyć pozycyjnego

parrot(110, voltage=220)
# TypeError: argument 'voltage' otrzymał wartość dwa razy
# → 110 trafia do voltage pozycyjnie, potem voltage=220 próbuje nadpisać

parrot(actor='John Cleese')
# TypeError: nieznany argument nazwany 'actor'
# → funkcja nie zna parametru o tej nazwie
```

#### Reguły w pigułce

```
✅ Argumenty pozycyjne zawsze PRZED nazwanymi
✅ Argumenty nazwane mogą być w dowolnej kolejności między sobą
✅ Każdy argument może otrzymać wartość tylko RAZ
✅ Nazwy argumentów muszą odpowiadać parametrom funkcji
```

---

### 🔢 Przykład duplikacji — częsty błąd

```python
def function(a):
    pass

function(0, a=0)
# TypeError: function() got multiple values for argument 'a'
```

Co się tu dzieje:

```
function(0, a=0)
         ↑  ↑
         │  └── nazwany:    a = 0
         └───── pozycyjny:  a = 0
                            ↑
                    Python widzi dwie wartości dla 'a' → błąd!
```

---

### 📦 `*args` i `**kwargs` — przechwytywanie wszystkiego

Python pozwala zdefiniować funkcję, która przyjmuje **dowolną liczbę** argumentów pozycyjnych i nazwanych:

```python
def cheeseshop(kind, *arguments, **keywords):
    print("-- Czy jest może", kind, "?")
    print("-- Przykro mi, nie mamy już sera", kind)
    for arg in arguments:
        print(arg)
    print("-" * 40)
    for kw in keywords:
        print(kw, ":", keywords[kw])
```

#### Co oznacza każdy parametr?

```
def cheeseshop(kind,        *arguments,              **keywords):
               ↑                ↑                        ↑
         normalny           krotka ze                słownik ze
         argument           WSZYSTKICH               WSZYSTKICH
         (wymagany)         dodatkowych              dodatkowych
                            argumentów               argumentów
                            pozycyjnych              nazwanych
```

#### Wywołanie

```python
cheeseshop(
    "limburger",
    "Jest bardzo płynny, proszę pana.",
    "Naprawdę jest bardzo, BARDZO płynny, proszę pana.",
    shopkeeper="Michael Palin",
    client="John Cleese",
    sketch="Sklep z serami"
)
```

#### Co Python widzi w środku funkcji?

```
kind       = "limburger"
arguments  = ("Jest bardzo płynny, proszę pana.",
              "Naprawdę jest bardzo, BARDZO płynny, proszę pana.")
keywords   = {"shopkeeper": "Michael Palin",
              "client":     "John Cleese",
              "sketch":     "Sklep z serami"}
```

#### Wynik

```
-- Czy jest może limburger ?
-- Przykro mi, nie mamy już sera limburger
Jest bardzo płynny, proszę pana.
Naprawdę jest bardzo, BARDZO płynny, proszę pana.
----------------------------------------
shopkeeper : Michael Palin
client : John Cleese
sketch : Sklep z serami
```

> 💡 **Kolejność kluczy w `**keywords` odpowiada kolejności podania argumentów** w wywołaniu — Python zachowuje ją od wersji 3.7.

---

### 🗂️ Kolejność parametrów w definicji funkcji

Jeśli używasz `*args` i `**kwargs`, muszą być w odpowiedniej kolejności:

```python
def f(normalny, *args, **kwargs):
    ...
#      ↑           ↑       ↑
#   zawsze      przed   zawsze
#   pierwsze   **kwargs  ostatni
```

```python
# ✅ Poprawnie
def f(a, b, *args, **kwargs): ...

# ❌ SyntaxError — **kwargs musi być ostatni
def f(a, **kwargs, *args): ...
```

---

### 🔍 Argumenty pozycyjne vs nazwane — porównanie

|Cecha|Pozycyjne `f(1, 2)`|Nazwane `f(a=1, b=2)`|
|---|---|---|
|Kolejność|Ma znaczenie|Nie ma znaczenia|
|Czytelność przy wielu arg.|Może być myląca|Zawsze jasna|
|Wymagane przy wywołaniu|Tak (dla wymaganych)|Tak (można podać po nazwie)|
|Możliwe po argumencie nazwanym|❌ Nie|✅ Tak|

---

### 💡 Kiedy warto używać argumentów nazwanych?

```python
# ❌ Ciężkie do czytania — co oznaczają te wartości?
connect("localhost", 5432, True, False, 30)

# ✅ Czytelne natychmiast
connect("localhost", port=5432, ssl=True, debug=False, timeout=30)
```

Argumenty nazwane szczególnie się opłacają gdy:

- funkcja ma **wiele parametrów opcjonalnych**
- chcesz pominąć niektóre domyślne wartości środkowych parametrów
- zależy ci na **czytelności** kodu dla innych (i dla siebie za 3 miesiące)

---

## 🎚️ Argumenty Pozycyjne i Nazwane plus Parametry specjalne (`/` i `*`)

> Kontroluj dokładnie _jak_ argumenty mogą być przekazywane — po pozycji, po nazwie, albo tylko jednym z tych sposobów.

---

### 📌 Po co w ogóle ograniczać sposób podawania argumentów?

Domyślnie Python pozwala przekazać każdy argument albo pozycyjnie, albo po nazwie. To wygodne, ale czasem chcesz być precyzyjny — żeby kod był **czytelniejszy**, **bezpieczniejszy** (API) albo po prostu **wyraźnie komunikował intencję**.

Do tego służą dwa specjalne symbole w definicji funkcji: `/` i `*`.

---

### 🗺️ Mapa parametrów

```python
def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):
      ─────────────   ───────────   ───────────
            │               │             │
            │         pozycyjny       tylko
            │         lub nazwany     nazwany
            │
       tylko pozycyjny
```

|Symbol|Znaczenie|
|---|---|
|`/`|Wszystko **przed** `/` — tylko pozycyjnie|
|_(brak)_|Wszystko **między** `/` a `*` — pozycyjnie lub po nazwie|
|`*`|Wszystko **po** `*` — tylko po nazwie|

Oba symbole są opcjonalne. Możesz używać tylko `/`, tylko `*`, obu naraz lub żadnego.

---

### 🔬 Cztery rodzaje funkcji — porównanie

#### 🔹 1. Standardowa — bez ograniczeń

```python
def standard_arg(arg):
    print(arg)
```

```python
standard_arg(2)       # ✅ pozycyjnie
standard_arg(arg=2)   # ✅ po nazwie
```

Brak `/` i `*` — pełna swoboda.

---

#### 🔹 2. Tylko pozycyjnie — `/`

```python
def pos_only_arg(arg, /):
    print(arg)
```

```python
pos_only_arg(1)       # ✅ pozycyjnie
pos_only_arg(arg=1)   # ❌ TypeError — nie wolno po nazwie!
```

Ukośnik `/` mówi: _„nie obchodzi mnie jak to się nazywa — podaj wartość po pozycji"_.

---

#### 🔹 3. Tylko po nazwie — `*`

```python
def kwd_only_arg(*, arg):
    print(arg)
```

```python
kwd_only_arg(3)       # ❌ TypeError — nie wolno pozycyjnie!
kwd_only_arg(arg=3)   # ✅ tylko po nazwie
```

Gwiazdka `*` mówi: _„musisz wprost powiedzieć co podajesz — żadnego zgadywania po kolejności"_.

---

#### 🔹 4. Wszystkie trzy strefy naraz

```python
def combined_example(pos_only, /, standard, *, kwd_only):
    print(pos_only, standard, kwd_only)
```

```python
combined_example(1, 2, 3)
# ❌ TypeError — kwd_only musi być podany po nazwie

combined_example(1, 2, kwd_only=3)
# ✅ pos_only=1 (pozycja), standard=2 (pozycja), kwd_only=3 (nazwa)

combined_example(1, standard=2, kwd_only=3)
# ✅ pos_only=1 (pozycja), standard=2 (nazwa), kwd_only=3 (nazwa)

combined_example(pos_only=1, standard=2, kwd_only=3)
# ❌ TypeError — pos_only nie może być podany po nazwie!
```

---

### 🔄 Tabela: co gdzie wolno

```
def combined_example(pos_only, /, standard, *, kwd_only):
```

|Parametr|Pozycyjnie|Po nazwie|
|---|:-:|:-:|
|`pos_only`|✅|❌|
|`standard`|✅|✅|
|`kwd_only`|❌|✅|

---

### 🚧 Zaawansowana pułapka — kolizja nazwy z `**kwds`

Rozważ tę funkcję:

```python
def foo(name, **kwds):
    return 'name' in kwds
```

Problem: nie można sprawić, żeby zwróciła `True`, bo `name` zawsze "przechwytuje" argument pozycyjny — nawet gdy próbujesz przekazać go przez `**kwds`:

```python
foo(1, **{'name': 2})
# ❌ TypeError: foo() got multiple values for argument 'name'
```

Python widzi dwie wartości dla `name` — jedną z pozycji (`1`), drugą ze słownika (`2`).

#### Rozwiązanie — użyj `/`

```python
def foo(name, /, **kwds):
    return 'name' in kwds
```

```python
foo(1, **{'name': 2})
# ✅ True
```

Dlaczego to działa? Bo `/` sprawia, że `name` jako parametr jest **wyłącznie pozycyjny** — a `'name'` jako klucz w `**kwds` to zupełnie coś innego. Nie ma konfliktu.

```
foo(1,          **{'name': 2})
    ↑                 ↑
name=1            kwds={'name': 2}
(pozycja)         (słownik kwargs)
← dwa różne miejsca, zero konfliktu ✅
```

---

### 🧭 Kiedy używać każdego rodzaju?

|Sytuacja|Zalecenie|
|---|---|
|Nazwa parametru nie ma znaczenia dla użytkownika|Użyj `/` (tylko pozycyjny)|
|Chcesz wymusić określoną kolejność argumentów|Użyj `/` (tylko pozycyjny)|
|Budujesz publiczne API — chcesz móc zmienić nazwę parametru w przyszłości|Użyj `/` (zmiana nazwy nie złamie kodu klientów)|
|Nazwa parametru niesie ważne znaczenie semantyczne|Użyj `*` (tylko nazwany)|
|Funkcja ma wiele opcjonalnych parametrów i kolejność byłaby myląca|Użyj `*` (tylko nazwany)|
|Chcesz maksymalnej elastyczności — bez ograniczeń|Nie używaj ani `/` ani `*`|

---

### 📋 Szybka ściąga — wszystkie formy

```python
def f(a, b):              # a i b: pozycyjnie LUB po nazwie
def f(a, b, /):           # a i b: TYLKO pozycyjnie
def f(*, a, b):           # a i b: TYLKO po nazwie
def f(a, /, b):           # a: tylko pozycyjnie | b: dowolnie
def f(a, /, *, b):        # a: tylko pozycyjnie | b: tylko po nazwie
def f(a, /, b, *, c):     # a: tylko poz. | b: dowolnie | c: tylko nazwa
```

---
## 📦 Arbitralne listy argumentów (`*args`)

> Napisz funkcję raz — wywołuj ją z dowolną liczbą argumentów.

---

### 📌 Czym są arbitralne listy argumentów?

Czasem nie wiesz z góry, ile argumentów zostanie przekazanych do funkcji. Zamiast wymuszać sztywną liczbę parametrów, możesz użyć `*args` — Python sam zapakuje wszystkie dodatkowe argumenty pozycyjne w **krotkę**.

```python
def write_multiple_items(file, separator, *args):
    file.write(separator.join(args))
```

```
write_multiple_items(file, separator, *args)
                      ↑       ↑         ↑
                  wymagany  wymagany   krotka ze wszystkich
                                       pozostałych argumentów
```

---

### 💡 Przykład praktyczny

```python
def concat(*args, sep="/"):
    return sep.join(args)
```

```python
concat("ziemia", "mars", "wenus")
# → 'ziemia/mars/wenus'    ← sep domyślnie "/"

concat("ziemia", "mars", "wenus", sep=".")
# → 'ziemia.mars.wenus'    ← sep podane wprost po nazwie
```

#### Co Python widzi w środku funkcji?

```
concat("ziemia", "mars", "wenus", sep=".")

args = ("ziemia", "mars", "wenus")   ← krotka
sep  = "."                           ← argument tylko-kluczowy
```

---

### 🔑 Ważna zasada — argumenty po `*args` są tylko-kluczowe

Każdy parametr zdefiniowany **po** `*args` może być przekazany **wyłącznie po nazwie** — nigdy pozycyjnie. Działa to tak samo jak `*` w parametrach specjalnych:

```python
def concat(*args, sep="/"):
    ...

concat("a", "b", "/")       # ❌ "/" trafi do args, nie do sep!
concat("a", "b", sep="/")   # ✅ sep podane wprost po nazwie
```

```
concat("a", "b", "/")
       ↑     ↑    ↑
       └─────┴────┘
         args = ("a", "b", "/")   ← "/" połknięte przez *args!
         sep  = "/"               ← wartość domyślna — bez zmian
```

---

### 📋 Kiedy używać `*args`?

|Sytuacja|Przykład|
|---|---|
|Łączenie dowolnej liczby napisów|`concat("a", "b", "c", "d")`|
|Funkcje matematyczne (suma, min, max)|`my_sum(1, 2, 3, 4, 5)`|
|Logowanie / drukowanie wielu wartości|`log("błąd", kod, szczegóły)`|
|Opakowywanie innych funkcji|`wrapper(*args, **kwargs)`|

---

### 🔍 `*args` a zwykłe argumenty — kolejność

`*args` zazwyczaj pojawia się **na końcu** listy parametrów, bo pochłania wszystkie pozostałe argumenty pozycyjne. Argumenty przed nim są wymagane i pobierane najpierw:

```python
def f(wymagany_1, wymagany_2, *args):
    ...

f(1, 2, 3, 4, 5)
# wymagany_1 = 1
# wymagany_2 = 2
# args       = (3, 4, 5)
```

---

## 📤  Rozpakowywanie argumentów (`*` i `**`)

> Masz dane w liście lub słowniku? Przekaż je do funkcji bez ręcznego wypisywania każdego elementu.

---

### 📌 Problem — dane są zapakowane, funkcja chce osobnych argumentów

Wyobraź sobie, że masz argumenty dla `range()` zapisane w liście:

```python
args = [3, 6]
```

`range()` oczekuje dwóch osobnych liczb — `start` i `stop`. Możesz je wypisać ręcznie:

```python
list(range(args[0], args[1]))   # działa, ale brzydko
```

Albo użyć operatora `*`, który **rozpakuje listę** do osobnych argumentów:

```python
list(range(*args))              # elegancko ✅
```

Oba wywołania dają ten sam wynik:

```python
list(range(3, 6))    # [3, 4, 5]
list(range(*args))   # [3, 4, 5]
```

---

### 🔍 Jak działa rozpakowywanie?

```
args = [3, 6]

range(*args)
      ↑
      Python rozwija to do: range(3, 6)
      tak jakbyś wpisał argumenty ręcznie
```

```
lista = [1, 2, 3]
f(*lista)   →   f(1, 2, 3)

krotka = (4, 5, 6)
f(*krotka)  →   f(4, 5, 6)
```

Operator `*` działa na każdej sekwencji — liście, krotce, a nawet napisie.

---

### 🗂️ Rozpakowywanie słownika — operator `**`

Słownik możesz rozpakować do **argumentów nazwanych** za pomocą `**`:

```python
def parrot(voltage, state='sztywna', action='fru'):
    print("-- Ta papuga nie zrobi", action, end=' ')
    print("nawet jeśli podłączę ją do", voltage, "woltów.", end=' ')
    print("Jest", state, "!")

d = {
    "voltage": "czterech milionów",
    "state":   "sztywna jak kłoda",
    "action":  "FRUU"
}

parrot(**d)
```

Wynik:

```
-- Ta papuga nie zrobi FRUU nawet jeśli podłączę ją do czterech milionów woltów. Jest sztywna jak kłoda !
```

#### Co Python widzi?

```
parrot(**d)

→  parrot(
       voltage = "czterech milionów",
       state   = "sztywna jak kłoda",
       action  = "FRUU"
   )
```

Klucze słownika stają się nazwami argumentów, wartości stają się wartościami argumentów.

---

### ⚖️ Porównanie `*` i `**`

|Operator|Źródło|Cel|Przykład|
|---|---|---|---|
|`*`|lista / krotka|argumenty **pozycyjne**|`f(*[1, 2, 3])`|
|`**`|słownik|argumenty **nazwane**|`f(**{"a": 1, "b": 2})`|

---

### 🔗 Można łączyć oba naraz

```python
def f(a, b, c, d):
    print(a, b, c, d)

args   = [1, 2]
kwargs = {"c": 3, "d": 4}

f(*args, **kwargs)   # f(1, 2, c=3, d=4)  ✅
```

---

### 💡 Praktyczne zastosowania

```python
# Przekazywanie zebranych argumentów do innej funkcji
def wrapper(*args, **kwargs):
    return inna_funkcja(*args, **kwargs)

# Budowanie wywołania dynamicznie
parametry = {"sep": " | ", "end": "\n"}
print("Python", "jest", "super", **parametry)
# Python | jest | super

# Łączenie dwóch słowników przez rozpakowanie
defaults = {"kolor": "niebieski", "rozmiar": "M"}
nadpisania = {"kolor": "czerwony"}
wynik = {**defaults, **nadpisania}
# {"kolor": "czerwony", "rozmiar": "M"}
```

---
## λ Wyrażenia Lambda

> Mała funkcja bez nazwy — tam gdzie potrzebujesz funkcji, ale szkoda miejsca na `def`.

---

### 📌 Czym jest wyrażenie lambda?

Lambda to **anonimowa funkcja** — działa dokładnie jak zwykła funkcja, ale jest zapisana w jednej linii i nie ma nazwy. Porównanie:

```python
# Zwykła funkcja
def dodaj(a, b):
    return a + b

# Odpowiadające jej wyrażenie lambda
lambda a, b: a + b
```

Oba zapisy robią dokładnie to samo. Lambda to po prostu **skrócony zapis** — lukier składniowy dla prostych funkcji jednolinijkowych.

---

### 🧩 Składnia

```
lambda argumenty : wyrażenie
         ↑               ↑
   jak w def f(...)    automatycznie zwracane (bez słowa return)
```

```python
lambda x: x * 2          # jeden argument
lambda a, b: a + b        # dwa argumenty
lambda: 42                # bez argumentów
lambda x, y, z: x+y+z    # trzy argumenty
```

> ⚠️ Lambda może zawierać **tylko jedno wyrażenie** — żadnych pętli, warunków wielolinijkowych ani wielu instrukcji.

---

### 💡 Zastosowanie 1 — zwracanie funkcji z funkcji

```python
def make_incrementor(n):
    return lambda x: x + n   # ← lambda "zapamiętuje" wartość n
```

```python
f = make_incrementor(42)

f(0)   # → 42    (0 + 42)
f(1)   # → 43    (1 + 42)
f(10)  # → 52    (10 + 42)
```

#### Co tu się dzieje?

```
make_incrementor(42) zwraca funkcję: lambda x: x + 42
                                                    ↑
                                        n=42 zapamiętane z zewnętrznego zakresu
```

`f` jest teraz funkcją — możesz ją wywoływać ile razy chcesz. Lambda "zamknęła w sobie" wartość `n=42` z otaczającej funkcji. Taką technikę nazywamy **domknięciem** (ang. _closure_).

---

### 💡 Zastosowanie 2 — jako argument do innej funkcji

Lambda najczęściej pojawia się tam, gdzie inna funkcja oczekuje **funkcji jako argumentu** — np. przy sortowaniu:

```python
pairs = [(1, 'jeden'), (2, 'dwa'), (3, 'trzy'), (4, 'cztery')]

pairs.sort(key=lambda pair: pair[1])   # sortuj po drugim elemencie krotki

print(pairs)
```

Wynik (posortowany alfabetycznie po napisach):

```
[(4, 'cztery'), (2, 'dwa'), (1, 'jeden'), (3, 'trzy')]
```

#### Jak to czytać?

```
key=lambda pair: pair[1]
         ↑           ↑
   każda krotka    weź jej drugi element (napis)
   z listy         i użyj go jako klucz sortowania
```

Bez lambdy musiałbyś pisać:

```python
def klucz_sortowania(pair):
    return pair[1]

pairs.sort(key=klucz_sortowania)   # działa, ale jest bardziej rozwlekłe
```

---

### ⚖️ Lambda vs `def` — kiedy używać której?

|Cecha|`lambda`|`def`|
|---|---|---|
|Długość|Jednolinijkowa|Wielolinijkowa|
|Nazwa funkcji|Anonimowa|Ma nazwę|
|Złożoność logiki|Tylko jedno wyrażenie|Dowolna złożoność|
|Możliwość wielokrotnego użycia|Trudniejsza (brak nazwy)|Łatwa|
|Czytelność przy prostej logice|✅ Bardzo dobra|Może być przesadzona|
|Czytelność przy złożonej logice|❌ Nieczytelna|✅ Odpowiednia|

#### Praktyczna zasada

```python
# ✅ Lambda ma sens — krótka, jednorazowa, czytelna
pairs.sort(key=lambda p: p[1])

# ❌ Lambda nie ma sensu — zbyt skomplikowana
fn = lambda x: x**2 if x > 0 else -x**2 + 2*x   # użyj def!
```

---

### 🔗 Lambda i zmienne z zewnętrznego zakresu

Podobnie jak funkcje zagnieżdżone, lambda może odczytywać zmienne z otaczającego zakresu:

```python
mnoznik = 3
potroic = lambda x: x * mnoznik

potroic(5)    # → 15
potroic(10)   # → 30
```

> ⚠️ **Pułapka z pętlami:** lambda w pętli przechwytuje **referencję** do zmiennej, nie jej wartość w momencie tworzenia. Szczegóły znajdziesz w temacie domknięć.

---

```python

actions = []
for i in range(5):
    actions.append(lambda: i)

# Oczekiwano: 0, 1, 2, 3, 4
# Wynik: 4, 4, 4, 4, 4
print([action() for action in actions])

actions = []
for i in range(5):
    # 'i=i' tworzy argument domyślny, który jest wiązany
    # w momencie DEFINICJI lambdy, a nie jej wywołania
    actions.append(lambda i=i: i)

# Wynik: 0, 1, 2, 3, 4
print([action() for action in actions])

```

---

## 📝 Napisy dokumentujące (docstringi)

> Dokumentuj kod tam gdzie powstaje — docstring to pierwsza rzecz, którą zobaczy każdy kto użyje twojej funkcji.

---

### 📌 Czym jest docstring?

Docstring to **literał tekstowy** umieszczony jako pierwsza instrukcja w ciele funkcji, klasy lub modułu. Python automatycznie przypisuje go do atrybutu `__doc__` obiektu, dzięki czemu jest dostępny w każdej chwili — z poziomu kodu, w konsoli interaktywnej i w generatorach dokumentacji.

```python
def my_function():
    """Nie robi nic, ale dokumentuje to."""
    pass

print(my_function.__doc__)
# → Nie robi nic, ale dokumentuje to.
```

---

### 🧩 Struktura docstringa

#### Jednolinijkowy — dla prostych funkcji

```python
def dodaj(a, b):
    """Zwróć sumę dwóch liczb."""
    return a + b
```

#### Wielolinijkowy — dla złożonych funkcji

```python
def my_function():
    """Nie robi nic, ale dokumentuje to.

    Nie, naprawdę, ona nic nie robi:

        >>> my_function()
        >>>
    """
    pass
```

Budowa wielolinijkowego docstringa:

```
"""Zwięzłe streszczenie — jedna linijka, kończy się kropką.
                                                           ↑
(pusta linia — oddziela streszczenie od szczegółów)

Szczegółowy opis: konwencje, efekty uboczne, przykłady użycia,
ograniczenia i wszystko co może być przydatne użytkownikowi.
"""
```

---

### 📋 Konwencje — co pisać, czego unikać

|Zasada|✅ Dobrze|❌ Źle|
|---|---|---|
|Pierwsza linia — zwięzłe streszczenie|`"""Zwróć sumę dwóch liczb."""`|`"""Ta funkcja przyjmuje a i b i zwraca ich sumę."""`|
|Zaczyna się wielką literą|`"""Oblicz..."""`|`"""oblicz..."""`|
|Kończy się kropką|`"""Zwróć wynik."""`|`"""Zwróć wynik"""`|
|Nie powtarza nazwy funkcji|`"""Zwróć sumę."""`|`"""dodaj() zwraca sumę."""`|
|Druga linia pusta (wielolinijkowy)|streszczenie + pusty + szczegóły|streszczenie bezpośrednio + szczegóły|

---

### 🔍 Wcięcia w docstringach

Python **automatycznie usuwa wspólne wcięcia** z wielolinijkowych docstringów, więc to co piszesz — widzisz:

```python
def my_function():
    """Nie robi nic, ale dokumentuje to.

    Nie, naprawdę, ona nic nie robi:

        >>> my_function()
        >>>
    """
    pass

print(my_function.__doc__)
```

Wynik:

```
Nie robi nic, ale dokumentuje to.

Nie, naprawdę, ona nic nie robi:

    >>> my_function()
    >>>
```

Wcięcia wewnątrz docstringa (jak przy przykładach `>>>`) są **zachowywane względem siebie** — usuwane jest tylko wspólne wcięcie całego bloku.

---

### 🛠️ Jak czytać docstringi?

```python
# Atrybut __doc__
print(my_function.__doc__)

# Wbudowana funkcja help()
help(my_function)
```

`help()` wyświetla docstring w sformatowany, czytelny sposób — dokładnie tak samo korzysta z niego Python w trybie interaktywnym i środowiska IDE (podpowiedzi przy autouzupełnianiu).

---

### 💡 Dlaczego warto pisać docstringi?

```
Bez docstringa:              Z docstringiem:

help(f)                      help(f)
→ f(a, b)                    → f(a, b)
  (brak dokumentacji)          Zwróć sumę dwóch liczb.
```

- IDE wyświetla docstring jako podpowiedź przy wpisywaniu kodu
- `help()` w konsoli interaktywnej zwraca docstring natychmiast
- Narzędzia jak **Sphinx** generują z docstringów pełną dokumentację HTML
- Inni programiści (i ty za kilka miesięcy) wiedzą co robi funkcja bez czytania jej kodu

> 💡 **Dobry nawyk:** pisz docstring **od razu** gdy definiujesz funkcję — nie "potem", bo "potem" rzadko nadchodzi.

---

## 🏷️ Adnotacje funkcji i styl kodowania

---

### CZĘŚĆ 1 — Adnotacje funkcji

> Opcjonalne etykiety typów — dokumentują czego funkcja oczekuje i co zwraca.

---

#### 📌 Czym są adnotacje funkcji?

Adnotacje to **opcjonalne metadane** dołączane do parametrów i zwracanej wartości funkcji. Python je przechowuje, ale **całkowicie ignoruje** przy wykonywaniu kodu — nic nie sprawdza, nie wymusza, nie rzuca błędów.

Ich jedynym celem jest **komunikacja z programistą** — samym sobą za kilka miesięcy, współpracownikami i narzędziami do statycznej analizy kodu (jak `mypy`).

---

#### 🧩 Składnia

```python
def f(ham: str, eggs: str = 'jajka') -> str:
      ↑    ↑    ↑      ↑              ↑
   nazwa  typ  nazwa  typ          typ zwracanej
   param       param  + domyślna  wartości
               opcjon. wartość
```

- **Adnotacja parametru:** `nazwa: typ` — po nazwie, przed ewentualną wartością domyślną
- **Adnotacja zwracanej wartości:** `-> typ` — między nawiasem zamykającym a dwukropkiem

---

#### 💡 Przykład

```python
def f(ham: str, eggs: str = 'jajka') -> str:
    print("adnotacje:", f.__annotations__)
    print("argumenty:", ham, eggs)
    return ham + ' i ' + eggs
```

```python
f('szynka')
```

Wynik:

```
adnotacje: {'ham': <class 'str'>, 'eggs': <class 'str'>, 'return': <class 'str'>}
argumenty: szynka jajka
'szynka i jajka'
```

#### Gdzie są przechowywane?

Adnotacje lądują w słowniku `__annotations__` funkcji:

```python
f.__annotations__
# {'ham': <class 'str'>, 'eggs': <class 'str'>, 'return': <class 'str'>}
```

---

#### 🔍 Adnotacje nie wymuszają typów!

```python
def dodaj(a: int, b: int) -> int:
    return a + b

dodaj("ala", "ma")   # ✅ Python nie rzuci błędu — zwróci "alama"
```

Adnotacje to **sugestia**, nie kontrakt. Jeśli chcesz faktycznego sprawdzania typów, użyj zewnętrznych narzędzi:

|Narzędzie|Do czego|
|---|---|
|`mypy`|Statyczna analiza typów przed uruchomieniem|
|`pyright`|Alternatywa dla mypy, używana w VS Code|
|Pydantic|Walidacja typów w trakcie działania programu|

---

#### 💬 Adnotacje w praktyce — przykłady

```python
# Typy wbudowane
def greet(name: str) -> str: ...

# Wartości domyślne + adnotacje
def connect(host: str, port: int = 8080) -> bool: ...

# None jako typ zwracany (funkcja nic nie zwraca)
def log(message: str) -> None: ...

# Bardziej złożone typy (z modułu typing)
from typing import list, Optional
def znajdz(items: list[str], query: str) -> Optional[str]: ...
```

---

---

### CZĘŚĆ 2 — Styl kodowania (PEP 8)

> Kod czyta się wielokrotnie więcej razy niż się go pisze — zadbaj o czytelność.

---

#### 📌 Czym jest PEP 8?

**PEP 8** to oficjalny przewodnik stylu kodowania w Pythonie. Stosuje go zdecydowana większość projektów i bibliotek. To nie są wymysły — to wypracowane przez lata konwencje, które sprawiają że każdy kod Pythona wygląda znajomo i jest łatwy do czytania.

---

#### 📋 Najważniejsze zasady

##### 📐 Formatowanie

|Zasada|Szczegół|
|---|---|
|**Wcięcia**|4 spacje — nigdy tabulatory|
|**Długość linii**|Maksymalnie **79 znaków**|
|**Puste linie**|2 przed funkcją/klasą, 1 między metodami w klasie|
|**Komentarze**|W osobnej linii powyżej kodu, który opisują|

```python
# ✅ Poprawnie
def oblicz_powierzchnie(szerokosc, wysokosc):
    # Mnożymy wymiary aby uzyskać powierzchnię
    return szerokosc * wysokosc


def inna_funkcja():
    ...
```

---

##### 🔤 Nazewnictwo

|Co nazywamy|Konwencja|Przykład|
|---|---|---|
|Klasy|`UpperCamelCase`|`MojaKlasa`, `HttpClient`|
|Funkcje i metody|`lowercase_with_underscores`|`oblicz_sume()`, `pobierz_dane()`|
|Zmienne|`lowercase_with_underscores`|`liczba_elementow`, `nazwa_pliku`|
|Stałe|`UPPER_CASE`|`MAX_ROZMIAR`, `PI`|
|Pierwszy argument metody|zawsze `self`|`def __init__(self, ...)`|

```python
# ✅ Poprawnie
class HttpClient:
    MAX_TIMEOUT = 30

    def pobierz_dane(self, url: str) -> str:
        ...

# ❌ Niepoprawnie
class http_client:
    maxTimeout = 30

    def PobierzDane(self, URL):
        ...
```

---

##### ➕ Spacje i operatory

```python
# ✅ Spacje wokół operatorów i po przecinkach
a = f(1, 2) + g(3, 4)
x = x*2 - 1
wynik = (a+b) * (c+d)

# ❌ Brak spacji lub nadmiar przy nawiasach
a=f(1,2)+g(3,4)
wynik = ( a+b ) * ( c+d )
```

---

##### 🌍 Znaki i kodowanie

```python
# ✅ UTF-8 lub ASCII — działa wszędzie
def calculate_area(width, height):
    ...

# ❌ Znaki spoza ASCII jako identyfikatory — unikaj gdy kod będzie
# czytany przez osoby mówiące innymi językami
def oblicz_powierzchnię(szerokość, wysokość):   # ę, ń — mogą sprawiać problemy
    ...
```

---

#### 🛠️ Narzędzia do automatycznego pilnowania stylu

Nie musisz wszystkiego pamiętać — narzędzia zrobią to za ciebie:

|Narzędzie|Co robi|
|---|---|
|`flake8`|Sprawdza styl i zgłasza naruszenia PEP 8|
|`black`|Automatycznie formatuje kod zgodnie z PEP 8|
|`isort`|Sortuje importy zgodnie z konwencjami|
|`pylint`|Kompleksowa analiza jakości kodu|

```bash
pip install black
black moj_plik.py   # automatycznie sformatuje cały plik
```

---

#### 💡 Dlaczego to ważne?

```
Bez PEP 8:                      Z PEP 8:

def f(x,y,z):                   def oblicz_sume(a, b, c):
 return x+y+z                       return a + b + c

class myClass:                  class MojaKlasa:
  def DoSomething(self,Val):         def zrob_cos(self, wartosc):
   self.val=Val                          self.wartosc = wartosc
```

Kod spędza więcej czasu na **czytaniu** niż na pisaniu. Spójny styl sprawia, że cały zespół czyta kod z taką samą łatwością — niezależnie od tego kto go napisał.

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>


<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>


<div align="center">

# Data Structures

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Temat](https://img.shields.io/badge/temat-data--structures-3776AB?style=for-the-badge)

</div>

---

Rozdział 05 skupia się na strukturach danych w Pythonie i praktycznym operowaniu na:

> ⌲ listach
>
> ⌲ krotkach
>
> ⌲ słownikach
>
> ⌲ zbiorach

---

## 📋  Metody listy

> Lista w Pythonie to nie tylko kontener — to bogaty zestaw narzędzi do manipulowania danymi.

---

### 📌 Przegląd wszystkich metod

|Metoda|Co robi|Zwraca|
|---|---|---|
|`append(x)`|Dodaje `x` na koniec listy|`None`|
|`extend(iter)`|Dodaje wszystkie elementy z `iter` na koniec|`None`|
|`insert(i, x)`|Wstawia `x` przed indeksem `i`|`None`|
|`remove(x)`|Usuwa pierwsze wystąpienie `x`|`None`|
|`pop(i=-1)`|Usuwa i **zwraca** element na pozycji `i`|element|
|`clear()`|Usuwa wszystkie elementy|`None`|
|`index(x)`|Zwraca indeks pierwszego wystąpienia `x`|`int`|
|`count(x)`|Liczy ile razy `x` występuje na liście|`int`|
|`sort()`|Sortuje listę w miejscu|`None`|
|`reverse()`|Odwraca listę w miejscu|`None`|
|`copy()`|Zwraca płytką kopię listy|`list`|

---

### 🔬 Każda metoda z bliska

#### ➕ Dodawanie elementów

```python
a = [1, 2, 3]

# append — jeden element na koniec
a.append(4)           # [1, 2, 3, 4]
a.append([5, 6])      # [1, 2, 3, 4, [5, 6]]  ← lista jako jeden element!

# extend — wiele elementów na koniec (rozpakowane)
a.extend([5, 6])      # [1, 2, 3, 4, 5, 6]    ← każdy element osobno

# insert — element w dowolnym miejscu
a.insert(0, 99)       # [99, 1, 2, 3]  ← na początku
a.insert(2, 99)       # [1, 2, 99, 3]  ← przed indeksem 2
a.insert(len(a), 99)  # [1, 2, 3, 99]  ← na końcu (jak append)
```

> 💡 **`append` vs `extend`** — kluczowa różnica:
> 
> ```python
> a = [1, 2]
> a.append([3, 4])   # → [1, 2, [3, 4]]   ← lista wewnątrz listy
> a.extend([3, 4])   # → [1, 2, 3, 4]     ← elementy dodane osobno
> ```

---

#### ➖ Usuwanie elementów

```python
a = [1, 2, 3, 2, 4]

# remove — usuwa pierwsze wystąpienie wartości
a.remove(2)    # → [1, 3, 2, 4]  ← usunięto tylko pierwsze 2
a.remove(9)    # → ValueError: 9 is not in list

# pop — usuwa i ZWRACA element
a = [1, 2, 3, 4]
a.pop()        # → zwraca 4,  lista: [1, 2, 3]
a.pop(0)       # → zwraca 1,  lista: [2, 3]
a.pop(10)      # → IndexError: pop index out of range

# clear — czyści całą listę
a.clear()      # → []
```

> ⚠️ `remove(x)` usuwa **pierwsze** wystąpienie — jeśli `x` nie istnieje, rzuca `ValueError`.  
> ⚠️ `pop()` na pustej liście rzuca `IndexError`.

---

#### 🔍 Wyszukiwanie

```python
a = ['jabłko', 'banan', 'kiwi', 'banan']

# index — znajdź pozycję elementu
a.index('banan')       # → 1  (pierwsze wystąpienie)
a.index('banan', 2)    # → 3  (szukaj od indeksu 2)
a.index('gruszka')     # → ValueError

# count — policz wystąpienia
a.count('banan')       # → 2
a.count('mango')       # → 0
```

Opcjonalne argumenty `start` i `stop` w `index()` działają jak w notacji slice:

```python
a.index(wartość, start, stop)
#                 ↑      ↑
#           od tej      do tej
#           pozycji     pozycji
#
# Uwaga: zwracany indeks jest zawsze względem POCZĄTKU listy, nie argumentu start
```

---

#### 🔃 Porządkowanie

```python
a = [3, 1, 4, 1, 5, 9, 2, 6]

# sort — sortuje w miejscu (modyfikuje oryginał)
a.sort()                      # → [1, 1, 2, 3, 4, 5, 6, 9]
a.sort(reverse=True)          # → [9, 6, 5, 4, 3, 2, 1, 1]
a.sort(key=lambda x: -x)      # własna funkcja klucza

# reverse — odwraca w miejscu
a.reverse()                   # → kolejność odwrócona

# copy — płytka kopia
b = a.copy()   # b to nowa lista z tymi samymi elementami
               # równoważne: b = a[:]
```

> 💡 Jeśli chcesz posortowaną **nową listę** bez zmiany oryginału, użyj funkcji `sorted()`:
> 
> ```python
> oryginał = [3, 1, 2]
> nowa = sorted(oryginał)   # oryginał bez zmian, nowa = [1, 2, 3]
> ```

---

### 🧪 Przykład z życia — krok po kroku

```python
fruits = ['pomarańcza', 'jabłko', 'winogrono', 'banan', 'kiwi', 'jabłko', 'banan']
```

```python
fruits.count('jabłko')       # → 2
fruits.count('mandarynka')   # → 0

fruits.index('banan')        # → 3
fruits.index('banan', 4)     # → 6  (szukaj od pozycji 4)

fruits.reverse()
# → ['banan', 'jabłko', 'kiwi', 'banan', 'winogrono', 'jabłko', 'pomarańcza']

fruits.append('gruszka')
# → ['banan', 'jabłko', 'kiwi', 'banan', 'winogrono', 'jabłko', 'pomarańcza', 'gruszka']

fruits.sort()
# → ['banan', 'banan', 'gruszka', 'jabłko', 'jabłko', 'kiwi', 'pomarańcza', 'winogrono']

fruits.pop()                 # → 'winogrono' (ostatni element usunięty i zwrócony)
```

---

### ⚠️ Ważna zasada — metody modyfikujące zwracają `None`

Metody, które **zmieniają listę w miejscu** (`append`, `insert`, `remove`, `sort`, `reverse`, `clear`), zwracają `None` — nie samą listę:

```python
# ❌ Częsty błąd
a = [3, 1, 2]
a = a.sort()    # a jest teraz None!

# ✅ Poprawnie
a = [3, 1, 2]
a.sort()        # lista posortowana w miejscu
print(a)        # [1, 2, 3]

# ✅ Albo tak, jeśli chcesz zachować oryginał
b = sorted(a)   # nowa posortowana lista, a bez zmian
```

To celowa decyzja projektowa Pythona: **jeśli metoda zwraca `None`, wiesz że modyfikuje oryginał**. Jeśli zwraca nowy obiekt — oryginał jest nienaruszony.

---

### 🚫 Czego nie można sortować?

`sort()` działa tylko gdy elementy da się ze sobą **porównać**. Kilka przypadków które rzucą `TypeError`:

```python
[None, 'hello', 10].sort()   # ❌ int nie porównywalny z str
[3+4j, 5+7j].sort()          # ❌ liczby zespolone nie mają relacji porządku
[1, 'dwa', 3].sort()         # ❌ mieszanie typów
```

```python
# ✅ Działa — wszystkie elementy tego samego porównywalnego typu
[3, 1, 4, 1, 5].sort()
['banan', 'jabłko', 'gruszka'].sort()
```

---
## 🥞 Lista jako Stos

> Stos to prosta i potężna struktura danych — a lista Pythona obsługuje ją natywnie.

---

### 📌 Czym jest stos?

Stos (ang. _stack_) to struktura danych działająca na zasadzie **LIFO** — _Last In, First Out_ (ostatni wchodzi, pierwszy wychodzi). Wyobraź sobie stos talerzy: kładziesz nowy talerz na wierzch i zdejmujesz też z wierzchu.

```
        ┌─────────┐
        │    7    │  ← wierzch stosu (ostatni dodany)
        ├─────────┤
        │    6    │
        ├─────────┤
        │    5    │
        ├─────────┤
        │    4    │
        ├─────────┤
        │    3    │  ← spód stosu (pierwszy dodany)
        └─────────┘
```

---

### 🧩 Dwie operacje — `append()` i `pop()`

|Operacja|Metoda|Opis|
|---|---|---|
|Połóż na wierzch|`append(x)`|Dodaje element na szczyt stosu|
|Zdejmij z wierzchu|`pop()`|Usuwa i zwraca element ze szczytu|

---

### 💡 Przykład krok po kroku

```python
stack = [3, 4, 5]
```

```python
stack.append(6)   # kładziemy 6 na wierzch
stack.append(7)   # kładziemy 7 na wierzch
print(stack)      # [3, 4, 5, 6, 7]
```

```python
stack.pop()       # zdejmujemy z wierzchu → zwraca 7
stack.pop()       # zdejmujemy z wierzchu → zwraca 6
stack.pop()       # zdejmujemy z wierzchu → zwraca 5
print(stack)      # [3, 4]
```

#### Wizualizacja operacji

```
START:      append(6):   append(7):   pop():  pop():  pop():
  [3]         [3]          [3]         [3]     [3]     [3]
  [4]         [4]          [4]         [4]     [4]     [4]
  [5]         [5]          [5]         [5]     [5]
              [6]          [6]         [6]
                           [7] ←         ← 7   ← 6    ← 5
```

---

### ⚠️ Pamiętaj

```python
stack = []
stack.pop()   # ❌ IndexError: pop from empty list
              #    zawsze sprawdź czy stos nie jest pusty!

# Bezpieczne zdejmowanie
if stack:
    element = stack.pop()
```

---

### 💬 Kiedy używać listy jako stosu?

- ↩️ **Cofanie operacji** — każda akcja trafia na stos, `Ctrl+Z` zdejmuje ostatnią
- 🔎 **Przeszukiwanie w głąb** (DFS) — algorytmy grafowe i drzewa
- 🔢 **Ewaluacja wyrażeń** — kalkulatory, parsery nawiasów
- 🌐 **Historia nawigacji** — "wstecz" w przeglądarce

---

## 🚶 Lista jako Kolejka

> Kolejka to struktura FIFO — kto pierwszy, ten pierwszy wychodzi. Ale nie każda implementacja jest równie wydajna.

---

### 📌 Czym jest kolejka?

Kolejka (ang. _queue_) działa na zasadzie **FIFO** — _First In, First Out_ (pierwszy wchodzi, pierwszy wychodzi). Dokładnie jak kolejka w sklepie — kto przyszedł wcześniej, ten wychodzi pierwszy.

```
         WEJŚCIE →  [Graham] [Terry] [Michael] [John] [Eric]  → WYJŚCIE
                      nowy                              najstarszy
```

---

### ⚠️ Dlaczego zwykła lista jest zła jako kolejka?

Technicznie możesz używać listy jako kolejki — ale to **zły pomysł wydajnościowy**:

```python
queue = ['Eric', 'John', 'Michael']
queue.append('Terry')    # ✅ szybkie — dodaje na koniec
queue.pop(0)             # ❌ WOLNE — usuwa z początku
```

Przy `pop(0)` Python musi **przesunąć każdy pozostały element** o jedno miejsce w lewo:

```
Przed pop(0):  ['Eric', 'John', 'Michael', 'Terry']
                  ↑ usuwamy
               ['John', 'Michael', 'Terry']
                  ↑       ↑          ↑
               każdy przesunięty o jedno miejsce ← O(n)!
```

Im dłuższa lista, tym wolniejsza operacja. Dla 1 000 000 elementów — milion przesunięć przy każdym `pop(0)`.

---

### ✅ Rozwiązanie — `collections.deque`

`deque` (_double-ended queue_ — kolejka dwustronna) jest zaprojektowana tak, by operacje na **obu końcach** były zawsze szybkie:

```python
from collections import deque

queue = deque(['Eric', 'John', 'Michael'])
```

```python
queue.append('Terry')    # pojawia się Terry
queue.append('Graham')   # pojawia się Graham

print(queue)
# deque(['Eric', 'John', 'Michael', 'Terry', 'Graham'])
```

```python
queue.popleft()   # → 'Eric'    (pierwszy przybyły, pierwszy wychodzi)
queue.popleft()   # → 'John'

print(queue)
# deque(['Michael', 'Terry', 'Graham'])
```

---

### 🔍 Wizualizacja krok po kroku

```
START:               append('Terry'):      append('Graham'):
← [Eric John Michael]   ← [Eric John Michael Terry]   ← [Eric John Michael Terry Graham]

popleft():           popleft():
Eric → [John Michael Terry Graham]   John → [Michael Terry Graham]
```

---

### ⚡ Porównanie wydajności

|Operacja|`list`|`deque`|
|---|:-:|:-:|
|Dodaj na koniec|✅ O(1) — szybko|✅ O(1) — szybko|
|Usuń z końca|✅ O(1) — szybko|✅ O(1) — szybko|
|Dodaj na początek|❌ O(n) — wolno|✅ O(1) — szybko|
|Usuń z początku|❌ O(n) — wolno|✅ O(1) — szybko|

> `O(n)` oznacza że czas rośnie **liniowo** wraz z rozmiarem listy — dla 1 000 000 elementów to 1 000 000 operacji przy każdym `pop(0)`.

---

### 🔑 Podsumowanie

```python
# Stos (LIFO) → zwykła lista
stack = []
stack.append(x)   # push
stack.pop()       # pop

# Kolejka (FIFO) → deque
from collections import deque
queue = deque()
queue.append(x)   # enqueue
queue.popleft()   # dequeue
```

---

## ⚡Wyrażenia listowe (List Comprehensions)

> Twórz listy w jednej linii — zwięźle, czytelnie i bez efektów ubocznych.

---

### 📌 Po co wyrażenia listowe?

Klasyczne tworzenie listy przez pętlę:

```python
squares = []
for x in range(10):
    squares.append(x**2)
# squares = [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

Ma pewien problem — po wykonaniu pętli **zmienna `x` nadal istnieje** w przestrzeni nazw. To efekt uboczny, którego często chcemy uniknąć.

Wyrażenie listowe rozwiązuje oba problemy — jest krótsze i **nie zostawia śladów**:

```python
squares = [x**2 for x in range(10)]
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

---

### 🧩 Składnia

```
[ wyrażenie  for  zmienna  in  sekwencja  if  warunek ]
      ↑              ↑             ↑            ↑
  co zrobić    jak to      po czym       (opcjonalnie)
  z każdym     nazywamy    iterujemy     filtr elementów
  elementem
```

Klauzul `for` i `if` może być **dowolnie wiele** — czytaj je w tej samej kolejności co odpowiadającą pętlę.

---

### 💡 Przykłady od prostych do złożonych

#### 🔹 Transformacja każdego elementu

```python
vec = [-4, -2, 0, 2, 4]

[x * 2 for x in vec]
# [-8, -4, 0, 4, 8]

[abs(x) for x in vec]
# [4, 2, 0, 2, 4]
```

---

#### 🔹 Filtrowanie elementów

```python
[x for x in vec if x >= 0]
# [0, 2, 4]  ← tylko nieujemne
```

---

#### 🔹 Wywołanie metody na każdym elemencie

```python
freshfruit = ['  banan', '  malina ', 'marakuja  ']

[fruit.strip() for fruit in freshfruit]
# ['banan', 'malina', 'marakuja']
```

---

#### 🔹 Krotki jako wynik — wymagają nawiasów!

```python
# ✅ Poprawnie — krotka w nawiasach
[(x, x**2) for x in range(6)]
# [(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25)]

# ❌ SyntaxError — brakuje nawiasów wokół krotki
[x, x**2 for x in range(6)]
# SyntaxError: did you forget parentheses around the comprehension target?
```

---

#### 🔹 Dwie pętle — iloczyn kartezjański

```python
[(x, y) for x in [1, 2, 3] for y in [3, 1, 4] if x != y]
# [(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]
```

To dokładny odpowiednik zagnieżdżonych pętli — **kolejność `for` i `if` jest taka sama**:

```python
# Równoważna pętla
combs = []
for x in [1, 2, 3]:        # ← zewnętrzna (pierwsza w comprehension)
    for y in [3, 1, 4]:    # ← wewnętrzna (druga w comprehension)
        if x != y:         # ← filtr (na końcu comprehension)
            combs.append((x, y))
```

---

#### 🔹 Spłaszczanie zagnieżdżonej listy

```python
vec = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

[num for elem in vec for num in elem]
# [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Czytaj to jako: _„dla każdego `elem` w `vec`, dla każdego `num` w `elem` — daj mi `num`"_.

---

#### 🔹 Złożone wyrażenia i funkcje

```python
from math import pi

[str(round(pi, i)) for i in range(1, 6)]
# ['3.1', '3.14', '3.142', '3.1416', '3.14159']
```

---

### 🔄 Trzy sposoby na to samo — porównanie

```python
# Sposób 1 — pętla for (klasyczny, z efektem ubocznym: x nadal istnieje)
squares = []
for x in range(10):
    squares.append(x**2)

# Sposób 2 — map + lambda (funkcyjny, mniej czytelny)
squares = list(map(lambda x: x**2, range(10)))

# Sposób 3 — list comprehension (zalecany)
squares = [x**2 for x in range(10)]
```

|Kryterium|`for` + `append`|`map` + `lambda`|List comprehension|
|---|:-:|:-:|:-:|
|Zwięzłość|❌|✅|✅|
|Czytelność|✅|❌|✅|
|Efekty uboczne (zmienna `x`)|❌ Tak|✅ Nie|✅ Nie|
|Obsługa filtrów (`if`)|✅|❌ (wymaga `filter()`)|✅|

---

### 🗺️ Jak czytać złożone wyrażenia?

Przy skomplikowanych comprehensions pomocne jest **rozwinięcie ich do pętli**:

```python
# Comprehension
result = [wyrażenie for a in X for b in Y if warunek]

# Rozwinięcie (identyczny wynik)
result = []
for a in X:
    for b in Y:
        if warunek:
            result.append(wyrażenie)
```

Kolejność zawsze ta sama — czytaj od lewej do prawej.

---

### ⚠️ Kiedy NIE używać list comprehension?

```python
# ❌ Zbyt skomplikowane — lepiej użyć zwykłej pętli
result = [f(x) if x > 0 else g(x) for x in data if h(x) and x not in seen]

# ✅ Czytelniejsze jako pętla
result = []
for x in data:
    if h(x) and x not in seen:
        result.append(f(x) if x > 0 else g(x))
```

> 💡 **Zasada ogólna:** jeśli comprehension nie mieści się w jednej czytelnej linii — użyj zwykłej pętli.

---

## 🔲 Zagnieżdżone wyrażenia listowe

> List comprehension wewnątrz list comprehension — potężne narzędzie do pracy z macierzami i strukturami 2D.

---

### 📌 Macierz jako lista list

W Pythonie macierz najprościej reprezentuje się jako **listę list**:

```python
matrix = [
    [1,  2,  3,  4],
    [5,  6,  7,  8],
    [9, 10, 11, 12],
]
```

Wizualnie:

```
kolumna →   0   1   2   3
wiersz 0  [ 1,  2,  3,  4]
wiersz 1  [ 5,  6,  7,  8]
wiersz 2  [ 9, 10, 11, 12]
```

---

### 🔄 Transpozycja macierzy — zamiana wierszy z kolumnami

Transpozycja to zamiana wierszy z kolumnami — wiersz 0 staje się kolumną 0 itd.:

```
PRZED:          PO TRANSPOZYCJI:
[ 1,  2,  3,  4]    [ 1,  5,  9]
[ 5,  6,  7,  8] →  [ 2,  6, 10]
[ 9, 10, 11, 12]    [ 3,  7, 11]
                    [ 4,  8, 12]
```

Zagnieżdżone wyrażenie listowe robi to w jednej linii:

```python
[[row[i] for row in matrix] for i in range(4)]
# [[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]
```

---

### 🔬 Jak to czytać — od zewnątrz do wewnątrz

Zagnieżdżone comprehension czytamy **od zewnętrznego `for` do wewnętrznego**:

```python
[[row[i] for row in matrix] for i in range(4)]
  ─────────────────────────  ────────────────
          ↑                        ↑
    wewnętrzne                zewnętrzne
  (dla każdego i:           (iteruj po kolumnach
   zbierz i-ty element       0, 1, 2, 3)
   z każdego wiersza)
```

Krok po kroku:

```
i = 0 → [row[0] for row in matrix] → [1, 5, 9]
i = 1 → [row[1] for row in matrix] → [2, 6, 10]
i = 2 → [row[2] for row in matrix] → [3, 7, 11]
i = 3 → [row[3] for row in matrix] → [4, 8, 12]

wynik: [[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]
```

---

### 🧩 Trzy równoważne zapisy

#### Zapis 1 — zagnieżdżone list comprehension (najzwięźlejszy)

```python
[[row[i] for row in matrix] for i in range(4)]
```

#### Zapis 2 — zewnętrzna pętla + wewnętrzne comprehension

```python
transposed = []
for i in range(4):
    transposed.append([row[i] for row in matrix])
```

#### Zapis 3 — dwie zwykłe pętle (najprostszy do zrozumienia)

```python
transposed = []
for i in range(4):
    transposed_row = []
    for row in matrix:
        transposed_row.append(row[i])
    transposed.append(transposed_row)
```

Wszystkie trzy dają identyczny wynik:

```python
[[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]
```

---

### ✅ W praktyce — użyj `zip()`

Dla transpozycji macierzy Python ma wbudowane, elegantsze rozwiązanie:

```python
list(zip(*matrix))
# [(1, 5, 9), (2, 6, 10), (3, 7, 11), (4, 8, 12)]
```

Co tu się dzieje?

```
*matrix     → rozpakuje macierz jako osobne argumenty:
              zip([1,2,3,4], [5,6,7,8], [9,10,11,12])

zip(...)    → "szyje razem" elementy na tych samych pozycjach:
              (1,5,9), (2,6,10), (3,7,11), (4,8,12)

list(...)   → zamienia obiekt zip na listę
```

> 💡 `*matrix` to rozpakowywanie sekwencji — opisane szczegółowo w rozdziale **Rozpakowywanie listy argumentów**.

#### Porównanie podejść

|Podejście|Zwięzłość|Czytelność|Wynik|
|---|:-:|:-:|---|
|Zagnieżdżone comprehension|✅|⚠️ Wymaga chwili|listy list|
|`zip(*matrix)`|✅|✅ Idiomatyczne|krotki|
|Dwie pętle|❌|✅ Prosta|listy list|

---

### ⚠️ Zasada ogólna

Zagnieżdżone list comprehension są potężne, ale łatwo z nimi przesadzić. Gdy wyrażenie staje się trudne do czytania:

```python
# ❌ Zbyt skomplikowane — co tu właściwie robi?
result = [[f(x) for x in row if x > 0] for row in matrix if sum(row) > 10]

# ✅ Rozbij na kroki z komentarzami lub użyj pętli
```

> 💡 **Zasada:** jeśli potrzebujesz chwili żeby zrozumieć swoje własne wyrażenie — użyj zwykłych pętli.

---

## 📤 Rozpakowywanie w Listach i Wyrażeniach Listowych

> Operator `*` nie tylko rozpakowuje argumenty funkcji — działa też bezpośrednio przy tworzeniu list.

---

### 📌 Rozpakowywanie podczas tworzenia listy

Prefix `*` przed dowolnym iterable rozpakuje go i wstawi jego elementy **w to miejsce** nowej listy:

```python
x = [1, 2, 3]

[0, *x, 4, 5, 6]
# [0, 1, 2, 3, 4, 5, 6]
```

Co tu się dzieje:

```
[0,  *x,       4, 5, 6]
 ↑    ↑         ↑
 0    rozpakuj  4, 5, 6
      [1, 2, 3]

→ [0, 1, 2, 3, 4, 5, 6]
```

---

### 🔗 Łączenie wielu list bez `+`

To elegancki sposób na **konkatenację** kilku list w jednej operacji:

```python
a = [1, 2, 3]
b = [4, 5]
c = [6, 7, 8, 9]

[*a, *b, *c]
# [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Porównanie z tradycyjnymi metodami:

```python
a + b + c           # działa, tworzy kopię przy każdym +
[*a, *b, *c]        # czytelniejsze, jedna operacja
```

---

### ⚠️ Tylko iterowalne obiekty!

`*` działa wyłącznie na obiektach, po których można iterować. Próba rozpakowania liczby lub innego nieiterowanego obiektu rzuca `TypeError`:

```python
x = 1
[0, *x, 2, 3]
# TypeError: Value after * must be an iterable, not int
```

Co jest iterowalne?

|Typ|Iterowalny?|
|---|:-:|
|`list`|✅|
|`tuple`|✅|
|`str`|✅ (każdy znak osobno)|
|`dict`|✅ (klucze)|
|`set`|✅|
|`range`|✅|
|`int`, `float`|❌|
|`None`|❌|

---

### ⚡ Rozpakowywanie w wyrażeniach listowych

Operator `*` działa też **wewnątrz list comprehension** — to elegancki sposób na spłaszczanie zagnieżdżonych struktur:

```python
x = [[1, 2, 3], [4, 5, 6], [], [7], [8, 9]]

[*element for element in x]
# [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Każdy element listy `x` jest **rozpakowywany** i jego zawartość trafia do wynikowej listy. Pusta lista `[]` nie wnosi nic — znika bez śladu.

---

### 🎭 Rozpakowywanie różnych typów

`*` w list comprehension działa na **każdym iterowalne** — nie tylko na listach:

```python
x = [[1, 2, 3], 'cat', {'spam': 'eggs'}]

[*element for element in x]
# [1, 2, 3, 'c', 'a', 't', 'spam']
```

Co się tu stało z każdym elementem?

```
[1, 2, 3]       → *[1, 2, 3]       → 1, 2, 3
'cat'           → *'cat'           → 'c', 'a', 't'    ← napis → litery!
{'spam': 'eggs'} → *{'spam':'eggs'} → 'spam'           ← słownik → klucze!
```

> ⚠️ Zachowaj ostrożność przy mieszaniu typów — wyniki mogą być zaskakujące, szczególnie gdy `*str` rozbija napis na litery, a `*dict` daje tylko klucze.

---

### 🔍 Porównanie — spłaszczanie listy list

Trzy sposoby spłaszczenia `[[1,2], [3,4], [5,6]]`:

```python
x = [[1, 2], [3, 4], [5, 6]]

# Sposób 1 — rozpakowywanie w comprehension (nowy, elegancki)
[*elem for elem in x]
# [1, 2, 3, 4, 5, 6]

# Sposób 2 — klasyczne comprehension z dwoma for-ami
[num for elem in x for num in elem]
# [1, 2, 3, 4, 5, 6]

# Sposób 3 — zagnieżdżone pętle
result = []
for elem in x:
    result.extend(elem)
# [1, 2, 3, 4, 5, 6]
```

---

## 🗑️ Instrukcja `del`

> Usuń element, fragment lub całą zmienną — bez zwracania wartości.

---

### 📌 `del` vs `pop()` — kluczowa różnica

Zarówno `del`, jak i `pop()` usuwają elementy z listy, ale robią to inaczej:

|Cecha|`del a[i]`|`a.pop(i)`|
|---|:-:|:-:|
|Usuwa element|✅|✅|
|Zwraca usuniętą wartość|❌|✅|
|Usuwa slice|✅|❌|
|Usuwa zmienną|✅|❌|

> 💡 Używaj `pop()` gdy chcesz **pobrać i usunąć** element. Używaj `del` gdy chcesz go **po prostu usunąć**.

---

### 💡 Usuwanie elementów po indeksie

```python
a = [-1, 1, 66.25, 333, 333, 1234.5]

del a[0]        # usuń element na pozycji 0
print(a)        # [1, 66.25, 333, 333, 1234.5]
```

---

### ✂️ Usuwanie slice'ów

`del` potrafi usunąć **cały wycinek** listy naraz:

```python
a = [1, 66.25, 333, 333, 1234.5]

del a[2:4]      # usuń elementy od indeksu 2 do 3 (włącznie)
print(a)        # [1, 66.25, 1234.5]
```

```
PRZED:  [1,  66.25,  333,  333,  1234.5]
                     ↑     ↑
                  del a[2:4]  — usuwamy te dwa

PO:     [1,  66.25,  1234.5]
```

---

### 🧹 Czyszczenie całej listy

```python
a = [1, 66.25, 1234.5]

del a[:]        # usuń wszystkie elementy (lista nadal istnieje)
print(a)        # []
```

Porównanie z podobnymi operacjami:

```python
del a[:]        # czyści listę — obiekt nadal istnieje pod nazwą 'a'
a.clear()       # to samo — metoda listy
a = []          # przypisuje nową pustą listę (poprzednia może nadal istnieć w pamięci)
```

---

### 💣 Usuwanie całej zmiennej

`del` może usunąć nie tylko element — ale całą **nazwę zmiennej** z przestrzeni nazw:

```python
a = [1, 2, 3]
del a           # zmienna 'a' przestaje istnieć

print(a)        # NameError: name 'a' is not defined
```

> ⚠️ Po `del a` — nazwa `a` znika. Odwołanie do niej jest błędem **dopóki nie zostanie jej przypisana nowa wartość**.

```python
del a           # usuwa nazwę
a = [4, 5, 6]  # teraz 'a' znowu istnieje — zupełnie nowy obiekt
```

---

### 🗺️ Podsumowanie — co `del` może usunąć

```python
a = [1, 2, 3, 4, 5]

del a[0]        # pojedynczy element   → [2, 3, 4, 5]
del a[1:3]      # slice                → [2, 5]
del a[:]        # cała zawartość       → []
del a           # cała zmienna         → NameError przy próbie dostępu
```

---

## 📦 Krotki (Tuples)

> Niemutowalna sekwencja — idealna gdy dane mają być stałe, logicznie powiązane i szybkie.

---

### 📌 Czym jest krotka?

Krotka to **niemutowalna sekwencja** wartości rozdzielonych przecinkami. W odróżnieniu od listy — raz stworzonej krotki **nie można zmienić**.

```python
t = 12345, 54321, 'hello!'   # tworzenie krotki (bez nawiasów!)
print(t)                      # (12345, 54321, 'hello!')
print(t[0])                   # 12345
```

Python automatycznie otacza krotkę nawiasami przy wyświetlaniu — dla czytelności przy zagnieżdżaniu.

---

### 🧩 Tworzenie krotek

```python
# Bez nawiasów — Python sam "widzi" krotkę
t = 1, 2, 3

# Z nawiasami — czytelniej, często wymagane
t = (1, 2, 3)

# Zagnieżdżona krotka
u = t, (4, 5, 6)
# → ((1, 2, 3), (4, 5, 6))
```

#### ⚠️ Krotka pusta i jednoelementowa — pułapki składniowe

```python
# Pusta krotka — puste nawiasy
empty = ()
len(empty)      # → 0

# Krotka jednoelementowa — WYMAGANY przecinek na końcu!
singleton = 'cześć',     # ← przecinek jest kluczowy
len(singleton)           # → 1
print(singleton)         # → ('cześć',)

# To NIE jest krotka — to po prostu string w nawiasach
nie_krotka = ('cześć')
type(nie_krotka)         # → <class 'str'>
```

```
'cześć'    → str
('cześć')  → str   ← nawiasy nie tworzą krotki!
('cześć',) → tuple ← przecinek tworzy krotkę
'cześć',   → tuple ← nawiasy opcjonalne
```

---

### 🔒 Niemutowalność — co to znaczy?

```python
t = (1, 2, 3)

t[0] = 99
# ❌ TypeError: 'tuple' object does not support item assignment
```

Elementów krotki **nie można zmieniać, dodawać ani usuwać** po jej utworzeniu.

#### Ale uwaga — krotka może zawierać mutowalne obiekty!

```python
v = ([1, 2, 3], [4, 5, 6])

v[0].append(99)   # ✅ modyfikujemy listę WEWNĄTRZ krotki
print(v)          # ([1, 2, 3, 99], [4, 5, 6])

v[0] = [9, 9, 9]  # ❌ TypeError — nie możemy podmienić samej listy
```

Krotka pilnuje **referencji** do obiektów — nie może ich zmienić, ale same obiekty mogą się zmieniać wewnętrznie:

```
v = ( [1, 2, 3] , [4, 5, 6] )
       ↑               ↑
   referencja       referencja
   (stała)          (stała)
       ↓
   [1, 2, 3, 99]   ← zawartość może się zmienić, referencja ta sama
```

---

### 📦 Pakowanie i rozpakowywanie

#### Pakowanie krotki

```python
t = 12345, 54321, 'hello!'   # trzy wartości "spakowane" w krotkę
```

#### Rozpakowywanie krotki

```python
x, y, z = t   # trzy zmienne otrzymują odpowiednie wartości

print(x)   # 12345
print(y)   # 54321
print(z)   # 'hello!'
```

Liczba zmiennych po lewej musi **dokładnie odpowiadać** liczbie elementów sekwencji:

```python
a, b = (1, 2, 3)   # ❌ ValueError: too many values to unpack
a, b, c, d = (1, 2, 3)   # ❌ ValueError: not enough values to unpack
a, b, c = (1, 2, 3)      # ✅
```

#### Rozpakowywanie z `*` — reszta do jednej zmiennej

```python
first, *rest = (1, 2, 3, 4, 5)
# first = 1
# rest  = [2, 3, 4, 5]

*beginning, last = (1, 2, 3, 4, 5)
# beginning = [1, 2, 3, 4]
# last = 5
```

#### Wielokrotne przypisanie — pakowanie i rozpakowywanie w jednym

```python
a, b = 1, 2   # to jest pakowanie (1, 2) + rozpakowywanie do a, b
```

Klasyczne zastosowanie — zamiana wartości bez zmiennej tymczasowej:

```python
a, b = b, a   # Python najpierw pakuje (b, a) w krotkę, potem rozpakowuje
```

---

### 📤 Rozpakowywanie w krotkach

Tak jak w listach, `*` działa też przy tworzeniu krotek:

```python
x = [1, 2, 3]
wynik = 0, *x, 4
# → (0, 1, 2, 3, 4)
```

---

### ⚖️ Krotka vs Lista — kiedy co używać?

|Kryterium|Krotka `(1, 2, 3)`|Lista `[1, 2, 3]`|
|---|:-:|:-:|
|Mutowalność|❌ Niemutowalna|✅ Mutowalna|
|Elementy zazwyczaj|Heterogeniczne (różne typy)|Homogeniczne (ten sam typ)|
|Dostęp do danych|Przez indeks / rozpakowywanie|Przez iterację|
|Użycie jako klucz słownika|✅ Tak|❌ Nie|
|Wydajność pamięci|✅ Mniejsza|Większa|

#### Praktyczna zasada

```python
# Lista — kolekcja podobnych elementów do przetworzenia
owoce = ['jabłko', 'banan', 'gruszka']
for owoc in owoce: ...

# Krotka — logicznie powiązane wartości różnych typów
punkt = (10.5, 20.3)
osoba = ('Jan', 'Kowalski', 1985)
kolor_rgb = (255, 128, 0)
```

---

## 🔵 Zbiory (Sets)

> Nieuporządkowana kolekcja unikalnych elementów — do eliminowania duplikatów i operacji matematycznych na zbiorach.

---

### 📌 Czym jest zbiór?

Zbiór to kolekcja, która:

- **nie zawiera duplikatów** — każdy element może wystąpić tylko raz
- **jest nieuporządkowana** — brak gwarancji kolejności elementów
- **jest mutowalna** — można dodawać i usuwać elementy

Klasyczne zastosowania:

```
✅ Szybkie sprawdzanie czy element należy do kolekcji
✅ Usuwanie duplikatów z listy
✅ Operacje matematyczne: suma, iloczyn, różnica zbiorów
```

---

### 🧩 Tworzenie zbiorów

```python
# Nawiasy klamrowe — jeden lub więcej elementów
basket = {'jabłko', 'pomarańcza', 'gruszka', 'banan'}

# Duplikaty są automatycznie usuwane!
basket = {'jabłko', 'pomarańcza', 'jabłko', 'gruszka', 'pomarańcza', 'banan'}
print(basket)   # {'pomarańcza', 'banan', 'gruszka', 'jabłko'}

# Funkcja set() — z dowolnego iterable
a = set('abrakadabra')   # unikalne litery
print(a)                 # {'a', 'r', 'b', 'k', 'd'}
```

#### ⚠️ Pusta krotka — obowiązkowo `set()` !

```python
pusty_zbior = set()   # ✅ pusty zbiór
pusty_slownik = {}    # ❌ to jest pusty SŁOWNIK, nie zbiór!
```

```
{}    → dict   ← Python interpretuje zawsze jako słownik
set() → set    ← jedyna poprawna forma pustego zbioru
```

---

### 🔍 Sprawdzanie zawierania — szybsze niż lista!

```python
basket = {'jabłko', 'pomarańcza', 'gruszka', 'banan'}

'pomarańcza' in basket   # → True
'wiechlina' in basket    # → False
```

Sprawdzanie `in` dla zbioru jest **znacznie szybsze** niż dla listy — zbiory używają tablic mieszających (hash tables), więc czas wyszukiwania jest stały niezależnie od rozmiaru zbioru:

|Struktura|Czas sprawdzania `in`|
|---|---|
|`list`|O(n) — rośnie liniowo|
|`set`|O(1) — zawsze stały|

---

### ➕➖ Operacje matematyczne na zbiorach

```python
a = set('abrakadabra')   # {'a', 'r', 'b', 'k', 'd'}
b = set('alakazam')      # {'a', 'l', 'k', 'z', 'm'}
```

```python
a - b    # RÓŻNICA — litery w a, których nie ma w b
         # {'r', 'd', 'b'}

a | b    # SUMA — litery w a lub b (lub w obu)
         # {'a', 'k', 'r', 'd', 'b', 'm', 'z', 'l'}

a & b    # ILOCZYN — litery obecne w obu
         # {'a', 'k'}

a ^ b    # RÓŻNICA SYMETRYCZNA — litery w a lub b, ale nie w obu
         # {'r', 'd', 'b', 'm', 'z', 'l'}
```

#### Wizualizacja operacji (diagramy Venna)

```
        a = {a, r, b, k, d}      b = {a, l, k, z, m}

        ┌──────────┐  ┌──────────┐
a - b:  │ r, d, b  │  │          │     tylko lewa strona
        └──────────┘  └──────────┘

        ┌──────────────────────────┐
a | b:  │ a, r, b, k, d, l, z, m  │   obie strony łącznie
        └──────────────────────────┘

              ┌──────┐
a & b:        │ a, k │                 tylko część wspólna
              └──────┘

        ┌──────────┐  ┌──────────┐
a ^ b:  │ r, d, b  │  │ l, z, m  │   wszystko POZA częścią wspólną
        └──────────┘  └──────────┘
```

---

### ✏️ Modyfikowanie zbioru — mutacje

Zbiór jest mutowalny — możesz go dowolnie rozbudowywać i przycinać po utworzeniu.

#### Dodawanie elementów

```python
s = {'jabłko', 'banan'}

# Dodaj jeden element
s.add('gruszka')
print(s)   # {'jabłko', 'banan', 'gruszka'}

# Dodaj wiele elementów naraz (z dowolnego iterable)
s.update(['kiwi', 'mango'])
print(s)   # {'jabłko', 'banan', 'gruszka', 'kiwi', 'mango'}

# Dodanie duplikatu — nic się nie dzieje
s.add('banan')
print(s)   # bez zmian — 'banan' już jest w zbiorze
```

#### Usuwanie elementów

```python
s = {'jabłko', 'banan', 'gruszka', 'kiwi'}

# remove() — rzuca KeyError jeśli elementu nie ma
s.remove('banan')    # ✅ usuwa 'banan'
s.remove('mango')    # ❌ KeyError: 'mango'

# discard() — bezpieczne, nie rzuca błędu
s.discard('kiwi')    # ✅ usuwa 'kiwi'
s.discard('mango')   # ✅ nic się nie dzieje — brak błędu

# pop() — usuwa i zwraca losowy element
element = s.pop()    # usuwa i zwraca dowolny element
print(element)       # nie wiesz który — zbiór jest nieuporządkowany!

# clear() — czyści cały zbiór
s.clear()
print(s)   # set()
```

#### Kiedy używać `remove()` a kiedy `discard()`?

```python
# remove() — gdy brak elementu to BUG — chcesz wiedzieć o błędzie
s.remove('wymagany_element')

# discard() — gdy element może, ale nie musi istnieć
s.discard('opcjonalny_element')
```

#### Operacje modyfikujące zbiór w miejscu

Odpowiedniki operatorów `|`, `&`, `-`, `^` które **zmieniają zbiór w miejscu** zamiast tworzyć nowy:

```python
a = {'a', 'b', 'c'}
b = {'b', 'c', 'd'}

a |= b    # a = a | b — suma (dodaj elementy z b do a)
# a → {'a', 'b', 'c', 'd'}

a &= b    # a = a & b — iloczyn (zostaw tylko wspólne)
# a → {'b', 'c', 'd'}

a -= b    # a = a - b — różnica (usuń elementy b z a)
# a → {'a'}

a ^= b    # a = a ^ b — różnica symetryczna
# a → {'a', 'd'}
```

|Operator|Metoda|Co robi|
|---|---|---|
|`\|=`|`update()`|Dodaje elementy z innego zbioru|
|`&=`|`intersection_update()`|Zostają tylko wspólne elementy|
|`-=`|`difference_update()`|Usuwa elementy obecne w drugim zbiorze|
|`^=`|`symmetric_difference_update()`|Zostają elementy tylko z jednego zbioru|

---

### ⚡ Wyrażenia zbiorowe (Set Comprehensions)

Zbiory obsługują wyrażenia analogiczne do wyrażeń listowych:

```python
# Filtrowanie liter
a = {x for x in 'abracadabra' if x not in 'abc'}
# → {'r', 'd'}
```

#### Rozpakowywanie w wyrażeniach zbiorowych

```python
fruits = [{'apple', 'avocado', 'apricot'}, {'banana', 'blueberry'}]

{*fruit for fruit in fruits}
# → {'blueberry', 'banana', 'avocado', 'apple', 'apricot'}
```

Każda wewnętrzna lista/zbiór jest **rozpakowywana** — elementy ze wszystkich grup trafiają do jednego zbioru, a duplikaty automatycznie znikają.

---

### 🚫 Czego zbiory nie potrafią

```python
s = {1, 2, 3}

s[0]           # ❌ TypeError — zbiory nie obsługują indeksowania
s[0] = 5       # ❌ TypeError — ani przypisania przez indeks
sorted(s)      # ✅ ale możesz posortować do nowej listy
list(s)        # ✅ lub skonwertować
```

Zbiory są nieuporządkowane — **nie ma "pierwszego" ani "ostatniego" elementu**.

---

### ⚖️ Zbiór vs Lista vs Krotka

|Cecha|`set`|`list`|`tuple`|
|---|:-:|:-:|:-:|
|Duplikaty|❌ Nie|✅ Tak|✅ Tak|
|Kolejność|❌ Nieuporządkowany|✅ Zachowana|✅ Zachowana|
|Indeksowanie|❌|✅|✅|
|Mutowalność|✅|✅|❌|
|Sprawdzanie `in`|✅ O(1)|❌ O(n)|❌ O(n)|
|Operacje zbiorowe|✅|❌|❌|

---

### 💡 Praktyczne zastosowania

```python
# Usuwanie duplikatów z listy
lista = [1, 2, 2, 3, 3, 3, 4]
unikalne = list(set(lista))   # [1, 2, 3, 4]

# Sprawdzanie wspólnych elementów dwóch list
lista_a = ['a', 'b', 'c', 'd']
lista_b = ['c', 'd', 'e', 'f']
wspolne = set(lista_a) & set(lista_b)   # {'c', 'd'}

# Elementy tylko w jednej liście
tylko_w_a = set(lista_a) - set(lista_b)   # {'a', 'b'}
```

---

## 🗂️ Słowniki (Dictionaries)

> Klucz → Wartość. Najbardziej wszechstronna struktura danych w Pythonie.

---

### 📌 Czym jest słownik?

Słownik to kolekcja par **klucz: wartość**, gdzie każdy klucz jest unikalny. W przeciwieństwie do list (indeksowanych liczbami), słowniki są indeksowane **kluczami dowolnego niemutowalnego typu**.

```
lista:    [0]  [1]   [2]       ← indeks: liczba
          "Jan" 25   "Kraków"

słownik: {"imię": "Jan", "wiek": 25, "miasto": "Kraków"}
              ↑               ↑
           klucz           wartość
```

---

### 🧩 Tworzenie słowników

### Nawiasy klamrowe — podstawowa forma

```python
# Pusty słownik
d = {}

# Słownik z wartościami początkowymi
tel = {'jack': 4098, 'sape': 4139}
```

#### Konstruktor `dict()` — z listy krotek

```python
dict([('sape', 4139), ('guido', 4127), ('jack', 4098)])
# {'sape': 4139, 'guido': 4127, 'jack': 4098}
```

#### Konstruktor `dict()` — z argumentów nazwanych

```python
dict(sape=4139, guido=4127, jack=4098)
# {'sape': 4139, 'guido': 4127, 'jack': 4098}
# Działa tylko gdy klucze są prostymi nazwami (bez spacji, myślników itd.)
```

#### Wyrażenia słownikowe (Dict Comprehensions)

```python
{x: x**2 for x in (2, 4, 6)}
# {2: 4, 4: 16, 6: 36}
```

#### Scalanie słowników przez rozpakowywanie `**`

```python
odds  = {i: i**2 for i in (1, 3, 5)}   # {1: 1, 3: 9, 5: 25}
evens = {i: i**2 for i in (2, 4, 6)}   # {2: 4, 4: 16, 6: 36}

{**odds, **evens}
# {1: 1, 3: 9, 5: 25, 2: 4, 4: 16, 6: 36}
```

Działa też z wyrażeniami słownikowymi — przydatne gdy słowniki są w liście:

```python
all_dicts = [odds, evens, {0: 0}]
{**d for d in all_dicts}
# {1: 1, 3: 9, 5: 25, 2: 4, 4: 16, 6: 36, 0: 0}
```

---

### 🔑 Jakie typy mogą być kluczami?

Klucz musi być **niemutowalny** — Python musi móc wyliczyć stały hash dla klucza.

|Typ|Jako klucz?|Przykład|
|---|:-:|---|
|`str`|✅|`{"imię": "Jan"}`|
|`int`, `float`|✅|`{1: "jeden"}`|
|`tuple` (z niemutowalnymi)|✅|`{(1, 2): "punkt"}`|
|`tuple` (z listą w środku)|❌|`{([1], 2): ...}` → TypeError|
|`list`|❌|`{[1, 2]: ...}` → TypeError|
|`dict`|❌|`{{}: ...}` → TypeError|
|`set`|❌|`{{1, 2}: ...}` → TypeError|

---

### ✏️ Podstawowe operacje

#### Odczyt i zapis

```python
tel = {'jack': 4098, 'sape': 4139}

# Dodawanie i modyfikacja
tel['guido'] = 4127       # nowy klucz
tel['jack'] = 9999        # nadpisuje istniejący — stara wartość znika!

# Odczyt
tel['jack']               # → 9999

# Odczyt nieistniejącego klucza
tel['irv']                # ❌ KeyError: 'irv'
tel.get('irv')            # ✅ → None  (brak błędu)
tel.get('irv', 0)         # ✅ → 0     (własna wartość domyślna)
```

#### Usuwanie

```python
del tel['sape']           # usuwa parę klucz: wartość
```

#### Sprawdzanie kluczy

```python
'guido' in tel            # → True
'jack' not in tel         # → False
```

#### Przeglądanie zawartości

```python
tel = {'jack': 4098, 'guido': 4127, 'irv': 4127}

list(tel)        # lista kluczy w kolejności wstawiania
# ['jack', 'guido', 'irv']

sorted(tel)      # posortowana lista kluczy
# ['guido', 'irv', 'jack']
```

---

### ✏️ Modyfikowanie słownika — mutacje

#### Dodawanie i aktualizacja

```python
d = {'a': 1, 'b': 2}

# Jeden klucz
d['c'] = 3                      # {'a': 1, 'b': 2, 'c': 3}

# Wiele kluczy naraz — z innego słownika lub listy krotek
d.update({'d': 4, 'e': 5})      # {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'e': 5}
d.update(f=6, g=7)              # można też przez argumenty nazwane

# Dodaj klucz TYLKO jeśli nie istnieje
d.setdefault('a', 99)           # 'a' już istnieje → zwraca 1, nic nie zmienia
d.setdefault('z', 99)           # 'z' nie istnieje → dodaje z: 99
```

#### Usuwanie elementów

```python
d = {'a': 1, 'b': 2, 'c': 3}

del d['b']                      # usuwa klucz 'b'

d.pop('c')                      # usuwa i ZWRACA wartość → 3
d.pop('x')                      # ❌ KeyError
d.pop('x', 'brak')              # ✅ zwraca 'brak' jeśli klucz nie istnieje

d.popitem()                     # usuwa i zwraca ostatnią parę (klucz, wartość)
                                # w starszych Pythonach — losową!

d.clear()                       # usuwa wszystkie elementy → {}
```

#### Przegląd metod mutacji

|Metoda|Co robi|Rzuca błąd?|
|---|---|:-:|
|`d[k] = v`|Dodaje lub nadpisuje|❌|
|`d.update(...)`|Dodaje/nadpisuje wiele|❌|
|`d.setdefault(k, v)`|Dodaje tylko jeśli brak klucza|❌|
|`del d[k]`|Usuwa klucz|✅ KeyError|
|`d.pop(k)`|Usuwa i zwraca wartość|✅ KeyError|
|`d.pop(k, domyślna)`|Usuwa i zwraca lub domyślną|❌|
|`d.popitem()`|Usuwa i zwraca ostatnią parę|✅ jeśli pusty|
|`d.clear()`|Czyści cały słownik|❌|

---

### 🔁 Iterowanie po słowniku

```python
d = {'imię': 'Jan', 'wiek': 25, 'miasto': 'Kraków'}

# Klucze (domyślnie)
for k in d:
    print(k)           # imię, wiek, miasto

# Wartości
for v in d.values():
    print(v)           # Jan, 25, Kraków

# Pary klucz-wartość
for k, v in d.items():
    print(f"{k}: {v}") # imię: Jan / wiek: 25 / miasto: Kraków
```

---

### 🔍 Bezpieczny dostęp — `get()` vs `[]`

```python
d = {'a': 1}

# Niebezpieczne — rzuca KeyError gdy klucz nie istnieje
d['b']            # ❌ KeyError

# Bezpieczne — zwraca None lub podaną wartość domyślną
d.get('b')        # → None
d.get('b', 0)     # → 0
d.get('a', 0)     # → 1 (klucz istnieje — zwraca prawdziwą wartość)
```

> 💡 Używaj `get()` zawsze gdy nie masz pewności czy klucz istnieje.

---

### 📋 Słownik jako licznik — klasyczny wzorzec

```python
tekst = "abrakadabra"
licznik = {}

for litera in tekst:
    licznik[litera] = licznik.get(litera, 0) + 1

print(licznik)
# {'a': 5, 'b': 2, 'r': 2, 'k': 1, 'd': 1}
```

---

## 🔁 Techniki pętli (Sekwencje i Słowniki)

> Python oferuje eleganckie wbudowane narzędzia do iterowania — bez ręcznych liczników i indeksów.

---

### 📌 Przegląd technik

|Technika|Kiedy używać|
|---|---|
|`items()`|Iterowanie po słowniku — klucz i wartość naraz|
|`enumerate()`|Iterowanie po sekwencji — indeks i wartość naraz|
|`zip()`|Równoczesne iterowanie po kilku sekwencjach|
|`reversed()`|Iterowanie od końca|
|`sorted()`|Iterowanie w posortowanej kolejności|
|`sorted(set(...))`|Iterowanie po unikalnych elementach w kolejności|

---

### 🗂️ `items()` — klucz i wartość ze słownika naraz

```python
knights = {'galahad': 'cnotliwy', 'robin': 'odważny'}

for k, v in knights.items():
    print(k, v)
```

```
galahad cnotliwy
robin odważny
```

Zamiast dwóch oddzielnych operacji — jedna, czytelna:

```python
# ❌ Niepotrzebnie skomplikowane
for k in knights:
    print(k, knights[k])

# ✅ Idiomatycznie
for k, v in knights.items():
    print(k, v)
```

---

### 🔢 `enumerate()` — indeks i wartość naraz

```python
for i, v in enumerate(['kółko', 'i', 'krzyżyk']):
    print(i, v)
```

```
0 kółko
1 i
2 krzyżyk
```

Możesz podać własny punkt startowy:

```python
for i, v in enumerate(['a', 'b', 'c'], start=1):
    print(i, v)
# 1 a / 2 b / 3 c
```

Zamiast `range(len(...))`:

```python
# ❌ Stary sposób — niepythonowy
for i in range(len(lista)):
    print(i, lista[i])

# ✅ Pythonowy
for i, v in enumerate(lista):
    print(i, v)
```

---

### 🤐 `zip()` — dwie sekwencje naraz

```python
questions = ['imię', 'misja', 'ulubiony kolor']
answers   = ['lancelot', 'święty graal', 'niebieski']

for q, a in zip(questions, answers):
    print(f'Jego {q} to {a}.')
```

```
Jego imię to lancelot.
Jego misja to święty graal.
Jego ulubiony kolor to niebieski.
```

`zip()` "szyje" sekwencje razem — jak zamek błyskawiczny:

```
questions: ['imię',     'misja',        'ulubiony kolor']
                 ↕           ↕                   ↕
answers:   ['lancelot', 'święty graal', 'niebieski'     ]

wynik:     [('imię', 'lancelot'), ('misja', 'święty graal'), ...]
```

> ⚠️ `zip()` zatrzymuje się na **krótszej** sekwencji. Jeśli chcesz iterować do końca dłuższej — użyj `itertools.zip_longest()`.

---

### ⏪ `reversed()` — iterowanie od końca

```python
for i in reversed(range(1, 10, 2)):
    print(i)
```

```
9  7  5  3  1
```

`reversed()` nie tworzy nowej listy — zwraca **iterator** (oszczędza pamięć). Działa na sekwencjach, które mają zdefiniowaną długość i indeksowanie (listy, krotki, napisy, `range`).

```python
# Odwrócenie listy bez tworzenia kopii
for item in reversed(moja_lista):
    ...

# Dla porównania — to tworzy nową listę
for item in moja_lista[::-1]:
    ...
```

---

### 🔤 `sorted()` — iterowanie w posortowanej kolejności

```python
basket = ['banan', 'jabłko', 'banan', 'pomarańcza', 'jabłko', 'gruszka']

for i in sorted(basket):
    print(i)
```

```
banan  banan  gruszka  jabłko  jabłko  pomarańcza
```

`sorted()` zwraca **nową posortowaną listę** — oryginał pozostaje niezmieniony. To kluczowa różnica względem `list.sort()`:

```python
sorted(lista)   # → nowa lista, oryginał bez zmian  ✅ bezpieczne
lista.sort()    # → modyfikuje oryginał             ⚠️ destruktywne
```

---

### 🎯 `sorted(set(...))` — unikalne elementy w kolejności

Klasyczny pythonowy idiom — eliminacja duplikatów **i** sortowanie w jednym:

```python
basket = ['banan', 'jabłko', 'banan', 'pomarańcza', 'jabłko', 'gruszka']

for f in sorted(set(basket)):
    print(f)
```

```
banan  gruszka  jabłko  pomarańcza
```

Krok po kroku:

```
basket       → ['banan', 'jabłko', 'banan', 'pomarańcza', 'jabłko', 'gruszka']
set(basket)  → {'banan', 'jabłko', 'pomarańcza', 'gruszka'}   ← bez duplikatów
sorted(...)  → ['banan', 'gruszka', 'jabłko', 'pomarańcza']   ← posortowane
```

---

### 🛡️ Nie modyfikuj listy podczas iterowania!

Zmiana listy w trakcie iterowania po niej może prowadzić do pominięcia elementów lub nieskończonej pętli. Zamiast tego — **utwórz nową listę**:

```python
import math

raw_data = [56.2, float('NaN'), 51.7, 55.3, 52.5, float('NaN'), 47.8]

# ✅ Bezpieczne — filtrujemy do nowej listy
filtered_data = []
for value in raw_data:
    if not math.isnan(value):
        filtered_data.append(value)

print(filtered_data)
# [56.2, 51.7, 55.3, 52.5, 47.8]
```

Lub jeszcze zwięźlej — jako list comprehension:

```python
filtered_data = [v for v in raw_data if not math.isnan(v)]
```

---

### 🔗 Łączenie technik

Techniki można swobodnie łączyć:

```python
# enumerate + zip — indeks i dwie wartości naraz
for i, (q, a) in enumerate(zip(questions, answers), start=1):
    print(f'{i}. {q}: {a}')

# sorted + enumerate — posortowane z indeksem
for i, owoc in enumerate(sorted(set(basket)), start=1):
    print(f'{i}. {owoc}')

# reversed + enumerate — od końca z indeksem
for i, v in enumerate(reversed(lista)):
    print(i, v)
```

---

## 🔍 Więcej na temat warunków

> Warunki w Pythonie to więcej niż proste porównania — poznaj pełną moc operatorów logicznych.

---

### 📌 Przegląd operatorów

| Operator                         | Typ                  | Opis                                    |
| -------------------------------- | -------------------- | --------------------------------------- |
| `==`, `!=`, `<`, `>`, `<=`, `>=` | Porównanie           | Porównuje wartości                      |
| `in`, `not in`                   | Należenie            | Sprawdza obecność w kontenerze          |
| `is`, `is not`                   | Tożsamość            | Sprawdza czy to ten sam obiekt          |
| `and`, `or`, `not`               | Logiczne             | Łączy i neguje wyrażenia boolowskie     |
| `:=`                             | Przypisanie (walrus) | Przypisuje i zwraca wartość w wyrażeniu |

---

### 🔎 `in` i `not in` — operatory należenia

Sprawdzają czy wartość **występuje** (lub nie) w kontenerze:

```python
'jabłko' in ['jabłko', 'banan', 'gruszka']   # → True
'mango' not in {'kiwi', 'banan'}              # → True
'a' in 'abrakadabra'                          # → True — działa też na napisach!
3 in range(1, 10)                             # → True
```

---

### 🪞 `is` i `is not` — operatory tożsamości

Sprawdzają czy dwie nazwy wskazują **dokładnie ten sam obiekt w pamięci** — nie tylko równe wartości:

```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

a == b    # → True  — wartości są równe
a is b    # → False — to dwa różne obiekty!
a is c    # → True  — c wskazuje na ten sam obiekt co a
```

```
a → [1, 2, 3]  ← obiekt #1
b → [1, 2, 3]  ← obiekt #2  (inny obiekt, ta sama wartość)
c ↗             ← c wskazuje na obiekt #1
```

> 💡 **Zasada:** używaj `==` do porównywania **wartości**, `is` do porównywania **tożsamości** (np. `is None`, `is True`, `is False`).

```python
# ✅ Poprawne użycie is
if x is None:
    ...
if x is not None:
    ...

# ❌ Pułapka — nie porównuj is dla liczb i napisów
x = 1000
y = 1000
x is y   # może być False! (zależy od implementacji)
x == y   # zawsze True — używaj tego
```

---

### 🔗 Łańcuchy porównań

Python pozwala łączyć porównania w łańcuchy — tak jak w matematyce:

```python
a < b == c        # a < b AND b == c
1 < 2 < 3         # → True
1 < 2 > 0         # → True
0 < x < 10        # czy x leży między 0 a 10?

# Odpowiednik bez łańcucha:
a < b and b == c
```

---

### 🧠 Operatory logiczne — `and`, `or`, `not`

#### Priorytety

```
Najwyższy priorytet:  not
                      and
Najniższy priorytet:  or
```

```python
A and not B or C
# równoważne: (A and (not B)) or C
# nie: A and (not (B or C))
```

#### Ewaluacja leniwa (short-circuit evaluation)

Python ocenia wyrażenia logiczne **od lewej do prawej** i **zatrzymuje się jak tylko wynik jest pewny**:

```python
# and — zatrzymuje się na pierwszym False
False and bardzo_wolna_funkcja()   # funkcja NIE jest wywoływana!

# or — zatrzymuje się na pierwszym True
True or bardzo_wolna_funkcja()    # funkcja NIE jest wywoływana!
```

```
A and B and C:
  A=False → STOP, wynik: False    (B i C nie sprawdzane)
  A=True  → sprawdź B
              B=False → STOP, wynik: False  (C nie sprawdzane)
              B=True  → sprawdź C → wynik: C
```

#### `and` i `or` zwracają wartość — nie tylko True/False!

Operatory `and` i `or` zwracają **ostatnio ewaluowany argument**, nie `True`/`False`:

```python
# or — zwraca pierwszy "prawdziwy" argument (lub ostatni jeśli wszystkie fałszywe)
'' or 'Trondheim' or 'Hammer Dance'   # → 'Trondheim'
0 or [] or 'coś'                      # → 'coś'
0 or [] or ''                         # → '' (wszystkie fałszywe — ostatni)

# and — zwraca pierwszy "fałszywy" argument (lub ostatni jeśli wszystkie prawdziwe)
1 and 2 and 3     # → 3   (wszystkie prawdziwe — ostatni)
1 and 0 and 3     # → 0   (pierwszy fałszywy)
```

#### Praktyczne zastosowanie — wartości domyślne

```python
string1, string2, string3 = '', 'Trondheim', 'Hammer Dance'

non_null = string1 or string2 or string3
# → 'Trondheim'  (pierwszy niepusty napis)
```

```
string1 = ''          → fałszywy, idź dalej
string2 = 'Trondheim' → prawdziwy → STOP, zwróć 'Trondheim'
string3 nie sprawdzany
```

---

### 🦆 Wartości prawdziwe i fałszywe

W Pythonie wiele obiektów może być bezpośrednio użytych jako warunek:

```python
# Fałszywe (falsy):
False, None, 0, 0.0, '', [], {}, set()

# Prawdziwe (truthy):
True, 1, -1, 'cokolwiek', [0], {'a': 1}, {0}
```

```python
lista = []
if not lista:       # zamiast: if len(lista) == 0
    print("Pusta!")

napis = "hello"
if napis:           # zamiast: if napis != ""
    print("Niepusty!")
```

---

### 🦭 Operator Walrus `:=`

Operator `:=` (zwany "walrus operator" od podobieństwa do oczu i kłów morsa 🦭) pozwala **przypisać i użyć wartości w jednym wyrażeniu**:

```python
# Bez walrusa — obliczasz dwa razy lub potrzebujesz dodatkowej linii
dane = pobierz_dane()
if dane:
    przetwórz(dane)

# Z walrusem — przypisanie i sprawdzenie w jednej linii
if dane := pobierz_dane():
    przetwórz(dane)
```

Szczególnie przydatny w pętlach:

```python
# Czytanie pliku partiami
while chunk := plik.read(1024):
    przetwórz(chunk)

# Zamiast:
chunk = plik.read(1024)
while chunk:
    przetwórz(chunk)
    chunk = plik.read(1024)
```

> ⚠️ W odróżnieniu od C, w Pythonie zwykłe `=` **nie może** być użyte wewnątrz wyrażenia — to celowa decyzja zapobiegająca błędom `if x = 5` zamiast `if x == 5`.

---

### 📋 Priorytety operatorów (od najwyższego)

```
Operatory numeryczne  (+, -, *, /)      ← najwyższy
Operatory porównania  (==, !=, <, > in, is...)
not
and
or                                      ← najniższy
```

```python
# Przykład — kolejność bez nawiasów
2 + 3 > 4 and not 1 == 2 or False
# → (((2+3) > 4) and (not (1==2))) or False
# → (True and True) or False
# → True
```

---

## ⚖️ Porównywanie sekwencji i innych typów

> Python porównuje sekwencje element po elemencie — jak słownik porównuje słowa.

---

### 📌 Porządek leksykograficzny

Porównywanie sekwencji działa jak **sortowanie słownikowe** — element po elemencie, od lewej do prawej:

```
1. Porównaj pierwsze elementy obu sekwencji
2. Jeśli są równe → przejdź do kolejnych
3. Jeśli się różnią → ten mniejszy decyduje o wyniku całego porównania
4. Jeśli jedna sekwencja skończyła się wcześniej → krótsza jest "mniejsza"
5. Jeśli wszystkie elementy są równe → sekwencje są równe
```

---

### 💡 Przykłady krok po kroku

```python
(1, 2, 3) < (1, 2, 4)
```

```
pozycja 0:  1 == 1  → równe, idź dalej
pozycja 1:  2 == 2  → równe, idź dalej
pozycja 2:  3 <  4  → RÓŻNE → wynik: True ✅
```

---

```python
(1, 2, 3, 4) < (1, 2, 4)
```

```
pozycja 0:  1 == 1  → równe, idź dalej
pozycja 1:  2 == 2  → równe, idź dalej
pozycja 2:  3 <  4  → RÓŻNE → wynik: True ✅
(czwarty element lewej krotki nie ma znaczenia — decyzja zapadła wcześniej)
```

---

```python
(1, 2) < (1, 2, -1)
```

```
pozycja 0:  1 == 1  → równe, idź dalej
pozycja 1:  2 == 2  → równe, idź dalej
lewa krotka skończyła się → krótsza jest mniejsza → True ✅
```

---

```python
(1, 2, 3) == (1.0, 2.0, 3.0)
```

```
pozycja 0:  1 == 1.0  → równe (int i float porównywane numerycznie)
pozycja 1:  2 == 2.0  → równe
pozycja 2:  3 == 3.0  → równe
wszystkie równe → True ✅
```

---

### 📋 Kompletna lista przykładów

```python
(1, 2, 3)             < (1, 2, 4)          # True — 3 < 4 na pozycji 2
[1, 2, 3]             < [1, 2, 4]          # True — działa też dla list
'ABC' < 'C' < 'Pascal' < 'Python'          # True — porównanie napisów
(1, 2, 3, 4)          < (1, 2, 4)          # True — 3 < 4 na pozycji 2
(1, 2)                < (1, 2, -1)         # True — krótsza jest mniejsza
(1, 2, 3)            == (1.0, 2.0, 3.0)    # True — int == float numerycznie
(1, 2, ('aa', 'ab'))  < (1, 2, ('abc', 'a'), 4)  # True — zagnieżdżone rekursywnie
```

---

### 🔤 Porównywanie napisów — Unicode

Napisy porównywane są **znak po znaku** według ich wartości w tablicy Unicode:

```python
'A' < 'B'    # True  — 65 < 66
'Z' < 'a'    # True  — 90 < 97 (wielkie litery przed małymi!)
'abc' < 'abd'  # True — 'c' < 'd' na pozycji 2
'ab' < 'abc'   # True — krótsza jest mniejsza
```

```
'ABC' < 'C' < 'Pascal' < 'Python'

'ABC' vs 'C':    'A'(65) < 'C'(67) → True
'C'   vs 'Pascal': 'C'(67) < 'P'(80) → True
'Pascal' vs 'Python': 'P'=='P', 'a'(97) < 'y'(121) → True
```

> ⚠️ Kolejność Unicode może zaskoczyć — `'Z' < 'a'` jest **prawdą**, bo wielkie litery mają niższe kody niż małe!

---

### 🔁 Porównywanie rekurencyjne — zagnieżdżone sekwencje

Gdy elementy sekwencji same są sekwencjami, porównanie odbywa się **rekursywnie**:

```python
(1, 2, ('aa', 'ab')) < (1, 2, ('abc', 'a'), 4)
```

```
pozycja 0:  1 == 1         → równe, idź dalej
pozycja 1:  2 == 2         → równe, idź dalej
pozycja 2:  ('aa', 'ab') vs ('abc', 'a')
              ↳ 'aa' vs 'abc':
                  'a' == 'a'  → równe
                  'a' <  'b'  → RÓŻNE → ('aa', 'ab') < ('abc', 'a') → True ✅
```

---

### ⚠️ Porównywanie różnych typów

#### Typy numeryczne — można mieszać

Liczby całkowite i zmiennoprzecinkowe są porównywane **numerycznie**:

```python
0 == 0.0    # True
1 < 1.5     # True
3 == 3.0    # True
```

#### Inne typy — ostrożnie!

Porównywanie `<` lub `>` między niekompatybilnymi typami rzuca `TypeError`:

```python
'tekst' < 42          # ❌ TypeError — napis vs liczba
[1, 2] < (1, 2)       # ❌ TypeError — lista vs krotka
```

```python
# ✅ Możliwe gdy typ definiuje metody porównania
from decimal import Decimal
Decimal('1.5') < 2.0   # może działać — zależy od implementacji
```

> 💡 Python nie wymyśla arbitralnej kolejności dla nieporównywalnych typów — zamiast tego rzuca błąd. To celowa decyzja zapobiegająca cichym błędom.

---

### 📋 Zasady w pigułce

|Sytuacja|Wynik|
|---|---|
|Pierwszy różny element decyduje|`(1, 2, **3**) < (1, 2, **4**)` → True|
|Krótsza sekwencja jest mniejsza|`(1, 2) < (1, 2, 99)` → True|
|Wszystkie elementy równe → równe|`(1, 2) == (1.0, 2.0)` → True|
|Zagnieżdżone — porównanie rekursywne|element po elemencie w głąb|
|Różne typy sekwencji|`TypeError`|
|Mieszane typy numeryczne|porównanie numeryczne|

---


<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>



<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>


<div align="center">

# Modules

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Temat](https://img.shields.io/badge/temat-modules-3776AB?style=for-the-badge)

</div>

---

Rozdział 06 skupia się na modułach i pakietach w Pythonie i praktycznym operowaniu na:

> ⌲ importowaniu modułów
>
> ⌲ wzorcu `__main__`
>
> ⌲ ścieżce wyszukiwania `sys.path`
>
> ⌲ pakietach i importach względnych
>
> ⌲ kontroli publicznego API (`__all__`)

---

## 📦 Czym jest moduł?

> Moduł to zwykły plik `.py` — najprostszy sposób, żeby podzielić kod na części wielokrotnego użytku.

---

### 📌 Co to jest?

Moduł = plik `.py`.  
To wszystko.

Masz funkcję, której używasz w kilku miejscach? Zamiast ją kopiować wszędzie, wrzucasz ją do osobnego pliku. Ten plik to właśnie moduł.

```python
# plik: rabaty.py  ← to jest moduł

def oblicz_rabat(cena, procent):
    return cena * (1 - procent / 100)
```

```python
# plik: main.py  ← tutaj go używasz

import rabaty

cena_po_rabacie = rabaty.oblicz_rabat(200, 15)
print(cena_po_rabacie)  # → 170.0
```

---

### 🔬 Jak to działa pod spodem?

Każdy moduł ma swoją własną **przestrzeń nazw** (`namespace`).  
To izolowane środowisko — zmienne i funkcje zdefiniowane w module `rabaty` nie kolidują z tymi w Twoim skrypcie.

```python
# rabaty.py
podatek = 0.23  # ta zmienna żyje w przestrzeni nazw "rabaty"

# main.py
import rabaty
podatek = 0.08  # ta zmienna żyje w przestrzeni nazw "main"

print(podatek)          # → 0.08  (lokalna)
print(rabaty.podatek)   # → 0.23  (z modułu)
# zero konfliktu!
```

Moduł ma też specjalną zmienną `__name__` — przechowuje nazwę modułu jako string:

```python
import rabaty
print(rabaty.__name__)  # → 'rabaty'
```

---

### 🏗️ Co warto wiedzieć projektując system?

Python ładuje każdy moduł **tylko raz** na sesję interpretera — wynik trafia do `sys.modules` (słownik). Kolejny `import` tego samego modułu po prostu zwraca obiekt z cache'u.  
To ma istotne implikacje:

```python
import sys

import rabaty
print(id(rabaty))      # → 140234...

import rabaty as r2
print(id(r2))          # → 140234...  (TEN SAM obiekt!)

print('rabaty' in sys.modules)  # → True
```

**Implikacja:** mutacja stanu modułu jest globalna.

```python
# moduł config.py
DEBUG = False

# gdzieś w kodzie:
import config
config.DEBUG = True  # zmiana widoczna WSZĘDZIE gdzie importowany jest config
```

To pattern używany celowo (np. Django settings), ale może być źródłem trudnych do debugowania bugów w dużych systemach.

---

## 🔌 Sposoby importowania

> Cztery warianty instrukcji `import` — każdy ma swoje miejsce, a jeden prawie nigdy.

---

### 🧩 Jakie mam opcje?

```python
# Wariant 1: importuj cały moduł
import os
os.getcwd()           # musisz pisać nazwę modułu za każdym razem

# Wariant 2: importuj konkretne rzeczy
from os import getcwd
getcwd()              # krócej, ale skąd to pochodzi! nieoczywiste

# Wariant 3: importuj z aliasem
import numpy as np
np.array([1, 2, 3])  # skrócona nazwa — konwencja w ekosystemie

# Wariant 4: importuj element z aliasem
from datetime import datetime as dt
dt.now()
```

---

### ⚖️ Kiedy co stosować?

|Wzorzec|Kiedy używać|Przykład|
|---|---|---|
|`import modul`|duże moduły, chcesz jasności skąd co pochodzi|`import os`|
|`from modul import X`|często używasz X, nazwa jest jednoznaczna|`from pathlib import Path`|
|`import modul as alias`|długie nazwy lub konwencja ekosystemu|`import pandas as pd`|
|`from modul import *`|**prawie nigdy** — tylko sesje interaktywne|-|

```python
# ✅ Dobra praktyka — od razu wiadomo że to z biblioteki standardowej
import os
import json
import pathlib

# ✅ Dobra praktyka — konwencja ekosystemu data science
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# ✅ OK — jeśli funkcja jest często używana i nazwa nie koliduje
from datetime import datetime, timedelta

# ❌ Unikaj — zaśmieca namespace, ukrywa zależności
from os import *
from datetime import *
```

---

### ⚠️ Pułapki i edge cases

#### 🔹 Problem z cyklicznymi importami

```python
# a.py
from b import funkcja_b   # Python próbuje załadować b...

# b.py
from a import funkcja_a   # ...ale b próbuje załadować a, które jest w trakcie ładowania!
# → ImportError: cannot import name 'funkcja_a' from partially initialized module 'a'
```

Rozwiązania: przenieś import na dół funkcji, wydziel wspólny kod do trzeciego modułu, lub zrestrukturyzuj architekturę.

---

#### 🔹 Lazy imports dla wydajności

```python
# Zamiast importować ciężki moduł na starcie...
import heavy_ml_library  # 3 sekundy ładowania przy starcie CLI

# Importuj tylko gdy faktycznie potrzebny
def train_model(data):
    import heavy_ml_library  # ładuje się tylko przy wywołaniu tej funkcji
    return heavy_ml_library.train(data)
```

---

## ⚙️ Wzorzec `__main__`

> Jeden plik, dwie role — moduł do importowania i skrypt do uruchamiania.

---

### 📌 Co to robi?

Ten blok kodu uruchomi się **tylko** gdy uruchomisz plik bezpośrednio. Gdy plik jest importowany — ten blok jest ignorowany.

```python
# plik: kalkulator.py

def dodaj(a, b):
    return a + b

if __name__ == "__main__":
    # ten kod NIE wykona się przy 'import kalkulator'
    wynik = dodaj(10, 5)
    print(f"10 + 5 = {wynik}")
```

```bash
python kalkulator.py  # → "10 + 5 = 15"
```

```python
import kalkulator     # nic nie wypisuje, tylko ładuje funkcje
kalkulator.dodaj(3, 4)  # → 7
```

---

### 💡 Typowe zastosowania

#### 🔹 Zastosowanie 1: szybkie testy bez test framework

```python
# utils/stringi.py

def slug(tekst):
    return tekst.lower().replace(" ", "-")

def skroc(tekst, dlugosc=100):
    return tekst[:dlugosc] + "..." if len(tekst) > dlugosc else tekst

if __name__ == "__main__":
    # Szybki smoke test — uruchom: python utils/stringi.py
    assert slug("Hello World") == "hello-world"
    assert skroc("abc", 2) == "ab..."
    print("✓ Wszystkie testy przeszły")
```

---

#### 🔹 Zastosowanie 2: CLI do modułu

```python
# analizator.py

def analizuj_plik(sciezka):
    with open(sciezka) as f:
        zawartosc = f.read()
    return {"znaki": len(zawartosc), "linie": zawartosc.count("\n")}

if __name__ == "__main__":
    import sys
    if len(sys.argv) != 2:
        print("Użycie: python analizator.py <plik>")
        sys.exit(1)
    wyniki = analizuj_plik(sys.argv[1])
    print(f"Znaki: {wyniki['znaki']}, Linie: {wyniki['linie']}")
```

```bash
python analizator.py raport.txt  # → Znaki: 4521, Linie: 87
```

---

### 🏗️ Wzorzec w dużych projektach

W profesjonalnych projektach `if __name__ == "__main__"` deleguje do funkcji `main()`:

```python
# src/crawler.py

import argparse
import logging

def main() -> None:
    parser = argparse.ArgumentParser(description="Web crawler")
    parser.add_argument("url", help="Startowy URL")
    parser.add_argument("--depth", type=int, default=3)
    parser.add_argument("--verbose", action="store_true")
    args = parser.parse_args()

    if args.verbose:
        logging.basicConfig(level=logging.DEBUG)

    crawl(args.url, depth=args.depth)

if __name__ == "__main__":
    main()
```

Dlaczego `main()` jako osobna funkcja?

- testowalna (`from crawler import main; main()`)
- definiowalna jako `entry_point` w `pyproject.toml`
- łatwiejsza obsługa wyjątków (`sys.exit(main())`)

```toml
# pyproject.toml
[project.scripts]
crawler = "src.crawler:main"   # pip install -e . → polecenie 'crawler' w PATH
```

---

## 🗺️ Jak Python szuka modułów (`sys.path`)

> `import cos` to przeszukiwanie listy katalogów — i kolejność tej listy ma znaczenie.

---

### 📌 Skąd Python bierze moduły?

Gdy piszesz `import cos`, Python szuka w kolejności:

```
1. Moduły wbudowane w interpreter (sys, os, math...)
2. Twój bieżący folder
3. Zainstalowane biblioteki (pip install X ląduje tutaj)
```

```python
# Sprawdź gdzie Python szuka:
import sys
for p in sys.path:
    print(p)

# /home/user/moj_projekt      ← twój folder
# /usr/lib/python3.12         ← biblioteka standardowa
# /usr/lib/python3/dist-packages  ← pip packages
```

---

### ⚠️ Pułapki i PYTHONPATH

> ⚠️ **Klasyczna pułapka dla początkujących:**

```
moj_projekt/
├── random.py       ← TY to stworzyłeś
└── main.py
```

```python
# main.py
import random
random.shuffle([1, 2, 3])
# AttributeError: module 'random' has no attribute 'shuffle'
# Python użył TWOJEGO random.py zamiast wbudowanego!
```

**Zmienna `PYTHONPATH`** — możesz dodać swoje katalogi na stałe:

```bash
# Linux/Mac
export PYTHONPATH="/moje/biblioteki:$PYTHONPATH"

# Windows
set PYTHONPATH=C:\moje\biblioteki;%PYTHONPATH%
```

```python
# Lub dynamicznie w kodzie (przydatne w skryptach)
import sys
sys.path.insert(0, '/moje/biblioteki')  # insert(0,...) daje priorytet
```

---

### 🏗️ Zarządzanie środowiskami

W profesjonalnych projektach **nigdy** nie manipulujesz `sys.path` ręcznie. Zamiast tego:

```bash
# Stwórz izolowane środowisko
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows

# Zainstaluj zależności
pip install -r requirements.txt
```

Dla własnych pakietów — instalacja w trybie editable:

```bash
# pyproject.toml lub setup.py musi istnieć
pip install -e .
# teraz 'import moj_pakiet' działa wszędzie w tym venv
```

Sprawdzenie skąd pochodzi moduł (przydatne przy debugowaniu konfliktów):

```python
import requests
print(requests.__file__)
# → /home/user/.venv/lib/python3.12/site-packages/requests/__init__.py
```

---

## ⚡ Pliki `.pyc` i cache

> Python kompiluje moduły do bytecode'u i zapamiętuje wynik — żeby kolejne ładowanie było szybsze.

---

### 📌 Czym jest `__pycache__`?

Widzisz ten folder po pierwszym uruchomieniu? To normalnie.

```
moj_projekt/
├── utils.py
└── __pycache__/
    └── utils.cpython-312.pyc  ← Python tworzy automatycznie
```

Python kompiluje Twój kod do bytecode'u i zapisuje go — następnym razem załaduje szybciej. **Nie musisz tego ruszać.** Możesz dodać do `.gitignore`:

```gitignore
__pycache__/
*.pyc
*.pyo
```

---

### 🔬 Jak to działa?

Python sprawdza sygnaturę pliku źródłowego (timestamp lub hash) i automatycznie rekompiluje jeśli zmieniłeś kod. To całkowicie transparentny mechanizm.

```
utils.py zmieniony? → Python widzi zmianę → rekompiluje → nadpisuje .pyc
utils.py niezmieniony? → Python ładuje .pyc bezpośrednio (szybciej)
```

> 💡 **Ważne:** `.pyc` przyspiesza tylko **ładowanie** modułu, nie jego wykonanie. Twój kod nie działa szybciej — interpreter ładuje go szybciej.

---

### 📦 Dystrybucja bez kodu źródłowego

Możesz dystrybuować pakiet tylko z `.pyc` (bez `.py`):

```bash
# Skompiluj wszystko
python -m compileall src/

# Flagi optymalizacyjne:
python -O  -m compileall src/   # usuwa assert statements → mniejsze pliki
python -OO -m compileall src/   # usuwa też docstringi

# Pliki lądują w:
# src/__pycache__/modul.cpython-312.opt-1.pyc  (flaga -O)
# src/__pycache__/modul.cpython-312.opt-2.pyc  (flaga -OO)
```

> ⚠️ Flaga `-OO` usuwa docstringi — jeśli Twój kod używa `modul.__doc__` lub introspekcji (np. frameworki do dokumentacji), to może powodować błędy.

---

## 🔍 Funkcja `dir()`

> Spis treści dowolnego modułu — i punkt wyjścia do introspekcji.

---

### 📌 Co oferuje moduł?

`dir()` to "spis treści" modułu. Nie pamiętasz jak się coś nazywa? Użyj `dir()`.

```python
import math

print(dir(math))
# ['__doc__', '__name__', 'acos', 'asin', 'atan', 'ceil',
#  'cos', 'e', 'exp', 'floor', 'log', 'pi', 'sin', 'sqrt', ...]

# Zapomniałeś jak się nazywa funkcja do zaokrąglania w górę?
[x for x in dir(math) if 'ceil' in x.lower()]  # → ['ceil']
```

---

### 💡 Praktyczne użycie

```python
# dir() bez argumentu → co masz w bieżącym zasięgu
x = 42
import os

print(dir())
# ['__builtins__', '__name__', 'os', 'x']

# dir() + help() = interaktywna dokumentacja
import json
help(json.dumps)
# Wyświetla pełną dokumentację funkcji z parametrami
```

#### 🔹 Filtrowanie — pomijanie "prywatnych" elementów

```python
import os

# Publiczne API modułu (bez __ dunder __ i _prywatnych)
publiczne = [name for name in dir(os) if not name.startswith('_')]
print(publiczne[:10])
# ['F_OK', 'O_APPEND', 'O_CREAT', 'O_EXCL', 'O_RDONLY', ...]
```

---

### 🔬 Introspekcja w praktyce

```python
import inspect

# Sprawdź sygnatury funkcji dynamicznie
import json
sig = inspect.signature(json.dumps)
print(sig)
# (obj, *, skipkeys=False, ensure_ascii=True, check_circular=True, ...)

# Znajdź wszystkie klasy w module
import http.client
klasy = [(name, obj) for name, obj in inspect.getmembers(http.client)
         if inspect.isclass(obj)]
# → [('BadStatusLine', ...), ('HTTPConnection', ...), ...]

# Dynamiczne ładowanie i inspekcja (przydatne w pluginach)
import importlib
modul = importlib.import_module('json')
print(modul.__spec__.origin)
# → /usr/lib/python3.12/json/__init__.py
```

---

## 🗂️ Pakiety

> Folder z modułami i plikiem `__init__.py` — sposób na porządek w większych projektach.

---

### 📌 Moduły w folderach

Pakiet = folder z plikiem `__init__.py`.  
Pozwala grupować powiązane moduły.

```
moj_sklep/
├── __init__.py      ← bez tego Python nie traktuje folderu jako pakietu
├── produkty.py
└── platnosci.py
```

```python
# Importowanie z pakietu
from moj_sklep import produkty
from moj_sklep.platnosci import zaplac
```

`__init__.py` może być **pusty** — wystarczy że istnieje.

---

### 🧩 Struktura i importowanie

Bardziej rozbudowana struktura:

```
sklep/
├── __init__.py
├── api/
│   ├── __init__.py
│   ├── produkty.py        → GET /api/produkty
│   └── zamowienia.py      → GET /api/zamowienia
├── modele/
│   ├── __init__.py
│   ├── produkt.py
│   └── uzytkownik.py
└── utils/
    ├── __init__.py
    ├── walidacja.py
    └── formatowanie.py
```

Trzy równoważne sposoby importowania:

```python
# Sposób 1 — pełna ścieżka (najczytelniejsze, gdzie co jest)
import sklep.modele.produkt
produkt = sklep.modele.produkt.Produkt(id=1, nazwa="Laptop")

# Sposób 2 — importuj moduł (najczęściej stosowane ✅)
from sklep.modele import produkt
p = produkt.Produkt(id=1, nazwa="Laptop")

# Sposób 3 — importuj klasę/funkcję bezpośrednio
from sklep.modele.produkt import Produkt
p = Produkt(id=1, nazwa="Laptop")
```

#### 🔹 `__init__.py` jako fasada pakietu

```python
# sklep/__init__.py
# Upraszczasz API pakietu dla użytkowników

from .modele.produkt import Produkt
from .modele.uzytkownik import Uzytkownik
from .api.produkty import pobierz_produkty
```

```python
# Teraz zamiast:
from sklep.modele.produkt import Produkt

# Użytkownicy mogą pisać krócej:
from sklep import Produkt
```

---

### 🏗️ Architektura i namespace packages

**Python 3.3+: Namespace packages** — pakiety bez `__init__.py`.  
Pozwalają rozdzielić pakiet między kilka lokalizacji na dysku:

```
# Dwa osobne foldery, jeden logiczny pakiet
/projekt_a/moja_firma/moduly_a/kod_a.py
/projekt_b/moja_firma/moduly_b/kod_b.py

# sys.path zawiera oba foldery
import moja_firma.moduly_a.kod_a  # działa!
import moja_firma.moduly_b.kod_b  # działa!
```

Przydatne przy **plugin systemach** i **monorepo**.

**Atrybuty `__path__` pakietu** — zaawansowana modyfikacja ścieżek wyszukiwania:

```python
import sklep
print(sklep.__path__)
# → ['/home/user/projekt/sklep']

# Można rozszerzyć — Python będzie szukał submodułów też tutaj
sklep.__path__.append('/sciezka/do/pluginow/sklep')
```

---

## 🔗 Importy względne

> Kropki zamiast pełnej ścieżki — importy wewnątrz własnego pakietu.

---

### 📌 Czym różni się od zwykłego importu?

Import względny używa kropek zamiast pełnej ścieżki. Kropka = "bieżący folder".

```python
# Jesteś w: sklep/platnosci/blik.py

from . import karta           # . = bieżący folder (platnosci/)
from .. import utils          # .. = folder wyżej (sklep/)
from ..modele import Produkt  # .. wyżej, potem do modele/
```

---

### ⚖️ Względne vs bezwzględne — kiedy co?

```python
# sklep/api/zamowienia.py

# ✅ Import względny — lepszy wewnątrz pakietu
from ..modele.zamowienie import Zamowienie
from ..utils.walidacja import waliduj

# ✅ Import bezwzględny — OK, ale powiązany z nazwą pakietu
from sklep.modele.zamowienie import Zamowienie
from sklep.utils.walidacja import waliduj
```

**Kiedy używać względnych:**

- wewnątrz własnego pakietu
- gdy pakiet może być przenoszony lub publikowany na PyPI

**Kiedy używać bezwzględnych:**

- w skryptach wejściowych (`main.py`, `app.py`)
- przy imporcie z zewnętrznych pakietów
- gdy importy względne zmniejszają czytelność

> ⚠️ Importy względne nie działają w skryptach uruchamianych bezpośrednio:
> 
> ```bash
> python sklep/api/zamowienia.py
> # ImportError: attempted relative import with no known parent package
> ```
> 
> Uruchamiaj jako moduł: `python -m sklep.api.zamowienia`

---

### ⚠️ Pułapki w dużych projektach

```python
# Klasyczna pułapka: skrypt w podfolderze projektu

# STRUKTURA:
# projekt/
# ├── src/
# │   ├── __init__.py
# │   ├── core.py
# │   └── api/
# │       ├── __init__.py
# │       └── views.py  ← uruchamiasz to bezpośrednio

# views.py
from ..core import Konfiguracja  # ImportError jeśli uruchomisz bezpośrednio!

# ROZWIĄZANIE:
# 1. python -m src.api.views      (z katalogu projekt/)
# 2. Zawsze miej entry point na poziomie projektu
# 3. Użyj pip install -e . i importuj jako zainstalowany pakiet
```

---

## 🌟 Kontrola `__all__`

> Jawna lista tego, co moduł lub pakiet wystawia na zewnątrz jako publiczne API.

---

### 📌 Co to robi?

`__all__` to lista tego, co jest "publiczne" w Twoim module. Wpływa na `from modul import *`.

```python
# utils.py
__all__ = ["dodaj", "odejmij"]  # tylko te dwie są "publiczne"

def dodaj(a, b):
    return a + b

def odejmij(a, b):
    return a - b

def _wewnetrzna_helper(x):  # prywatna, nie eksportowana
    return x * 2
```

```python
from utils import *
dodaj(1, 2)       # ✓ dostępna
odejmij(1, 2)     # ✓ dostępna
_wewnetrzna_helper(5)  # NameError — nie zaimportowana
```

---

### 💡 Praktyczne zastosowanie w pakiecie

```python
# sklep/__init__.py
# Definiujesz publiczne API całego pakietu

from .modele.produkt import Produkt
from .modele.uzytkownik import Uzytkownik
from .api import pobierz_produkty, stworz_zamowienie

__all__ = [
    "Produkt",
    "Uzytkownik",
    "pobierz_produkty",
    "stworz_zamowienie",
]

# Teraz użytkownicy pakietu wiedzą dokładnie co jest API publicznym
```

---

### 🏗️ Konwencje i dokumentacja API

```python
# Wzorzec profesjonalnej biblioteki

# sklep/modele/produkt.py
from __future__ import annotations
from typing import TYPE_CHECKING

__all__ = ["Produkt", "ProduktNieznaleziony"]

class Produkt:
    """Model produktu w sklepie.

    Przykład:
        >>> p = Produkt(id=1, nazwa="Laptop", cena=2999.99)
        >>> p.zastosuj_rabat(10)
        2699.991
    """
    # ...

class ProduktNieznaleziony(Exception):
    """Wyjątek gdy produkt nie istnieje w bazie."""
    pass

# _InternalCache to nie jest w __all__ — implementacja, nie API
class _InternalCache:
    pass
```

Narzędzia do generowania dokumentacji (Sphinx, mkdocs) używają `__all__` do określenia co dokumentować. Jeśli nie zdefiniujesz `__all__`, dokumentacja pokaże wszystko włącznie z prywatnymi szczegółami implementacji.

---

## ♻️ Przeładowanie modułu

> Gdy cache modułów zaczyna przeszkadzać w trakcie developmentu.

---

### 📌 Zmieniłem kod, ale Python nie widzi zmian

```python
# Normalnie: Python ładuje moduł raz i cache'uje
import moj_modul
# ... edytujesz moj_modul.py ...
import moj_modul  # nic się nie zmienia! Python użył cache'u

# Rozwiązanie: reload
import importlib
importlib.reload(moj_modul)  # teraz Python wczyta nową wersję
```

> 💡 Najczęściej przydatne w Jupyter Notebook podczas developmentu.

---

### 🪐 Jupyter i `%autoreload`

```python
# Na początku Jupyter Notebook — raz, a zawsze:
%load_ext autoreload
%autoreload 2

# Od teraz każda zmiana w plikach .py jest automatycznie
# wykrywana i przeładowywana przed wykonaniem komórki
```

---

### ⚠️ Dlaczego reload jest problematyczny?

```python
import importlib
import moj_modul

MojaKlasa = moj_modul.MojaKlasa
obj = MojaKlasa()

importlib.reload(moj_modul)  # przeładowujemy

# PUŁAPKA:
print(isinstance(obj, moj_modul.MojaKlasa))  # → False!
# obj jest instancją STAREJ wersji klasy
# moj_modul.MojaKlasa to już NOWA klasa po reload

# Dlatego reload w produkcji to zły pomysł
# Lepsze rozwiązania: hot reload przez subprocess, gunicorn --reload, watchdog
```

---

## 📋 Cheat Sheet

> Najważniejsze wzorce z tego rozdziału w jednym miejscu.

---

```python
# ════════════════════════════════════════════
#  IMPORTY — najczęstsze wzorce
# ════════════════════════════════════════════

import os                               # cały moduł
from pathlib import Path                # konkretna klasa
import numpy as np                      # alias (konwencja)
from datetime import datetime, date     # wiele elementów

# ════════════════════════════════════════════
#  WZORZEC __main__
# ════════════════════════════════════════════

def main() -> None:
    print("Uruchomiono bezpośrednio")

if __name__ == "__main__":
    main()

# ════════════════════════════════════════════
#  INSPEKCJA MODUŁU
# ════════════════════════════════════════════

import os
dir(os)                                 # lista nazw w module
help(os.path.join)                      # dokumentacja
os.__file__                             # ścieżka do pliku
os.__version__                          # wersja (jeśli dostępna)

# ════════════════════════════════════════════
#  sys.path — gdzie Python szuka
# ════════════════════════════════════════════

import sys
sys.path                                # lista ścieżek
sys.path.insert(0, '/moja/sciezka')     # dodaj na początku (priorytet)
sys.modules                             # cache załadowanych modułów

# ════════════════════════════════════════════
#  PAKIETY — importy względne
# ════════════════════════════════════════════

from . import siostrzany_modul          # z tego samego folderu
from .. import modul_wyzej              # folder wyżej
from ..podfolder import cos             # folder wyżej → do podfolderu

# ════════════════════════════════════════════
#  KONTROLA API
# ════════════════════════════════════════════

__all__ = ["KlasaPubliczna", "funkcja_publiczna"]

# ════════════════════════════════════════════
#  RELOAD (tylko development)
# ════════════════════════════════════════════

import importlib
importlib.reload(moj_modul)             # przeładuj po zmianie kodu

# Jupyter:
# %load_ext autoreload
# %autoreload 2
```

---


<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>



<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>


<div align="center">

# Input and Output

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Temat](https://img.shields.io/badge/temat-input--output-3776AB?style=for-the-badge)

</div>

---

Rozdział 07 skupia się na wejściu i wyjściu w Pythonie i praktycznym operowaniu na:

> ⌲ formatowaniu tekstu (f-stringi, `str.format()`, `%`)
>
> ⌲ reprezentacjach `str()` i `repr()`
>
> ⌲ czytaniu i zapisywaniu plików
>
> ⌲ serializacji danych do JSON
>
> ⌲ bezpiecznym użyciu `pickle`

---

## 🖨️ Formatowanie wyjścia — przegląd

> Cztery sposoby na zamianę danych w tekst — od nowoczesnego f-stringa po archaiczny operator `%`.

---

### 🧩 Jakie mam opcje?

Python oferuje kilka sposobów formatowania tekstu.  
Od najnowszego do najstarszego:

|Metoda|Przykład|Kiedy?|
|---|---|---|
|**f-string**|`f"Mam {wiek} lat"`|✅ zawsze — domyślny wybór|
|**str.format()**|`"Mam {} lat".format(wiek)`|🟡 starszy kod, szablony|
|**%** operator|`"Mam %d lat" % wiek`|❌ nie w nowym kodzie (wyjątek: `logging`)|
|**ręczne**|`str(wiek).rjust(5)`|🔧 specjalne wyrównania|

---

### ⚖️ Co wybrać i dlaczego?

```python
imie = "Anna"
wiek = 28
zarobki = 8750.5

# f-string — Python 3.6+, najczytelniejszy ✅
print(f"Pracownik: {imie}, wiek: {wiek}, zarobki: {zarobki:.2f} zł")

# str.format() — przydatny gdy szablon jest oddzielony od danych
SZABLON = "Pracownik: {imie}, wiek: {wiek}, zarobki: {zarobki:.2f} zł"
print(SZABLON.format(imie=imie, wiek=wiek, zarobki=zarobki))

# % — widzisz w starym kodzie, nie pisz nowego
print("Pracownik: %s, wiek: %d, zarobki: %.2f zł" % (imie, wiek, zarobki))
```

Wszystkie trzy dają ten sam wynik:

```
Pracownik: Anna, wiek: 28, zarobki: 8750.50 zł
```

---

## ✨ f-stringi — złoty standard

> Prefiks `f` i dowolne wyrażenie w `{}` — domyślny sposób formatowania tekstu od Pythona 3.6.

---

### 📌 Podstawy

Dodaj `f` przed cudzysłowem, wyrażenia Pythona wstaw w `{}`:

```python
imie = "Marek"
rok = 2024

print(f"Cześć, {imie}!")              # → Cześć, Marek!
print(f"Rok: {rok}")                  # → Rok: 2024
print(f"Za 10 lat: {rok + 10}")       # → Za 10 lat: 2034
print(f"Wielkie: {imie.upper()}")     # → Wielkie: MAREK
```

Formatowanie liczb:

```python
pi = 3.14159265358979
cena = 1234567.89

print(f"Pi ≈ {pi:.2f}")              # → Pi ≈ 3.14   (2 miejsca po przecinku)
print(f"Pi ≈ {pi:.5f}")              # → Pi ≈ 3.14159
print(f"Cena: {cena:,.2f} zł")       # → Cena: 1,234,567.89 zł
print(f"Procent: {0.4567:.1%}")      # → Procent: 45.7%
```

---

### 📏 Wyrównanie i padding

```python
# Wyrównanie w kolumnach
pracownicy = [("Anna", 8500), ("Bartosz", 12000), ("Celina", 9750)]

print(f"{'Imię':<12} {'Zarobki':>10}")
print("-" * 24)
for imie, zarobki in pracownicy:
    print(f"{imie:<12} {zarobki:>10,.0f} zł")
```

```
Imię            Zarobki
------------------------
Anna              8,500 zł
Bartosz          12,000 zł
Celina            9,750 zł
```

Operatory wyrównania:

|Znak|Wyrównanie|Przykład|Wynik|
|---|---|---|---|
|`<`|do lewej (domyślne dla tekstu)|`f"{'ab':<6}"`|`'ab    '`|
|`>`|do prawej (domyślne dla liczb)|`f"{'ab':>6}"`|`'    ab'`|
|`^`|do środka|`f"{'ab':^6}"`|`'  ab  '`|
|`=`|wypełnienie między znakiem a cyframi (tylko liczby)|`f"{-42:0=6}"`|`'-00042'`|

```python
# Padding z wypełnieniem — znak wypełnienia stoi PRZED znakiem wyrównania
print(f"{'UWAGA':=^30}")    # → ============UWAGA=============
print(f"{'OK':0>5}")        # → 000OK  ← 0 jako znak wypełnienia, wyrównanie do prawej
print(f"{42:05d}")          # → 00042  ← liczba uzupełniona zerami

# Liczby w różnych systemach
n = 255
print(f"Dec: {n:d}, Hex: {n:x}, Oct: {n:o}, Bin: {n:b}")
# → Dec: 255, Hex: ff, Oct: 377, Bin: 11111111
print(f"Hex z prefixem: {n:#x}")  # → 0xff
```

> 💡 Gdy wolnego miejsca nie da się podzielić po równo, `^` dokłada dodatkowy znak po **prawej** stronie — stąd 12 znaków `=` z lewej i 13 z prawej.

---

### 🐞 Debugowanie z `=`

Specyfikator `=` to życie uratowane przy debugowaniu — wypisuje nazwę zmiennej i wartość:

```python
x = 42
lista = [1, 2, 3]
tekst = "hello"

# Zamiast print(f"x={x}, lista={lista}, tekst={tekst}")
print(f"{x=}, {lista=}, {tekst=}")
# → x=42, lista=[1, 2, 3], tekst='hello'

# Działa też z wyrażeniami
y = 10
print(f"{x + y = }")    # → x + y = 52
print(f"{len(lista)=}") # → len(lista)=3
```

---

### ⚠️ Pułapki i wzorce zaawansowane

#### 🔹 f-stringi nie są szablonami

```python
# ❌ To nie zadziała — f-string ewaluuje się natychmiast
szablon = f"Cena: {cena} zł"  # 'cena' musi istnieć tu i teraz

# ✅ Jeśli potrzebujesz szablonu — użyj str.format() lub string.Template
SZABLON = "Cena: {cena} zł"
def formatuj(cena):
    return SZABLON.format(cena=cena)
```

---

#### 🔹 Zagnieżdżone wyrażenia i formatowanie dynamiczne

```python
# Szerokość kolumny jako zmienna
szerokosc = 20
for produkt in ["Laptop", "Mysz", "Klawiatura"]:
    print(f"{produkt:{szerokosc}}")  # dynamiczna szerokość!

# Precyzja jako zmienna
precyzja = 3
print(f"{3.14159265:.{precyzja}f}")  # → 3.142
```

---

#### 🔹 Wydajność — budowanie długich tekstów

```python
# f-string to najszybsza metoda formatowania w CPythonie,
# ale przy sklejaniu tysięcy kawałków liczy się SPOSÓB łączenia:

# ❌ Wolne — każde += może tworzyć nowy string (koszt rośnie kwadratowo)
wynik = ""
for i in range(10000):
    wynik += f"linia {i}\n"

# ✅ Szybkie — zbierz kawałki w liście, sklej raz na końcu
linie = [f"linia {i}" for i in range(10000)]
wynik = "\n".join(linie)
```

---

## 📐 `str.format()` — starszy brat

> Szablon oddzielony od danych — pola `{}` wypełniane są dopiero w momencie wywołania `.format()`.

---

### 📌 Podstawy

```python
# Pozycyjnie — {} zastępuje kolejne argumenty
print("Cześć {} i {}!".format("Ania", "Bartek"))
# → Cześć Ania i Bartek!

# Z indeksami — możesz zmieniać kolejność
print("{1} i {0}".format("pierwszy", "drugi"))
# → drugi i pierwszy

# Z nazwami — czytelniejsze
print("Dziś jest {dzien}, godzina {godzina}".format(
    dzien="poniedziałek",
    godzina="14:30"
))
# → Dziś jest poniedziałek, godzina 14:30
```

---

### 💡 Szablony i słowniki

```python
# Szablon jako stała — formatujesz później
EMAIL_SZABLON = """
Drogi/a {imie},

Dziękujemy za zamówienie nr {nr_zamowienia}.
Kwota: {kwota:.2f} zł
Data wysyłki: {data}

Z poważaniem,
Sklep
"""

def wyslij_email(dane):
    return EMAIL_SZABLON.format(**dane)

dane = {
    "imie": "Kowalski",
    "nr_zamowienia": "ZAM-2024-001",
    "kwota": 349.99,
    "data": "2024-03-15"
}
print(wyslij_email(dane))
```

```python
# Rozpakowanie słownika przez ** — klucze stają się nazwami pól
tabela = {"Python": 1991, "Java": 1995, "JavaScript": 1995}
print("Python: {Python}, Java: {Java}, JavaScript: {JavaScript}".format(**tabela))
# → Python: 1991, Java: 1995, JavaScript: 1995

# Formatowanie w pętli — nazwane pola + specyfikator szerokości
for jezyk, rok in tabela.items():
    print("{jezyk:<15} → {rok}".format(jezyk=jezyk, rok=rok))
```

```
Python          → 1991
Java            → 1995
JavaScript      → 1995
```

---

### 🏗️ Gdy `str.format()` wygrywa z f-stringiem

```python
# Przypadek 1: Szablony ładowane z zewnątrz (baza danych, config)
import configparser

config = configparser.ConfigParser()
config.read('szablony.ini')
szablon = config['email']['powitanie']  # "Cześć {imie}!"
# f-string tu nie zadziała — nie mamy wyrażenia w kodzie
wynik = szablon.format(imie="Ania")

# Przypadek 2: Internacjonalizacja (i18n)
import gettext
_ = gettext.gettext

# Tłumacz może zmienić kolejność {imie} i {produkt} dla innego języka
komunikat = _("Drogi {imie}, Twój {produkt} jest gotowy.")
print(komunikat.format(imie="Jan", produkt="laptop"))

# Przypadek 3: Szablon wybierany dynamicznie w trakcie działania programu
WZORCE = {
    "formal": "Szanowny Pan/Pani {nazwisko}",
    "casual": "Hej {imie}!",
}
styl = "formal"
print(WZORCE[styl].format(nazwisko="Kowalski"))
```

---

## 🔧 Ręczne formatowanie stringów

> Metody `ljust()`, `rjust()`, `center()` i `zfill()` — wyrównanie bez mini-języka formatowania.

---

### 📌 Wyrównywanie tekstu

```python
tekst = "Python"

print(tekst.ljust(20))       # "Python              "  ← lewo
print(tekst.rjust(20))       # "              Python"  ← prawo
print(tekst.center(20))      # "       Python       "  ← środek
print(tekst.center(20, "-")) # "-------Python-------"  ← z wypełnieniem

# Uzupełnianie zerami
print("42".zfill(6))         # → 000042
print("-3.14".zfill(8))      # → -0003.14  (znak się liczy!)
```

---

### 💡 Kiedy to ma sens?

Ręczne metody przydają się gdy budujesz raport tekstowy, logujesz do terminala lub składasz tekst z kawałków o zmiennej długości:

```python
def tabela_produktow(produkty):
    """Wypisuje sformatowaną tabelę w terminalu."""
    naglowek = "Produkt".ljust(20) + "Cena".rjust(11) + "Ilość".rjust(9) + "Wartość".rjust(13)
    separator = "-" * len(naglowek)

    print(naglowek)
    print(separator)

    for produkt, cena, ilosc in produkty:
        wartosc = cena * ilosc
        print(
            produkt.ljust(20)
            + f"{cena:.2f}".rjust(11)
            + str(ilosc).rjust(9)
            + f"{wartosc:.2f}".rjust(13)
        )

    print(separator)

produkty = [
    ("Laptop Dell XPS", 4999.99, 3),
    ("Mysz Logitech", 149.00, 15),
    ("Monitor 27\"", 1799.50, 7),
]
tabela_produktow(produkty)
```

```
Produkt                    Cena    Ilość      Wartość
-----------------------------------------------------
Laptop Dell XPS         4999.99        3     14999.97
Mysz Logitech            149.00       15      2235.00
Monitor 27"             1799.50        7     12596.50
-----------------------------------------------------
```

> 💡 To samo da się zapisać krócej f-stringiem: `f"{produkt:<20} {cena:>10.2f} {ilosc:>8} {wartosc:>12.2f}"` — wynik jest identyczny. Metody ręczne są czytelniejsze, gdy operujesz na pojedynczych stringach, np. `nazwa.ljust(szerokosc, ".")`.

---

## 🦕 Stary operator `%`

> Składnia w stylu `printf` z języka C — trzeba ją umieć czytać, ale nie pisać w nowym kodzie.

---

### 📌 Co to jest i czy używać?

To archaiczna składnia z lat 90. Nadal spotykasz ją w starym kodzie. **Nie pisz jej w nowych projektach** — używaj f-stringów.

```python
# Tak wygląda — zapamiętaj żeby czytać, nie żeby pisać
imie = "Python"
wersja = 3.12

print("Język: %s, wersja: %.1f" % (imie, wersja))
# → Język: Python, wersja: 3.1   ← %.1f zaokrągla do 1 miejsca po przecinku

# Główne specyfikatory:
# %s  → string (str())
# %d  → liczba całkowita
# %f  → liczba zmiennoprzecinkowa
# %r  → repr()
# %05d → całkowita z zerami, min 5 znaków
```

---

### 🏗️ Kiedy `%` jest OK?

```python
# Logging — tu % jest POPRAWNE i zalecane
import logging

username = "anna"
age = 28

# ✅ Tak — logger sam zformatuje tylko jeśli poziom jest aktywny
logging.debug("Przetwarzam użytkownika: %s, wiek: %d", username, age)

# ❌ Tak nie — f-string ewaluuje się zawsze, nawet gdy DEBUG wyłączony
logging.debug(f"Przetwarzam użytkownika: {username}, wiek: {age}")
# Jeśli logging.DEBUG jest wyłączony — tracisz czas na formatowanie
```

---

## 🪞 `str()` vs `repr()`

> Dwie reprezentacje tego samego obiektu — jedna dla człowieka, druga dla programisty.

---

### 📌 Jaka różnica?

```python
tekst = "Witaj\nświecie"
liczba = 3.14

# str() — czytelne dla człowieka
print(str(tekst))    # Witaj
                     # świecie     ← \n zamieniony na nową linię
print(str(liczba))   # 3.14

# repr() — czytelne dla Pythona (możesz wkleić do kodu)
print(repr(tekst))   # 'Witaj\nświecie'  ← dosłownie, ze znakami ucieczki
print(repr(liczba))  # 3.14
```

---

### ⚖️ Kiedy co?

```python
from datetime import datetime

teraz = datetime.now()

print(str(teraz))   # 2024-03-15 14:30:45.123456   ← ładne dla użytkownika
print(repr(teraz))  # datetime.datetime(2024, 3, 15, 14, 30, 45, 123456)
                    # ← możesz to wkleić i odtworzyć obiekt

# W f-stringach możesz użyć !r i !s
zwierze = "kot\npies"
print(f"Zwierzę: {zwierze!s}")   # Zwierzę: kot
                                  #           pies
print(f"Zwierzę: {zwierze!r}")   # Zwierzę: 'kot\npies'
```

---

### 🏗️ Implementacja w klasach

```python
class Produkt:
    def __init__(self, nazwa, cena):
        self.nazwa = nazwa
        self.cena = cena

    def __str__(self):
        """Dla użytkownika — print(), str(), f-string"""
        return f"{self.nazwa} — {self.cena:.2f} zł"

    def __repr__(self):
        """Dla developera — debugging, logi, REPL"""
        return f"Produkt(nazwa={self.nazwa!r}, cena={self.cena!r})"

p = Produkt("Laptop", 4999.99)

print(p)           # Laptop — 4999.99 zł        (używa __str__)
print(repr(p))     # Produkt(nazwa='Laptop', cena=4999.99)  (używa __repr__)

lista = [p]
print(lista)       # [Produkt(nazwa='Laptop', cena=4999.99)]
                   # ← w kontenerach Python używa __repr__!
```

> 💡 **Zasada:** `__repr__` powinien być na tyle precyzyjny, żeby można było odtworzyć obiekt. Jeśli klasa definiuje tylko `__repr__`, to `str()` i `print()` też go użyją — dlatego `__repr__` implementuj zawsze, a `__str__` tylko gdy potrzebujesz ładniejszej wersji dla użytkownika.

---

## 📁 Praca z plikami

> `open()` + `with` — otwieranie, czytanie i zapisywanie plików bez wycieków zasobów.

---

### 📌 Otwieranie i czytanie pliku

```python
# Otwieranie pliku — zawsze podawaj encoding!
plik = open("dane.txt", "r", encoding="utf-8")
zawartosc = plik.read()
plik.close()  # ← trzeba ręcznie zamknąć

# Lepiej: używaj with — zamyka automatycznie, nawet przy wyjątku
with open("dane.txt", "r", encoding="utf-8") as plik:
    zawartosc = plik.read()
# Tu plik jest już zamknięty
```

> 💡 **Dlaczego `encoding="utf-8"`?** Do Pythona 3.14 domyślne kodowanie zależy od systemu (np. `cp1252` na Windows). Od Pythona 3.15 ([PEP 686](https://peps.python.org/pep-0686/)) domyślnie obowiązuje UTF-8 — ale jawne `encoding="utf-8"` nadal jest dobrą praktyką: kod działa tak samo na każdej wersji i każdym systemie.

**Tryby otwierania:**

|Tryb|Znaczenie|Czy tworzy nowy?|
|---|---|---|
|`"r"`|odczyt|❌ błąd jeśli brak|
|`"w"`|zapis (nadpisuje!)|✅ tworzy|
|`"a"`|dopisywanie na końcu|✅ tworzy|
|`"x"`|zapis tylko do nowego pliku|✅ tworzy (błąd jeśli istnieje)|
|`"r+"`|odczyt + zapis|❌ błąd jeśli brak|
|`"rb"`|odczyt binarny|❌ błąd jeśli brak|
|`"wb"`|zapis binarny|✅ tworzy|

```python
# Zapis do pliku
with open("wyniki.txt", "w", encoding="utf-8") as plik:
    plik.write("Linia pierwsza\n")
    plik.write("Linia druga\n")

# Dopisywanie — nie nadpisuje istniejących danych
with open("log.txt", "a", encoding="utf-8") as plik:
    plik.write("Nowy wpis\n")
```

---

### 📖 Różne sposoby czytania

```python
# Cały plik naraz — OK dla małych plików
with open("plik.txt", encoding="utf-8") as f:
    caly_tekst = f.read()          # jeden string

with open("plik.txt", encoding="utf-8") as f:
    linie = f.readlines()          # lista stringów (z \n na końcu)

with open("plik.txt", encoding="utf-8") as f:
    linie = f.read().splitlines()  # lista stringów (bez \n)

# Iteracja po liniach — najlepsze dla dużych plików ✅
with open("duzy_plik.txt", encoding="utf-8") as f:
    for linia in f:                # nie ładuje całości do pamięci!
        linia = linia.strip()      # usuwa \n i białe znaki
        if linia:                  # pomijaj puste linie
            print(linia)

# Czytanie porcjami (chunk) — dla bardzo dużych plików
with open("gigantyczny.bin", "rb") as f:
    while chunk := f.read(8192):   # 8 KB naraz; := przypisuje i sprawdza (pusty → koniec)
        przetworz(chunk)
```

---

### 🏗️ Pathlib, wzorce i bezpieczeństwo

#### 🔹 `pathlib` zamiast ścieżek jako stringów

```python
from pathlib import Path

# Budowanie ścieżek — działa na każdym systemie
katalog = Path("dane") / "2024" / "marzec"
plik = katalog / "raport.txt"

# Sprawdzenia
print(plik.exists())          # → True/False
print(plik.suffix)            # → '.txt'
print(plik.stem)              # → 'raport'
print(plik.parent)            # → dane/2024/marzec

# Tworzenie katalogów
katalog.mkdir(parents=True, exist_ok=True)

# Czytanie/zapis przez pathlib (bez open!)
tekst = plik.read_text(encoding="utf-8")
plik.write_text("nowa zawartość", encoding="utf-8")

# Glob — wyszukiwanie plików (** = rekurencyjnie, alternatywa: rglob("*.txt"))
for plik_txt in Path(".").glob("**/*.txt"):
    print(plik_txt)
```

---

#### 🔹 Obsługa wyjątków przy pracy z plikami

```python
from pathlib import Path

def wczytaj_config(sciezka: str) -> dict:
    plik = Path(sciezka)

    try:
        tekst = plik.read_text(encoding="utf-8")
    except FileNotFoundError as e:
        raise FileNotFoundError(f"Plik konfiguracyjny nie istnieje: {sciezka}") from e
    except PermissionError as e:
        raise PermissionError(f"Brak uprawnień do odczytu: {sciezka}") from e
    except UnicodeDecodeError as e:
        raise ValueError(f"Problem z kodowaniem pliku {sciezka}: {e}") from e

    return parse_config(tekst)
```

> 💡 `raise ... from e` zachowuje oryginalny wyjątek w tracebacku — przy debugowaniu widzisz pełną przyczynę (więcej w rozdziale 08 — Exception Chaining).

---

#### 🔹 Atomowy zapis — błąd nie uszkodzi pliku

```python
import os
import tempfile
from pathlib import Path

def bezpieczny_zapis(sciezka: Path, dane: str) -> None:
    """Zapisuje atomowo — błąd nie uszkodzi istniejącego pliku."""
    # Pisz do pliku tymczasowego w TYM SAMYM katalogu, potem podmień
    with tempfile.NamedTemporaryFile(
        mode="w",
        encoding="utf-8",
        dir=sciezka.parent,
        delete=False,
        suffix=".tmp",
    ) as tmp:
        tmp.write(dane)
        tmp.flush()
        os.fsync(tmp.fileno())  # dane fizycznie na dysku, nie tylko w buforze
        tmp_sciezka = Path(tmp.name)

    # replace() (os.replace) jest operacją atomową w obrębie jednego systemu plików
    tmp_sciezka.replace(sciezka)
```

---

## 🗂️ Metody obiektów pliku

> Pełny zestaw narzędzi obiektu pliku — czytanie, zapis, pozycja kursora i bufor.

---

### 📌 Podstawowe metody

```python
with open("plik.txt", "r+", encoding="utf-8") as f:

    # Czytanie
    f.read()           # cały plik jako string
    f.read(100)        # pierwsze 100 znaków
    f.readline()       # jedna linia (z \n)
    f.readlines()      # wszystkie linie jako lista

    # Zapis
    f.write("tekst")   # zwraca liczbę zapisanych znaków
    f.writelines(["linia1\n", "linia2\n"])  # lista stringów

    # Pozycja
    f.tell()           # aktualna pozycja (binarnie: bajty od początku; tekstowo: znacznik dla seek())
    f.seek(0)          # przejdź na początek
    f.seek(0, 2)       # przejdź na koniec (whence=2)

    # Info
    f.closed           # → False (plik otwarty)
    f.name             # → 'plik.txt'
    f.mode             # → 'r+'
```

---

### 🔬 `seek()` i `tell()` w praktyce

```python
# Przykład: przeczytaj plik, wróć na początek, przeczytaj ponownie
with open("dane.csv", encoding="utf-8") as f:
    naglowek = f.readline()       # → "id,imie,wiek\n"
    pozycja_po_naglowku = f.tell()

    for linia in f:
        if "error" in linia:
            f.seek(pozycja_po_naglowku)  # wróć za nagłówek
            break

# Tryb binarny — seek z whence
with open("plik.bin", "rb") as f:
    f.seek(0, 2)               # idź na koniec
    rozmiar = f.tell()         # rozmiar pliku w bajtach
    print(f"Rozmiar: {rozmiar} B")

    f.seek(-4, 2)              # 4 bajty przed końcem
    ostatnie_bajty = f.read(4)
```

> ⚠️ W trybie **tekstowym** bezpieczne są tylko: `seek(0)`, `seek(0, 2)` (skok na koniec) i pozycje zwrócone wcześniej przez `tell()`. Niezerowe przesunięcia względem bieżącej pozycji (`whence=1`) lub końca (`whence=2`) działają **tylko w trybie binarnym** — w tekstowym rzucają `io.UnsupportedOperation`.
>
> Dodatkowo `tell()` nie działa w trakcie pętli `for linia in f` (`OSError`) — zapamiętaj pozycję **przed** pętlą, jak w przykładzie.

---

### ⚡ Buforowanie i `flush()`

```python
import os

# Python buforuje zapisy — dane mogą nie trafić na dysk od razu
with open("log.txt", "a", encoding="utf-8") as f:
    f.write("Ważny wpis\n")
    f.flush()              # przekazuje bufor Pythona do systemu operacyjnego
    os.fsync(f.fileno())   # dopiero to gwarantuje fizyczny zapis na dysk

# Dla logów krytycznych — buforowanie liniowe (tylko tryb tekstowy)
with open("critical.log", "a", encoding="utf-8", buffering=1) as log:
    log.write("Coś się stało\n")  # bufor opróżniany po każdej linii

# Wyłączenie buforowania (tylko tryb binarny)
with open("strumien.bin", "wb", buffering=0) as f:
    f.write(b"\x00\x01")

# print() też można opróżnić od razu — np. postęp w terminalu
print("Postęp...", end="", flush=True)
```

---

## 🔄 JSON — serializacja danych

> Uniwersalny, tekstowy format wymiany danych — Python ↔ JSON w czterech funkcjach: `dumps`, `loads`, `dump`, `load`.

---

### 📌 Zapisz i wczytaj dane

JSON to format wymiany danych — działa w każdym języku programowania i jest czytelny dla człowieka.

```python
import json

# Python → JSON string (serializacja)
dane = {
    "imie": "Anna",
    "wiek": 28,
    "hobby": ["Python", "szachy", "wędrówki"],
    "aktywna": True,
    "ocena": None
}

json_string = json.dumps(dane)
print(json_string)
# → {"imie": "Anna", "wiek": 28, "hobby": ["Python", "szachy", "wędrówki"], ...}
#   ← polskie znaki jako \uXXXX, bo domyślnie ensure_ascii=True

# JSON string → Python (deserializacja)
odczytane = json.loads(json_string)
print(odczytane["imie"])  # → Anna
```

#### 🔹 Zapis do pliku i odczyt

```python
import json

dane = {"produkt": "Laptop", "cena": 4999.99, "dostepny": True}

# Zapis
with open("produkt.json", "w", encoding="utf-8") as f:
    json.dump(dane, f, ensure_ascii=False, indent=2)

# Odczyt
with open("produkt.json", "r", encoding="utf-8") as f:
    wczytane = json.load(f)

print(wczytane["produkt"])  # → Laptop
```

Plik `produkt.json` wygląda tak:

```json
{
  "produkt": "Laptop",
  "cena": 4999.99,
  "dostepny": true
}
```

> 💡 Ściąga: funkcje z **`s`** na końcu (`dumps`, `loads`) pracują na **s**tringach, bez `s` (`dump`, `load`) — na plikach.

---

### ⚙️ Opcje i typy danych

#### 🔹 Mapowanie typów Python ↔ JSON

|Python|JSON|
|---|---|
|`dict`|`{}` obiekt|
|`list`, `tuple`|`[]` tablica|
|`str`|`"string"`|
|`int`, `float`|`liczba`|
|`True` / `False`|`true` / `false`|
|`None`|`null`|

#### 🔹 Opcje `dumps()`

```python
import json

dane = {"miasto": "Wrocław", "temperatura": 21.5}

# Czytelne formatowanie (indent) + polskie znaki (ensure_ascii=False)
print(json.dumps(dane, indent=4, ensure_ascii=False))
# {
#     "miasto": "Wrocław",
#     "temperatura": 21.5
# }

# Sortowanie kluczy
print(json.dumps({"b": 2, "a": 1}, sort_keys=True))
# → {"a": 1, "b": 2}

# Kompaktowy — dla API, minimalna objętość
print(json.dumps(dane, separators=(",", ":"), ensure_ascii=False))
# → {"miasto":"Wrocław","temperatura":21.5}
```

---

#### 🔹 Pułapki konwersji

```python
import json

# Klucze słownika ZAWSZE stają się stringami
json.loads(json.dumps({1: "a"}))            # → {'1': 'a'}  ← int zamienił się w str!

# Krotka wraca jako lista
json.loads(json.dumps((1, 2)))              # → [1, 2]

# NaN / Infinity — Python je zapisze, ale to NIEPOPRAWNY JSON dla innych języków
json.dumps(float("nan"))                    # → 'NaN'
json.dumps(float("nan"), allow_nan=False)   # → ValueError
```

---

### 🏗️ Serializacja własnych klas i edge case'y

#### 🔹 Własny encoder i `default=`

```python
import base64
import json
from datetime import date, datetime
from decimal import Decimal

# ❌ Problematyczne typy — JSON ich nie obsługuje natywnie
dane = {
    "data": datetime.now(),
    "cena": Decimal("99.99"),
    "bajty": b"dane binarne",
}
# json.dumps(dane)  → TypeError: Object of type datetime is not JSON serializable

# ✅ Rozwiązanie 1: własny encoder
class PythonJSONEncoder(json.JSONEncoder):
    def default(self, obj):
        if isinstance(obj, (datetime, date)):
            return obj.isoformat()
        if isinstance(obj, Decimal):
            return str(obj)  # str, nie float — float gubi precyzję (ważne przy kwotach!)
        if isinstance(obj, bytes):
            return base64.b64encode(obj).decode("ascii")  # bajty → bezpieczny tekst
        return super().default(obj)

wynik = json.dumps(dane, cls=PythonJSONEncoder, ensure_ascii=False)
print(wynik)
# → {"data": "2024-03-15T14:30:45.123456", "cena": "99.99", "bajty": "ZGFuZSBiaW5hcm5l"}

# ✅ Rozwiązanie 2: szybki skrót — default=str dla wszystkiego, czego JSON nie zna
json.dumps({"data": datetime(2024, 3, 15, 14, 30)}, default=str)
# → '{"data": "2024-03-15 14:30:00"}'
```

---

#### 🔹 `dataclasses` + `asdict()`

```python
import json
from dataclasses import dataclass, asdict

@dataclass
class Produkt:
    nazwa: str
    cena: float
    dostepny: bool = True

p = Produkt("Laptop", 4999.99)
json.dumps(asdict(p))  # → '{"nazwa": "Laptop", "cena": 4999.99, "dostepny": true}'
```

---

#### 🔹 Bezpieczne parsowanie zewnętrznego JSON

```python
import json

def parsuj_json_bezpiecznie(tekst: str, maks_rozmiar: int = 1_000_000) -> dict:
    """Parsuje JSON z podstawową walidacją."""

    if len(tekst) > maks_rozmiar:
        raise ValueError(f"JSON zbyt duży: {len(tekst)} > {maks_rozmiar}")

    try:
        dane = json.loads(tekst)
    except json.JSONDecodeError as e:
        raise ValueError(f"Nieprawidłowy JSON: {e.msg} (linia {e.lineno})") from e

    if not isinstance(dane, dict):
        raise TypeError(f"Oczekiwano obiektu JSON, dostano: {type(dane).__name__}")

    return dane
```

---

## 🧊 `pickle` vs JSON

> Binarna serializacja dowolnych obiektów Pythona — potężna, ale niebezpieczna dla danych z zewnątrz.

---

### ⚖️ Kiedy co?

|Cecha|JSON|pickle|
|---|---|---|
|Format|tekstowy, czytelny|binarny|
|Języki|wszystkie|tylko Python|
|Typy|podstawowe|dowolne obiekty Pythona|
|Bezpieczeństwo|✅ bezpieczny|❌ **nigdy z zewnątrz!**|
|Rozmiar|większy|mniejszy|
|Szybkość|wolniejszy|szybszy|

```python
import pickle
from datetime import datetime

# pickle obsługuje typy, których JSON nie obsługuje
dane = {
    "zbior": {1, 2, 3},              # set — w JSON niemożliwy
    "krotka": (1, 2),                # wraca jako krotka, nie lista
    "data": datetime(2024, 3, 15),   # dowolne obiekty Pythona
    "klasa": dict,                   # klasy i funkcje — zapisywane przez nazwę
}

# Serializacja
with open("dane.pkl", "wb") as f:
    pickle.dump(dane, f)

# Deserializacja
with open("dane.pkl", "rb") as f:
    wczytane = pickle.load(f)
```

> ⚠️ Nie wszystko da się spiklować: `lambda`, funkcje zagnieżdżone, otwarte pliki czy połączenia sieciowe rzucą `PicklingError` lub `TypeError`.

---

### ⚠️ Pickle jest niebezpieczny

#### 🔹 Atak przez `__reduce__`

```python
# ❌ NIGDY nie ładuj pickle z niezaufanego źródła — to arbitrary code execution
# Atakujący może spreparować plik .pkl, który wykona dowolny kod:

import os
import pickle

class Exploit:
    def __reduce__(self):
        # wykona się przy pickle.load() — tu niewinne echo,
        # w prawdziwym ataku: dowolne polecenie systemowe
        return (os.system, ("echo 'Masz problem!'",))
```

Zamiast `pickle` dla danych z zewnątrz używaj:

- **JSON** — proste dane
- **MessagePack** — binarny, szybki, bezpieczny
- **Protocol Buffers / Cap'n Proto** — schematy i kontrakty między serwisami
- **pickle** — tylko dla **własnych** danych wewnątrz aplikacji

---

#### 🔹 Bezpieczniejsze użycie — podpis HMAC

```python
import hashlib
import hmac
import pickle

SEKRET = b"moj-tajny-klucz"  # w praktyce: zmienna środowiskowa / secret manager

def zapisz_bezpiecznie(dane, sciezka):
    serialized = pickle.dumps(dane)
    podpis = hmac.new(SEKRET, serialized, hashlib.sha256).digest()
    with open(sciezka, "wb") as f:
        f.write(podpis + serialized)

def wczytaj_bezpiecznie(sciezka):
    with open(sciezka, "rb") as f:
        dane_raw = f.read()
    podpis, serialized = dane_raw[:32], dane_raw[32:]
    oczekiwany = hmac.new(SEKRET, serialized, hashlib.sha256).digest()
    if not hmac.compare_digest(podpis, oczekiwany):
        raise ValueError("Dane zostały zmodyfikowane!")
    return pickle.loads(serialized)
```

> 💡 HMAC chroni przed **modyfikacją** danych, ale ich nie szyfruje — każdy z dostępem do pliku nadal może je odczytać.

---

## 📋 Cheat Sheet

> Najważniejsze wzorce z tego rozdziału w jednym miejscu.

---

```python
# ════════════════════════════════════════════
#  F-STRINGI
# ════════════════════════════════════════════

f"tekst {zmienna}"                   # podstawowe
f"{liczba:.2f}"                      # 2 miejsca po przecinku
f"{liczba:,.0f}"                     # separator tysięcy
f"{liczba:.1%}"                      # procent
f"{tekst:<20}"                       # wyrównanie lewo, 20 znaków
f"{tekst:>20}"                       # wyrównanie prawo
f"{tekst:^20}"                       # wyśrodkowanie
f"{tekst:=^20}"                      # wyśrodkowanie z wypełnieniem
f"{n:#x}"                            # hex z prefixem 0x
f"{n:08b}"                           # bin z zerami, 8 znaków
f"{zmienna=}"                        # debug: wypisuje "zmienna=wartość"
f"{obj!r}"                           # użyj repr()
f"{obj!s}"                           # użyj str()

# ════════════════════════════════════════════
#  PLIKI
# ════════════════════════════════════════════

# Odczyt (alternatywy — każda przesuwa kursor, wybierz jedną)
with open("plik.txt", "r", encoding="utf-8") as f:
    caly     = f.read()              # → string
    linie    = f.readlines()         # → lista z \n
    linia    = f.readline()          # → jedna linia
    for linia in f: ...              # → iteracja (pamięciooszczędna)

# Zapis
with open("plik.txt", "w", encoding="utf-8") as f:
    f.write("tekst\n")
    f.writelines(["l1\n", "l2\n"])

# Dopisywanie
with open("log.txt", "a", encoding="utf-8") as f:
    f.write("nowy wpis\n")

# Binarny
with open("plik.bin", "rb") as f:
    bajty = f.read()

# pathlib (zalecane)
from pathlib import Path
Path("plik.txt").read_text(encoding="utf-8")
Path("plik.txt").write_text("treść", encoding="utf-8")

# ════════════════════════════════════════════
#  JSON
# ════════════════════════════════════════════

import json

# Python → string
json.dumps(dane)
json.dumps(dane, indent=2, ensure_ascii=False, sort_keys=True)

# String → Python
json.loads(tekst)

# Python → plik
with open("dane.json", "w", encoding="utf-8") as f:
    json.dump(dane, f, indent=2, ensure_ascii=False)

# Plik → Python
with open("dane.json", "r", encoding="utf-8") as f:
    dane = json.load(f)

# ════════════════════════════════════════════
#  STR vs REPR
# ════════════════════════════════════════════

str(obj)    # czytelne dla użytkownika → __str__
repr(obj)   # czytelne dla kodu → __repr__

# W klasach:
def __str__(self): return "dla użytkownika"
def __repr__(self): return "Klasa(param=wartość)"  # odtwarzalny!
```

---


<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>



<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>


<div align="center">

# Errors and Exceptions

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Temat](https://img.shields.io/badge/temat-errors--exceptions-3776AB?style=for-the-badge)

</div>

---

Rozdział 08 skupia się na błędach i wyjątkach w Pythonie i praktycznym operowaniu na:

> ⌲ czytaniu tracebacków i odróżnianiu błędów składni od wyjątków
>
> ⌲ obsłudze wyjątków (`try` / `except` / `else` / `finally`)
>
> ⌲ zgłaszaniu i łańcuchowaniu wyjątków (`raise`, `raise ... from`)
>
> ⌲ własnych klasach wyjątków
>
> ⌲ grupach wyjątków (`ExceptionGroup`, `except*`) i notatkach (`add_note()`)
>
> ⌲ logowaniu, debugowaniu i testowaniu obsługi błędów

---

## 🛟 Po co nam wyjątki?

> Obsługa wyjątków to plan B dla kodu — świadoma reakcja na sytuacje, których program nie kontroluje.

---

### 📌 Plan awaryjny dla programu

Wyobraź sobie pilota samolotu. Przez większość lotu wszystko idzie zgodnie z planem, ale w kokpicie leży gruba książka procedur awaryjnych: co zrobić, gdy zgaśnie silnik, gdy spadnie ciśnienie, gdy zawiedzie radio. Pilot nie liczy na to, że awaria się zdarzy — po prostu jest na nią **przygotowany**.

Obsługa wyjątków to właśnie taki **plan B dla Twojego kodu**. Program prawie zawsze styka się ze światem, którego nie kontroluje:

|Sytuacja|Co może pójść nie tak|
|---|---|
|🗄️ Łączysz się z bazą danych|Serwer bazy jest wyłączony|
|🌐 Pobierasz dane z API|API zwraca błąd albo nie odpowiada|
|📄 Otwierasz plik|Plik nie istnieje lub brakuje uprawnień|
|⌨️ Prosisz użytkownika o liczbę|Użytkownik wpisuje „trzy” zamiast `3`|
|🔎 Szukasz rekordu po identyfikatorze|Takiego rekordu po prostu nie ma|

Bez obsługi błędów każda z tych sytuacji kończy się **awarią całej aplikacji** i ścianą niezrozumiałego tekstu na ekranie. Z obsługą błędów możesz zamiast tego wyświetlić komunikat *„Trwa ponowna próba połączenia…”*, poprosić o poprawne dane albo pokazać okrojoną, ale działającą wersję strony.

> 💡 **Zasada:** celem obsługi wyjątków **nie jest ukrywanie błędów**, lecz świadome decydowanie, co program ma zrobić, gdy coś pójdzie nie po myśli.

---

## 🧱 Błędy składni vs wyjątki

> Dwa rodzaje błędów — jeden nie pozwala programowi wystartować, drugi pojawia się w trakcie działania.

---

### ⚖️ Czym się różnią?

| |**Błąd składni** (*syntax error*)|**Wyjątek** (*exception*)|
|---|---|---|
|**Czym jest**|Kod jest napisany niezgodnie z regułami języka|Kod jest poprawny, ale coś zawiodło w trakcie działania|
|**Kiedy wykrywany**|Zanim program w ogóle ruszy|Podczas wykonywania programu|
|**Czy da się go obsłużyć**|❌ Nie — trzeba poprawić kod|✅ Tak — za pomocą `try` / `except`|
|**Analogia**|Zdanie z rażącym błędem gramatycznym|Poprawne zdanie: „Podaj mi sól” — ale soli nie ma na stole|

---

### 📌 Błąd składni (`SyntaxError`)

Błąd składni (zwany też **błędem parsowania**) to najczęstsza „skarga” Pythona u osób, które dopiero zaczynają naukę:

```python
>>> if wiek > 18 print("Pełnoletni")
  File "<stdin>", line 1
    if wiek > 18 print("Pełnoletni")
                 ^^^^^
SyntaxError: invalid syntax
```

Python powtarza błędną linię i wskazuje strzałkami (`^`) miejsce, w którym **zauważył** problem. W nazwie pliku (`<stdin>` oznacza konsolę) i numerze linii znajdziesz adres usterki.

> ⚠️ Strzałki pokazują, gdzie parser się „potknął”, a nie zawsze to, co trzeba poprawić. Tutaj wskazują na `print`, choć prawdziwą przyczyną jest **brakujący dwukropek** tuż przed nim: `if wiek > 18:`.

> 💡 W nowym REPL-u (Python 3.13+) zamiast `<stdin>` zobaczysz `<python-input-0>` — numer kolejnej instrukcji wpisanej w konsoli. Znaczenie jest to samo: kod nie pochodzi z pliku, tylko z trybu interaktywnego.

---

## 💥 Wyjątki i traceback

> Błąd wykryty w trakcie działania programu to wyjątek — a traceback to mapa, która prowadzi prosto do jego źródła.

---

### 📌 Pierwsze wyjątki

Nawet idealnie poprawny składniowo kod może zawieść w trakcie działania. Błędy wykryte podczas wykonywania programu nazywamy **wyjątkami**. Nie muszą one oznaczać katastrofy — za chwilę nauczysz się je obsługiwać — ale jeśli nikt się nimi nie zajmie, program zatrzyma się z komunikatem:

```python
>>> 10 * (1 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    10 * (1 / 0)
          ~~^~~
ZeroDivisionError: division by zero

>>> 4 + pomidor * 3
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    4 + pomidor * 3
        ^^^^^^^
NameError: name 'pomidor' is not defined

>>> "2" + 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    "2" + 2
    ~~~~^~~
TypeError: can only concatenate str (not "int") to str
```

---

### 🔬 Anatomia tracebacku

Każdy taki komunikat ma stałą budowę. Weźmy program `kalkulator.py`, w którym jedna funkcja wywołuje drugą:

```python
def divide_numbers(a, b):
    return a / b

def calculate():
    return divide_numbers(10, 0)

calculate()
```

Python odpowie tzw. **tracebackiem** (*śladem stosu*, ang. *stack trace*):

```
Traceback (most recent call last):
  File "kalkulator.py", line 7, in <module>         ← 3️⃣ stąd wszystko się zaczęło
    calculate()
    ~~~~~~~~~^^
  File "kalkulator.py", line 5, in calculate        ← 2️⃣ ta funkcja wywołała kolejną
    return divide_numbers(10, 0)
  File "kalkulator.py", line 2, in divide_numbers   ← 1️⃣ tu nastąpił wybuch
    return a / b
           ~~^~~
ZeroDivisionError: division by zero                 ← 🎯 TYP i OPIS błędu
```

> 💡 **Traceback czyta się od dołu do góry:**
>
> 1. Ostatnia linia mówi, **co** się stało: typ wyjątku (`ZeroDivisionError`) i szczegóły (`division by zero`).
> 2. Linie tuż nad nią wskazują, **gdzie** dokładnie — plik, numer linii i nazwę funkcji.
> 3. Im wyżej, tym dalej cofasz się w łańcuchu wywołań, aż do miejsca, od którego wszystko się zaczęło.

Traceback, choć z początku onieśmiela, to w rzeczywistości **mapa skarbów** prowadząca prosto do usterki.

---

### 📚 Najczęściej spotykane wbudowane wyjątki

|Wyjątek|Kiedy się pojawia|Przykład|
|---|---|---|
|`ZeroDivisionError`|Dzielenie przez zero|`5 / 0`|
|`ValueError`|Poprawny typ, ale niewłaściwa wartość|`int("abc")`|
|`TypeError`|Operacja na niewłaściwym typie|`"2" + 2`|
|`NameError`|Użycie nieistniejącej zmiennej|`print(nieznana)`|
|`KeyError`|Brak klucza w słowniku|`{"a": 1}["b"]`|
|`IndexError`|Indeks poza zakresem listy|`[1, 2, 3][10]`|
|`AttributeError`|Obiekt nie ma takiego atrybutu|`"tekst".push("x")`|
|`FileNotFoundError`|Plik nie istnieje|`open("brak.txt")`|
|`ModuleNotFoundError`|Nie ma takiego modułu|`import nieistniejacy`|
|`KeyboardInterrupt`|Użytkownik przerwał program (`Ctrl`+`C`)|—|

> 💡 Nazwy wbudowanych wyjątków to zwykłe identyfikatory, a nie zarezerwowane słowa kluczowe. Pełną listę znajdziesz w dokumentacji: [Built-in Exceptions](https://docs.python.org/3/library/exceptions.html).

---

## 🛡️ Obsługa wyjątków: `try` / `except`

> Ryzykowny kod trafia do `try`, a reakcja na konkretne błędy — do bloków `except`.

---

### 📌 Od awarii do obsługi

Napiszmy program, który dzieli przez siebie dwie liczby podane przez użytkownika:

```python
a = input("Podaj pierwszą liczbę: ")
b = input("Podaj drugą liczbę: ")
print(a / b)
```

Wpisujemy `5` i `2`, a w odpowiedzi dostajemy… `TypeError: unsupported operand type(s) for /: 'str' and 'str'`. Funkcja `input()` zawsze zwraca **tekst**, a tekstu nie da się dzielić. Poprawiamy:

```python
a = int(input("Podaj pierwszą liczbę: "))
b = int(input("Podaj drugą liczbę: "))
print(a / b)
```

Dla `5` i `2` dostajemy `2.5`. Sukces? Niezupełnie. Złośliwy (albo po prostu zmęczony) użytkownik może wpisać:

- `1a` → `ValueError: invalid literal for int() with base 10: '1a'`
- `5` i `0` → `ZeroDivisionError: division by zero`

Zamiast mnożyć instrukcje `if` sprawdzające każdy przypadek, otaczamy ryzykowny kod blokiem **`try`** i przechwytujemy konkretne wyjątki w blokach **`except`**:

```python
try:
    a = int(input("Podaj pierwszą liczbę: "))
    b = int(input("Podaj drugą liczbę: "))
    print(f"Wynik: {a / b}")
except ValueError:
    print("😕 To nie wygląda na liczbę całkowitą.")
except ZeroDivisionError:
    print("🚫 Przez zero nie dzielimy!")

print("Program działa dalej 🙂")
```

```
Podaj pierwszą liczbę: 5
Podaj drugą liczbę: 0
🚫 Przez zero nie dzielimy!
Program działa dalej 🙂
```

Program się nie wysypał — zamiast tego grzecznie poinformował użytkownika o problemie i **pracował dalej**.

---

### 🔬 Jak działa `try` — krok po kroku

1. Python wykonuje instrukcje z bloku **`try`**.
2. Jeśli **nie wystąpi** żaden wyjątek — bloki `except` są pomijane.
3. Jeśli wyjątek **wystąpi** — reszta bloku `try` jest pomijana, a Python szuka pierwszego bloku `except`, który pasuje do typu wyjątku. Wykonuje go i przechodzi dalej, za całą instrukcję `try`.
4. Jeśli **żaden** `except` nie pasuje — wyjątek „wylatuje” na zewnątrz, do otaczającego kodu. Jeśli nikt go nie obsłuży, program kończy się tracebackiem (*nieobsłużony wyjątek*, ang. *unhandled exception*).

```
wykonaj blok try
│
├── brak wyjątku ───────► else (jeśli jest) ───► finally (jeśli jest) ──► program biegnie dalej ✔
│
└── wyjątek
    │
    ├── pasuje except ──► PIERWSZY pasujący ───► finally (jeśli jest) ──► program biegnie dalej ✔
    │
    └── nic nie pasuje ────────────────────────► finally (jeśli jest) ──► wyjątek leci wyżej ⬆
```

> 💡 Bloki `else` i `finally` omówione są w dalszych sekcjach — na schemacie są od razu, żeby obraz był kompletny.

---

### 🔁 Pytaj, aż się uda

Klasyczny wzorzec: pętla, która ponawia pytanie, dopóki użytkownik nie poda poprawnej wartości.

```python
while True:
    try:
        age = int(input("Ile masz lat? "))
        break                                   # sukces → wychodzimy z pętli
    except ValueError:
        print("Ups! To nie jest poprawna liczba. Spróbuj jeszcze raz…")

print(f"Za rok będziesz mieć {age + 1} lat 🎂")
```

Użytkownik wciąż może przerwać program skrótem `Ctrl`+`C` — Python zgłasza wtedy wyjątek `KeyboardInterrupt`, którego tutaj (słusznie!) nie przechwytujemy.

---

### 📡 Wyjątki przenikają przez funkcje

`try` obsługuje nie tylko wyjątki zgłoszone bezpośrednio w swoim bloku, ale także te, które wyleciały z **wywoływanych w nim funkcji** — nawet bardzo głęboko zagnieżdżonych:

```python
>>> def risky():
...     return 1 / 0
...
>>> def middle():
...     return risky()
...
>>> try:
...     middle()
... except ZeroDivisionError as err:
...     print("Błąd w czasie wykonania:", err)
...
Błąd w czasie wykonania: division by zero
```

Wyjątek „wspina się” w górę stosu wywołań (mówimy, że **propaguje**), aż trafi na pasujący `except` — albo na sam szczyt programu.

---

## 🎯 Dopasowywanie wyjątków

> Który blok `except` się wykona — kilka typów naraz, kolejność bloków i dostęp do obiektu wyjątku.

---

### 🧩 Wiele wyjątków — osobno albo razem

Jedna instrukcja `try` może mieć **wiele bloków `except`**. Wykona się **co najwyżej jeden** z nich — pierwszy pasujący.

Jeśli kilka wyjątków chcesz obsłużyć **w ten sam sposób**, wymień je w jednym bloku:

```python
values = [10, 5, "hello", 0, 8]

for value in values:
    try:
        print(100 / int(value))
    except (ValueError, ZeroDivisionError):
        print(f"⏭️  Pomijam niepoprawną wartość: {value!r}")
```

```
10.0
20.0
⏭️  Pomijam niepoprawną wartość: 'hello'
⏭️  Pomijam niepoprawną wartość: 0
12.5
```

> 💡 **Nowość od Pythona 3.14 ([PEP 758](https://peps.python.org/pep-0758/)):** gdy nie używasz `as`, nawiasy można pominąć.
>
> ```python
> except ValueError, ZeroDivisionError:          # ✅ Python 3.14+
>     ...
> except (ValueError, ZeroDivisionError) as e:   # ✅ z „as” nawiasy są obowiązkowe
>     ...
> ```

---

### ⚠️ Kolejność bloków `except` ma znaczenie

Blok `except` łapie wyjątki wskazanej klasy **oraz wszystkich jej klas potomnych**. Na przykład `LookupError` jest „rodzicem” zarówno `KeyError`, jak i `IndexError`:

```python
data = {"imie": "Ala"}

try:
    print(data["nazwisko"])
except LookupError as e:          # złapie i KeyError, i IndexError
    print(f"Nie znaleziono: {e}")
```

Ponieważ wykonuje się **pierwszy pasujący** blok, bardziej ogólne klasy muszą stać **niżej** niż szczegółowe:

```python
class B(Exception): pass
class C(B): pass          # C jest szczególnym przypadkiem B
class D(C): pass          # D jest szczególnym przypadkiem C

for cls in [B, C, D]:
    try:
        raise cls()
    except D:
        print("D")
    except C:
        print("C")
    except B:
        print("B")
```

Wynik: **`B`, `C`, `D`** — każdy wyjątek trafia do „swojego” bloku. Gdybyś jednak odwrócił kolejność i postawił `except B` na początku, zobaczyłbyś **`B`, `B`, `B`**, bo `B` pasuje do wszystkich trzech klas.

> ⚠️ Zasada w pigułce: **od szczegółu do ogółu**. `except Exception` na samym początku „zjadłby” wszystkie pozostałe bloki.

---

### 🔍 Zaglądamy do środka wyjątku: `as`

Po nazwie wyjątku możesz dopisać `as nazwa`, aby dostać się do **obiektu wyjątku**:

```python
>>> try:
...     raise Exception("konserwa", "jajka")
... except Exception as inst:
...     print(type(inst))       # typ wyjątku
...     print(inst.args)        # argumenty zapisane w .args
...     print(inst)             # __str__ wypisuje argumenty bezpośrednio
...     x, y = inst.args        # rozpakowanie argumentów
...     print(f"x = {x}, y = {y}")
...
<class 'Exception'>
('konserwa', 'jajka')
('konserwa', 'jajka')
x = konserwa, y = jajka
```

W praktyce najczęściej przydaje się po prostu tekst błędu i nazwa jego typu:

```python
try:
    int("dwanaście")
except ValueError as e:
    print(f"Typ: {type(e).__name__}")   # Typ: ValueError
    print(f"Opis: {e}")                 # Opis: invalid literal for int() with base 10: 'dwanaście'
```

---

## 🌳 Hierarchia wyjątków

> Wszystkie wyjątki tworzą drzewo klas — jego znajomość decyduje o tym, co naprawdę łapie dany `except`.

---

### 📌 Drzewo genealogiczne wyjątków

Warto znać górną część hierarchii:

```
BaseException                    ← praprzodek wszystkich wyjątków
 ├── SystemExit                  ← zgłaszany przez sys.exit()
 ├── KeyboardInterrupt           ← Ctrl+C
 ├── GeneratorExit
 └── Exception                   ← tu zaczyna się świat „zwykłych” błędów
      ├── ArithmeticError
      │    ├── ZeroDivisionError
      │    └── OverflowError
      ├── LookupError
      │    ├── IndexError
      │    └── KeyError
      ├── OSError
      │    ├── FileNotFoundError
      │    ├── PermissionError
      │    ├── ConnectionError
      │    └── TimeoutError
      ├── ValueError
      ├── TypeError
      ├── NameError
      ├── AttributeError
      ├── ImportError
      │    └── ModuleNotFoundError
      ├── RuntimeError
      │    └── RecursionError
      └── ExceptionGroup         ← grupa wyjątków (sekcja o except*)
```

> ⚠️ `SystemExit` i `KeyboardInterrupt` **nie** dziedziczą po `Exception`. To celowe: sygnalizują, że program **powinien się zakończyć**, więc zwykle nie należy ich przechwytywać. Dlatego `except Exception:` jest bezpieczniejsze niż goły `except:`, który łapie absolutnie wszystko — łącznie z próbą zamknięcia programu.

---

### ⚖️ Łapanie „wszystkiego” — z głową

`except Exception` działa jak symbol wieloznaczny, który przechwytuje (prawie) każdy błąd. Edytory i lintery często ostrzegają wtedy komunikatem *„too broad exception clause”* — i mają rację, bo taki blok może ukryć błąd, którego się nie spodziewałeś (np. `AttributeError` z literówki).

Najlepszy wzorzec to: **najpierw konkretne wyjątki, na końcu ogólny — który loguje błąd i rzuca go dalej**:

```python
import logging

try:
    with open("ustawienia.txt", encoding="utf-8") as f:
        threshold = int(f.readline().strip())
except OSError as err:
    print(f"📁 Problem z plikiem: {err}")
except ValueError:
    print("🔢 W pliku nie ma poprawnej liczby całkowitej.")
except Exception as err:
    logging.exception("Nieoczekiwany błąd: %r", err)
    raise                     # ← nie połykamy! przekazujemy wyżej
```

Samo `raise` (bez argumentów) ponownie zgłasza właśnie obsługiwany wyjątek — więcej w sekcji o zgłaszaniu wyjątków.

---

## ✅ Blok `else` i świadome ignorowanie

> `else` wykonuje się tylko po udanym `try`, a `pass`, `continue` i `suppress` pozwalają celowo pominąć przewidziany błąd.

---

### 📌 Blok `else` — „gdy wszystko poszło dobrze”

Instrukcja `try` może mieć opcjonalny blok **`else`**, umieszczany **po wszystkich** blokach `except`. Wykona się on tylko wtedy, gdy blok `try` **nie zgłosił żadnego wyjątku**.

```python
import sys

for path in sys.argv[1:]:
    try:
        f = open(path, encoding="utf-8")
    except OSError:
        print(f"❌ Nie mogę otworzyć pliku {path}")
    else:
        print(f"✅ {path} ma {len(f.readlines())} linii")
        f.close()
```

> 💡 **Dlaczego nie wrzucić tego kodu po prostu do `try`?** Bo blok `try` powinien obejmować **tylko** to, co faktycznie może zgłosić obsługiwany wyjątek. Gdyby `f.readlines()` siedziało w `try`, a samo zgłosiło `OSError`, dostałbyś mylący komunikat „nie mogę otworzyć pliku”, choć plik otworzył się poprawnie. `else` chroni przed takim przypadkowym przechwyceniem.

---

### 🔇 Świadome ignorowanie: `pass`, `continue`, `suppress`

Czasem naprawdę chcesz zignorować błąd. Wtedy w bloku `except` umieszczasz `pass` (nic nie rób) albo — w pętli — `continue` (przejdź do następnej iteracji):

```python
values = [10, 5, 6, 0, 9, 8, 2]

for value in values:
    try:
        result = 10 / value
    except ZeroDivisionError:
        continue                 # pomiń zero, nie wykonuj kodu poniżej
    print(f"10 / {value} = {result:.2f}")
```

Siedem wartości, sześć wyników — zero zostało po cichu pominięte.

Eleganckim zamiennikiem `try`/`except`/`pass` jest `contextlib.suppress`:

```python
import os
from contextlib import suppress

with suppress(FileNotFoundError):
    os.remove("plik_tymczasowy.tmp")   # nie istnieje? trudno, idziemy dalej
```

> ⚠️ Ignoruj wyłącznie **konkretne, przewidziane** wyjątki. Konstrukcja `except Exception: pass` to jedna z najgorszych praktyk — błędy znikają bez śladu, a Ty godzinami szukasz, dlaczego program „po prostu nie działa”.

---

## 🚨 Zgłaszanie wyjątków: `raise`

> Twój kod też może zgłosić wyjątek — gdy wykryje sytuację, na którą nie powinien się godzić.

---

### 📌 Podstawowe użycie

```python
def set_age(age: int) -> int:
    if age < 0:
        raise ValueError(f"Wiek nie może być ujemny (podano: {age})")
    if age > 150:
        raise ValueError(f"Wiek {age} wygląda nierealnie")
    return age

try:
    set_age(-5)
except ValueError as e:
    print(f"⚠️  {e}")      # ⚠️  Wiek nie może być ujemny (podano: -5)
```

Dlaczego `raise`, a nie zwykłe `print("Zły wiek")`? Bo `print` tylko **informuje**, a program biegnie dalej z błędnymi danymi. `raise` **przerywa** bieg i zmusza kod wywołujący do podjęcia decyzji: obsłużyć problem albo pozwolić mu przerwać program.

Po `raise` podajesz **obiekt wyjątku** albo **klasę wyjątku** (dziedziczącą po `BaseException`). Klasę Python sam zamieni na obiekt, wywołując konstruktor bez argumentów:

```python
raise ValueError          # skrót od: raise ValueError()
```

---

### 🔁 Ponowne zgłoszenie: samo `raise`

Czasem chcesz **zauważyć** wyjątek i coś z tym zrobić — zapisać do logu, zamknąć połączenie, zapisać stan do pliku — ale **nie zamierzasz go obsługiwać**. Wtedy wewnątrz `except` używasz samego `raise`:

```python
>>> try:
...     raise NameError("CześćiCzołem")
... except NameError:
...     print("Przeleciał wyjątek! Zapisuję stan przed awarią… 💾")
...     raise
...
Przeleciał wyjątek! Zapisuję stan przed awarią… 💾
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
    raise NameError("CześćiCzołem")
NameError: CześćiCzołem
```

> 💡 To idealny wzorzec, gdy program **ma** się zatrzymać, ale nie chcesz, żeby zrobił to „po chamsku” — bez zamknięcia gniazda sieciowego, bez zapisania niedokończonej pracy, bez śladu w logach.

---

## 🔗 Łańcuch wyjątków: `raise ... from ...`

> Gdy podczas obsługi jednego wyjątku pojawia się kolejny, Python łączy je w łańcuch i pokazuje całą historię.

---

### 📌 Łańcuch niejawny

```python
>>> try:
...     open("baza.sqlite")
... except OSError:
...     raise RuntimeError("Nie potrafię obsłużyć tego błędu")
...
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
    open("baza.sqlite")
    ~~~~^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: 'baza.sqlite'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "<stdin>", line 4, in <module>
    raise RuntimeError("Nie potrafię obsłużyć tego błędu")
RuntimeError: Nie potrafię obsłużyć tego błędu
```

Komunikat *„During handling of the above exception, another exception occurred”* znaczy: **„w trakcie obsługi poprzedniego błędu wydarzył się kolejny”** — co zwykle sugeruje usterkę w samym kodzie obsługi.

---

### 🧷 Łańcuch jawny: `from`

Jeśli **celowo** zamieniasz jeden wyjątek na inny (np. niskopoziomowy błąd sieci na zrozumiały błąd Twojej aplikacji), powiedz to wprost za pomocą `from`:

```python
class ConfigError(Exception):
    """Błąd konfiguracji aplikacji."""

def load_port(config: dict) -> int:
    try:
        return int(config["port"])
    except KeyError as exc:
        raise ConfigError("W konfiguracji brakuje klucza 'port'") from exc
    except ValueError as exc:
        raise ConfigError(f"Port musi być liczbą, a nie {config['port']!r}") from exc

load_port({"host": "localhost"})
```

```
Traceback (most recent call last):
  File "config.py", line 6, in load_port
    return int(config["port"])
               ~~~~~~^^^^^^^^
KeyError: 'port'

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  ...
ConfigError: W konfiguracji brakuje klucza 'port'
```

Teraz komunikat brzmi *„The above exception was the direct cause…”* — **„powyższy wyjątek był bezpośrednią przyczyną następnego”**. Użytkownik Twojej funkcji dostaje czytelny `ConfigError`, a programista przy debugowaniu wciąż widzi pierwotny `KeyError`.

---

### ✂️ Przecięcie łańcucha: `from None`

Gdy pierwotny wyjątek to tylko szczegół implementacji, który niepotrzebnie zaśmieca komunikat, możesz go ukryć:

```python
>>> try:
...     open("baza.sqlite")
... except OSError:
...     raise RuntimeError("Baza danych jest niedostępna") from None
...
Traceback (most recent call last):
  File "<stdin>", line 4, in <module>
    raise RuntimeError("Baza danych jest niedostępna") from None
RuntimeError: Baza danych jest niedostępna
```

---

### ⚖️ Podsumowanie — który zapis kiedy?

|Zapis|Komunikat łączący|Kiedy stosować|
|---|---|---|
|`raise Nowy(...)` w `except`|*During handling of the above exception…*|Raczej nieplanowane — błąd w obsłudze błędu|
|`raise Nowy(...) from exc`|*The above exception was the direct cause…*|Świadoma zamiana wyjątku na inny|
|`raise Nowy(...) from None`|*(brak — łańcuch ukryty)*|Pierwotny wyjątek jest nieistotny dla odbiorcy|

---

## 🏗️ Własne wyjątki

> Wbudowane wyjątki mówią o problemach technicznych — reguły biznesowe Twojej aplikacji zasługują na własne, wymowne klasy.

---

### 📌 Najprostszy własny wyjątek

Twoja aplikacja ma własne reguły — „kwota musi być dodatnia”, „brak środków na koncie”, „produkt niedostępny”. Do ich zgłaszania wystarczy klasa dziedzicząca (bezpośrednio lub pośrednio) po `Exception`:

```python
class InsufficientFundsError(Exception):
    """Na koncie brakuje środków na wykonanie operacji."""
```

Tak, to wszystko — cała moc pochodzi z dziedziczenia. Docstring zamiast `pass` to dobry zwyczaj: od razu dokumentuje, co wyjątek oznacza.

> 💡 **Konwencja nazewnicza:** nazwy wyjątków kończą się zwykle na **`Error`** — dokładnie tak jak wbudowane `ValueError` czy `TypeError`.

---

### 💡 Przykład praktyczny: wirtualny portfel 💰

Reguły: kwota wpłaty musi być **dodatnia** i **nie większa niż 1000 zł**. Każde naruszenie ma mieć osobny komunikat.

```python
class WalletError(Exception):
    """Bazowy wyjątek dla wszystkich błędów portfela."""

class AmountTooLowError(WalletError):
    """Kwota wpłaty jest zerowa lub ujemna."""

class AmountTooHighError(WalletError):
    """Kwota wpłaty przekracza dopuszczalny limit."""


MAX_DEPOSIT = 1000

def validate_deposit(amount: int) -> None:
    if amount <= 0:
        raise AmountTooLowError(f"Kwota musi być dodatnia (podano {amount} zł).")
    if amount > MAX_DEPOSIT:
        raise AmountTooHighError(f"Limit to {MAX_DEPOSIT} zł (podano {amount} zł).")


total = 0
for _ in range(5):
    try:
        amount = int(input("Podaj kwotę wpłaty: "))
        validate_deposit(amount)
    except ValueError:
        print("❌ To nie jest liczba.")
    except AmountTooLowError as e:
        print(f"📉 Za mało! {e}")
    except AmountTooHighError as e:
        print(f"📈 Za dużo! {e}")
    else:
        total += amount
        print(f"✅ Wpłacono {amount} zł.")

print(f"\n💰 Razem wpłacono: {total} zł")
```

```
Podaj kwotę wpłaty: 200
✅ Wpłacono 200 zł.
Podaj kwotę wpłaty: sto
❌ To nie jest liczba.
Podaj kwotę wpłaty: -10
📉 Za mało! Kwota musi być dodatnia (podano -10 zł).
Podaj kwotę wpłaty: 1111
📈 Za dużo! Limit to 1000 zł (podano 1111 zł).
Podaj kwotę wpłaty: 50
✅ Wpłacono 50 zł.

💰 Razem wpłacono: 250 zł
```

Zwróć uwagę na trzy rzeczy:

- 🧬 **Wspólna klasa bazowa `WalletError`** pozwala złapać *wszystkie* błędy portfela jednym `except WalletError`, a jednocześnie rozróżniać je, gdy trzeba.
- ✂️ **Walidacja wydzielona do funkcji** — kod jest czytelniejszy niż gąszcz `if`-ów w pętli.
- 🛡️ **Dodawanie do sumy w `else`** — wykona się tylko dla poprawnej kwoty.

---

### 🧬 Wyjątki z dodatkowymi informacjami

Wyjątek to pełnoprawna klasa, więc może przechowywać dane przydatne przy obsłudze błędu:

```python
class AmountTooHighError(WalletError):
    def __init__(self, amount: int, limit: int):
        self.amount = amount
        self.limit = limit
        self.excess = amount - limit
        super().__init__(f"Przekroczono limit o {self.excess} zł (limit: {limit} zł).")


try:
    raise AmountTooHighError(amount=1500, limit=1000)
except AmountTooHighError as e:
    print(e)                                         # Przekroczono limit o 500 zł (limit: 1000 zł).
    print(f"Możesz wpłacić jeszcze najwyżej {e.limit} zł.")
```

W prawdziwych projektach w ten sposób zapisuje się np. adres API, z którym nie udało się połączyć, kod odpowiedzi serwera czy znacznik czasu awarii.

> 💡 Wiele modułów biblioteki standardowej (i bibliotek zewnętrznych) definiuje własne wyjątki — np. `json.JSONDecodeError` czy `requests.exceptions.Timeout`. Ich dokumentacja zwykle mówi, **kiedy** dana funkcja je zgłasza. Warto tam zaglądać, bo dzięki temu wiesz, co przechwytywać.

---

## 🧹 Sprzątanie: `finally`

> Blok `finally` wykonuje się zawsze — niezależnie od tego, czy wyjątek wystąpił, został obsłużony, czy poleciał dalej.

---

### 📌 Co to robi?

Instrukcja `try` ma jeszcze jeden opcjonalny blok — **`finally`**. Jego zawartość wykona się **zawsze**, jako ostatni krok przed opuszczeniem instrukcji `try`:

```python
>>> try:
...     raise KeyboardInterrupt
... finally:
...     print("Do widzenia, świecie! 👋")
...
Do widzenia, świecie! 👋
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
    raise KeyboardInterrupt
KeyboardInterrupt
```

---

### 🔬 Pełna instrukcja w akcji

```python
def divide(x, y):
    try:
        result = x / y
    except ZeroDivisionError:
        print("🚫 Dzielenie przez zero!")
    else:
        print(f"✅ Wynik: {result}")
    finally:
        print("🧹 Sprzątam (finally)")
```

|Wywołanie|Co zobaczysz|Wyjaśnienie|
|---|---|---|
|`divide(10, 4)`|`✅ Wynik: 2.5`<br/>`🧹 Sprzątam (finally)`|Brak wyjątku → `else`, potem `finally`|
|`divide(10, 0)`|`🚫 Dzielenie przez zero!`<br/>`🧹 Sprzątam (finally)`|Obsłużony wyjątek → `except`, potem `finally`|
|`divide("10", "4")`|`🧹 Sprzątam (finally)`<br/>`TypeError: unsupported operand…`|Nieobsłużony `TypeError` → najpierw `finally`, **potem** wyjątek leci dalej|

---

### 🏗️ Do czego to służy w praktyce?

Do **zwalniania zasobów zewnętrznych**: zamykania plików, połączeń sieciowych, połączeń z bazą danych, zwalniania blokad — bez względu na to, czy praca się udała:

```python
connection = connect_to_database()      # funkcja przykładowa
try:
    connection.execute("UPDATE konta SET saldo = saldo - 100 WHERE id = 7")
finally:
    connection.close()                  # połączenie zamknie się ZAWSZE
```

---

### ⚠️ Szczegółowe reguły i pułapki

- Jeśli wyjątek z `try` **nie został obsłużony** przez żaden `except`, zostanie zgłoszony ponownie **po** wykonaniu `finally`.
- To samo dotyczy wyjątku, który wystąpi **wewnątrz** `except` lub `else` — najpierw `finally`, potem wyjątek leci dalej.
- Jeśli blok `try` dojdzie do `break`, `continue` lub `return`, `finally` wykona się **tuż przed** nimi.

**Nie umieszczaj `return`, `break` ani `continue` w bloku `finally`.** Takie instrukcje „połykają” wyjątki i nadpisują wartość zwracaną z `try`:

```python
>>> def bool_return():
...     try:
...         return True
...     finally:
...         return False
...
>>> bool_return()
False
```

> ⚠️ Od Pythona 3.14 kompilator ostrzega przed tym komunikatem `SyntaxWarning: 'return' in a 'finally' block` ([PEP 765](https://peps.python.org/pep-0765/)).

---

## 🚪 Gotowe sprzątanie: `with`

> Menedżery kontekstu same po sobie sprzątają — `with` to wygodny skrót dla wzorca `try` / `finally`.

---

### 📌 Problem: plik otwarty „na zawsze”

Niektóre obiekty same wiedzą, jak po sobie posprzątać. Spójrz na ten kod:

```python
for line in open("moj_plik.txt", encoding="utf-8"):
    print(line, end="")
```

Działa, ale plik pozostaje otwarty przez **nieokreślony czas**. W małym skrypcie to drobiazg, w dużej aplikacji — wyciek zasobów. Rozwiązaniem jest instrukcja **`with`**:

```python
with open("moj_plik.txt", encoding="utf-8") as f:
    for line in f:
        print(line, end="")
# ← tutaj plik jest już na pewno zamknięty — nawet jeśli w pętli wystąpił wyjątek
```

---

### 🔬 Co `with` robi za kulisami?

`with` to w gruncie rzeczy wygodny skrót dla wzorca `try`/`finally`:

```python
# To, co robi „with” za kulisami (w uproszczeniu):
f = open("moj_plik.txt", encoding="utf-8")
try:
    for line in f:
        print(line, end="")
finally:
    f.close()
```

---

### 🧰 Menedżery kontekstu

Obiekty obsługujące `with` nazywamy **menedżerami kontekstu** (*context managers*). Poza plikami to m.in.:

|Menedżer kontekstu|Co sprząta automatycznie|
|---|---|
|`open(...)`|Zamyka plik|
|`threading.Lock()`|Zwalnia blokadę|
|`tempfile.TemporaryDirectory()`|Usuwa katalog tymczasowy|
|`contextlib.suppress(...)`|„Połyka” wskazane wyjątki|

> 💡 Obiekty, które zapewniają takie automatyczne sprzątanie, mówią o tym w swojej dokumentacji. Gdy masz wybór między ręcznym `try`/`finally` a `with` — **wybieraj `with`**.

---

## 🧺 Grupy wyjątków: `ExceptionGroup` i `except*`

> Zamiast reagować tylko na pierwszy błąd, można zebrać wszystkie i zgłosić je razem.

---

### 📌 Kiedy jeden błąd to za mało?

Zwykle reagujemy na **pierwszy** błąd. Bywają jednak sytuacje, w których lepiej **zebrać wszystkie** i zgłosić je razem:

- 🧵 kilka zadań wykonywanych **równolegle** (np. w `asyncio`) zawiodło jednocześnie,
- 📝 walidujesz formularz i chcesz pokazać użytkownikowi **wszystkie** błędy, a nie tylko pierwszy,
- 🧪 uruchamiasz serię testów i zbierasz wszystkie niepowodzenia.

Wbudowana klasa `ExceptionGroup` przechowuje listę wyjątków. Sama też jest wyjątkiem, więc można ją zgłosić i przechwycić jak każdy inny:

```python
>>> def f():
...     excs = [OSError("błąd 1"), SystemError("błąd 2")]
...     raise ExceptionGroup("były problemy", excs)
...
>>> f()
  + Exception Group Traceback (most recent call last):
  |   File "<stdin>", line 1, in <module>
  |     f()
  |     ~^^
  |   File "<stdin>", line 3, in f
  |     raise ExceptionGroup("były problemy", excs)
  | ExceptionGroup: były problemy (2 sub-exceptions)
  +-+---------------- 1 ----------------
    | OSError: błąd 1
    +---------------- 2 ----------------
    | SystemError: błąd 2
    +------------------------------------
```

---

### 🎯 `except*` — wybieranie z paczki

Zwykły `except` traktuje grupę jako całość. Wersja z gwiazdką, **`except*`**, „wyciąga” z grupy tylko wyjątki pasującego typu — pozostałe przechodzą do kolejnych bloków, a jeśli nikt ich nie obsłuży, są zgłaszane dalej.

Praktyczny przykład — walidacja formularza, która zbiera **wszystkie** błędy:

```python
def validate_user(data: dict) -> None:
    errors = []
    if not data.get("name"):
        errors.append(ValueError("Imię jest wymagane"))
    if "@" not in data.get("email", ""):
        errors.append(ValueError("Niepoprawny adres e-mail"))
    if not isinstance(data.get("age"), int):
        errors.append(TypeError("Wiek musi być liczbą całkowitą"))
    if errors:
        raise ExceptionGroup("Formularz zawiera błędy", errors)


try:
    validate_user({"name": "", "email": "jan.kowalski.pl", "age": "trzydzieści"})
except* ValueError as eg:
    for err in eg.exceptions:
        print(f"⚠️  Niepoprawna wartość: {err}")
except* TypeError as eg:
    for err in eg.exceptions:
        print(f"⚠️  Niepoprawny typ: {err}")
```

```
⚠️  Niepoprawna wartość: Imię jest wymagane
⚠️  Niepoprawna wartość: Niepoprawny adres e-mail
⚠️  Niepoprawny typ: Wiek musi być liczbą całkowitą
```

Zwróć uwagę: **wykonały się oba bloki `except*`** — to zasadnicza różnica w porównaniu ze zwykłym `except`, gdzie wykonuje się co najwyżej jeden.

> ⚠️ Trzy rzeczy do zapamiętania:
>
> - Wewnątrz grupy umieszczasz **obiekty** wyjątków (`ValueError("…")`), a nie same klasy (`ValueError`).
> - W jednej instrukcji `try` nie można mieszać `except` z `except*`.
> - Grupy mogą być **zagnieżdżone** — `except*` przeszukuje je w całości.

---

### 🏗️ Zbieranie błędów w praktyce

Typowy wzorzec — wykonaj wszystko, zapamiętaj każde niepowodzenie, a na końcu zgłoś je razem:

```python
errors = []
for test in tests:
    try:
        test.run()
    except Exception as e:
        errors.append(e)

if errors:
    raise ExceptionGroup("Niepowodzenia testów", errors)
```

---

## 📝 Notatki w wyjątkach: `add_note()`

> Kod, który przechwycił wyjątek, może dopisać do niego kontekst — traceback pokaże wszystkie notatki.

---

### 📌 Dopisywanie kontekstu

Wyjątek zwykle tworzy się z opisem tego, **co** poszło nie tak. Czasem jednak dopiero kod, który go przechwycił, zna ważny **kontekst** — np. numer wiersza w pliku albo identyfikator użytkownika. Do tego służy metoda **`add_note()`**: dopisuje tekst do wyjątku, a traceback wyświetla wszystkie notatki w kolejności dodania.

```python
>>> try:
...     raise TypeError("zły typ")
... except Exception as e:
...     e.add_note("Dane pochodziły z formularza rejestracji")
...     e.add_note("Użytkownik: jan@example.com")
...     raise
...
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
    raise TypeError("zły typ")
TypeError: zły typ
Dane pochodziły z formularza rejestracji
Użytkownik: jan@example.com
```

---

### 💡 Notatki + grupa wyjątków = idealny raport

Wczytujemy dane (skrypt `wczytaj.py`) i chcemy wiedzieć, **w którym wierszu** wystąpił każdy błąd:

```python
rows = ["12", "7", "abc", "30", ""]
errors = []

for line_no, raw in enumerate(rows, start=1):
    try:
        value = int(raw)
    except ValueError as e:
        e.add_note(f"📍 Wiersz {line_no}: {raw!r}")
        errors.append(e)

if errors:
    raise ExceptionGroup("Nie udało się wczytać części danych", errors)
```

```
  + Exception Group Traceback (most recent call last):
  |   File "wczytaj.py", line 12, in <module>
  |     raise ExceptionGroup("Nie udało się wczytać części danych", errors)
  | ExceptionGroup: Nie udało się wczytać części danych (2 sub-exceptions)
  +-+---------------- 1 ----------------
    | Traceback (most recent call last):
    |   File "wczytaj.py", line 6, in <module>
    |     value = int(raw)
    | ValueError: invalid literal for int() with base 10: 'abc'
    | 📍 Wiersz 3: 'abc'
    +---------------- 2 ----------------
    | Traceback (most recent call last):
    |   File "wczytaj.py", line 6, in <module>
    |     value = int(raw)
    | ValueError: invalid literal for int() with base 10: ''
    | 📍 Wiersz 5: ''
    +------------------------------------
```

> 💡 Każdy wyjątek w grupie zachowuje własny traceback — widać zarówno **gdzie** wystąpił, jak i **którego wiersza** dotyczył.

---

## 🏆 Dobre praktyki

> Zasady, które odróżniają kod amatorski od profesjonalnego.

---

### 🎯 Bądź konkretny

```python
# ❌ Źle — łapie wszystko, także literówki i błędy logiczne
try:
    result = int(user_input) / divisor
except Exception:
    print("Coś poszło nie tak")

# ✅ Dobrze — obsługujesz to, czego się spodziewasz
try:
    result = int(user_input) / divisor
except ValueError:
    print("Podaj poprawną liczbę.")
except ZeroDivisionError:
    print("Dzielnik nie może być zerem.")
```

Konkretne wyjątki = precyzyjna reakcja i łatwiejsze debugowanie. Ogólny `except Exception` jest dopuszczalny **na końcu**, jako siatka bezpieczeństwa — pod warunkiem, że **loguje** błąd.

---

### 🔇 Nie połykaj błędów

```python
import logging

# ❌ Źle — błąd znika bez śladu
try:
    process(data)
except Exception:
    pass

# ✅ Dobrze — przynajmniej zostaw ślad
try:
    process(data)
except Exception as e:
    logging.exception("Przetwarzanie nie powiodło się: %s", e)
```

---

### 📣 Fail fast, fail loudly — zawiedź szybko i głośno

Lepiej, żeby program zatrzymał się **od razu** z jasnym komunikatem, niż żeby działał dalej na błędnych danych i zepsuł coś trzy moduły dalej.

```python
def calculate_discount(price: float, percent: float) -> float:
    if not 0 <= percent <= 100:
        raise ValueError(f"Rabat musi mieścić się w zakresie 0–100%, podano {percent}%")
    return price * (1 - percent / 100)
```

---

### ✂️ Trzymaj blok `try` krótko

Umieszczaj w `try` **tylko** linie, które mogą zgłosić obsługiwany wyjątek. Resztę przenieś do `else` lub za instrukcję.

---

### 🪂 Degraduj się z gracją (*graceful degradation*)

Gdy coś zawiedzie, program często może działać dalej — w okrojonej formie:

```python
import logging

def get_user_profile(user_id: int) -> dict:
    try:
        return fetch_profile_from_api(user_id)
    except ConnectionError:
        logging.warning("API niedostępne — zwracam profil podstawowy (id=%s)", user_id)
        return {"id": user_id, "name": "Gość", "details_available": False}
```

Albo ponowić próbę — jak w przykładzie z bazą danych z sekcji „Po co nam wyjątki?”:

```python
import time

def connect_with_retry(attempts: int = 3, delay: float = 2.0):
    for attempt in range(1, attempts + 1):
        try:
            return connect_to_database()
        except ConnectionError as e:
            if attempt == attempts:
                raise ConnectionError(f"Nie udało się połączyć po {attempts} próbach") from e
            print(f"🔄 Trwa ponowna próba połączenia ({attempt}/{attempts})…")
            time.sleep(delay)
```

> 💡 Po ostatniej nieudanej próbie nie ma sensu czekać — od razu zgłaszamy błąd, a `from e` zachowuje w tracebacku pierwotną przyczynę.

---

### ⚖️ Nie nadużywaj wyjątków

Wyjątki **nie zastępują** zwykłej logiki ani walidacji. Jeśli coś jest normalną, częstą ścieżką programu, często lepiej sprawdzić to wprost:

```python
# Dla słownika czytelniej jest użyć .get(), niż łapać KeyError
color = settings.get("color", "niebieski")
```

> 💡 W Pythonie mówi się o dwóch filozofiach: **LBYL** (*Look Before You Leap* — „sprawdź, zanim skoczysz”) i **EAFP** (*Easier to Ask Forgiveness than Permission* — „łatwiej prosić o wybaczenie niż o pozwolenie”). Python często preferuje EAFP, czyli `try`/`except` — ale zdrowy rozsądek wygrywa z dogmatem.

---

### 🔒 Nie loguj danych wrażliwych

Hasła, numery kart, tokeny dostępowe czy dane osobowe **nie mają czego szukać** w logach — nawet w komunikatach o błędach.

---

## 📓 Logowanie błędów

> `print` wystarcza na początku — w prawdziwej aplikacji potrzebujesz modułu `logging`: poziomów ważności, znaczników czasu i zapisu do pliku.

---

### 📌 Poziomy logowania

|Poziom|Wartość|Kiedy używać|
|---|:---:|---|
|🔍 `DEBUG`|10|Szczegóły przydatne tylko przy szukaniu błędów|
|ℹ️ `INFO`|20|Potwierdzenie, że wszystko działa zgodnie z planem|
|⚠️ `WARNING`|30|Coś nieoczekiwanego, ale program działa dalej|
|❌ `ERROR`|40|Poważny problem — jakaś operacja się nie powiodła|
|🔥 `CRITICAL`|50|Katastrofa — program może nie być w stanie działać|

`logging.basicConfig(level=...)` ustawia **minimalny** poziom — komunikaty o niższej ważności są pomijane.

---

### 🏗️ Logowanie z kontekstem — do pliku

```python
import logging

logging.basicConfig(
    level=logging.INFO,
    format="%(asctime)s | %(levelname)-8s | %(message)s",
    filename="moj_program.log",
    encoding="utf-8",
)
logger = logging.getLogger(__name__)


def average(numbers: list[float]) -> float | None:
    logger.debug("Liczę średnią z: %s", numbers)          # pominięte przy poziomie INFO
    if not numbers:
        logger.warning("Otrzymano pustą listę — brak danych do obliczeń")
        return None
    try:
        result = sum(numbers) / len(numbers)
    except TypeError:
        logger.exception("Lista zawiera niepoprawne elementy: %r", numbers)
        return None
    logger.info("Średnia obliczona pomyślnie: %.2f", result)
    return result


average([4, 8, 15])
average([])
average([1, "dwa", 3])
```

Zawartość `moj_program.log`:

```
2026-10-12 10:15:01,123 | INFO     | Średnia obliczona pomyślnie: 9.00
2026-10-12 10:15:01,124 | WARNING  | Otrzymano pustą listę — brak danych do obliczeń
2026-10-12 10:15:01,124 | ERROR    | Lista zawiera niepoprawne elementy: [1, 'dwa', 3]
Traceback (most recent call last):
  File "srednia.py", line 18, in average
    result = sum(numbers) / len(numbers)
             ~~~^^^^^^^^^
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

> 💡 `logger.exception(...)` wywołany wewnątrz `except` zapisuje komunikat na poziomie `ERROR` **wraz z pełnym tracebackiem**. Loguj nie tylko sam błąd, ale też **dane, które go wywołały** — to skraca debugowanie z godzin do minut.

---

### 🌐 Logowanie scentralizowane

Gdy aplikacja działa na wielu serwerach albo u klientów, warto zbierać błędy w jednym miejscu. Służą do tego usługi takie jak **Sentry** — wysyłają pełny wyjątek z kontekstem, grupują podobne błędy i pokazują, które występują najczęściej. Dzięki temu nie musisz dopytywać użytkownika: „A gdzie panu ten błąd wyskoczył?”.

---

## 🔎 Debugowanie

> Obsługa błędów to jedno, a znalezienie ich przyczyny — drugie. Podstawowy warsztat detektywa.

---

### 📌 Czytaj traceback (od dołu!)

Wróć do sekcji o anatomii tracebacku: ostatnia linia mówi **co**, linie nad nią mówią **gdzie**, a cała reszta pokazuje **drogę**, którą przebył wyjątek.

---

### 🔁 Odtwórz błąd

Żeby naprawić błąd, musisz umieć go **wywołać na żądanie**. Zapisz dokładne kroki, które do niego prowadzą, i spróbuj zbudować **minimalny przykład** — najkrótszy kod, który wciąż się wysypuje.

---

### 🖨️ `print` — skromny, ale skuteczny

```python
def process_data(data):
    print(f"[DEBUG] Wejście: {data!r} (typ: {type(data).__name__})")
    result = data ** 2
    print(f"[DEBUG] Wynik: {result!r}")
    return result

process_data(5)          # działa: 25
process_data("hello")    # TypeError: unsupported operand type(s) for ** or pow(): 'str' and 'int'
```

Wydruk `typ: str` tuż przed awarią od razu zdradza winowajcę.

---

### 🐞 Debugger: `breakpoint()`

Wstaw `breakpoint()` w dowolnym miejscu kodu — program zatrzyma się tam i otworzy interaktywny debugger `pdb`. Możesz podglądać zmienne (`p nazwa`), wykonywać kolejne linie (`n`), wchodzić do funkcji (`s`) i wznowić działanie (`c`).

---

## 🧪 Testowanie obsługi błędów

> Kod obsługi błędów to też kod — i też może mieć błędy. Trzeba go testować.

---

### 📌 Test bez bibliotek

```python
def divide(a: float, b: float) -> float:
    if b == 0:
        raise ValueError("Nie można dzielić przez zero")
    return a / b


def test_divide_by_zero():
    try:
        divide(10, 0)
    except ValueError as e:
        assert str(e) == "Nie można dzielić przez zero"
    else:
        raise AssertionError("Oczekiwano ValueError, a nic się nie stało!")


test_divide_by_zero()
print("✅ Test zaliczony")
```

Test sprawdza dwie rzeczy: że wyjątek **w ogóle** wystąpił (inaczej trafimy do `else` i zgłosimy `AssertionError`) oraz że ma **właściwy komunikat**.

> 💡 W `else` używamy `raise AssertionError(...)` zamiast `assert False` — instrukcje `assert` znikają, gdy Python działa z flagą `-O`, a jawne `raise` zadziała zawsze.

---

### ⚡ Test z `pytest`

W bibliotece `pytest` to samo zapisujemy znacznie zwięźlej:

```python
import pytest

def test_divide_by_zero():
    with pytest.raises(ValueError, match="dzielić przez zero"):
        divide(10, 0)
```

---

### 💥 Wstrzykiwanie awarii (*fault injection*)

Jak sprawdzić, czy program poradzi sobie z awarią sieci, skoro sieć akurat działa? **Wywołaj awarię celowo:**

```python
import random

def unreliable_fetch(text: str) -> str:
    if random.random() < 0.2:                       # 20% szans na awarię
        raise ConnectionError("Symulowana awaria sieci 🔌")
    return text.upper()

def safe_fetch(text: str) -> str | None:
    try:
        return unreliable_fetch(text)
    except ConnectionError:
        return None


def test_fault_injection():
    random.seed(42)                                  # powtarzalne wyniki
    successes = failures = 0
    for _ in range(100):
        result = safe_fetch("python")
        if result is None:
            failures += 1
        else:
            assert result == "PYTHON"
            successes += 1
    print(f"Sukcesy: {successes}, obsłużone awarie: {failures}")
    assert successes + failures == 100


test_fault_injection()
# → Sukcesy: 81, obsłużone awarie: 19
```

Sto prób, żadna nie wysypała programu — obsługa błędów zdała egzamin. 🎓

---

## 📖 Słowniczek PL ⇄ EN

> Polskie terminy z tego rozdziału i ich angielskie odpowiedniki z dokumentacji.

---

|Polski termin|Angielski odpowiednik|
|---|---|
|wyjątek|*exception*|
|błąd składni|*syntax error*|
|zgłosić / rzucić wyjątek|*raise an exception*|
|obsłużyć / przechwycić wyjątek|*handle / catch an exception*|
|nieobsłużony wyjątek|*unhandled exception*|
|ślad stosu|*traceback / stack trace*|
|propagacja wyjątku|*exception propagation*|
|łańcuch wyjątków|*exception chaining*|
|działania porządkujące|*clean-up actions*|
|menedżer kontekstu|*context manager*|
|grupa wyjątków|*exception group*|
|łagodna degradacja|*graceful degradation*|
|wstrzykiwanie awarii|*fault injection*|

---

## 📋 Cheat Sheet

> Najważniejsze wzorce z tego rozdziału w jednym miejscu.

---

```python
# ════════════════════════════════════════════
#  TRY / EXCEPT / ELSE / FINALLY
# ════════════════════════════════════════════

try:
    ...                                  # kod, który może zawieść (jak najkrócej!)
except (ValueError, TypeError) as e:
    ...                                  # obsługa spodziewanych błędów
except Exception:
    logging.exception("Nieoczekiwany błąd")
    raise                                # nieznanego błędu nie połykamy
else:
    ...                                  # tylko gdy try zakończył się sukcesem
finally:
    ...                                  # ZAWSZE — sprzątanie

try:
    ...
except ValueError, TypeError:            # Python 3.14+ — bez nawiasów (tylko bez "as")
    ...
except LookupError:                      # łapie też potomków: KeyError, IndexError
    ...

from contextlib import suppress
with suppress(FileNotFoundError):        # świadome ignorowanie konkretnego błędu
    os.remove("plik.tmp")

# ════════════════════════════════════════════
#  RAISE I ŁAŃCUCH WYJĄTKÓW
# ════════════════════════════════════════════

raise ValueError("opis")                 # zgłoś nowy wyjątek
raise ValueError                         # skrót od raise ValueError()
raise                                    # (w except) zgłoś ponownie obsługiwany wyjątek
raise ConfigError("...") from exc        # jawna przyczyna → "direct cause"
raise ConfigError("...") from None       # ukryj łańcuch

# ════════════════════════════════════════════
#  WŁASNE WYJĄTKI
# ════════════════════════════════════════════

class AppError(Exception):               # wspólna baza dla błędów aplikacji
    """Bazowy wyjątek aplikacji."""

class NotFoundError(AppError):           # nazwy kończą się na "Error"
    def __init__(self, item_id):
        self.item_id = item_id           # dodatkowe dane dla obsługi błędu
        super().__init__(f"Nie znaleziono: {item_id}")

# ════════════════════════════════════════════
#  SPRZĄTANIE
# ════════════════════════════════════════════

with open("plik.txt", encoding="utf-8") as f:   # zamknie się zawsze — preferuj with
    ...

zasob = otworz()
try:
    ...
finally:
    zasob.close()                        # bez return/break/continue w finally!

# ════════════════════════════════════════════
#  GRUPY I NOTATKI
# ════════════════════════════════════════════

raise ExceptionGroup("opis", [ValueError("a"), TypeError("b")])

try:
    ...
except* ValueError as eg:                # może wykonać się kilka bloków except*
    for err in eg.exceptions: ...

e.add_note("kontekst, np. numer wiersza")   # dopisz informację do wyjątku

# ════════════════════════════════════════════
#  LOGOWANIE I TESTY
# ════════════════════════════════════════════

logger.exception("Błąd dla id=%s", user_id)   # w except: ERROR + pełny traceback

with pytest.raises(ValueError, match="zero"):
    divide(10, 0)

# ════════════════════════════════════════════
#  ZŁOTE ZASADY
# ════════════════════════════════════════════

# 1. Łap KONKRETNE wyjątki — od szczegółu do ogółu
# 2. Nigdy nie połykaj błędów po cichu (except Exception: pass ❌)
# 3. Zgłaszaj szybko i głośno (fail fast)
# 4. Blok try — jak najkrótszy, reszta do else
# 5. Zasoby zamykaj przez with (albo finally)
# 6. Loguj błąd z kontekstem, ale bez danych wrażliwych
# 7. Testuj ścieżki błędów tak samo jak ścieżki sukcesu
```

---


<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>



<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=100&section=footer" width="100%"/>
</div>
