---
description: Commit alle endringer, bump service worker cache-versjon, og push til GitHub
---

Gjør følgende i rekkefølge:

1. Kjør `git diff --stat` og `git status` for å se hva som er endret
2. Bump service worker cache-versjonen i `sw.js` (finn gjeldende versjon og øk tallet med 1, f.eks. `kurv-v6` → `kurv-v7`)
3. Stage alle endrede filer med `git add`
4. Lag en commit med en beskrivende norsk commit-melding basert på endringene (bruk imperativ form, maks 72 tegn på første linje)
5. Push til `origin main`
6. Bekreft at alt gikk bra med `git log --oneline -3`
