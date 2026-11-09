# Stempeluhr

Arbeitszeit per Klick erfassen: **Kommen** startet die Zeit, **Gehen** stoppt sie und bucht die Stunden auf den Tag.
Kalender von November 2026 bis Oktober 2028 mit KW-Summen, bundesweiten Feiertagen, Nachtragen/Löschen und CSV-Export/-Import.

Läuft komplett offline als installierbare Web-App (PWA). Die Daten bleiben auf dem Handy (Browser-Speicher), es gibt keinen Server.

## Auf GitHub Pages veröffentlichen

1. Auf github.com ein neues Repository anlegen, z.B. `stempeluhr` (öffentlich, denn GitHub Pages ist bei kostenlosen Konten nur für öffentliche Repos verfügbar).
2. Diese Dateien hochladen: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md`
   (im Browser: „Add file“ → „Upload files“, oder per `git push`).
3. Im Repo: **Settings → Pages → Build and deployment → Source: „Deploy from a branch“**, Branch `main`, Ordner `/ (root)`, **Save**.
4. Nach 1–2 Minuten ist die App erreichbar unter `https://<dein-github-name>.github.io/stempeluhr/`.

## Auf dem Android-Handy installieren

1. Die Adresse in **Chrome** öffnen.
2. Menü **⋮ → „App installieren“** (oder „Zum Startbildschirm hinzufügen“ → „Installieren“).
3. Die Stempeluhr erscheint als eigene App im App-Drawer, öffnet ohne Adressleiste und funktioniert danach auch ohne Internet.

## Wichtig zu den Daten

- Gespeichert wird nur auf diesem Handy, in Chrome. **Chrome-Daten löschen oder die App deinstallieren löscht auch die Zeiten.**
- Deshalb regelmäßig **„CSV speichern“** nutzen (z.B. monatlich). Mit **„Import“** lässt sich die CSV später wieder einlesen, etwa auf einem neuen Handy. Bereits vorhandene Einträge werden dabei übersprungen.
- Daten aus der Claude-Version: dort „CSV speichern“, hier „Import“.

## Updates

Nach einer Änderung an `index.html` in `sw.js` die Zeile `const VERSION = "stempeluhr-v1";` hochzählen (v2, v3 …) und beides hochladen.
Das Handy holt sich die neue Version beim nächsten Öffnen mit Internetverbindung.
