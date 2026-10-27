---
name: buch-steckbrief
description: Ein Buch aus Eselsohr auf einen Blick, mit eigenem Lesestand und eigener Bewertung, Zitaten, eigenen Exemplaren, Kreisen, die es lesen, und dem, was andere geschrieben haben, spoilerfrei. Verwenden bei Fragen wie „Was halten andere von Der Schwarm?“, „Was habe ich zu diesem Buch notiert?“ oder „Wer liest das gerade im Kreis?“.
---

Ausdrückliche Wünsche der Person haben immer Vorrang vor dieser Anleitung.

1. Finde das Buch: Ruf `list-books` mit dem Titel als `search` auf. Hat die Person das Buch nicht in ihren Büchern, sag das. Die Werkzeuge kennen dann keine Angaben dazu.
2. Gibt es mehrere Treffer, etwa verschiedene Ausgaben, frag kurz nach oder nimm den, den die Person gerade liest.
3. Ruf `show-book` mit der `id` auf.

## Antworten

Eine kompakte Übersicht, leere Teile weglassen:
- Titel, Autor·in, Reihe und Band, Seiten, Verlag, Erscheinungsjahr, Genres, ein, zwei Sätze aus der Beschreibung.
- Bei der Person: Status, Seite und Fortschritt, ihre Sterne und ihr Text, ihre Zitate, eigene Exemplare und bei wem sie gerade sind.
- Kreise, in denen es Kreisbuch ist (`circle_book_in`).
- Was andere schreiben (`reviews`, `average_rating`): kurz zusammengefasst. Beiträge mit `has_spoiler` nicht wiedergeben, nur erwähnen, dass es sie gibt.

Verlinke das Buch mit `url`. Bewerten, Zitate speichern oder Exemplare eintragen geht in der Eselsohr-App.
