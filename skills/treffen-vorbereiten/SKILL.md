---
name: treffen-vorbereiten
description: Bereitet das nächste Lesekreis-Treffen in Eselsohr vor, mit Termin, Leseplan, eigenem Lesestand, Seiten pro Tag und den Fragen des Kreises. Verwenden bei Fragen wie „Schaffe ich das Kreisbuch bis zum Treffen?“, „Wann treffen wir uns?“ oder „Was besprechen wir beim nächsten Treffen?“.
---

Ausdrückliche Wünsche der Person haben immer Vorrang vor dieser Anleitung.

1. Ruf `list-circles` auf. Ist die Person in mehreren Kreisen und nennt keinen, nimm den Kreis mit dem nächsten Treffen und sag, welchen du genommen hast.
2. Aus der Antwort brauchst du:
   - `next_meeting`: Datum, Uhrzeit, Ort oder `online_url`, Gastgeber·in, wer zugesagt hat (`coming`, `not_coming`) und die eigene Antwort (`my_answer`),
   - `circle_book` mit `reading_plan`: die Etappe, die bis zum Treffen fällig ist (`due_on`, Zielseite),
   - den eigenen Lesestand (`my_shelf.current_page`) und `members_progress`,
   - `discussion_questions`, falls es welche gibt.
3. Rechne aus, wie viele Seiten die Person bis zum Treffen noch lesen muss und wie viele das pro Tag sind. Nimm dafür `today` aus `get-overview`, falls du das heutige Datum nicht sicher kennst. Fehlt ein Leseplan, rechne bis zum Ende des Buchs, und sag das dazu.

## Antworten

Gib eine kurze Übersicht:
- Wann und wo, wer kommt, und ob die Person schon zugesagt hat.
- Lesestand: „Du bist auf Seite X, bis zum Treffen sollen es Y sein. Das sind Z Seiten, etwa N pro Tag.“
- Wie weit die anderen sind, nur in Zahlen aus `members_progress`, ohne Bewertung.
- Die Fragen des Kreises, falls vorhanden. Eigene Diskussionsideen nur, wenn die Person danach fragt, und dann ohne Handlung über ihre aktuelle Seite hinaus.

Keine Spoiler: Verrate nichts aus Teilen des Buchs, die nach der aktuellen Seite der Person liegen. Zusagen, absagen oder die Seite eintragen geht nur in der Eselsohr-App, verlinke dafür die `url` des Kreises.
