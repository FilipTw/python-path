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
├── 09-classes/
│   ├── notes.py
│   └── README.md
```

---

## 📝 Notatki

Wszystkie przemyślenia i skróty myślowe z każdych zagadnień w [NOTES.md](../NOTES.md)

---

<div align="center">

# Classes

*data: -*

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![2026](https://img.shields.io/badge/perspektywa-2026%2B-0d1117?style=for-the-badge&logoColor=white)
![Temat](https://img.shields.io/badge/temat-classes-3776AB?style=for-the-badge)

</div>

---

Rozdział 09 skupia się na klasach w Pythonie i praktycznym operowaniu na:

> ⌲ nazwach, przestrzeniach nazw i zasięgach (LEGB, `global`, `nonlocal`)
>
> ⌲ definiowaniu klas, instancjach, metodach i `self`
>
> ⌲ zmiennych klasy i instancji, metodach specjalnych i `@dataclass`
>
> ⌲ dziedziczeniu (także wielokrotnym), MRO i `super()`
>
> ⌲ hermetyzacji, właściwościach (`@property`), `@classmethod` i `@staticmethod`
>
> ⌲ polimorfizmie, klasach abstrakcyjnych, protokołach i typach generycznych
>
> ⌲ iteratorach, generatorach i wyrażeniach generatorowych

---

## 🏡 Jedna historia: inteligentny dom

> Klasy najłatwiej zrozumieć na czymś namacalnym — dlatego cały rozdział opowiada jedną historię: projektujemy i budujemy inteligentny dom.

---

### 📌 Plan budowy

Każde nowe pojęcie dokłada do domu kolejną cegiełkę, a przykłady z różnych sekcji pasują do siebie jak elementy jednego projektu.

|Etap|Co budujemy|Czego się uczysz|
|:---:|---|---|
|🧱|Fundamenty|czym jest klasa, jak działają nazwy, przestrzenie nazw i zasięgi|
|🏠|Dom i jego pokoje (`Dom`, `Pokoj`)|definicja klasy, `__init__`, `self`, atrybuty, metody, metody specjalne, `@dataclass`|
|🔌|Urządzenia (`Urzadzenie`, `Lampa`, `Glosnik`, `Termostat`)|dziedziczenie, MRO, zmienne prywatne, `@property`, `@classmethod`, `@staticmethod`|
|🤝|Kontrakty między domem a urządzeniami|polimorfizm, *duck typing*, klasy abstrakcyjne, protokoły, typy generyczne|
|🚶|Obchód domu|iteratory, generatory, wyrażenia generatorowe|
|🏁|Wszystko razem|kompletny mini-system, dobre praktyki, słowniczek, ściąga|

> 💡 Każda sekcja jest samodzielna: kod z danej sekcji działa bez kopiowania czegokolwiek z poprzednich. Dzięki temu możesz wracać do wybranych tematów w dowolnej kolejności.

---

### 🗺️ Mapa dokumentacji

Notatki bazują na rozdziale 9 oficjalnego tutoriala ([Classes](https://docs.python.org/3/tutorial/classes.html)) i rozszerzają go o tematy, które w praktyce idą z klasami w parze. Ta tabela pokazuje, gdzie czego szukać:

|Dokumentacja (rozdz. 9)|Sekcja w tych notatkach|
|---|---|
|Wstęp|Czym właściwie jest klasa?|
|9.1 A Word About Names and Objects|Nazwy i obiekty|
|9.2 Python Scopes and Namespaces|Przestrzenie nazw i zasięgi|
|9.3 A First Look at Classes|Pierwsza klasa: `Dom` · Zmienne klasy i zmienne instancji|
|9.4 Random Remarks|Zmienne klasy i zmienne instancji · Kilka uwag różnych|
|9.5 Inheritance|Dziedziczenie · Dziedziczenie wielokrotne i MRO|
|9.6 Private Variables|Zmienne prywatne i hermetyzacja|
|9.7 Odds and Ends|Pierwsza klasa: `Dom` (obiekty metod) · Metody specjalne i `@dataclass` · Polimorfizm i *duck typing*|
|9.8 Iterators|Iteratory|
|9.9 Generators|Generatory|
|9.10 Generator Expressions|Wyrażenia generatorowe|
|*poza dokumentacją*|Właściwości · Metody klasy i statyczne · Klasy abstrakcyjne · Protokoły · Typy generyczne · Wszystko razem|

---

## 🧱 Czym właściwie jest klasa?

> Klasa to projekt, a obiekt to dom zbudowany według tego projektu — razem łączą dane z zachowaniem.

---

### 📐 Projekt i domy

Wyobraź sobie architekta, który rysuje **projekt domu**. Na papierze jest wszystko: liczba pokoi, miejsce na drzwi, instalacja elektryczna. Nie da się jednak w tym projekcie zamieszkać. Dopiero gdy ekipa budowlana postawi według niego dom przy ul. Lipowej 7, a potem drugi przy ul. Dębowej 3, powstają prawdziwe budynki. Każdy z nich ma własny adres, własny kolor elewacji i własnych mieszkańców, ale wszystkie zbudowano według **tego samego projektu**.

W programowaniu obiektowym (*object-oriented programming*, OOP) jest dokładnie tak samo:

```
                      klasa Dom (projekt)
                               │
          ┌────── budowa ──────┼────── budowa ──────┐
          ▼                    ▼                    ▼
    ul. Lipowa 7         ul. Dębowa 3         ul. Klonowa 12
        biały               zielony               szary
    └──────────────── obiekty (instancje) ─────────────────┘
```

- **Klasa** (*class*) to projekt. Opisuje, jakie **dane** będzie przechowywał każdy obiekt (adres, kolor) i co będzie potrafił **robić** (otworzyć bramę, przywitać gościa).
- **Obiekt**, inaczej **instancja** (*instance*), to konkretny egzemplarz zbudowany według klasy.

Klasa łączy więc w jedną całość **dane** i **zachowanie**. Utworzenie klasy tworzy nowy **typ** obiektu — tak jak `int`, `str` czy `list` to typy wbudowane w Pythona.

---

### 👀 Pierwszy rzut oka na kod

```python
class Dom:
    def __init__(self, adres):
        self.adres = adres

    def przywitaj(self):
        return f"Witaj w domu przy {self.adres}!"


lipowa = Dom("ul. Lipowa 7")
debowa = Dom("ul. Dębowa 3")

print(lipowa.przywitaj())
print(debowa.przywitaj())
```

```
Witaj w domu przy ul. Lipowa 7!
Witaj w domu przy ul. Dębowa 3!
```

Na razie nie przejmuj się szczegółami — każdy element tego kodu omówimy w sekcji „Pierwsza klasa: `Dom`”. Już teraz widać jednak najważniejsze: jedna klasa, dwa niezależne obiekty, każdy z własnym adresem.

---

### 📖 Słowniczek na start

|Pojęcie|Po angielsku|W naszym domu|
|---|---|---|
|klasa|*class*|projekt domu|
|obiekt, instancja|*object, instance*|konkretny dom przy konkretnej ulicy|
|atrybut (dana)|*attribute, data attribute*|adres, kolor elewacji, lista pokoi|
|metoda|*method*|czynność, którą dom potrafi wykonać, np. `przywitaj()`|
|`self`|—|„ten konkretny dom, o który właśnie chodzi”|
|`__init__`|*initializer*|ekipa wykańczająca nowo postawiony dom|

---

### 🐍 Co wyróżnia klasy w Pythonie

Mechanizm klas w Pythonie łączy pomysły z języków C++ i Modula-3, ale ma kilka cech, które warto znać od początku:

- **Wszystko jest publiczne.** Python nie ma słów kluczowych `private` ani `protected` — prywatność opiera się na umowie między programistami (szczegóły w sekcji o zmiennych prywatnych).
- **Wszystkie metody są „wirtualne”.** Klasa pochodna może nadpisać dowolną metodę klasy bazowej (sekcja o dziedziczeniu).
- **Klasy same są obiektami.** Tworzy się je w trakcie działania programu i można je później modyfikować.
- **Typy wbudowane mogą być klasami bazowymi.** Możesz napisać klasę dziedziczącą po `list` czy `dict`.
- **Dziedziczenie wielokrotne** jest dozwolone: klasa może mieć kilku „rodziców” (sekcja o dziedziczeniu wielokrotnym).

> 💡 W Pythonie **wszystko jest obiektem**: liczba, napis, funkcja, moduł, a nawet sama klasa. Każdy obiekt zna swoją klasę:
>
> ```python
> >>> type(42)
> <class 'int'>
> >>> "salon".__class__
> <class 'str'>
> ```

---

## 🔑 Nazwy i obiekty

> Nazwa to klucz, a obiekt to dom — przypisanie `b = a` dorabia drugi klucz, a nie buduje drugiego domu.

---

### 📌 Nazwa to klucz, obiekt to dom

W wielu językach zmienną wyobrażamy sobie jako pudełko z wartością w środku. W Pythonie lepiej pasuje inny obraz: **nazwa to klucz, a obiekt to dom**. Przypisanie `b = a` nie buduje drugiego domu, tylko **dorabia drugi klucz** do tego samego budynku.

Obiekty mają swoją tożsamość, a do jednego obiektu może prowadzić wiele nazw (nawet z różnych zasięgów). To zjawisko nazywamy **aliasowaniem** (*aliasing*).

```python
pokoje = ["salon", "kuchnia"]
plan_architekta = pokoje          # drugi klucz do TEJ SAMEJ listy

plan_architekta.append("garaż")   # architekt dobudowuje garaż…

print(pokoje)                     # …i widzi to każdy właściciel klucza
print(pokoje is plan_architekta)
```

```
['salon', 'kuchnia', 'garaż']
True
```

```
  pokoje ──────────┐
                   ▼
            ┌───────────────────────────────┐
            │ ['salon', 'kuchnia', 'garaż'] │   ← jeden obiekt (jedna lista)
            └───────────────────────────────┘
                   ▲
  plan_architekta ─┘
```

---

### ⚖️ Kiedy aliasowanie ma znaczenie?

Przy obiektach **niezmiennych** (*immutable*) — liczbach, napisach, krotkach — aliasy są niegroźne, bo takiego obiektu i tak nie da się zmienić. Można jedynie przełożyć klucz na inny obiekt:

```python
kolor = "biały"
kolor_sasiada = kolor        # dwa klucze do tego samego napisu
kolor_sasiada = "żółty"      # przekładamy klucz sąsiada na NOWY napis

print(kolor, kolor_sasiada)
```

```
biały żółty
```

Przy obiektach **zmiennych** (*mutable*) — listach, słownikach, większości obiektów własnych klas — aliasy mają ogromne znaczenie. Zmiana wykonana „przez jeden klucz” jest widoczna „przez wszystkie”.

---

### 📨 Aliasowanie przy wywoływaniu funkcji

Ta sama zasada działa przy przekazywaniu argumentów. Funkcja nie dostaje kopii domu, tylko **kolejny klucz** do niego:

```python
def dobuduj_taras(lista_pomieszczen):
    lista_pomieszczen.append("taras")


moje_pokoje = ["salon", "kuchnia"]
dobuduj_taras(moje_pokoje)
print(moje_pokoje)
```

```
['salon', 'kuchnia', 'taras']
```

To jednocześnie zaleta i ryzyko. **Zaleta:** przekazanie nawet ogromnego obiektu jest tanie, bo kopiujemy tylko „klucz” (referencję). **Ryzyko:** funkcja może zmienić obiekt, a wywołujący zobaczy tę zmianę.

> 💡 Gdy potrzebujesz **niezależnej kopii**, zrób ją jawnie: `pokoje.copy()`, `list(pokoje)` albo — dla struktur zagnieżdżonych — `copy.deepcopy(pokoje)`.

> 💡 **`is` czy `==`?** Operator `is` sprawdza, czy dwa klucze otwierają **ten sam dom** (tożsamość). Operator `==` sprawdza, czy dwa domy **wyglądają tak samo** (równość wartości).
>
> ```python
> >>> a = ["salon"]
> >>> b = ["salon"]
> >>> a == b, a is b
> (True, False)
> ```

---

## 🗂️ Przestrzenie nazw i zasięgi

> Gdzie Python szuka nazw — przestrzenie nazw jako wieszaki na klucze, reguła LEGB oraz `global` i `nonlocal`.

---

### 📌 Przestrzeń nazw: wieszak na klucze

Ten temat może wydawać się oderwany od klas, ale bez niego trudno zrozumieć, jak klasy działają w środku. Zostańmy przy kluczach.

**Przestrzeń nazw** (*namespace*) to odwzorowanie **nazw na obiekty**. Wyobraź ją sobie jako **wieszak na klucze**: każdy haczyk ma etykietę (nazwę), a wiszący na nim klucz prowadzi do obiektu. Większość przestrzeni nazw jest w Pythonie zwykłymi słownikami.

Przykłady przestrzeni nazw:

- **wbudowana** (*built-in*): funkcje takie jak `print()`, `len()` czy `abs()` oraz wbudowane wyjątki;
- **globalna modułu**: nazwy zdefiniowane na najwyższym poziomie pliku;
- **lokalna funkcji**: nazwy utworzone podczas wywołania funkcji;
- **atrybuty obiektu**: tak, zbiór atrybutów obiektu też jest przestrzenią nazw.

Najważniejsza cecha: **różne przestrzenie nazw nie mają ze sobą nic wspólnego**. Na dwóch różnych wieszakach może wisieć klucz z etykietą `pilot`, a każdy otwiera coś innego. Dwa moduły mogą bez konfliktu zdefiniować funkcję o tej samej nazwie, bo użytkownik i tak musi poprzedzić ją nazwą modułu.

> 💡 **Atrybut** to każda nazwa występująca po kropce. W wyrażeniu `dom.adres` nazwa `adres` jest atrybutem obiektu `dom`, a w `math.pi` nazwa `pi` jest atrybutem modułu `math`. Atrybuty mogą być tylko do odczytu albo zapisywalne. Zapisywalne można też usunąć: `del dom.adres`.

---

### ⏳ Kiedy wieszaki powstają i znikają

|Przestrzeń nazw|Powstaje|Znika|
|---|---|---|
|wbudowana (moduł `builtins`)|przy starcie interpretera|nigdy (żyje do końca programu)|
|globalna modułu|przy wczytaniu modułu|zwykle dopiero przy zamknięciu interpretera|
|lokalna funkcji|przy **wywołaniu** funkcji|gdy funkcja zwróci wynik lub zgłosi nieobsłużony wyjątek|

Instrukcje wykonywane na najwyższym poziomie — czy to ze skryptu, czy wpisywane w konsoli — należą do modułu o nazwie `__main__`, więc mają własną przestrzeń globalną.

---

### 🔭 Zasięg i reguła LEGB

**Zasięg** (*scope*) to obszar kodu, z którego daną przestrzeń nazw widać **bezpośrednio**, czyli bez pisania kropki. Gdy Python napotyka nazwę, przeszukuje zasięgi w ściśle określonej kolejności, od najbliższego. Ta kolejność to słynna reguła **LEGB**.

Wyobraź sobie, że szukasz pilota do telewizora:

```
L  Local       w tym pokoju          (bieżąca funkcja)
│  nie ma?
▼
E  Enclosing   w całym mieszkaniu    (funkcje otaczające)
│  nie ma?
▼
G  Global      w całym budynku       (moduł)
│  nie ma?
▼
B  Built-in    w mieście             (wbudowane)
│  nie ma?
▼
NameError ❌
```

```python
pilot = "pilot z holu budynku"            # G – zasięg globalny


def mieszkanie():
    pilot = "pilot z przedpokoju"         # E – zasięg otaczający

    def salon():
        print(pilot)                      # w salonie (L) pilota nie ma → szukamy wyżej

    salon()


mieszkanie()
print(len("salon"))                       # len pochodzi z zasięgu wbudowanego (B)
```

```
pilot z przedpokoju
5
```

---

### ✍️ Przypisanie zawsze działa „u siebie”

**Odczyt** nazwy przeszukuje zasięgi według LEGB. Z **przypisaniem** jest inaczej: jeśli nie użyjesz `global` ani `nonlocal`, przypisanie **zawsze tworzy lub zmienia nazwę w najbardziej wewnętrznym zasięgu**. Przypisanie nie kopiuje przy tym żadnych danych, tylko wiesza klucz na haczyku. Tak samo działają `import` i `def`: wiążą nazwę w zasięgu lokalnym.

Do zmiany tej reguły służą dwa słowa kluczowe:

|Instrukcja|Co robi|
|---|---|
|`global nazwa`|„wieszaj i szukaj tego klucza na wieszaku **modułu**”|
|`nonlocal nazwa`|„wieszaj i szukaj tego klucza na wieszaku **funkcji otaczającej**”|

---

### 🎨 Przykład: remont w trzech wersjach

Poniższy przykład to dokładny odpowiednik przykładu z dokumentacji. Sprawdzamy, który „kolor ścian” zmieni się po każdym z trzech rodzajów przypisania:

```python
def remont():
    def maluj_lokalnie():
        kolor = "lokalny błękit"

    def maluj_nielokalnie():
        nonlocal kolor
        kolor = "nielokalna zieleń"

    def maluj_globalnie():
        global kolor
        kolor = "globalna biel"

    kolor = "testowy beż"
    maluj_lokalnie()
    print("Po przypisaniu lokalnym:   ", kolor)
    maluj_nielokalnie()
    print("Po przypisaniu nielokalnym:", kolor)
    maluj_globalnie()
    print("Po przypisaniu globalnym:  ", kolor)


