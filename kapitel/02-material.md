# Kapitel 2: Material och människans behov

> **I det här kapitlet lär du dig**
> - vad hållfasthet, styvhet och densitet betyder och hur du jämför material
> - varför trä, aluminium, plast, textil och grafen har så olika egenskaper
> - varför ett material inte är bra eller dåligt i sig, utan bra eller dåligt för en viss uppgift
> - hur du analyserar en konstruktion utifrån de behov den ska uppfylla

Varför är flygplan byggda av aluminium i stället för stål? Varför kan en tunn träbalk bära ett tak, samtidigt som en träplatta spricker om du belastar den fel? Och varför är inte biobaserad plast alltid bättre för miljön? Sådana frågor går inte att besvara utan att förstå materialen. När du väljer material väljer du samtidigt hur saken kan tillverkas, hur länge den håller och vad som händer efteråt.

## Egenskaper du behöver kunna jämföra

- **Hållfasthet** är hur stor belastning materialet tål innan det går sönder eller formas om. Den anges som **spänning**, alltså kraft per area, i enheten MPa. 1 MPa är 1 N/mm².
- **Styvhet** är hur lite materialet böjer sig eller töjs under belastning. Ett material kan vara styvt men sprött.
- **Densitet** är massa per volym, i kg/m³.
- **Specifik hållfasthet** är hållfasthet dividerad med densitet. Den visar hur starkt materialet är i förhållande till sin vikt.

Dessutom spelar pris, tillgång, formbarhet, beständighet och miljöpåverkan roll.

## Trä

Trä består av långa celler som ligger i stammens längdriktning. Det gör att egenskaperna beror på riktning. Ett sådant material kallas **anisotropt**. Trä är starkt längs fibrerna, både i drag och i tryck, men svagt tvärs fibrerna. Det är alltså fel att säga att trä generellt tål tryck dåligt. Det som är dåligt är att belasta det tvärs fibrerna, särskilt i drag.

