# Sicherheit und Datenschutz

Der PlayTest-Skill soll beim Testen helfen, ohne sensible Daten zu verbreiten.

## Niemals protokollieren

- Passwörter
- API-Keys
- Tokens
- Session-Cookies
- Einmalcodes
- echte E-Mail-Inhalte
- Zahlungsdaten
- private Kundendaten
- vollständige personenbezogene Profile
- geheime Serverpfade mit Zugangsdaten

## Screenshots

Screenshots sind hilfreich, aber riskant.

Vor Screenshots prüfen:

- Sind E-Mail-Adressen sichtbar?
- Sind Namen, Rechnungsdaten oder Profile sichtbar?
- Sind Tokens oder interne URLs sichtbar?
- Sind Admin-Geheimnisse sichtbar?

Wenn ja:

- keinen Screenshot erstellen,
- Screenshot lokal halten,
- sensible Bereiche schwärzen,
- nur abstrakt beschreiben.

## Testaccounts

Gute Testaccounts:

- sind klar als Test erkennbar,
- nutzen keine echten persönlichen Daten,
- haben minimale Rechte,
- werden nach dem Test gelöscht oder deaktiviert,
- besitzen keine produktiven Zahlungsdaten.

## Live-Tests

Live-Tests brauchen besondere Vorsicht:

- Backup erstellen oder prüfen.
- Testmarker verwenden.
- Testdaten zurückbauen.
- Rückbau prüfen.
- Keine echten Nutzer stören.
- Keine externen Nebenwirkungen auslösen.

## Zahlungsfunktionen

Nur testen, wenn Sandbox/Testmodus aktiv ist.

Nicht erlaubt ohne Freigabe:

- echte Abbuchung,
- echte Rechnung,
- echtes Abo,
- echte Rückerstattung,
- echte Zahlungsdaten speichern.

## Gute Protokollsprache

Schlecht:

```text
Login mit max@example.com und Passwort ...
```

Gut:

```text
Login mit temporärem Testaccount erfolgreich. Zugangsdaten wurden nicht protokolliert.
```

Schlecht:

```text
Token eyJ...
```

Gut:

```text
API lieferte einen Auth-Token. Token wurde nicht gespeichert.
```

