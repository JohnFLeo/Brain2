- Kernel-level Threads bieten die Möglichkeit für einen [[Prozess]] mehrere [[Aktivitätsträger]] zu nutzen, die vom [[Scheduler]] getrennt voneinander gehandhabt werden (im Gegensatz zu [[User-level Thread]]s)
- Sie werden typischerweise durch [[Systemaufruf]]e erzeugt
- Änderung der Prioritätsebenen ist über [[Systemaufruf]]e möglich
- Anhalten und Löschen der Aktivitätsträger ist über [[Systemaufruf]]e möglich
## Bewertung
- Kernel-level Threads arbeiten alle unabhängig
- Alle Möglichkeiten des [[Scheduler]]s sind nutzbar
