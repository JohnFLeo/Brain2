siehe [hier](BS/Altklausuren-20240913/2023s-BS-K1-Klausur.pdf)
![[2023s-BS-K1-Klausur.pdf#page=2&rect=25,630,557,761|2023s-BS-K1-Klausur, p.2]]
- Lade Inhalt der Speicherzelle auf die der PC (Programmzähler) zeigt
- Dekodiere den Inhalt -> RTI
- Führe den Befehl aus
	- Lade alle Register die vorher gesichert wurden
	- gehe in den [[Benutzer Modus]] (passiert implizit durch laden des CCR)
- Überprüfe, ob eine [[Unterbrechung]] vorliegt 
- wenn nein dann
	- Inkrementiere den PC
	- Beginne von vorne
- wenn ja dann
	- Sichere alle Registerinhalte
	- gehe in [[Privilegierter Modus]]
	- Lade PC der [[ISR]](Interrupt Service Routine)
	- Beginne von vorne

![[2023s-BS-K1-Klausur.pdf#page=2&rect=29,338,558,380|2023s-BS-K1-Klausur, p.2]]
- Eine [[Externe Unterbrechung]] wird von außerhalb der CPU getriggert z.B. Festplatte ist fertig mit dem Laden von angefragten Daten
- Eine [[Interne Unterbrechung]] wird von Fehlern oder Events die durch ein Programm erzeugt worden sind getriggert z.B. Division by zero

![[2023s-BS-K1-Klausur.pdf#page=2&rect=37,176,560,240|2023s-BS-K1-Klausur, p.2]]
Das ist der sogenannte [[Systemaufruf]]. Dieser dient als Schnittstelle für Anwendungen zum Betriebssystem und ist unabdingbar um wieder ins Betriebssystem übergehen zu können für z.B. das Anfordern von Daten von einer Festplatte
![[2023s-BS-K1-Klausur.pdf#page=3&rect=23,699,554,770|2023s-BS-K1-Klausur, p.3]]
- Ein [[Prozess]] dient als Platform auf der ein [[Programm]] ausgeführt werden kann. Weiter ist ein [[Prozess]] eine Einheit, die für ein Multitasking von Programmen unerlässlich ist. 
- Er besteht aus einem [[Aktivitätsträger]], dem Programm, dem Kontext, und dem [[PCB]](Process Control Block). 
- Weiter bietet er eine Schutz-Umgebung die verhindert, dass Anwendungen auf Speicher von anderen Anwendungen zugreifen können. Weiter bietet er für die Anwendung einen eigenen Adressraum.

![[2023s-BS-K1-Klausur.pdf#page=3&rect=29,566,561,627|2023s-BS-K1-Klausur, p.3]]
Gleiche Daten und gleicher Code (Speicher), Dateien, Netzwerkverbindungen
![[2023s-BS-K1-Klausur.pdf#page=3&rect=36,413,566,458|2023s-BS-K1-Klausur, p.3]]
Man schränkt die Nebenläufigkeit ein um gleichzeitigen Zugriff auf gemeinsame Ressourcen zu verhindern -> möglichst wenig zeitliche Durchmischung
**Maßnahmen**
- Bei Zugriff auf gemeinsame Ressource wird Prozess angehalten
- Dem Scheduler wird das Umschalten untersagt
![[2023s-BS-K1-Klausur.pdf#page=3&rect=39,300,564,348|2023s-BS-K1-Klausur, p.3]]
Ein Spinlock ist eine Sperre zum Schutz gemeinsam genutzter Ressourcen, welche mittels aktivem Warten umgesetzt wird. 
**Zu Begin** 
- Sperrvariable := frei
**Bei versuchtem Zugriff**
- while Sperrvariable == gesperrt loop
	- warten
- endloop
- Prozess -setzt-> Sperrvariable := gesperrt
- Prozess -greift-zu-> Ressource
- Prozess -modifizeiert-> Ressource
- Prozess -setzt-> Sperrvariable := frei
![[2023s-BS-K1-Klausur.pdf#page=3&rect=36,177,568,224|2023s-BS-K1-Klausur, p.3]]
Für kurze Kritische Abschnitte ist ein Spinlock effizienter da weniger Overhead zu erwarten ist