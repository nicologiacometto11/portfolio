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

Il workflow `.github/workflows/deploy.yml` lo pubblica a ogni push su `main`, oppure a mano da Actions → "Run workflow". Non c'è build: viene pubblicato solo `index.html`.

Impostazione da fare una volta sola: Settings → Pages → Source = GitHub Actions.

## Da fare

- Aggiungere i contatti (email, telefono o LinkedIn) nella sezione Contatti.
- Controllare le descrizioni dei progetti.
- Aggiungere screenshot dei progetti.
