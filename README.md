<p align="center">
  <img src="assets/logo.png" alt="Eselsohr" width="120">
</p>

<h1 align="center">Eselsohr für Claude</h1>

<p align="center">
  Deine Bücher, Lesekreise, Termine und Ausleihen aus <a href="https://mein-eselsohr.de">Eselsohr</a> in Claude, nur lesend.
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/Lizenz-MIT-blue" alt="Lizenz: MIT"></a>
  <img src="https://img.shields.io/badge/Zugriff-nur%20lesend-success" alt="Nur lesend">
  <img src="https://img.shields.io/badge/Sprache-Deutsch-lightgrey" alt="Deutsch">
</p>

---

[Eselsohr](https://mein-eselsohr.de) ist ein soziales Netzwerk für alle, die gern lesen: Lesekreise, die eigene Büchersammlung und Leihen unter Freunden. Mit diesem Plugin fragst du Claude nach deinen eigenen Eselsohr-Daten, zum Beispiel:

- „Was lese ich gerade, und wie weit bin ich?“
- „Schaffe ich den Leseplan meines Lesekreises bis zum nächsten Treffen?“
- „Welches ungelesene Buch aus meinem Regal passt als Nächstes?“
- „Wer hat gerade meine Bücher, und was muss ich bald zurückgeben?“
- „Welche Zitate habe ich zu Mut gespeichert?“

Claude kann in Eselsohr **nichts eintragen, ändern oder löschen**. Es sieht nur, was du selbst in Eselsohr siehst. Du brauchst ein Konto bei [mein-eselsohr.de](https://mein-eselsohr.de). Eselsohr ist auf Deutsch.

## Was drin ist

| Teil | Inhalt |
| --- | --- |
| **MCP-Server** | `https://mein-eselsohr.de/mcp` (HTTP), Anmeldung per OAuth |
| **Skills** | Fertige Abläufe für typische Fragen, siehe unten |

### Werkzeuge des Servers

Alle Werkzeuge lesen nur.

| Werkzeug | Was es liefert |
| --- | --- |
| `get-overview` | Einstieg: was du gerade liest, deine Lesekreise mit Kreisbuch und nächstem Treffen, die Termine der nächsten 14 Tage |
| `list-books` | Deine Bücher (Wunschliste, geplant, lese ich, gelesen) mit Lesestand und eigener Bewertung |
| `show-book` | Ein Buch im Detail mit deiner Bewertung, deinen Zitaten, Exemplaren und öffentlichen Rezensionen anderer (ohne Spoiler) |
| `list-circles` | Deine Lesekreise mit Mitgliedern, Leseplan, nächstem Treffen, Abstimmung und Fragen |
| `list-dates` | Deine Termine: Treffen, Kreis-Termine, Rückgaben, Ausleihen und Vorbestellungen |
| `list-loans` | Verliehene und ausgeliehene Bücher, auch von Hand eingetragene aus der Bücherei |
| `list-quotes` | Deine gespeicherten Zitate mit Seite und Notiz |

### Skills

| Skill | Wofür |
| --- | --- |
| `erste-schritte` | Kurzer Überblick direkt nach dem Verbinden, und was du fragen kannst |
| `treffen-vorbereiten` | Nächstes Treffen mit Leseplan, eigenem Stand und Seiten pro Tag |
| `naechstes-buch` | Vorschlag aus dem eigenen Regal, passend zu Stimmung, Genre oder Länge |
| `buch-steckbrief` | Ein Buch auf einen Blick, mit deinen Notizen und den Meinungen anderer |
| `ausleihen-ueberblick` | Wer hat was, was ist bald fällig, was ist überfällig |
| `reihe-ueberblick` | Welche Bände einer Reihe du hast und wo Lücken sind |
| `zitate-finden` | Gespeicherte Zitate zu einem Wort, Thema oder Buch |
| `lesejahr-rueckblick` | Dein Lesejahr in Zahlen: Bücher, Seiten, Lieblinge, Genres |

## Installieren

### Claude Code

```
/plugin marketplace add subthiel-eu/eselsohr-claude-plugin
/plugin install eselsohr@eselsohr
```

Danach unter `/mcp` bei `eselsohr` die Anmeldung starten, im Browser bei Eselsohr anmelden und der Verbindung zustimmen.

### Claude Desktop und Cowork

Lade das Repo als ZIP herunter (**Code › Download ZIP**) oder baue es selbst. Im ZIP muss der Inhalt dieses Repos direkt liegen, nicht ein Ordner darum:

```
git archive --format=zip -o eselsohr-claude.zip HEAD
```

Das ZIP in Claude als eigenes Plugin hochladen.

### Nur die Verbindung, ohne Skills

Wer keine Skills braucht, fügt in Claude unter **Einstellungen › Konnektoren** einen eigenen Konnektor mit der Adresse `https://mein-eselsohr.de/mcp` hinzu. Die Seite **Einstellungen › KI-Assistent** in Eselsohr erklärt das Schritt für Schritt.

## Datenschutz: welche Daten wohin gehen

- **Anmeldung:** OAuth 2.1 mit dynamischer Client-Registrierung, Scope `mcp:use`. Du meldest dich bei Eselsohr an und stimmst der Verbindung auf der Zustimmungsseite von Eselsohr zu. Claude bekommt kein Passwort, nur ein Zugriffstoken.
- **Was Claude sehen kann:** nur, was du selbst in Eselsohr siehst: deine Bücher, Bewertungen, Zitate, Termine, Ausleihen und deine Lesekreise. Dazu gehören die Namen der Mitglieder deiner Kreise und, soweit sie ihn teilen, ihr Lesefortschritt.
- **Wann Daten fließen:** erst, wenn du Claude etwas zu Eselsohr fragst. Dann ruft Claude die Werkzeuge oben auf, und die Antworten gehen an Anthropic. Dort gelten die [Datenschutzbestimmungen von Anthropic](https://www.anthropic.com/legal/privacy).
- **Was das Plugin selbst schickt:** nichts. Es enthält keinen Code, keine Hooks, kein Tracking und keine Telemetrie, nur die Server-Adresse und Skill-Texte. Es startet auch nichts lokal (kein `npx`, kein `uvx`), der Server läuft bei Eselsohr.
- **Schreiben:** gibt es nicht. Der Server bietet keine Werkzeuge, die etwas eintragen, ändern oder löschen.
- **Trennen:** in Eselsohr unter **Einstellungen › KI-Assistent** siehst du alle verbundenen Assistenten und trennst sie jederzeit.

Ausführlich: [Datenschutzerklärung von Eselsohr](https://mein-eselsohr.de/privacy), Abschnitt „KI-Assistenten“.

## Hilfe und Kontakt

- Fehler oder Wunsch? Am einfachsten über die Feedback-Lasche in [Eselsohr](https://mein-eselsohr.de), oder hier ein [Issue](https://github.com/subthiel-eu/eselsohr-claude-plugin/issues) anlegen.
- [Impressum](https://mein-eselsohr.de/imprint) · [Datenschutz](https://mein-eselsohr.de/privacy) · [Nutzungsbedingungen](https://mein-eselsohr.de/terms)

## Entwicklung

Das Plugin wird zusammen mit Eselsohr gepflegt. Die Skills sind dieselben wie im ChatGPT-Paket von Eselsohr, nur mit „Claude“ statt „ChatGPT“. Neue Texte oder Skills heben die `version` in `.claude-plugin/plugin.json`. Neue Werkzeuge auf dem Server brauchen kein neues Plugin, höchstens angepasste Skills.

Zum Ausprobieren ohne Installation:

```
claude --plugin-dir .
claude plugin validate . --profile directory
```

---

## English

**Eselsohr for Claude** connects Claude to your own data in [Eselsohr](https://mein-eselsohr.de), a German social network for readers with reading circles, a personal book collection and lending between friends. It is **read-only**: Claude can see your books, ratings, quotes, dates, loans and reading circles (including member names and, where they share it, their reading progress), but it cannot create, change or delete anything.

The plugin bundles the remote MCP server `https://mein-eselsohr.de/mcp` (HTTP, OAuth 2.1 with dynamic client registration, scope `mcp:use`) and eight skills. It contains no code, hooks, telemetry or local launchers (`npx`/`uvx`). Data only leaves Eselsohr when you ask Claude about it, and is then processed by Anthropic. Disconnect at any time under **Einstellungen › KI-Assistent** in Eselsohr. Privacy policy: <https://mein-eselsohr.de/privacy>. The service and the skills are in German.

```
/plugin marketplace add subthiel-eu/eselsohr-claude-plugin
/plugin install eselsohr@eselsohr
```

Licensed under the [MIT License](LICENSE).
