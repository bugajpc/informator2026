Jesteś ekspertem ds. projektowania stron internetowych, UX/UI oraz copywritingu nowoczesnych marek.
Twoim zadaniem jest wygenerowanie kompletnego kodu HTML (z wbudowanym CSS w tagu `<style>`) dla statycznej strony informacyjnej (Landing Page) promującej nowy kierunek w szkole.

### Cel:
Strona ma zachować dokładnie ten sam układ, nowoczesny, czysty styl (tzw. "Apple/Vercel Aesthetic"), co zaprezentowany na wzorcu. Opiera się na systemie Grid z frameworka Bootstrap 5 oraz minimalistycznym, "przyjaznym, ale profesjonalnym" designie.

### Wytyczne techniczne oraz wizualne:
1. **Framework:** Wykorzystaj Bootstrap 5 (z CDN). Dodaj responsywność.
2. **Typografia:** Bezszeryfowy krój `Inter` (z Google Fonts, wagi 400, 500, 600, 800). Wyrównuj treść zawsze do lewej strony.
3. **Kolorystyka (Jasny Motyw / Light Mode):**
   - **Tło strony:** Bardzo jasnoszary/off-white (`#fcfcfd`).
   - **Tła komponentów (karty, bloczki):** Śnieżna biel (`#ffffff`), oddzielone bardzo delikatnym obramowaniem (`#f3f4f6`) i subtelnym cieniem (zwiększonym delikatnie przy :hover).
   - **Teksty:** Głęboki kolor tytanowy/grafitowy (`#1a1a1a` dla tytułów, `#4b5563` dla akapitów).
   - **Akcent (Primary Color):** Jasny, elektryczny błękit (`#2563eb`). Używaj go bardzo oszczędnie: na jednym, dwóch najważniejszych słowach w nagłówku, ewentualnie w tagach na samej górze lub jako akcent informacyjny.
4. **Wizualia (Ikony i Obrazy):**
   - **Brak wypunktowań!** Zamiast zwykłych kropek (bullets) - używaj `Bootstrap Icons` w zaokrąglonych, pastelowych tłach.
   - **Zdjęcia (Hero i kody QR):** Zdjęcia główne muszą mieć silnie zaokrąglone brzegi (`border-radius: 24px`) oraz bardzo lekki filtr przyciemniający (`brightness(0.95)`), a kody QR `12px` zaokrąglenia. Ścieżki do obrazów uzupełnij "placeholderami" typu `assets/hero_image.png`, `assets/qr_code.png`.

### Struktura kodu HTML:
1. **Hero Section (Sekcja Główna):**
   - Na górze drobny Tag / Badge z niebieskim tłem, mocno zaokrąglony, zawierający ważny wizualny tekst (np. klasa dwujęzyczna).
   - Nagłówek potężny (Hero Text, waga `800`, ok. `3.8rem` na komputerach, pomniejszony na ekranach mobilnych). Wyizoluj z niego jedno najważniejsze słowo opisujące kierunek i nadaj mu klasę akcentującą kolor (np. `text-accent`).
   - Podtytuł/wstęp (Lead, czytelny rozmiar).
   - Z prawej strony (lub pod spodem na mobile) zajmujące 50% szerokości zdjęcie (img z klasą dodającą cienie i zaokrąglenie).
2. **Atuty (Co nas wyróżnia):**
   - Siatka atutów w formie 2 kolumn i 2 wierszy.
   - Każdy z 4 atutów to kontener obok którego widnieje duża ikona w boksie z jasnoniebieskim tłem. Tytuł obok, zajawka tekstowa poniżej.
   - Jeśli jeden z atutów to długa lista (np. poznawane narzędzia, sprzęt), BEZWZGLĘDNIE zamień je na **Tagi/Pigułki (Pills)**. „Pigułka” to element `display: inline-flex` z okrągłymi brzegami, jasnym tłem, szarym fontem, małą ikonką przed tekstem narzędzia. Zero przecinków, zero litanii teksu.
3. **Kwalifikacje i CTA:**
   - Dwa bloki kart umieszczone u dołu (np. zajmujące 8 kolumn bota) przypominające „panele” posiadające mini tag dla nazwy obwodu ewaluacyjnego (np. `[Kwalifikacja 1]`) i czytelny tekst obok.
   - W kolumnie obok (zajmującej 4 kolumny boxu): Karta "Wezwanie do działania" wyświetlająca kwadratowy kod QR, pogrubiony niebieski tekst skłaniający do podjęcia akcji ("Zeskanuj kod..."), oraz mały podtytuł dla dociekliwych powtarzający istotę strony WWW pod QR kodem.

### Twoje Zadanie:
Wygeneruj dla mnie 1-plikowe, czyste rozwiązanie oparte na powyższym układzie. Zaserwuj mi wyłącznie odpowiedź z całościowym kodem w formacie `<html lang="pl">...`. Zadbaj o estetykę CSS, a zwłaszcza marginesy i padding (korzystaj z klas pomocniczych P/M). 

**Poniżej znajduje się wsad merytoryczny o nowym kierunku/profilu! Zmapuj tę wiedzę na układ podany w wytycznych:**

[WPISZ TUTAJ INFORMACJE O TWOIM NOWYM KIERUNKU]

- PROFIL: (np. Technik Mechatronik / Technik Logistyk / Klasa biologiczno-chemiczna)
- INFO DO GÓRNEGO TAGA: (np. KLASY PATRONACKIE)
- GŁÓWNY SKRÓCONY OPIS: (np. Krótki opis co będą umieć po szkole...)
- 4 GŁÓWNE ATUTY (Co nas wyróżnia): (Wymień 4 atuty, wraz z szeroką listą narzędzi, maszyn lub programów żeby generator stworzył pigułki)
- KWALIFIKACJE LUB TYTUŁY: (Dwie kwalifikacje/korzyści lub nazwy profilowane na koniec szkoły)
- PRZEKAZ DO KODU QR: (Gdzie pokierować skanującego kod np. "Pobierz harmonogram rekrutacji")
