---
description: Sjekk at CSS og design i handlelist.html følger Heirloom-designsystemet
---

Les `stitch_kurv/kurv_heirloom/DESIGN.md` og deretter CSS-seksjonen i `handlelist.html`.

Sjekk følgende punkter og rapporter avvik:

**Farger**
- Brukes CSS-variabler (`var(--accent)` osv.) overalt – ingen hardkodede fargeverdier?
- Er fargeverdiene i `[data-theme="light"]` og `[data-theme="dark"]` i tråd med Heirloom-paletten?

**"No-Line"-regelen**
- Finnes det `border: 1px solid` noe sted som separerer seksjoner eller containere? (Ghost borders på 15% opacity er OK)
- Er separasjon oppnådd via bakgrunnsfargeoverganger i stedet?

**Typografi**
- Brukes Playfair Display til titler, tomme tilstander og seksjonshoder?
- Brukes DM Sans til listeinnhold og UI?
- Brukes uppercase + letter-spacing til label-metadata?

**Knapper**
- Har primærknapper gradient (`var(--btn-grad)`)?
- Har primærknapper `border-radius: 9999px` (pill-form)?

**Glassmorphism**
- Har headeren `backdrop-filter: blur(20px)` og semi-transparent bakgrunn?

**Skygger**
- Brukes myke skygger (`var(--sh)`, `var(--sh2)`) i stedet for harde?

List opp konkrete linjenummer og foreslå fixes for alle avvik du finner.
