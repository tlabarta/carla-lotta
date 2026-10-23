# Carla-Lotta Fromm – Portfolio

Statische Website, kein Build-Schritt, kein Framework. Alles liegt direkt im Repository.

```
index.html        Startseite
style.css         gemeinsames Stylesheet (Playfair Display für Kopf und Überschriften, EB Garamond für Text)
images/           Abbildungen (eine pro Arbeit, bei Vergleichen zwei) + favicon.svg + platzhalter.svg
pdfs/             Volltexte
files/            Originaldateien (nicht veröffentlicht, siehe .gitignore)
```

## Eine neue Arbeit hinzufügen

1. PDF nach `pdfs/` legen, am besten mit sprechendem Namen: `fromm-kurztitel-jahr.pdf`.
2. Ein Bild (JPG, möglichst 1200–1600 px breit) nach `images/` legen. Große PDFs vorher
   verkleinern (Bilder auf 150 dpi), damit das Repository schlank bleibt.
   Zwei Bilder nebeneinander (Vergleich): `<div class="pair" style="grid-template-columns: Bfr Hfr">`
   mit zwei `<img>`, wobei B und H die Seitenverhältnisse (Breite/Höhe × 1000) der beiden Bilder sind.
3. In `index.html` einen `<article class="work">`-Block kopieren und Bild, Bildunterschrift,
   Titel, Seminarzeile, Abstract und PDF-Link ersetzen (Reihenfolge im Block: Titel, Seminarzeile, Bild, Abstract, Link).

Die Bildunterschrift folgt der kunsthistorischen Konvention:
*Künstler:in, Titel, Jahr, Technik, Sammlung, Ort. Foto: Bildnachweis.*

## Veröffentlichen mit GitHub Pages

1. Neues Repository auf GitHub anlegen, z. B. `carla-lotta.github.io`
   (dann ist die Seite unter `https://carla-lotta.github.io` erreichbar)
   oder ein beliebiger Name (dann unter `https://<nutzer>.github.io/<repo>`).
2. Dateien hochladen bzw. pushen.
3. Unter *Settings → Pages* als Source „Deploy from a branch“, Branch `main`, Ordner `/ (root)` wählen.
4. Nach ein bis zwei Minuten ist die Seite online. `.nojekyll` sorgt dafür, dass GitHub die Dateien unverändert ausliefert.

## Lokal ansehen

```
python3 -m http.server 8000
```

und dann `http://localhost:8000` im Browser öffnen.
