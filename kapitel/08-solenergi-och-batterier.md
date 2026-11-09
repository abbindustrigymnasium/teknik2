# Kapitel 8: Solceller, batterier och dimensionering

> **I det här kapitlet lär du dig**
> - hur en solcell fungerar och vad en IV-kurva visar
> - hur du beräknar verkningsgrad, energi och drifttid
> - hur en laddare och ett litiumbatteri fungerar tillsammans
> - hur du dimensionerar ett litet off-grid-system och bedömer om resultatet är rimligt

En sensor långt ute i skogen behöver el, men det finns inget eluttag i närheten. Ett **off-grid-system** producerar och lagrar sin egen energi. Det låter enkelt: en solpanel och ett batteri. Men räknar du fel lyser lampan bara några timmar efter en mulen dag, eller så laddas batteriet aldrig fullt. I det här kapitlet lär du dig att räkna innan du bygger och att mäta efteråt.

## Energisystemets delar

```mermaid
flowchart LR
    A[Solpanel] --> B[Laddare CN3065]
    B --> C[Li-ion-batteri]
    C --> D[Eventuell spänningsomvandlare]
    D --> E[Last]
```

Varje del har förluster, så att energin som kommer ut är mindre än energin som kommer in.

## Solcellen

En solcell består av en halvledare, vanligen kisel. **Den fotovoltaiska effekten** innebär att ljus lyfter elektroner till en högre energinivå. Övergången mellan två olika dopade halvledarskikt, en så kallad pn-övergång, driver då en ström i en yttre krets. **Monokristallint kisel** består av ett sammanhängande kristallgitter och ger god verkningsgrad.

### IV-kurvan

En panel har inte en bestämd effekt. Effekten beror på ström, spänning och belastning. **IV-kurvan** visar ström som funktion av spänning, och **effektkurvan** visar P = U · I.

- **Tomgångsspänning (U_oc)** är spänningen utan belastning. Strömmen är då noll.
- **Kortslutningsström (I_sc)** är strömmen utan spänning. Effekten är då noll.
- **MPP** (Maximum Power Point) är punkten där effekten är störst.

### Genomräknat exempel: hitta MPP

Följande värden är påhittade men realistiska för en panel på 6 V och 210 mA:

| U (V) | I (A) | P = U · I (W) |
|---|---|---|
| 6,6 | 0,000 | 0,000 |
| 6,2 | 0,060 | 0,372 |
| 6,0 | 0,120 | 0,720 |
| 5,6 | 0,190 | 1,064 |
| 5,0 | 0,205 | 1,025 |
| 4,0 | 0,210 | 0,840 |
| 0,0 | 0,215 | 0,000 |

Maxeffekten i tabellen är cirka 1,06 W vid 5,6 V. Märkeffekten 1,25 W gäller vid standardiserade provningsförhållanden, medan dina mätningar sker i verkligt ljus. Därför är det rimligt att mäta lägre effekt. Skugga, smuts, värme och fel vinkel sänker effekten ytterligare.

### Verkningsgrad

**Verkningsgraden** η är nyttig effekt dividerad med tillförd effekt.

**Exempel.** En panel är 110 × 69 mm. Instrålningen är 800 W/m². Panelen ger 0,95 W.

- Area: 0,110 · 0,069 = 0,00759 m²
- Tillförd effekt: 800 · 0,00759 ≈ 6,07 W
- Verkningsgrad: 0,95 / 6,07 ≈ 0,156, alltså cirka 16 %

Måtten är exempel. Mät din panels aktiva yta. En luxmätare mäter synligt ljus, så om du räknar om lux till W/m² är det en uppskattning, som dessutom beror på ljuskällans spektrum.

## Batteriet

Ett **litiumjonbatteri** lagrar energi kemiskt, genom att litiumjoner rör sig mellan elektroderna. En vanlig cell har märkspänningen 3,6–3,7 V och laddas till högst 4,2 V. Kapaciteten anges i ampertimmar (Ah) eller milliampertimmar (mAh). Energin i wattimmar är kapacitet · spänning.

**Exempel.** En 18650-cell på 2 500 mAh och 3,7 V lagrar 2,5 · 3,7 = 9,25 Wh. Räknar du bara med 90 % användbar energi blir det cirka 8,3 Wh. Kontrollera databladet för din cell.

## Laddaren

CN3065 är en laddningskrets för en cell. Den laddar enligt principen **konstant ström, sedan konstant spänning (CC/CV)**: först med begränsad ström, och när cellen nått 4,2 V hålls spänningen medan strömmen minskar. Läs databladet för just din modul, eftersom modulerna skiljer sig åt.

CN3065 är en **linjär** laddare. Skillnaden mellan panelens spänning och batteriets spänning blir värme. Om panelen levererar 0,19 A vid 5,6 V och batteriet är på 3,7 V tas ungefär 0,19 · 3,7 ≈ 0,70 W upp i batteriet av de 1,06 W som panelen levererar. Verkningsgraden är 3,7 / 5,6 ≈ 66 %.

## Dimensionering

Att **dimensionera** är att räkna fram vilka storlekar som behövs för att uppfylla kraven.

### Genomräknat exempel: en sensornod

En sensor drivs med 5 V via en step-up-modul med verkningsgraden 85 %. Den drar i snitt 40 mA vid 5 V.

