# Meal Planer für den Ninja Speedi

Private Web-App für das Programm Speedi Meals am Ninja Speedi (ON400EU). Nur für Familie und Freunde gedacht: nicht indexiert, kein Impressum, Link wird direkt geteilt.

Läuft komplett im Browser, Daten bleiben lokal (localStorage). Keine Cookies, kein Tracking, keine externen Ressourcen.

## Dateien
| Datei | Zweck |
|---|---|
| `index.html` | die App (läuft auch allein als Datei) |
| `sw.js`, `manifest.webmanifest`, `icon*` | Offline-Start und „Zum Startbildschirm“ (nur über https) |
| `.htaccess` | `X-Robots-Tag: noindex` für alle Dateien (Apache) |

## Hochladen
Ordner (ohne `.git`, `README.md`) in ein Verzeichnis der Website laden, z. B. `/meal-planer/`, und den Link direkt teilen.

**Nicht** in `robots.txt` sperren: Dann sieht Google das `noindex` nicht und kann die URL trotzdem listen, falls sie irgendwo verlinkt wird.

Bitte nicht auf öffentlichen Seiten, in Foren oder Social Media posten. Sobald die App öffentlich beworben wird, gilt sie nicht mehr als rein privat, und dann sind Impressum (§ 18 MStV) und Datenschutzerklärung nötig.
