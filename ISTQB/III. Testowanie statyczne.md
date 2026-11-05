### Cechy
- Działania bez uruchomienia kodu, przegląd kodu, analiza statyczna używając narzędzi. Stosowane wszędzie, gdzie da się czytać.
- Ujawnia defekty (kiedy testowanie dynamiczne ujawnia awarie).
- Wykonuje się wcześniej, wiec to się tyczy pojęcia Shift-Left.
- Podczas wykonywania testowania statycznego znajduje się martwy kod, duplikaty, odstępstwa od standardów, luki w bezpieczeństwie, luki w pokryciu, niespójność z wymaganiami.
- Nie znajduje natomiast defektów zależnych w runtime, czyli wydajność, rzeczywisty czas odpowiedzi, nie zastępuje dynamicznego testowania.

### Informacja zwrotna 
Z racji, że testowanie statyczne nie wymaga pisania i uruchomienia kodu oraz, że wykonuje się je od początku, to informacje zwrotne są wczesne oraz dosyć często, zmniejsza ryzyko nieporozumień odnośnie wymagań. 

### Proces przeglądu 
1. ***Planowanie*** - zakres, cel, produkty pracy, szacowanie nadkładu i terminu
2. ***Rozpoczęcie*** - rozdanie materiałów
3. ***Przegląd indywidualny*** - każdy recenzent samodzielnie znajduje anomalie 
4. ***Komunikacja i analiza*** - omówienie anomalii, ocena, status
5. ***Naprawa i raportowanie*** - raporty defektów, naprawy, zbieranie metryk, sprawdzanie kryteriów

### Typy testowania statycznego
- ***Nieformalny*** - brak formalnego procesu, opcjonalne spotkanie
- ***Przejście*** (walkthrough) - prowadzi autor, celami są: ocena jakości, nowe pomysły, sesje scenariuszowe, protokolant jest obowiązkowy
- ***Przegląd techniczny*** - recenzentami są eksperci techniczni
- ***Inspekcja*** - najbardziej formalne, zdefiniowany proces, role, kryteria wejścia i wyjścia, reguły i checklisty, metryki, autor nie może być liderem, ani protokolantem, protokolant jest obowiązkowy

Typ jest dobierany do celu, ryzyka, zasobów i kultury organizacji. 





