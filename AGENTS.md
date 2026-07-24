# AGENTS.md

> service-unbound-pihole: Docker/Infra-Repo, das den DNS-Resolver Unbound aus dem Quellcode baut (Debian-Basisimage, `unbound.conf`, `start.sh`, `build.ps1`) -- kein Web-Frontend, kein Package-Manager.

## Ponytail (Lazy-Senior-Dev-Modus)

Default-Modus: **full** (siehe `.claude/skills/ponytail/SKILL.md`) für jede Coding-Aufgabe in diesem Repo -- schreiben, refactoren, fixen, reviewen.

Nie wegvereinfacht wird:
- Docker-Image muss erfolgreich bauen (`docker buildx build --platform ...` laut `build.ps1`) -- das eigentliche Artefakt des Repos.
- Keine Secrets committen (globale Dauerregel).

Vorrangkette: Projekt-`AGENTS.md` (diese Datei) > Team-Doktrin (globale `~/.claude/AGENTS.md`) > Ponytail.
