## Konzepte
- Turingmaschiene
- [[von Neumann Architektur]]
- [[Harvard Architektur]]
- 3-Adressmaschiene
- 2-Adressmaschiene
- Stapelmaschiene (0-Adressmaschiene)
- Von Neumann Zyklus
- RISC vs CISC

## [[Speicherarchitektur]]
- [[Cache]]
	- Trennung von Datenverarbeitung und Speicherzugriff
	- Direct Mapped Cache(\<Addr\>mod Cachegröße)
	- Vollassozitiver Cache(\<Addr\> -> CAM(Assoziativspeicher) -> Datum)
	- Zwifach Assoziativer Cache
- Elmore Delay
- Banking (Interleafing)
- SRAM vs [[DRAM]]
- Speicherblock vs Cache Line
- LRU
- LFU
- Cache Controller
- Hit
- MMU
	- Segmentierung
	- Seiten
	- Verwaltungstabellen
	- Transaction Look Ahead Buffer
	- Scheduler
## Mikroarchitektur(RISCV)
- Befehlstypen
- Komponenten
- ISA
	- Adressierungsarten
	- Opernadenauswahl
	- Architekturprinzip
- Mikroprogrammierung
	- PLA
	- Assoziativspeicher
	- vertikale vs horizontale Mikroprogrammierung
## Fließbandverarbeitung(RISCV)
- Feste Befehlsformate immer 32 bit lang
- Addressen sind 5 bit lang
- WindowPtr
- Funktionen
- Probleme(Sprünge und Branches)
## Programmierung(RISCV)
- Assembly
- Assmebler
- Compiler
- Macros
- Konventionen
## [[Skalare Architektur]]
- Klasse an Prozessoren
- eine Information pro Zyklus
- [[Pipelining]]
- Pipeline Stall
- Out of Order
- Static Branchprediction
- RISC da gleiche ausführungsdauer
## [[Superskalare Architektur]]
- SIMD
- MIMD
- Nebenläufigkeit und parallelität
- Register renaming
- [[Branch Prediction]]
- 
## Vektorrechner
## VHDL
- Synthese
- 
