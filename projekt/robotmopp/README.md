# Projekt: Robotmopp

Driverbot 2.0: en ESP8266-bil som styrs från ROS2 och städar en arena.

## Syfte

Du bygger en robotmopp. Din ESP8266-bil styrs från ROS2 på datorn via en MQTT-brygga. Uppdraget är att täcka en arena på 2 × 2 m med en whiteboardpenna under bilen. Arenan delas in i ett rutnät med 8 × 8 rutor på 25 cm, så att du kan mäta hur stor del av ytan bilen har städat.

Du använder simuleringen från sköldpaddeprojektet, gör en tydlig projektplan med komponenter, ritar chassit i CAD och sätter ihop roboten.

## Koppling till kursen

**Kriterier i vanliga ord.** Du visar att du kan arbeta systematiskt från plan till CAD och färdig bil, lösa problem både i simulering och i verkligheten, använda begrepp och modeller med rimlighetsbedömningar, mäta och utvärdera resultat, och dokumentera och presentera din lösning.

**Centralt innehåll.** Tillämpning av teknikutvecklingsprocessen, problemlösning, metodik i projekt, tillämpning av programmering, systematiskt kvalitetsarbete och riskanalys, modellering och simulering, digitaliseringens betydelse, kommunikation och dokumentation, samt digitala ritningar och modeller.

**Kapitel som förbereder.**

- [Kapitel 1: Teknikutveckling och projektarbete](../../kapitel/01-teknikutveckling-och-projekt.md)
- [Kapitel 3: Digitala ritningar, CAD och laserskärning](../../kapitel/03-cad-och-laserskarning.md)
- [Kapitel 4: Elektronik som styr och reglerar](../../kapitel/04-elektronik.md)
- [Kapitel 5: Modeller, simulering och programmering](../../kapitel/05-modeller-och-programmering.md)
- [Kapitel 6: Mätning, kvalitet, risk och arbetsmiljö](../../kapitel/06-kvalitet-och-risk.md)

## Vad du ska göra

- Gör en projektplan med komponentlista, bland annat ultraljudssensor HC-SR04 och ljussensor.
- Rita ett chassi i CAD med fästen för penna och sensorer, och sätt ihop bilen.
- Testa städprogrammet i simulering (labb 8), koppla bilen till ROS2 (labb 9) och kör autonomt (labb 10).

| Nivå | Vad bilen ska klara |
|---|---|
| Nivå 1 | Du styr bilen manuellt från ROS2 och berör alla 64 rutor. |
| Nivå 2 | Hinderstopp och autonom slumpstädning med mätt täckning. |
| Nivå 3 | Spiral eller "undvik ritat" med ljussensorn, jämfört med slump. |

**MQTT.** Du använder den broker som läraren anger. Adress och eventuell inloggning får du av läraren. Lägg aldrig in lösenord, nycklar eller inloggningsuppgifter i ditt repo.

## Krav och leverabler

- Projektplan med komponentlista.
- CAD-modell av chassit, kontrollerad mot komponentlistan.
- Färdig bil med monterad penna och sensorer.
- Resultat från labbarna och mätprotokoll från arenan.
- Demo på robotbanan.

## Arbetsgång

| Lektion | Innehåll |
|---|---|
| 1 | Projektstart: genomgång av Driverbot 2.0 och robotmoppen (arena, rutnät, nivå 1–3). Bli klar med turtlesim-labbarna till och med labb 7. |
| 2 | Projektplan: gör komponentlista (ESP8266, motor, servo, HC-SR04, ljussensor, penna) och skissa chassit. |
| 3 | CAD: börja modellera chassit med plats för motor, servo och ESP8266. |
| 4 | CAD fortsättning: fästen för whiteboardpenna, ultraljudssensor och ljussensor. Kontrollera måtten mot komponentlistan. |
| 5 | Labb 8 del 1–2: täckningsmätarnoden (8×8 rutnät) och manuell städning med teleop i turtlesim. |
| 6 | Labb 8 del 3–4: autonom städare med tillståndsmaskinen KOR_FRAMAT/BACKA_SVANG och launch-fil. Jämför manuell och autonom täckning. |
| 7 | Labb 9 del 1–2: ladda upp ny firmware på ESP8266 och testa bilen via MQTT utan ROS2. |
| 8 | Labb 9 del 3–4: bryggnoden ROS2–MQTT. Kör bilen med teleop och läs av ultraljudssensorn i ROS2. |
| 9 | Sätt ihop robotmoppen: montera chassit, pennan och sensorerna på bilen och testkör. |
| 10 | Nivå 1 på arenan: kalibrera bilen, styr manuellt från ROS2 och försök beröra alla 64 rutor. Börja på hinderstoppet i labb 10. |
| 11 | Labb 10: hinderstopp, hinder-undvikare och autonom slumpstädning på arenan. Mät täckningen i rutnätet (nivå 2). |
| 12 | Nivå 3: spiral eller "undvik ritat" med ljussensorn, jämför med slump. Trimma och dokumentera resultaten inför demon. |
| 13 | Övergång till nästa projekt: starta Databaser och mobil apputveckling, installera PocketBase och designa databasen för förstudieprojektet. |

Projektet är planerat till 30 timmar.

## Bedömning

Du bedöms på hur väl du använder ROS2 och verktygen, hur systematiskt du utvecklar och testar lösningen, hur du följer konstruktionsprocessen från plan till CAD och färdig bil, och hur du dokumenterar, presenterar och utvärderar resultatet. Projektet avslutas med demo på robotbanan.

## Material

- [ROS2-repot med alla labbar](https://github.com/abbjetmus/ROS2)
- [Labb 8: Robotmopp i simulering](https://github.com/abbjetmus/ROS2/blob/main/labs/labb-8-robotmopp-simulering.md)
- [Labb 9: Koppla bilen](https://github.com/abbjetmus/ROS2/blob/main/labs/labb-9-koppla-bilen.md)
- [Labb 10: Autonom bil](https://github.com/abbjetmus/ROS2/blob/main/labs/labb-10-autonom-bil.md)
- [Från turtlesim till riktig bil](https://github.com/abbjetmus/ROS2/blob/main/fran-turtlesim-till-riktig-bil.md)

I ROS2-repot finns också en presentation om Driverbot 2.0. Labbarna innehåller exempel på adresser och namn. Använd alltid de uppgifter som läraren anger.

## Tips

- Testa alltid i simulering först. En bugg där kostar en omstart.
- Testa firmware utan ROS2 med bilen på en låda, så att hjulen snurrar fritt.
- Fäst pennan med lite fjädring så att den följer golvet.
- Ändra en parameter i taget och skriv upp resultatet.
- Kontrollera hur HC-SR04 ska kopplas till ESP8266 med din matningsspänning, se [kapitel 4](../../kapitel/04-elektronik.md).
- Lägg märke till skillnaden mellan simulering och verklighet. Den skillnaden är en stor del av lärdomen i projektet.
