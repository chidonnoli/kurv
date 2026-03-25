# Kurv – Handleliste

## Prosjektoversikt
Kurv er en PWA (Progressive Web App) handleliste-app for iOS/Android. Alt kjører i én enkelt HTML-fil (`handlelist.html`) uten byggesteg eller avhengigheter.

## Teknisk stack
- **Ren HTML/CSS/JS** – ingen rammeverk, ingen npm
- **PWA** med Service Worker (`sw.js`) og manifest (`manifest.json`)
- **LocalStorage** for persistens
- Fonter: Playfair Display (serif) + DM Sans

## Filstruktur
```
handlelist.html   # Hele appen – HTML, CSS og JS i én fil
manifest.json     # PWA-manifest
sw.js             # Service Worker for offline-støtte
```

## Kjøre lokalt
Åpne `handlelist.html` direkte i nettleser, eller bruk en lokal server:
```bash
npx serve .
```

## Arkitektur
All kode ligger i `handlelist.html` delt opp i:
- **CSS** (linje ~15–387): CSS-variabler for lys/mørk modus, komponentstyling
- **HTML** (linje ~389–511): Statisk markup – onboarding, app-shell, sheets
- **JS** (linje ~512–1050): State, render-funksjoner, event handlers

### State-variabler
| Variabel | Beskrivelse |
|---|---|
| `items[]` | Alle handlevarer |
| `LISTS[]` | Listenavn (f.eks. "Ukeshandel") |
| `AL` | Aktiv liste-indeks |
| `weekPlan{}` | Ukesplan (dag → måltider) |
| `hist[]` | Handlingshistorikk |

### Nøkkelfunksjoner
- `render()` – tegner opp hele appen på nytt
- `renderList()` – bygger varelistens DOM, grupperer per butikk/kategori
- `toggle(id)` – haker av/av en vare med animasjon
- `quickAdd()` – legger til vare fra input-feltet i bunnen
- `addSwipe()` – registrerer touch-swipe for å slette varer

### Temaer
CSS-variabler i `[data-theme="light"]` og `[data-theme="dark"]`. Bytt med `toggleDark()`.

## Viktige konvensjoner
- Ikke introduser byggesteg eller avhengigheter – alt skal fungere som ren HTML
- Hold all kode i `handlelist.html` med mindre noe absolutt krever en separat fil
- Bruk CSS-variabler (`var(--accent)` osv.) for alle farger – ikke hardkod
- Animer med CSS-klasser og `animation:`-regler, ikke JS-basert animasjon
- Tekst er på norsk bokmål
