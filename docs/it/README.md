# NonDesigner – Documentazione ufficiale del modulo PrestaShop

**NonDesigner** è un modulo per **PrestaShop** che aggiunge alla scheda prodotto un **disegnatore grafico 2D** (editor/customizer) con cui i clienti personalizzano i prodotti online: testo, immagini, forme, font, QR-Code, ombre, effetti. Per ogni ordine il modulo genera automaticamente i **file pronti per la stampa**: **SVG vettoriale** e **PNG in scala 1:1**, scaricabili dal Back Office di PrestaShop.

Questo repository contiene la **documentazione pubblica** (guida utente e manuale di configurazione) del modulo.

- Sito ufficiale: [nondesigner.com](https://www.nondesigner.com/)
- Demo online: [nondesigner.com/demonondesigner/it/](https://www.nondesigner.com/demonondesigner/it/)
- Acquisto su PrestaShop Addons: [NonDesigner – Disegnatore grafico 2D per prodotti personalizzati](https://addons.prestashop.com/it/varianti-di-prodotto/99215-nondesigner-disegnatore-grafico-2d-per-prodotti-personalizzati.html)
- Sviluppatore: [Media Web](https://www.mediaweb-x.com/)

🌐 **Lingue:** Italiano (questa documentazione) · [tutte le lingue](../../README.md)

## Funzionalità principali

- Editor grafico 2D nella scheda prodotto, con pannelli attivabili singolarmente: testo, immagini, forme, livelli, QR-Code, filtri foto, effetti immagine.
- Generazione automatica di file **SVG vettoriali pronti per la stampa** e **PNG 1:1** per ogni ordine ricevuto.
- Stampa **fronte/retro** (solo fronte, fronte/retro identici, fronte/retro differenti).
- **Tre metodi di dimensionamento** dell'area di stampa: dimensioni fisse, attributi distinti (larghezza/altezza) o valori accoppiati (L x A).
- **Margine di abbondanza** configurabile per evitare bordi bianchi dopo il taglio.
- Sagome del prodotto rettangolari o circolari, con angoli quadrati o arrotondati.
- Catalogo di font installati **localmente sul tuo server** (nessun caricamento esterno dei font in tempo reale).
- Supporto **Multinegozio** nativo di PrestaShop.
- Pulizia automatica (Cron) o manuale dei design dei carrelli abbandonati.
- Nessuna attivazione di licenza richiesta.

## Requisiti in breve

| Requisito | Valore |
|---|---|
| Versioni PrestaShop compatibili | da 1.7.6.1 a 8.x e 9.x |
| Versioni PHP supportate | da 7.2 a 8.5 |
| Estensioni PHP richieste | GD Library, cURL, Zip, SimpleXML |
| Direttive PHP consigliate | `upload_max_filesize` ≥ 10M, `post_max_size` ≥ 10M |

Dettagli: [Requisiti e installazione](installazione.md).

## Indice della documentazione (italiano)

1. [Come installare il modulo NonDesigner su PrestaShop](installazione.md) – requisiti di sistema, compatibilità, installazione.
2. [Come configurare il modulo NonDesigner (impostazioni globali)](configurazione-modulo.md) – schede Generale, Gestione Forme, Gestione Caratteri, Configurazione Strumenti, pulizia dei carrelli abbandonati.
3. [Come configurare il disegnatore su un singolo prodotto](configurazione-prodotto.md) – abilitazione, fronte/retro, sagoma, modello PDF, applicazione in blocco a una categoria.
4. [Come impostare le dimensioni di stampa del prodotto](dimensioni-prodotto.md) – margine di abbondanza e i tre metodi di dimensionamento con formati accettati ed errori comuni.
5. [Come gestire gli ordini e scaricare i file SVG pronti per la stampa](ordini-e-esportazione-svg.md) – design nel Back Office, esportazione SVG, JSON, sicurezza.
6. [Come gestire prezzi e varianti dei prodotti personalizzati](prezzi-e-varianti.md) – sovrapprezzi per fronte/retro, angoli arrotondati, prodotto senza stampa.
7. [Domande frequenti (FAQ) e risoluzione problemi](faq.md).

## Assistenza

Per supporto: accedi al tuo account **PrestaShop Addons** → **I miei acquisti** → invia un messaggio dalla scheda di supporto del modulo. Le richieste ricevono risposta entro 24–48 ore lavorative.

## Nota importante

Prima di installare il modulo, esegui un backup dei file del server e del database e, se possibile, prova l'installazione su un server di test.

---

*NonDesigner è sviluppato e distribuito da Media Web.*
