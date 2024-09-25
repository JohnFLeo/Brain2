## Ohne [[Unterbrechung]]
Lade Inhalt der Adresse welche in PC steht -> IR
Interpretiere den Wert in IR
Evtl weitere Daten holen (Zugriff auf Adresse PC+1)
Befehl ausführen
PC inkrementieren
Beginne von vorne
![[GdBS-C-Arch.pdf#page=15&rect=64,229,461,372|GdBS-C-Arch, p.15]]
## Mit [[Unterbrechung]]
wie oben nur kommt die Überprüfung und evtl Behandlung einer [[Unterbrechung]] hinzu
![[GdBS-D-OS.pdf#page=28&rect=51,52,472,371|GdBS-D-OS, p.28]]
kleine Ausnahme bilden die sogenannten [[Systemaufruf]]e
## Befehlsarten
**I(mmediate) und R(egister)-Befehle**
- ADD, SUB, MUL, DIV, MOD
- AND, OR, XOR, NOT
**J(ump)-Befehle**
- JMP \<Addr\>
**B(ranch)-Befehle**
- Nutzt Flags in CCR
- JEQ \<Addr\>
- JNE \<Addr\>
- JLT \<Addr\>
- JGE \<Addr\>
**Systemaufrufe**