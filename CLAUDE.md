# CLAUDE.md

Webbsida för boken **Du Hinner! Ta makten över din tid** av Jonas Hjalmar Blom.
Domän: duhinner.se. Hostad på samma plats som jonashjalmarblom.se.

## Struktur

```
index.html              ← Startsida (hero, om boken, illustrationer, e-learning, video, köp)
css/styles.css          ← All styling
images/                 ← du-hinner.jpg (bokomslag) + illustrationer
referenser/index.html   ← Källförteckning (fylls i av Jonas)
CNAME                   ← duhinner.se
```

## Design

- Typografi: Cormorant Garamond (rubriker) + Inter (brödtext) via Google Fonts
- Färger från bokomslaget:
  - `--mint: #DDE8C8` — bakgrundsgrönt (hero-bakgrund, accenter)
  - `--orange: #E8451C` — primär accentfärg (CTA-knappar, etiketter)
  - `--navy: #1A1D4A` — rubrikfärg, navigation, footer
  - `--cream: #FAFAF8` — sektionsbakgrund
- Inga externa beroenden utöver Google Fonts

## Sektioner

1. **Hero** — bokomslag + rubrik + CTA
2. **Om boken** — beskrivning + metainfo
3. **Illustrationer** — bildgrid (platshållare, lägg till filer i `images/`)
4. **E-learning** — Fabella-integration (uppdatera länken när kursen är live)
5. **Videoföreläsningar** — YouTube-embed-mall finns i kommentarerna
6. **Köp boken** — länkar till Adlibris, Bokus, Akademibokhandeln (uppdatera URL:er)
7. **Footer**

## Vad som återstår

- [ ] Lägg till illustrationer i `images/` och ersätt platshållarna i `#illustrations-grid`
- [ ] Lägg till faktiska köplänkar i `#kop-boken`
- [ ] Lägg till Fabella-länk i e-learning-sektionen
- [ ] Lägg till videor (YouTube-embed-mall finns i kommentarerna i index.html)
- [ ] Fyll i referenslistan i `referenser/index.html`
- [ ] Ladda upp alla filer till webhotellet och peka duhinner.se dit

## Lägga till en illustration

Lägg bildfilen i `images/`, sedan i `index.html` under `#illustrations-grid`:

```html
<div class="illustration-card">
  <img src="images/FILNAMN.jpg" alt="Beskrivning av illustrationen" />
</div>
```

## Lägga till en YouTube-video

I `index.html` under `#video-grid`, ersätt ett platshållarkort eller lägg till nytt:

```html
<div class="video-card">
  <div class="video-thumb">
    <iframe
      src="https://www.youtube.com/embed/VIDEO_ID"
      title="Titel på videon"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen>
    </iframe>
  </div>
  <div class="video-info">
    <h3>Titel på föreläsningen</h3>
    <p>Kort beskrivning</p>
  </div>
</div>
```
