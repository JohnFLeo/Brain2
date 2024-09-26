**Ziel:** Multitasking oder auch Multi-User Operation dabei möglichst gut Optimieren
**Umsetzung:** Ein Prozess bildet einen virtuellen [[Prozessor]] das heißt
- Er enthält das [[Programm]], das sich in Ausführung befindet inklusive der aktuellen Daten 
- [[Programm]] kann mehrfach ausgeführt werden 
- Mehrere gleichartige Prozesse existieren mit evtl. unterschiedlichen aktuellen Daten

**Bestandteile**
- Speicher(siehe [[von Neumann Architektur]])
	- Bereich für Daten
	- Bereich für Code
- [[Aktivitätsträger]]
- Schutzumgebung 
	- eigener Adressraum
	- Andere Anwendungen können nicht in den Speicherbereich eingreifen
- Verwaltungseinheit für Ressourcen (Kontext für Ressourcenanforderungen)
	- Dateien
	- Semaphore
	- Queues
	- Pipes
	- Sockets
	- Geräteverbindungen
- [[PCB]]

**Beispiel**
- [[Prozess(Linux)]]
