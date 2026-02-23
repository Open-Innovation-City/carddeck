# Open Innovation City – Card Deck

Statische Website, konvertiert aus einem Safari-Webarchiv für GitHub Pages.

## Deployment

1. Dieses Repository auf GitHub pushen
2. In den Repository-Einstellungen unter **Settings → Pages** als Source den Branch `main` (bzw. `master`) und den Ordner `/` (root) auswählen
3. GitHub Pages veröffentlicht die Seite automatisch unter `https://<username>.github.io/<repository-name>/`

## Struktur

```
index.html        # Hauptseite
css/              # Stylesheets (normalize, webflow, custom, fonts)
js/               # JavaScript (webflow, jquery, webfont)
images/           # SVGs, PNGs
fonts/            # Schriftarten (Open Sans, Webflow Icons)
.nojekyll         # Deaktiviert Jekyll-Verarbeitung (wichtig für Pfade mit Unterstrichen)
```

## Hinweis

Externe Links (z.B. zu openinnovationcity.de, Partner-Logos) verweisen weiterhin auf die Originaldomains.
