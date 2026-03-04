Jesteś ekspertem ds. projektowania do druku (DTP) i stron wizytówkowych.
Twoim zadaniem jest wygenerowanie kompletnego kodu HTML (z wbudowanym CSS w tagu `<style>`) dla statycznej ulotki informacyjnej promującej nowy kierunek w szkole. Strona ma być optymalizowana do wydruku w formacie A5 (zapis do PDF).

### Cel:
Strona ma zachować czytelny, nowoczesny układ opierając się na systemie Grid z frameworka Bootstrap 5, ale ułożony tak, by zmieścić się na jednej kartce A5 (148mm × 210mm) pionowo.

### Wytyczne techniczne oraz wizualne:
1. **Format:** Wykorzystaj Bootstrap 5 (z CDN) opierając layout w znacznej mierze na kolumnach typu `col-6`, `col-12`, `col-7`, `col-5` (zamiast np. `col-md-6`), unikając tym samym łamania layoutu na małym ekranie. Zdefiniuj w CSS `@page { size: A5; margin: 0; }` oraz na elemencie `body`: `width: 148mm; height: 210mm; font-size: 10px; margin: 0 auto; box-sizing: border-box; overflow: hidden; padding: 8mm; -webkit-print-color-adjust: exact !important; print-color-adjust: exact !important;`. To bardzo ważne żeby drukarka zapisała kolory tła!
2. **Cienie i Animacje:** Ze względu na zapis bezpośrednio do pliku PDF, **bezwzględnie zrezygnuj** z jakichkolwiek animacji (`transition`), cieni (`box-shadow`) i zachowań po najechaniu myszką (`:hover`). Skup się na płaskim designie.
3. **Typografia:** Bezszeryfowy krój `Inter` (z Google Fonts). Wyrównuj treść zawsze do lewej strony. Rozmiary fontów na A5 muszą być mniejsze niż na standardowej WWW (np. `10px` tekst bazowy, `26px` hero nagłówek).
4. **Kolorystyka:**
   - **Pure White (`#FFFFFF`):** Background - Główne tło dokumentu (`body`). 
   - **Deep Ocean (`#134659`):** Primary - Główne Nagłówki (tytuły h1-h6), reszta nazwy kierunku, ikony list atutów, małe tytuły sekcji i badge tagowe na dole (np. w bloku kwalifikacji).
   - **Tech Cyan (`#06B6D4`):** Secondary Accent - Wykorzystany WYŁĄCZNIE do pokolorowania jednego kluczowego słowa w nagłówku H1, czyli docelówki zawodowej (np. słowo "PROGRAMISTA", "INFORMATYK"). Nadaj mu tag z klasą (np. `.text-profession`).
   - **Energy Red (`#D9231D`):** Accent - Zarezerwowany WYŁĄCZNIE dla głównych tagów na samej górze (np. "Nowość", "Klasa dwujęzyczna", "Jedyny w Polsce"). Nie używaj go do wyróżniania fragmentów nagłówka ani dla ikon.
   - **Soft Cloud (`#F0F4F8`):** Neutral - Tła wokół ikon przy atutach, tła "pigułek" narzędziowych (tech-pill), a także jako wypełnienie tła okienek Kwalifikacji i Karty QR na spodzie. Wszystkie obiekty i pudełka posiadające to tło **muszą posiadać cienkie, delikatne obramowanie** (np. `border: 1px solid #E2E8F0;`), aby projekt nie był płaski i ładnie odcinał się od białego tła w wydruku.
   - **Steel Text (`#2D3748`):** Typography - Teksty akapitów, główny czytelny font opisów.
