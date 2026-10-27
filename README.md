# Meal Planer für den Ninja Speedi

Mobile Web-App für das Programm Speedi Meals am Ninja Speedi (ON400EU). Läuft komplett im Browser, Daten bleiben lokal (localStorage). Keine Cookies, kein Tracking, keine externen Ressourcen.

## Dateien
| Datei | Zweck |
|---|---|
| `index.html` | die App (läuft auch allein als Datei) |
| `impressum.html`, `datenschutz.html` | Rechtliches, Platzhalter ausfüllen |
| `sw.js`, `manifest.webmanifest`, `icon*` | Offline-Start und „Zum Startbildschirm“ (nur über https) |
| `robots.txt`, `sitemap.xml`, `og-image.png` | SEO und Vorschaubild für geteilte Links |

## Vor dem Hochladen: Platzhalter ersetzen
Alle Platzhalter haben die Form `__NAME__`. Prüfen mit:

```sh
grep -rn "__[A-Z_]*__" --include="*.html" --include="*.txt" --include="*.xml" .
```

`__BASE_URL__` ist die volle Adresse des App-Ordners **mit** abschließendem Slash, z. B. `https://www.beispiel.de/meal-planer/`:

```sh
sed -i 's#__BASE_URL__#https://www.beispiel.de/meal-planer/#g' index.html impressum.html datenschutz.html robots.txt sitemap.xml
```

Liegt die App in einem Unterordner, gehört `robots.txt` nicht in den Ordner, sondern es reicht, die Sitemap-Zeile in die vorhandene `robots.txt` der Website aufzunehmen bzw. die URL in die vorhandene Sitemap.

## Hochladen
Den ganzen Ordner (ohne `.git`, `README.md`) per FTP/Dateimanager in einen Ordner der Website laden, z. B. `/meal-planer/`. Nicht per iframe in ein CMS einbetten: Service Worker, Bildschirm-wach-Funktion und SEO funktionieren dann schlechter.

Danach: Seite in der Google Search Console einreichen.
