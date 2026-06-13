# Beispiel Prompts

Diese Beispiele können direkt angepasst werden.

## Neuer Nutzer einer Website

```text
/playtest
Teste die Website aus Sicht eines neuen Besuchers.
Prüfe Startseite, Navigation, Kontaktformular, mobile Darstellung und rechtliche Links.
Notiere, was verständlich ist und wo Vertrauen fehlt.
```

## Live-Test einer Registrierung

```text
/playtest-live
Teste die Live-Registrierung aus Sicht eines neuen Nutzers.
Nutze nur einen temporären Testaccount.
Speichere keine Zugangsdaten im Protokoll.
Prüfe, ob Login, Logout und Profilanzeige funktionieren.
Lösche oder deaktiviere den Testaccount am Ende, falls möglich.
```

## Admin-Editor

```text
/playtest-live
Teste den Admin-Editor live.
Erstelle vorher ein Backup.
Rolle: Redakteur/Admin.
Prüfe: Datensatz suchen, öffnen, ändern, speichern, öffentlich prüfen, zurücksetzen.
Nutze einen klaren Testmarker und entferne ihn am Ende.
```

## SaaS-Dashboard

```text
/playtest
Teste das Dashboard lokal.
Rolle: Teamlead.
Prüfe: Login, Übersicht, Filter, Export, Detailseite, Fehlermeldungen.
Nutze Playwright, falls vorhanden.
```

## Online-Shop

```text
/playtest
Teste den Warenkorb und Checkout bis vor die Zahlung.
Rolle: neuer Kunde.
Keine echte Zahlung ausführen.
Prüfe: Produkt suchen, Warenkorb, Adresse, Versand, Fehlermeldungen, Datenschutztexte.
```

## Spiel oder Gamified App

```text
/playtest
Teste das Spiel aus Sicht eines erfahrenen Spielers, der es zum ersten Mal sieht.
Prüfe: Einstieg, Tutorial, Charakterauswahl, erste Aktion, Inventar, Speichern, Wiederaufnahme.
Simuliere weitere Spieler nur, wenn Sub-Agenten erlaubt sind.
```

## API mit UI-Bezug

```text
/playtest
Teste die neue Suchfunktion über UI und API.
Rolle: Power-User.
Prüfe: Sucheingabe, Filter, leere Ergebnisse, Fehlerzustände, API-Antwort und Anzeige in der Oberfläche.
```

## Barrierearmut

```text
/playtest
Teste die Oberfläche aus Sicht eines Tastaturnutzers.
Prüfe Fokusreihenfolge, sichtbare Fokuszustände, Formularlabels, Fehlermeldungen und Kontraste.
```

## Mobile Nutzung

```text
/playtest
Teste die App auf mobiler Breite.
Rolle: Nutzer unterwegs.
Prüfe Navigation, Lesbarkeit, Buttons, Formulare, Scrollverhalten und Layoutbrüche.
```

## Regression nach Bugfix

```text
/playtest
Teste den Bugfix für [BUG-ID].
Reproduziere zuerst die alte Fehlerstrecke.
Prüfe dann, ob der Fehler weg ist.
Teste zusätzlich eine angrenzende Funktion, die durch den Fix betroffen sein könnte.
```

