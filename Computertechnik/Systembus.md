- [Definition](#definition)
- [Bus Arten](#bus-arten)
- [Lese/Schreibvorgang](#lese-schreibvorgang)



## Definition

Ein Systembus sind die ***Datenschienen*** (Busse) über die in einem Mikrorechner die ***CPU*** mit ihrer Umgebung ***kommuniziert***.


>***Wichtige Bussysteme*** sind 
>Datenbus
>Adressbus
>Steuerbus

Ein Bus besteht aus mehreren nebeneinander verlaufenden Signalleitungen auf denen synchronisiert Informationen übertragen werden.
An diesen Bussen sind mehrere Komponenten angeschlossen.

>***!!!Achtung!!!*** 
>Ein Systembus ist heutzutage nur noch die Verbindung von CPU und Chipsatz. Viele Bussysteme von früher werden heute direkt in die CPU eingelagert. Allgemein gibt es den klassischen Systembus nicht mehr.


<img src="assets/image-20220703160217191.png" alt="image-20220703160217191" style="zoom:67%;" />

<br>
<br>

## Bus Arten

> ***Serieller Bus***
> Senden der Information nacheinander

> ***paralleler Bus***
> Senden der Information über mehrere Signalleitungen, sodass mehrere Informationspakete übertragen werden können.

>***Adressbus***
>Übertragung von Speicher- und Peripherieadressen.
>Auf dem Adressbus werden die Adressen angelegt wohin sie geschrieben werden sollen.

>***Datenbus***						
>Übertragung zwischen CPU, RAM und Peripherie.

> ***Steuerbus***
> Regelung der Übertragung bestimmter Signale an einzelne Komponenten.
> Lesen aus RAM, Schreiben in RAM, Ein- und Ausgabe von peripheren Geräten, Interrupt Signale

<br>
<br>

## Lese/Schreibvorgang

Zunächst legt die CPU die ***Speicheradresse auf*** den ***Adressbus***.
Danach werden die ***Read-Leitungen***, welche im Controller sitzen, auf ***high*** gesetzt, damit der RAM Inhalt ausgelesen möchte.

Wenn der RAM fertig ist wird das ***Datum auf*** den ***Datenbus gelegt*** und signalisiert mit einem high auf der Read-Leitung, dass die CPU dies auslesen kann.

Sobald die CPU das Datum ausgelesen hat, wird die ***Read-Leitung*** auf ***low*** gesetzt und ist damit wieder frei für den nächsten Auftrag.



