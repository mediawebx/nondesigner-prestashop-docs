# NonDesigner – Benutzerhandbuch und Konfigurationsanleitung (Deutsch)

**NonDesigner** ist ein **PrestaShop-Modul**, das der Produktseite einen **grafischen 2D-Designer** (Produktkonfigurator / Editor) hinzufügt. Kunden fügen Texte, Bilder, Formen, Schriftarten und QR-Codes hinzu, um Produkte online zu personalisieren. Für jede Bestellung erstellt das Modul automatisch **druckfertige Dateien: Vektor-SVG und PNG im Maßstab 1:1**, die direkt über das PrestaShop-Backoffice verwaltet werden können.

- Offizielle Website: [nondesigner.com/de/](https://www.nondesigner.com/de/)
- Demo online: [nondesigner.com/demonondesigner/de/](https://www.nondesigner.com/demonondesigner/de/)
- Kauf auf PrestaShop Addons: [NonDesigner - 2D-Grafikdesigner für personalisierte Produkte](https://addons.prestashop.com/de/produktvarianten/99215-nondesigner-2d-grafikdesigner-fur-personalisierte-produkte.html)
- Entwickler: [Media Web](https://www.mediaweb-x.com/)

🌐 **Sprachen:** Deutsch (dieses Handbuch) · [alle Sprachen](../../README.md)

## Hauptfunktionen

- Grafischer 2D-Designer auf der Produktseite mit einzeln aktivierbaren Panels: Text, Bilder, Formen, Ebenen, QR-Code, Fotofilter, Bildeffekte.
- Automatische Erstellung **druckfertiger Vektor-SVG-Dateien** und **PNG-Dateien (1:1)** für jede eingegangene Bestellung.
- **Vorder-/Rückseitendruck** (nur Vorderseite, Vorder- und Rückseite identisch, Vorder- und Rückseite unterschiedlich).
- **Drei Methoden zur Größenberechnung** des Druckbereichs: feste Abmessungen, separate Attribute (Breite/Höhe) oder gepaarte Werte (B x H).
- Konfigurierbare **Beschnittzugabe**, um weiße Ränder nach dem Zuschnitt zu vermeiden.
- Rechteckige oder runde Produktformen, mit eckigen oder abgerundeten Ecken.
- Schriftarten **lokal auf Ihrem eigenen Server** installiert (kein externes Laden in Echtzeit).
- Native Unterstützung für PrestaShop **Multistore**.
- Automatische (Cronjob) oder manuelle Bereinigung der Designs abgebrochener Warenkörbe.
- Keine Lizenzaktivierung erforderlich.

## Systemanforderungen im Überblick

| Anforderung | Wert |
|---|---|
| Kompatible PrestaShop-Versionen | 1.7.6.1 bis 8.x und 9.x |
| Unterstützte PHP-Versionen | PHP 7.2 bis PHP 8.5 |
| Erforderliche PHP-Erweiterungen | GD Library, cURL, Zip, SimpleXML |
| Empfohlene PHP-Direktiven | `upload_max_filesize` ≥ 10M, `post_max_size` ≥ 10M |

Details: [Systemanforderungen und Installation](installation.md).

## Inhaltsverzeichnis

1. [So installieren Sie das NonDesigner-Modul in PrestaShop](installation.md) – Systemanforderungen, Kompatibilität, Installation.
2. [So konfigurieren Sie das NonDesigner-Modul (globale Einstellungen)](modulkonfiguration.md) – Registerkarten Allgemein, Formenverwaltung, Schriftartenverwaltung, Tool-Konfiguration, Bereinigung abgebrochener Warenkörbe.
3. [So konfigurieren Sie den Designer für ein einzelnes Produkt](produktkonfiguration.md) – Aktivierung, Vorder-/Rückseitendruck, Produktform, PDF-Vorlage, Massenanwendung auf eine Kategorie.
4. [So legen Sie die Druckabmessungen eines Produkts fest](produktabmessungen.md) – Beschnittzugabe und die drei Methoden zur Größenberechnung, akzeptierte Formate und häufige Fehler.
5. [So verwalten Sie Bestellungen und laden druckfertige SVG-Dateien herunter](bestellungen-und-svg-export.md) – Design im Backoffice, SVG- und JSON-Export, Sicherheit.
6. [So verwalten Sie Preise und Varianten personalisierter Produkte](preise-und-varianten.md) – Zuschläge für Vorder-/Rückseitendruck, abgerundete Ecken, Produkt ohne Druck.
7. [Häufig gestellte Fragen (FAQ) und Fehlerbehebung](faq.md).

## Support

Melden Sie sich in Ihrem **PrestaShop Addons**-Konto an, gehen Sie zu **Meine Käufe** und senden Sie eine Nachricht über die Support-Seite des Moduls. Anfragen werden innerhalb von 24–48 Arbeitsstunden beantwortet.

## Wichtiger Hinweis

Erstellen Sie vor der Installation des Moduls eine Sicherung Ihrer Serverdateien und Ihrer Datenbank und testen Sie die Installation nach Möglichkeit zuerst auf einem Testserver.

---

*NonDesigner wird von Media Web entwickelt und vertrieben.*
