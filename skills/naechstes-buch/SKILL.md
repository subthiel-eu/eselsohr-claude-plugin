---
name: naechstes-buch
description: Schlägt aus dem eigenen Eselsohr-Regal das nächste Buch vor, passend zu Wunsch, Stimmung, Genre oder Länge. Verwenden bei Fragen wie „Was lese ich als Nächstes?“, „Etwas Leichtes für den Urlaub aus meinem Regal?“ oder „Ein ungelesener Krimi unter 400 Seiten?“.
---

Ausdrückliche Wünsche der Person haben immer Vorrang vor dieser Anleitung.

## Kandidaten holen

1. Ruf `list-books` mit `status: "planned"` auf, danach mit `status: "wishlist"`. Nennt die Person ein Genre, gib es als `genre` mit. Will sie nur Bücher, die sie schon besitzt, nimm nur Einträge, bei denen sie ein eigenes Exemplar hat.
2. Gibt es mehr als die erste Seite an Ergebnissen, hol mit `offset` weitere, höchstens so viele, wie du für eine gute Auswahl brauchst.
3. Filtere nach dem, was die Person gesagt hat, etwa Seitenzahl (`pages`). Fehlt eine Angabe zu einem Buch, schließ es nicht stillschweigend aus, sondern sag, dass sie fehlt.
4. Für die zwei bis vier besten Kandidaten ruf `show-book` auf, um Beschreibung, Genres und Bewertungen anderer zu sehen. Mehr Aufrufe nur, wenn die Person ausdrücklich eine längere Liste will.

## Antworten

- Schlag höchstens drei Bücher vor, jeweils mit Titel, Autor·in, Seitenzahl und einem Satz, warum es zur Frage passt. Begründe nur mit Angaben aus den Werkzeugen, etwa Genre, Länge, Beschreibung oder ihren Bewertungen ähnlicher Bücher.
- Verlinke jedes Buch mit seiner `url`.
- Stehen geplante Bücher bereit, nenne sie vor Wunschlisten-Büchern, die die Person vielleicht erst kaufen müsste.
- Findet sich nichts Passendes, sag das offen. Allgemeine Empfehlungen außerhalb von Eselsohr gibst du nur, wenn die Person danach fragt, und kennzeichnest sie klar als nicht aus ihrem Regal.

Verrate keine Handlung über die Klappentexte hinaus. Eintragen oder als „Lese ich gerade“ markieren geht nur in der Eselsohr-App, nicht hier.
