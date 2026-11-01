# Beiträge

Die Repositories der Organisation `fixplay-orga` werden von Fixplay gepflegt.
Beiträge sind willkommen — für `fixplay-diagnoseTool` gilt die MIT-Lizenz, für
alle anderen Repositories die Rechte des Eigentümers.

## Bevor du einen Pull Request öffnest

- Bei Fehlern und Ideen zuerst ein Issue anlegen (Ausnahme: Sicherheitslücken,
  siehe [`SECURITY.md`](SECURITY.md)).
- Änderungen klein und nachvollziehbar halten; ein PR = ein Thema.
- Die projektspezifischen Hinweise in `CLAUDE.md` und `README.md` des
  jeweiligen Repositories beachten (Build-, Test- und Release-Befehle).

## Qualität

- Tests und Lint müssen grün sein; die CI prüft das je Repository.
- Commit-Nachrichten im Conventional-Commit-Stil (`feat:`, `fix:`, `docs:`,
  `chore:`, `test:`, `ci:`).
- Keine Secrets, Zugangsdaten oder personenbezogenen Daten committen.

## Release

Versionen werden über Git-Tags ausgeliefert (`v*` im Backend und im
diagnoseTool, `web-v*` für Web-Images). Nicht eigenmächtig taggen oder
veröffentlichen.
