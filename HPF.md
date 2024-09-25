kurz für Highest Priority First
- sowohl [[präemptiv]] als auch nicht [[präemptiv]]
- Sortierung der Bereit-Warteschlange nach Prioritäten
- Priorität typischerweise ganzzahliger Wert
- Unterschiedliche Ordnungen möglich
- Kleinerer Wert oder höherer Wert hat höhere Priorität
- statische Prioritäten aber auch als dynamische Prioritäten
- Echtzeitsysteme -> statische Prioritäten dadurch erhält man eine gewisse Vorhersagbarkeit der Reaktionszeiten
- Also: [[SJF]] ist eigentlich HPF mit dynamischer Priorität basierend auf der Rechenzeit

**Probleme**
- **Aushungerung**: durch ständige Verfügbarkeit höher priorer [[Prozess]]e kommt ein [[Prozess]] nie zum laufen
- **Prioritätenumkehr**: Hochpriorer Prozess möchte exklusive [[Ressource]], die ein niederpriorer Prozess momentan besitzt (z.B. Zugang zu Drucker) dieser kann diese aber nicht freigeben da mittelpriorer [[Prozess]] den niederprioren für einen beliebig langen Zeitraum verdrängt.(Solange P3 nicht fertig ist besitzt er die [[Ressource]] -> P1 bleibt blockiert)

![[GdBS-E-Proc.pdf#page=56&rect=56,37,691,256|GdBS-E-Proc, p.56]]
**Lösung**
- **Aushungerung**: dynamische Anhebung der Priorität für lang wartende [[Prozess]]e (Alterung)
- **Prioritätenumkehr**: dynamische anhebung der Priorität für [[Prozess]]e, die exklusive [[Ressource]]n besitzen auf die hochpriore [[Prozess]]e warten -> P3 bekommt temporär die gleiche Priorität wie P1

![[GdBS-E-Proc.pdf#page=58&rect=50,33,666,284|GdBS-E-Proc, p.58]]
