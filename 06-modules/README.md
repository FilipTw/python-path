<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,20,24&height=160&section=header&text=🐍%20python-path&fontSize=50&fontColor=fff&fontAlignY=40" width="100%"/>
</div>

# Python Path

> Od zera do automatyzacji. Uczę się Pythona solidnie, temat po temacie.

---

## 📁 Struktura

```
python-path/
│
├── 06-modules/
│   ├── notes.py
│   └── README.md
```

---

## 📝 Notatki

Wszystkie przemyślenia i skróty myślowe z każdych zagadnień w [NOTES.md](./NOTES.md)

---

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
