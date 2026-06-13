# /playtest

Starte einen lokalen Play-Test mit dem AI-PlayTest-Skill.

## Verhalten

Nutze `SKILL.md` aus diesem Repository als Arbeitsgrundlage und führe die Startabfrage aus:

1. Was soll getestet werden?
2. Welche lokale oder Staging-Umgebung soll genutzt werden?
3. Aus welcher Rolle soll getestet werden?
4. Welche Funktionen gehören in die Checkliste?
5. Gibt es Testdaten oder Testzugänge?
6. Sollen mehrere Rollen oder Sub-Agenten simuliert werden?

Lege anschließend einen lokalen Play-Test-Ordner an, bevorzugt mit:

```bash
python3 scripts/init_playtest.py --mode local --root .
```

Wenn das Script nicht verfügbar ist, lege die Struktur manuell an.

## Sicherheitsregeln

- Keine Secrets, Tokens, Passwörter oder personenbezogenen Daten in Testdateien schreiben.
- `PLAYTEST/` muss lokal bleiben und in `.gitignore` stehen.
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