remont()
print("W zasięgu globalnym:       ", kolor)
```

```
Po przypisaniu lokalnym:    testowy beż
Po przypisaniu nielokalnym: nielokalna zieleń
Po przypisaniu globalnym:   nielokalna zieleń
W zasięgu globalnym:        globalna biel
```

Co się stało?

|Krok|Wyjaśnienie|
|---|---|
|`maluj_lokalnie()`|Utworzyła **własną**, lokalną zmienną `kolor`, która zniknęła po zakończeniu funkcji. Kolor w `remont()` się nie zmienił.|
|`maluj_nielokalnie()`|Dzięki `nonlocal` zmieniła zmienną `kolor` **funkcji otaczającej**, czyli `remont()`.|
|`maluj_globalnie()`|Dzięki `global` utworzyła zmienną `kolor` **na poziomie modułu**. Zmienna w `remont()` pozostała „nielokalną zielenią”.|
|ostatni `print`|Poza funkcją widać tylko kolor globalny, czyli „globalną biel”.|

---

### ⚠️ Zasięgi ustala się statycznie, a używa dynamicznie

Python decyduje o tym, czy nazwa jest lokalna, **czytając kod funkcji przed jej uruchomieniem**. Jeżeli gdziekolwiek w funkcji jest przypisanie do danej nazwy, ta nazwa jest lokalna w **całej** funkcji. Stąd bierze się klasyczna pułapka:

```python
>>> licznik_gosci = 0
>>> def wpusc_goscia():
...     licznik_gosci += 1      # przypisanie → nazwa lokalna w całej funkcji
...
>>> wpusc_goscia()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    wpusc_goscia()
    ~~~~~~~~~~~~^^
  File "<stdin>", line 2, in wpusc_goscia
    licznik_gosci += 1      # przypisanie → nazwa lokalna w całej funkcji
    ^^^^^^^^^^^^^
UnboundLocalError: cannot access local variable 'licznik_gosci' where it is not associated with a value
```

Funkcja próbuje odczytać lokalne `licznik_gosci`, zanim cokolwiek do niego przypisano. Rozwiązaniem byłoby `global licznik_gosci`, ale jeszcze lepiej trzymać taki stan w obiekcie. Właśnie do tego służą klasy.

> 💡 Używaj `global` oszczędnie. Kod, który zmienia zmienne globalne z wnętrza funkcji, trudno czytać i testować. Klasy rozwiązują ten problem elegancko: stan trzymamy w atrybutach obiektu.

> 💡 **Dlaczego to ważne dla klas?** Ciało klasy dostaje własną przestrzeń nazw, ale **nie tworzy zasięgu widocznego z metod**. Metoda nie „widzi” bezpośrednio nazw zdefiniowanych w klasie i musi sięgać po nie przez `self.` lub nazwę klasy. Wrócimy do tego w sekcji „Kilka uwag różnych”.

---

## 🏠 Pierwsza klasa: `Dom`

> Składnia definicji klasy, obiekt klasy, `__init__` i `self`, obiekty instancji i obiekty metod.

---

### 📌 Składnia definicji klasy

Najprostsza definicja klasy wygląda tak:

```python
class NazwaKlasy:
    <instrukcja-1>
    .
    .
    .
    <instrukcja-N>
```

Definicja klasy, podobnie jak definicja funkcji (`def`), **jest zwykłą instrukcją**: klasa zaczyna istnieć dopiero wtedy, gdy Python wykona tę instrukcję. Możesz ją nawet umieścić wewnątrz `if` albo funkcji.

Co dzieje się w trakcie wykonywania definicji klasy?

1. Python tworzy **nową przestrzeń nazw** (nowy wieszak) i wykonuje w niej ciało klasy.
2. Każde przypisanie i każde `def` w ciele klasy wiesza nazwę właśnie na tym wieszaku.
3. Na końcu powstaje **obiekt klasy** (*class object*), który opakowuje ten wieszak, a nazwa `NazwaKlasy` zostaje z nim powiązana.

Że ciało klasy naprawdę się *wykonuje*, łatwo sprawdzić:

```python
class Dom:
    print("Czytam projekt domu…")
```

```
Czytam projekt domu…
```

Napis pojawił się, choć nie utworzyliśmy ani jednego domu — Python po prostu przeczytał projekt.

---

### 📐 Obiekt klasy

Obiekt klasy to projekt, który można czytać i według którego można budować. Obsługuje dwie operacje: **odwołania do atrybutów** i **tworzenie instancji**.

```python
class Dom:
    """Projekt domu na osiedlu Słoneczne Wzgórze."""

    osiedle = "Słoneczne Wzgórze"

    def przywitaj(self):
        return "Witaj w domu!"
```

**Odwołania do atrybutów** mają standardową składnię `obiekt.nazwa`. Dostępne są wszystkie nazwy, które znalazły się w przestrzeni nazw klasy:

```python
>>> Dom.osiedle
'Słoneczne Wzgórze'
>>> Dom.przywitaj
<function Dom.przywitaj at 0x...>
>>> Dom.__doc__
'Projekt domu na osiedlu Słoneczne Wzgórze.'
```

`__doc__` zwraca **docstring**, czyli napis dokumentujący umieszczony zaraz pod nagłówkiem klasy. Atrybuty klasy można też zmieniać: `Dom.osiedle = "Nowe Osiedle"`.

**Tworzenie instancji** wygląda jak wywołanie funkcji: klasę „wywołujemy”, a ona zwraca nowy obiekt.

```python
>>> moj_dom = Dom()          # budujemy dom według projektu
>>> moj_dom.przywitaj()
'Witaj w domu!'
```

---

### 🧰 `__init__`: ekipa wykańczająca

Taki dom jest jednak pusty: nie ma adresu ani koloru. Chcemy, żeby każdy nowy dom od razu dostawał swoje dane. Służy do tego specjalna metoda `__init__()`. Python wywołuje ją **automatycznie** zaraz po utworzeniu obiektu, a argumenty podane przy tworzeniu instancji trafiają właśnie do niej:

```python
class Dom:
    """Projekt domu na osiedlu Słoneczne Wzgórze."""

    osiedle = "Słoneczne Wzgórze"

    def __init__(self, adres, kolor_elewacji):
        self.adres = adres
        self.kolor_elewacji = kolor_elewacji

    def przywitaj(self):
        return f"Witaj w domu przy {self.adres}!"
```

```python
>>> lipowa = Dom("ul. Lipowa 7", "biały")
>>> lipowa.adres, lipowa.kolor_elewacji
('ul. Lipowa 7', 'biały')
```

> 💡 **Czym jest `self`?** To pierwszy parametr każdej zwykłej metody, czyli **ten konkretny obiekt, na rzecz którego metoda działa**. Gdy piszesz `Dom("ul. Lipowa 7", "biały")`, Python tworzy pusty dom i wywołuje `__init__(nowy_dom, "ul. Lipowa 7", "biały")`. Wewnątrz metody `self` to właśnie ten nowy dom, a `self.adres = adres` oznacza: „zapisz adres **w tym domu**”. Samego `self` nigdy nie przekazujesz ręcznie — robi to za Ciebie Python.

> 💡 `__init__` często nazywa się „konstruktorem”, ale precyzyjnie jest to **inicjalizator**. Sam obiekt powstaje wcześniej (w metodzie `__new__`), a `__init__` dostaje go już gotowego i tylko „wykańcza”, czyli ustawia początkowy stan. Stąd nasza analogia z ekipą wykańczającą.

---

### 🏘️ Obiekty instancji

Co można zrobić z gotowym domem? Instancja rozumie tylko odwołania do atrybutów, a te są dwojakiego rodzaju: **atrybuty danych** i **metody**.

**Atrybuty danych** (w innych językach: pola, zmienne instancji) nie wymagają żadnej deklaracji. Tak jak zmienne lokalne, **pojawiają się w chwili pierwszego przypisania** — nawet spoza klasy:

```python
>>> lipowa.goscie = 1                 # atrybut powstaje w tej chwili
>>> while lipowa.goscie < 10:
...     lipowa.goscie = lipowa.goscie * 2
...
>>> lipowa.goscie
16
>>> del lipowa.goscie                 # i znika bez śladu
```

> ⚠️ To, że *można* dopisywać atrybuty z zewnątrz, nie znaczy, że *należy*. Gdy każdy dom ma inny zestaw atrybutów, łatwo o błędy. Dobra praktyka: **wszystkie atrybuty instancji twórz w `__init__`**, nawet jeśli na początku mają wartość `None` albo są pustą listą.

**Metody** to funkcje „należące” do obiektu. Nazwy metod instancji wynikają z jej klasy: każdy atrybut klasy, który jest funkcją, daje odpowiednią metodę instancji. Dlatego `lipowa.przywitaj` jest metodą, bo `Dom.przywitaj` jest funkcją, a `lipowa.osiedle` metodą nie jest, bo `Dom.osiedle` to napis.

---

### 🔔 Obiekty metod: dzwonek przymocowany do drzwi

Zwykle metodę wywołujemy od razu:

```python
>>> lipowa.przywitaj()
'Witaj w domu przy ul. Lipowa 7!'
```

Ale `lipowa.przywitaj` (bez nawiasów) to pełnoprawny **obiekt metody**, który można zapisać i wywołać później. Przypomina to **dzwonek przymocowany do drzwi konkretnego domu**: gdziekolwiek go zabierzesz, zawsze dzwoni w tym jednym domu.

```python
>>> dzwonek = lipowa.przywitaj      # zdejmujemy „dzwonek” z drzwi Lipowej 7
>>> dzwonek()
'Witaj w domu przy ul. Lipowa 7!'
```

Zauważ, że `przywitaj` zdefiniowano z parametrem `self`, a wywołujemy ją bez argumentów. Gdzie podział się `self`? Na tym polega cała magia metod: **instancja jest automatycznie przekazywana jako pierwszy argument**. Wywołanie `lipowa.przywitaj()` jest dokładnie równoważne wywołaniu `Dom.przywitaj(lipowa)`:

```python
>>> Dom.przywitaj(lipowa)
'Witaj w domu przy ul. Lipowa 7!'
```

Ogólnie: wywołanie metody z *n* argumentami to wywołanie funkcji z klasy z *n + 1* argumentami, przy czym na początek listy trafia instancja.

---

### 🔬 Jak to działa pod spodem?

Gdy odwołujesz się do atrybutu instancji, który nie jest atrybutem danych:

1. Python szuka nazwy w klasie obiektu.
2. Jeśli znajdzie tam **funkcję**, pakuje ją razem z instancją w **obiekt metody** (to nasz „dzwonek”).
3. Gdy wywołasz obiekt metody, Python tworzy nową listę argumentów — najpierw instancja, potem Twoje argumenty — i z nią wywołuje funkcję.

Obiekt metody pamięta oba składniki:

```python
>>> dzwonek.__self__ is lipowa          # do którego domu przymocowany
True
>>> dzwonek.__func__ is Dom.przywitaj   # jaka funkcja w nim działa
True
```

---

## 🪧 Zmienne klasy i zmienne instancji

> Szyld osiedla jest jeden dla wszystkich domów, a numer domu — własny dla każdego z nich.

---

### 📌 Szyld osiedla i numer domu

Wszystkie domy na osiedlu stoją pod jednym szyldem „Słoneczne Wzgórze”, ale każdy ma własny adres. W klasie wyrażamy to tak:

- **zmienna klasy** (*class variable*) to dana **wspólna dla wszystkich instancji** — jeden szyld dla całego osiedla;
- **zmienna instancji** (*instance variable*) to dana **unikalna dla każdego obiektu** — numer konkretnego domu.

```python
class Dom:
    osiedle = "Słoneczne Wzgórze"     # zmienna klasy – wspólna dla wszystkich domów

    def __init__(self, adres):
        self.adres = adres            # zmienna instancji – własna dla każdego domu
```

```python
>>> lipowa = Dom("ul. Lipowa 7")
>>> debowa = Dom("ul. Dębowa 3")
>>> lipowa.osiedle                    # wspólne dla wszystkich domów
'Słoneczne Wzgórze'
>>> debowa.osiedle                    # wspólne dla wszystkich domów
'Słoneczne Wzgórze'
>>> lipowa.adres                      # unikalne dla lipowej
'ul. Lipowa 7'
>>> debowa.adres                      # unikalne dla dębowej
'ul. Dębowa 3'
```

Zmiana zmiennej klasy jest widoczna we wszystkich instancjach. Wymieniamy jeden szyld, a widzą to wszyscy:

```python
>>> Dom.osiedle = "Słoneczne Wzgórze II"
>>> lipowa.osiedle, debowa.osiedle
('Słoneczne Wzgórze II', 'Słoneczne Wzgórze II')
```

---

### 🔍 Jak Python szuka atrybutu: najpierw dom, potem projekt

Gdy piszesz `lipowa.osiedle`, Python sprawdza najpierw **atrybuty instancji**, a dopiero gdy nic tam nie znajdzie, sięga do **klasy**. Jeśli więc ta sama nazwa występuje i w instancji, i w klasie, **wygrywa instancja**.

Dzięki temu zmienna klasy świetnie sprawdza się jako **wartość domyślna**: projekt przewiduje grafitowy dach, ale właściciel jednego domu może wybrać inny:

```python
class Dom:
    kolor_dachu = "grafitowy"         # wartość domyślna z projektu

    def __init__(self, adres):
        self.adres = adres
```

```python
>>> lipowa = Dom("ul. Lipowa 7")
>>> debowa = Dom("ul. Dębowa 3")
>>> debowa.kolor_dachu = "czerwony"   # tworzy atrybut INSTANCJI
>>> lipowa.kolor_dachu, debowa.kolor_dachu
('grafitowy', 'czerwony')
>>> vars(lipowa)                      # własne atrybuty lipowej
{'adres': 'ul. Lipowa 7'}
>>> vars(debowa)                      # dębowa ma własny dach, który przesłania projekt
{'adres': 'ul. Dębowa 3', 'kolor_dachu': 'czerwony'}
```

> 💡 Funkcja `vars(obiekt)` (albo atrybut `obiekt.__dict__`) pokazuje przestrzeń nazw instancji, czyli jej „wieszak na klucze”. Widać na nim, że `lipowa` nie ma własnego `kolor_dachu`, więc korzysta z projektu.

---

### ⚠️ Najsłynniejsza pułapka: zmienny obiekt jako zmienna klasy

Przypomnij sobie sekcję „Nazwy i obiekty”: jeden obiekt zmienny, wiele kluczy. Spójrz, co się dzieje, gdy listę domowników umieścimy w klasie:

```python
class Dom:
    domownicy = []                    # ❌ błąd: JEDNA lista dla WSZYSTKICH domów

    def __init__(self, adres):
        self.adres = adres

    def wprowadz(self, imie):
        self.domownicy.append(imie)
```

```python
>>> lipowa = Dom("ul. Lipowa 7")
>>> debowa = Dom("ul. Dębowa 3")
>>> lipowa.wprowadz("Anna")
>>> debowa.wprowadz("Bartek")
>>> lipowa.domownicy                  # niespodziewanie wspólna dla wszystkich domów!
['Anna', 'Bartek']
```

Bartek wprowadził się do dwóch domów jednocześnie. Dlaczego? `self.domownicy.append(...)` niczego nie przypisuje, tylko **modyfikuje** listę znalezioną w klasie, a ta lista jest jedna dla wszystkich.

**Poprawnie:** każdy dom dostaje własną listę w `__init__`:

```python
class Dom:
    def __init__(self, adres):
        self.adres = adres
        self.domownicy = []           # ✅ nowa, pusta lista dla każdego domu

    def wprowadz(self, imie):
        self.domownicy.append(imie)
```

```python
>>> lipowa = Dom("ul. Lipowa 7")
>>> debowa = Dom("ul. Dębowa 3")
>>> lipowa.wprowadz("Anna")
>>> debowa.wprowadz("Bartek")
>>> lipowa.domownicy
['Anna']
>>> debowa.domownicy
['Bartek']
```

---

### ⚖️ Podsumowanie

| |Zmienna klasy|Zmienna instancji|
|---|---|---|
|**Gdzie definiujemy**|w ciele klasy, poza metodami|w metodach, zwykle w `__init__`, przez `self.`|
|**Kto ją widzi**|wszystkie instancje (jedna wspólna kopia)|tylko jedna instancja|
|**Typowe zastosowania**|stałe, wartości domyślne, ustawienia wspólne|stan konkretnego obiektu|
|**Analogia**|szyld osiedla|numer i kolor konkretnego domu|
|**Uwaga**|**nigdy** nie trzymaj w niej listy ani słownika, który ma być osobny dla każdego obiektu|—|

---

## 🧩 Kilka uwag różnych

> Garść drobniejszych, ale ważnych obserwacji z dokumentacji — wciąż na przykładzie naszego domu.

---

### 🔓 Nie ma prawdziwego ukrywania danych

Klasy w Pythonie nie potrafią wymusić ukrycia danych — wszystko opiera się na **konwencjach** i wzajemnym zaufaniu. Klient klasy (kod, który jej używa) może więc zepsuć **niezmienniki** (*invariants*), czyli reguły, których pilnują metody. Przykładowo, gdyby `Dom` przechowywał osobno listę pokoi i ich liczbę, ręczna zmiana jednego bez drugiego rozsynchronizowałaby obiekt. Klient może natomiast bezpiecznie dodawać **własne** atrybuty, o ile nie koliduje nazwami z istniejącymi.

---

### ✍️ `self.` trzeba pisać zawsze

Wewnątrz metody nie ma skrótu pozwalającego odwołać się do atrybutu bez `self.`. To celowa decyzja: od razu widać, co jest **zmienną lokalną**, a co **atrybutem obiektu**.

---

### 🏷️ `self` to tylko konwencja

Dla Pythona nazwa pierwszego parametru nie ma znaczenia — mógłbyś napisać `def przywitaj(ten_dom):`. Nie rób tego jednak: inni programiści, edytory i narzędzia oczekują nazwy `self`.

---

### 📞 Metody mogą wołać inne metody

Robią to tak samo jak przy atrybutach, przez `self.`:

```python
class Dom:
    def __init__(self, adres):
        self.adres = adres
        self.domownicy = []

    def wprowadz(self, imie):
        self.domownicy.append(imie)

    def wprowadz_rodzine(self, *imiona):
        for imie in imiona:
            self.wprowadz(imie)       # metoda wywołuje inną metodę