5. **Wizualia (Ikony i Obrazy):**
   - Zamiast wypunktowań (UL/LI) stosuj ikony `Bootstrap Icons`. Obfite listy narzędzi zmieniaj na tzw. "pigułki" (pill) - szarjasne tło (`Soft Cloud`), zaokrąglone krawędzie, układając je ciasno obok siebie (`d-flex flex-wrap`).
   - Zdjęcia i kody QR: Mogą mieć zaokrąglone krawędzie (np. `8px`), ale **bez żadnych cieni** i żadnego filtra przyciemniajacego. Oczekiwane zdjęcie hero powinno być wygenerowane sztuczną inteligencją: eleganckie, z pozytywnym nastrojem, nawiązujące do branży i sprzętu o którym mowa w opisie. Powinno mieć wyraźną głębię ostrości w tle (rozmycie), bez zbytniego skupiania widoku na szczegołowych twarzach ludzkich.

### Struktura wielkości (Bootstrap Grid na A5):
1. **Hero:** U góry w `row` po lewej stronie `col-6`: Nagłówek potężny H1 (główna treść w Deep Ocean, a docelowe stanowisko zawodu wydzielone w `span` i zabarwione na Tech Cyan). Zaraz pod nagłówkiem umieść ewentualny Tag/Badge informujący o *Patronacie* (tło ciemno-szare, margines w dół). Pod tagiem z patronatem wstaw wstęp, który musi być bogaty w treść - koniecznie użyj większej ilości tekstu z oryginalnego wsadu. Po prawej `col-6`: dopasowane tematyczne zdjęcie z AI (zgodne z wizualiami), a **bezpośrednio pod nim** umieść od prawej strony Główne Tagi w kolorze `Energy Red` (np. "Nowość", "Jedyny w Polsce" używając klas ułatwiających wyrównanie do prawej: np. `d-flex justify-content-end flex-wrap mt-2`).
2. **Atuty:** Poniżej `h2` ("Co nas wyróżnia" w Deep Ocean), a pod tym 2 kolumny po 2 atuty, każdy po `col-6` jeden obok drugiego. Tworzymy siatkę w rzędzie (`row`). Każdy atut zaczyna się ikoną (`Deep Ocean` na tle `Soft Cloud`), tytuł (`Deep Ocean`). Pod tytułem zamieść wyczerpujący opis w 2-3 zdaniach, z wykorzystaniem treści. Na samym dole atutu długa lista narzędzi jest zamknięta w małe pigułki (`Soft Cloud`).
3. **Kwalifikacje i CTA:** Umieszczone na dole strony. Po lewej okienko zajmujące `col-7` z dwoma kwalifikacjami wewnątrz. Po prawej `col-5` zajmuje Karta "Zeskanuj kod QR" namawiająca do rekrutacji (na tle `Soft Cloud`, teksty w Deep Ocean).

### Twoje Zadanie:
Wygeneruj 1-plikowe, czyste rozwiązanie oparte na powyższym układzie. Zaserwuj mi odpowiedź wyłącznie z całościowym plikiem w formacie `<html lang="pl">...`. Bez owijania w bawełnę ale profesjonalnie. Zadbaj o estetykę CSS, czystości marginesów (`px-0`, wyłączeniu breakpointów na kolumnach - dawaj na twardo `col-6`).

**Zmapuj poniższe informacje o nowym kierunku:**

[WPISZ TUTAJ INFORMACJE O TWOIM NOWYM KIERUNKU]

- PROFIL: (np. Technik Mechatronik / Technik Logistyk / Klasa biologiczno-chemiczna)
- INFO DO GÓRNEGO TAGA: (np. KLASY PATRONACKIE)
- GŁÓWNY SKRÓCONY OPIS: (np. Krótki opis co będą umieć po szkole...)
- 4 GŁÓWNE ATUTY (Co nas wyróżnia): (Wymień 4 atuty, wraz z szeroką listą narzędzi na "pigułki")
- KWALIFIKACJE LUB TYTUŁY: (Dwie kwalifikacje na koniec szkoły)
- PRZEKAZ DO KODU QR: (Gdzie pokierować skanującego kod np. "Pobierz harmonogram")
