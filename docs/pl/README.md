# NonDesigner – Podręcznik użytkownika i instrukcja konfiguracji (polski)

**NonDesigner** to **moduł PrestaShop**, który dodaje do strony produktu **kreator graficzny 2D** (edytor / konfigurator personalizacji produktów). Klienci dodają teksty, obrazy, kształty, czcionki i kody QR, aby spersonalizować produkty online, a dla każdego zamówienia moduł automatycznie generuje **pliki gotowe do druku: wektorowy SVG i PNG w skali 1:1**, którymi można zarządzać bezpośrednio z panelu administracyjnego PrestaShop.

- Oficjalna strona: [nondesigner.com/pl/](https://www.nondesigner.com/pl/)
- Demo online: [nondesigner.com/demonondesigner/pl/](https://www.nondesigner.com/demonondesigner/pl/)
- Zakup w PrestaShop Addons: [NonDesigner - Kreator graficzny 2D do spersonalizowanych produktów](https://addons.prestashop.com/pl/warianty-produktow/99215-nondesigner-kreator-graficzny-2d-do-spersonalizowanych-produktow.html)
- Deweloper: [Media Web](https://www.mediaweb-x.com/)

🌐 **Języki:** Polski (ten podręcznik) · [wszystkie języki](../../README.md)

## Najważniejsze funkcje

- Kreator graficzny 2D na stronie produktu, z panelami włączanymi osobno: tekst, obrazy, kształty, warstwy, kod QR, filtry zdjęć, efekty obrazu.
- Automatyczne generowanie **wektorowych plików SVG gotowych do druku** oraz **PNG 1:1** dla każdego otrzymanego zamówienia.
- Druk **przód/tył** (tylko przód, identyczny przód/tył, różny przód/tył).
- **Trzy metody obliczania rozmiaru** obszaru druku: wymiary stałe, odrębne atrybuty (szerokość/wysokość) lub połączone wartości (Sz x W).
- Konfigurowalny **margines spadu**, który zapobiega białym marginesom po przycięciu.
- Kształty produktu prostokątne lub okrągłe, z rogami ostrymi lub zaokrąglonymi.
- Czcionki instalowane **lokalnie na Twoim serwerze** (bez zewnętrznego ładowania w czasie rzeczywistym, zgodność z RODO).
- Natywna obsługa **Multistore** PrestaShop.
- Automatyczne (Cron) lub ręczne czyszczenie projektów z porzuconych koszyków.
- Nie wymaga aktywacji licencji.

## Wymagania systemowe w skrócie

| Wymaganie | Wartość |
|---|---|
| Kompatybilne wersje PrestaShop | od 1.7.6.1 do 8.x i 9.x |
| Obsługiwane wersje PHP | od PHP 7.2 do PHP 8.5 |
| Wymagane rozszerzenia PHP | GD Library, cURL, Zip, SimpleXML |
| Zalecane dyrektywy PHP | `upload_max_filesize` ≥ 10M, `post_max_size` ≥ 10M |

Szczegóły: [Wymagania i instalacja](instalacja.md).

## Spis treści

1. [Jak zainstalować moduł NonDesigner w PrestaShop](instalacja.md) – wymagania systemowe, kompatybilność, instalacja.
2. [Jak skonfigurować moduł NonDesigner (ustawienia globalne)](konfiguracja-modulu.md) – zakładki Ogólne, Zarządzanie kształtami, Zarządzanie czcionkami, Konfiguracja narzędzi, czyszczenie porzuconych koszyków.
3. [Jak skonfigurować kreator przy produkcie](konfiguracja-produktu.md) – aktywacja, druk przód/tył, kształt produktu, szablon PDF, masowe zastosowanie do kategorii.
4. [Jak ustawić wymiary druku produktu](wymiary-produktu.md) – margines spadu i trzy metody obliczania rozmiaru, akceptowane formaty i częste błędy.
5. [Jak zarządzać zamówieniami i pobierać pliki SVG gotowe do druku](zamowienia-i-eksport-svg.md) – projekt w panelu administracyjnym, eksport SVG i JSON, bezpieczeństwo.
6. [Jak zarządzać cenami i wariantami produktów spersonalizowanych](ceny-i-warianty.md) – dopłaty za druk przód/tył, zaokrąglone rogi, produkt bez druku.
7. [Najczęściej zadawane pytania (FAQ) i rozwiązywanie problemów](faq.md).

## Wsparcie

Zaloguj się na swoje konto **PrestaShop Addons**, przejdź do sekcji **Moje zakupy** i wyślij wiadomość z karty wsparcia modułu. Na zgłoszenia odpowiadamy w ciągu 24-48 godzin roboczych.

## Zastrzeżenie

Przed instalacją modułu wykonaj kopię zapasową plików serwera i bazy danych oraz, jeśli to możliwe, najpierw przetestuj instalację na serwerze testowym.

---

*NonDesigner jest tworzony i dystrybuowany przez Media Web.*
