# Playtest lokal

Ein lokaler Play-Test prüft Funktionen in deiner Entwicklungsumgebung, bevor sie in Staging oder Live landen.

## Wann lokal testen?

- Nach einem neuen Feature.
- Nach Bugfixes.
- Vor einem Pull Request.
- Vor einem Deploy.
- Wenn du UX, Formularlogik oder Speicherverhalten prüfen willst.

## Typischer Ablauf

1. Agent startet Startabfrage.
2. Agent prüft vorhandene Zusatzwerkzeuge.
3. Nutzer erlaubt oder verbietet Zusatzwerkzeuge.
4. Agent legt `PLAYTEST/Playtest-local_DD-MM-YYYY-X/` an.
5. Agent startet lokale App oder nutzt bestehende URL.
6. Agent testet Funktionen aus der definierten Rolle.
7. Agent dokumentiert währenddessen.
8. Agent fasst am Ende zusammen.

## Beispiel: Website

```text
/playtest
Teste die Startseite und Kontaktstrecke lokal.
Rolle: neuer Besucher.
Wichtig sind Verständlichkeit, mobile Darstellung, Formularvalidierung und Datenschutz.
```

Mögliche Checkliste:

- Startseite lädt.
- Navigation funktioniert.
- Kontaktformular zeigt Pflichtfelder.
- Fehlertexte sind verständlich.
- Erfolgsstatus erscheint nach Testversand.
- Keine sensiblen Daten im Browser-Log.

## Beispiel: App

```text
/playtest
Teste die neue Aufgabenverwaltung lokal.
Rolle: Teammitglied, das die App zum ersten Mal nutzt.
Prüfe: Aufgabe erstellen, bearbeiten, erledigen, filtern, löschen.
```

## Beispiel: Editor

```text
/playtest
Teste den lokalen Markdown-Editor.
Rolle: Redakteur.
Prüfe: Dokument öffnen, Titel ändern, Text formatieren, speichern, neu laden.
```

## Was in lokalen Tests erlaubt ist

Meist unkritisch:

- lokale Testdaten anlegen,
- lokale Datenbank zurücksetzen,
- Screenshots speichern,
- Playwright nutzen,
- Logs prüfen,
- Sub-Agenten für Rollen simulieren.

Trotzdem gilt:

- keine echten Secrets protokollieren,
- keine echten Kundendaten kopieren,
- keine lokalen `.env`-Inhalte ins Protokoll schreiben.

