# Autonomio

Autonomio is a modern SaaS platform for intelligent business management in the automotive industry.

## Autonomio Landing Page

Produktionsfertige statische Landingpage.

### Dateien
| Datei | Zweck |
|-------|-------|
| `index.html` | Hauptseite (responsive, Tailwind CDN) |
| `logo.svg` | Logo / Favicon |
| `CNAME` | Custom Domain (`autonomio.app`) |
| `404.html` | Redirect bei unbekannten Routen |
| `robots.txt` | Basis Crawler Regeln |

### Waitlist API
POST Ziel: `/api/v1/waitlist`

Auflösung der API Base:
1. `window.WAITLIST_API_BASE` (falls gesetzt)
2. Lokal: `http://localhost:8080`
3. Sonst: gleiche Origin (relativ)

Override Beispiel (im `<head>`):
```html
<script>window.WAITLIST_API_BASE='https://api.autonomio.app';</script>
```

Backend muss CORS für Domain erlauben und JSON liefern.

### Deployment (GitHub Pages)
1. Push nach `main` → Workflow `deploy-landing.yml` veröffentlicht.
2. Settings → Pages: Source = GitHub Actions.
3. Custom Domain eintragen `autonomio.app` → HTTPS erzwingen sobald verfügbar.

### DNS (A Records für Root)
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```
Optional: `www` CNAME → `<username>.github.io`.

### Lokal Testen
`index.html` direkt öffnen. Für Formular lokalen Backend Dienst starten (Port 8080) oder API Base setzen.

### Anpassen
- Texte in `index.html`
- Analytics Snippet vor `</body>`
- `logo.svg` ersetzen (gleicher Dateiname)

### Rechtliches
Footer Links (Impressum / Datenschutz) später ergänzen.

© 2025 Autonomio. Alle Rechte vorbehalten.
