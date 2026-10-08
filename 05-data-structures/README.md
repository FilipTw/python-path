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
├── 05-data-structures/
│   ├── notes.py
│   └── README.md
```

---

## 📝 Notatki

Wszystkie przemyślenia i skróty myślowe z każdych zagadnień w [NOTES.md](../NOTES.md)

---

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