```

```python
>>> lipowa = Dom("ul. Lipowa 7")
>>> lipowa.wprowadz_rodzine("Anna", "Bartek", "Celina")
>>> lipowa.domownicy
['Anna', 'Bartek', 'Celina']
```

---

### 🧷 Metodą może zostać nawet funkcja zdefiniowana poza klasą

Każda funkcja, która jest atrybutem klasy, staje się metodą — nawet jeśli zdefiniowano ją gdzie indziej:

```python
def zadzwon(self):                    # zwykła funkcja poza klasą
    return f"Dzyń-dzyń pod adresem {self.adres}!"


class Dom:
    def __init__(self, adres):
        self.adres = adres

    dzwonek = zadzwon                 # od teraz każdy dom ma metodę dzwonek()
```

```python
>>> Dom("ul. Lipowa 7").dzwonek()
'Dzyń-dzyń pod adresem ul. Lipowa 7!'
```

Działa, ale dokumentacja ostrzega, że taka praktyka zwykle tylko **dezorientuje czytelnika**. Warto o niej wiedzieć, rzadko warto jej używać.

---

### 🌍 Metody widzą zasięg globalny modułu, ale nie zasięg klasy

Tu wraca obiecany wątek z sekcji „Przestrzenie nazw i zasięgi”. Metoda szuka nazw według LEGB, a **ciało klasy nie jest w tym łańcuchu**. Klasa nigdy nie służy za zasięg globalny metody — tę rolę pełni moduł, w którym metodę zdefiniowano. Dlatego poniższy kod nie zadziała:

```python
class Dom:
    osiedle = "Słoneczne Wzgórze"

    def tabliczka(self):
        return f"Osiedle {osiedle}"   # ❌ brak self. – Python szuka w L, E, G, B
```

```python
>>> Dom().tabliczka()
Traceback (most recent call last):
  ...
NameError: name 'osiedle' is not defined. Did you mean: 'self.osiedle'?
```

Poprawnie: `self.osiedle` (albo `Dom.osiedle`).

> 💡 Podpowiedź `Did you mean: 'self.osiedle'?` pojawia się od Pythona 3.12: gdy `NameError` wystąpi w metodzie, a obiekt `self` ma atrybut o tej samej nazwie, Python sam sugeruje poprawkę.

---

### 🪪 Każda wartość zna swoją klasę

Każdy obiekt ma atrybut `__class__`, który wskazuje jego klasę, czyli typ:

```python
>>> lipowa.__class__
<class '__main__.Dom'>
```

---

## ✨ Metody specjalne i `@dataclass`

> Metody z podwójnym podkreśleniem włączają własne klasy w mechanizmy Pythona, a `@dataclass` potrafi napisać je za Ciebie.

---

### 📌 Kiedy dom nie umie się przedstawić

Spróbuj wypisać obiekt naszej klasy:

```python
>>> class Dom:
...     def __init__(self, adres):
...         self.adres = adres
...
>>> print(Dom("ul. Lipowa 7"))
<__main__.Dom object at 0x...>
```

Mało pomocne. Python nie wie, jak przedstawić nasz dom, dopóki mu tego nie powiemy. Służą do tego **metody specjalne**, nazywane też *dunder methods* (od **d**ouble **under**score, czyli podwójnego podkreślenia) albo „metodami magicznymi”. Poznaliśmy już jedną: `__init__`. Python sam wywołuje je w odpowiednich sytuacjach.

|Metoda|Kiedy Python ją wywołuje|Przykład|
|---|---|---|
|`__init__(self, ...)`|przy tworzeniu obiektu|`Dom("ul. Lipowa 7")`|
|`__repr__(self)`|gdy potrzebny jest opis techniczny (konsola, debugowanie)|`repr(dom)`, `dom` w REPL|
|`__str__(self)`|gdy potrzebny jest opis „dla ludzi”|`print(dom)`, `str(dom)`|
|`__len__(self)`|przy pytaniu o długość|`len(dom)`|
|`__eq__(self, inny)`|przy porównaniu|`dom1 == dom2`|
|`__iter__(self)`|gdy obiekt ma być iterowany|`for pokoj in dom` (sekcja „Iteratory”)|

---

### 🗣️ Dom, który umie się przedstawić

Nauczmy nasz dom przedstawiać się, podawać liczbę pokoi i porównywać z innymi domami:

```python
class Dom:
    def __init__(self, adres):
        self.adres = adres
        self.pokoje = []

    def dodaj_pokoj(self, nazwa):
        self.pokoje.append(nazwa)

    def __repr__(self):
        return f"Dom({self.adres!r})"

    def __str__(self):
        return f"🏠 Dom przy {self.adres} (pokoje: {len(self)})"

    def __len__(self):
        return len(self.pokoje)

    def __eq__(self, inny):
        if not isinstance(inny, Dom):
            return NotImplemented
        return self.adres == inny.adres
```

```python
>>> lipowa = Dom("ul. Lipowa 7")
>>> lipowa.dodaj_pokoj("salon")
>>> lipowa.dodaj_pokoj("kuchnia")
>>> lipowa                            # __repr__
Dom('ul. Lipowa 7')
>>> print(lipowa)                     # __str__
🏠 Dom przy ul. Lipowa 7 (pokoje: 2)
>>> len(lipowa)                       # __len__
2
```

> 💡 **Zawsze pisz `__repr__`.** To najtańsza inwestycja w wygodę debugowania. Dobry `__repr__` wygląda jak kod, którym można odtworzyć obiekt: `Dom('ul. Lipowa 7')`.

> 💡 Istnieje też metoda `__del__`, wywoływana, gdy obiekt ma zostać usunięty z pamięci (tzw. destruktor). Python sam zarządza pamięcią (*garbage collection*), więc `__del__` jest potrzebny bardzo rzadko. Do zamykania plików czy połączeń sieciowych używaj instrukcji `with`.

---

### ⚖️ Równość a tożsamość

Domyślnie operator `==` dla obiektów własnych klas zachowuje się jak `is`: dwa obiekty są „równe” tylko wtedy, gdy są **tym samym obiektem w pamięci**. Często chcemy jednak porównywać **zawartość**. Do tego służy `__eq__`. W naszej klasie dwa domy są równe, jeśli mają ten sam adres:

```python
>>> Dom("ul. Lipowa 7") == Dom("ul. Lipowa 7")     # ten sam adres → równe
True
>>> Dom("ul. Lipowa 7") is Dom("ul. Lipowa 7")     # ale to dwa różne obiekty
False
```

> 💡 Zwrócenie `NotImplemented` (a nie `False`), gdy porównujemy dom z czymś zupełnie innym, to sygnał dla Pythona: „nie umiem tego porównać, zapytaj drugi obiekt”. To standardowy, uprzejmy wzorzec.

> ⚠️ **`__eq__` wyłącza hashowanie.** Gdy klasa definiuje `__eq__`, ale nie definiuje `__hash__`, Python ustawia `__hash__ = None`. Takich obiektów nie da się użyć jako kluczy słownika ani elementów zbioru:
>
> ```python
> >>> {lipowa}
> Traceback (most recent call last):
>   File "<stdin>", line 1, in <module>
>     {lipowa}
> TypeError: cannot use 'Dom' as a set element (unhashable type: 'Dom')
> ```
>
> Jeśli potrzebujesz hashowalnych obiektów, dopisz `__hash__` spójny z `__eq__` — równe obiekty muszą mieć równe hashe — np. `return hash(self.adres)`.

---

### 🤖 `@dataclass`: niech Python napisze to za Ciebie

Czasem potrzebujemy klasy, która po prostu **grupuje kilka nazwanych danych** — podobnie jak *record* w Pascalu albo *struct* w C. Taki jest właśnie **pokój**: ma nazwę, metraż i piętro. Pisanie dla niego ręcznie `__init__`, `__repr__` i `__eq__` byłoby nudne i powtarzalne. Idiomatyczne rozwiązanie to moduł `dataclasses`:

```python
from dataclasses import dataclass


@dataclass
class Pokoj:
    nazwa: str
    metraz: float
    pietro: int = 0                   # wartość domyślna
```

Na podstawie samych adnotacji typów dekorator `@dataclass` wygenerował `__init__`, `__repr__` i `__eq__`:

```python
>>> salon = Pokoj("salon", 32.5)
>>> salon
Pokoj(nazwa='salon', metraz=32.5, pietro=0)
>>> salon.metraz
32.5
>>> salon == Pokoj("salon", 32.5)
True
```

> 💡 Używaj `@dataclass`, gdy klasa służy głównie **przechowywaniu danych**. Gdy dominuje **zachowanie** (wiele metod, logika, pilnowanie niezmienników), pisz zwykłą klasę. Nic nie stoi na przeszkodzie, by je łączyć: dom pełen logiki może przechowywać listę prostych pokoi-dataclass.

> ⚠️ Skoro `@dataclass` generuje `__eq__`, to — tak jak w ręcznie pisanej klasie — ustawia też `__hash__ = None`. Hashowalną dataclass uzyskasz przez `@dataclass(frozen=True)`; jej obiekty stają się wtedy niezmienne.

---

## 🧬 Dziedziczenie

> Wspólny kod trafia do klasy bazowej, a klasy pochodne dziedziczą go, nadpisują, rozszerzają albo uzupełniają.

---

### 📌 Wspólna podstawa, różne szczegóły

Dom stoi. Czas zrobić z niego **inteligentny dom**, czyli wyposażyć go w lampy, głośniki, termostaty i rolety sterowane z aplikacji. Wszystkie te urządzenia mają wiele wspólnego, ale każde jest trochę inne — idealne zadanie dla dziedziczenia.

Każde urządzenie w naszym domu ma **nazwę**, stoi w jakimś **pokoju** i można je **włączyć i wyłączyć**. Lampa dodatkowo ma jasność, a głośnik potrafi grać muzykę. Zamiast kopiować wspólny kod do każdej klasy, tworzymy **klasę bazową** (*base class*, „rodzic”) i **klasy pochodne** (*derived classes*, „dzieci”), które ją **dziedziczą** (*inherit*):

```
Urzadzenie          ← nazwa, pokoj, wlaczone · wlacz(), wylacz(), przelacz(), opis()
├── Lampa           ← + jasnosc · nadpisuje wlacz(), rozszerza opis()
└── Glosnik         ← + glosnosc · dodaje zagraj()
```

Składnia jest prosta: klasę bazową podajemy w nawiasie.

```python
class NazwaKlasyPochodnej(NazwaKlasyBazowej):
    ...
```

Zamiast prostej nazwy może tam stać dowolne wyrażenie, np. klasa z innego modułu: `class Lampa(urzadzenia.Urzadzenie):`.

---

### 🔌 Nasza rodzina urządzeń

```python
class Urzadzenie:
    """Dowolne urządzenie inteligentnego domu."""

    def __init__(self, nazwa, pokoj):
        self.nazwa = nazwa
        self.pokoj = pokoj
        self.wlaczone = False

    def wlacz(self):
        self.wlaczone = True

    def wylacz(self):
        self.wlaczone = False

    def przelacz(self):
        if self.wlaczone:
            self.wylacz()
        else:
            self.wlacz()

    def opis(self):
        stan = "wł." if self.wlaczone else "wył."
        return f"{self.nazwa} [{self.pokoj}] – {stan}"


class Lampa(Urzadzenie):
    def __init__(self, nazwa, pokoj, jasnosc=100):
        super().__init__(nazwa, pokoj)      # niech rodzic zrobi swoją część
        self.jasnosc = jasnosc              # a my dokładamy swoją

    def wlacz(self):                        # NADPISANIE metody rodzica
        super().wlacz()
        print(f"💡 {self.nazwa} świeci na {self.jasnosc}%")

    def opis(self):                         # ROZSZERZENIE metody rodzica
        return super().opis() + f", jasność {self.jasnosc}%"


class Glosnik(Urzadzenie):
    def __init__(self, nazwa, pokoj, glosnosc=30):
        super().__init__(nazwa, pokoj)
        self.glosnosc = glosnosc

    def zagraj(self, utwor):                # NOWA metoda, której rodzic nie ma
        print(f"🎵 {self.nazwa} gra: {utwor}")
```

Klasa pochodna może postąpić z kodem rodzica na cztery sposoby:

|Co robi dziecko|Przykład|Znaczenie|
|---|---|---|
|**dziedziczy** bez zmian|`Glosnik` nie definiuje `opis()`|używa wersji rodzica|
|**nadpisuje** (*override*)|`Lampa.wlacz()`|podmienia zachowanie rodzica na własne|
|**rozszerza**|`Lampa.opis()` z `super().opis()`|korzysta z wersji rodzica i coś do niej dodaje|
|**dodaje** coś nowego|`Glosnik.zagraj()`|metoda, której rodzic w ogóle nie ma|

---

### 🔍 Jak Python znajduje metodę

Gdy wywołujesz metodę obiektu, Python szuka jej **najpierw w klasie obiektu, potem w klasie bazowej, potem w jej bazowej** i tak dalej, aż do wbudowanej klasy `object`, po której dziedziczą wszystkie klasy. Pierwsza znaleziona wersja wygrywa.

```python
>>> lampa = Lampa("Lampa sufitowa", "salon", jasnosc=80)
>>> lampa.przelacz()
💡 Lampa sufitowa świeci na 80%
>>> lampa.opis()
'Lampa sufitowa [salon] – wł., jasność 80%'
>>> glosnik = Glosnik("Głośnik", "kuchnia")
>>> glosnik.zagraj("Chopin – Nokturn Es-dur")
🎵 Głośnik gra: Chopin – Nokturn Es-dur
>>> glosnik.opis()                          # odziedziczone bez zmian
'Głośnik [kuchnia] – wył.'
```

Prześledźmy `lampa.przelacz()`:

1. Klasa `Lampa` nie ma metody `przelacz` → Python szuka w `Urzadzenie` i tam ją znajduje.
2. `Urzadzenie.przelacz` wywołuje `self.wlacz()`. Kluczowe pytanie: **która** wersja `wlacz`?
3. `self` to lampa, więc wyszukiwanie zaczyna się znów od klasy `Lampa`. Wywołana zostaje **`Lampa.wlacz`**, stąd komunikat 💡.

> 💡 **Wszystkie metody w Pythonie są „wirtualne”** (w terminologii C++). Metoda klasy bazowej, która woła inną metodę przez `self`, może w praktyce wywołać wersję **nadpisaną w klasie pochodnej**. Rodzic nie musi nic wiedzieć o swoich dzieciach, a i tak współpracuje z ich zachowaniem.

---

### 📣 Wywołanie wersji rodzica: `super()` albo nazwa klasy

Dokumentacja opisuje prosty sposób wywołania metody klasy bazowej: `NazwaKlasyBazowej.metoda(self, argumenty)`. W naszym przykładzie `Urzadzenie.opis(self)` dałoby ten sam efekt co `super().opis()`. Działa to jednak tylko wtedy, gdy klasa bazowa jest dostępna w zasięgu globalnym pod tą nazwą.

```python
>>> Urzadzenie.opis(lampa)                  # wywołanie przez nazwę klasy
'Lampa sufitowa [salon] – wł.'
```

> 💡 Na co dzień używaj **`super()`**. Nie wpisujesz na sztywno nazwy rodzica, więc zmiana hierarchii nie wymaga poprawek w kodzie, a przy dziedziczeniu wielokrotnym `super()` działa poprawnie (o tym w następnej sekcji).

---

### 🧪 `isinstance()` i `issubclass()`

Dwie wbudowane funkcje pozwalają zapytać o relacje dziedziczenia:

```python
>>> isinstance(lampa, Lampa), isinstance(lampa, Urzadzenie), isinstance(lampa, Glosnik)
(True, True, False)
>>> issubclass(Lampa, Urzadzenie)
True
>>> issubclass(bool, int), issubclass(float, int)
(True, False)
```

- `isinstance(obiekt, Klasa)` zwraca `True`, jeśli `obiekt.__class__` to `Klasa` **lub klasa z niej wywiedziona**. Lampa *jest* urządzeniem.
- `issubclass(A, B)` zwraca `True`, jeśli `A` dziedziczy po `B`. `bool` dziedziczy po `int` (dlatego `True + True == 2`), a `float` po `int` nie dziedziczy.

> 💡 **Test „jest” i „ma”.** Dziedziczenie stosuj, gdy możesz uczciwie powiedzieć „*Lampa **jest** urządzeniem*”. Gdy pasuje raczej „*Dom **ma** urządzenia*”, użyj **kompozycji**: obiekt przechowuje inne obiekty w swoich atrybutach (np. `self.urzadzenia = []`). Dom nie powinien dziedziczyć po lampie tylko po to, żeby umieć świecić.

---

## 💎 Dziedziczenie wielokrotne i MRO

> Klasa może mieć kilku rodziców — o kolejności przeszukiwania decyduje MRO, a `super()` oznacza „następny w kolejce”.

---

### 📌 Lampka nocna z głośnikiem

Producent wypuścił **lampkę nocną z wbudowanym głośnikiem**. Jest jednocześnie lampą i głośnikiem. Python pozwala wyrazić to wprost, podając kilka klas bazowych:

```python
class NazwaKlasyPochodnej(Baza1, Baza2, Baza3):
    ...
