Ein Spinlock ist eine Sperre zum Schutz gemeinsam genutzter [[Ressource]]n, welche mittels aktivem Warten umgesetzt wird.
**Funktionsweise**
- Zu Beginn wird die Sperrvariable auf den Wert frei gesetzt
- Wenn Sperrvariable frei ist, kann sie von einem [[Prozess]] gesperrt werden und der [[Prozess]] kann auf die gesicherte [[Ressource]] zugreifen
- Nach der Modifizierung der [[Ressource]] wird die Sperrvariable wieder auf frei gesetzt
- Ist die Sperrvariable auf gesperrt gesetzt, so überprüft ein wartender [[Prozess]] diese ständig bis sie frei ist

 **Vorteile**
 - Für kurze [kritische Abschnitte](Kritischer%20Abschnitt.md) effizient 
 
 **Nachteile**
 - Aktives Warten verbraucht Rechenzeit
 - Effizienz abhängig von der [Scheduling](Scheduler.md)-Strategie

Einsatz fast ausschließlich in Multiprozessorsytemen 
- Koordinierung über mehrere [[Prozessor]]en hinweg 
- nur für kurze kritische Abschnitte effizient  z.B. Zugang zur Bereit-Warteschlange beim [Scheduling](Scheduler.md)