---
type: proactive
agent_id: anna
date: 2026-06-07
linked_tasks: []
---

# Agent-Wechsel-Möglichkeiten für Entwicklungs-Sessions

## Insight
Für längere Entwicklungs-Sessions, bei denen Elias direkt mit Karla arbeiten möchte, gibt es zwei Varianten:

**Variante A – Task-basierter Direktmodus:**
Anna startet einen fortlaufenden Karla-Task (via `task_id`). Elias schreibt weiterhin Anna, aber Anna leitet Nachrichten 1:1 an Karla weiter. Vorteil: Kontext bleibt erhalten (Anna weiss, was besprochen wurde). Nachteil: Anna ist als "Zwischenstation" immer noch im Weg.

**Variante B – /switch agent in OpenCode:**
Elias nutzt den nativen OpenCode-Befehl `/switch agent karla` und spricht direkt mit Karla ohne Umweg. Beim Rücksprung `/switch agent anna` startet Anna frisch. Vorteil: Direkter Zugriff. Nachteil: Beim Wechsel geht Kontext verloren.

**Lösungsansätze:**
- Pragmatisch: Kombination beider Varianten je nach Bedarf
- Systematisch: Briefing-Konvention (Karla schreibt relevanten Kontext in eine Datei, die Anna beim Zurückwechseln lesen kann)

## Begründung
Der Workflow "Anna für Gespräch, Karla für Entwicklung" ist zentral für das System. Ein sauberer Wechsel-Mechanismus ist wichtig für die Produktivität.

## Mögliche Auswirkungen
- Bei Bedarf kann Karla ein Briefing-System bauen, das Kontext zwischen den Agenten transportiert
- Macht das System insgesamt flexibler
