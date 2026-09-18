# Modbus till EBO

Kunskapsbas för tolkning av Modbus-signaler och namngivning enligt EBO-standard.

Syftet är att hjälpa en Copilot-agent att analysera Modbuslistor från PLC, DUC och andra automationssystem och föreslå konsekventa EBO-namn utifrån signalens verkliga funktion.

## Kunskapsbas

- [Ordlista](EBO_Modbus_ordlista.md)  
  Förklarar vanliga förkortningar, komponentnamn och tekniska begrepp inom fastighetsautomation.

- [EBO-suffix](ebo-suffix.md)  
  Innehåller suffixstandard och regler för hur olika typer av signaler ska namnges i EBO.

- [Modbusregler](modbusregler.md)  
  Beskriver hur registertyp, datatyp, läs-/skrivbehörighet, skalning och enhet kan användas som stöd vid funktionell tolkning av en Modbuspunkt.

## Grundprincip

En Modbuspunkt ska inte klassificeras enbart utifrån registertyp eller datatyp.

Följande information ska vägas samman:

1. Signalnamn
2. Beskrivning
3. Utrustningens funktion
4. Registertyp
5. Datatyp
6. Läs-/skrivbehörighet
7. Skalning
8. Enhet
9. Systembild eller funktionsbeskrivning, om sådan finns

## Arbetsgång

Vid analys av en Modbuslista:

1. Identifiera vad signalen faktiskt representerar.
2. Använd ordlistan för att tolka förkortningar och utrustningsnamn.
3. Använd Modbusreglerna för att bedöma signaltyp och rimlighet.
4. Matcha funktionen mot rätt EBO-suffix.
5. Kontrollera datatyp, skalning, enhet och läs-/skrivbehörighet.
6. Markera signalen som **KONTROLL** om informationen är motsägelsefull eller otillräcklig.

## Viktigt

Kunskapsbasen är ett stöd för tolkning och kvalitetssäkring.

Den ska inte användas för att gissa när underlaget är otillräckligt. Om flera tolkningar är möjliga ska punkten markeras som **KONTROLL** i stället för att agenten väljer ett namn på osäker grund.
