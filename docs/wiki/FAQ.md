# FAQ

## Ist das ein Ersatz für Unit-Tests?

Nein. Play-Tests ergänzen Unit-, Integration- und E2E-Tests. Sie prüfen den Ablauf aus Nutzersicht.

## Muss ich Playwright nutzen?

Nein. Playwright ist optional. Der Skill fragt, ob passende Tools vorhanden sind und genutzt werden dürfen.

## Werden Play-Test-Dateien committed?

Nein. Standardmäßig wird `PLAYTEST/` in `.gitignore` eingetragen.

## Darf der Agent live schreiben?

Nur mit Backup, Rückbauplan und Freigabe.

## Kann der Skill mehrere Nutzer simulieren?

Ja, wenn Sub-Agenten oder Multi-Agent-Workflows verfügbar und erlaubt sind. Sonst simuliert der Hauptagent die Rollen nacheinander.

## Was passiert bei Zugangsdaten?

Der Agent darf sie verwenden, wenn du sie sicher bereitstellst. Er darf sie aber nicht in Testdateien schreiben.

## Was passiert, wenn kein Backup existiert?

Dann darf der Agent keine riskanten Live-Schreibaktionen durchführen. Er testet read-only oder fragt nach Freigabe und Backup-Weg.

## Ist der Skill deutsch oder englisch?

Die aktuelle Dokumentation ist deutsch. Der Skill kann aber in anderen Sprachen verwendet werden, wenn der Nutzer das verlangt.

## Wie token-sparsam ist der Skill?

Der eigentliche `SKILL.md` ist bewusst kompakt. Ausführliche Erklärungen stehen im README und Wiki, damit Agenten sie nur lesen, wenn sie gebraucht werden.

