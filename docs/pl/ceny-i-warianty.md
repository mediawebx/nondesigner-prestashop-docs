[← Indeks](README.md) · [← Zamówienia i eksport SVG](zamowienia-i-eksport-svg.md) · Następna strona: [FAQ →](faq.md)

# Jak zarządzać cenami i wariantami produktów spersonalizowanych za pomocą NonDesigner

## Czy NonDesigner zmienia cenę produktu?

Nie. Moduł **NonDesigner** zarządza **wyłącznie interfejsem graficznym** i doświadczeniem personalizacji wizualnej; **nie zmienia bezpośrednio ceny** produktu.

Wszystkie różnice cenowe (dopłaty lub rabaty za opcje obróbki, takie jak druk dwustronny, zaokrąglone rogi lub brak druku) muszą być zarządzane **natywnie za pomocą kombinacji/wariantów PrestaShop**.

## Jak ustawić cenę druku przód/tył, zaokrąglonych rogów lub braku druku? (przykład praktyczny)

### A. Jak sprzedawać także produkt neutralny bez druku?

Aby oferować zarówno produkt surowy/niezadrukowany, jak i spersonalizowany:

1. Utwórz grupę atrybutów (np. **„Druk"**) i dodaj wśród jej wartości opcję **„Bez druku"** (lub „Brak personalizacji").
2. Przypisz wartości „Bez druku" **cenę bazową** nieobrobionego produktu.
3. Ustaw opcję **Włącz przycisk „Dodaj do koszyka"** na **Tak** (zobacz [Konfiguracja produktu](konfiguracja-produktu.md#co-robi-opcja-włącz-przycisk-dodaj-do-koszyka)).

### B. Jak ustawić dopłaty za opcje druku?

1. Utwórz wartości dla opcji druku (np. **„Druk tylko z przodu"**, **„Druk dwustronny"**, **„Zaokrąglone rogi"**).
2. W panelu **Kombinacje** PrestaShop ustaw **wpływ na cenę** (dopłatę) dla każdej kombinacji wymagającej obróbki.
3. W zakładce **NonDesigner** produktu **przypisz wartości atrybutu** do odpowiadających im opcji modułu (np. powiąż „Druk dwustronny" z trybem przód/tył kreatora). Zobacz [druk przód/tył](konfiguracja-produktu.md#jak-skonfigurować-druk-przódtył) i [zaokrąglone rogi](konfiguracja-produktu.md#jak-skonfigurować-zaokrąglone-rogi).

### Rezultat

Gdy klient wybierze wariant na stronie produktu **przed otwarciem kreatora**, PrestaShop automatycznie obliczy i zastosuje **prawidłową cenę w koszyku**.

---

Następna strona: [FAQ →](faq.md)
