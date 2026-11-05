### Cykl życia, a testowanie
- ***Sekwencyjne*** - poziomy testowania odpowiadają fazom w projekcie, testowanie statyczne wcześniej, dynamiczne później
- ***Iteracyjne-przyrostowe*** - testowanie wraz z przyrostem/sprintami, ważne są tutaj testy regresji
- ***Dobre praktyki*** - testerzy są włączeni od początku, przeglądają nawet roboczą wersję dokumentacji, każdy test ma cel specyficzny to poziomu 
 - ***Test-First***:
	 - **TDD** (Test-Driven-Development) - najpierw powstają testy, które odzwierciedlają oczekiwane działanie, a później jest pisana implementacja, kiedy test przechodzi, można refaktorować kod i używać testów jako mini-regresji
	 - **ATDD** (Acceptance-TDD) - testy akceptacyjne powstają wcześniej, na podstawie **kryteriów akceptacji**
	 - **BDD** (Behavior-Driven-Development) - Zachowanie opisane w formacie Given/When/Then (biznesowo czytelne), a później jest przerobione na testy
- ***Shift-Left*** - testy jak najwcześniej, analiza statyczna
- ***Retrospektywy*** - spotkania po zakończeniu testowania, by podsumować pracę, wyciągnąć wnioski i udoskonalić przyszłe prace/iteracje

### Poziomy testów
- ***Komponentowe*** (Unit) - szczegółowy kod 
- ***Integracji*** - komunikacja między modułami, spójność między komponenetami
- ***Systemowe*** - e2e, środowisko zbliżone do produkcyjnego
- ***Integracji systemów*** - testowanie interfejsów używających zewnętrznych usług
- ***Akceptacyjne*** - walidacja, budowanie zaufania do produktu i jego jakości, wyznaczają gotowość do wdrożenia systemu

### Typy testów
- ***Funkcjonalne*** - sprawdzają czy system działa poprawnie
- ***Niefunkcjonalne*** - sprawdzają czy działa bezpiecznie, dostatecznie szybko, kompatybilność, utrzymywalność, przenośność
- ***Czarnokrzynkowe*** - bez znajomości struktury kodu, na podstawie specyfikacji
- ***Białoskrzynkowe*** - ze struktury kodu, architektury (różne ścieżki)
- ***Potwierdzające*** (retest) - czy dana naprawa zadziałała
- ***Regresji*** - czy nowa zmiana nie wpłynęła na resztę
Każdy z typów testów może wystąpić na każdym poziomie.

### Testowanie utrzymaniowe
- ***Wyzwalacze*** - modyfikacje takie jak: poprawki, ulepszenia, zmiany środowiska, naprawy awaryjne
- ***Migracja/Upgrade*** 
- ***Wycofanie*** - archiwizacja danych
- ***Analiza wpływu*** - wskazuje, jakie obszary zmiana dotyka
