![[Tutorium05_Folien.pdf#page=3&rect=38,46,414,119|Tutorium05_Folien, p.3]]
- nebenläufige [[Aktivitätsträger]] sind unabhängig voneinander 
	- müssen nicht aufeinander warten
	- müssen sich nicht synchronisieren 
- nebenläufige [[Aktivitätsträger]] können unabhängig voneinander ablaufen
- nebenläufige Aktivitätsträger können [parallel](Parallelität) laufen
## Probleme
 - Befehle einer Programmiersprache nicht unteilbar (atomar) 
 - Abbildung auf mehrere Maschinenbefehle
 - mehrere Anweisungen zusammen nie atomar 
 - (unerwartete) Prozesswechsel innerhalb einer Anweisung oder zwischen zwei zusammengehörigen Anweisungen können zu Inkonsistenzen führen
 
 ![[GdBS-E-Proc.pdf#page=94&rect=54,67,478,411|GdBS-E-Proc, p.94]]**zwischen print und reset erhöht sich der count dadurch gehen die zwei counts verloren**
 ![[GdBS-E-Proc.pdf#page=96&rect=85,87,610,285|GdBS-E-Proc, p.96]]
 **Observer hält den count in seinem Register 0 fest wird unterbrochen und überschreibt dann mit dem Inhalt von R0 alle Änderungen vom Logger**
 ![[GdBS-E-Proc.pdf#page=97&rect=90,54,608,256|GdBS-E-Proc, p.97]]
## Ursache
gemeinsame Nutzung von Ressourcen (cnt-Variable)
## Lösung
[[Koordinierung]]