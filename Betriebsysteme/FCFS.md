kurz für First Come First Served
- nicht-[[präemptiv]]
- Warteschlange für [[Prozess]]e im Zustand [Bereit](Prozesszustand.md)
- [[Prozess]]e werden hinten eingereiht
- n [[Prozess]]e werden vorne entnommen wobei n die Anzahl an verfügbaren [Prozessoren](Prozessor.md) ist und zu [Laufend](Prozesszustand.md) geändert
- Bei [Blockieung](Prozesszustand.md) wird [[Prozessor]] freigegeben
- Bei [Deblockierung](Prozesszustand.md) wird [[Prozess]] hinten in die Warteschlange eingereiht

![[GdBS-E-Proc.pdf#page=38&rect=72,67,459,175|GdBS-E-Proc, p.38]]
![[GdBS-E-Proc.pdf#page=39&rect=64,45,544,256|GdBS-E-Proc, p.39]]
## Bewertung
- fair
- Wartezeit nicht minimal da sich Staus hinter lang laufenden [[Prozess]]en bilden
- nicht für Time-Sharing oder interaktiven Betrieb geeignet