# AI-PlayTest-Skill Wiki

Willkommen im Wiki zum **AI-PlayTest-Skill**.

Dieser Skill hilft KI-Agenten dabei, Software wie echte Nutzer zu testen: nicht nur „läuft der Build?“, sondern „kann ein Mensch diesen Ablauf wirklich benutzen?“.

Der Skill funktioniert für:

- Websites
- Web-Apps
- Admin-Bereiche
- Editoren
- Spiele
- SaaS-Tools
- Shops
- APIs mit UI-Bezug
- interne Tools
- lokale, Staging- und Live-Umgebungen

## Grundidee

Ein Play-Test prüft eine Funktion aus einer Rolle heraus.

Beispiele:

- Eine neue Nutzerin registriert sich zum ersten Mal.
- Ein Admin bearbeitet Inhalte im Editor.
- Ein Spieler erstellt einen Charakter und spielt eine Runde.
- Ein Kunde legt ein Produkt in den Warenkorb.
- Ein Redakteur veröffentlicht eine Seite.
- Ein Support-Mitarbeiter prüft einen Bugreport.

Der Agent notiert währenddessen alles lokal im Projektordner.

## Wichtigste Prinzipien

- Play-Test-Dateien bleiben lokal.
- `PLAYTEST/` gehört in `.gitignore`.
- Keine Passwörter, Tokens oder personenbezogenen Daten in Markdown-Dateien.
- Live-Tests brauchen Backup, Testdaten und Rückbauplan.
- Der Agent fragt, bevor er optionale Tools wie Playwright, Superpowers, Caveman, Sub-Agenten oder DEV-Skills nutzt.
- Am Ende gibt es eine verständliche Auswertung.

## Schnellnavigation

- [[Installation]]
- [[Playtest lokal]]
- [[Live Playtests]]
- [[Beispiel Prompts]]
- [[Sicherheit und Datenschutz]]
- [[Zusatzwerkzeuge und Modelle]]
- [[Dateien und Ordner]]
- [[Troubleshooting]]
- [[Discussions und Community]]
- [[FAQ]]

## Minimaler Start

```text
/playtest
Teste die neue Registrierungsstrecke aus Sicht eines neuen Nutzers.
```

Oder live:

```text
/playtest-live
Teste den Admin-Editor live. Erstelle vorher ein Backup, nutze temporäre Testdaten und setze am Ende alles zurück.
```

## Ergebnis

Nach einem guten Play-Test hast du:

- ein Testprotokoll,
- eine Auswertung,
- eine Bugliste,
- eine Todo-Liste,
- Verbesserungsvorschläge,
- optional Screenshots oder JSON-Reports,
- bei Live-Tests eine Rückbauprüfung.

