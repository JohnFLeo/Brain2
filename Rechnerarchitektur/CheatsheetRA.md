Universelle Turingmaschiene
Harvard vs Princeton bzw. von Neumann
LoadStore Harvard architektur
Stapelmaschiene
1 Adressmaschiene
2 Adressmaschiene
3 Adressmaschiene
Befehlszyklus
Variante 1:
  IF->ID->OF->EX->OS
Variante 2:
  IF->ID + OF(RegFile)->EX->MEM(Speicher)->WB(RegFile)

---

(**C**ontent**A**ddressable**M**emory) != RAM
Voll Assoziativ Cache
Mengen Assoziativ Cache
Direct mapped Cache
vierfach assoziativ Cache
write through vs write back(dirty bit)
Cachecontroller(nach OSI) und Service Access Point
LRU LFU
interleaving

---

Overlays(Verwaltung durch Programmierer)
Adressierungsarten(Mitschrift2)
- inherente Adressierung
- implizite unmittelbare Adressierung
- direkte absolute Adressierung
- indizierte Adressierung
- indirekte Adressierung
- relative Adressierung
Segmentverwaltung
Seitenverwaltung
Memory Management Unit
Transaction Look Ahead Buffer

---

Pipeline
**echte Datenabhängigkeit** (Read After Write)
- add t r s
- add v t u (t ist noch veraltet)
**Ausgabeabhängigkeit** (Write After Write)
- add t r s
- ld t a (schneller -> wert aus add in t nicht a)
**Gegenabhängigkeit** (Write After Read)
- add t r s (langsamer-> r erhält zu früh a und addition kommt durcheinander)
- ld r a 
Vermeidung von Datenabhängigkeiten
- NOPs einfügen
- Umsortierung
- Interlocking
- Bypass

- Verzögerter Sprung(Branch Delay Slot)= Befehl nach branch wird immer ausgeführt
- Statische Sprungvorhersage-> Compiler nicht Hardware
  aber keine Datenabhängigkeit berücksichtigt
- Dynamische Sprungvorhersage
	- Zustandsautomat über Assoziativspeicher BranchAddr ->Branchtargetaddr
	- Zustände: Strongly not taken, not taken, taken strongly taken
- Hochdynamische Sprungvorhersage
	- Branch history Schieberegister 
		- wird für jede Branchadresse gepflegt
		- Enthält vergangenheit taken bzw not taken als Pattern
	- Pattern history Table 
		- für jedes Pattern jedes Branches wird ein sätigender Zähler gehalten

---

RISC-V Microarchitectur
Übersetzungsprozess

---

Superskalare Architektur
- SIMD
- MIMD
- SISD
- MISD
Vektorrechner
- SAXPY (Single Precission A * X + Y)
- DAXPY (Double Precission A * X + Y)
Fließkommaeinheit
Register renaming
CISC -> mikroIntrROM->RISC
Tomasulo Algorithmus (out of order Instruction)
- The reservation stations control when an instruction can execute, rather than a single dedicated hazard unit.
- Reservation stations
- Common Data Bus -> Contains not Target but Source
- Queue
- Load Buffer
- Registers
- Store Buffer
- Cycle:
	- Issue->Rename Registers and place into Reservation Station if possible
	- Execute-> wait if operands still missing (watch CDB)
	- Write result-> Write to CDB and free Reservation Station