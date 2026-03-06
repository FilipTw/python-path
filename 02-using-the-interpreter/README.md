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
├── 02-using-the-interpreter/
│   ├── notes.py
│   └── README.md
```

---

## 📝 Notatki

Wszystkie przemyślenia i skróty myślowe z każdych zagadnień w [NOTES.md](./NOTES.md)

---

# Wiedza Teoretyczna Rozdziału Using The Interpreter

---

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