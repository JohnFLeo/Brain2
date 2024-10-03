![[GdBS-E-Proc.pdf#page=84&rect=42,58,711,376|GdBS-E-Proc, p.84]]
## [[Kernel-level Thread]] vs [[User-level Thread]]

## [[Koordinierung]]
## Bewertung
**Vorteile**
- Aufteilung auf mehrere gleichzeitige Aufgaben
	- z.B. mehrere Fenster 
	- z.B. Netzwerkaufgaben neben Benutzerinteraktion 
	- z.B. viele gleichzeitige Anfragen in Server-Anwendungen 
- Ausnutzung von Mehrkernprozessoren und -systemen 
	- echte Parallelität bei nur einem [[Prozess]]
- in der Regel übersichtlicherer Code 
- [[Prozess]] als Hülle für gemeinsame [[Ressource]]n der [Threads](Aktivitätsträger.md) 
- gleiche Daten und gleicher Code (Speicher) 
- Schutzumgebung 
	- Umschaltung zwischen [Threads](Aktivitätsträger.md) im gleichen [[Prozess]] ist effizienter als zwischen [Threads](Aktivitätsträger.md) verschiedener [[Prozess]]e 
- gemeinsam genutzte Dateien, Netzwerkverbindungen etc.

**Nachteile**
- Problem der [[Koordinierung]]