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
├── 07-input-output/
│   ├── notes.py
│   └── README.md
```

---

## 📝 Notatki

Wszystkie przemyślenia i skróty myślowe z każdych zagadnień w [NOTES.md](./NOTES.md)

---

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