[Träguiden](https://www.traguiden.se/om-tra/materialet-tra/traets-egenskaper-och-kvalitet/mekaniska-egenskaper1/traets-styrka-och-styvhet/) anger ungefärliga värden för felfritt trä av gran och furu med cirka 12 % fuktkvot:

| Belastning | Längs fibrerna | Tvärs fibrerna |
|---|---|---|
| Drag | 100 MPa | 3 MPa |
| Tryck | 50 MPa | 7 MPa |

Virke i verkligheten har kvistar och andra defekter, så konstruktionsvirke har väsentligt lägre värden. När en byggnad dimensioneras används standardiserade hållfasthetsklasser och säkerhetsfaktorer.

### Genomräknat exempel: fibrernas riktning

En felfri träkloss har tvärsnittet 20 × 20 mm. Hur stor tryckkraft tål den ungefär?

Arean är A = 20 · 20 = 400 mm². Kraften blir F = σ · A.

- Längs fibrerna: F = 50 N/mm² · 400 mm² = 20 000 N = 20 kN.
- Tvärs fibrerna: F = 7 N/mm² · 400 mm² = 2 800 N = 2,8 kN.

Samma bit trä tål alltså ungefär sju gånger mer om den belastas i rätt riktning. Det är brottgränser för felfritt trä. Ett riktigt bärverk dimensioneras med lägre värden och säkerhetsmarginaler.

### Fukt och brand

**Fuktkvot** är hur mycket vatten träet innehåller i förhållande till sin torra vikt. Enligt Träguiden ger lägre fuktkvot högre hållfasthet och styvhet, och tryckhållfastheten påverkas mer av fukt än draghållfastheten. Fukt får också träet att svälla och krympa, framför allt tvärs fibrerna, och det kan ge sprickor. Trä som är fuktigt länge kan angripas av mögel och röta, så konstruktionen måste skydda träet och låta det torka.

Trä är brännbart, och det måste alltid beaktas. Grövre virke förkolnar samtidigt relativt långsamt och förutsägbart, så det går att dimensionera för att behålla bärförmågan under en viss tid vid brand.

## Aluminium

Ren aluminium är mjuk och lätt att forma. Hållfastheten kommer från **legering**, alltså inblandning av andra ämnen, ofta tillsammans med värmebehandling. Då blir skillnaden stor.

### Genomräknat exempel: specifik hållfasthet

| Material | Sträckgräns (typvärde) | Densitet | Sträckgräns / densitet |
|---|---|---|---|
| Ren aluminium, mjuk (1100-O) | ca 34 MPa | 2 710 kg/m³ | ca 13 kN·m/kg |
| Stål S355 | 355 MPa | 7 850 kg/m³ | ca 45 kN·m/kg |
| Aluminiumlegering 7075-T6 | ca 480 MPa | 2 810 kg/m³ | ca 171 kN·m/kg |

Så här räknas raden för stål: 355 · 10⁶ Pa / 7 850 kg/m³ ≈ 45 000 N·m/kg = 45 kN·m/kg. Ren aluminium är klart svagare än stål. Legeringen är däremot, räknat per kilo, mycket starkare. Det är därför höghållfasta aluminiumlegeringar [används i flygplansstrukturer](https://en.wikipedia.org/wiki/7075_aluminium_alloy). Värdena varierar med legering och behandling, så en verklig konstruktion bygger på leverantörens data.

### Miljöpåverkan

Att framställa aluminium ur malm kräver mycket energi. [International Aluminium Institute](https://international-aluminium.org/landing/aluminium-recycling-saves-95-of-the-energy-needed-for-primary-aluminium-production/) anger cirka 186 GJ per ton för primär aluminium (globalt genomsnitt, från gruva till gjuten metall) och cirka 8,3 GJ per ton för återvunnen aluminium. Återvinningen kräver alltså bara omkring 4–5 % av energin. Institutet är en branschorganisation och siffrorna är genomsnitt.

Bilden är ändå nyanserad:

- **Elens ursprung** avgör hur stora utsläppen blir. Elektrolys med vattenkraft ger mycket lägre utsläpp än elektrolys med kolkraft.
- **Utvinning av bauxit** och framställning av aluminiumoxid påverkar mark och ger restprodukter som måste tas om hand.
- **Återvinning räcker inte ensam**. Mycket aluminium sitter i produkter som används i årtionden, så en stor del av efterfrågan måste fortfarande mötas med ny metall.
- **Olika legeringar blandas** vid insamling, vilket kan försämra kvaliteten.

Ett lätt material kan också spara energi under användningen, till exempel i fordon. Därför behöver helheten vägas ihop, vilket du gör med livscykelanalys i [kapitel 9](09-livscykelanalys-och-varden.md).

## Plast

Plast är ett samlingsnamn för väldigt olika material. Egenskaperna varierar från mjuk påsplast till glasfiberarmerad plast som tål mekanisk belastning i maskiner. Ett generellt påstående om "plastens hållfasthet" säger därför nästan ingenting. Du måste veta vilken plast det gäller.

**Termoplaster** kan smältas om, som PLA och PETG som ofta används i 3D-skrivare. **Härdplaster** har tvärbindningar och kan inte smältas om, som epoxi.

Tre ord blandas ofta ihop:

| Begrepp | Betydelse |
|---|---|
| Biobaserad | Tillverkad helt eller delvis av biologiska råvaror i stället för fossila |
| Biologiskt nedbrytbar | Kan brytas ned av mikroorganismer under vissa förhållanden |
| Komposterbar | Biologiskt nedbrytbar i kompostering, ofta bara i industriell anläggning |

[EU-kommissionen](https://environment.ec.europa.eu/topics/plastics/biobased-biodegradable-and-compostable-plastics_en) slår fast att biobaserad plast inte nödvändigtvis är biologiskt nedbrytbar eller komposterbar. Biobaserad polyeten är ett exempel: råvaran kommer från växter, men materialet bryts inte ned snabbare än vanlig polyeten. Omvänt kan fossil plast vara nedbrytbar. Dessutom bryts inte en "nedbrytbar" plast nödvändigtvis ned i naturen, och märkningen kan leda till nedskräpning. Läs mer hos [Naturvårdsverket](https://www.naturvardsverket.se/amnesomraden/plast/).

## Textil

Textil är fibrer som spunnits till garn och sedan vävts, stickats eller pressats samman. **Naturfibrer** är till exempel bomull och ull. **Syntetfibrer** är till exempel polyester och polyamid.

Textil är inte bara kläder. **Tekniska textilier** används till krockkuddar, filter, skyddskläder, geotextil under vägar och som fiberförstärkning i kompositer. Fiberns riktning avgör styrkan, precis som i trä.

[Naturvårdsverket](https://www.naturvardsverket.se/amnesomraden/textil/) framhåller att sättet textilen tillverkas på betyder mycket för miljöpåverkan, och att det viktigaste du kan göra är att använda textilier längre.

## Grafen

**Grafen** är ett lager kol som bara är en atom tjockt, med atomerna i ett sexkantigt mönster. Forskningen på materialet belönades med [Nobelpriset i fysik 2010](https://www.nobelprize.org/prizes/physics/2010/summary/). I laboratorier har det visat mycket hög hållfasthet och god ledningsförmåga för el och värme.

Grafen har stor potential, men det är viktigt att skilja på vad som visats i laboratoriet och vad som går att köpa. Vissa tillämpningar, framför allt som tillsats i kompositer, bläck och beläggningar, finns redan kommersiellt. Många andra användningar, till exempel inom elektronik och medicin, är fortfarande på forskningsstadiet. Hindren handlar bland annat om att tillverka materialet i stor skala med jämn kvalitet. [Graphene Flagship](https://www.graphene-flagship.eu/), ett europeiskt forskningsinitiativ, följer utvecklingen.

## Analysera och samtala om konstruktioner

En konstruktion finns för att uppfylla ett **behov**. När du analyserar den kan du gå från behovet och framåt:

1. Vilket behov ska den uppfylla, och för vem?
2. Vilka funktioner krävs?
3. Vilka belastningar och miljöer utsätts den för?
4. Vilket material och vilken form har valts, och varför?
5. Vad kostar valet i pengar, energi och miljöpåverkan?
6. Vem får det lättare eller svårare av lösningen?

**Exempel: en mobilhållare i trä.** Behovet är att se skärmen utan att hålla i mobilen. Funktionen kräver en stabil vinkel och en fot som inte tippar. Belastningen är liten, men en tunn tapp utsätts för krafter som kan klyva den längs fibrerna. Materialet är billigt och går att laserskära, men tål fukt dåligt. Den som har små händer eller använder en stor mobil kan behöva andra mått. Genom att gå igenom punkterna på det här sättet får du ett samtal om konstruktionen som bygger på skäl, inte bara på tycke och smak.

## Begrepp

- **Hållfasthet:** hur stor spänning materialet tål.
- **Styvhet:** hur lite materialet deformeras under last.
- **Spänning:** kraft per area, oftast i MPa.
- **Specifik hållfasthet:** hållfasthet per densitet.
- **Anisotropt:** egenskaperna beror på riktning.
- **Legering:** metall med tillsatser som ger andra egenskaper.

## Testa dig själv

1. Varför är det fel att säga att trä generellt tål tryck dåligt?
2. Varför kan samma material vara rätt i ett fall och fel i ett annat?
3. Vad är det som gör aluminiumlegeringar så mycket starkare än ren aluminium?
4. Vad väger man in om man ska bedöma aluminiumets miljöpåverkan?
5. Varför säger "plast" i sig lite om hållfastheten?
6. Vad är skillnaden mellan biobaserad och biologiskt nedbrytbar?
7. Varför bör du vara försiktig med påståenden om vad grafen kommer att göra?

## Övningar

**Grund.** En felfri träkloss med tvärsnittet 30 × 30 mm trycks längs fibrerna. Hur stor kraft tål den ungefär, med 50 MPa?

<details><summary>Svar</summary>

A = 900 mm². F = 50 · 900 = 45 000 N = 45 kN.

</details>

**Grund.** Du återvinner 10 kg aluminium i stället för att framställa ny metall. Hur mycket energi sparas, med genomsnittsvärdena ovan? Ange svaret i MJ och kWh (1 kWh = 3,6 MJ).

<details><summary>Svar</summary>

Primär: 10 kg · 186 MJ/kg = 1 860 MJ. Återvunnen: 10 · 8,3 = 83 MJ. Besparing: 1 777 MJ, vilket är 1 777 / 3,6 ≈ 494 kWh. (186 GJ/ton är samma sak som 186 MJ/kg.)

</details>

**Vidare.** Välj två av materialen i kapitlet till ett skyddshölje för en sensor som ska sitta utomhus. Motivera med hållfasthet, fukt och miljö.

**Utmaning.** Analysera en konstruktion du använder varje dag med de sex frågorna. Föreslå en förändring som gör den bättre för någon som i dag får det svårare med produkten.

## Koppling till projektet

I [Laserskär](../projekt/laserskar/README.md) ska du konstruera i tunt trä, och fibrernas riktning avgör om tappar och smala delar håller. I [Robotmopp](../projekt/robotmopp/README.md) väljer du material till chassit, och i [MikroGrid](../projekt/mikrogrid/README.md) återkommer aluminium, kisel och batterimetaller i livscykelanalysen.

## Läs mer

- [Träguiden](https://www.traguiden.se/), om trä som konstruktionsmaterial
- [Svenskt Trä](https://www.svenskttra.se/)
- Källorna till siffrorna finns länkade i texten.

[← Föregående](01-teknikutveckling-och-projekt.md) | [Innehåll](../README.md) | [Nästa →](03-cad-och-laserskarning.md)
