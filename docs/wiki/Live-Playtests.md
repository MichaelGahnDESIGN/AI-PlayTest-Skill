# Live Playtests

Live-Tests sind wertvoll, aber riskant. Dieser Skill behandelt Live-Tests deshalb besonders vorsichtig.

## Wann live testen?

- Nach einem Deploy.
- Für produktionsnahe Auth-, Admin-, Editor- oder Payment-Sandbox-Flows.
- Wenn Staging nicht realistisch genug ist.
- Wenn ein Kunde oder Nutzer einen Live-Fehler meldet.

## Pflicht vor schreibenden Live-Tests

Vor jeder schreibenden Live-Aktion muss klar sein:

- Gibt es ein aktuelles Backup?
- Was ist im Backup enthalten?
- Wurde das Backup geprüft?
- Welche Testdaten werden erstellt?
- Wie werden Testdaten zurückgebaut?
- Wie wird der Rückbau geprüft?
- Wer hat die Live-Schreibaktion freigegeben?

## Live-Test ohne Schreibaktion

Read-only ist oft der beste erste Schritt.

Beispiel:

```text
/playtest-live
Teste die öffentliche Website read-only.
Rolle: neuer Besucher.
Nicht registrieren, nichts absenden, keine Daten verändern.
```

## Live-Test mit Schreibaktion

Beispiel:

```text
/playtest-live
Teste den Admin-Editor live.
Erstelle vorher ein Backup.
Nutze einen temporären Testdatensatz mit Marker PlayTest-YYYYMMDD.
Prüfe, ob die Änderung öffentlich übernommen wird.
Setze den Testdatensatz danach zurück und prüfe, dass der Marker nicht mehr sichtbar ist.
```

## Rückbauprüfung

Ein Rückbau ist erst erledigt, wenn geprüft wurde:

- Testdatensatz existiert nicht mehr oder hat Originalwerte.
- Testmarker ist öffentlich nicht mehr sichtbar.
- API/Website/Healthcheck funktioniert.
- Keine temporären Rollen, Nutzer oder Einladungscodes bleiben übrig.

## Was nicht ohne ausdrückliche Freigabe passieren darf

- echte Zahlungen,
- produktive Massenmails,
- echte Nutzerrollen ändern,
- Kundendaten löschen,
- Datenbankmigrationen,
- Deployments,
- externe Webhooks,
- irreversible Admin-Aktionen.

## Dokumentation im Live-Test

In `Test-Protokoll.md` notieren:

- Live-URL,
- Backup-Pfad oder Backup-ID,
- Testmarker,
- erlaubte Schreibaktionen,
- Rückbau-Methode,
- Rückbauprüfung.

In `Test-Auswertung.md` notieren:

- Was funktioniert hat.
- Was nicht funktioniert hat.
- Welche Risiken bleiben.
- Ob Ausgangszustand wiederhergestellt wurde.

