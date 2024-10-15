![[Modern Processor Design_ Fundamentals of Superscalar Processors ( PDFDrive ).pdf#page=144&rect=35,50,406,333|Modern Processor Design_ Fundamentals of Superscalar Processors ( PDFDrive ), p.129]]
![[Modern Processor Design_ Fundamentals of Superscalar Processors ( PDFDrive ).pdf#page=148&rect=54,326,401,627|Modern Processor Design_ Fundamentals of Superscalar Processors ( PDFDrive ), p.133]]
Serial: 
- Chip Select für jeden DRAM-Chip einzeln. Die restlichen Anschlüsse werden geteilt

Parallel: 
- Die Datenverbindung ist vierfach so groß also bei n Bit pro DRAM hat Data ein 4nBit Interface -> Bessere Daten Bandbreite
- Aber erhöhte "Kosten" da mehr Anschlüsse verwendet werden

Interleaved:
- Mehrere Gruppen die jeweils gleiche Addr und Cmd Linien haben
- die Gruppen können unabhängig voneinander arbeiten -> erhöhte Transaktion Bandbreite(2x)
- Aber erhöhte "Kosten" da mehr Anschlüsse verwendet werden