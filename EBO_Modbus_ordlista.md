# Ordlista för tolkning av signalnamn i EBO / Modbus

Denna ordlista är avsedd som stöd för en språkmodell eller agent som ska tolka Modbuslistor, driftbilder och funktionsbilder och därefter föreslå EBO-namn och suffix.

Grundprincipen är:

> Tolka först signalens funktion. Välj suffix därefter.

Ett ord i en driftbild eller punktlista ska inte automatiskt kopplas till ett suffix utan att sammanhanget kontrolleras.

## Generella begrepp

| Vanligt ord | Andra varianter | Tolkning |
|---|---|---|
| Börvärde | BV, Bv, Setpoint, SP, Set, Inställt värde, Önskat värde, Referens | Önskat mål |
| Beräknat börvärde | Ber BV, Beräknad BV, Calc SP, Effective SP, Aktivt börvärde, Reglerbörvärde | Börvärde efter logik eller kompensering |
| Ärvärde | ÄV, Aktuellt värde, Mätvärde, Processvärde, PV, Actual, Present Value | Verkligt aktuellt värde |
| Manöver | Start, Stop, Till, Från, Kommando, Command, Cmd, Enable, Run command | Order till utrustning |
| Indikering | Ind., Ind, Status, Feedback, FB, Signal, Återkoppling | Vad utrustningen eller givaren rapporterar |
| Driftsvar | Driftind., Running, Run feedback, Run status, Motor running | Verifiering att utrustningen faktiskt går |
| Tillstånd | State, Mode, Status, Operating state, Driftläge | Logiskt tillstånd |
| Styrsignal | Output, AO, DO, Control signal, Command value, Speed command | Utsignal till utrustning |
| Verkningsgrad | Verkn.grad, Efficiency, η, Eff | Beräknad effektivitet |
| Manuellstyrning | Manual, Hand, Override, Force, Forced, Handkörning | Lokal eller programmatisk tvångsstyrning |
| Auto | Automatic, Reglering, Normal, Remote | Automatisk styrning |
| Larm | Alarm, Fault, Fel, Trip, Warning, Varning | Fel- eller avvikelsestatus |
| Summalarm | Common alarm, General fault, Sum alarm, Collective alarm | Samlat larm |
| Kvittering | Ack, Acknowledge, Reset alarm | Kvittera larm |
| Återställning | Reset, Reset fault, Reset trip | Återställning |
| Gräns | Limit, Threshold, Lim, Set limit | Larm- eller reglergräns |
| Höggräns | High limit, Hi, HL | Övre gräns |
| Låggräns | Low limit, Lo, LL | Nedre gräns |
| Fördröjning | Delay, Timer, T, Time delay | Tidsfördröjning |
| Eftergång | Run-on, Overrun, Postrun | Fortsatt drift efter stoppbegäran |
| Blockering | Interlock, Inhibit, Blocked, Disabled | Funktion hindrad |
| Förregling | Interlock, Permissive | Villkor som måste vara uppfyllt |
| Driftvillkor | Enable condition, Permissive, Start condition | Krav för drift |
| Startvillkor | Start permissive, Enable | Villkor för start |
| Nödstopp | Emergency stop, E-stop, ESTOP | Säkerhetsstopp |
| Drifttid | Runtime, Run hours, Operating hours | Ackumulerad drifttid |

## Luftbehandlingsaggregat

