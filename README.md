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

`.session-log` zeigt dir eine ausführliche Beschreibung der Typen und ihrer Verwendung.

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

## Lizenz

MIT License – siehe [LICENSE](./LICENSE) für Details.
