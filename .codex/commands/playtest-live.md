# /playtest-live

Starte einen Live-Play-Test mit dem AI-PlayTest-Skill.

## Verhalten

Nutze `SKILL.md` aus diesem Repository als Arbeitsgrundlage und führe vor allen Schreibaktionen die Live-Startabfrage aus:

1. Was soll live getestet werden?
2. Welche Live-URL oder Live-App ist betroffen?
3. Aus welcher Rolle soll getestet werden?
4. Welche Funktionen gehören in die Checkliste?
5. Welche Testzugänge, Einladungscodes oder Testdaten sind erlaubt?
6. Wo liegt das Backup oder wie wird es erstellt?
7. Wie werden Testdaten am Ende zurückgebaut?
8. Sollen mehrere Rollen oder Sub-Agenten simuliert werden?

Lege anschließend einen lokalen Live-Play-Test-Ordner an, bevorzugt mit:

```bash
python3 scripts/init_playtest.py --mode live --root .
```

Wenn das Script nicht verfügbar ist, lege die Struktur manuell an.

## Live-Sicherheitsregeln

- Keine schreibende Live-Aktion ohne Backup oder geprüften Rückfallpunkt.
- Keine Live-Testdaten ohne Rückbauplan.
- Keine Secrets, Tokens, Passwörter, Zahlungsdaten oder personenbezogenen Daten in Testdateien schreiben.
- Testdaten klar markieren.
- Rückbau am Ende durchführen und prüfen.
- Wenn Rückbau nicht sicher möglich ist, nur read-only testen oder nach Freigabe fragen.

## Ergebnis

Am Ende kurz berichten:

- Play-Test-Ordner
- Backup/Rückfallpunkt
- getestete Rolle
- getestete Funktionen
- was funktioniert
- was nicht funktioniert
- Rückbauprüfung
- wichtigste Bugs
- nächste Todos
