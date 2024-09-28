kurz für Test-and-Set-Instruction
**Funktionsweise**
- Setzen eines Bits im Speicher auf 1
-  Rückgabe des vorherigen Werts des Bits
->  Lese- und Schreib-Operation unteilbar (atomar)
- [[Gegenseitiger Ausschluss]] mit TAS
![[GdBS-E-Proc.pdf#page=120&rect=59,106,649,376&color=yellow|GdBS-E-Proc, p.120]]

**Vorteile**
- gleicher Code für jeden Prozess verwendbar

**Nachteile**
- aktives Warten

In der Praxis wird folgender Trick genutzt:
![[GdBS-E-Proc.pdf#page=121&rect=83,62,660,174|GdBS-E-Proc, p.121]]
