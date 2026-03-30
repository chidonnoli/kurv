---
description: Gjennomgå siste endringer for bugs, UX-problemer og forbedringer
---

Les `handlelist.html` og kjør `git diff HEAD~3..HEAD` for å se de siste endringene.

Gjennomgå og rapporter:

**Bugs**
- Finnes det JavaScript-feil som kan oppstå (udefinerte variabler, manglende null-sjekker, feil i event handlers)?
- Er alle nye HTML-elementer med `id` referert korrekt i JS?

**UX**
- Er alle nye interaktive elementer touchvennlige (min 44px touch target)?
- Mangler noen loading/feedback-tilstander?
- Er animasjoner konsistente med resten av appen?

**PWA / mobil**
- Er `safe-area-inset` ivaretatt for nye elementer nederst på skjermen?
- Fungerer swipe-interaksjoner fortsatt etter endringene?

**Kode**
- Er det duplisert kode som kan forenkles?
- Er det ubrukte CSS-klasser eller JS-funksjoner etter siste endringer?

Gi konkrete forslag med linjenummer der relevant.