```

Powstaje słynny **romb** (*diamond*): obie klasy bazowe mają wspólnego przodka.

```
               Urzadzenie
                    ▲
            ┌───────┴───────┐
          Lampa          Glosnik
            ▲               ▲
            └───────┬───────┘
            LampaZGlosnikiem
```

Pojawia się pytanie: w jakiej kolejności Python ma przeszukiwać klasy? I czy `Urzadzenie.__init__` wykona się raz, czy dwa razy? Sprawdźmy na wersji naszych klas, która dodatkowo „melduje się” przy inicjalizacji i wylicza swoje możliwości:

```python
class Urzadzenie:
    def __init__(self, nazwa, pokoj):
        print("→ Urzadzenie.__init__")
        self.nazwa = nazwa
        self.pokoj = pokoj
        self.wlaczone = False

    def mozliwosci(self):
        return ["wł./wył."]


class Lampa(Urzadzenie):
    def __init__(self, nazwa, pokoj, jasnosc=100):
        print("→ Lampa.__init__")
        super().__init__(nazwa, pokoj)
        self.jasnosc = jasnosc

    def mozliwosci(self):
        return super().mozliwosci() + ["światło"]


class Glosnik(Urzadzenie):
    def __init__(self, nazwa, pokoj, glosnosc=30):
        print("→ Glosnik.__init__")
        super().__init__(nazwa, pokoj)
        self.glosnosc = glosnosc

    def mozliwosci(self):
        return super().mozliwosci() + ["dźwięk"]


class LampaZGlosnikiem(Lampa, Glosnik):
    """Lampka nocna z wbudowanym głośnikiem."""
```

```python
>>> nocna = LampaZGlosnikiem("Lampka nocna", "sypialnia")
→ Lampa.__init__
→ Glosnik.__init__
→ Urzadzenie.__init__
>>> nocna.jasnosc, nocna.glosnosc
(100, 30)
>>> nocna.mozliwosci()
['wł./wył.', 'dźwięk', 'światło']
```

Każda inicjalizacja wykonała się **dokładnie raz**, a lampka ma zarówno jasność, jak i głośność. Jak to możliwe?

---

### 🧭 MRO: kolejka, w której Python szuka metod

Każda klasa ma **kolejność rozwiązywania metod** (*Method Resolution Order*, **MRO**). To lista klas, którą Python przegląda po kolei, szukając atrybutu:

```python
>>> [klasa.__name__ for klasa in LampaZGlosnikiem.__mro__]
['LampaZGlosnikiem', 'Lampa', 'Glosnik', 'Urzadzenie', 'object']
```

Dokumentacja podaje regułę uproszczoną: w najprostszych przypadkach przeszukiwanie biegnie **w głąb, od lewej do prawej, bez przeszukiwania tej samej klasy dwa razy** tam, gdzie hierarchie się nakładają. Romb pokazuje, co znaczy ta ostatnia część: wspólny przodek (`Urzadzenie`) nie trafia do kolejki zaraz po `Lampa`, tylko na sam koniec — dopiero gdy przejrzane zostaną wszystkie jego dzieci.

W rzeczywistości Python wyznacza MRO algorytmem **linearyzacji C3**, który gwarantuje, że:

- zachowana jest kolejność od lewej do prawej podana w nawiasie;
- każdy rodzic występuje **tylko raz**, nawet w rombie;
- kolejność jest **monotoniczna**: dziedziczenie po klasie nie „przetasowuje” kolejności jej przodków.

To ma znaczenie, bo romby są w Pythonie wszechobecne: **każda** klasa dziedziczy po `object`, więc każde dziedziczenie wielokrotne tworzy co najmniej jeden romb.

---

### 🔗 `super()` znaczy „następny w kolejce”, a nie „mój rodzic”

To najważniejsza i najbardziej zaskakująca lekcja tej sekcji. Spójrz jeszcze raz na wynik `mozliwosci()`: `['wł./wył.', 'dźwięk', 'światło']`. Skąd w środku wziął się „dźwięk”, skoro `Lampa` dziedziczy wyłącznie po `Urzadzenie`?

Bo `super()` w klasie `Lampa` **nie oznacza „klasa bazowa Lampy”**, tylko **„następna klasa w MRO obiektu, na którym pracujemy”**. Dla obiektu `LampaZGlosnikiem` następnym po `Lampa` jest `Glosnik`:

```
nocna.mozliwosci()
 └─ Lampa.mozliwosci       → super() = Glosnik       (następny w MRO!)
     └─ Glosnik.mozliwosci → super() = Urzadzenie
         └─ Urzadzenie.mozliwosci → ["wł./wył."]
     ← ["wł./wył.", "dźwięk"]
 ← ["wł./wył.", "dźwięk", "światło"]
```

W innych językach z dziedziczeniem wielokrotnym ten mechanizm znany jest jako *call-next-method* („wywołaj następną metodę”). Dzięki niemu klasy mogą **współpracować** (*cooperative multiple inheritance*): każda robi swoją część i przekazuje pałeczkę dalej, a wspólny przodek wykonuje się tylko raz. Klasa `Lampa` nie musi nawet wiedzieć, że istnieje jakiś `Glosnik`.

---

### 🔧 Dla dociekliwych: kooperacyjny `__init__` z `**kwargs`

W powyższym przykładzie nie da się ustawić głośności lampki, bo `Lampa` przekazuje dalej tylko `nazwa` i `pokoj`. W prawdziwych projektach kooperacyjne klasy przyjmują swoje argumenty **jako nazwane**, a resztę przekazują dalej w `**kwargs`:

```python
class Urzadzenie:
    def __init__(self, nazwa, pokoj, **kwargs):
        super().__init__(**kwargs)
        self.nazwa = nazwa
        self.pokoj = pokoj


class Lampa(Urzadzenie):
    def __init__(self, jasnosc=100, **kwargs):
        super().__init__(**kwargs)
        self.jasnosc = jasnosc


class Glosnik(Urzadzenie):
    def __init__(self, glosnosc=30, **kwargs):
        super().__init__(**kwargs)
        self.glosnosc = glosnosc


class LampaZGlosnikiem(Lampa, Glosnik):
    pass
```

```python
>>> nocna = LampaZGlosnikiem(nazwa="Lampka nocna", pokoj="sypialnia", jasnosc=20, glosnosc=10)
>>> nocna.jasnosc, nocna.glosnosc
(20, 10)
```

Każda klasa „wyjmuje” z argumentów swoje, a resztę podaje następnej klasie w MRO.

---

### 🚫 Nie każdy układ jest dozwolony

Jeśli żądana kolejność jest wewnętrznie sprzeczna, Python odmówi utworzenia klasy. Przykład: chcemy, by `Urzadzenie` było sprawdzane *przed* `Lampa`, a jednocześnie `Lampa` dziedziczy po `Urzadzenie`, więc musi być sprawdzana *przed* nim:

```python
>>> class Dziwolag(Urzadzenie, Lampa):
...     pass
...
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    class Dziwolag(Urzadzenie, Lampa):
        pass
TypeError: Cannot create a consistent method resolution order (MRO) for bases Urzadzenie, Lampa
```

> 💡 Dziedziczenie wielokrotne to potężne narzędzie, ale łatwo nim zagmatwać kod. Najbezpieczniej stosować je w formie **domieszek** (*mixins*): małych klas dodających jedną, dobrze określoną umiejętność (np. „potrafi się ściemniać”). W pozostałych przypadkach często lepsza jest kompozycja.

---

## 🔒 Zmienne prywatne i hermetyzacja

> Python nie ma prawdziwie prywatnych pól — ma konwencje: `_nazwa` dla szczegółów wewnętrznych i `__nazwa` z przekształcaniem nazw.

---

### 📌 Hermetyzacja: panel zamiast plątaniny kabli

Każde urządzenie ma w środku elektronikę, ale użytkownik obsługuje je przyciskami na panelu. **Hermetyzacja** (*encapsulation*) to właśnie to: obiekt udostępnia przemyślany **interfejs publiczny** (metody, przyciski), a szczegóły wewnętrzne (adres IP, kod serwisowy, kable) chowa przed światem. Ukrywanie szczegółów nazywa się **ukrywaniem informacji** (*information hiding*). Dzięki niemu:

- nikt przypadkiem nie zepsuje stanu obiektu;
- autor klasy może zmieniać jej wnętrze bez psucia kodu użytkowników.

W Javie czy C++ służą do tego modyfikatory `public`, `protected` i `private`. Python, jak już wiesz, **nie ma prawdziwie prywatnych zmiennych**. Ma za to trzy poziomy konwencji:

|Zapis|Znaczenie|Analogia|
|---|---|---|
|`nazwa`|publiczne: część oficjalnego interfejsu|przycisk na panelu|
|`_nazwa`|wewnętrzne: „nie dotykaj, to szczegół implementacji”|drzwiczki serwisowe z naklejką „tylko dla serwisu”|
|`__nazwa`|*name mangling*: Python zmienia nazwę, by uniknąć kolizji w podklasach|schowek podpisany nazwą producenta, żeby nikt nie pomylił go ze schowkiem innej firmy|

---

### 🚪 Jedno podkreślenie: umowa między programistami

```python
class Urzadzenie:
    def __init__(self, nazwa, pokoj):
        self.nazwa = nazwa
        self.pokoj = pokoj
        self._adres_ip = "192.168.1.20"     # szczegół wewnętrzny
```

```python
>>> lampa = Urzadzenie("Lampa sufitowa", "salon")
>>> lampa._adres_ip                         # da się, ale nie powinno się
'192.168.1.20'
```

Nazwa z wiodącym podkreśleniem to **niepubliczna część API** — może się zmienić w kolejnej wersji bez ostrzeżenia. Python niczego nie blokuje: to drzwi zamknięte na klamkę, a nie na klucz. Takiego atrybutu używa się wewnątrz klasy i jej podklas.

---

### 🔀 Dwa podkreślenia: *name mangling*

Identyfikator postaci `__nazwa` (**co najmniej dwa** podkreślenia na początku i **najwyżej jedno** na końcu) Python w obrębie definicji klasy **tekstowo zamienia** na `_NazwaKlasy__nazwa`. Wiodące podkreślenia samej nazwy klasy są przy tym pomijane. Zjawisko to nazywa się *name mangling*, po polsku „przekształcaniem” albo „zniekształcaniem” nazw.

```python
class Urzadzenie:
    def __init__(self, nazwa):
        self.nazwa = nazwa
        self.__pin_serwisowy = "4321"
```

```python
>>> lampa = Urzadzenie("Lampa sufitowa")
>>> lampa.__pin_serwisowy
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    lampa.__pin_serwisowy
AttributeError: 'Urzadzenie' object has no attribute '__pin_serwisowy'
>>> vars(lampa)                             # zajrzyjmy na „wieszak” obiektu
{'nazwa': 'Lampa sufitowa', '_Urzadzenie__pin_serwisowy': '4321'}
>>> lampa._Urzadzenie__pin_serwisowy        # pod przekształconą nazwą wciąż dostępny
'4321'
```

> 💡 Metody specjalne, takie jak `__init__`, **nie** podlegają przekształceniu, bo mają dwa podkreślenia także na końcu.

---

### 🛡️ Do czego naprawdę służy *name mangling*

Nie służy do ukrywania tajemnic — jak widać, wystarczy znać regułę. Jego prawdziwy cel to **ochrona wewnętrznych wywołań klasy przed przypadkowym nadpisaniem w podklasie**.

Scenariusz: `Urzadzenie` w `__init__` zapisuje ustawienia początkowe metodą `aktualizuj()`. Autor klasy `Glosnik` nadpisuje `aktualizuj()` z **inną sygnaturą** (osobno klucze i wartości). Bez ochrony inicjalizacja rodzica wywoła wersję dziecka i się wysypie:

```python
class UrzadzenieBezOchrony:
    def __init__(self, nazwa, ustawienia):
        self.nazwa = nazwa
        self.ustawienia = {}
        self.aktualizuj(ustawienia)          # woła wersję z KLASY OBIEKTU…

    def aktualizuj(self, ustawienia):
        for klucz, wartosc in ustawienia.items():
            self.ustawienia[klucz] = wartosc


class GlosnikBezOchrony(UrzadzenieBezOchrony):
    def aktualizuj(self, klucze, wartosci):  # …a ta ma inną sygnaturę
        for klucz, wartosc in zip(klucze, wartosci):
            self.ustawienia[klucz] = wartosc
```

```python
>>> GlosnikBezOchrony("Głośnik", {"glosnosc": 30})
Traceback (most recent call last):
  ...
TypeError: GlosnikBezOchrony.aktualizuj() missing 1 required positional argument: 'wartosci'
```

Rozwiązanie z dokumentacji: klasa bazowa zachowuje **prywatną kopię** swojej metody i w `__init__` używa właśnie jej:

```python
class Urzadzenie:
    def __init__(self, nazwa, ustawienia):
        self.nazwa = nazwa
        self.ustawienia = {}
        self.__aktualizuj(ustawienia)        # zawsze wersja z klasy Urzadzenie

    def aktualizuj(self, ustawienia):
        for klucz, wartosc in ustawienia.items():
            self.ustawienia[klucz] = wartosc

    __aktualizuj = aktualizuj                # prywatna kopia oryginalnej metody


class Glosnik(Urzadzenie):
    def aktualizuj(self, klucze, wartosci):
        # nowa sygnatura aktualizuj(), ale __init__() rodzica dalej działa
        for klucz, wartosc in zip(klucze, wartosci):
            self.ustawienia[klucz] = wartosc
```

```python
>>> glosnik = Glosnik("Głośnik", {"glosnosc": 30})
>>> glosnik.ustawienia
{'glosnosc': 30}
>>> glosnik.aktualizuj(["glosnosc", "bas"], [50, 7])
>>> glosnik.ustawienia
{'glosnosc': 50, 'bas': 7}
```

Dlaczego teraz działa? W klasie `Urzadzenie` nazwa `__aktualizuj` zamienia się w `_Urzadzenie__aktualizuj`. Gdyby `Glosnik` zdefiniował własne `__aktualizuj`, stałoby się ono `_Glosnik__aktualizuj`, czyli **zupełnie inną nazwą**. Te dwie metody nie mogą się więc przypadkowo nadpisać.

> ⚠️ Przekształcanie nazw działa **tylko w tekście definicji klasy**. Kod przekazany do `exec()` lub `eval()` nie traktuje klasy wywołującej jako „bieżącej”. To samo dotyczy `getattr()`, `setattr()`, `delattr()` i bezpośredniego dostępu do `__dict__`: tam trzeba podać pełną, przekształconą nazwę.

> 💡 W codziennej pracy wystarcza **jedno podkreślenie**. Po dwa sięgaj tylko wtedy, gdy projektujesz klasę do dziedziczenia i chcesz uchronić jej wewnętrzne mechanizmy przed kolizjami nazw.

---

## 🌡️ Właściwości: `@property`

> Metody, z których korzysta się jak ze zwykłego atrybutu — walidacja i wartości wyliczane bez zmiany interfejsu klasy.

---

### 📌 Historia pewnego termostatu

Pierwsza wersja klasy `Termostat` była prosta: zwykły, publiczny atrybut.

```python
class Termostat:
    def __init__(self, pokoj, temperatura=21.0):
        self.pokoj = pokoj
        self.temperatura = temperatura
```

```python
>>> salon = Termostat("salon")
>>> salon.temperatura = 23.5
>>> salon.temperatura = 95                  # sauna w salonie? Nikt nie protestuje…
>>> salon.temperatura
95
```

Klasa się przyjęła i setki miejsc w kodzie piszą teraz `termostat.temperatura = ...`. Potrzebujemy jednak **walidacji**: temperatura musi mieścić się w zakresie 5–30 °C.

Programista Javy powiedziałby: „trzeba było od początku pisać `get_temperatura()` i `set_temperatura()`”. Zmiana wszystkich wywołań na metody **zepsułaby jednak kod wszystkich użytkowników** klasy. Python ma na to elegantsze rozwiązanie: **właściwość** (*property*). Pozwala zdefiniować metody, z których korzysta się **jak ze zwykłego atrybutu**.

---

### 🔧 Getter, setter i deleter

```python
class Termostat:
    MIN, MAX = 5.0, 30.0

    def __init__(self, pokoj, temperatura=21.0):
        self.pokoj = pokoj
        self.temperatura = temperatura          # ← już tu działa walidacja (setter)!

    @property
    def temperatura(self):
        """Zadana temperatura w °C."""
        return self._temperatura

    @temperatura.setter
    def temperatura(self, wartosc):
        if not self.MIN <= wartosc <= self.MAX:
            raise ValueError(f"Temperatura musi mieścić się w zakresie {self.MIN}–{self.MAX} °C")
        self._temperatura = float(wartosc)

    @temperatura.deleter
    def temperatura(self):
        print("Przywracam ustawienie fabryczne")
        self._temperatura = 21.0

    @property
    def temperatura_f(self):
        """Ta sama temperatura w stopniach Fahrenheita (tylko do odczytu)."""
        return self._temperatura * 9 / 5 + 32
