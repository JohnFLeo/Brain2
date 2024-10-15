Eine Semaphore grich. Zeichenträger ist eine Systemdatenstruktur mit zwei Operationen
- P-Operation (proberen; passeren; wait; down) wartet bis Zugang frei ist
- V-Operation (verhogen; vrijgeven; signal; up) macht Zugang für anderen [[Prozess]] frei
- eine private Integer-Variable zur internen Steuerung
![[GdBS-E-Proc.pdf#page=128&rect=94,42,650,372&color=yellow|GdBS-E-Proc, p.128]]
**Funktionsweise**
- Vor dem Zugriff auf eine geschützte [[Ressource]], muss ein [[Prozess]] die P-Operation aufrufen 
- Ist der Wert der Variablen $\le$ 0, so wird der aufrufende [[Prozess]] [blockiert](Prozesszustand.md) und in eine Warteschlange eingereiht 
- Falls nicht, bekommt der [[Prozess]] Zugriff auf die [[Ressource]] 
- Zum Freigeben der [[Ressource]] muss die V-Operation aufgerufen werden, welche die [blockierten](Prozesszustand.md) [[Prozess]]e aus der Warteschlange benachrichtigt
## Implementierung über [[Sperrung von Unterbrechungen]] (Monoprozessor)
- P-Operation
![[GdBS-E-Proc.pdf#page=130&rect=81,37,662,345&color=yellow|GdBS-E-Proc, p.130]]
- V-Operation
![[GdBS-E-Proc.pdf#page=131&rect=100,217,675,346&color=yellow|GdBS-E-Proc, p.131]]
## Anwendungsmöglichkeiten
### [[Gegenseitiger Ausschluss]] über einem Semaphore
![[GdBS-E-Proc.pdf#page=129&rect=59,125,656,376&color=yellow|GdBS-E-Proc, p.129]]

### Synchronisierung
- S1 soll vor S2 aufgerufen werden
![[GdBS-E-Proc.pdf#page=132&rect=91,37,683,189&color=yellow|GdBS-E-Proc, p.132]]
## Bewertung
**Vorteile**
- kein Aktives warten
- Scheduler kann mit einbezogen werden in die Semaphor-Operationen z.B. Priorisierung welcher Prozess aufgeweckt werden soll bei V-Operation
**Nachteile**
- Ineffizient bei kurzen kritischen Abschnitten da höherer Overhead