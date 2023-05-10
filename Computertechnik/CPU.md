# CPU

[TOC]

## Einteilung der Maßeinheiten


| ausgeschriebene Schreibweise | 1*10 Schreibweise | Maßeinheit | Einheit      |
| ---------------------------- | ----------------- | ---------- | ------------ |
| `0,00 000 0011 n`            | `1*10^-9 `        | `n`        | `Nano`       |
| `0,00 001	`               | `1*10°-6`         | `µ`        | `Mikro`      |
| `0,001`                      | `1*10^-3 `        | `m`        | `Milli`      |
| `1`                          | -                 | -          | `Basisgröße` |
| `1 000 000`                  | `1*10 ^3`         | `K`        | `Kilo`       |
| `1 000 000 000`              | `1*10 ^6`         | `M`        | `Mega`       |
| `1 000 000 000 000`          | `1*10 ^9`         | `G`        | `Giga`       |
| `1 000 000 000 000 000`      | `1*10 ^12`        | `T`        | `Tera`       |



Die Größe des Mikroprozessors  beschreibt die Größe der Bauteile eines Prozessors. 
Die verbauten ***Transistoren*** in einem Mikroprozessor haben eine ***Größe im µm (Mikrometer) Bereich***.

Heutige Prozessoren sind bereits im ***5nm Bereich***.



## Mikroprozessoren

Ein Mikroprozessor, auch ***Central Processing Unit (CPU)*** bezeichnet eine Einheit, die alle ***Abläufe und die Verarbeitung*** der Daten ***steuert***.



<img src="/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155227809.png" alt="image-20220703155227809" style="zoom:67%;" />



Eine CPU ist durch einen Bus (nebeneinander liegende Transportleitungen) mit einem Speicher (RAM) verbunden.

Ebenfalls an den Bus angeschlossen sind Controller, die die Eingabe oder Aufgabe der Peripheriegeräte übernimmt und damit die Haupt CPU entlastet.
Controller sind „eigene Computer“, mit eigenen Mikroprozessoren, sowie RAM und ROM mit einer simplen Aufgabenverteilung.





## Aufgaben des Prozessors:


### Ansteuerung der Peripheriegeräte-Controller

>In- und Output der Peripheriegeräte



### Speicherzugriff:

>Daten- und Programmanweisungen werden (auch Informationen der Peripherie) in der CPU zwischengelagert



### Verarbeitung der Daten:

>arithmetische (Addition, Subtraktion, …) oder logische (and, or, xor) Operationen werden miteinander verknüpft





## Prozessortypen

### Von Neumann Prozessor

Gemeinsame Speicherung von Daten- und Programmanweisungen in der CPU

#### Vorteil

> kostengünstiger
> platzsparender



#### Nachteil

> anfällig für Fehlinterpretationen (Datenanweisungen werden als Programmanweisungen interpretiert und lassen große Fehler entstehen)
> Flaschenhals Prinzip: viele Daten- und Programmanweisungen müssen über einen Datenbus.



<img src="/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155309607.png" alt="image-20220703155309607" style="zoom:67%;" />



### Harvard Prozessor

Speicherung der Daten- und Programmanweisungen in einer jeweils einzelne, dafür vorgesehene CPU



#### Vorteil

> keine Anfälligkeit für Fehlinterpretationen



#### Nachteil

> teurer
> mehr Platz



