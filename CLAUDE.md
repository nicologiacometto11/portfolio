# Portfolio di Nicolò Silvio Giacometto: contesto del progetto

Sito portfolio personale di Nicolò per proporsi come sviluppatore freelance. Lingua del sito e dei commenti: italiano. Nicolò scrive in italiano, tono informale, preferisce risposte brevi e dirette.

Nota: il `CLAUDE.md` nella cartella superiore (`~/Sviluppo`) riguarda Stars & Dungeons, un altro progetto. Per questo repo vale solo questo file.

## Stato attuale

Prima versione completa, pagina singola. Repo: `github.com/nicologiacometto11/portfolio` (SSH, branch `main`). Git si usa con Fork.

## Stack e comandi

Sito statico: un solo file `index.html` con HTML e CSS dentro, nessun JavaScript, nessuna build, nessuna dipendenza. Font in locale nella cartella `fonts/` (Bricolage Grotesque, Source Sans 3, JetBrains Mono, solo subset latin, woff2), niente richieste a Google.

```
python3 -m http.server 8000   # poi http://localhost:8000
```

Hosting: GitHub Pages (repo pubblico), pubblicato dal workflow `.github/workflows/deploy.yml` a ogni push su `main`. URL: `https://nicologiacometto11.github.io/portfolio/`. Il workflow pubblica solo `index.html`, le cartelle `en/` e `fonts/`, `favicon.svg`, `og-image.png`, `foto.webp`: ogni file nuovo (immagini, CSS) va copiato anche nello step "Prepara la cartella da pubblicare".

## Lingue

Versione inglese in `en/index.html`, stessa struttura e stesso CSS (copiato). Ogni modifica a testi o stile va fatta in entrambe le pagine. Asset con `../` nella versione inglese.

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
- Le tecnologie si indicano solo dove sono note (oggi: quelle trovate nelle cartelle dei progetti, vedi sotto).
- Testi semplici e diretti, senza trattini lunghi a metà frase e senza giri di parole.

## CV

La sezione `#percorso` viene dal CV (`~/Desktop/CV_Nicolo_Silvio_Giacometto.pdf`). Nel sito NON vanno data di nascita, indirizzo di casa, patente e foto. Il PDF non è pubblicato.

## Progetti mostrati

Descritti guardando le cartelle in `~/Sviluppo` (3 novembre 2026):

- Equipe Sport: redesign Shopify di Grugliasco (tema con sezioni Liquid su misura, app con Shopify Function di sconto) (in corso)
- Psychart: app Flutter + FastAPI + PostgreSQL per psicologi e medici, cifratura E2EE, `psychart.it`, gratis, fatta da solo
- La Dea Ranch: sito vetrina React/Vite su GitHub Pages, centro ippico di Val della Torre (in corso)
- itstracker: tracker serie TV e film, PWA con Firebase e TMDB (fatto con un socio, repo sotto l'org `itsurri`), `itsurri.github.io/itstracker`
- Stars & Dungeons: companion web per un GDR, React/Vite/Supabase

Tennis Manager e Stream Utility sono stati tolti dal sito.

## Da fare

- Valutare la partita IVA e rivedere di conseguenza i testi ("freelance", "nuovi progetti"). Quando c'è, metterla nel footer.
- Aggiungere screenshot dei progetti (quelli dei siti online si possono fare da browser; per le app mobile servono quelli di Nicolò).
- Controllare le descrizioni dei progetti (scritte guardando le cartelle) e la frase in "Chi sono" ("ultimo anno", "part-time").
- Eventuale LinkedIn in `#contatti`.
- Con un dominio personale aggiornare gli URL assoluti nei meta tag (`og:url`, `og:image`, `canonical`, `hreflang`).

## Proposte non ancora fatte

- Recensioni vere dei clienti (Dea Ranch, Equipe Sport), con permesso a pubblicarle.
- Mini casi di studio per i lavori per clienti: com'era prima, cosa ho fatto, com'è adesso (solo fatti veri).
- Google Search Console, per far indicizzare il sito (non tocca il codice).
- Controllo con Lighthouse (velocità, accessibilità, SEO) e correzioni.
- Link al sito nel CV e nel campo "Website" del profilo GitHub (lo fa Nicolò).
- Dominio personale (es. `nicologiacometto.it`): record A e CNAME verso GitHub Pages, Settings → Pages → Custom domain.
- Bottone WhatsApp piccolo e fisso in basso da telefono.
- Contatore di visite senza cookie (GoatCounter o Plausible), facoltativo.
- CV scaricabile in PDF senza dati personali (niente indirizzo né data di nascita), con bottone "Scarica il CV".

## Convenzioni

- Un solo file HTML finché la pagina resta semplice. Se cresce, dividere CSS e immagini in file separati senza introdurre una build.
- Nuove sezioni: stessa struttura delle esistenti (`section` con `h2` a sinistra e contenuto in `.body`).
- Commit in italiano, messaggi brevi.
