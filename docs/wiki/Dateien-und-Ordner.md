# Dateien und Ordner

Der Skill erzeugt eine klare lokale Teststruktur.

## Standardstruktur

```text
PLAYTEST/
└── Playtest-live_DD-MM-YYYY-1/
    ├── Test-Aufgabe.md
    ├── Test-Protokoll.md
    ├── Test-Auswertung.md
    ├── Test-Bugfix.md
    ├── Test-Todo.md
    ├── Test-Verbesserungsvorschlaege.md
    └── Artefakte/
```

## Test-Aufgabe.md

Enthält:

- Testziel,
- Umgebung,
- Rolle,
- Checkliste,
- Annahmen,
- Sicherheitsregeln.

## Test-Protokoll.md

Enthält:

- zeitlichen Ablauf,
- Schritte,
- Beobachtungen,
- Status je Funktion,
- Belege,
- bei Live-Tests Backup und Rückbau.

## Test-Auswertung.md

Enthält:

- Gesamturteil,
- was funktioniert,
- was nicht funktioniert,
- Risiken,
- Empfehlung.

## Test-Bugfix.md

Ein Bug sollte enthalten:

- Titel,
- Bereich,
- Schweregrad,
- Schritte zur Reproduktion,
- erwartetes Ergebnis,
- tatsächliches Ergebnis,
- Auswirkung,
- Vorschlag,
- Status.

## Test-Todo.md

Enthält konkrete nächste Aufgaben.

Beispiel:

```text
- [ ] Inventar-Fehler beim Laden prüfen.
- [ ] Fehlermeldung bei ungültigem Formular verbessern.
- [ ] Playwright-Regression für Login ergänzen.
```

## Test-Verbesserungsvorschlaege.md

Enthält Ideen, die keine direkten Bugs sind.

Beispiele:

- bessere Tooltips,
- klarere CTA-Texte,
- schnellere Suche,
- bessere mobile Navigation,
- weniger technische Fehlermeldungen,
- bessere Onboarding-Hinweise.

## Artefakte

Für lokale Belege:

- Screenshots,
- JSON-Reports,
- Konsolenlogs,
- Netzwerkfehler,
- Exportdateien.

Keine Secrets speichern.

