# Projekt: MikroGrid

Från solstråle till lagrad energi och livscykelanalys.

## Syfte

Du utvecklar förståelse för fotovoltaik, energilagring och kraftelektronik, både teoretiskt och praktiskt. Genom att konstruera och testa en prototyp av ett småskaligt energisystem, ett mikronät för off-grid-bruk, tränar du på att tillämpa tekniska modeller, dimensionera kretsar och göra mätningar. Projektet belyser också samspelet mellan teknik, människa och miljö genom en kritisk livscykelanalys av solpaneler och batterier, från råvaror som kisel, litium och kobolt till återvinning och cirkulära flöden.

## Koppling till kursen

**Kriterier i vanliga ord.** Du visar att du kan arbeta dig genom teknikutvecklingsprocessen, lösa tekniska problem, göra beräkningar och rimlighetsbedömningar, värdera lösningar utifrån hållbarhet samt dokumentera och presentera din lösning.

**Centralt innehåll.** Tillämpning av teknikutvecklingsprocessen, problemlösning, systematiskt kvalitetsarbete och riskanalys, beräkning och dimensionering, modellering, framtidens teknik och hållbar utveckling, värdering utifrån genus, etik och hållbarhet samt kommunikation och dokumentation.

**Kapitel som förbereder.**

- [Kapitel 4: Elektronik som styr och reglerar](../../kapitel/04-elektronik.md)
- [Kapitel 6: Mätning, kvalitet, risk och arbetsmiljö](../../kapitel/06-kvalitet-och-risk.md)
- [Kapitel 8: Solceller, batterier och dimensionering](../../kapitel/08-solenergi-och-batterier.md)
- [Kapitel 9: Livscykelanalys, hållbarhet och etik](../../kapitel/09-livscykelanalys-och-varden.md)
- [Kapitel 10: Entreprenörskap och teknisk kommunikation](../../kapitel/10-entreprenorskap-och-kommunikation.md)

## Vad du ska göra

Ni arbetar i grupper om 2–3 och utvecklar ett fungerande mikrosystem, till exempel autonom belysning, en sensorstation eller en nödladdningsenhet. Ni dimensionerar energibehovet i förhållande till solinstrålning och batterikapacitet, kopplar ihop CN3065-laddaren med en 18650 Li-ion-cell eller LiPo-ackumulator och integrerar en belastning, och eventuellt en enkel mikrokontroller eller LED-krets.

## Krav och leverabler

- **Fysisk prototyp:** en fungerande, kapslad miniatyrmodell av ett off-grid energisystem som integrerar 6 V/1,25 W-solpanelen, CN3065-laddaren, batteriet och en definierad last, till exempel USB-uttag eller sensornod.
- **Teknisk rapport och analys:** kretsschema, mätdata med effektkurvor och laddningstid, dimensioneringsberäkningar samt en fördjupad livscykel- och hållbarhetsanalys som kritiskt granskar teknikens miljöpåverkan och återvinningsbarhet.
- Avslutande presentation på en teknisk mässa, där prototyperna demonstreras i drift.

## Arbetsgång

Det finns ingen färdig lektionsplan med lektioner för projektet. Projektet är uppdelat i faser, och läraren anger hur de fördelas på lektionerna. Planerad tid är 30 timmar.

| Fas | Innehåll |
|---|---|
| 1. Teori, halvledarfysik och systemförståelse | Den fotovoltaiska effekten i monokristallint kisel, laddningsreglering med CN3065 och batterikemi för litiumceller. Grundläggande mätningar på solpanelen under olika ljusförhållanden och vinklar för att plotta IV-kurvor och beräkna verkningsgrad. |
| 2. Dimensionering, design och kretsbygge | Grupper om 2–3 tar fram ett mikrosystem, dimensionerar energibehovet och kopplar ihop laddaren, batteriet och lasten. |
| 3. Systemtest, verifiering och datainsamling | Kvalitetssäkring och mätning under kontrollerade belastningscykler: spänningsfall, laddströmmar och drifttid. Analys av tillförlitlighet och energiförluster samt en enkel riskanalys för batterihantering. |
| 4. Livscykelanalys och hållbarhetsvärdering | Teknisk och etisk analys av värdekedjan: råvaruutvinning, energikrävande smältprocesser för kisel, geopolitiska och sociala aspekter kring batterimetaller samt mekanisk och hydrometallurgisk återvinning. |
| 5. Dokumentation och presentation | Teknisk rapport med kretsschema, beräkningar och mätdiagram. Avslutande presentation på en teknisk mässa. |

## Bedömning

Bedömningen sker löpande och utifrån den tekniska rapporten och prototypen.

| Område | E | C | A |
|---|---|---|---|
| **Tekniska processer, problemlösning och dimensionering** | Genomför kretskopplingen och mätningarna med handledning, följer instruktioner för CN3065-modulen och gör enkla, rimliga beräkningar på systemets effekt. | Dimensionerar självständigt systemet, utför korrekta mätningar på solcellens och batteriets prestanda samt felsöker och optimerar kretsen vid behov. | Genomför avancerade dimensioneringsberäkningar, analyserar verkningsgrad och energiförluster systematiskt samt modifierar och optimerar konstruktionen med stor teknisk precision. |
| **Teknik, människa, samhälle och hållbarhet** | Beskriver översiktligt hur solenergisystem och batterier tillverkas samt nämner grundläggande miljö- och återvinningsaspekter. | Analyserar och resonerar kring råvaruutvinningens påverkan, energianvändning vid tillverkning och hur återvinning kan ske i ett livscykelperspektiv. | Gör en nyanserad, kritisk och djupgående värdering av solenergiteknikens hållbarhet. Väger miljövinster mot ekologiska och etiska utmaningar vid råvaruproduktion och föreslår relevanta cirkulära lösningar. |
| **Teknisk kommunikation och dokumentation** | Upprättar en grundläggande dokumentation med enkla skisser eller scheman och förklarar systemets funktion med vardagligt och visst tekniskt språk. | Presenterar en välstrukturerad rapport med korrekta tekniska kretsscheman och relevant fackspråk. | Rapporten håller hög teknisk kvalitet med professionella kretsscheman, tydlig visualisering av mätdata samt ett stringent och korrekt vetenskapligt och tekniskt språk. |

## Material

- Solpanel 6 V, 210 mA, monokristallin, med integrerad CN3065-laddare.
- Li-ion 18650-batterier eller 3,7 V LiPo-celler med inbyggt skyddskort, batterihållare, multimetrar, laboratorieaggregat, kablar och kopplingsdäck, strömbrytare och belastningar som motstånd, 5 V step-up-moduler, lysdioder eller små mikrokontroller.
- Halogenlampor eller starka LED-byggstrålkastare för att simulera solljus vid dåligt väder, samt luxmätare.
- Läs de källor som anges i [kapitel 8](../../kapitel/08-solenergi-och-batterier.md) och [kapitel 9](../../kapitel/09-livscykelanalys-och-varden.md).

## Tips

- **Säkerhet först.** Läraren går igenom brandsäkerhet och kortslutningsrisker vid arbete med litiumbatterier. Följ den genomgången, använd skyddsutrustningen och koppla aldrig utan att kontrollera polariteten.
- Dimensionera innan du bygger och skriv ut dina antaganden.
- Minska förbrukningen innan du ökar panelen.
- Använd en luxmätare med försiktighet, eftersom omräkningen till W/m² beror på ljuskällan. Redovisa hur du gjort.
- Mät och spara mätdata löpande, och notera ljusförhållanden och panelens vinkel.
