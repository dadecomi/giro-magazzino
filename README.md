# Giro Magazzino – PWA offline (scadenze/rotture)

App web **gratuita** e **offline** per fare il giro scadenze/rotture in magazzino (pensata per tablet Android).  
Tasti grandi, funzionamento semplice, esportazione CSV apribile con Excel.

## Funzioni
- 📝 Segna **OK / In scadenza / Rotta / Scaduta** per ogni prodotto
- 📦 Traccia l'**appartamento** della merce rotta o scaduta (quando la metti da parte)
- 🔌 **Offline-first**: se non c'è rete o si spegne il tablet, i dati restano (IndexedDB + Service Worker)
- ⬇️ **Esportazione Excel (CSV)** + JSON
- 📱 **PWA**: aggiungi alla schermata Home su Android

## Installazione con GitHub Pages (gratis)
1. Crea un nuovo repository su GitHub, per es. `giro-magazzino`.
2. Scarica questo progetto come ZIP e estrailo.
3. Carica i file nel repository (`index.html`, `sw.js`, `manifest.webmanifest`, `products.json`, cartella `assets/`).
4. Vai su **Settings → Pages** e imposta:
   - **Branch**: `main` (o `master`)
   - **Folder**: `/ (root)`
   - Salva: dopo poco avrai l'URL pubblica del sito (https).
5. Apri l'URL con il tablet Android e fai **Aggiungi alla schermata Home** (diventa un'app senza barra URL).
6. La prima volta apri l'app online per far scaricare i file. Da quel momento funziona anche **offline**.

## Uso rapido
- Premi **Nuovo Giro** (o **Continua Giro** se ne hai uno aperto).
- Vai su **Giro** e usa i 4 pulsanti grandi per segnare lo stato dell'articolo corrente.
- **In scadenza/Scaduta** chiedono *data di scadenza*, **Rotta** permette *quantità* e *note*.
- La scheda **Apparta** ti mostra le voci `Rotta/Scaduta` da mettere da parte → premi **Segna come Appartata**.
- In **Export** premi **Esporta Excel (CSV)** per scaricare il file del giro.

## Dati
- I prodotti iniziali (50 salumi/carni) sono in `products.json`. Puoi modificarlo o aggiungerne altri.
- I dati del giro restano **solo sul dispositivo** (browser/Tablet) in **IndexedDB**.

## Backup/Trasferimento dati
Da **Export** salva il JSON del giro e caricalo dove vuoi. CSV è apribile con Excel.

## Note
- Per il pieno offline, apri almeno una volta l'app **con internet** per scaricare la cache.
- Se vuoi fare una versione multi-magazzino o multi-utente, scrivi nel codice nella sezione `// --- Sessions ---`.