```

Jak to czytać?

- `@property` nad metodą `temperatura` tworzy **getter**: odczyt `t.temperatura` wywołuje tę metodę.
- `@temperatura.setter` tworzy **setter**: przypisanie `t.temperatura = 23` wywołuje metodę z argumentem `23`. Nazwa dekoratora to **nazwa właściwości** + `.setter`, a metoda ma **tę samą nazwę**.
- `@temperatura.deleter` tworzy **deleter**: `del t.temperatura` wywołuje tę metodę (rzadko potrzebny).
- Prawdziwa wartość mieszka w atrybucie `_temperatura` z podkreśleniem, czyli w szczególe wewnętrznym z poprzedniej sekcji.

```python
>>> salon = Termostat("salon")
>>> salon.temperatura                       # getter
21.0
>>> salon.temperatura = 23.5                # setter – składnia bez zmian!
>>> salon.temperatura_f                     # właściwość wyliczana na bieżąco
74.3
>>> salon.temperatura = 95                  # setter odrzuca złą wartość
Traceback (most recent call last):
  ...
ValueError: Temperatura musi mieścić się w zakresie 5.0–30.0 °C
>>> del salon.temperatura                   # deleter
Przywracam ustawienie fabryczne
>>> salon.temperatura
21.0
```

Kod użytkowników klasy nie zmienił się ani o znak: nadal piszą `salon.temperatura = 23.5`, a klasa po cichu pilnuje poprawności.

Walidacja działa nawet w `__init__`, bo przypisanie `self.temperatura = temperatura` też przechodzi przez setter:

```python
>>> Termostat("łazienka", 40)
Traceback (most recent call last):
  ...
ValueError: Temperatura musi mieścić się w zakresie 5.0–30.0 °C
```

---

### 🧮 Właściwości tylko do odczytu i właściwości wyliczane

`temperatura_f` ma tylko getter, więc jest **tylko do odczytu**. Jej wartość jest **wyliczana przy każdym odczycie** z aktualnej temperatury, dzięki czemu nigdy nie rozjedzie się z `temperatura`. Gdybyśmy trzymali obie wartości jako osobne atrybuty, zmiana jednej wymagałaby pamiętania o drugiej.

```python
>>> salon.temperatura_f = 80
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    salon.temperatura_f = 80
    ^^^^^^^^^^^^^^^^^^^
AttributeError: property 'temperatura_f' of 'Termostat' object has no setter
```

> 💡 **Nie pisz na zapas getterów i setterów.** W Pythonie zaczyna się od zwykłego atrybutu. Gdy kiedyś potrzebujesz walidacji albo wyliczania, zamieniasz go na `@property`, a interfejs klasy pozostaje bez zmian.

---

## 🏭 Metody klasy i metody statyczne

> Nie każda metoda potrzebuje konkretnego obiektu — `@classmethod` dostaje całą klasę, a `@staticmethod` nie dostaje nic.

---

### 📌 Trzy rodzaje metod

Dotąd każda metoda dostawała jako pierwszy argument **konkretny obiekt** (`self`). Czasem jednak metoda nie potrzebuje konkretnego termostatu, tylko całej klasy — albo niczego.

|Rodzaj metody|Dekorator|Pierwszy parametr|Do czego ma dostęp|Typowe zastosowanie|
|---|---|---|---|---|
|metoda instancji|*(brak)*|`self`, czyli obiekt|do obiektu i klasy|prawie wszystko|
|metoda klasy|`@classmethod`|`cls`, czyli klasa|do klasy (nie do konkretnego obiektu)|alternatywne konstruktory, fabryki|
|metoda statyczna|`@staticmethod`|*(brak)*|do niczego automatycznie|funkcje pomocnicze związane tematycznie z klasą|

```python
class Termostat:
    TRYB_EKO = 19.0

    def __init__(self, pokoj, temperatura=21.0):
        self.pokoj = pokoj
        self.temperatura = temperatura

    @classmethod
    def ekologiczny(cls, pokoj):
        """Alternatywny konstruktor: termostat od razu w trybie eko."""
        return cls(pokoj, cls.TRYB_EKO)

    @staticmethod
    def na_fahrenheity(stopnie_c):
        """Zwykła funkcja pomocnicza, trzymana w klasie dla porządku."""
        return stopnie_c * 9 / 5 + 32
```

Dla zwięzłości temperatura jest tu zwykłym atrybutem. W prawdziwej klasie połączylibyśmy ten kod z właściwością z poprzedniej sekcji.

```python
>>> sypialnia = Termostat.ekologiczny("sypialnia")     # wywołanie na KLASIE
>>> sypialnia.temperatura
19.0
>>> Termostat.na_fahrenheity(20)                       # nie potrzebujemy żadnego obiektu
68.0
>>> sypialnia.na_fahrenheity(25)                       # z obiektu też można
77.0
```

---

### 🧬 Dlaczego `cls`, a nie po prostu `Termostat`?

Bo metoda klasy **dziedziczy się poprawnie**. Gdy wywołasz ją na klasie pochodnej, `cls` będzie właśnie tą klasą pochodną:

```python
>>> class TermostatLazienkowy(Termostat):
...     TRYB_EKO = 22.0                # w łazience „eko” to trochę cieplej
...
>>> lazienka = TermostatLazienkowy.ekologiczny("łazienka")
>>> type(lazienka).__name__, lazienka.temperatura
('TermostatLazienkowy', 22.0)
```

Gdybyśmy w `ekologiczny` wpisali na sztywno `Termostat(...)`, dostalibyśmy zwykły termostat z temperaturą 19 °C.

> 💡 Metoda **statyczna** to po prostu funkcja, która „mieszka” w klasie, bo tematycznie do niej pasuje. Jeśli nie ma związku z klasą, lepiej zostawić ją jako zwykłą funkcję w module. Z kolei metoda **klasy** to idealne narzędzie do tworzenia obiektów na różne sposoby: `Termostat.ekologiczny(...)`, `Dom.z_pliku(...)` czy `datetime.fromisoformat(...)` z biblioteki standardowej.

---

## 🦆 Polimorfizm i *duck typing*

> Ten sam kod działa z obiektami różnych typów — liczy się to, co obiekt potrafi, a nie po kim dziedziczy.

---

### 📌 Jedno polecenie, wiele form

Mamy dom i mamy urządzenia. Teraz najciekawsze: jak sprawić, żeby **jeden kawałek kodu** — np. scena „Dobranoc” w aplikacji — obsługiwał **dowolne** urządzenie, także takie, którego jeszcze nie wymyślono?

**Polimorfizm** (z gr. „wielopostaciowość”) oznacza, że **ten sam kod działa z obiektami różnych typów**, a każdy z nich reaguje po swojemu. Korzystasz z niego od pierwszego dnia nauki Pythona, nawet o tym nie wiedząc:

```python
>>> len("salon"), len(["salon", "kuchnia"]), len({"salon": 32.5})
(5, 2, 1)
>>> 2 + 3, "ul. Lipowa" + " 7", ["salon"] + ["kuchnia"]
(5, 'ul. Lipowa 7', ['salon', 'kuchnia'])
```

Jedna funkcja `len()` liczy znaki w napisie, elementy listy i klucze słownika. Jeden operator `+` dodaje liczby, skleja napisy i łączy listy. Wyobraź sobie świat, w którym musiałbyś pamiętać o `len_napisu()`, `len_listy()` i `len_slownika()`…

Pamiętasz `__len__` z sekcji o metodach specjalnych? Właśnie dzięki niemu `len()` działa także z naszym domem. **Metody specjalne to sposób na włączenie własnych klas do polimorfizmu wbudowanego w Pythona.**

---

### 🌙 Scena „Dobranoc”

Teraz polimorfizm we własnym kodzie. Każde urządzenie inaczej się wyłącza: lampa gaśnie, głośnik cichnie, rolety się opuszczają. Funkcja sceny nie musi jednak znać tych szczegółów. Wystarczy, że każde urządzenie ma metodę `wylacz()`:

```python
class Urzadzenie:
    def __init__(self, nazwa):
        self.nazwa = nazwa

    def wylacz(self):
        print(f"⏻ {self.nazwa}: wyłączam")


class Lampa(Urzadzenie):
    def wylacz(self):
        print(f"💡 {self.nazwa}: gaszę światło")


class Glosnik(Urzadzenie):
    def wylacz(self):
        print(f"🎵 {self.nazwa}: wyciszam muzykę")


class Rolety(Urzadzenie):
    def wylacz(self):
        print(f"🪟 {self.nazwa}: opuszczam rolety")


def dobranoc(urzadzenia):
    """Scena wieczorna: wyłącza wszystko, cokolwiek to jest."""
    for urzadzenie in urzadzenia:
        urzadzenie.wylacz()


dobranoc([
    Lampa("Lampa sufitowa"),
    Glosnik("Głośnik w kuchni"),
    Rolety("Rolety w sypialni"),
])
```

```
💡 Lampa sufitowa: gaszę światło
🎵 Głośnik w kuchni: wyciszam muzykę
🪟 Rolety w sypialni: opuszczam rolety
```

Funkcja `dobranoc()` ma **jedną** pętlę i **jedno** wywołanie, a obsługuje trzy różne zachowania. Gdy jutro dojdzie klasa `Klimatyzacja`, `dobranoc()` zadziała z nią bez żadnych zmian. To właśnie siła polimorfizmu: kod jest **elastyczny** i **wielokrotnego użytku**.

---

### 🦆 *Duck typing*: jeśli kwacze jak kaczka…

Teraz niespodzianka. Kupiliśmy robota sprzątającego innej firmy. Jego klasa **nie dziedziczy** po naszym `Urzadzenie`, ale też ma metodę `wylacz()`:

```python
class RobotSprzatajacy:                     # obca klasa, bez wspólnego rodzica
    def wylacz(self):
        print("🤖 Robot: wracam do stacji dokującej")


dobranoc([Lampa("Lampa sufitowa"), RobotSprzatajacy()])
```

```
💡 Lampa sufitowa: gaszę światło
🤖 Robot: wracam do stacji dokującej
```

Działa! Python nie sprawdza, **jakiego typu** jest obiekt, tylko czy **ma potrzebną metodę** w chwili, gdy jest ona wywoływana. To tzw. **typowanie kaczkowe** (*duck typing*), od powiedzenia:

> *„Jeśli coś chodzi jak kaczka i kwacze jak kaczka, to jest kaczką.”*

Dokumentacja ujmuje to tak: kodowi, który oczekuje określonego abstrakcyjnego typu danych, często można przekazać **dowolną klasę naśladującą metody tego typu**. Klasyczny przykład: funkcja czytająca dane z pliku przyjmie każdy obiekt z metodami `read()` i `readline()`, nie tylko prawdziwy plik.

Ciemna strona tej swobody: błąd ujawnia się dopiero **w chwili wywołania**. Ktoś dorzucił do sceny doniczkę:

```python
>>> class Doniczka:
...     pass
...
>>> dobranoc([Lampa("Lampa sufitowa"), Doniczka()])
💡 Lampa sufitowa: gaszę światło
Traceback (most recent call last):
  ...
AttributeError: 'Doniczka' object has no attribute 'wylacz'
```

Lampa zgasła, ale scena wywróciła się w połowie — i to dopiero o 23:00, gdy ktoś ją uruchomił. Python nie sprawdza typów z góry, jak kompilator C++ czy Javy: metoda jest wyszukiwana dopiero wtedy, gdy dana linia faktycznie się wykonuje (tzw. **późne wiązanie**, ang. *late binding*).

> 💡 Listę metod i atrybutów obiektu możesz podejrzeć funkcją `dir(obiekt)`, a obecność konkretnej metody sprawdzić przez `hasattr(obiekt, "wylacz")`. To jednak tylko doraźne łatki. Jak **jawnie zapisać kontrakt**, czyli zasadę „urządzenie musi umieć się wyłączyć”? Python daje dwa narzędzia: **klasy abstrakcyjne** i **protokoły**.

---

## 📜 Klasy abstrakcyjne (ABC)

> Klasa abstrakcyjna zapisuje kontrakt w kodzie — Python odmówi utworzenia obiektu, który go nie spełnia.

---

### 📌 Interfejs i klasa abstrakcyjna: norma gniazdka

Pomyśl o **gniazdku elektrycznym**. Norma określa kształt wtyczki, napięcie i częstotliwość, czyli **co** urządzenie musi spełniać, ale nie mówi, **jak** ma działać czajnik czy lampa. Każdy producent realizuje to po swojemu.

- **Interfejs** (*interface*) to taka norma: lista wymaganych operacji (wejść i wyjść) **bez implementacji**.
- **Klasa abstrakcyjna** (*abstract class*) to norma **plus gotowe elementy wspólne**, np. standardowa obudowa i bezpiecznik, z których każdy producent może skorzystać.

Ani normy, ani „urządzenia w ogóle” nie da się kupić w sklepie. Kupuje się konkretny czajnik lub konkretną lampę. Tak samo **klasy abstrakcyjnej nie można zainstancjonować**: potrzebna jest konkretna klasa pochodna, która uzupełni wszystkie braki.

---

### 🧰 Moduł `abc`

Python realizuje oba pomysły za pomocą modułu `abc` (*Abstract Base Classes*). Klasa dziedzicząca po `ABC` może oznaczyć metody dekoratorem `@abstractmethod`, czyli „każda klasa pochodna **musi** to zaimplementować”:

```python
from abc import ABC, abstractmethod


class Urzadzenie(ABC):
    """Część wspólna wszystkich urządzeń + lista obowiązków."""

    def __init__(self, nazwa, pokoj):
        self.nazwa = nazwa
        self.pokoj = pokoj
        self.wlaczone = False

    @abstractmethod
    def wlacz(self):
        """Każde urządzenie MUSI umieć się włączyć – po swojemu."""

    @abstractmethod
    def wylacz(self):
        """…i wyłączyć."""

    def opis(self):                          # metoda konkretna – gotowa dla wszystkich
        stan = "wł." if self.wlaczone else "wył."
        return f"{self.nazwa} [{self.pokoj}] – {stan}"
```

Klasy abstrakcyjnej nie da się zainstancjonować:

```python
>>> Urzadzenie("Coś", "salon")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    Urzadzenie("Coś", "salon")
    ~~~~~~~~~~^^^^^^^^^^^^^^^^
TypeError: Can't instantiate abstract class Urzadzenie without an implementation for abstract methods 'wlacz', 'wylacz'
```

Konkretna klasa, która spełnia wszystkie wymagania, działa normalnie i dostaje w prezencie gotową metodę `opis()`:

```python
class Lampa(Urzadzenie):
    def wlacz(self):
        self.wlaczone = True
        print(f"💡 {self.nazwa}: świecę")

    def wylacz(self):
        self.wlaczone = False
        print(f"💡 {self.nazwa}: gasnę")
```

```python
>>> lampa = Lampa("Lampa sufitowa", "salon")
>>> lampa.wlacz()
💡 Lampa sufitowa: świecę
>>> lampa.opis()
'Lampa sufitowa [salon] – wł.'
```

A teraz kluczowa korzyść. Ktoś napisał klasę `Rolety` i zapomniał o `wylacz()`:

```python
class Rolety(Urzadzenie):
    def wlacz(self):
        self.wlaczone = True
        print(f"🪟 {self.nazwa}: podnoszę rolety")
```

```python
>>> Rolety("Rolety", "sypialnia")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    Rolety("Rolety", "sypialnia")
    ~~~~~~^^^^^^^^^^^^^^^^^^^^^^^
TypeError: Can't instantiate abstract class Rolety without an implementation for abstract method 'wylacz'
```

> 💡 **Kontrakt egzekwowany przez Pythona.** Z klasą abstrakcyjną błąd pojawia się **w chwili tworzenia obiektu**, czyli przy uruchomieniu aplikacji lub w pierwszym teście — a nie o 23:00, gdy scena „Dobranoc” po raz pierwszy spróbuje opuścić rolety.

---

### 🔌 Interfejs jako czysta klasa abstrakcyjna

Python nie ma osobnego słowa kluczowego `interface`. Interfejs to po prostu klasa abstrakcyjna, która zawiera **wyłącznie** metody abstrakcyjne. Dodajmy umiejętność „da się ściemniać”, którą mają tylko niektóre urządzenia:

```python
class Sciemnialne(ABC):
    """Interfejs: urządzenie, którego moc można płynnie regulować."""

    @abstractmethod
    def ustaw_jasnosc(self, procent):
        ...


class LampaSciemnialna(Lampa, Sciemnialne):
    def ustaw_jasnosc(self, procent):
        print(f"💡 {self.nazwa}: jasność {procent}%")
```

```python
>>> nocna = LampaSciemnialna("Lampka nocna", "sypialnia")
>>> nocna.ustaw_jasnosc(20)
💡 Lampka nocna: jasność 20%
>>> isinstance(nocna, Sciemnialne), isinstance(nocna, Urzadzenie)
(True, True)
```

To przykład dziedziczenia wielokrotnego w roli domieszki z sekcji o MRO: klasa jest urządzeniem i *dodatkowo* spełnia interfejs `Sciemnialne`.

| |Interfejs|Klasa abstrakcyjna|
|---|---|---|
|Definiuje **co** trzeba umieć|✅|✅|
|Dostarcza gotowy kod (**jak**)|❌|✅ (część metod)|
|Można utworzyć obiekt|❌|❌|
|W Pythonie|klasa `ABC` tylko z `@abstractmethod`|klasa `ABC` z metodami abstrakcyjnymi i konkretnymi|

---

## 🤝 Protokoły

> Typowanie strukturalne: obiekt pasuje do protokołu, jeśli ma odpowiednie metody — bez dziedziczenia i bez importowania.

---

### 📌 Typowanie nominalne a strukturalne

Klasy abstrakcyjne opierają się na **typowaniu nominalnym** (*nominal typing*): relację „A jest typu B” trzeba **jawnie zapisać** przez dziedziczenie. `Lampa` jest `Urzadzeniem`, bo w kodzie stoi `class Lampa(Urzadzenie)`.

**Protokoły** (`typing.Protocol`, od Pythona 3.8) opierają się na **typowaniu strukturalnym** (*structural typing*): obiekt pasuje do protokołu, jeśli **ma odpowiednią strukturę**, czyli wymagane metody i atrybuty. Dziedziczenie nie jest potrzebne. To *duck typing* z sekcji o polimorfizmie, ale zapisany jawnie i sprawdzalny przez narzędzia.

---

### 🩺 Moduł diagnostyki

Budujemy moduł, który zbiera raport o stanie domu. Do działania potrzebuje od każdego źródła **tylko jednego**: metody `status()`. Nie obchodzi go, czy obiekt umie się włączać, grać muzykę czy świecić.

```python
from typing import Protocol


