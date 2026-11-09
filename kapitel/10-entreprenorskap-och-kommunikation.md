# Kapitel 10: Entreprenörskap och teknisk kommunikation

> **I det här kapitlet lär du dig**
> - vad entreprenörskap innebär i ett tekniskt projekt
> - hur du beskriver en idé som en affärsmodell och räknar på den
> - hur du skriver en teknisk rapport som någon annan kan kontrollera
> - hur du visualiserar data och presenterar en lösning

En lösning som bara fungerar på din bänk förändrar ingenting. Någon måste förstå den, tro på den och vilja använda eller betala för den. Därför är förmågan att omsätta idéer till handling och att kommunicera teknik lika viktig som själva konstruktionen. I det här kapitlet samlar du ihop det du gjort i kursens projekt.

## Entreprenörskap

**Entreprenörskap** är att upptäcka en möjlighet och göra något av den. Det gäller inte bara den som startar ett företag. En person som startar en förening, förbättrar en rutin på jobbet eller bygger ett verktyg som andra får glädje av agerar också entreprenöriellt.

### Innovation

**Innovation** är en ny lösning som faktiskt börjar användas. En uppfinning som ligger i en låda är inte en innovation. Innovation kan vara en ny produkt, en ny process, en ny tjänst eller ett nytt sätt att ta betalt.

### Villkoren

Entreprenörskapets villkor avgör vad som går att genomföra:

| Villkor | Frågor |
|---|---|
| Marknad | Vem har behovet, hur många är de och vilka alternativ finns? |
| Kapital | Vad kostar det att komma igång, och var kommer pengarna från? |
| Regler | Vilka krav gäller, till exempel på produktsäkerhet och dataskydd? |
| Kompetens | Vad kan vi själva och vad behöver vi hjälp med? |
| Risk | Vad händer om det inte fungerar? |
| Tillgänglighet | Vilka har möjlighet att bli entreprenörer, och vilka hindras? |

På [Verksamt](https://www.verksamt.se/), en webbplats från svenska myndigheter, finns information om att starta och driva företag.

### Affärsmodell

En **affärsmodell** beskriver hur en verksamhet skapar värde och tar betalt. Ställ till exempel de här frågorna:

- **Vem** är kunden?
- **Vilket problem** löser vi?
- **Hur** når vi kunden?
- **Vad** betalar kunden för, och hur ofta?
- **Vilka kostnader** har vi?

Ett av de vanligaste misstagen är att bygga något innan man har pratat med dem som ska använda det. Gör därför tidiga och enkla tester av idén, till exempel med en skiss, en prototyp eller en enkät.

### Genomräknat exempel: nollpunkt

Du vill sälja färdiga solcellsstationer till föreningar. Fasta kostnader är 30 000 kr per år. Varje station säljs för 500 kr och de rörliga kostnaderna är 200 kr per styck.

Varje såld station bidrar med 500 − 200 = 300 kr. Antalet som behövs för att täcka de fasta kostnaderna, **nollpunkten**, är

30 000 / 300 = 100 stationer.

Säljer du 120 stationer blir vinsten 120 · 300 − 30 000 = 6 000 kr. Beräkningen är enkel, men den visar snabbt om idén är rimlig. Klarar du verkligen att sälja 100 stationer om året? Kostnaden för garanti och återtagning av gamla batterier behöver också räknas med.

## Teknisk kommunikation

God **teknisk kommunikation** gör att en annan person kan förstå vad du gjort, kontrollera det och bygga vidare.

### Teknisk rapport

| Avsnitt | Innehåll |
|---|---|
| Sammanfattning | Syfte, metod och viktigaste resultat, kort |
| Bakgrund och syfte | Varför arbetet gjordes, krav och avgränsningar |
| Metod | Hur du gjorde, tillräckligt detaljerat för att gå att upprepa |
| Konstruktion | Ritningar, scheman och beräkningar |
| Resultat | Mätvärden, tabeller och diagram, utan tolkning |
| Diskussion | Vad resultaten betyder, felkällor, rimlighet |
| Slutsats | Vad som uppfylldes av kraven och vad du skulle göra annorlunda |
| Referenser | Källor som går att hitta |

Språket ska vara sakligt, och begrepp ska användas på samma sätt genom hela texten. Skriv till exempel "motordrivaren" hela tiden och inte omväxlande "styrkretsen" och "driverkortet". Blanda inte in resultat i metoden och tolkningar i resultaten. Hitta aldrig på mätvärden, och redovisa även sådant som inte fungerade.

### Scheman och ritningar

Ett **kretsschema** visar hur komponenter är kopplade, med standardiserade symboler och namn. Det ska gå att läsa utan att titta på det fysiska bygget. **Digitala ritningar och modeller** ska ha mått, enheter och version, så att det går att tolka dem och tillverka efter dem, och du ska kunna motivera dina mått. Läs mer i [kapitel 3](03-cad-och-laserskarning.md).

### Diagram

Ett diagram ska kunna förstås på egen hand:

- Ange titel, axlar, storhet och enhet.
- Välj diagramtyp efter frågan: linje för förändring över tid, spridning för samband, stapel för jämförelse.
- Skriv ut enheter, använd rimligt antal decimaler och var ärlig med axlarnas skala.

### Dokumentation

Bra dokumentation sker löpande. I ett kodprojekt är **versionshantering** till exempel Git ett sätt att spara ändringar och visa vad som ändrats när. En tydlig README förklarar vad projektet är och hur man startar det. Lägg aldrig lösenord, nycklar eller inloggningsuppgifter i publika filer.

### Muntlig presentation och mässa

På en **teknisk mässa** visar du en fungerande prototyp och pratar med besökare. Förbered dig så här:

1. **En mening** som säger vad lösningen gör och för vem.
2. **Det viktigaste resultatet**, med mätvärden.
3. **En demonstration** som fungerar, och en reservplan om den inte gör det.
4. **Det som inte fungerade** och vad du lärde dig.
5. **Svar på kritiska frågor** om säkerhet, kostnad och hållbarhet.

Anpassa språket efter lyssnaren. En klasskamrat, en elingenjör och en kund behöver olika detaljer. Det är lätt att säga för mycket, så låt prototypen och siffrorna tala.

## Begrepp

- **Entreprenörskap:** att omsätta idéer till handling.
- **Innovation:** ny lösning som börjar användas.
- **Affärsmodell:** hur en verksamhet skapar värde och tar betalt.
- **Fasta kostnader:** kostnader som inte beror på antal sålda enheter.
- **Rörliga kostnader:** kostnader som ökar med antalet enheter.
- **Nollpunkt:** antal sålda enheter då intäkter och kostnader är lika stora.
- **Kretsschema:** ritning över elektriska kopplingar.
- **Versionshantering:** verktyg för att spara och följa ändringar.

## Koppling till projektet

Kapitlet används i slutet av varje projekt. I [MikroGrid](../projekt/mikrogrid/README.md) sammanställer du en teknisk rapport och visar prototypen på en teknisk mässa. I [Robotmopp](../projekt/robotmopp/README.md) visar du en demo på robotbanan. I [Laserskär](../projekt/laserskar/README.md) dokumenterar du konstruktionen, och i [Databaser och mobil apputveckling](../projekt/databaser-och-mobilapp/README.md) visar du designen och appen.

## Läs mer

- [Verksamt](https://www.verksamt.se/)
- [Ellen MacArthur Foundation om cirkulära affärsmodeller](https://www.ellenmacarthurfoundation.org/topics/circular-economy-introduction/overview)

[← Föregående](09-livscykelanalys-och-varden.md) | [Innehåll](../README.md)
