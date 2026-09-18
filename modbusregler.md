# Modbusregler

## Syfte

Denna fil hjälper agenten att tolka Modbuspunkter funktionellt.

Modbusinformationen ska aldrig ensam avgöra EBO-namn. Signalnamn, beskrivning, registertyp, datatyp, enhet, skalning och läs-/skrivbehörighet ska vägas ihop.

---

## Registertyper

### Coil

Boolesk signal, 0 eller 1.

Kan användas för:
- start/stopp
- enable/disable
- reset
- manöver

Kan normalt läsas och skrivas.

### Discrete Input

Boolesk signal, 0 eller 1.

Används ofta för:
- driftindikering
- larm
- gränsläge
- status

Normalt endast läsning.

### Holding Register

16-bitars register.

Kan innehålla:
- heltal
- unsigned heltal
- börvärden
- parametrar
- tidvärden
- statusord
- delar av Float32-värden

Kan normalt läsas och skrivas.

### Input Register

16-bitars register.

Används ofta för:
- temperatur
- tryck
- flöde
- mätvärden

Normalt endast läsning.

---

## Datatyper

### Bool

Två tillstånd:
- 0 = False
- 1 = True

### Int16

Signed 16 bit.

Område:
-32768 till 32767

Används när negativa värden kan förekomma.

### UInt16

Unsigned 16 bit.

Område:
0 till 65535

Används när negativa värden inte är möjliga, exempelvis:
- tid
- räknare
- procent
- statuskod

### Int32 / UInt32

Använder normalt två register.

### Float32

Använder normalt två 16-bitars register.

Byte order och word order måste kontrolleras.

---

## Funktionell tolkning

### Bool + Read Only

Talar ofta för:
- indikering
- status
- drift
- larm

### Bool + Read/Write

Talar ofta för:
- manöver
- start/stopp
- enable
- reset

### Numerisk + Read Only

Talar ofta för:
- mätvärde
- temperatur
- tryck
- flöde
- varvtal

### Numerisk + Read/Write

Talar ofta för:
- börvärde
- parameter
- gränsvärde
- tidsinställning

Detta är ledtrådar, inte absoluta regler.

---

## Skalning

Kontrollera alltid skalning.

Exempel:

Registervärde:
215

Skalning:
0.1

Verkligt värde:
21.5 °C

Agenten får inte anta skalning om den saknas.

---

## Enhet

Enheten hjälper till att avgöra signalens funktion.

Exempel:

°C  
→ sannolikt temperatur

Pa  
→ sannolikt tryck

%  
→ kan vara börvärde, återkoppling eller mätvärde

sekunder/minuter/timmar  
→ ofta parameter eller tidsinställning

---

## Statusord

Ett Holding Register kan vara ett statusord.

Exempel:

Registervärde:
5

Binärt:
0000000000000101

Det betyder att flera bitar kan representera olika tillstånd.

Ett statusord ska därför inte automatiskt behandlas som ett vanligt numeriskt mätvärde.

---

## Namntolkning

Signalens text ska användas tillsammans med Modbusinformationen.

Exempel:

Signalnamn:
Fan Start

Om signalen är:
Read/Write + Bool  
→ sannolikt startkommando

Om signalen är:
Read Only + Bool  
→ kan istället vara startstatus eller indikering

---

## Konflikter

Om informationen säger emot sig själv ska agenten inte gissa.

Exempel:

Signalnamn:
Supply Air Temperature

Datatyp:
Bool

Detta är en konflikt.

Resultat:
KONTROLL

---

## Osäkerhet

Markera punkten som **KONTROLL** om:

- funktionen inte kan avgöras
- registertypen verkar fel
- datatypen verkar orimlig
- skalning saknas
- enheten inte stämmer
- signalnamnet är tvetydigt
- flera EBO-suffix är möjliga

Agenten ska hellre markera **KONTROLL** än välja ett suffix på osäker grund.

---

## Grundprincip

Modbusdata ska ge ledtrådar, inte facit.

Agenten får inte dra slutsatsen att en viss registertyp, datatyp eller läs-/skrivbehörighet automatiskt innebär en viss EBO-funktion.

Alla tillgängliga uppgifter ska vägas samman innan klassificering och namnförslag görs.
