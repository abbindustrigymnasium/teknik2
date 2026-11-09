# Projekt: Databaser och mobil apputveckling

En backend i PocketBase och en mobilapp i Flutter.

## Syfte

Nästan alla appar du använder sparar data någonstans: inlägg, användare och gillningar. I det här projektet lär du dig hur en databas fungerar och designas, hur du bygger en backend i PocketBase och hur du gör en mobilapp i Flutter som pratar med den. Hela vägen följer vi samma exempel, Kvittra, en enkel social app där man skriver inlägg, kommenterar, gillar och följer varandra.

## Koppling till kursen

**Kriterier i vanliga ord.** Du visar att du kan lösa ett tekniskt problem med programmering, använda begrepp och modeller inom databaser och appar, dokumentera en design och värdera hur digitala lösningar påverkar människor, till exempel genom vilka data som samlas in.

**Centralt innehåll.** Tillämpning av programmering för problemlösning, problemlösning inom informationsteknik, metodik i projekt, digitaliseringens betydelse för produktion, kommunikation och människans livsmiljö samt kommunikation och dokumentation.

**Kapitel som förbereder.**

- [Kapitel 1: Teknikutveckling och projektarbete](../../kapitel/01-teknikutveckling-och-projekt.md)
- [Kapitel 6: Mätning, kvalitet, risk och arbetsmiljö](../../kapitel/06-kvalitet-och-risk.md)
- [Kapitel 7: Databaser, appar och digitalisering](../../kapitel/07-databaser-och-digitalisering.md)

## Vad du ska göra

- Installera PocketBase och lär dig databasdesign med tabeller, fält och relationer.
- Designa databasen för ert eget projekt från förstudien.
- Bygg Kvittra i PocketBase, lägg in data, skriv SQL-frågor och sätt API-regler för inloggning.
- Lär dig Dart och Flutter: widgets, layout, state och navigation.
- Använd flutter_compositions och koppla appen till PocketBase.
- Bygg klart Kvittra-appen med inloggning, flöde, inlägg, kommentarer och likes.

## Krav och leverabler

- Databasdesign för ert eget projekt.
- Övningarna i varje modul.
- Färdig Kvittra-app som fungerar mot din PocketBase-backend.

## Arbetsgång

| Lektion | Innehåll |
|---|---|
| 1 | PocketBase |
| 2 | Flutter och Dart: introduktion |
| 3 | Installera Flutter och grunder |
| 4 | Mera Flutter |
| 5 | Introduktion till Flutter Compositions |
| 6 | Koppla Flutter till PocketBase |
| 7–8 | Bygga klart appen Kvittra |
| 9–20 | Innehållet är inte fastställt i lektionsplanen. Läraren anger hur tiden används, utifrån punkterna under "Vad du ska göra". |

I [Robotmopp](../robotmopp/README.md) har sista lektionen redan startat det här projektet, med installation av PocketBase och design av förstudieprojektets databas.

## Bedömning

Läraren följer ditt arbete under lektionerna. Det du visar är din databasdesign, dina övningar i varje modul och den färdiga Kvittra-appen som fungerar mot din PocketBase-backend.

## Material

- [Kursrepo på GitHub](https://github.com/abbjetmus/pocketbase-flutter-kurs)
- [Modul 01: Databaser och PocketBase](https://github.com/abbjetmus/pocketbase-flutter-kurs/tree/main/01-databaser-och-pocketbase)
- [Modul 02: Flutter](https://github.com/abbjetmus/pocketbase-flutter-kurs/tree/main/02-flutter)
- [Modul 03: Flutter Compositions](https://github.com/abbjetmus/pocketbase-flutter-kurs/tree/main/03-flutter-compositions)
- [Sammanfattning (pptx)](https://github.com/abbjetmus/pocketbase-flutter-kurs/blob/main/Databaser%20och%20mobilapputveckling%20-%20sammanfattning.pptx)
- [PocketBase dokumentation](https://pocketbase.io/docs/)
- [Flutter dokumentation](https://docs.flutter.dev/)

## Tips

- Rita databasen på papper innan du bygger den.
- Testa dina API-regler genom att försöka göra något som inte ska vara tillåtet. Kom ihåg att en tom regel ger åtkomst för alla.
- Lägg aldrig in lösenord eller hemliga nycklar i kod som hamnar i ett publikt repo.
- Samla bara in de personuppgifter du behöver.
- Gör en liten sak färdig åt gången och provkör ofta.
