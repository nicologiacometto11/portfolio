# Portfolio

Sito portfolio personale di Nicolò Silvio Giacometto, sviluppatore freelance a Torino.

Pagina statica, un solo file: `index.html` con HTML e CSS dentro, nessuna dipendenza da installare. Gli unici file esterni sono i font di Google Fonts.

## Provarlo in locale

Apri `index.html` nel browser, oppure:

```
python3 -m http.server 8000
```

e vai su http://localhost:8000.

## Pubblicarlo

Il sito è su GitHub Pages: https://nicologiacometto11.github.io/portfolio/

Il workflow `.github/workflows/deploy.yml` lo pubblica a ogni push su `main`, oppure a mano da Actions → "Run workflow". Non c'è build: vengono pubblicati solo `index.html`, `favicon.svg`, `og-image.png` e `foto.webp`. Un file nuovo va aggiunto anche allo step "Prepara la cartella da pubblicare" del workflow.

Impostazione da fare una volta sola: Settings → Pages → Source = GitHub Actions.

## Contenuto

Header con scheda dati, poi le sezioni Cosa faccio, Lavori (Equipe Sport, Psychart, La Dea Ranch, itstracker, Stars & Dungeons), Percorso (dal CV), Strumenti, Chi sono e Contatti (email, telefono, GitHub).

Nel sito non ci sono data di nascita, indirizzo di casa e foto del CV.

## Da fare

- Aggiungere screenshot dei progetti.
- Controllare le descrizioni dei progetti.
- Valutare la partita IVA e rivedere di conseguenza i testi ("freelance", "nuovi progetti").
- Eventuale LinkedIn nei Contatti.
