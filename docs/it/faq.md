[← Indice](README.md)

# NonDesigner – Domande frequenti (FAQ) e risoluzione problemi

Risposte alle domande più comuni sul modulo **NonDesigner** per PrestaShop (disegnatore grafico 2D per prodotti personalizzati con file SVG pronti per la stampa).

## Compatibilità e requisiti

### Con quali versioni di PrestaShop funziona NonDesigner?
Da PrestaShop **1.7.6.1** fino alle versioni **8.x** e **9.x**.

### Quale versione di PHP serve per NonDesigner?
Sono supportate le versioni da **PHP 7.2 a PHP 8.5**. Servono le estensioni **GD Library, cURL, Zip e SimpleXML**.

### NonDesigner richiede una licenza da attivare?
No. Una volta installato e configurato è subito operativo. [Dettagli](installazione.md).

### NonDesigner supporta il Multinegozio di PrestaShop?
Sì. Impostazioni, forme, font e pulizia dei design supportano il Multinegozio nativo; con più negozi puoi avere configurazioni e cataloghi di font diversi per ciascuno. In Multinegozio un controllo impedisce di visualizzare o esportare i design di un altro negozio ("Accesso Negato").

### NonDesigner rispetta il GDPR per i font?
Il modulo non carica i font da servizi esterni in tempo reale: scarica i file `.ttf` sul tuo server e li serve localmente. [Dettagli](configurazione-modulo.md#scheda-gestione-caratteri).

## File di stampa

### Quali file genera NonDesigner per la stampa?
Per ogni ordine ricevuto genera un file **SVG vettoriale** e un **PNG in scala 1:1**, gestibili dal Back Office. [Come scaricarli](ordini-e-esportazione-svg.md).

### Con quale programma apro i file SVG di NonDesigner?
Con **Inkscape** (gratuito), che permette anche di esportarli in altri formati compatibili con i programmi di grafica.

### Come evito i bordi bianchi dopo il taglio del prodotto stampato?
Imposta il **margine di abbondanza** (di solito 2–3 mm per lato, chiedi il valore al tuo fornitore di stampa). [Dettagli](dimensioni-prodotto.md#1-margine-di-abbondanza-per-lato-mm).

### Le immagini dei design compaiono nelle email di conferma ordine?
No. Nell'email compare un testo che segnala la presenza di un design personalizzato, consultabile nella cronologia ordini dell'account cliente.

## Problemi comuni

### Carico un'immagine di grandi dimensioni ma il sistema restituisce errore. Come risolvo?
**Causa:** la dimensione del file supera il limite del modulo o del server.

**Soluzione:** controlla il valore in *Configurazione Generale → Dimensione massima immagine utente (MB)*. Se è corretto, verifica con il tuo hosting i limiti `upload_max_filesize` e `post_max_size` nel `php.ini` del server. [Dettagli](configurazione-modulo.md#2-dimensione-massima-immagine-utente-mb).

### Le dimensioni del prodotto vengono lette come 0 / 0 nel frontend. Come risolvo?
**Causa:** stai usando il metodo "Attributi distinti" o "Valori accoppiati" ma il nome/valore dell'attributo contiene caratteri non validi o più numeri non separati correttamente.

**Soluzione:** rileggi [Come impostare le dimensioni di stampa](dimensioni-prodotto.md). Per i valori accoppiati usa la lettera `x` (es. `50x70`) e **non** trattini (`-`) o slash (`/`). Per gli attributi distinti ogni valore deve contenere un solo numero.

### La pulizia automatica dei carrelli abbandonati non si avvia. Come risolvo?
**Causa:** l'URL del cronjob non è configurato correttamente nel pannello del server (cPanel/Plesk).

**Soluzione:** copia l'URL completo dalla scheda *Configurazione Strumenti* e assicurati che il server esegua una chiamata **HTTP GET** (es. tramite `wget` o `curl`). [Dettagli](configurazione-modulo.md#4-pulizia-dei-design-dei-carrelli-abbandonati).

### Come gestisco le variazioni di prezzo (fronte/retro, angoli arrotondati, nessuna stampa)?
NonDesigner non modifica il prezzo: usa le Combinazioni/Varianti di PrestaShop. [Guida con esempio pratico](prezzi-e-varianti.md).

### Posso lasciare acquistare il prodotto anche senza personalizzazione?
Sì: lascia visibile l'opzione "Abilita il pulsante Aggiungi al carrello" e crea una variante "Nessuna stampa". [Come fare](prezzi-e-varianti.md#a-come-vendere-anche-il-prodotto-neutro-senza-stampa).

## Assistenza

### Come contatto il supporto tecnico di NonDesigner?
Accedi al tuo account **PrestaShop Addons**, vai in **I miei acquisti** e invia un messaggio dalla scheda di supporto del modulo. Le richieste ricevono risposta entro **24–48 ore lavorative**.

---

*Prima di installare il modulo esegui sempre un backup di file e database, e provalo su un server di test.*
