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
├── 03-informal-introduction/
│   ├── notes.py
│   └── README.md
```

---

## 📝 Notatki

Wszystkie przemyślenia i skróty myślowe z każdych zagadnień w [NOTES.md](./NOTES.md)


---

<div align="center">

# Nieformalne Wprowadzenie do Pythona

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