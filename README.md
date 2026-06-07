# Anna – Dein persönliches AI-Assistenten-System

Anna ist ein team-basiertes AI-Assistenten-System. Sie ist die Orchestratorin und delegiert Fachaufgaben an Spezialisten.

## Team

| Spezialist | Rolle |
|---|---|
| **Anna** | Orchestratorin – Gesprächsführung, Koordination, Delegation |
| **Ida** | Psychologin – empathische Beratung, klinische Psychologie, Leitlinien |
| **Lisa** | Wissenschaftlerin – Recherche, Faktenchecks, Technik & Politik |
| **Karla** | Softwareentwicklerin – Code, Automatisierung, Systempflege |
| **Tara** | Journal-Schreiberin – Rohtext in strukturierte Einträge formatieren |
| **Any** | Anytype-Spezialist – Anytype-API-Operationen |

## Kurzbefehle

- `.team` – Team-Übersicht anzeigen
- `.hilfe` – Alle Kurzbefehle auflisten
- `.funktionen` – Fähigkeiten pro Spezialist zeigen
- `.readme` – Diese README anzeigen

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
├── agents/                ← Tool-Shims
└── skills/                ← Tool-Skills
```

## Tool-Unabhängigkeit

Das System ist als reine Markdown-Architektur aufgebaut und funktioniert mit OpenCode, Claude Code, Codex oder jedem Chat-LLM. Die Team-Verträge in `Team/` sind der SSOT – die tool-spezifischen Shims in `agents/` sind nur dünne Zeiger.

## Lizenz

© 2026 Paperless Movement S.L. – lizenziert unter CC BY-NC-SA 4.0
