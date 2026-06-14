# /playtest

Starte einen lokalen Play-Test mit dem AI-PlayTest-Skill.

## Verhalten

Nutze den Skill `playtest` und führe die Startabfrage aus:

1. Was soll getestet werden?
2. Welche lokale oder Staging-Umgebung soll genutzt werden?
3. Aus welcher Rolle soll getestet werden?
4. Welche Funktionen gehören in die Checkliste?
5. Gibt es Testdaten oder Testzugänge?
6. Sollen mehrere Rollen oder Sub-Agenten simuliert werden?
7. Welche Zusatzwerkzeuge sind vorhanden und dürfen genutzt werden?

Prüfe vor dem Start, ob Superpowers-Skills, Playwright/Browser-Tools, Caveman-Skills, Sub-Agent-/Multi-Agent-Funktionen, DEV-/Deploy-Skills oder passende MCP-Server vorhanden sind. Frage den Nutzer, welche davon du nutzen darfst.

Lege anschließend einen lokalen Play-Test-Ordner an, bevorzugt mit:

```bash
python3 ~/.claude/skills/playtest/scripts/init_playtest.py --mode local --root .
```

Wenn das Script nicht verfügbar ist, lege die Struktur manuell an.

## Sicherheitsregeln

- Keine Secrets, Tokens, Passwörter oder personenbezogenen Daten in Testdateien schreiben.
- **Lokal-only:** `PLAYTEST/`, Play-Test-Branches (`PlayTest*`) und Backups bleiben **lokal** — nie committen, nie zu GitHub pushen, nie deployen. `PLAYTEST/`, `BACKUPS/`, `*.sql*` und `.env*` (außer `.env.example`) müssen in `.gitignore` stehen. Nur `main` pushen, niemals `git push --all`.
- Schreibe keine produktiven Daten, wenn der Nutzer keinen Live-Test verlangt hat.

## Ergebnis

Am Ende kurz berichten:

- Play-Test-Ordner
- getestete Rolle
- getestete Funktionen
- was funktioniert
- was nicht funktioniert
- wichtigste Bugs
- nächste Todos
