# Gestione Formazioni — Frontend

Interfaccia web da pubblicare su **GitHub Pages** (gratis).

## Configurazione API URL

Apri `index.html` e cerca questa riga vicino all'inizio del `<script>`:

```js
const API = localStorage.getItem('api_url') || 'http://localhost:8000';
```

Dopo il deploy del backend su Render, puoi impostare l'URL direttamente
nel browser aprendo la console (F12) e digitando:

```js
localStorage.setItem('api_url', 'https://TUO-BACKEND.onrender.com')
location.reload()
```

Oppure sostituisci direttamente `'http://localhost:8000'` con l'URL di Render.

## Deploy su GitHub Pages

### Passo 1 — Crea repository GitHub
1. Vai su https://github.com → **New repository**
2. Nome: `formazioni-app` (o qualsiasi nome)
3. Lascia pubblico (necessario per GitHub Pages gratis)
4. Clicca **Create repository**

### Passo 2 — Carica il file
```bash
git init
git add index.html
git commit -m "frontend formazioni"
git remote add origin https://github.com/TUONOME/formazioni-app.git
git push -u origin main
```

### Passo 3 — Attiva GitHub Pages
1. Nel repository → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** → cartella: **/ (root)**
4. Clicca **Save**

Dopo 1-2 minuti l'app sarà disponibile su:
`https://TUONOME.github.io/formazioni-app`

## Struttura pagine

| Sezione | Funzione |
|---|---|
| Dashboard | Statistiche generali + riepilogo per cantiere |
| Scadenze | Tutte le scadenze imminenti, filtrabili per giorni |
| Dipendenti | Lista + ricerca + CRUD completo |
| Cantieri | Gestione sedi di lavoro |
| Attestati | Tutti gli attestati con semaforo colori |
| Visite Mediche | Visite con durata in mesi personalizzabile |
| Catalogo Corsi | Tutti i 37 corsi pre-caricati |
| Esporta Excel | Scarica tutto in xlsx aggiornato |
