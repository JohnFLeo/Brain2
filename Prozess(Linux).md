Erzeugung von [[Prozess]]en
- [[Systemaufruf]] fork
	- aus einem [[Prozess]] werden zwei fast völlig identische Prozesse den Vater(Parent) und das Kind(Child)
	- liefert return value Kind-ID wenn vom Parent aus aufgerufen
	- liefert return value 0 wenn vom Child aus aufgerufen
	- beide Prozesse haben dieselben informationen
- [[Systemaufruf]] exec
	- ein Prozess startet erneut mit anderem Programm
	- Prozess bleibt bestehen und führt neues bzw. anderes Programm aus
	- Übergabe von Argumenten und von Umgebungsvariablen
- durch Kombination von exec und fork werden häufig neue Prozesse angestoßen
	- zunächst fork -> neuer Prozess aber gleiches Programm
	- dann exec -> der neue Prozess startet ein anderes Programm
	- Bsp.: Shell aufruf
- 
[[PCB(Linux)]]