| Begrepp | Andra varianter | Betydelse |
|---|---|---|
| Tilluft | TL, Supply air, SA | Luft in till lokaler |
| Frånluft | FL, Extract air, EA | Luft från lokaler |
| Uteluft | UL, Outside air, OA | Luft utifrån |
| Avluft | AL, Exhaust air | Luft som lämnar aggregatet |
| Tilluftsfläkt | TF, SAF, Supply fan | Fläkt för tilluft |
| Frånluftsfläkt | FF, EAF, Extract fan | Fläkt för frånluft |
| Filter | Filter, Filt | Luftfilter |
| Filtertryck | ΔP filter, Difftryck, Filter DP | Tryckfall över filter |
| Spjäll | Damper, DMP, ST | Luftspjäll |
| Brandspjäll | Fire damper, FD | Brandskyddsspjäll |
| Återvinning | VVX, Heat recovery, HR, HX | Värmeåtervinning |
| Rotor | Roterande VVX, Rotary exchanger | Roterande värmeväxlare |
| Plattväxlare | Plate HX | Plattvärmeväxlare |
| Bypass | Bypass damper | Förbikoppling |
| Frostskydd | Frysvakt, Frost protection, FP | Skydd mot frysning |
| Värmebatteri | Heating coil, HC | Uppvärmning |
| Kylbatteri | Cooling coil, CC | Kylning |
| Kanaltryck | Duct pressure, Static pressure | Tryck i kanal |
| Luftflöde | Airflow, Flow | Luftmängd |
| CO₂ | Koldioxid | Luftkvalitet |
| VOC | Luftkvalitet | Flyktiga organiska ämnen |

## Undercentral / värmesystem

Vanliga ord och uttryck:

- Framledning
- FL
- Supply temperature
- Returledning
- RL
- Return temperature
- Radiatorkrets
- Värmekrets
- Golvvärme
- Shunt
- Shuntventil
- Blandningsventil
- Sekundär
- Primär
- Delta-T
- ΔT
- Utekompensering
- Värmekurva
- Kurvlutning
- Parallellförskjutning
- Nattsänkning
- Sommardrift
- Vinterdrift
- Varmhållning
- Frostskydd
- Minbegränsning
- Maxbegränsning
- Pumpmotionering
- Pumpstopp
- Pumpstart
- Returbegränsning

Viktigt:

`Framledning BV`, `FL-BV`, `Supply SP` och `Beräknad framledning` kan vara olika funktioner och ska inte automatiskt få samma suffix.

## Frånluftsfläktar

Vanliga signaler:

- Start
- Stop
- Drift
- Driftsvar
- Driftindikering
- Styrsignal
- Varvtalsbörvärde
- Varvtal
- Frekvens
- Hz
- Frekvensbörvärde
- Motorström
- Effekt
- Energi
- Summalarm
- Motorfel
- Frekvensomriktarfel
- Hand/Auto
- Serviceomkopplare
- Tryckbörvärde
- Kanaltryck
- Flödesbörvärde
- Luftflöde

Viktigt:

`Drift` kan betyda både kommando och återkoppling beroende på tillverkare och sammanhang.

## Kylmaskiner

Vanliga ord och signaler:

- Kylmaskin
- Chiller
- Compressor
- Kompressor
- Evaporator
- Förångare
- Condenser
- Kondensor
- Kylmedel
- Köldbärare
- Kylbärare
- KB
- KB fram
- KB retur
- Brine
- Brine in/out
- CHW supply
- CHW return
- Leaving water temperature
- Entering water temperature
- LWT
- EWT
- Kompressorlast
- Capacity
- Load
- Demand
- Steg 1
- Steg 2
- Steg 3
- Cooling demand
- Kylbehov
- Börvärde kylvatten
- Kondensortryck
- Förångningstryck
- Hetgastemperatur
- Sugtryck
- Hetgastryck
- Suction pressure
- Discharge pressure
- High pressure
- Low pressure
- HP
- LP
- Freeze protection
- Flow switch
- Flödesvakt
- Driftklar
- Ready
- Available
- Enabled
- Running
- Trip
- Lockout

Viktigt att skilja på:

- `Enable` = tillåt drift
- `Demand` = behov finns
- `Running` = maskinen går
- `Ready` = maskinen kan starta

## Kylsystem

Vanliga begrepp:

