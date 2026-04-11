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
