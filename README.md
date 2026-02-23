# Open Innovation Card Deck – GitHub Pages

Statische Version von [carddeck.openinnovationcity.de](https://carddeck.openinnovationcity.de) für GitHub Pages Hosting.

Ursprünglich erstellt mit **Webflow** (zuletzt veröffentlicht: November 2023).

---

## Schritt 1: Assets herunterladen

Da Assets (CSS, Bilder, JS, PDF) direkt von der Live-Seite kommen müssen,
führe einmalig das Download-Script aus – am besten auf einem Rechner mit
normalem Internetzugang:

```bash
bash download-assets.sh
```

Das Script lädt alle benötigten Dateien in die richtigen Unterordner:
- `css/` – Webflow-Styles
- `js/` – Webflow-JavaScript
- `images/` – alle SVGs, Icons und Logos
- `OIC_Method-Cards_Printing-sheet.pdf` – downloadbare PDF

**Alternative ohne Script:** Öffne die Live-Seite im Browser und nutze
*Datei → Seite speichern unter → Webseite, vollständig*. Dann die
resultierenden Ordner in dieses Repo kopieren.

**Beste Option (empfohlen):** Nutze den **Webflow Export**:
Webflow Designer → Project Settings → Export Code → ZIP herunterladen.
Das gibt dir alle Dateien sauber verpackt, inklusive originalem CSS.

---

## Schritt 2: Repository einrichten

```bash
git init
git add .
git commit -m "Initial commit: OIC Carddeck static site"
git branch -M main
git remote add origin https://github.com/DEIN-ORG/carddeck.git
git push -u origin main
```

---

## Schritt 3: GitHub Pages aktivieren

1. GitHub Repo → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / `/ (root)`
4. Speichern → die Seite ist nach kurzer Zeit unter
   `https://DEIN-ORG.github.io/carddeck/` erreichbar

Für eine eigene Domain (z.B. `carddeck.openinnovationcity.de`):
- Im Pages-Settings unter „Custom domain" eintragen
- Beim DNS-Provider einen CNAME-Eintrag anlegen:
  `carddeck` → `DEIN-ORG.github.io`

---

## Dateistruktur

```
/
├── index.html                          ← Hauptseite
├── OIC_Method-Cards_Printing-sheet.pdf ← Download-PDF
├── css/
│   ├── normalize.css
│   ├── webflow.css
│   └── open-innovation-city.webflow.css
├── js/
│   └── webflow.js
└── images/
    └── (alle SVGs, Icons, Logos)
```

---

## Hinweise

- **jQuery** wurde auf das offizielle jQuery-CDN umgestellt
  (statt Webflow-spezifischem CloudFront-Link) – das ist für GitHub Pages nötig.
- Google Fonts (Open Sans) werden weiterhin extern geladen.
- Webflow-Animationen funktionieren nur, solange `js/webflow.js` geladen ist.
