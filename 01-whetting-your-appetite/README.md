## Whetting Your Appetite
*data: -*

```
Python to język programowania, który daje wiele możliwości w perspektywie rozwoju na rok 2026+.

Pythona można używać w wielu obszarach m.in.: 
	⌲ Automatyzacji (Selenium, Scrapy, Beautiful Soup, Playwright, ...)
	⌲ Aplikacji webowych (Django, DRF, FastAPI, Flask, Reflex, ...)
	⌲ AI (TensorFlow, PyTorch, Keras, Scikit-learn, Streamlit(Web UI ), Pydantic AI, ...)
 	⌲ Analizy danych i Data science (Pandas/Polars, NumPy, Matplotlib, Seaborn, ...)
 	⌲ Programowania gier, aplikacji mobilnych i obszarów związanych z DevOps i administracją systemami ...

Ważne pojęcia:

 1. Python jako język interpretowany

 a) Interpreter jest podstawowym narzędziem umożliwiającym wykonywanie kodu w językach skryptowych.

 b) Działa jak tłumacz symultaniczny – na bieżąco przekłada kod napisany przez człowieka na język "zer i jedynek", który rozumie komputer (tłumaczy kod źródłowy języka wysokiego poziomu na sekwencję instrukcji, które mogą być wykonane przez komputer w czasie rzeczywistym).

 c) Interpreter vs Kompilator - interpreter nie generuje pliku binarnego, lecz odczytuje i wykonuje kod linia po linii.

 Wyobraź sobie, że kompilator to tłumacz, który najpierw przekłada całą książkę, a dopiero potem daje Ci gotowy tekst. Interpreter z kolei czyta i tłumaczy "na żywo", zdanie po zdaniu. 

 Python korzysta właśnie z tego drugiego rozwiązania. 
 Dlatego zrozumienie, jak działa ten "tłumacz na żywo", jest kluczem do pisania naprawdę szybkiego kodu w Pythonie.


 Działanie Interpretera w Python'ie:

	Tak Python przetwarza Twój program od momentu jego uruchomienia:

	☞ Dzielenie na słowa (Analiza leksykalna): Python tnie Twój kod na najmniejsze sensowne kawałki (tzw. tokeny). 
	Oddziela od siebie komendy, nazwy zmiennych, liczby i nawiasy, żeby wiedzieć, z czym ma do czynienia.

	☞ Układanie mapy logiki (Analiza składniowa): Z tych małych kawałków tworzony jest schemat programu (drzewo AST). 
	Na tym etapie Python uczy się zaleceń – np. rozumie, że konkretna grupa słów to pętla, a inna to definicja funkcji.

	☞ Tworzenie uniwersalnego półproduktu (Kompilacja do bytecode'u): Schemat programu jest tłumaczony na bytecode – wewnętrzny, uproszczony język Pythona. Dzięki temu Twój program zadziała na każdym komputerze, niezależnie od tego, 
	czy to Windows, Mac, czy Linux.

	☞ Właściwe działanie (Wykonanie przez PVM): Do akcji wkracza "silnik" Pythona (czyli maszyna wirtualna PVM). 
	Odczytuje on gotowy bytecode instrukcja po instrukcji i po prostu wykonuje Twoje polecenia, zarządzając przy tym pamięcią komputera.


 2. Python a wysoko-poziomowe typy danych

	❖ Zgadywanie typów "w locie": W Pythonie nie musisz z góry określać, czy zmienna przechowuje tekst, czy liczbę. Interpreter sam to rozpoznaje w trakcie działania programu i w razie potrzeby automatycznie dopasowuje formaty.

	❖ Automatyczne sprzątanie pamięci: Python sam dba o porządek w pamięci komputera. Działa to jak system "liczników popularności" – system liczy, w ilu miejscach w kodzie dany element jest używany. Gdy dany obiekt przestaje być komukolwiek potrzebny (licznik spada do zera), Python automatycznie go usuwa.

	❖ Radzenie sobie z zapętleniami: Czasami dwa niepotrzebne obiekty wskazują nawzajem na siebie. Python ma specjalny mechanizm (moduł gc), który wykrywa takie "zamknięte kółka" i też je usuwa, by nie blokowały pamięci.

	❖ Koszty wygody: Chociaż takie automatyczne rozpoznawanie typów jest wygodne i bezpieczne, może zwalniać działanie programu (szczególnie przy dużych ilościach danych). Dlatego Python stosuje w tle różne sztuczki optymalizacyjne – np. trzyma często używane rzeczy w szybkiej pamięci podręcznej.

 3. Dodatkowe informacje:

 	Zarządzanie funkcjami (Stos wywołań): kiedy program uruchamia funkcję, dodaje ją na szczyt specjalnej listy 
 	(tzw. stosu). Każda funkcja otrzymuje tam swoją własną, odizolowaną przestrzeń na tymczasowe zmienne. 
 	Gdy skończy zadanie, jest natychmiast usuwana z listy, dzięki czemu jej dane są bezpieczne 
 	i nie mieszają się zresztą programu.

	Ładowanie modułów: Python doczytuje dodatkowe pliki z kodem w locie. 
	Aby przyspieszyć ten proces w przyszłości, od razu tłumaczy je na szybszy format (pliki .pyc) i zachowuje w pamięci podręcznej. 
	Dodatkowo każdy moduł działa w swojej własnej, zamkniętej strefie, co zapobiega konfliktom nazw 
	(np. gdy dwie różne wtyczki mają funkcję o tej samej nazwie).

	Obsługa błędów: gdy w kodzie wystąpi niespodziewany błąd, Python zaczyna cofać się krok po kroku po wspomnianym 
	"stosie wywołań". Szuka po drodze instrukcji ratunkowej (bloku try-except). 
	Jeśli ją znajdzie, wykonuje plan awaryjny. 
	Jeśli przeszuka wszystko i nic nie znajdzie – zatrzymuje program i wyświetla komunikat o błędzie.


Ciekawostki:

 Autorzy:

" Swoją drogą, nazwa języka pochodzi od programu BBC „Latający Cyrk Monty Pythona” i nie ma nic wspólnego z gadami. Tworzenie odniesień do skeczy Monty Pythona w dokumentacji jest nie tylko dozwolne, wręcz do tego zachęcamy!"


```
---

