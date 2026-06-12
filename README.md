# Anna – Dein persönliches AI-Assistenten-System

Anna ist ein team-basiertes AI-Assistenten-System. Sie ist die Orchestratorin und delegiert Fachaufgaben an Spezialisten.

## Team

| Spezialist | Rolle |
|---|---|
| **Anna** | Orchestratorin – Gesprächsführung, Koordination, Delegation |
| **Ida** | Psychologin – empathische Beratung, klinische Psychologie, Leitlinien |
| **Lisa** | Wissenschaftlerin – Recherche, Faktenchecks, Technik & Politik |
| **Karla** | Softwareentwicklerin – Code, Automatisierung, Systempflege, Weiterentwicklung des Assistenten-Systems |
| **Tara** | Journal-Schreiberin – Rohtext in strukturierte Einträge formatieren |
| **Any** | Anytype-Spezialist – Anytype-API-Operationen |

## Kurzbefehle

- `.team` – Team-Übersicht anzeigen
- `.hilfe` – Alle Kurzbefehle auflisten
- `.funktionen` – Fähigkeiten pro Spezialist zeigen
- `.readme` – Diese README anzeigen
- `.session-log` – Erklärung der Session-Log-Arten

## Session-Logs

Anna schreibt bei Bedarf ein Log in `Team Knowledge/session-logs/`, um Sessions-übergreifend Kontinuität zu sichern. Es gibt vier Log-Typen:

| Typ | Wann | Beschreibung |
|---|---|---|
| `close-session` | "Session beenden" | Vollständige Zusammenfassung mit Entscheidungen und nächsten Schritten |
| `proactive` | "Merke dir …" | Wichtiger Insight, den Anna behalten soll |
| `realignment` | "Eigentlich möchte ich …" | Korrektur einer bisherigen Richtung |
| `mid-session-insight` | Von Anna erkannt | Unerwartete Erkenntnis während des Gesprächs |

`.session-log` zeigt dir eine ausführliche, verständliche Erklärung der Typen und ihrer Verwendung.

## Architektur

```
Anna/
├── AGENTS.md              ← Root-Vertrag
├── README.md              ← Diese Datei
├── .user.yaml             ← Username (SSOT)
├── CLAUDE.md              ← Claude-Code-Zeiger
├── opencode.jsonc         ← OpenCode-Konfiguration
├── Team/                  ← Team-Verträge (SSOT)
│   ├── agent-index.md     ← Routing-Tabelle
│   ├── Anna - Orchestratorin/
│   ├── Ida - Psychologin/
│   ├── Lisa - Wissenschaftlerin/
│   ├── Karla - Softwareentwicklerin/
│   ├── Tara - Journal-Schreiberin/
│   └── Any - Anytype-Spezialist/
└── agents/                ← Tool-Shims
```

## Tool-Unabhängigkeit

Das System ist als reine Markdown-Architektur aufgebaut und funktioniert mit OpenCode, Claude Code, Codex oder jedem Chat-LLM. Die Team-Verträge in `Team/` sind der SSOT – die tool-spezifischen Shims in `agents/` sind nur dünne Zeiger.

## Anytype-Synchronisierung

Das Anna-System kann Inhalte in Anytype speichern – angebunden über den Anytype MCP-Server.

### Grundprinzip
- **Git ist SSOT** (Single Source of Truth) – Anytype ist ein paralleler Zugriffsweg
- Alle Anytype-Operationen laufen über den Spezialisten **Any**
- Inhalte werden **1:1 unverändert** gespeichert (keine Zusammenfassung, Kürzung oder Umformatierung)
- Ausnahme: Der Benutzer fragt explizit nach einer Zusammenfassung

### Speicherbare Inhalte
- **Journal-Einträge** – Rohtext → Tara (Formatierung) → Any (Speicherung)
- **Session-Logs** – Werden lokal als `.md` abgelegt und parallel nach Anytype gespiegelt
- **Webseiten & Dokumentation** – Können via `webfetch` geholt und in Anytype archiviert werden
- **Beliebige Notizen** – Können direkt an Any übergeben werden

### Tags
Jeder Anytype-Eintrag erhält automatisch:
- `Erstellt durch AI` (purple)
- `OpenCode` (blue)
- Bei Journal-Einträgen zusätzlich: `Journal` (teal)
- Bei Session-Logs zusätzlich: `Anna Session-Log` (teal)

### Fehlertoleranz
Ist Anytype nicht erreichbar, wird nur lokal gespeichert – der Fehler wird gemeldet, aber das System blockiert nicht.

## Lizenz

MIT License – siehe [LICENSE](./LICENSE) für Details.
