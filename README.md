# Linkera - Personal Branding Platform

Linkera è una piattaforma avanzata per il personal branding che trasforma l'identità digitale in un'esperienza potente e personalizzabile attraverso un singolo link.

## 🚀 Deployment su Netlify

### Deploy Automatico (Raccomandato)

1. **Carica il progetto su GitHub**
   - Crea un nuovo repository
   - Fai push di tutti i file del progetto

2. **Connetti a Netlify**
   - Vai su [netlify.com](https://netlify.com)
   - Click "New site from Git"
   - Seleziona il tuo repository GitHub
   - Netlify rileverà automaticamente le impostazioni dal file `netlify.toml`

3. **Configura le variabili d'ambiente**
   - Nel dashboard Netlify: Site settings > Environment variables
   - Aggiungi: `VITE_API_URL` con l'URL del tuo backend

### Deploy Manuale

1. **Build locale**
   ```bash
   cd client
   npm install
   npx vite build
   ```

2. **Upload su Netlify**
   - Trascina la cartella `dist` su netlify.com

## 🛠 Tecnologie

- **Frontend**: React, Vite, TailwindCSS
- **UI Components**: Radix UI, Shadcn/ui
- **State Management**: TanStack Query
- **Database**: PostgreSQL con Drizzle ORM
- **Authentication**: Session-based con Express

## 📁 Struttura Progetto

```
├── client/              # Frontend React
│   ├── src/
│   │   ├── components/  # Componenti UI
│   │   ├── pages/       # Pagine principali
│   │   ├── hooks/       # Custom hooks
│   │   └── lib/         # Utilities e configurazioni
├── server/              # Backend Express
├── shared/              # Schema e tipi condivisi
├── attached_assets/     # Assets e immagini
└── netlify.toml        # Configurazione Netlify
```

## 🎨 Funzionalità Principali

### Dashboard Personalizzazione
- **Editor Profilo Avanzato**: Personalizzazione completa del profilo
- **Gestione Sfondi**: 50+ sfondi predefiniti + caricamento personalizzato
- **Widget Personalizzabili**: 9 colori (incluso trasparente), 3 forme, 3 layout
- **Drag & Drop**: Riordinamento intuitivo dei widget
- **Galleria Foto**: Upload e gestione immagini
- **Link Social**: Integrazione con tutte le piattaforme principali

### Profilo Pubblico
- **Responsive Design**: Ottimizzato per tutti i dispositivi
- **Anteprima Real-time**: Visualizzazione istantanea delle modifiche
- **QR Code**: Generazione automatica per condivisione rapida
- **Analytics**: Tracking dei click sui link

### Business Features
- **Sezione Servizi**: Gestione prezzi e descrizioni
- **Orari di Apertura**: Configurazione orari business
- **Mappa Interattiva**: Localizzazione geografica
- **Calendario Appuntamenti**: Sistema di prenotazione

## 🔧 Configurazione Backend

Il frontend è configurato per funzionare con un backend separato. Per il deployment completo:

1. **Deploy Backend su Heroku/Railway/Render**
2. **Configura Database** (Neon, Supabase, PlanetScale)
3. **Aggiorna VITE_API_URL** nelle variabili d'ambiente Netlify

## 📱 Demo e Anteprima

- Layout responsive ottimizzato per mobile
- Animazioni fluide e transizioni eleganti
- Interfaccia intuitiva in italiano
- Design moderno con dark/light mode

## 🔐 Sicurezza

- Headers di sicurezza configurati
- Protezione CSRF
- Validazione input con Zod
- Session management sicuro

## 📈 Performance

- Bundle optimized con code splitting
- CDN globale Netlify
- Lazy loading componenti
- Immagini ottimizzate

---

Il progetto è pronto per il deployment su Netlify con tutte le configurazioni ottimizzate per performance e sicurezza.