class ZrodloDiagnostyki(Protocol):
    """Wszystko, co potrafi zaraportować swój stan."""

    def status(self) -> str: ...


def raport(zrodla: list[ZrodloDiagnostyki]) -> None:
    for zrodlo in zrodla:
        print("🩺", zrodlo.status())
```

Teraz dwie klasy, które **nic nie wiedzą o protokole**: nie dziedziczą po nim i nawet go nie importują. Pierwsza to nasza lampa. Druga to stacja pogodowa z **zewnętrznej biblioteki**, której kodu nie możemy zmienić:

```python
class Lampa:
    def __init__(self, nazwa):
        self.nazwa = nazwa

    def wlacz(self):
        print(f"💡 {self.nazwa}: świecę")

    def status(self) -> str:
        return f"{self.nazwa}: żarówka sprawna"


class StacjaPogodowa:                       # klasa z cudzej biblioteki
    def status(self) -> str:
        return "Stacja pogodowa: 12 °C, bezwietrznie"


raport([Lampa("Lampa sufitowa"), StacjaPogodowa()])
```

```
🩺 Lampa sufitowa: żarówka sprawna
🩺 Stacja pogodowa: 12 °C, bezwietrznie
```

Obie klasy **pasują do protokołu strukturalnie**, bo mają metodę `status()`. Gdyby `ZrodloDiagnostyki` było klasą abstrakcyjną, `StacjaPogodowa` musiałaby po niej dziedziczyć — a tego w cudzej bibliotece nie zmienimy.

---

### 🔎 Gdzie wychodzą błędy?

W czasie działania programu protokół niczego nie wymusza. Jego siła ujawnia się w **statycznym analizatorze typów** (*static type checker*), takim jak **mypy** czy **pyright**, który czyta kod przed uruchomieniem. Dorzućmy do raportu doniczkę bez metody `status()`:

```python
class Doniczka:
    pass


raport([Lampa("Lampa sufitowa"), Doniczka()])
```

Uruchomiony, ten kod wywróci się dopiero przy wywołaniu `status()` na doniczce (`AttributeError`) — dokładnie jak przy *duck typing*. Analizator typów wyłapie jednak błąd, zanim program w ogóle ruszy:

```
$ mypy dom.py
dom.py:38: error: List item 1 has incompatible type "Doniczka"; expected "ZrodloDiagnostyki"  [list-item]
Found 1 error in 1 file (checked 1 source file)
```

Analizator wskazuje błąd **w miejscu użycia**, czyli tam, gdzie obiekt trafia do funkcji oczekującej protokołu — a nie przy tworzeniu obiektu, jak w ABC.

> 💡 Jeśli potrzebujesz sprawdzać protokół **w czasie działania** programu (`isinstance(obiekt, ZrodloDiagnostyki)`), oznacz go dekoratorem `@typing.runtime_checkable`. Taki test sprawdza jednak tylko **obecność** metod, a nie ich sygnatury.

---

### ✂️ Każdy moduł mówi, czego potrzebuje

Najładniejsza cecha protokołów: **protokół należy do miejsca, w którym jest używany**, a nie do hierarchii klas. Moduł scen potrzebuje włączania i wyłączania, moduł diagnostyki tylko statusu. Każdy definiuje własny, wąski protokół:

```python
from typing import Protocol


class Sterowalne(Protocol):                 # potrzeby modułu scen
    def wlacz(self) -> None: ...
    def wylacz(self) -> None: ...


class ZrodloDiagnostyki(Protocol):          # potrzeby modułu diagnostyki
    def status(self) -> str: ...
```

Lampa może pasować do obu protokołów, a stacja pogodowa tylko do drugiego — i to jest w porządku. Takie rozbijanie dużego interfejsu na małe, skrojone pod konkretnego odbiorcę nazywa się **zasadą segregacji interfejsów** (*Interface Segregation Principle*, litera **I** w regułach **SOLID**). Dzięki temu moduły są ze sobą luźno powiązane (*loose coupling*).

---

### ⚖️ ABC czy protokół?

| |Klasa abstrakcyjna (ABC)|Protokół|
|---|---|---|
|**Rodzaj typowania**|nominalne (jawne dziedziczenie)|strukturalne („ma odpowiednie metody”)|
|**Czy klasa musi dziedziczyć i importować?**|tak|nie|
|**Kiedy wychodzi błąd?**|przy **tworzeniu** obiektu (w czasie działania)|w miejscu **użycia**, podczas analizy typów (mypy, pyright, edytor)|
|**Wspólny, gotowy kod dla podklas**|✅|❌ (zwykle tylko sygnatury)|
|**Najlepszy, gdy…**|kontrolujesz całą rodzinę klas i chcesz współdzielić kod|łączysz niezależne moduły i biblioteki, których nie możesz zmieniać|

> 💡 To nie jest wybór „albo–albo”. Rozsądny podział: **ABC** dla własnej, zwartej hierarchii (nasze `Urzadzenie` z gotowym `opis()`), **protokoły** na granicach modułów (diagnostyka przyjmie wszystko, co ma `status()`).

---

## 🔣 Typy generyczne

> Typ z parametrem — jedna funkcja lub klasa dla wielu typów, bez utraty informacji o tym, co dokładnie przechowuje.

---

### 📌 Problem: funkcja, która gubi informację o typie

Chcemy funkcji zwracającej pierwszy element dowolnej sekwencji, np. pierwszą lampę z listy. Jak opisać typy jej argumentu i wyniku?

```python
class Lampa:
    def __init__(self, nazwa, jasnosc=100):
        self.nazwa = nazwa
        self.jasnosc = jasnosc


class Glosnik:
    def __init__(self, nazwa, glosnosc=30):
        self.nazwa = nazwa
        self.glosnosc = glosnosc
```

Pierwszy pomysł to `Any`:

```python
from typing import Any

def pierwszy(elementy: list[Any]) -> Any:
    return elementy[0]
```

Działa, ale **analizator typów traci całą wiedzę**. Wynik może być czymkolwiek, więc nie podpowie, że `pierwszy(lampy).jasnosc` jest poprawne, ani nie ostrzeże przed literówką.

---

### 🔣 Funkcja generyczna

**Typ generyczny** (*generic*) to „typ z parametrem”. Zamiast konkretnego typu piszemy **zmienną typu**, zwyczajowo `T`, którą podajemy w nawiasie kwadratowym po nazwie funkcji (składnia dostępna od Pythona 3.12):

```python
from collections.abc import Sequence


def pierwszy[T](elementy: Sequence[T]) -> T:
    return elementy[0]
```

Czytamy: „dla dowolnego typu `T`: przyjmuję sekwencję elementów typu `T` i zwracam jeden element typu `T`”. Jaki to typ, wynika z wywołania:

```python
>>> lampy = [Lampa("Lampa sufitowa", 80), Lampa("Kinkiet", 40)]
>>> pierwszy(lampy).jasnosc          # analizator wie, że to Lampa
80
>>> pierwszy(["salon", "kuchnia"])   # tu T = str
'salon'
```

Dla `lampy: list[Lampa]` analizator ustala `T = Lampa`, więc wie, że wynik jest lampą i ma atrybut `jasnosc`. Dla listy napisów `T = str`. **Jedna funkcja, pełna informacja o typach.**

> 💡 `Sequence` (z `collections.abc`) to dowolna uporządkowana kolekcja z dostępem przez indeks: lista, krotka, napis i wiele innych. To lepszy wybór niż `list`, bo funkcja przyjmie więcej rodzajów danych.

---

### 🗝️ Kilka parametrów typu

Parametrów może być więcej. Funkcja znajdująca w słowniku wartość dla danego klucza:

```python
def znajdz[K, V](mapa: dict[K, V], klucz: K) -> V:
    return mapa[klucz]


oswietlenie = {"salon": Lampa("Lampa sufitowa", 80), "sypialnia": Lampa("Lampka nocna", 20)}
print(znajdz(oswietlenie, "sypialnia").nazwa)
```

```
Lampka nocna
```

`K` (*key*) to typ klucza, `V` (*value*) to typ wartości. Dla `dict[str, Lampa]` analizator ustala `K = str` i `V = Lampa`. Pilnuje więc, by klucz był napisem, i wie, że wynik jest lampą. Nazwy `T`, `K` i `V` to tylko konwencja, choć warto się jej trzymać.

---

### 📦 Klasa generyczna: rejestr urządzeń

Najczęściej generyki spotyka się w klasach-kontenerach. Zbudujmy **rejestr urządzeń jednego rodzaju**:

```python
class Rejestr[T]:
    """Rejestr urządzeń jednego rodzaju."""

    def __init__(self) -> None:
        self._elementy: list[T] = []

    def dodaj(self, element: T) -> None:
        self._elementy.append(element)

    def usun(self, element: T) -> None:
        if element in self._elementy:
            self._elementy.remove(element)

    def wszystkie(self) -> list[T]:
        return list(self._elementy)
```

Przy tworzeniu obiektu podajemy konkretny typ, a `T` zostaje nim „zastąpione”:

```python
>>> lampy = Rejestr[Lampa]()
>>> lampy.dodaj(Lampa("Lampa sufitowa"))
>>> lampy.dodaj(Lampa("Kinkiet"))
>>> [lampa.nazwa for lampa in lampy.wszystkie()]
['Lampa sufitowa', 'Kinkiet']
```

Dla analizatora `Rejestr[Lampa]` wygląda teraz tak, jakbyśmy napisali osobną klasę, w której wszędzie zamiast `T` stoi `Lampa`. Tę samą klasę wykorzystamy do głośników (`Rejestr[Glosnik]`) bez pisania czegokolwiek od nowa.

---

### ⚠️ Adnotacje nie są egzekwowane

**Python nie sprawdza typów w czasie działania programu.** Adnotacje to wskazówki dla ludzi i narzędzi. Poniższy kod uruchomi się bez błędu:

```python
>>> lampy.dodaj(Glosnik("Głośnik"))   # głośnik w rejestrze lamp!
>>> len(lampy.wszystkie())
3
```

Wyłapie to dopiero analizator typów:

```
$ mypy dom.py
dom.py:33: error: Argument 1 to "dodaj" of "Rejestr" has incompatible type "Glosnik"; expected "Lampa"  [arg-type]
Found 1 error in 1 file (checked 1 source file)
```

> 💡 Przy pracy z adnotacjami warto uruchamiać **mypy** lub **pyright** — a większość edytorów (VS Code, PyCharm) robi to na bieżąco.

---

### 🎯 Ograniczenie typu: `T` musi być urządzeniem

Rejestr urządzeń nie powinien przyjmować np. napisów. Parametr typu może mieć **górne ograniczenie** (*upper bound*), zapisywane po dwukropku:

```python
class Rejestr[T: Urzadzenie]:   # T może być tylko Urzadzeniem lub jego podklasą
    ...
```

Teraz `Rejestr[Lampa]` jest poprawny, a `Rejestr[str]` analizator odrzuci. Dodatkowa korzyść: wewnątrz klasy wolno używać na elementach wszystkiego, co ma `Urzadzenie`, np. `element.wlacz()`.

---

### 🕰️ Starsza składnia (Python < 3.12)

W starszym kodzie spotkasz zapis z `TypeVar` i `Generic`. Znaczy dokładnie to samo:

```python
from typing import Generic, TypeVar

T = TypeVar("T")


class StaryRejestr(Generic[T]):
    def __init__(self) -> None:
        self._elementy: list[T] = []
```

> 💡 **Kiedy sięgać po generyki?** Gdy piszesz funkcję lub klasę, która **działa tak samo dla wielu typów**, ale między wejściem a wyjściem obowiązuje **związek** („zwracam to, co dostałem”, „przechowuję elementy jednego rodzaju”). Jeśli takiego związku nie ma, zwykle wystarczy konkretny typ, unia typów (`Lampa | Glosnik`) albo protokół.

---

## 🚶 Iteratory

> Obiekt iterowalny to dom, a iterator to przewodnik — `iter()`, `next()` i `StopIteration` pracują pod maską każdej pętli `for`.

---

### 📌 Dom i przewodnik

Dom jest gotowy i wyposażony. Pora go **obejść**: pokój po pokoju, odczyt po odczycie. Ta i dwie kolejne sekcje pokazują, jak Python przechodzi przez kolejne elementy czegokolwiek — od listy po nieskończony strumień danych z czujnika.

Dwa słowa, które brzmią prawie tak samo i są nieustannie mylone:

- **obiekt iterowalny** (*iterable*) to coś, **po czym można przejść** pętlą `for`: lista, krotka, napis, słownik, plik… i za chwilę nasz dom;
- **iterator** (*iterator*) to obiekt, który **prowadzi przez kolejne elementy**.

Najlepiej wyobrazić to sobie jako **dom i przewodnika**. Dom (obiekt iterowalny) można zwiedzać, ale sam nikogo nie oprowadza. Oprowadza **przewodnik** (iterator), który:

- **pamięta, w którym pokoju jesteście** (ma stan);
- na hasło „dalej” **prowadzi do następnego pokoju** (metoda `__next__()`);
- **idzie tylko do przodu**: nie cofa się ani nie zaczyna od nowa;
- gdy pokoje się skończą, ogłasza **koniec wycieczki** (wyjątek `StopIteration`).

Każda nowa grupa zwiedzających dostaje **nowego przewodnika**: wywołanie `iter(dom)` za każdym razem tworzy świeży iterator.

```
obiekt iterowalny                 iterator
(lista, napis, Dom)  ─ iter() ─►  przewodnik ze stanem
ma __iter__()                     ma __iter__() i __next__()
                                     │
                                     ├── next() ──────►  kolejny pokój
                                     │
                                     └── brak pokoi ──►  StopIteration
```

---

### 🔬 `iter()`, `next()` i `StopIteration`

Pętla `for` robi to wszystko po cichu. Rozbierzmy ją na części na prostej liście pokoi:

```python
>>> pokoje = ["przedpokój", "salon", "kuchnia"]
>>> przewodnik = iter(pokoje)           # lista wydaje nam przewodnika
>>> przewodnik
<list_iterator object at 0x...>
>>> next(przewodnik)
'przedpokój'
>>> next(przewodnik)
'salon'
>>> next(przewodnik)
'kuchnia'
>>> next(przewodnik)                    # koniec wycieczki
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    next(przewodnik)                    # koniec wycieczki
    ~~~~^^^^^^^^^^^^
StopIteration
```

Lista jest iterowalna, ale **sama nie jest iteratorem**, bo nie ma metody `__next__`:

```python
>>> next(pokoje)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    next(pokoje)
    ~~~~^^^^^^^^
TypeError: 'list' object is not an iterator
>>> hasattr(pokoje, "__iter__"), hasattr(pokoje, "__next__")
(True, False)
>>> hasattr(przewodnik, "__iter__"), hasattr(przewodnik, "__next__")
(True, True)
```

> 💡 Wbudowane funkcje `iter(x)` i `next(x)` to w uproszczeniu wygodne skróty: wywołują odpowiednio `x.__iter__()` i `x.__next__()`.

---

### 🔁 Co naprawdę robi pętla `for`

Pętla

```python
for pokoj in pokoje:
    print(pokoj)
```

jest w praktyce równoważna temu kodowi:

```python
pokoje = ["przedpokój", "salon", "kuchnia"]

przewodnik = iter(pokoje)               # 1. poproś o przewodnika
while True:
    try:
        pokoj = next(przewodnik)        # 2. „dalej!”
    except StopIteration:               # 3. koniec wycieczki → wyjdź z pętli
        break
    print(pokoj)                        # 4. ciało pętli
```

```
przedpokój
salon
kuchnia
```

Pętla `for` sama obsługuje `StopIteration`, dlatego na co dzień nigdy go nie widzisz.

---

### 🪫 Przewodnik pamięta i się wyczerpuje

Iterator ma **stan**: jeśli przejdziesz część drogi ręcznie, pętla podejmie wycieczkę tam, gdzie skończyłeś. A gdy przejdzie wszystko, jest **wyczerpany** (*exhausted*): kolejna próba niczego już nie zwróci.

```python
>>> przewodnik = iter(pokoje)
>>> next(przewodnik)                    # przedpokój już za nami
'przedpokój'
>>> for pokoj in przewodnik:            # pętla zaczyna od salonu!
...     print(pokoj)
...
salon
kuchnia
>>> list(przewodnik)                    # wyczerpany: nic więcej nie pokaże
[]
>>> list(pokoje)                        # ale dom stoi – można zwiedzać od nowa
['przedpokój', 'salon', 'kuchnia']
```

---

### 🏠 Nasz dom jako obiekt iterowalny

Aby klasa była iterowalna, wystarczy metoda `__iter__()` zwracająca iterator. Dom przechowuje pokoje na liście, więc najprościej oddać iterator tej listy:

```python
class Dom:
    def __init__(self, adres, pokoje):
        self.adres = adres
        self.pokoje = list(pokoje)

    def __iter__(self):
        return iter(self.pokoje)            # każde zwiedzanie = nowy przewodnik
