Elegante Methode in Monoprozessorsystemen um Probleme bei Nebenläufigkeit zu vermeiden
**Funktionsweise**
- Spezielle Instruktionen
	- SEI sperrt [[Unterbrechung]]en
	- CLI gibt [[Unterbrechung]]en wieder frei
![[GdBS-E-Proc.pdf#page=126&rect=65,86,647,283&color=yellow|GdBS-E-Proc, p.126]]

**Vorteile**
- einfach in der Umsetzung

**Nachteile**
- extra Befehle nötig
- nur für kurze [kritische Abschnitte](Kritischer%20Abschnitt) geeignet