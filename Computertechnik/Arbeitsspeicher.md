# Arbeitsspeicher

- [Arbeitsspeicher](#arbeitsspeicher)
  * [Geschichtlicher Hintergrund](#geschichtlicher-hintergrund)
  * [Nicht flüchtige Speicher (ROM)](#nicht-fl-chtige-speicher--rom-)
  * [flüchtiger Speicher (RAM)](#fl-chtiger-speicher--ram-)
    + [Statische RAM (SRAM)](#statische-ram--sram-)
    + [Dynamische RAM (DRAM)](#dynamische-ram--dram-)
      - [DRAM Typen](#dram-typen)
    + [Speichertiming](#speichertiming)
      - [Standard DRAM](#standard-dram)
      - [Page Mode DRAM](#page-mode-dram)
      - [Burst EDO RAM](#burst-edo-ram)
      - [Registered Dimm](#registered-dimm)
      - [Dimm mit Fehlerkorrektur (ECC)](#dimm-mit-fehlerkorrektur--ecc-)

<br>

## Geschichtlicher Hintergrund

<br>

Zunächst gab es keine Arbeitsspeicher, sondern lediglich ***Register***.
Das Problem war, dass sofern kein Strom fließt, auch ***keine Informationen gespeichert*** werden konnten.
Eine frühe Form waren ***Kernspeicher***, ***Magetkernspeicher*** oder auch ***Ferritkernspeicher***, kleine Spulen, die Magnetfelder erzeugen und die Informationen gespeichert werden

Das ***erste statische RAM*** (alle Informationen müssen bis zu einem bestimmten Byte komplett entladen und beladen werden) hatte eine Speicherkapazität von ***64 Bit***.

<br>

![237756827-5e5f5c99-fc8b-4e25-89f7-b18741257569](https://github.com/mysdiir/FIAE_Kompendium/assets/70364903/0a0b468d-f915-4c83-bcc1-19cd78c8e5eb)

<br>

Der erste ***dynamische RAM*** (DRAM) ermöglichte einen ***wahlfreien Zugriff auf das RAM***, also erschuf die Möglichkeit gezielt auf dein Byte zuzugreifen.

<br>

![237756831-12744306-827e-4de2-ad17-74bb84fcde59](https://github.com/mysdiir/FIAE_Kompendium/assets/70364903/8a4382c0-41f5-414a-82da-bc120ddb34f0)

<br>
<br>

## Nicht flüchtige Speicher (ROM)

***Read-Only-Memory***, bzw. nicht flüchtige Speicher sind Speicher, auf die im normalen Betrieb nur ***lesend zugegriffen*** werden kann.

<br>

![237756838-ddce50f4-2a24-4c82-ab7f-fa943128834f](https://github.com/mysdiir/FIAE_Kompendium/assets/70364903/d609255d-7cd3-4ac1-8a8f-2a142783aae8)

<br>

> ***Masken ROM***
>
> Informationen werden bei der Herstellung fest eingebrannt und könne nicht mehr gelöscht werden
> Kann BIOS enthalten

<br>

> ***PROM (Programmable Read-Only-Memory)***
>
> Nur einmalig elektrisch beschreibbar
> nicht löschbar

<br>

> **EEPROM (Electrically Erasable Programmable Read-Only-Memory)**
>
>
> elektrisch beschreibbar und löschbar
> Enthalten meistens das BIOS
> Updatefähig

<br>

> ***Flash-EPROM***
> Elektrisch beschreibbar und löschbar
> auch als NAND-Flash-Speicher beschreibbar
> SSD
> NAND Flash-Speicher, auf die Daten geschrieben werden
> jede Speicherzelle akzeptiert eine bestimmte Menge an Bits

<br>

> ***TLC (Tripple-Level Cell)***
> speichert drei Informationseinheiten pro Zelle
> eine Zelle kann 8 unterschiedliche Spannungszustände annehmen

<br>

> ***QLC (Quad-Level Cell)***
> speichert vier Informationsbit pro Zelle
> eine Zelle kann 16 unterschiedliche Spannungszustände annehmen

<br>
<br>

## flüchtiger Speicher (RAM)


### Statische RAM (SRAM)

> Vorteile
> sehr schnell
> benötigt zur Datenspeicherung keine Auffrischungszyklen

> Nachteil
> Teuer
> kleinere Kapazität

<br>

### Dynamische RAM (DRAM)

> Vorteile
> Günstiger Preis pro Bit

> Nachteile
> Datenspeicherung erfolgt mittels Transistor. Deshalb sind häufige Auffrischungszyklen notwendig

<br>

#### DRAM Typen

> ***FPM-RAM*** (***Fast Page Mode RAM***)
> Taktfrequenzen von 16 bis 66 MHz
> 72 Pins
> Zugriffszeit von ca. 70 ns

> ***EDO-RAM*** (***Extended Data Output RAM***)
> Zugriffszeit von 50 bis 70 ns
> Taktfrequenz von 33 bis 75 MHz
> Speicherkapazität von bis zu 32MB

> ***SD-RAM***
> alle Signale synchronisiert zum Systemtakt
> Chipsatz und Speicher kommunizieren via Bussystem

> ***DDR2***
> höher getaktet
> Geschwindigkeitsvorteile
> Taktraten bis 800 MHz

<br>

![237756842-a6bcd8d5-b7aa-4bc3-86ce-9bbd3ede4302](https://github.com/mysdiir/FIAE_Kompendium/assets/70364903/1b6e9e00-ac98-4054-be1b-e9c0d9362342)

<br>

> ***DDR3/DDR4***
> Spannungsversorgung 1,5 und 1,2 Volt
> höhere Taktraten


![237756845-626a8677-a599-4d2f-a6b9-c4b236bd3116](https://github.com/mysdiir/FIAE_Kompendium/assets/70364903/4eb8788b-837e-4abe-bf23-173340bc47ad)

<br>


### Speichertiming

Unter Speichertiming versteht man die S***chnelligkeit der Verarbeitung*** eines Auftrags und deren Speicherung, sowie Abruf
im RAM.

<br>

#### Standard DRAM

Wenn eine ***Spalte beschrieben*** wird, wird damit die ***Spannung erhöht***
(steigende Flanke) und es kann in die nächste Spalte gewechselt werden.

<br>

#### Page Mode DRAM

Sobald klar ist, dass ***mehrfach*** eine ***Spalte beschrieben*** wird, ist das ***Deklarieren der Speicherzelle*** als solche unnötig.

<br>

#### Burst EDO RAM

Jedes Mal wenn es zu einer ***fallenden Flanke*** kommt, wird vom RAM die ***nächste Zelle*** ***angewählt***

<br>

![237756846-d5f4a496-df5a-42ea-853f-6282d3988a1a](https://github.com/mysdiir/FIAE_Kompendium/assets/70364903/60c6861f-f6a4-46a4-92f4-e789d3286d2c)


<br>

#### Registered Dimm

Hierbei handelt es sich um eine Sorte von Speichermodulen, die häufig bei ***Server*** oder ***Workstations*** verwendet wird.
Sie haben die Aufgabe die ***elektrische Last von Speichercontroller zu verringern*** und die ***Datenintegrität der zuführenden Speicherchips zu erhöhen***.

> ***Nachteile***
> deutlich höhere Preise
> zwingende Notwendigkeit eines Mainboards
> Eingangssignale erscheinen erst einen Taktzyklus später
> nicht mit Unregistered Modulen kombinierbar

<br>

#### Dimm mit Fehlerkorrektur (ECC)

Der Error Correction Code (ECC) ist ein ***Hashwert*** über die ***64 Bits*** **jeder Speicherzelle**.
Diese Informationen werden vom ***Speichercontroller berechne***t und in ***8 zusätzlichen Bits abgelegt.***
Deswegen haben ECC 72 Bits pro Zeile.
Diese gehasten Werte beinhalten die Grundinformation als gespeicherte, verkleinerte Form.

