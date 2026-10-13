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
├── 08-errors-exceptions/
│   ├── notes.py
│   └── README.md
```

---

## 📝 Notatki

Wszystkie przemyślenia i skróty myślowe z każdych zagadnień w [NOTES.md](../NOTES.md)

---

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
