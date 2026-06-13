# Zusatzwerkzeuge und Modelle

Der PlayTest-Skill bleibt absichtlich allgemein. Zusatzwerkzeuge können ihn deutlich stärker machen.

## Der Skill fragt zuerst

Der Agent soll prüfen, was vorhanden ist, und fragen:

```text
Ich habe Playwright, Superpowers und einen DEV-Skill gefunden.
Darf ich sie für diesen Play-Test nutzen?
```

## Empfohlene Zusatzwerkzeuge

### Playwright oder Browser-Tools

Gut für:

- echte Klickpfade,
- Screenshots,
- Konsolenfehler,
- Netzwerkfehler,
- mobile Viewports,
- Regressionstests.

### Superpowers-Skills

Gut für:

- strukturierte Planung,
- systematisches Debugging,
- Test-Driven Development,
- Verifikation vor Abschluss,
- Code Review.

### Caveman-Skills

Gut für:

- sehr kurze Statusmeldungen,
- kompakte Protokollzusammenfassungen,
- geringeren Tokenverbrauch.

### Sub-Agenten und Multi-Agenten

Gut für:

- mehrere Nutzerrollen,
- Admin und Nutzer parallel,
- Spieler und Spielleiter,
- Käufer und Support,
- Reviewer und Redakteur.

### DEV-/Deploy-Skills

Gut für:

- Backup,
- Restore-Plan,
- Staging,
- Live-Checks,
- Deploy-Prüfung,
- Rückbau.

## Modell-Empfehlungen

Kurzfassung:

- einfache lokale Tests: schnelles, günstiges Coding-/Reasoning-Modell reicht oft.
- komplexe Live-Tests: stärkeres Reasoning-/Coding-Modell nutzen.
- riskante Admin-, Datenbank-, Zahlungs- oder Deploy-Tests: bestes verfügbares Modell nutzen.

Beispiele:

- Claude Code: Sonnet 4.6 oder höher, bei sehr riskanten Aufgaben Opus 4.8 oder aktueller.
- ChatGPT Codex: GPT-5-Codex oder neuestes Codex-Modell.
- ChatGPT Cowork: GPT-5.5 oder aktuelles bestes Reasoning-/Coding-Modell.

Wichtig: Modellnamen ändern sich. Nutze im Zweifel das aktuell beste Coding-/Agentenmodell deiner Umgebung.

