# Karoline E. Normann — Portfolio

Personlig portefølje-nettside for klesdesigner Karoline E. Normann, bygget som en statisk side med vanlig HTML og CSS.

**Live:** [knormann.no](https://www.knormann.no)

## Oversikt

Siden er bevisst holdt enkel: ingen rammeverk, ingen build-steg, ingen JavaScript. Bare statiske HTML-filer med innebygd CSS som rendrer raskt og lar seg redigere uten verktøy ut over en teksteditor. Designet henter inspirasjon fra modernistisk magasin-typografi — kun Inter sans-serif i tunge vekter, beige bakgrunn, mye luft.

## Filstruktur

```
.
├── index.html              # Forside med grid av prosjekter
├── om.html                 # Om designeren
├── arbeider.html           # Arkiv over tidligere prosjekter, delt på årstall
├── avgangsoppgave.html     # Avgangsoppgave 2026 med embedded PDF-er
├── prosjekt-mal.html       # Mal for nye prosjektsider
├── pdf/                    # PDF-dokumenter (porteføljer, lookbooks, techpacks)
└── README.md
```

## Teknologi

- **HTML5** og **CSS3** (ingen preprocessors)
- **Google Fonts** — Inter (lastes inn fra CDN)
- **CSS Counters** for automatisk nummerering av dokumentseksjoner
- **CSS Grid** for layout
- **`<iframe>`** for innebygd PDF-visning med nedlastings-fallback

## Designprinsipper

- **Typografi:** Inter sans-serif, vekter 300–700, store letter-spacing-verdier på uppercase-tekst
- **Fargepalett:** `--bg: #f4f1ec` (beige), `--ink: #1a1a1a` (sort), `--muted: #8a8378` (varm grå), `--line: #d8d1c5` (kantlinje)
- **Spacing:** generøse marger, tynne 1px-skiller i stedet for kort eller bokser
- **Bevegelse:** subtile fade-in-animasjoner ved sidelasting

## Legge til et nytt prosjekt

1. Kopier `prosjekt-mal.html` til et nytt filnavn, f.eks. `prosjekt-2025-a.html`
2. Erstatt alt i `[klammer]` med faktisk innhold
3. Legg til/fjern `<article class="doc">`-blokker etter behov — nummerering (01, 02, 03 ...) genereres automatisk via CSS Counters
4. Legg PDF-ene i `pdf/`-mappen
5. Oppdater lenken i `arbeider.html` så den peker til den nye filen

## Deploy

Siden deployes automatisk til Netlify når `main`-branchen oppdateres. Ingen build-konfigurasjon nødvendig — Netlify serverer filene direkte.

## Lisens

Innhold (tekst, bilder, PDF-er) er © Karoline E. Normann. Koden er åpen til inspirasjon, men ikke ment for direkte gjenbruk uten tilpasning.
