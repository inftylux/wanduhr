# Wanduhr

Eine Wanduhr-WebApp: Das echte Ziffernblatt-Foto füllt die ganze Seite, die ebenfalls
eingescannten Zeiger drehen wie bei der echten Uhr und läuten zur vollen und halben
Stunde.

## Funktionen

- Ziffernblatt und Zeiger sind echte Fotos (`werk/`), ebenfalls freigestellt
- **Exaktes Drehzentrum**: Pivots aus Kreisfits am Ziffernblatt (konzentrische Ringe)
  und am Zeigerende (Nabenloch/Nabenring) — die Spitze des Minutenzeigers berührt
  exakt den äusseren Minutenring
- Beim Ziffernblatt **ziehen** stellt die Uhrzeit (mit Glockenschlägen bei überflogenen
  halben/vollen Stunden); ein kurzer **Klick** aufs Blatt stellt auf die echte Zeit zurück
- **Glockenschlag** zur vollen Stunde (Anzahl = Stunden, 24-Std.-Zählung) und ein
  einzelner Schlag zur halben Stunde
- Auf dem iPhone wie eine eigene **App im Vollbild** installierbar
  („Teilen“ → „Zum Home-Bildschirm“), inkl. App-Icon (Zeigerstellung 13:50)

## Dateien (nur diese sind für den Betrieb nötig)

| Datei | Zweck |
|---|---|
| `index.html` | Uhr (HTML/CSS/JS) |
| `manifest.json` | Web-App-Manifest (Fullscreen, Icons) |
| `schlag-lang.m4a` | Glockenschlag |
| `werk/ziffernblatt-frei.png` | Ziffernblatt, Ecken transparent |
| `werk/kleinerZeiger-crop.png` | Stundenzeiger (Nabe bei 44.49 %, 90.77 %) |
| `werk/groesserZeiger-crop.png` | Minutenzeiger (Nabe bei 50.47 %, 92.07 %) |
| `werk/icon.png` | Favicon (128×128) |
| `werk/apple-touch-icon.png` | iOS-App-Icon (180×180) |

Alles Weitere (Originalfotos, Backups, Audio-Arbeitdateien) ist per `.gitignore`
aus dem Repo ausgeschlossen.

## Deployment

Ordnerstruktur wie vorgesehen auf einen Webserver hochladen
(HTTP(S), z. B. `git clone` + statischer Server). HTTPS empfohlen,
damit Audio und die Home-Screen-App-Funktion zuverlässig funktionieren.

## Benutzung

- Uhr läuft automatisch zur echten Zeit
- Ziehen am Ziffernblatt: Zeiger stellen
- Kurzer Klick aufs Ziffernblatt: zurück auf echte Zeit
- iOS: Seite in Safari öffnen → Teilen → „Zum Home-Bildschirm“
