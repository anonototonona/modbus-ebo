# EBO-suffix

Denna fil är konverterad från den ursprungliga Excel-listan med EBO-suffix.

Suffix ska väljas utifrån signalens funktion och sammanhang. Om underlaget är otillräckligt eller motsägelsefullt ska signalen markeras som **KONTROLL** i stället för att ett suffix gissas.

> **Obs:** Stavning, benämningar och suffix har bevarats från källfilen. Eventuella avvikelser eller äldre benämningar bör verifieras mot aktuell konstruktionsmanual innan de används som normerande standard.

## Givande reglerande med frysskyddsfunktion

| Beskrivning | Suffix |
|---|---|
| Beräknat Börvärde | `_BB` |
| Larmgräns Frysvakt | `_LLG` |
| Börvärde retur stoppat system | `_RET B` |
| Börvärde retur vid drift | `_MIN B` |
| Återställning frysvakt | `_ÅTSTART` |
| Larm Utlost Frysvakt | `_FT` |
| Larm Givarfelslarm | `_GF` |

## Givare reglerande allmant

| Beskrivning | Suffix |
|---|---|
| Beräknat Börvärde | `_BB` |
| Grundbörvärde | `_B` |
| Differens Laglarm | `_LLD` |
| Differens Hoglarm | `_HLD` |
| Larmfördröjning | `_LT` |
| Dödzon | `_DZ` |
| Larm Laglarm | `_LL` |
| Larm Hoglarm | `_HL` |
| Larm Givarfelslarm | `_GF` |

## Givare allmänt

| Beskrivning | Suffix |
|---|---|
| Larmfördröjning* | `_LT` |
| Låglarm gräns* | `_LLG` |
| Höglarm gräns* | `_HLG` |
| Larm Låglarm* | `_LL` |
| Larm Höglarm* | `_HL` |
| Larm Givarfelslarm* | `_GF` |

## Styrkurva

| Beskrivning | Suffix |
|---|---|
| Brytpunkt Kurva (Indata) | `_X1` |
| Brytpunkt Kurva (Utdata) | `_Y1` |
| Brytpunkt Kurva (Indata) | `_X2` |
| Brytpunkt Kurva (Utdata) | `_Y2` |
| Ytterligare n brytpunkter lika ovan* | `_Xn, _Yn` |
| Parallellförskjutning kurva | `_FS` |

## Reglerande ställdon med frysvaktsfunktion.

| Beskrivning | Suffix |
|---|---|
| Värmereglering P-Band | `_PB` |
| Värmereglerig I-Tid | `_IT` |
| Värmereglering D-Tid | `_TD` |
| Minbegränsnings reg. P-band | `MIN_PB` |
| Minbegränsnings reg. P-band | `MIN_IT` |
| Minbegränsnings reg. P-band | `MIN_TD` |
| Varmhållningsreglering P-band | `RET_PB` |
| Varmhållningsreglering P-band | `RET_IT` |
| Varmhållningsreglering P-band | `RET_TD` |
| Larm Minbegränsning aktiv | `MIN_L` |

## Reglerande ställdon allmänt

| Beskrivning | Suffix |
|---|---|
| Reglering P-Band | `_PB` |
| Reglerig I-Tid | `_IT` |
| Reglering D-Tid | `_TD` |

## Ställdon allmänt

| Beskrivning | Suffix |
|---|---|
| Styrsignal ställdon (analogt) | `(Utan Suffix)` |
| Styrsignal ställdon (digitalt) | `(Utan Suffix)` |
| Återföring Öppet läge* | `_Ö` |
| Återföring Stängt läge* | `_S` |
| Larm Avvikande läge* | `_AL` |

## Reglerande värmeåtervinning

| Beskrivning | Suffix |
|---|---|
| Styrsignal ställdon | `(Utan Suffix)` |
| Reglering P-Band | `_PB` |
| Reglerig I-Tid | `_IT` |
| Reglering D-Tid | `_TD` |
| Verkningsgrad* | `_V` |
| Gräns styrsignal för beräkning av V.grad* | `_G` |
| Larmgräns låg verkningsgrad* | `_LLG` |
| Larm Summalarm återvinning* | `_SL` |
| Larm Låg verkningsgrad* | `_LL` |

## Motor

| Beskrivning | Suffix |
|---|---|
| Driftindikering* | `_D` |
| Drifttid | `_DT` |
| Drifttidlarmgräns | `_DLG` |
| Stoppgräns | `_STP` |
| Nollställning Drifttid | `_NDT` |
| Stopp fördröjning | `STOPP_FD` |
| Start fördröjning | `START_FD` |
| Felfördröjning | `FEL_FD` |
| Gräns driftindikering | `_GRI` |
| Larm Driftstopp | `_DS` |
| Larm Handmanöver | `_HM` |
| Larm Allmänt | `_L` |
| Larm Drifttid | `_DTL` |

## Frekvensomformare

| Beskrivning | Suffix |
|---|---|
| Reglering P-Band* | `_PB` |
| Reglering I-Tid* | `_IT` |
| Reglering D-Tid* | `_TD` |
| Börvärde Styrsignal* | `_B` |
| Larm Summalarm frekvensomformare | `_SL*` |

## Förbrukningsmätare

| Beskrivning | Suffix |
|---|---|
| Mätarställning energi | `_Q` |
| Mätarställning volym | `_V` |
| Aktuell uttagen effekt | `_E` |
| Aktuellt Flöde | `_F` |
| Temperatur Hög | `_TH` |
| Temperatur Låg | `_TL` |
| Temperatur Delta | `_TD` |

### El

| Beskrivning | Suffix |
|---|---|
| Mätarställning energi | `_Q` |
| Aktuell uttagen effekt | `_E` |
| Ström L1 | `_IL1` |
| Ström L2 | `_IL2` |
| Ström L3 | `_IL3` |
| Effektivvärde Ström | `_IA` |

### Vatten

| Beskrivning | Suffix |
|---|---|
| Mätarställning | `_V` |

## Timer

| Beskrivning | Suffix |
|---|---|
| Indikering timer | `_D` |
| Timertid | `_T` |
| Timertid kvar vid aktivering | `_TL` |
| Manuell Start/stopp timer | `Aktivera` |

## Larm Allmänt

| Beskrivning | Suffix |
|---|---|
| Larmfördröjning | `_LT` |
| Larm Summalarm | `_SL` |
| Larm Allmänt larm | `_L` |

## Driftfall

| Beskrivning | Suffix |
|---|---|
| Korsvisförreglings funktion utlöst | `Korsför` |
| Korsvisförregling val (Till/Från) | `Korsvis` |
| Kylåtervinning aktiv* | `Kylåter` |
| Natkyla aktiv* | `NKyla` |
| Sommardriftfall aktivt | `Sommar` |
| Sommarmånad | `SoMånad` |
| Vintermånad | `ViMånad` |
| Vintertemp | `ViTemp` |
| Manuell styrning av system | `_MS` |
| Serviceomkopplare | `SO` |
| Larm System styrs manuellt | `LM` |
| Larm Serviceomkopplare ej i läge automatik | `SO_L` |
| Nattsänkning aktiv | `NATT` |
| Manuell styrning av system | `_MS` |
| Larm System styrs manuellt | `LM` |

## Tidschema

| Beskrivning | Suffix |
|---|---|
| Tidschema dagdrift aktiv | `TID_Drift` |
