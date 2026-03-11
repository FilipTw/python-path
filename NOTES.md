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
