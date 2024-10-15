Probleme durch Datenabhängigkeiten. Über die Pipeline können Befehle "überholt" werden.
Man unterscheidet in:
- WAW(Write After Write)Ausgabeabhängigkeit
- RAW(Read After Write)Echte Datenabhängigkeit
- WAR(Write After Read)Gegenabhängigkeit
- Load und Store sind kürzer als andere Befehle -> kann zu Problemen führen
Lösung
- Interlocking
    - Interlocking Schaltung
    - Bypass Schaltung
- Umsortieren von Code
- Auffüllen mit NOP(stalling)

