---
name: lesejahr-rueckblick
description: Erstellt einen persönlichen Rückblick auf ein Lesejahr aus Eselsohr, mit Anzahl Bücher, Seiten, Lieblingen, Formaten und Genres. Verwenden bei Fragen wie „Wie war mein Lesejahr?“, „Wie viele Bücher habe ich 2026 gelesen?“ oder „Welche Genres habe ich dieses Jahr gelesen?“.
---

Ausdrückliche Wünsche der Person haben immer Vorrang vor dieser Anleitung.

1. Bestimme das Jahr. Ohne Angabe nimm das aktuelle Jahr aus `today` von `get-overview`. Dort stehen auch `read_this_year` und das `reading_goal`.
2. Ruf `list-books` mit `status: "read"` und `finished_year` auf. Hol mit `limit` und `offset` alle Seiten, bis keine Bücher mehr kommen.
3. Werte aus, was die Liste hergibt:
   - Anzahl der Bücher und Summe der Seiten (Bücher ohne `pages` zählst du nicht mit und sagst, wie viele das sind),
   - Lieblingsbücher (`favorite`) und die am besten bewerteten,
   - gedruckt, E-Book und Hörbuch (`read_as`),
   - der stärkste Monat nach `finished_at`.
4. Genres stehen nicht in der Liste. Fragt die Person danach, ruf `show-book` für die gelesenen Bücher auf, bei mehr als 30 Büchern nur für eine Auswahl, und sag, dass die Auswertung auf dieser Auswahl beruht.

## Antworten

Ein kurzer, warmer Rückblick mit den Zahlen oben, danach die Lieblinge mit Link (`url`). Vergleiche mit dem Leseziel, ohne zu werten, ob das viel oder wenig ist. Zahlen kommen ausschließlich aus den Werkzeugen, nichts schätzen oder auffüllen.

Ein teilbares Bild des Lesejahrs gibt es in der Eselsohr-App unter „Mein Lesejahr“, darauf kannst du hinweisen.