![image-20220703155322654](/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155322654.png)![imag



## Klassifizierung von Prozessoren



Unter einem ***Befehlssatz*** versteht man die ***Gesamtheit aller Programminstruktionen***, also einem Ansatz, um einen Mikroprozessor zu klassifizieren.

Unter ***Programminstruktionen*** versteht man ***arithmetisch logische Operationen*** wie AND, SUB, NOR, XOR, etc, sowie ***Vergleichsbefehle*** und ***Shift- und Rotationsbefehle***



> ***Datentransfer***
> Ein- / Ausgabebefehle
> Lade- und Speicherbefehle

> ***Steuerbefehle***
> Sprungbefehle: unbedingt, bedingt, relativ
> Kontrollbefehle: STOP, Unterprogrammsprung



### RISC (Reduced Instruction Set Computing)

Ziel:

> Befehlssatz wird möglich minimal gehalten

Vorteil:

> wenige, effiziente Befehle

Besonderes:

> Komplexität liegt im Compiler





### CISC (Complex Instruction Set Computig)

Ziel:

> viele Befehlssätze durch intern gespeicherte Mikrooperationen (µ Ops) bis zu 250 Befehle

Vorteil:

> größeres Spektrum an ausführbaren Aufgaben
> Kürzere Programme

Besonderes:

> benötigt viel Chipfläche, Komplexität liegt in der SPU



### Universal- und Spezialprozessoren

> ***Universalprozessor***
> GGP (General Purpose Processors)
> Frei programmierbar
> Umfangreicher Satz von Befehlen
> Für vieles einsetzbar

> ***Spezialprozessor***
> weniger flexibel
> sehr effizient in bestimmter Aufgabe (GPU, Controller, etc)

Grundlage zur Auswahl einer CPU gilt:

***Kompromiss*** zwischen ***Optimierung*** auf einen bestimmten Zweck und ***breites Spektrum*** an möglichen Anwendungen zu finden.



## Aufbau eines Prozessors





<img src="/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155637811.png" alt="image-20220703155637811" style="zoom:67%;" />



### Steuerwerk (blau)

Herz des Prozessors

Steuerwerk läuft nach dem EVA Prinzip

> Eingabe
> Verarbeitung
> Ausgabe
> Sprungbefehl bedeutet eine neue / Teilverarbeitung eines Befehls



![image-20220703155505870](/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155505870.png)



Befehlsregister (***Register = Speicherzelle***) holt sich befehle aus RAM
Befehle bestehen aus:

> Adresse,
> Befehl
> Kombination aus beidem

Gesamtaufgabe wird in Teilschritte in (Mykrooperationen) aufgeteilt

***Adresswerk***: versieht die bits mit einer Adresse, damit sie klar erkenntlich für den Speicher wird
***Befehlsdecoder***: versieht die bits mit eindeutig zuordbaren aufgaben
***Programmcounter***: einfacher Zähler, der auf die nächste auszuführende Operation zuweist 
***Befehlsregister: Aufgaben werden gespeichert***





### Register

***MUX*** Zwischenspeicher
da Speicher langsamer ist als Prozessor, es handelt sich hierbei um einen ***multiplexer***
Er Verbindet die Ein- und Ausgänge zu einander offen, an der Stelle an der sie gebraucht werden (im jeweiligen Registersatz)
Er schleust die Daten durch.

Im ***Register*** sind ***Flip-Flop Schaltungen*** verwendet, die ***Daten zwischenspeichern*** können.
Da Strom an sich nicht gespeichert werden kann, wird ein anderes System verwendet. Solange Strom im System vorhanden ist, wird das Datum gespeichert.



#### Arten von Registern

***General-Purpose-Register***: kann frei gelesen und gespeichert werden
***Spezialregister***: Werden für interne Funktion des Prozessors benutzt



<img src="/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155551818.png" alt="image-20220703155551818" style="zoom:67%;" />



### Rechenwerk

ALU ***Arithmetische Logische Unit Rechenunit***, die arithmetische Operationen ausführt
Diese sind hochkomplexe Schaltungen die am Ende Logische Operatoren wie ***AND, OR, XOR, NOR*** enthalten, ebenso wie arithmetische Operatoren wie Addition, Subtraktion und Multiplikation
Jede Operation wird durch eine logische oder arithmetische Operation geschickt und verarbeitet, der Multiplexer entscheidet (anhand der vorher gestellten Aufgabe) welche Ausgabe tatsächlich resultiert.

***Akkumulator***
In einem Akkumulator wird ein ***Operand*** einer vorhergehenden Operation ***gelagert***, damit es zu einer Rechnung, einem Vergleich kommen kann. Er ist Teil innerhalb der ALU.



<img src="assets/image-20220703155615114.png" alt="image-20220703155615114" style="zoom:67%;" />

## Assembler Code



### Definition

> Code, der durch durch **mnemonische Abkürzungen** dargestellt ist.
> Mnemonische Codes sind zugehörige Kürzel zur Identifikation von Operationen ADD, LDA etc.



### Programmablauf

Der Compiler wandelt Quellcode in Maschinencode um.
Dieser Maschinencode wird in einen Befehlssatz umgewandelt, der jeweils in einzelnen Blöcken eigene Aufgaben haben.
Die folgenden Beispiele werden mit einem 16 bit langem Befehlssatz verdeutlicht

`000000110000001000000010000100000000000110000101` `000000100001000100000001000100000000001100010001 00000010000100100000011100000000`



<img src="/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155750580.png" alt="image-20220703155750580" style="zoom:67%;" />



#### Aufteilung in 16 bit Befehlssätze



`0000001100000010` `0000001000010000` `0000000110000101` `0000001000010001` `0000000100010000` `0000001100010001` `0000001000010010` `0000011100000000`

Aufteilung in einzelne Aufgabengebiete des jeweiligen Befehlssatzes





### Reserviert

`0000` `001100000010`			Für die ***Reserve*** werden ***4 Bit*** eingeteilt
Hier werden bit Stellen reserviert, damit ***andere CPU-Generationen mehr OP-Code darstellen*** kann. Wird für zukünftig neue Befehle verwendet.






###  Op-Code

`0000` `001` `100000010`			Für en Op-Code werden ***3 Bit*** eingeteilt
Op-Code sind ***Assemblerbefehle***, die **verschiedene Funktionen** übernehmen.

![image-20220703155826164](C:\Users\mathi\OneDrive\FIA\Hardware\Computertechnik\1. CPU\assets\image-20220703155826164.png)






### Nummernzeichen



`0000 001` `1` `00000010`			Für das Nummernzeichen wird ***1 Bit*** eingeteilt
Das Nummernzeichen entscheidet, ob es sich beim ***Operanden*** um einen ***numerischen Wert*** oder um eine ***Adresse im Speicher*** (Inhalt von Variablen) handelt .



<img src="/home/matze/Dropbox/FIA 2312/Unterricht/Hardware/Computertechnik/1. CPU/assets/image-20220703155920628.png" alt="image-20220703155920628" style="zoom:67%;" />






### Operand

`0000 001 1` `00000010`			Für den Operanden werden 8 Bit eingeteilt
***Was wird in den Akkumulator geladen?***
Wenn es eine ***Zahl*** ist, dann ist klar, dass das eine Zahl ist
Wenn es sich hierbei um eine ***Speicheradresse***, ziehe den Inhalt der Speicheradresse rein





### Interpretation des Befehlssatzes

#### Darstellung auf Bitebene

| Reservierte Bits | Op-Code | Nummernzeichen | Zahl / Speicheradresse |
| ---------------- | ------- | -------------- | ---------------------- |
| 0000             | 001     | 1              | 0000 0010              |



#### Darstellung auf Interpretationsebene

| Reservierte Bits | Op-Code | Nummernzeichen   | Zahl / Speicheradresse |
| ---------------- | ------- | ---------------- | ---------------------- |
| reserviert       | LOAD    | numerischer Wert | 2                      |

***Ergo:*** Lade die Zahl 2



### Beispielaufgabe

Wandeln Sie den Binärcode in Assemblercode um



`000 00011 0000 01010 01`	
`0000` `001`  `1` `0000 0101 001`	

| Reservierte Bits | Op-Code | Nummernzeichen   | Zahl / Speicheradresse |
| ---------------- | ------- | ---------------- | ---------------------- |
| 0000             | 001     | 1                | 0000 0101 001          |
| reserviert       | LOAD    | numerischer Wert | 41                     |


`0000 0100 0001 0000`

`0000`     `010`     `0`     `0001 0000`

| Reservierte Bits | Op-Code | Nummernzeichen  | Zahl / Speicheradresse |
| ---------------- | ------- | --------------- | ---------------------- |
| 0000             | 010     | 0               | 0001 0000              |
| reserviert       | STORE   | Speicheradresse | 16                     |

Speichere 16. Store Value im Akkumulator auf Platz 16



***Note:***

>Es wird für jede Operation im MUX jeweils 2 bitstellen gespeichert. 
>Einmal für den Assembler Code und einmal für die Zahl (als Nummer oder der Adresse)

 



## Stack (Stapelspeicher)



Ein ***Stapel*** (***Stack***) kann nur eine bestimmte Menge von Bits aufnehmen. Es kann immer ***nur*** der ***oberste Stapel bearbeite***t werden. Dazu gibt es zwei wichtige Operationen:

> Push (ablegen)
> Pop (holen)



Ein ***Stack wächst von unten nach oben***, entsprechend wird bei einem Push oder Pop Befehl der Stack größer oder kleiner.
Der Stackpointer ist nur ein ***eigenes Register, das auf die aktuelle Adresse des zu bearbeitenden Elements im Stack zeigt.***
Das Stack ist ein variabler Speicher, das heißt er ist nicht an eine maximale Größe gebunden und kann variabel mitwachsen.
Er setzt sich auf die nächsten freien Adressen.



### Subroutine

Eine Subroutine ist ein Unterprogramm (eine Funktion oder ähnliches), welche variabel im Stack gespeichert und geholt werden kann.



### Stackpointer Assembler Code



| Op Code | Mnemonisch | Funktion                | Beispiel |
| ------- | ---------- | ----------------------- | -------- |
| 1000    | JSR        | Springe zu Subroutine x | JSR 40   |
| 1001    | RTS        | Rückgabe an Subroutine  | RTS      |
| 1010    | PUSHA      | Kopiere Akku zu Stack   | PUSHA    |
| 1011    | PULA       | Kopiere Stack zu Akku   | PULA     |
| 1100    | ISP        | Erhöhe Stackpointer     | ISP      |
| 1101    | DSP        | Verringere Stackpointer | DSP      |



## Interrupts



Bei plötzlich auftretenden Ereignissen wie Tastatureingaben können zwei Situationen helfen

> ***Polling***
> *in regelmäßigen Abständen wird nach potentiellen Quellen(z.B. Tastatureingaben) gesucht
> ***hochgradig ineffizient***, da sehr viel Ressourcen unnötig verbraucht werden

> ***Interrupt***
> Signal wird von Quelle weitergeleitet, eine ***Unterbrechung*** (***Interrupt***) wird eingeleitet
> Die Interrupt Quelle löst bei Ereignis einen Interrupt Request (IRQ) aus, in dem es ***selbstständig*** das ***Signal sendet***.

> I***nterrupt-Serviceroutine (ISR)***
> Eine Routine die definiert welches Ereignis oder welche Ereignisquelle welche ***Priorität*** hat
> Niedrige Prioritäten werden durch höhere Prioritäten ebenfalls interrupted
> Treiber erstellen in der ISR die höhe der Priorität





### Software-Interrupts (Traps)

Traps werden von ***Steuerwerk aufgerufen*** und sind ***synchron zum Programmablauf***.
Die Synchronisation zum Programmablauf ist deshalb wichtig, damit es ***im Takt*** der ***CPU*** ausgeführt werden kann.

> Bsp.: Divided by zero: Divisionen durch 0 enthalten ein unendlich großes Ergebnis, was den RAM und die CPU überrumpeln würden. Deswegen ist eine wichtige Trap die Divided by Zero Trap, als Notstopp.





### Hardware-Interrupts

***Asynchron zum Programmablau***f, da sie von der ***Hardware direkt ausgelöst*** werden.
Sie kommen deshalb von der Hardware selbst.

> Tastaturcontroller Drücken einer Taste
> Watch-Dog Überwachung des Systems, wenn nicht rechtzeitig zurückgesetzt, dann Reboot des Systems
> Echtzeituhr Gibt Signal wenn eine Millisekunde vorbei ist



### Funktion eines Interrupts

Bei Hardware-Interrupts wird ein ***Interrupt-Controller*** benötigt. Dieser hat die Aufgabe die ankommenden Interrupt Signale aufzunehmen, zu sortieren, mit einer ***ID*** (Herkunft des Interrupt-Signals) zu versehen und die ***Priorität*** des Interrupt-Signals zu ermitteln.
Dieser Prozess nennt sich IRQ-Vektornummer



### Ablauf eines Interrupts

> IRQ (Interrupt-Request)
> aktueller Befehl wird beendet
> Inhalte des Spezialregisters werden kopiert (um später das Programm genau an der Stelle weiterlaufen zu lassen)
> Interrupt Vektor Nummer wird bestimmt
> ISR wird geladen



![img](https://upload.wikimedia.org/wikipedia/commons/c/cf/Interrupt_Process.PNG)
