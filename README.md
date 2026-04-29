# Hannah Koch - Medien Portfolio

Persönliche Portfolio-Website für Bewerbungen im Podcast- und Medienbereich.

**Live-URL nach Deployment:** `https://hannahkooch.github.io`

---

## Aufbau

```
hannah-portfolio/
├── index.html          # Komplette Seite (HTML + CSS + JS in einer Datei)
├── images/
│   └── hannah.jpg      # Profilfoto
└── README.md
```

Eine Single-Page-Struktur, alles in `index.html`. Keine Build-Tools, kein Framework.

---

## Auf GitHub Pages deployen (Username-Site)

Hannahs GitHub-Account ist `hannahkooch`. Damit die Seite auf `hannahkooch.github.io` läuft, muss das Repository **exakt** so heissen: `hannahkooch.github.io`.

### Schritt 1: Repository auf GitHub anlegen

1. Auf [github.com](https://github.com) einloggen (Account `hannahkooch`)
2. Oben rechts auf das `+` und dann auf **New repository**
3. Repository-Name: **`hannahkooch.github.io`** (genau so, klein geschrieben)
4. Sichtbarkeit: **Public**
5. Haken bei *Add a README* NICHT setzen (haben wir schon)
6. Auf **Create repository** klicken

### Schritt 2: Dateien hochladen

**Option A - per Web-Interface (am einfachsten):**

1. Im neuen Repository auf **uploading an existing file** klicken
2. Den kompletten Inhalt vom Ordner `hannah-portfolio` reinziehen (also `index.html`, `README.md` und den `images`-Ordner)
3. Unten auf **Commit changes** klicken

**Option B - per Terminal (wenn Git installiert ist):**

```bash
cd hannah-portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/hannahkooch/hannahkooch.github.io.git
git push -u origin main
```

### Schritt 3: GitHub Pages aktivieren

In den meisten Fällen läuft die Seite bereits automatisch, weil das Repo auf `username.github.io` heisst. Falls nicht:

1. Im Repository auf **Settings** klicken
2. Links auf **Pages**
3. Bei *Source*: **Deploy from a branch** auswählen
4. *Branch*: **main**, Folder: **/ (root)**
5. **Save**

Nach 1-2 Minuten ist die Seite unter `https://hannahkooch.github.io` live.

---

## Inhalte anpassen

Alles wichtige steht in `index.html`. Bereiche zum Anpassen:

| Wo? | Was? |
|---|---|
| Hero-Section (Zeile ~520) | Begrüßung, Tagline, Meta-Infos |
| About-Section | Persönlicher Text und Quote |
| Werdegang | Timeline-Einträge mit Daten und Beschreibungen |
| Arbeitsproben | Spotify-Embeds, YouTube-Embeds, Instagram-Links |
| Stärken | Persönliche Stärken und „Warum Podcast" |
| Kontakt | E-Mail-Adresse |

Foto austauschen: einfach `images/hannah.jpg` ersetzen, gleicher Dateiname.

---

## Custom Domain (optional, falls später eine eigene Domain dazukommt)

1. Im Repo unter **Settings -> Pages** unter *Custom domain* die Domain eintragen
2. Beim Domain-Provider einen `CNAME`-Eintrag auf `hannahkooch.github.io` setzen
3. **Enforce HTTPS** aktivieren

---

## Technische Notizen

- Schriften: **Fraunces** (Display) und **Manrope** (Body) via Google Fonts
- Keine externen Libraries, kein Build-Step
- Spotify- und YouTube-Embeds laden lazy, also nur wenn sichtbar
- Instagram Reels werden als gestylte Cards verlinkt (Instagram bietet keine zuverlässigen Embeds für statische Seiten)
- Responsive ab ca. 360px Breite getestet
- Keine Cookies, kein Tracking

---

Bei Fragen: einfach melden.
