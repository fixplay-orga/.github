# Sicherheitsrichtlinie

## Geltungsbereich

Diese Richtlinie gilt für alle Repositories der Organisation
[`fixplay-orga`](https://github.com/fixplay-orga) und die betriebenen Dienste
(fixplay.de, partners.fixplay.de, Admin-API, Werkstatt-Tools und Apps).

## Schwachstellen melden

Bitte **keine öffentlichen Issues** für Sicherheitslücken anlegen.

- Im betroffenen Repository unter **Security → Report a vulnerability** eine
  vertrauliche Meldung (GitHub Private Vulnerability Reporting) einreichen.
- Alternativ den Repository-Owner direkt kontaktieren; vertrauliche Details
  gehören nicht in einen öffentlichen Kanal.

Hilfreich sind:

- betroffene Komponente und Version bzw. Commit,
- Reproduktionsschritte oder ein Proof of Concept,
- Auswirkung (z. B. Datenzugriff, Rechteausweitung, Verfügbarkeit),
- Hinweise zu einer möglichen Behebung.

## Ablauf

1. Eingang wird bestätigt und die Meldung nachvollzogen.
2. Betroffene Bereiche werden eingegrenzt und eine Behebung vorbereitet.
3. Die Korrektur wird als Security Advisory bzw. privat koordiniert
   veröffentlicht; Credits werden auf Wunsch genannt.
4. Eine Offenlegung erfolgt erst nach Rücksprache und nach Verfügbarkeit eines
   Fixes.

## Umgang mit Secrets

Zugangsdaten, API-Keys und Firebase-Credentials liegen ausschließlich in
`.env`-Dateien bzw. GitHub Secrets und werden nie in Repositories, Issues oder
Screenshots veröffentlicht. Verdächtige Schlüssel bitte melden, nicht
weitergeben.
