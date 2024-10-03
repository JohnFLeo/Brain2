- Zusätzliche [[Aktivitätsträger]], die von der Anwendung selbst verwaltet werden
- Die Umschaltung zwischen der Register passiert in einem geschlossenen [[Prozess]]
- Häufig genutzt in Kombination mit [[Kernel-level Thread]]s d.h. [Scheduling](Scheduler.md) auf mehreren Ebenen 
## Bewertung
- Nur so parallel wie die Zahl der [[Kernel-level Thread]]s
- User-level Threads können schneller umgeschaltet werden da kein Wechsel ins [[Betriebssystem]] nötig ist
- User-level Threads sind mit jeder beliebigen [Strategie](Auswahlstrategie.md) umschaltbar
- Bei [Blockierung](Prozesszustand.md) des User-level Threads bleibt [[Aktivitätsträger]] im [[Betriebssystem]] hängen