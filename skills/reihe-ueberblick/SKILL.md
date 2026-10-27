---
name: reihe-ueberblick
description: Zeigt, welche Bände einer Buchreihe die Person in Eselsohr hat, gelesen hat oder sich wünscht, und wo in ihrer eigenen Sammlung Lücken sind. Verwenden bei Fragen wie „Welche Bände von Harry Potter habe ich?“, „Welcher Band kommt als Nächstes?“ oder „Wo bin ich in der Reihe?“.
---

Ausdrückliche Wünsche der Person haben immer Vorrang vor dieser Anleitung.

1. Ruf `list-books` mit `status: "all"` und dem Namen der Reihe oder der Autorin bzw. des Autors als `search` auf. Hol weitere Seiten mit `offset`, falls nötig.
2. Behalte die Einträge, deren `series` zur gefragten Reihe passt. Sind mehrere Reihen ähnlich benannt, frag nach, welche gemeint ist.
3. Sortiere nach `volume` und ordne jeden Band ein: gelesen, lese ich gerade, geplant, Wunschliste, und ob ein eigenes Exemplar da ist.

## Antworten

- Eine Liste der Bände in Reihenfolge mit Status, jeweils mit Link (`url`).
- Der nächste Band zum Lesen: der erste nach dem höchsten gelesenen, den die Person schon hat oder plant.
- Lücken nur in den eigenen Einträgen benennen, etwa „Band 3 fehlt in deinem Eselsohr“. Ob es weitere oder angekündigte Bände gibt, wissen die Werkzeuge nicht. Sag das ehrlich und verweise auf die Reihenseite in Eselsohr, die über die `url` eines Bands erreichbar ist. Bandzahlen oder Erscheinungstermine nicht erfinden.

Keine Handlung späterer Bände verraten, wenn die Person sie noch nicht gelesen hat.
