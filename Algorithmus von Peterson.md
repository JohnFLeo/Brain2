**Vorraussetzungen**
- faire [Scheduling](Scheduler)-Strategie 
- gemeinsame Variablen für beide [[Prozess]]e 
- Lesen und Schreiben von Variablen ist unteilbar (atomar)

**Implementierung**
- kommt ohne besondere Anweisungen aus
- [[Wechselseitiger Ausschluss]]
- lebendige (live) und sichere (safe) Implementierung

![[GdBS-E-Proc.pdf#page=113&rect=49,17,656,377&color=yellow|GdBS-E-Proc, p.113]]
**Funktionsweise**
- Durch turn ready0 und ready1 ist immer nur ein [[Prozess]] im [kritischen Abschnitt](Kritischer%20Abschnitt) 
- Die Variable turn löst folgendes Problem der Verklemmung
![[GdBS-E-Proc.pdf#page=112&rect=52,155,551,373|GdBS-E-Proc, p.112]]

**Problem**
- Aktives Warten
- Nur für zwei Prozesse -> Erweiterung auf n [[Prozess]]e ist sehr kompliziert
- Unterschiedliche Anweisungen pro Prozess vor einem [kritischen Abschnitt](Kritischer%20Abschnitt) 