- Kylkrets
- Primärkrets
- Sekundärkrets
- Kylvatten
- Köldbärare
- Kylbärare
- Glykol
- Shunt
- Bypass
- Differenstryck
- ΔP
- Kylventil
- 2-vägsventil
- 3-vägsventil
- Kylpump
- Primärpump
- Sekundärpump
- Framledningstemperatur
- Returtemperatur
- Temperaturdifferens
- Flöde
- Flödesbörvärde
- Minflöde
- Maxflöde
- Frikyla
- Free cooling
- Dry cooler
- Vätskekylare
- Kondensorfläkt
- Driftfall
- Kylbehov
- Kylsteg

## Tryckluftsanläggningar

Vanliga ord och signaler:

- Kompressor
- Compressor
- Lastad
- Avlastad
- Loaded
- Unloaded
- Load
- Unload
- Start
- Running
- Ready
- Available
- Local
- Remote
- Auto
- Manual
- Tryck
- Discharge pressure
- System pressure
- Nättryck
- Börtryck
- Pressure setpoint
- Dagpunkt
- Dew point
- Tork
- Dryer
- Torkfel
- Filtertryckfall
- Diff pressure
- Kondensatavskiljare
- Drain
- Purge
- Motorström
- Effekt
- Energiförbrukning
- Drifttimmar
- Lasttimmar
- Service
- Service required
- Warning
- Alarm
- Shutdown
- Emergency stop

Viktigt:

`Loaded / Unloaded` är inte samma sak som `Running / Stopped`.

En kompressor kan gå men vara avlastad.

## Pumpar

Vanliga ord och signaler:

- Pump
- P
- Cirkulationspump
- CP
- Start
- Stop
- Drift
- Driftsvar
- Run
- Running
- Enable
- Ready
- Fel
- Trip
- Summalarm
- Motorfel
- Torrkörning
- Dry run
- Lågt tryck
- Högt tryck
- Lågt flöde
- Flödesvakt
- Differenstryck
- DP
- Tryckbörvärde
- Varvtal
- RPM
- Frekvens
- Hz
- Hastighetsbörvärde
- Speed reference
- Speed feedback
- Auto
- Hand
- Lokal
- Remote
- Duty
- Standby
- Lead
- Lag
- Växling
- Motionering
- Eftergång
- Blockerad

### Tvillingpumpar

- Lead pump
- Lag pump
- Duty pump
- Standby pump
- Pump 1 aktiv
- Pump 2 aktiv
- Alternering
- Växeldrift

## Motorer

Vanliga ord och signaler:

- Motor
- M
- Start
- Stop
- Run
- Running
- Run command
- Run feedback
- Enable
- Motor enable
- Motor status
- Motor fault
- Trip
- Thermal trip
- Överlast
- Overload
- Motorskydd
- Motor protection
- Kontaktor
- Contactor
- Frekvensomformare
- VFD
- VSD
- Drive
- Speed
- Speed SP
- RPM
- Hz
- Current
- Ampere
- A
- Power
- kW
- Torque
- Moment
- Direction
- Forward
- Reverse
- Lokal
- Remote
- Auto
- Manual
- Service

## Tvetydiga ord som måste tolkas i sammanhang

Följande ord får inte automatiskt översättas till ett visst suffix:

- Status
- Drift
- Aktiv
- Enable
- On
- Till
- Ind.
- Feedback
- Control
- Output
- Value
- State
- Mode
- Demand
- Request
- Ready
- Available
- Alarm
- Fault
- Warning

Exempel:

`TF01 Drift` kan beroende på sammanhang betyda:

- startkommando
- driftsvar
- tillstånd
- driftfall
- enable

Agenten ska därför analysera:

1. närliggande signaler
2. apparatens funktion
3. enhet
4. datatyp
5. R eller R/W
6. systembild
7. signalens plats i logiken

innan suffix väljs.

## Rekommenderad agentregel

> Skapa en intern synonymordlista där flera ord kan mappas till samma funktionella kategori, men välj EBO-suffix först efter att den funktionella rollen är verifierad.

> Utgå från funktion först, suffix därefter. Utgå aldrig från signalnamnets ordval ensamt.
