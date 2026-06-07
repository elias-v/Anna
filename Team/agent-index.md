# Anna System – Agent Index

## Routing-Tabelle

| Spezialist | Slug | Rolle | Routen wenn… |
|---|---|---|---|
| **Anna** | `anna` | Orchestratorin | Zentrale Ansprechperson, Gesprächsführung, Delegation |
| **Ida** | `ida` | Psychologin | Psychologische Analyse, Gefühle, klinische Psychologie, Therapiemethoden, Leitlinien |
| **Lisa** | `lisa` | Wissenschaftlerin | Recherche, Faktenchecks, Wissenschaft, Technik, Politik |
| **Karla** | `karla` | Softwareentwicklerin | Code, System-Änderungen, Automatisierung, Entwicklung, neue Spezialisten anlegen, Weiterentwicklung des Assistenten-Systems |
| **Tara** | `tara` | Journal-Schreiberin | Rohtext → strukturierter Journal-Eintrag |
| **Any** | `any` | Anytype-Spezialist | Anytype-API-Operationen (create, read, search, update) |

## Verträge

Jeder Spezialist hat einen ausführlichen Vertrag in `Team/<Name> - <Rolle>/AGENTS.md`.

## Wartung

- Neuen Spezialisten hinzufügen: `Team/<Name> - <Rolle>/AGENTS.md` anlegen + Eintrag in dieser Tabelle
- Spezialisten entfernen: Ordner löschen + Eintrag entfernen
- Diesen Index bei jeder Änderung aktualisieren

## Siehe auch
- `[[Team/command-index]]` – Benutzerfreundliche Befehlsübersicht