```

```python
>>> lipowa = Dom("ul. Lipowa 7", ["przedpokój", "salon", "kuchnia", "sypialnia"])
>>> for pokoj in lipowa:
...     print("🚪", pokoj)
...
🚪 przedpokój
🚪 salon
🚪 kuchnia
🚪 sypialnia
>>> "salon" in lipowa                     # operator in też korzysta z iteracji
True
>>> list(lipowa)                          # dom można zwiedzać wielokrotnie
['przedpokój', 'salon', 'kuchnia', 'sypialnia']
```

---

### 🔙 Własny iterator: obchód od końca

Teraz napiszmy **własnego przewodnika**, który oprowadza po pokojach od ostatniego do pierwszego. To odpowiednik klasy `Reverse` z dokumentacji. Iterator potrzebuje dwóch metod:

- `__next__()`, która zwraca kolejny element albo zgłasza `StopIteration`;
- `__iter__()`, która w przypadku iteratora **zwraca samego siebie** (`return self`).

```python
class ObchodOdKonca:
    """Iterator: oprowadza po pokojach w odwrotnej kolejności."""

    def __init__(self, pokoje):
        self.pokoje = pokoje
        self.indeks = len(pokoje)           # stan: gdzie jesteśmy

    def __iter__(self):
        return self                         # iterator jest swoim własnym przewodnikiem

    def __next__(self):
        if self.indeks == 0:
            raise StopIteration             # koniec wycieczki
        self.indeks = self.indeks - 1
        return self.pokoje[self.indeks]
```

```python
>>> obchod = ObchodOdKonca(["przedpokój", "salon", "kuchnia"])
>>> iter(obchod) is obchod
True
>>> for pokoj in obchod:
...     print(pokoj)
...
kuchnia
salon
przedpokój
>>> list(obchod)                          # ten przewodnik już skończył pracę
[]
```

> 💡 **Każdy iterator jest obiektem iterowalnym**, bo ma `__iter__` zwracające `self` — dlatego można go użyć w pętli `for`. Ale **nie każdy obiekt iterowalny jest iteratorem**: lista, napis czy nasz `Dom` nie mają `__next__`. Różnica w praktyce: obiekt iterowalny można przechodzić **wiele razy**, iterator **tylko raz**.

---

### ♾️ Iteratory bez końca

Iterator nie musi się kończyć. Wystarczy, że `__next__` nigdy nie zgłosi `StopIteration`. Brzmi groźnie, ale bywa bardzo przydatne, np. dla strumienia odczytów z czujnika, który działa, dopóki działa dom. Iterator **i tak pobiera tylko jeden element naraz**, więc nie zajmuje coraz więcej pamięci. Wrócimy do tego w sekcji o generatorach.

---

### 🏷️ `Iterable` w adnotacjach typów

Gdy funkcja chce tylko **przejść** po elementach, w adnotacji podaj `Iterable`, a nie `list`. Wtedy przyjmie listę, krotkę, zbiór, generator, a nawet nasz `Dom`:

```python
from collections.abc import Iterable


def oprowadz(pokoje: Iterable[str]) -> None:
    for pokoj in pokoje:
        print("👉", pokoj)


oprowadz(("salon", "kuchnia"))           # krotka
oprowadz(lipowa)                          # nasz Dom
```

```
👉 salon
👉 kuchnia
👉 przedpokój
👉 salon
👉 kuchnia
👉 sypialnia
```

---

## ⚙️ Generatory

> Funkcja z `yield` umie zrobić przerwę i wrócić do pracy — to najwygodniejszy sposób pisania iteratorów.

---

### 📌 Funkcja, która umie zrobić przerwę

Klasa `ObchodOdKonca` działa, ale zajęła kilkanaście linii: `__init__`, `__iter__`, `__next__`, ręczne pilnowanie indeksu i `StopIteration`. **Generator** pozwala napisać tego samego przewodnika w trzech linijkach:

```python
def od_konca(pokoje):
    for indeks in range(len(pokoje) - 1, -1, -1):
        yield pokoje[indeks]
```

```python
>>> for pokoj in od_konca(["przedpokój", "salon", "kuchnia"]):
...     print(pokoj)
...
kuchnia
salon
przedpokój
```

Generator to zwykła funkcja, w której zamiast `return` pojawia się **`yield`**. Oba słowa oddają wartość, ale różnią się tym, co dzieje się dalej:

| |`return`|`yield`|
|---|---|---|
|**Oddaje wartość**|✅|✅|
|**Co dalej z funkcją?**|**kończy się**; zmienne lokalne znikają|**zatrzymuje się**; cały stan zostaje zachowany|
|**Ile razy może oddać wartość**|raz|dowolnie wiele razy|

Wszystko, co robi generator, da się zrobić klasą-iteratorem, ale generator jest zwięźlejszy, bo Python **sam** tworzy metody `__iter__()` i `__next__()`, **sam** pamięta zmienne lokalne (nie trzeba `self.indeks`) i **sam** zgłasza `StopIteration`, gdy funkcja się kończy.

---

### ⏸️ Przewodnik, który czeka na hasło „dalej”

Zobaczmy, jak dokładnie generator zatrzymuje się i wznawia. Ten przewodnik komentuje każdy swój krok:

```python
def wycieczka():
    print("  (przewodnik: zaczynamy)")
    yield "przedpokój"
    print("  (przewodnik: idziemy dalej…)")
    yield "salon"
    print("  (przewodnik: ostatni przystanek)")
    yield "kuchnia"
    print("  (przewodnik: koniec wycieczki)")
```

```python
>>> w = wycieczka()                       # nic się nie wypisało!
>>> w
<generator object wycieczka at 0x...>
>>> next(w)
  (przewodnik: zaczynamy)
'przedpokój'
>>> next(w)
  (przewodnik: idziemy dalej…)
'salon'
>>> next(w)
  (przewodnik: ostatni przystanek)
'kuchnia'
>>> next(w)
  (przewodnik: koniec wycieczki)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
    next(w)
    ~~~~^^^
StopIteration
```

Krok po kroku:

1. **Wywołanie `wycieczka()` nie wykonuje ani jednej linii ciała funkcji.** Tworzy tylko **obiekt generatora**, czyli przewodnika gotowego do pracy, który czeka na sygnał.
2. Pierwsze `next(w)` uruchamia funkcję od początku do pierwszego `yield`, oddaje `"przedpokój"` i **zatrzymuje się**.
3. Każde kolejne `next(w)` **wznawia** funkcję dokładnie w miejscu zatrzymania i biegnie do następnego `yield`.
4. Gdy funkcja dobiegnie końca, generator zgłasza `StopIteration` — tak jak każdy iterator.

> 💡 **Generator jest iteratorem.** `iter(w) is w` zwraca `True`, a `w` ma metody `__iter__` i `__next__`. Generatory to po prostu najwygodniejszy sposób tworzenia iteratorów.

---

### 💤 Leniwość: liczyć dopiero wtedy, gdy trzeba

Prawdziwa moc generatorów to **leniwe wartościowanie** (*lazy evaluation*): generator wykonuje tylko tyle pracy, ile potrzeba do wyprodukowania **następnej** wartości, i robi przerwę. Zwykła funkcja zwracająca listę działa **zachłannie** (*eager evaluation*): liczy wszystko od razu i trzyma wynik w pamięci.

Nasz termostat co minutę dostaje odczyt z czujnika temperatury. Czujnik działa bez końca, więc lista odczytów nie wchodzi w grę — nigdy nie skończylibyśmy jej budować. Generator radzi sobie z tym bez trudu:

```python
import random


def odczyty_temperatury(start=21.0):
    """Nieskończony strumień odczytów z czujnika (symulacja)."""
    temperatura = start
    while True:                                  # nigdy się nie kończy…
        temperatura += random.uniform(-0.3, 0.9)
        yield round(temperatura, 1)              # …ale oddaje po jednym odczycie
```

Pobierzmy pięć pierwszych odczytów za pomocą `itertools.islice` („wytnij kawałek iteratora”):

```python
from itertools import islice

random.seed(7)                                   # stałe ziarno → powtarzalny wynik
print(list(islice(odczyty_temperatury(), 5)))
```

```
[21.1, 21.0, 21.5, 21.2, 21.6]
```

---

### 🏭 Produkcja oddzielona od konsumpcji

Generatory pięknie **rozdzielają produkcję danych od ich zużycia**. Generator wie, *jak* zdobyć odczyty. Kod, który z nich korzysta, decyduje, *co* z nimi zrobić i *kiedy* przestać:

```python
random.seed(7)
for odczyt in odczyty_temperatury():
    if odczyt > 25:
        print(f"🔥 {odczyt} °C – włączam klimatyzację")
        break
```

```
🔥 25.3 °C – włączam klimatyzację
```

Generator wyprodukował dokładnie tyle odczytów, ile było trzeba — ani jednego więcej. Gdy w innym miejscu programu będziemy szukać spadku poniżej 18 °C, użyjemy **tego samego** generatora z innym warunkiem. Logikę odczytu czujnika mamy w jednym miejscu, więc jej ulepszenie nie wymaga poprawek w wielu pętlach. Kod jest **modularny** i łatwy w utrzymaniu.

---

### 📜 Przykład z życia: ogromny dziennik zdarzeń

System domu zapisuje każde zdarzenie w pliku `dom.log`. Po kilku latach plik ma miliony linii. Wczytanie go w całości do pamięci (`plik.readlines()`) byłoby marnotrawstwem, skoro szukamy tylko alarmów, a każdą linię oceniamy niezależnie od pozostałych. Generator czyta **jedną linię naraz**:

```python
def zdarzenia(sciezka):
    """Oddaje kolejne linie dziennika, nie wczytując całego pliku."""
    with open(sciezka, encoding="utf-8") as plik:
        for linia in plik:
            yield linia.rstrip("\n")


for zdarzenie in zdarzenia("dom.log"):
    if "ALARM" in zdarzenie:
        print(zdarzenie)
```

Niezależnie od wielkości pliku program trzyma w pamięci naraz tylko jedną linię.

---

### ↪️ `yield from`: przekaż dalej

Gdy generator ma oddać **wszystkie** elementy innego obiektu iterowalnego, zamiast pętli z `yield` wystarczy `yield from`:

```python
def caly_dom(pietra):
    for pietro in pietra:
        yield from pietro                         # = for pokoj in pietro: yield pokoj


parter = ["przedpokój", "salon", "kuchnia"]
pietro = ["sypialnia", "łazienka"]
print(list(caly_dom([parter, pietro])))
```

```
['przedpokój', 'salon', 'kuchnia', 'sypialnia', 'łazienka']
```

---

### ⚖️ Kiedy generator, a kiedy lista?

|Generator ✅|Lista ✅|
|---|---|
|danych jest bardzo dużo albo nieskończenie wiele|danych jest niewiele|
|przetwarzasz elementy **po kolei, jeden po drugim**|potrzebujesz dostępu do **dowolnego** elementu (`lista[5]`)|
|przechodzisz po danych **jeden raz**|przechodzisz po danych **wiele razy**|
|chcesz zacząć pracę, zanim wszystko zostanie wyliczone|potrzebujesz `len()`, sortowania, wycinków|

> ⚠️ Generator **nie pamięta** oddanych wartości i **nie da się go przewinąć**. Jeśli potrzebujesz wszystkich wartości naraz (np. do policzenia średniej i odchylenia standardowego), zamień skończony generator na listę: `list(generator)`. Pamiętaj tylko, że wtedy wszystkie wartości trafią do pamięci, a dla generatora nieskończonego taka operacja nigdy się nie skończy.

> 💡 W adnotacjach typów generator oddający liczby zmiennoprzecinkowe opisuje się jako `Iterator[float]` (wersja prosta) albo `Generator[float, None, None]` (wersja pełna — z typem wartości wysyłanych do generatora i zwracanych na końcu). Od Pythona 3.13 dwa ostatnie parametry mają domyślnie wartość `None`, więc wystarczy `Generator[float]`. Oba typy znajdziesz w `collections.abc`.

---

## 🧵 Wyrażenia generatorowe

> Generator w jednej linijce — zapisany jak wyrażenie listowe, tylko w nawiasach okrągłych zamiast kwadratowych.

---

### 📌 Generator w jednej linijce

Proste generatory można zapisać jeszcze krócej, jako **wyrażenie generatorowe** (*generator expression*). Wygląda jak wyrażenie listowe (*list comprehension*), tylko **w nawiasach okrągłych zamiast kwadratowych**:

```python
>>> [m * m for m in range(5)]             # lista: wszystko liczone od razu
[0, 1, 4, 9, 16]
>>> (m * m for m in range(5))             # generator: nic jeszcze nie policzono
<generator object <genexpr> at 0x...>
```

Wyrażenia generatorowe są zwykle **oszczędniejsze w pamięci** niż odpowiadające im wyrażenia listowe. Najlepiej sprawdzają się wtedy, gdy wynik od razu konsumuje funkcja otaczająca, np. `sum()`, `max()`, `min()`, `any()`, `all()`, `set()` czy `list()`.

---

### 🏠 Przykłady na pokojach naszego domu

Weźmy pokoje z sekcji o `@dataclass`:

```python
from dataclasses import dataclass


@dataclass
class Pokoj:
    nazwa: str
    metraz: float
    pietro: int = 0


pokoje = [
    Pokoj("salon", 32.5),
    Pokoj("kuchnia", 14.0),
    Pokoj("sypialnia", 16.5, pietro=1),
    Pokoj("łazienka", 7.0, pietro=1),
]
```

```python
>>> sum(p.metraz for p in pokoje)                     # powierzchnia całego domu
70.0
>>> max((p.metraz, p.nazwa) for p in pokoje)          # największy pokój
(32.5, 'salon')
>>> set(p.pietro for p in pokoje)                     # na których piętrach są pokoje
{0, 1}
>>> any(p.metraz > 30 for p in pokoje)                # czy jest pokój powyżej 30 m²?
True
>>> list(p.nazwa for p in pokoje if p.pietro == 1)    # pokoje na piętrze
['sypialnia', 'łazienka']
```

Odpowiednikiem iloczynu skalarnego z dokumentacji jest koszt paneli podłogowych, gdy w każdym pokoju cena za metr jest inna:

```python
>>> metraze = [32.5, 14.0, 16.5]
>>> ceny_za_m2 = [120, 90, 100]
>>> sum(m * c for m, c in zip(metraze, ceny_za_m2))   # 3900 + 1260 + 1650
6810.0
```

Zagnieżdżone pętle też są dozwolone. Oto zbiór wszystkich słów w dzienniku zdarzeń:

```python
>>> dziennik = ["salon lampa włączona", "kuchnia lampa wyłączona"]
>>> sorted(set(slowo for linia in dziennik for slowo in linia.split()))
['kuchnia', 'lampa', 'salon', 'wyłączona', 'włączona']
```

---

### 🔘 Kiedy można pominąć nawiasy

Nawiasy okrągłe są potrzebne **prawie zawsze**. Wyjątek: gdy wyrażenie generatorowe jest **jedynym argumentem** funkcji, wystarczą nawiasy samego wywołania. Poniższe zapisy są równoważne:

```python
sum(p.metraz for p in pokoje)
sum((p.metraz for p in pokoje))
```

Przy kilku argumentach dodatkowe nawiasy są obowiązkowe: `sorted((p.nazwa for p in pokoje), reverse=True)`.

---

### 🆕 Nowość w Pythonie 3.15: rozpakowywanie w wyrażeniach generatorowych

Od Pythona 3.15 ([PEP 798](https://peps.python.org/pep-0798/)) w wyrażeniu generatorowym (i listowym) można użyć gwiazdki `*`, by **rozpakować** każdy element. Przydaje się to do „spłaszczania” zagnieżdżonych struktur, np. listy pięter, z których każde jest listą pokoi:

```python
>>> pietra = [["przedpokój", "salon"], [], ["sypialnia", "łazienka"]]
>>> g = (*pietro for pietro in pietra)       # ✅ Python 3.15+
>>> list(g)
['przedpokój', 'salon', 'sypialnia', 'łazienka']
```

I znów, jako jedyny argument funkcji, bez dodatkowych nawiasów: `list(*pietro for pietro in pietra)`. W starszych wersjach ten sam efekt da podwójna pętla `(pokoj for pietro in pietra for pokoj in pietro)` albo `yield from` z sekcji o generatorach.

> ⚠️ W Pythonie 3.14 i starszych ten zapis kończy się błędem `SyntaxError: iterable unpacking cannot be used in comprehension`.

---

### 💾 Lista czy generator? Różnica w pamięci

```python
import sys

lista = [m * m for m in range(1_000_000)]
generator = (m * m for m in range(1_000_000))

print(f"lista:     {sys.getsizeof(lista):>9,} B")
print(f"generator: {sys.getsizeof(generator):>9,} B")
```

Wynik na Pythonie 3.14 (dokładne liczby zależą od wersji Pythona i systemu):

```
lista:     8,448,728 B
generator:       208 B
```

Lista trzyma milion gotowych liczb. Generator trzyma tylko „przepis” i bieżący stan, niezależnie od tego, ile elementów jeszcze wyprodukuje. Sam `getsizeof` listy nie obejmuje nawet pamięci zajętej przez liczby, na które lista wskazuje.

> 💡 Prosta reguła: jeśli wynik jest od razu „zjadany” przez funkcję taką jak `sum()`, `max()` czy `any()`, użyj **nawiasów okrągłych**. Jeśli potrzebujesz gotowej listy do wielokrotnego użytku, użyj **kwadratowych**.

---

## 🏁 Wszystko razem: mały system inteligentnego domu

> Wszystkie elementy rozdziału w jednym programie — komentarze podpowiadają, który temat ilustruje dany fragment.

---

### 📌 Kod

Traktuj ten program jako powtórkę: każdy fragment opisuje komentarz z nazwą omówionego wcześniej mechanizmu.

```python
from abc import ABC, abstractmethod
from collections.abc import Iterable, Iterator
from dataclasses import dataclass
from typing import Protocol


