# .modelwahl – Dynamischer Recherche-Prompt

**Führe folgende Recherche durch und formatiere das Ergebnis exakt wie unten beschrieben:**

1. **Recherchiere** die aktuell (heutiges Datum) kostenlos nutzbaren AI-Modelle auf folgenden Plattformen:
   - **OpenCode Zen**: Offizielle Seite prüfen (opencode.ai/docs/de/zen/)
   - **Ollama Cloud**: Offizielle Seite prüfen (ollama.com/pricing)
   - **OpenRouter**: Offizielle Sammlung prüfen (openrouter.ai/collections/free-models)
2. **Gruppiere** die Modelle in genau diese vier Kategorien: **Allgemeines Reasoning**, **Coding**, **Agentisches Arbeiten**, **Websuche**
3. **Wähle pro Kategorie die 3 besten Modelle** aus (Platz 1 = bestes, Platz 2 = zweitbestes, Platz 3 = drittbestes)
4. **Gib NUR die Liste aus** – keine Einleitung, keine Erklärungen, keine Quellenangaben, keine Hinweise
5. **Gib vor der Liste eine Info-Zeile** mit folgendem Text aus:
   _Modelle nutzen mit: `/model alias` im Chat (z. B. `/model or-nemotron-ultra`). Nach Config-Änderung: `Ctrl+R` zum Neuladen._
6. **Verifiziere jedes Modell explizit!** Nur Modelle auflisten, die du mit einer Quelle (z.B. offizielle Preiseite des Anbieters) bestätigen kannst. Bei Zweifeln: NICHT auflisten, sondern weglassen. Nur Modelle auflisten, deren Verfügbarkeit als "kostenlos" du mit einer Quelle bestätigst.
7. **Formatvorgabe (exakt einhalten):**
8. **Füge den Alias in Backticks** hinter jedem Modellnamen ein:
   - **OpenCode Zen** → Präfix `opencode-`, z. B. `opencode-nemotron-ultra`
   - **OpenRouter** → Präfix `or-`, z. B. `or-nemotron-ultra`
   - **Ollama Cloud** → Präfix `ollama-`, z. B. `ollama-gpt-oss-120b`
   - Wenn ein Modell auf mehreren Plattformen verfügbar ist, den Alias der **primären** Plattform nennen.

```
**Allgemeines Reasoning**
1. Modellname (`alias`) (Provider)
2. Modellname (`alias`) (Provider)
3. Modellname (`alias`) (Provider)

**Coding**
1. Modellname (`alias`) (Provider)
2. Modellname (`alias`) (Provider)
3. Modellname (`alias`) (Provider)

**Agentisches Arbeiten**
1. Modellname (`alias`) (Provider)
2. Modellname (`alias`) (Provider)
3. Modellname (`alias`) (Provider)

**Websuche**
1. Modellname (`alias`) (Provider)
2. Modellname (`alias`) (Provider)
3. Modellname (`alias`) (Provider)
```

- Jede Kategorie beginnt mit **Fettdruck** des Kategorienamens
- Keine Klammern um die Nummern, nur Punkt nach der Zahl
- Keine zusätzlichen Leerzeilen zwischen den Kategorien (genau eine reicht zur Trennung)
- Keine Einleitung oder Abschlusskommentare
- Provider in Klammern, z. B. (OpenRouter), (Ollama Cloud), (OpenCode Zen)
- Bei Modellen, die auf mehreren Plattformen verfügbar sind: (OpenCode Zen / OpenRouter)
- Das Alias des Modells steht in Backticks hinter dem Modellnamen
- Die Liste ist absteigend sortiert: Platz 1 = bestes Modell, Platz 3 = drittbestes (schwächstes) der drei

**Wichtig:** Die Recherche muss aktuell sein (heutiges Datum). Die Ausgabe muss bei jedem Durchlauf gleich aussehen – nur die Modellnamen können sich ändern, wenn das Angebot sich geändert hat.
