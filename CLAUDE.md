# Portfolio di Nicolò Giacometto: contesto del progetto

Sito portfolio personale di Nicolò per proporsi come sviluppatore freelance. Lingua del sito e dei commenti: italiano. Nicolò scrive in italiano, tono informale, preferisce risposte brevi e dirette.

Nota: il `CLAUDE.md` nella cartella superiore (`~/Sviluppo`) riguarda Stars & Dungeons, un altro progetto. Per questo repo vale solo questo file.

## Stato attuale

Prima versione completa, pagina singola. Repo: `github.com/nicologiacometto11/portfolio` (SSH, branch `main`). Git si usa con Fork.

## Stack e comandi

Sito statico: un solo file `index.html` con HTML e CSS dentro, nessun JavaScript, nessuna build, nessuna dipendenza. Unico file esterno: i font di Google Fonts (Bricolage Grotesque, Source Sans 3, JetBrains Mono).

```
python3 -m http.server 8000   # poi http://localhost:8000
```

Hosting: GitHub Pages (repo pubblico), pubblicato dal workflow `.github/workflows/deploy.yml` a ogni push su `main`. URL: `https://nicologiacometto11.github.io/portfolio/`. Il workflow pubblica solo `index.html`: se si aggiungono file (immagini, CSS), vanno copiati anche nello step "Prepara la cartella da pubblicare".

## Struttura della pagina

Header con nome e scheda dati (base, clienti in zona, formazione, disponibilità), poi le sezioni `#servizi`, `#lavori`, `#stack`, `#chi-sono`, `#contatti` e il footer.

I lavori sono un registro a righe (tipo e stato a sinistra, titolo, descrizione e tag a destra), non card.

## Design

- Colori e font sono token CSS in `:root` all'inizio dello `<style>`. Non scrivere colori direttamente nei componenti.
- Accento granata (`--accent`), sfondo grigio-azzurro chiaro. Il tema scuro segue `prefers-color-scheme` ed è definito con gli stessi token.
- Layout responsive: sotto 760px le sezioni vanno su una colonna, sotto 560px anche le righe dei lavori.
- Evitare: emoji come marcatori, gradienti viola-blu, tutto centrato, card con bordi arrotondati ovunque.

## Contenuti: regole

- Usare solo fatti veri su Nicolò e sui progetti. Niente prezzi, anni di esperienza, testimonianze o tecnologie inventate.
- Le tecnologie si indicano solo dove sono note (oggi: Shopify per Equipe Sport, React e Vite per Tennis Manager).
- Testi semplici e diretti, senza trattini lunghi a metà frase e senza giri di parole.

## Progetti mostrati

- Equipe Sport: redesign e-commerce Shopify, negozio di Grugliasco (in corso)
- La Dea Ranch: sito vetrina, centro ippico di Val della Torre (in corso)
- Psychart: SaaS per cartelle cliniche di psicologi italiani, `psychart.it`
- Tennis Manager: web app React/Vite su Netlify
- Stream Utility: app Windows per dirette Twitch/Kick/YouTube, incarico di refactoring (in corso)

## Da fare

- Aggiungere i contatti (email, telefono o LinkedIn) in `#contatti`. Per ora c'è solo GitHub.
- Far controllare a Nicolò le descrizioni dei progetti, in particolare Psychart e Tennis Manager.
- Aggiungere screenshot dei progetti.
- Verificare che `psychart.it` sia il link giusto da mostrare.
- Pubblicare su Netlify o GitHub Pages ed eventuale dominio personale.
- Meta tag per la condivisione dei link (anteprima) e favicon.

## Convenzioni

- Un solo file HTML finché la pagina resta semplice. Se cresce, dividere CSS e immagini in file separati senza introdurre una build.
- Nuove sezioni: stessa struttura delle esistenti (`section` con `h2` a sinistra e contenuto in `.body`).
- Commit in italiano, messaggi brevi.