# ── Pokoje: @dataclass ──────────────────────────────────────────────────────
@dataclass
class Pokoj:
    nazwa: str
    metraz: float


# ── Urządzenia: klasa abstrakcyjna + dziedziczenie ──────────────────────────
class Urzadzenie(ABC):
    def __init__(self, nazwa: str, pokoj: str) -> None:
        self.nazwa = nazwa
        self.pokoj = pokoj
        self.wlaczone = False

    @abstractmethod
    def wlacz(self) -> None: ...

    def wylacz(self) -> None:
        self.wlaczone = False
        print(f"   ⏻  {self.nazwa}: wyłączam")

    def status(self) -> str:
        stan = "wł." if self.wlaczone else "wył."
        return f"{self.nazwa} [{self.pokoj}] – {stan}"


class Lampa(Urzadzenie):
    def __init__(self, nazwa: str, pokoj: str, jasnosc: int = 100) -> None:
        super().__init__(nazwa, pokoj)
        self.jasnosc = jasnosc

    def wlacz(self) -> None:
        self.wlaczone = True
        print(f"   💡 {self.nazwa}: świecę na {self.jasnosc}%")


class Termostat(Urzadzenie):
    MIN, MAX = 5.0, 30.0                               # zmienne klasy

    def __init__(self, nazwa: str, pokoj: str, temperatura: float = 21.0) -> None:
        super().__init__(nazwa, pokoj)
        self.temperatura = temperatura

    @property                                          # właściwość z walidacją
    def temperatura(self) -> float:
        return self._temperatura

    @temperatura.setter
    def temperatura(self, wartosc: float) -> None:
        if not self.MIN <= wartosc <= self.MAX:
            raise ValueError(f"Zakres: {self.MIN}–{self.MAX} °C")
        self._temperatura = float(wartosc)

    def wlacz(self) -> None:
        self.wlaczone = True
        print(f"   🌡️ {self.nazwa}: grzeję do {self.temperatura} °C")

    def status(self) -> str:                           # rozszerzenie przez super()
        return super().status() + f", {self.temperatura} °C"


# ── Rejestr: klasa generyczna z ograniczeniem ───────────────────────────────
class Rejestr[T: Urzadzenie]:
    def __init__(self) -> None:
        self._elementy: list[T] = []

    def dodaj(self, element: T) -> None:
        self._elementy.append(element)

    def __iter__(self) -> Iterator[T]:                 # obiekt iterowalny
        return iter(self._elementy)

    def w_pokoju(self, pokoj: str) -> Iterator[T]:     # generator
        for element in self._elementy:
            if element.pokoj == pokoj:
                yield element


# ── Dom: kompozycja – dom MA pokoje i urządzenia ────────────────────────────
class Dom:
    osiedle = "Słoneczne Wzgórze"

    def __init__(self, adres: str) -> None:
        self.adres = adres
        self.pokoje: list[Pokoj] = []
        self.urzadzenia: Rejestr[Urzadzenie] = Rejestr()

    def dodaj_pokoj(self, nazwa: str, metraz: float) -> None:
        self.pokoje.append(Pokoj(nazwa, metraz))

    @property
    def powierzchnia(self) -> float:                   # wyrażenie generatorowe
        return sum(pokoj.metraz for pokoj in self.pokoje)

    def __len__(self) -> int:                          # metody specjalne
        return len(self.pokoje)

    def __iter__(self) -> Iterator[Pokoj]:
        return iter(self.pokoje)

    def __str__(self) -> str:
        return f"🏠 {self.adres} ({self.osiedle}): {len(self)} pokoje, {self.powierzchnia} m²"


# ── Diagnostyka: protokół ───────────────────────────────────────────────────
class ZrodloDiagnostyki(Protocol):
    def status(self) -> str: ...


class StacjaPogodowa:                                  # obca klasa – bez dziedziczenia
    def status(self) -> str:
        return "Stacja pogodowa: 12 °C, bezwietrznie"


def raport(zrodla: Iterable[ZrodloDiagnostyki]) -> None:
    for zrodlo in zrodla:
        print("   🩺", zrodlo.status())


# ── Scena wieczorna: generator ──────────────────────────────────────────────
def wieczorny_obchod(dom: Dom) -> Iterator[str]:
    for pokoj in dom:                                  # dom jest iterowalny
        for urzadzenie in dom.urzadzenia.w_pokoju(pokoj.nazwa):
            urzadzenie.wylacz()                        # polimorfizm
        yield pokoj.nazwa


# ── Uruchomienie ────────────────────────────────────────────────────────────
dom = Dom("ul. Lipowa 7")
dom.dodaj_pokoj("salon", 32.5)
dom.dodaj_pokoj("kuchnia", 14.0)
dom.dodaj_pokoj("sypialnia", 16.5)

dom.urzadzenia.dodaj(Lampa("Lampa sufitowa", "salon", jasnosc=80))
dom.urzadzenia.dodaj(Termostat("Termostat", "salon", 22))
dom.urzadzenia.dodaj(Lampa("Lampka nocna", "sypialnia", jasnosc=20))

print(dom)

print("\n▶ Scena „Powrót do domu”:")
for urzadzenie in dom.urzadzenia:
    urzadzenie.wlacz()

print("\n▶ Diagnostyka:")
raport([*dom.urzadzenia, StacjaPogodowa()])

print("\n▶ Wieczorny obchód:")
for nazwa_pokoju in wieczorny_obchod(dom):
    print(f"   ✔ {nazwa_pokoju}: gotowe do snu")
```

---

### ▶️ Wynik

```
🏠 ul. Lipowa 7 (Słoneczne Wzgórze): 3 pokoje, 63.0 m²

▶ Scena „Powrót do domu”:
   💡 Lampa sufitowa: świecę na 80%
   🌡️ Termostat: grzeję do 22.0 °C
   💡 Lampka nocna: świecę na 20%

▶ Diagnostyka:
   🩺 Lampa sufitowa [salon] – wł.
   🩺 Termostat [salon] – wł., 22.0 °C
   🩺 Lampka nocna [sypialnia] – wł.
   🩺 Stacja pogodowa: 12 °C, bezwietrznie

▶ Wieczorny obchód:
   ⏻  Lampa sufitowa: wyłączam
   ⏻  Termostat: wyłączam
   ✔ salon: gotowe do snu
   ✔ kuchnia: gotowe do snu
   ⏻  Lampka nocna: wyłączam
   ✔ sypialnia: gotowe do snu
```

Zwróć uwagę na kolejność w obchodzie: generator gasi urządzenia w salonie, **zatrzymuje się** na `yield` i oddaje nazwę pokoju pętli, która wypisuje „✔ salon”. Dopiero kolejny obrót pętli **wznawia** generator i prowadzi go do kuchni. Produkcja i konsumpcja przeplatają się krok po kroku.

---

## 🏆 Dobre praktyki

> Zasady, które odróżniają przemyślaną klasę od przypadkowego worka na dane i funkcje.

---

### 🏷️ Nazewnictwo (PEP 8)

|Element|Konwencja|Przykład|
|---|---|---|
|klasy|`PascalCase` (*CapWords*): każde słowo wielką literą, bez podkreśleń|`Dom`, `LampaZGlosnikiem`|
|metody, funkcje, atrybuty, zmienne|`snake_case`: małe litery z podkreśleniami|`dodaj_pokoj`, `kolor_elewacji`|
|stałe (także stałe klasowe)|`WIELKIE_LITERY`|`TRYB_EKO`, `MIN`, `MAX`|
|szczegóły wewnętrzne|wiodące podkreślenie|`_temperatura`, `_adres_ip`|
|pierwszy parametr metody instancji / klasy|`self` / `cls`|`def wlacz(self)`, `def ekologiczny(cls, ...)`|

---

### 📐 Projektowanie klas

1. **Jedna klasa, jedna odpowiedzialność** (*Single Responsibility Principle*). Klasa powinna mieć jeden powód do zmiany. `Dom` zarządza pokojami i urządzeniami, ale **nie** wysyła maili z powiadomieniami — tym niech zajmie się osobna klasa `Powiadomienia`.
2. **Spójność** (*cohesion*). Wszystko w klasie powinno dotyczyć jej głównego celu. `Termostat` ma temperaturę i tryby, ale nie ma metody do opłacania rachunku za prąd.
3. **„Jest” → dziedziczenie, „ma” → kompozycja.** Lampa *jest* urządzeniem; dom *ma* urządzenia. W razie wątpliwości wybierz kompozycję.
4. **Wszystkie atrybuty twórz w `__init__`.** Obiekt powinien być kompletny od chwili narodzin.
5. **Zmienne obiekty nigdy jako zmienne klasy**, chyba że naprawdę mają być wspólne (pułapka z sekcji „Zmienne klasy i zmienne instancji”).
6. **Zaczynaj od zwykłych atrybutów**, a `@property` wprowadzaj dopiero wtedy, gdy potrzebujesz walidacji albo wyliczania.
7. **Zawsze pisz `__repr__`** albo korzystaj z `@dataclass`, który zrobi to za Ciebie.
8. **Kontrakty zapisuj jawnie**: ABC dla własnych hierarchii, protokoły na granicach modułów.
9. **Używaj analizatora typów** (mypy, pyright). Adnotacje bez sprawdzania to tylko komentarze.
10. **Nie komplikuj.** Nie każdy problem wymaga klasy. Jeśli „klasa” ma jedną metodę i `__init__`, być może wystarczy zwykła funkcja.

---

## 📖 Słowniczek PL ⇄ EN

> Polskie terminy z tego rozdziału i ich angielskie odpowiedniki z dokumentacji.

---

|Polski termin|Angielski odpowiednik|
|---|---|
|klasa|*class*|
|obiekt, instancja|*object, instance*|
|obiekt klasy|*class object*|
|atrybut, atrybut danych|*attribute, data attribute*|
|metoda, obiekt metody|*method, method object*|
|inicjalizator|*initializer* (`__init__`)|
|przestrzeń nazw|*namespace*|
|zasięg|*scope*|
|aliasowanie|*aliasing*|
|obiekt zmienny / niezmienny|*mutable / immutable object*|
|zmienna klasy / zmienna instancji|*class variable / instance variable*|
|metoda specjalna|*special method, dunder method*|
|klasa bazowa / klasa pochodna|*base class / derived class*|
|dziedziczenie (wielokrotne)|*(multiple) inheritance*|
|nadpisanie metody|*method overriding*|
|kolejność rozwiązywania metod|*method resolution order (MRO)*|
|domieszka|*mixin*|
|kompozycja|*composition*|
|hermetyzacja|*encapsulation*|
|ukrywanie informacji|*information hiding*|
|przekształcanie nazw|*name mangling*|
|właściwość|*property*|
|metoda klasy / metoda statyczna|*class method / static method*|
|polimorfizm|*polymorphism*|
|typowanie kaczkowe|*duck typing*|
|późne wiązanie|*late binding*|
|klasa abstrakcyjna|*abstract base class (ABC)*|
|protokół|*protocol*|
|typowanie nominalne / strukturalne|*nominal / structural typing*|
|typ generyczny, zmienna typu|*generic type, type variable*|
|górne ograniczenie typu|*upper bound*|
|obiekt iterowalny|*iterable*|
|iterator wyczerpany|*exhausted iterator*|
|generator|*generator*|
|wyrażenie generatorowe|*generator expression*|
|leniwe / zachłanne wartościowanie|*lazy / eager evaluation*|

---

## 📋 Cheat Sheet

> Najważniejsze wzorce z tego rozdziału w jednym miejscu.

---

```python
# ════════════════════════════════════════════
#  KLASA, INSTANCJA, SELF
# ════════════════════════════════════════════

class Dom:
    """Docstring klasy → Dom.__doc__"""

    osiedle = "Słoneczne Wzgórze"        # zmienna klasy – wspólna dla wszystkich

    def __init__(self, adres):           # inicjalizator, wywoływany automatycznie
        self.adres = adres               # zmienna instancji – własna dla obiektu
        self.pokoje = []                 # listy i słowniki ZAWSZE tutaj, nie w klasie

    def przywitaj(self):                 # metoda instancji
        return f"Witaj przy {self.adres}!"

lipowa = Dom("ul. Lipowa 7")             # utworzenie instancji
lipowa.przywitaj()                       # ≡ Dom.przywitaj(lipowa)
vars(lipowa)                             # przestrzeń nazw instancji (__dict__)

# ════════════════════════════════════════════
#  METODY SPECJALNE I DATACLASS
# ════════════════════════════════════════════

def __repr__(self): return f"Dom({self.adres!r})"   # dla programisty – pisz zawsze
def __str__(self):  return f"🏠 {self.adres}"       # dla użytkownika – print()
def __len__(self):  return len(self.pokoje)         # len(dom)
def __eq__(self, inny):                             # dom1 == dom2 (wyłącza hash!)
    if not isinstance(inny, Dom):
        return NotImplemented
    return self.adres == inny.adres

@dataclass                               # __init__, __repr__, __eq__ za darmo
class Pokoj:
    nazwa: str
    metraz: float
    pietro: int = 0

# ════════════════════════════════════════════
#  DZIEDZICZENIE I MRO
# ════════════════════════════════════════════

class Lampa(Urzadzenie):                 # dziedziczenie
    def __init__(self, nazwa, pokoj, jasnosc=100):
        super().__init__(nazwa, pokoj)   # następna klasa w MRO
        self.jasnosc = jasnosc

class LampaZGlosnikiem(Lampa, Glosnik): ...   # dziedziczenie wielokrotne
LampaZGlosnikiem.__mro__                 # kolejność rozwiązywania metod
isinstance(obj, Urzadzenie)              # obiekt klasy lub podklasy?
issubclass(Lampa, Urzadzenie)            # klasa dziedziczy po klasie?

# ════════════════════════════════════════════
#  PRYWATNOŚĆ, WŁAŚCIWOŚCI, RODZAJE METOD
# ════════════════════════════════════════════

self._adres_ip = "..."                   # wewnętrzne – umowa, nie blokada
self.__pin = "4321"                      # name mangling → _Urzadzenie__pin

@property                                # getter: t.temperatura
def temperatura(self): return self._temperatura

@temperatura.setter                      # setter: t.temperatura = 23 (walidacja)
def temperatura(self, wartosc): ...

@classmethod                             # dostaje klasę – alternatywne konstruktory
def ekologiczny(cls, pokoj): return cls(pokoj, cls.TRYB_EKO)

@staticmethod                            # nie dostaje nic – funkcja pomocnicza
def na_fahrenheity(c): return c * 9 / 5 + 32

# ════════════════════════════════════════════
#  KONTRAKTY: ABC, PROTOKOŁY, GENERYKI
# ════════════════════════════════════════════

class Urzadzenie(ABC):                   # klasa abstrakcyjna – nominalna
    @abstractmethod
    def wlacz(self): ...                 # podklasa MUSI zaimplementować

class ZrodloDiagnostyki(Protocol):       # protokół – strukturalny, bez dziedziczenia
    def status(self) -> str: ...

def pierwszy[T](elementy: Sequence[T]) -> T: ...   # funkcja generyczna (3.12+)
class Rejestr[T: Urzadzenie]: ...                 # klasa generyczna z ograniczeniem

# ════════════════════════════════════════════
#  ZASIĘGI (LEGB)
# ════════════════════════════════════════════

global licznik                           # przypisuj w zasięgu modułu
nonlocal kolor                           # przypisuj w funkcji otaczającej
# Local → Enclosing → Global → Built-in; ciało klasy NIE jest w tym łańcuchu

# ════════════════════════════════════════════
#  ITERATORY I GENERATORY
# ════════════════════════════════════════════

it = iter(obiekt)                        # obiekt iterowalny → iterator
next(it)                                 # kolejny element albo StopIteration

class Obchod:                            # własny iterator
    def __iter__(self): return self
    def __next__(self): ...              # raise StopIteration na końcu

def od_konca(dane):                      # generator – funkcja z yield
    for i in range(len(dane) - 1, -1, -1):
        yield dane[i]

yield from podlista                      # oddaj wszystkie elementy podlisty
sum(p.metraz for p in pokoje)            # wyrażenie generatorowe – leniwe
(*pietro for pietro in pietra)           # 3.15+: rozpakowanie (PEP 798)

# ════════════════════════════════════════════
#  ZŁOTE ZASADY
# ════════════════════════════════════════════

# 1. Jedna klasa = jedna odpowiedzialność
# 2. „Jest” → dziedziczenie, „ma” → kompozycja
# 3. Wszystkie atrybuty instancji twórz w __init__
# 4. Listy i słowniki nigdy jako zmienne klasy
# 5. Zawsze pisz __repr__ (albo użyj @dataclass)
# 6. Zwykły atrybut najpierw, @property dopiero gdy potrzeba
# 7. super() zamiast nazwy klasy bazowej
# 8. Kontrakty jawnie: ABC w hierarchii, protokoły na granicach
# 9. Generator, gdy dane są duże, nieskończone albo czytane raz
```

---
