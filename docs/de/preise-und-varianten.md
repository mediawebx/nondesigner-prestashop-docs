[← Inhaltsverzeichnis](README.md) · [← Bestellungen und SVG-Export](bestellungen-und-svg-export.md) · Nächste Seite: [FAQ →](faq.md)

# So verwalten Sie Preise und Varianten personalisierter Produkte mit NonDesigner

## Ändert NonDesigner den Produktpreis?

Nein. Das Modul **NonDesigner** verwaltet **ausschließlich die grafische Oberfläche** und das visuelle Personalisierungserlebnis; es **ändert den Preis des Produkts nicht direkt**.

Alle Preisunterschiede (Zuschläge oder Rabatte für Verarbeitungsoptionen, etwa Vorder-/Rückseitendruck, abgerundete Ecken oder kein Druck) müssen **nativ über die Kombinationen/Varianten von PrestaShop** verwaltet werden.

## Wie lege ich den Preis für Vorder-/Rückseitendruck, abgerundete Ecken oder kein Druck fest? (praktisches Beispiel)

### A. Wie verkaufe ich auch das neutrale Produkt ohne Druck?

Um sowohl das rohe/unbedruckte als auch das personalisierte Produkt anzubieten:

1. Erstellen Sie eine Attributgruppe (z. B. **„Druck"**) und fügen Sie unter deren Werten die Option **„Kein Druck"** (oder „Keine Personalisierung") hinzu.
2. Weisen Sie dem Wert „Kein Druck" den **Grundpreis** des unverarbeiteten Produkts zu.
3. Setzen Sie die Option **Schaltfläche „In den Warenkorb" aktivieren** auf **Ja** (siehe [Produktkonfiguration](produktkonfiguration.md#was-bewirkt-die-option-schaltfläche-in-den-warenkorb-aktivieren)).

### B. Wie lege ich Zuschläge für Druckoptionen fest?

1. Erstellen Sie die Werte für die Druckoptionen (z. B. **„Nur Vorderseitendruck"**, **„Vorder- und Rückseitendruck"**, **„Abgerundete Ecken"**).
2. Legen Sie im Panel **Kombinationen** von PrestaShop die **Preisauswirkung** (Zuschlag) für jede Kombination fest, die eine Verarbeitung beinhaltet.
3. **Ordnen Sie** auf der Registerkarte **NonDesigner** des Produkts die **Attributwerte** den entsprechenden Optionen des Moduls **zu** (z. B. verknüpfen Sie „Vorder- und Rückseitendruck" mit dem Vorder-/Rückseitenmodus des Designers). Siehe [Vorder-/Rückseitendruck](produktkonfiguration.md#wie-richte-ich-den-vorder-rückseitendruck-ein) und [abgerundete Ecken](produktkonfiguration.md#wie-stelle-ich-abgerundete-ecken-ein).

### Ergebnis

Wählt der Kunde die Variante auf der Produktseite **bevor er den Designer öffnet**, berechnet und wendet PrestaShop automatisch den **korrekten Preis im Warenkorb** an.

---

Nächste Seite: [FAQ →](faq.md)
