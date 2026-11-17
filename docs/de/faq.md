[← Inhaltsverzeichnis](README.md)

# NonDesigner – Häufig gestellte Fragen (FAQ) und Fehlerbehebung

Antworten auf die häufigsten Fragen zum Modul **NonDesigner** für PrestaShop (grafischer 2D-Designer für personalisierte Produkte mit druckfertigen SVG-Dateien).

## Kompatibilität und Anforderungen

### Mit welchen PrestaShop-Versionen funktioniert NonDesigner?
Von PrestaShop **1.7.6.1** bis zu den Versionen **8.x** und **9.x**.

### Welche PHP-Version benötigt NonDesigner?
Unterstützt werden **PHP 7.2 bis 8.5**. Erforderlich sind die Erweiterungen **GD Library, cURL, Zip und SimpleXML**.

### Erfordert NonDesigner eine Lizenzaktivierung?
Nein. Nach der Installation und Konfiguration ist es sofort einsatzbereit. [Details](installation.md).

### Unterstützt NonDesigner den PrestaShop-Multistore?
Ja. Einstellungen, Formen, Schriftarten und die Bereinigung von Designs unterstützen den nativen Multistore; bei mehreren Shops können Sie für jeden unterschiedliche Konfigurationen und Schriftartenkataloge haben. Bei Multistore verhindert eine Kontrolle, dass Designs eines anderen Shops angezeigt oder exportiert werden („Zugriff verweigert").

### Wie geht NonDesigner mit Schriftarten im Hinblick auf die DSGVO um?
Das Modul lädt Schriftarten nicht in Echtzeit von externen Diensten: Es lädt die `.ttf`-Dateien auf Ihren Server herunter und stellt sie lokal bereit. [Details](modulkonfiguration.md#registerkarte-schriftartenverwaltung).

## Druckdateien

### Welche Dateien erzeugt NonDesigner für den Druck?
Für jede eingegangene Bestellung erzeugt es eine **Vektor-SVG**-Datei und ein **PNG im Maßstab 1:1**, die über das Backoffice verwaltet werden. [So laden Sie sie herunter](bestellungen-und-svg-export.md).

### Mit welchem Programm öffne ich die SVG-Dateien von NonDesigner?
Mit **Inkscape** (kostenlos); damit lassen sie sich auch in andere, mit Grafikprogrammen kompatible Formate exportieren.

### Wie vermeide ich weiße Ränder nach dem Zuschneiden des bedruckten Produkts?
Legen Sie die **Beschnittzugabe** fest (üblicherweise 2–3 mm pro Seite; fragen Sie Ihren Druckdienstleister nach dem Wert). [Details](produktabmessungen.md#1-beschnittzugabe-pro-seite-mm).

### Erscheinen die Designs in Bestellbestätigungs-E-Mails?
Nein. Die E-Mail enthält einen Hinweistext zum Vorhandensein eines personalisierten Designs, das im Bestellverlauf des Kundenkontos eingesehen werden kann.

## Häufige Probleme

### Ich lade ein großes Bild hoch, aber das System gibt einen Fehler zurück. Wie behebe ich das?
**Ursache:** Die Dateigröße überschreitet das vom Modul oder vom Server zulässige Limit.

**Lösung:** Überprüfen Sie den Wert unter *Allgemeine Konfiguration → Maximale Bildgröße für Benutzer (MB)*. Ist er korrekt, prüfen Sie zusammen mit Ihrem Hosting-Anbieter die Limits `upload_max_filesize` und `post_max_size` in der `php.ini` Ihres Servers. [Details](modulkonfiguration.md#2-maximale-bildgröße-für-benutzer-mb).

### Die Produktabmessungen werden im Frontend als 0 / 0 gelesen. Wie behebe ich das?
**Ursache:** Sie verwenden die Methode „Separate Attribute" oder „Gepaarte Werte", aber der Attributname/-wert enthält ungültige Zeichen oder mehrere Zahlen, die nicht korrekt getrennt sind.

**Lösung:** Lesen Sie [So legen Sie die Druckabmessungen fest](produktabmessungen.md) erneut. Verwenden Sie für gepaarte Werte den Buchstaben `x` (z. B. `50x70`) und **keine** Bindestriche (`-`) oder Schrägstriche (`/`). Bei separaten Attributen darf jeder Wert nur eine Zahl enthalten.

### Die automatische Bereinigung abgebrochener Warenkörbe startet nicht. Wie behebe ich das?
**Ursache:** Die Cronjob-URL wurde im Serverpanel (cPanel/Plesk) nicht korrekt konfiguriert.

**Lösung:** Kopieren Sie die vollständige URL von der Registerkarte *Tool-Konfiguration* und stellen Sie sicher, dass der Server einen **HTTP-GET**-Aufruf ausführt (z. B. über `wget` oder `curl`). [Details](modulkonfiguration.md#4-bereinigung-von-designs-abgebrochener-warenkörbe).

### Wie verwalte ich Preisunterschiede (Vorder-/Rückseitendruck, abgerundete Ecken, kein Druck)?
NonDesigner ändert den Preis nicht: Verwenden Sie die Kombinationen/Varianten von PrestaShop. [Anleitung mit praktischem Beispiel](preise-und-varianten.md).

### Kann ich den Kauf des Produkts auch ohne Personalisierung ermöglichen?
Ja: Lassen Sie die Option „Schaltfläche In den Warenkorb aktivieren" sichtbar und legen Sie eine Variante „Kein Druck" an. [So geht's](preise-und-varianten.md#a-wie-verkaufe-ich-auch-das-neutrale-produkt-ohne-druck).

## Support

### Wie kontaktiere ich den technischen Support von NonDesigner?
Melden Sie sich in Ihrem **PrestaShop Addons**-Konto an, gehen Sie zu **Meine Käufe** und senden Sie eine Nachricht über die Support-Seite des Moduls. Anfragen werden innerhalb von **24–48 Arbeitsstunden** beantwortet.

---

*Erstellen Sie vor der Installation des Moduls immer eine Sicherung Ihrer Dateien und Ihrer Datenbank und testen Sie es zuerst auf einem Testserver.*
