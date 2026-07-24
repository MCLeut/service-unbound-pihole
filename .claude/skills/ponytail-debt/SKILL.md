---
name: ponytail-debt
description: >
  Sammelt alle ponytail: -Kommentare des Repos in ein Schulden-Ledger, damit
  bewusste Abkürzungen getrackt werden statt still zu verrotten. Einsetzen bei
  "ponytail debt", "ponytail ledger", "was wurde abgekürzt", "welche Shortcuts
  sind offen". One-shot-Report, ändert nichts.
---

# Ponytail-Debt-Ledger (Projektfassung)

> Basis: DietrichGebert/ponytail skills/ponytail-debt/SKILL.md (MIT), Stand
> 2026-07-24. Lokal adaptiert: Kommentar-Präfixe und Ausschlüsse auf diesen
> Stack gemappt.

Jede bewusste Ponytail-Abkürzung trägt einen "ponytail:"-Kommentar mit Decke und
Upgrade-Pfad. Dieser Skill sammelt sie in ein Ledger, damit aus "später" nie
"nie" wird.

## Scan

grep -rnE '#\s*ponytail:' . --exclude-dir=.git --exclude-dir=.serena --exclude-dir=.repomix

Dieses Repo ist durchgehend `#`-Kommentar-Stacks (Dockerfile, `start.sh`
Bash, `unbound.conf`, `build.ps1` PowerShell, `.gitignore`) -- ein einziges
Präfix deckt alle Dateien ab. Der Kommentar-Präfix hält Prosa, die die
Konvention nur erwähnt, aus dem Ledger heraus.

## Output

Eine Zeile pro Marker, gruppiert nach Datei:

"<datei>:<zeile>, <was vereinfacht wurde>. Decke: <benannte Grenze>. Upgrade: <Auslöser zum Nachrüsten>."

Rot-Risiko flaggen: jeder "ponytail:"-Kommentar ohne Upgrade-Pfad oder Auslöser
bekommt ein "no-trigger"-Tag.

Abschluss: "<N> Marker, <M> ohne Auslöser." Nichts gefunden: "Kein ponytail:-Debt. Ledger sauber."

## Grenzen

Liest und berichtet nur, ändert nichts. Persistieren nur auf Zuruf (dann nach
PONYTAIL-DEBT.md). One-shot.
