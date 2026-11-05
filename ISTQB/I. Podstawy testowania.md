### Czym jest testowanie 
Testowanie to kilka procesów:
![[Pasted image 20261104203214.png]]

### Dlaczego jest konieczne 
- ***Pomyłka*** (błąd ludzki) -> ***Defekt*** (bug) -> ***Awaria*** (błędne działanie systemu - nie tylko zależy od defektu, lecz może zależeć od środowiska) 
- ***Analiza przyczyn źródłowych*** (**root cause**) - idziemy od tyłu (Awaria -> Defekt -> Pomyłka)
- ***Testowanie vs QA***
	- **QA** - proces i prewencja - zorientowane na proces - obejmuje również retrospektywy i szkolenia
	- **testowanie** - kontrola jakości (**QC**) - zorientowane na produkt
- ***Wkład w sukces*** - wykrywanie defektów w wymaganiach i kodzie 

### Zasady testowania
- Testy ujawniają defekty, nie dowodzą ich braku (redukowanie prawdopodobieństwa niewykrycia defektów)
- Testy się zużywają (po jakimś czasie nie pokazują nowych defektów, lecz służą dla regresji)
- Testy się kumulują (Pareto - 80% defektów znajduje się w 20% modułów)
- Złudzenie braku defektów (wskazanie defektów oraz ich naprawa wciąż nie świadczą, że system spełnia potrzeby użytkownika)
- Wczesne testy obniżają koszt i oszczędzają czas, w porównaniu do stanu, kiedy defekty są wykryte później
- Testowanie gruntowne jest niemożliwe (np. pole składające się z 10 znaków: dla przetestowania wszystkich kombinacji liter alfabetu łacińskiego daje $26^{10}$ przypadków)
- Testowanie zależy od kontekstu (inaczej się testuje system medyczny, a inaczej grę)

### Pojęcia
- ***Podstawa testów*** - wymagania, historyjki, projekt (w czego wyprowadzamy testy)
- ***Warunek testowy*** - co chcemy sprawdzić
- ***Przypadek testowy*** - warunki wstępne, dane wejściowe, kroki, oczekiwane wyniki, warunki końcowe
- ***Procedura testowa*** - kolejność wykonania 
- ***Testalia*** - produkty pracy testera
- ***Obiekt testowy*** - to co testujemy 
- ***Uprząż testowa***
- ***Środowisko testowe***

### Role
- Rola ***zarządzania testami*** - planowani, monitorowanie, nadzór, zakończenie
- Rola ***testera*** - analiza, projektowanie, implementacja, wykonanie

### Umiejętności i podejście całego zespołu
- ***Wiedza testera*** - wiedza testowa, komunikacja, krytyczne myślenie, wiedza domenowa i techniczna
- ***Podejście całego zespołu*** - jakość jest odpowiedzialnością wszystkich
- ***Niezależność testowania*** - autor testuje własny kod < inny programista < niezależny zespół w organizacji < zewnętrzny
- ***Uprzedzenia poznawcze*** - szukamy dowodów potwierdzających własne przekonania 

