# Nutrizione

App per il telefono (PWA) con la dieta settimanale, il diario nutrizionale a calendario e la lista della spesa.

- **Dieta**: settimana tipo giorno per giorno (colazione, merenda, pranzo, spuntini, cena) e dieta a basso residuo per la fase acuta.
- **Diario**: calendario con le spunte giornaliere (colazione, spuntini, olio, frutta secca, sintomi, allenamento), note e riflessioni settimanali.
- **Spesa**: lista per reparto, personalizzabile, da spuntare.

I dati del diario e della lista restano solo sul telefono (localStorage). Dall'icona in alto a destra si esporta e si importa un backup in formato JSON.

## File

| File | A cosa serve |
| --- | --- |
| `index.html` | L'app: interfaccia, dati della dieta, salvataggio e backup |
| `manifest.webmanifest` | Nome, icone e scorciatoie per l'installazione |
| `sw.js` | Funzionamento offline (cache dei file) |
| `icons/` | Icone dell'app |
| `robots.txt` | Chiede ai motori di ricerca di non indicizzare il sito |

## Pubblicazione

Il sito è statico: basta servire questa cartella così com'è (Netlify, GitHub Pages o qualsiasi hosting HTTPS). Dopo una modifica a `index.html` o alle icone conviene aumentare la versione di `CACHE` in `sw.js`, così il telefono scarica i file nuovi.
