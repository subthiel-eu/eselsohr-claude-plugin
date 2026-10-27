---
name: ausleihen-ueberblick
description: Überblick über verliehene und ausgeliehene Bücher in Eselsohr, auch aus der Bücherei, mit Rückgabedaten und Überfälligem zuerst. Verwenden bei Fragen wie „Wer hat gerade meine Bücher?“, „Was muss ich bald zurückgeben?“ oder „Welche Büchereibücher sind überfällig?“.
---

Ausdrückliche Wünsche der Person haben immer Vorrang vor dieser Anleitung.

1. Ruf `list-loans` auf. Die Antwort trennt:
   - `lent_out`: eigene Bücher, die gerade bei anderen liegen (`with`, `since`, `due_on`, `overdue`),
   - `borrowed`: Bücher anderer, die die Person gerade hat,
   - `borrowed_elsewhere`: Bücher aus der Bücherei oder von Leuten außerhalb von Eselsohr (`from`, `return_on`, `overdue`),
   - `open_requests`: offene Anfragen.
2. Fragt die Person nach einem bestimmten Zeitraum („diese Woche“), nimm `today` aus `get-overview` als Bezug oder `list-dates` mit `kind: "return"` bzw. `kind: "loan"`.

## Antworten

- Überfälliges zuerst, dann was in den nächsten Tagen fällig ist, dann der Rest.
- Je Buch: Titel, bei wem bzw. von wem, seit wann, bis wann, mit Link (`url`).
- Leere Gruppen weglassen.
- Bittet die Person um eine freundliche Erinnerung an jemanden, formuliere einen kurzen Text zum Kopieren. Verschicken kann diese Verbindung nichts. Rückgaben bestätigen oder verlängern geht in der Eselsohr-App.

Nenne keine Mail-Adressen oder Kontaktdaten, die nicht in den Werkzeugergebnissen stehen.
