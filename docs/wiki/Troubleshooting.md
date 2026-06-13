# Troubleshooting

## `/playtest-live` startet keinen Assistenten

Mögliche Gründe:

- Deine Umgebung unterstützt keine lokalen Slash Commands.
- Der Skill wurde nicht im richtigen Skill-Ordner installiert.
- Die Umgebung hat Skills nicht neu geladen.

Lösung:

```text
Nutze den PlayTest-Skill und starte einen Live-Play-Test.
```

Oder Installation prüfen:

```bash
ls ~/.codex/skills/playtest
ls ~/.claude/skills/playtest
```

## `PLAYTEST/` wird nicht ignoriert

Prüfen:

```bash
git check-ignore PLAYTEST/test.txt
```

Wenn nicht ignoriert:

```bash
echo "PLAYTEST/" >> .gitignore
```

## Script läuft nicht

Prüfen:

```bash
python3 --version
python3 scripts/init_playtest.py --mode local --root .
```

Wenn Python fehlt, Struktur manuell anlegen.

## Live-Test darf nicht schreiben

Dann read-only testen:

```text
Teste live nur lesend. Keine Registrierung, kein Speichern, keine Datenänderung.
```

## Kein sicherer Rückbau möglich

Nicht schreiben.

Stattdessen:

- UI öffnen,
- Validierung prüfen,
- Speichern nicht ausführen,
- fehlenden Rückbaupfad als Risiko dokumentieren.

## Playwright findet keine Texte

Manche Apps rendern stark in Canvas oder Shadow DOM.

Alternativen:

- Screenshots visuell prüfen,
- API-Endpunkte ergänzend testen,
- stabile Test-IDs einbauen,
- Accessibility/Semantics verbessern,
- Browser-Konsole und Netzwerk prüfen.

## Agent schreibt zu viel

Nutze Caveman oder fordere kurze Protokolle:

```text
Nutze knappe Protokolle. Keine langen Erklärungen, nur Status, Beobachtung, Bug, Todo.
```

