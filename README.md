# Karoline E. Normann — Portfolio

## Filstruktur

```
portfolio/
├── index.html              ← Forside
├── om.html                 ← Om meg
├── arbeider.html           ← Tidligere prosjekter (delt på årstall)
├── avgangsoppgave.html     ← Avgangsoppgaven 2026
├── prosjekt-mal.html       ← MAL — kopier denne for nye prosjekter
└── pdf/                    ← Alle PDF-er
```

## Hvordan legge til et tidligere prosjekt

Hvert tidligere prosjekt får sin egen side, bygget fra `prosjekt-mal.html`.

### Steg 1: Lag en ny prosjektside
1. Kopier `prosjekt-mal.html`
2. Gi den et beskrivende navn, f.eks. `prosjekt-2025-a.html`

`arbeider.html` lenker allerede til disse filnavnene:
- `prosjekt-2025-a.html`, `prosjekt-2025-b.html`, `prosjekt-2025-c.html`
- `prosjekt-2024-a.html`, `prosjekt-2024-b.html`, `prosjekt-2024-c.html`
- `prosjekt-2023-a.html`, `prosjekt-2023-b.html`

Bruk disse navnene først — så slipper du å endre noe på arbeider-siden. Hvis du vil ha andre navn, må du oppdatere `href="..."` i `arbeider.html`.

### Steg 2: Fyll inn innhold
Åpne filen og søk etter `[` for å finne alt som må byttes ut:
- `[Prosjekttittel]` — navnet på prosjektet
- `[ÅR]` — årstall (f.eks. 2025)
- `[Kategori]` — f.eks. Konsept, Studie, Mønster, Kolleksjon
- Beskrivelsen
- `[Dokumenttittel]` for hver PDF-seksjon
- `[filnavn].pdf` — navnet på PDF-filen i `pdf/`-mappen

### Steg 3: Tilpass antall PDF-er
Malen har 3 PDF-seksjoner som standard.

- **Trenger du flere?** Kopier hele `<article class="doc">...</article>`-blokken og lim inn under. Endre kun `id="dok1"` til et nytt unikt navn (f.eks. `id="dok4"`). Legg også til en ny lenke i `<div class="toc">` øverst.
- **Trenger du færre?** Slett hele `<article>`-blokken og den matchende lenken i toc-en.

Nummerering (01, 02, 03...) skjer **automatisk** basert på rekkefølgen.

### Steg 4: Legg PDF-ene i pdf/-mappen
PDF-ene må ligge i `pdf/`-mappen med samme filnavn som du skrev i koden.

---

## Avgangsoppgaven 2026

PDF-ene som må ligge i `pdf/`-mappen:
- `portefolje.pdf` (brukes også for Kolleksjonsplan)
- `loggbok.pdf`
- `lookbok.pdf`
- `techpack1.pdf`
- `techpack2.pdf`
- `brandbook.pdf`

---

## Annet å fylle inn

Søk gjennom alle filer etter `[` og bytt ut:
- `[e-post]` — flere steder
- Tekstene i `om.html` (intro, utdanning, ferdigheter, erfaring)
- `[Kolleksjonens navn]` i arbeider.html og avgangsoppgave.html
- Prosjekttitler på arbeider-siden

## Bilder

Bytt "Bilde"-bokser ut med ekte bilder:

```html
<div class="tile-img"><img src="bilder/portefolje-cover.jpg" alt=""></div>
```

Lag mappen `bilder/` og legg bildene der.

## Publisering

Enkleste alternativer (gratis):
- **Netlify Drop** — netlify.com/drop, dra mappen inn, får link med en gang
- **Vercel** — dra-og-slipp eller GitHub
- **GitHub Pages** — krever GitHub-konto

For å koble `knormann.no`: kjøp domenet hos f.eks. domeneshop.no (~100 kr/år), pek det mot Netlify/Vercel.
