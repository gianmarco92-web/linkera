# Guida al Deployment su Netlify - Linkera

## Opzione 1: Deploy Automatico da GitHub (Raccomandato)

### Step 1: Preparazione Repository
1. Crea un nuovo repository su GitHub
2. Carica tutti i file del progetto
3. Assicurati che il file `netlify.toml` sia incluso

### Step 2: Netlify Setup
1. Vai su [netlify.com](https://netlify.com) e crea un account
2. Click "New site from Git"
3. Connetti il tuo repository GitHub
4. Imposta le seguenti configurazioni:
   - **Build command**: `npx vite build --config vite.config.netlify.ts`
   - **Publish directory**: `dist`
   - **Base directory**: (lascia vuoto)

### Step 3: Variabili d'Ambiente
Nel pannello Netlify, vai in Site settings > Environment variables e aggiungi:
```
NODE_ENV=production
VITE_API_URL=https://your-backend.herokuapp.com
```

## Opzione 2: Deploy Manuale

### Step 1: Build del Progetto
```bash
# Installa le dipendenze
npm install

# Build per produzione
npx vite build --config vite.config.netlify.ts
```

### Step 2: Upload Manuale
1. Vai su netlify.com
2. Trascina la cartella `dist` nell'area "Deploy manually"
3. Il sito sarà disponibile immediatamente

## Configurazioni Incluse

### netlify.toml
- Redirects per SPA routing
- Configurazione build ottimizzata
- Headers di sicurezza

### vite.config.netlify.ts
- Bundle ottimizzato per produzione
- Code splitting per performance migliori
- Alias path configurati

## Note Importanti

1. **Database**: Il progetto usa PostgreSQL. Per Netlify dovrai:
   - Usare un servizio database esterno (Neon, Supabase, PlanetScale)
   - Configurare le variabili d'ambiente per il database

2. **Backend**: Netlify è per frontend statici. Il backend Express dovrebbe essere deployato su:
   - Heroku
   - Vercel (come serverless functions)
   - Railway
   - Render

3. **Assets**: Le immagini in `attached_assets` sono incluse automaticamente nel build

## Risultato
- Sito veloce e ottimizzato
- CDN globale di Netlify
- HTTPS automatico
- Deploy automatici ad ogni push (se connesso a Git)

## URL di Test
Dopo il deploy, il sito sarà disponibile su un URL tipo:
`https://amazing-name-123456.netlify.app`

Puoi cambiare il nome del sito dalle impostazioni Netlify.