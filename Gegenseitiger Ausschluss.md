Gleichbedeutend mit [[Wechselseitiger Ausschluss]] auch Mutex (engl.: Mutual Exclusion) genannt
![[GdBS-E-Proc.pdf#page=104&rect=83,48,701,342&color=yellow|GdBS-E-Proc, p.104]]


**Idee**
- Vorkehrungen, dass nicht mehrere [[Prozess]]e gleichzeitig im [kritischen Abschnitt](Kritischer%20Abschnitt) sind
- [[Prozess]] kommt an einen [kritischen Abschnitt](Kritischer%20Abschnitt)
	- wartet bis alle anderen [[Prozess]]e den Abschnitt verlassen haben
-  vor und nach [kritischen Abschnitt](Kritischer%20Abschnitt) muss es spezielle Anweisungen geben
	- meist benötigen diese Anweisungen gemeinsame Datenstrukturen

**Probleme**
 - [[Deadlock]]