kurz für Round Robin
- Zuteilung erfolgt reihum
- ähnlich wie [[FCFS]] aber mit automatischer [Verdrängung](präemptiv) nach bestimmtem Zeitintervall -> Zeitscheibe
- Warteschlange für [[Prozess]]e im Zustand [Bereit](Prozesszustand) 
- [[Prozess]]e werden hinten eingereiht, vorne entnommen 
- nach Ablauf der Zeitscheibe wird der [[Prozess]] erneut eingereiht

![[GdBS-E-Proc.pdf#page=61&rect=62,36,503,161|GdBS-E-Proc, p.61]]
- muss [[Prozess]] den [[Prozessor]] verlassen, wird die Zeitscheibe abgebrochen siehe [Blockierung, Terminierung](präemptiv)
- Die Länge der Zeitscheibe ist ausschlaggebend
	- kurze Zeitscheibe: ständige Kontextwechsel -> Overhead
	- lange Zeitscheibe: Annäherung an [[FCFS]] -> selbe Problematik
	- beeinflusst mittlere Verweil- und Wartezeit

![[GdBS-E-Proc.pdf#page=64&rect=65,33,600,373|GdBS-E-Proc, p.64]]
## Bewertung
 - geeignet für Time-Sharing-Betrieb 
 - gleichmäßige Verteilung der Rechenzeit 
 - fair (?) 
 - Wartezeit kann lang sein das hängt jedoch von Anzahl der bereiten [Prozesse](Prozess) und der Zeitscheibenlänge ab 
 - nicht gut für interaktiven Betrieb 
 - [blockierende](Prozesszustand) [[Prozess]]e benachteiligt denn diese nutzen Zeitscheibe nicht aus und müssen wieder hinten anstehen