**Steg 1: lasten.**

- På 5 V-sidan: P = 5 · 0,040 = 0,20 W
- Från batteriet: 0,20 / 0,85 ≈ 0,235 W

**Steg 2: drifttid på batteri.** 8,3 Wh / 0,235 W ≈ 35 h.

**Steg 3: energi per dygn.** 24 h · 0,235 W ≈ 5,6 Wh.

**Steg 4: vad panelen ger.** Anta 3 timmar per dygn med effekt nära MPP. Då går det in 0,70 W · 3 h ≈ 2,1 Wh i batteriet.

**Slutsats.** Panelen täcker bara ungefär 37 % av behovet. Systemet går inte i balans. Vad gör vi?

| Åtgärd | Effekt |
|---|---|
| Låt sensorn vara aktiv 25 % av tiden och dra 2 mA i viloläge: snitt 11,5 mA, cirka 1,6 Wh/dygn | Går i balans |
| Större panel | Mer energi, men större, dyrare och mer material |
| Större batteri | Klarar fler dagar utan sol, men ger inte mer energi över tid |

Den billigaste och klokaste åtgärden är oftast att **minska förbrukningen**. Antagandet om soltimmar är avgörande: mörka vinterveckor ger mycket mindre energi än sommaren. Skriv ut dina antaganden, så att någon annan kan kontrollera dem.

### Laddtid

Med 190 mA tar 2 500 mAh minst 2 500 / 190 ≈ 13 timmar. Lägger du till ungefär 10 % för förluster i laddningen hamnar du nära 14,5 timmar med full sol. Det är ingenting du kan vänta dig på en dag.

## Verifiering

Beräkningarna är en modell, och den ska jämföras med verkligheten. Du behöver mäta:

- spänningen över panel, batteri och last,
- strömmen in till batteriet och ut till lasten,
- hur länge systemet körs.

En multimeter i strömläge ska kopplas i **serie**, och en voltmeter **parallellt**. Att lägga en amperemeter över ett batteri är en kortslutning.

## Begrepp

- **Off-grid:** system utan anslutning till elnätet.
- **Fotovoltaisk effekt:** ljus skapar elektrisk spänning i en halvledare.
- **IV-kurva:** ström som funktion av spänning.
- **MPP:** punkten med högst effekt.
- **Verkningsgrad:** nyttig effekt delad med tillförd effekt.
- **Kapacitet:** batteriets laddning, i Ah eller mAh.
- **CC/CV:** laddning med konstant ström och sedan konstant spänning.
- **Linjär laddare:** laddare där överskottsspänningen blir värme.
- **Dimensionering:** att beräkna vilka storlekar som krävs.

## Testa dig själv

1. Varför är effekten noll både vid tomgång och kortslutning?
2. Varför kan du mäta lägre effekt än märkeffekten?
3. Vad händer med energi när en linjär laddare arbetar?
4. Vad skiljer kapacitet i mAh från energi i Wh?
5. Varför är minskad förbrukning ofta bättre än en större panel?
6. Hur ska en amperemeter kopplas?
7. Varför är antagandena i en dimensionering viktiga att skriva ut?

## Övningar

**Grund.** En panel är 0,10 m · 0,07 m och levererar 0,8 W vid 700 W/m². Beräkna verkningsgraden.

<details><summary>Svar</summary>

Tillförd effekt: 700 · 0,007 = 4,9 W. Verkningsgrad: 0,8 / 4,9 ≈ 0,163, cirka 16 %.

</details>

**Grund.** En 3,7 V-cell har kapaciteten 1 800 mAh. Hur mycket energi lagrar den?

<details><summary>Svar</summary>

1,8 Ah · 3,7 V = 6,66 Wh.

</details>

**Vidare.** En LED-lampa drar 0,5 W i 6 timmar per natt. Hur mycket energi behövs per natt? Räcker ett batteri på 6,66 Wh med 90 % användbar kapacitet?

<details><summary>Svar</summary>

0,5 · 6 = 3,0 Wh. Användbart: 6,66 · 0,9 ≈ 6,0 Wh. Det räcker i ungefär två nätter.

</details>

**Vidare.** Mät en IV-kurva för din panel i två olika vinklar och beräkna MPP. Hur mycket skiljer det?

**Utmaning.** Dimensionera ett system för en sensor som drar 10 mA vid 3,3 V konstant. Välj antaganden, beräkna hur stort batteri och hur stor panel som krävs för tre mulna dagar. Redovisa alla antaganden.

## Koppling till projektet

Det här är grunden för [MikroGrid](../projekt/mikrogrid/README.md). Du mäter IV-kurvor, dimensionerar ett system och kontrollerar att beräkningarna stämmer. Eftersom ni ska mäta under belastning hör [kapitel 6](06-kvalitet-och-risk.md) ihop med det här kapitlet.

## Läs mer

- [Energimyndigheten](https://www.energimyndigheten.se/)
- [Fraunhofer ISE Photovoltaics Report](https://www.ise.fraunhofer.de/en/publications/studies/photovoltaics-report.html)

[← Föregående](07-databaser-och-digitalisering.md) | [Innehåll](../README.md) | [Nästa →](09-livscykelanalys-och-varden.md)
