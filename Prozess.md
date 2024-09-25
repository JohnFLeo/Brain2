**Ziel:** Multitasking oder auch Multi-User Operation dabei möglichst gut Optimieren
**Umsetztung:** Ein Prozess bildet einen virtuellen [[Prozessor]] das heißt
- Er enthält das [[Programm]], das sich in Ausführung befindet inklusive der aktuellen Daten 
- [[Programm]] kann mehrfach ausgeführt werden 
- Mehrere gleichartige Prozesse exisitieren mit evtl. unterschiedlichen aktuellen Daten

**Bestandteile**
- Speicher(siehe [[von Neumann Architektur]])
- [[Aktivitätsträger]]
- Schutzumgebung 
	- eigener Addressraum
	- Andere Anwendungen können nicht in den Speicherbereich eingreifen
- Kontext für Ressourcenanforderungen
	- Dateien
	- Semaphore
	- Queues
	- Pipes
	- Sockets
	- Geräteverbindungen
	- Verwaltungseinheit für Ressourcen
- [[PCB]]

**Beispiel**
- [[Prozess(Linux)]]
