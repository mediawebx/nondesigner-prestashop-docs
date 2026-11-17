[← Indice](README.md) · [← Ordini ed esportazione SVG](ordini-e-esportazione-svg.md) · Prossima pagina: [FAQ →](faq.md)

# Come gestire prezzi e varianti dei prodotti personalizzati con NonDesigner

## NonDesigner modifica il prezzo del prodotto?

No. Il modulo **NonDesigner** gestisce **esclusivamente l'interfaccia grafica** e l'esperienza visiva di personalizzazione; **non modifica direttamente il prezzo** del prodotto.

Tutte le variazioni di prezzo (sovrapprezzi o sconti per le lavorazioni, ad esempio stampa fronte/retro, angoli arrotondati o nessuna stampa) vanno gestite con le **Combinazioni/Varianti native di PrestaShop**.

## Come impostare il prezzo per stampa fronte/retro, angoli arrotondati o nessuna stampa? (esempio pratico)

### A. Come vendere anche il prodotto neutro "senza stampa"?

Per offrire sia il prodotto grezzo/neutro sia quello personalizzato:

1. Crea un gruppo attributo (es. **"Stampa"**) e inserisci tra i suoi valori l'opzione **"Nessuna stampa"** (o "Senza personalizzazione").
2. Assegna al valore "Nessuna stampa" il **prezzo base** del prodotto non lavorato.
3. Imposta l'opzione **Abilita il pulsante "Aggiungi al carrello"** su **Sì** (vedi [Configurazione del prodotto](configurazione-prodotto.md#cosa-fa-lopzione-abilita-il-pulsante-aggiungi-al-carrello)).

### B. Come impostare i sovrapprezzi per le lavorazioni di stampa?

1. Crea i valori per le opzioni stampate (es. **"Stampa Solo Fronte"**, **"Stampa Fronte e Retro"**, **"Angoli Arrotondati"**).
2. Nel pannello **Combinazioni** di PrestaShop imposta l'**impatto sul prezzo** (sovrapprezzo) per ciascuna combinazione con lavorazione.
3. Nella scheda **NonDesigner** del prodotto **mappa i valori dell'attributo** sulle opzioni corrispondenti del modulo (es. associa "Stampa Fronte e Retro" alla modalità Fronte/Retro del disegnatore). Vedi [fronte/retro](configurazione-prodotto.md#come-impostare-la-stampa-fronteretro) e [angoli arrotondati](configurazione-prodotto.md#come-impostare-gli-angoli-arrotondati).

### Risultato

Quando il cliente sceglie la variante nella scheda prodotto **prima di aprire il disegnatore**, PrestaShop calcola e applica automaticamente il **prezzo corretto nel carrello**.

---

Prossima pagina: [FAQ →](faq.md)
