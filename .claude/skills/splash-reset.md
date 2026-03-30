---
description: Nullstill splash-screen slik at den vises på nytt ved neste refresh
---

For å se splash-screenen på nytt:

1. Åpne Safari-konsollen: **Utvikle → Vis JavaScript-konsoll** (`⌥⌘C`)
2. Lim inn og kjør:
   ```js
   localStorage.removeItem('k_ob')
   ```
3. `undefined` i retur er forventet – det betyr at det fungerte
4. Trykk `⌘R` for å refresh

Hvis siden ser gammel ut etter refresh, tøm cachen først: **Utvikle → Tøm hurtigbuffere** (`⌥⌘E`), deretter `⌘R`.
