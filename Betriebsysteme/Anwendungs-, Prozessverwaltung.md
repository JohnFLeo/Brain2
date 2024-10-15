## Anwendungsstart
Wechsel in [[Benutzer Modus]] 
Sprung in den Anwendungs-Code
vgl. [[Prozess(Linux)]]
## Umschalten zwischen [[Prozess]]en
auch Kontextwechsel genannt löst das Prolem, dass es mehr [[Aktivitätsträger]] als [[Prozessor]]en gibt und somit eine [Ressourcenzuteilung](Betriebsmittel.md)erfolgen muss.
**Vereinfachtes Problem:**
Es gibt nur einen [[Prozessor]], und zwei [[Prozess]]e. Damit die beiden Prozesse voneinander ungestört agieren können müssen sie bei dem Wechsel ihren Kontext (alle Register) sichern bzw wieder laden. Wir konstruieren einen Umschalter, für jeden der beiden [[Prozess]]en 
Daraus ergibt sich die Essenz des Umschaltens
- Wechsel der Registerinhalten(mit PC) vgl. [[Prozessor]]
- Prozess darf Wechsel nicht bemerken lediglich die Ausführung darf sich verzögern

Vernachlässigt wurde dabei
- Für jeden weiteren [[Prozess]] wird ein weiterer Umschalter benötigt
- Ablaufumgebun ist nicht eingerichtet(keine Schutzumgebung)

**Allgemein ergeben sich zwei Strategien:**
- Prozesse geben freiwillig CPU ab
	- Umschaltung nicht transparent
	- Bsp.: [[Systemaufruf]] yield gibt dem [[Betriebssystem]] Möglichkeit den nächsten [[Prozess]] auszuwählen
	- Bsp.: Co-Routinen [[Systemaufruf]] yield mit [[Prozess]]-ID Parameter der [[Prozess]] bestimmt seinen Nachfolger -> keine Fairness, Umschaltstrategie in der Anwendung
- Besser: [[Scheduler]] Komponente
## [[Multithreading]] 
