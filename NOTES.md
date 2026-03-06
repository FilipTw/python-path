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
