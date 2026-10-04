# Werkuren-app — online zetten met GitHub Pages

Deze map is klaar om te publiceren: **4 MB, 28 bestanden**, geen enkel bestand
boven de 2,5 MB. Daarmee blijft hij ruim onder de upload-limieten van GitHub.

Alle bestanden horen in de **hoofdmap** van de repository, niet in een submap.

De app is gebouwd voor een repository die **`werkuren`** heet, dus het adres wordt:

    https://<jouw-gebruikersnaam>.github.io/werkuren/

---

## Stap 1 — Repository aanmaken

Ga naar https://github.com/new en maak een repository met de naam **`werkuren`**.

- Zet hem op **Public** (Pages werkt op de gratis versie alleen voor publieke repo's).
- Vink *Add a README* niet aan.

## Stap 2 — Bestanden uploaden

1. Pak deze zip uit op je computer.
2. Open de repository in je browser.
3. Klik op **Add file** → **Upload files** (rechts boven de bestandenlijst).
4. Sleep **alle** bestanden en mappen uit de uitgepakte map naar binnen.
   Let op de verborgen map: **`.nojekyll`** moet mee.
   - macOS: druk op **Cmd + Shift + .** om verborgen bestanden te zien.
   - Windows: Verkenner → **Weergave** → **Verborgen items** aanvinken.
5. Klik op **Commit changes**.

Controleer daarna of je in de hoofdmap dit ziet staan:

    assets/    icons/    index.html    main.dart.js    manifest.json
    favicon.png    logo.png    .nojekyll

## Stap 3 — Pages aanzetten

1. **Settings** → links **Pages**.
2. *Source*: **Deploy from a branch**.
3. *Branch*: **main**, map **/ (root)** → **Save**.

Na een minuut of twee staat de app live op:

    https://<gebruikersnaam>.github.io/werkuren/

## Stap 4 — Op je telefoon

Open dat adres in de browser en kies *Toevoegen aan beginscherm*. De app opent
dan als een gewone app met het KW-icoon.

---

## Als het uploaden in de browser blijft mislukken

GitHub's web-upload is beperkt. Gebruik dan een **lokale kloon** — dat is ook
wat GitHub zelf aanraadt bij deze fout. Twee manieren:

**Met GitHub Desktop** (aanrader als je niet met Git werkt)

1. Download https://desktop.github.com en log in.
2. **File** → **Clone repository** → kies `werkuren` → kies een lege map.
3. Pak deze zip uit in die map, zodat `index.html` naast `assets` en `icons` staat.
4. Onderaan een omschrijving invullen → **Commit to main** → **Push origin**.

**Met Git vanaf de opdrachtregel**

    git clone https://github.com/<gebruikersnaam>/werkuren.git
    cd werkuren
    # pak hier de zip inhoud uit
    git add -A
    git commit -m "Werkuren-app online"
    git push

Bij beide routes gaan verborgen bestanden zoals `.nojekyll` automatisch mee.

---

## Belangrijk om te weten

**De uren staan per apparaat.** Alles wordt bewaard in de browseropslag van het
toestel waarop je werkt. Vul je uren in op je telefoon, dan zie je ze niet
automatisch op je laptop. Gebruik voorlopig één apparaat.

**Wis je browsergegevens niet** zonder erbij na te denken: dan zijn de uren weg.
De app maakt geen reservekopie.

**De app haalt één onderdeel van internet.** Flutter laadt zijn tekenmodule van
Google's CDN. Dat is de standaardinstelling en werkt op elke hosting, maar het
betekent wel dat de app internet nodig heeft — wat voor een webapp toch geldt.

**Een andere repositorynaam?** Dan moet de app opnieuw gebouwd worden met dat
pad, anders laadt hij niet.

**Eigen domein?** Later mogelijk via Settings → Pages → Custom domain.

---

## Wat er in deze map zit

| Bestand / map | Waarvoor |
|---|---|
| `index.html` | de pagina zelf, met het laadscherm en het logo |
| `main.dart.js` | de hele app |
| `assets/` | logo's, lettertypes, app-gegevens |
| `icons/` | de app-iconen voor je beginscherm |
| `logo.png`, `logo_monogram.png` | het logo in de app en op het laadscherm |
| `favicon.png` | het tabblad-icoon |
| `manifest.json` | maakt hem installeerbaar als app |
| `.nojekyll` | **verplicht** — zonder dit laat GitHub Pages bestanden weg |

