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
