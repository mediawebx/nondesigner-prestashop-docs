[← Indeks](README.md)

# NonDesigner – Najczęściej zadawane pytania (FAQ) i rozwiązywanie problemów

Odpowiedzi na najczęstsze pytania dotyczące modułu **NonDesigner** dla PrestaShop (kreator graficzny 2D do spersonalizowanych produktów z plikami SVG gotowymi do druku).

## Kompatybilność i wymagania

### Z jakimi wersjami PrestaShop działa NonDesigner?
Od PrestaShop **1.7.6.1** do wersji **8.x** i **9.x**.

### Jakiej wersji PHP wymaga NonDesigner?
Obsługiwane są wersje **PHP od 7.2 do 8.5**. Wymagane są rozszerzenia **GD Library, cURL, Zip i SimpleXML**.

### Czy NonDesigner wymaga aktywacji licencji?
Nie. Po zainstalowaniu i skonfigurowaniu jest natychmiast gotowy do użytku. [Szczegóły](instalacja.md).

### Czy NonDesigner jest kompatybilny z Multistore PrestaShop?
Tak. Ustawienia, kształty, czcionki i czyszczenie projektów obsługują natywny Multistore; przy kilku sklepach możesz mieć różne konfiguracje i katalogi czcionek dla każdego z nich. W Multistore mechanizm kontroli uniemożliwia wyświetlenie lub eksport projektów z innego sklepu („Odmowa dostępu").

### Jak NonDesigner obsługuje czcionki w kontekście RODO?
Moduł nie ładuje czcionek z zewnętrznych usług w czasie rzeczywistym: pobiera pliki `.ttf` na Twój serwer i udostępnia je lokalnie. [Szczegóły](konfiguracja-modulu.md#zakładka-zarządzanie-czcionkami).

## Pliki do druku

### Jakie pliki generuje NonDesigner do druku?
Dla każdego otrzymanego zamówienia generuje **wektorowy plik SVG** i **PNG w skali 1:1**, zarządzane z panelu administracyjnego. [Jak je pobrać](zamowienia-i-eksport-svg.md).

### Jakim programem otworzyć pliki SVG z NonDesigner?
Programem **Inkscape** (darmowy), który umożliwia też eksport do innych formatów zgodnych z programami graficznymi.

### Jak uniknąć białych marginesów po przycięciu zadrukowanego produktu?
Ustaw **margines spadu** (zazwyczaj 2-3 mm na stronę; zapytaj o wartość swojego dostawcę usług drukarskich). [Szczegóły](wymiary-produktu.md#1-margines-spadu-na-stronę-mm).

### Czy projekty pojawiają się w e-mailach z potwierdzeniem zamówienia?
Nie. E-mail zawiera tekst informujący o obecności spersonalizowanego projektu, dostępnego do przeglądania w historii zamówień konta klienta.

## Częste problemy

### Przesyłam duży obraz, ale system zwraca błąd. Jak to rozwiązać?
**Przyczyna:** rozmiar pliku przekracza limit dozwolony przez moduł lub serwer.

**Rozwiązanie:** sprawdź wartość ustawioną w *Konfiguracja Ogólna → Maksymalny rozmiar obrazu użytkownika (MB)*. Jeśli jest prawidłowa, sprawdź razem ze swoim dostawcą hostingu limity `upload_max_filesize` i `post_max_size` w pliku `php.ini` serwera. [Szczegóły](konfiguracja-modulu.md#2-maksymalny-rozmiar-obrazu-użytkownika-mb).

### Wymiary produktu są odczytywane jako 0 / 0 we frontendzie. Jak to rozwiązać?
**Przyczyna:** korzystasz z metody „Odrębne atrybuty" lub „Połączone wartości", ale nazwa/wartość atrybutu zawiera nieprawidłowe znaki lub kilka liczb nieprawidłowo oddzielonych.

**Rozwiązanie:** zapoznaj się ponownie z [Jak ustawić wymiary druku](wymiary-produktu.md). Dla połączonych wartości używaj litery `x` (np. `50x70`) i **nie** stosuj myślników (`-`) ani ukośników (`/`). Dla odrębnych atrybutów każda wartość musi zawierać jedną liczbę.

### Automatyczne czyszczenie porzuconych koszyków nie uruchamia się. Jak to rozwiązać?
**Przyczyna:** URL zadania Cron nie został prawidłowo skonfigurowany w panelu serwera (cPanel/Plesk).

**Rozwiązanie:** skopiuj pełny URL wyświetlany w zakładce *Konfiguracja narzędzi* i upewnij się, że serwer wykonuje wywołanie **HTTP GET** (np. za pomocą `wget` lub `curl`). [Szczegóły](konfiguracja-modulu.md#4-czyszczenie-projektów-z-porzuconych-koszyków).

### Jak zarządzać różnicami cenowymi (przód/tył, zaokrąglone rogi, brak druku)?
NonDesigner nie zmienia ceny: użyj kombinacji/wariantów PrestaShop. [Przewodnik z przykładem praktycznym](ceny-i-warianty.md).

### Czy mogę umożliwić zakup produktu bez personalizacji?
Tak: zostaw widoczną opcję „Włącz przycisk Dodaj do koszyka" i utwórz wariant „Bez druku". [Jak to zrobić](ceny-i-warianty.md#a-jak-sprzedawać-także-produkt-neutralny-bez-druku).

## Wsparcie

### Jak skontaktować się z pomocą techniczną NonDesigner?
Zaloguj się na swoje konto **PrestaShop Addons**, przejdź do sekcji **Moje zakupy** i wyślij wiadomość z karty wsparcia modułu. Zgłoszenia są obsługiwane w ciągu **24-48 godzin roboczych**.

---

*Przed instalacją modułu zawsze wykonaj kopię zapasową plików i bazy danych oraz najpierw przetestuj go na serwerze testowym.*
