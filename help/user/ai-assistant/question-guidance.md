---
title: Richtlijnen voor vragen aan AI-assistent
description: Plaatsaanduiding
feature: AI Assistant
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: f09f3f5b7d4419ead5308e4c5be3b518b4e16ff5
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Vraag-advies voor AI Assistant in Journey Optimizer B2B edition

Bekijk de volgende set voorbeeldvragen voor het opvragen van AI Assistant in Journey Optimizer B2B edition. Deze informatie bevat ook tips voor het formuleren van vragen om optimale antwoorden te krijgen van AI Assistant.

## Op doelstellingen gebaseerde vragen

De volgende voorbeeldvragen worden gegroepeerd op doelstellingen die u kunt verwezenlijken wanneer het gebruiken van AI Medewerker:

| Doelstelling | Beschrijving | Voorbeeld |
| --- | --- | --- |
| Leerconcepten en doorlopende workflows | Als beginnende gebruiker, kunt u AI Medewerker gebruiken om de concepten van Real-Time CDP en van Adobe Journey Optimizer B2B edition te leren, en aan boord aan producten en eigenschappen die u niet vertrouwd met bent. <br> als ervaren gebruiker, kunt u AI Medewerker gebruiken om een randgeval op te lossen dat uw werkschema kan blokkeren. | <li>Vertel me wat gebruiksgevallen voor Real-Time CDP. <li>Verklaar het concept van de Groep van de Kopieer aan me. |
| Problemen oplossen | Met AI Assistant leert u hoe u fouten in de basisbeginselen die u in uw workflow tegenkomt, kunt opsporen. | <li>Wat betekent deze fout &lt;ERROR_MESSAGE>? <li>Waarom kan ik het publiek met de naam &quot;...&quot; niet verwijderen? |
| Zandbakhygiëne | Met AI Assistant kunt u eventuele duplicaten of ongebruikte objecten identificeren, zodat u de sandbox op efficiënte wijze kunt onderhouden. | <li>Kun je me een vergelijkbaar publiek laten zien? <li>Zijn er regelingen die geen bijbehorende dataset hebben? |
| Waardeanalyse | Met AI Assistant kunt u de meest gebruikte gegevensobjecten identificeren en prestatie-indicatoren beoordelen of de meest waardevolle gegevensobjecten vinden. | <li>Hoeveel rekeningen zijn in onze &quot;...&quot;segmentdefinitie? <li>Wanneer is het publiek geactiveerd naar de bestemming Experience Cloud Audiences? |
| Zoeken | De Medewerker van AI van het gebruik om gesteunde voorwerpen van Experience Platform en Adobe Journey Optimizer B2B edition, zoals rekeningspubliek, datasets, bestemmingen, schema&#39;s, bronnen, rekeningsreizen, het kopen groepsmalplaatjes, en oplossingsbelangen te vinden | <li>Geef een lijst weer van de soorten publiek met &quot;Luma&quot; in de naam die zijn gebruikt voor reizen naar de account. <li>Welke kenmerken bevinden zich in het XDM-schema &quot;Luma: Custom Actions&quot;? |
| Effectanalyse | Met AI Assistant kunt u gegevensobjecten identificeren die in bepaalde workflows zijn gebruikt, zodat u het effect van wijzigingen kunt beoordelen. | <li>Welk accountpubliek gebruikt `workEmail.address` in het schema &quot;B2B-persoon&quot;? <li>In welke gegevenssets is ... `jobTitle` opgeslagen? |

## Uw vragen formuleren

U moet uw vragen duidelijk en in de juiste context stellen aan AI Assistant om een zo accuraat mogelijk antwoord te krijgen. Raadpleeg de volgende tips voor het stellen van een duidelijke vraag met betrekking tot de context:

* Geef uw taak en/of vraag beknopt weer.
* Vermijd dubbelzinnige taal of te complexe syntaxis om het begrip te vergemakkelijken.
* Een relevante context bieden met betrekking tot uw taak en/of vraag als context kan AI Assistant helpen meer relevante reacties te genereren.

In de volgende tabellen vindt u een aantal aanbevolen procedures die u kunt volgen bij het gebruik van AI Assistant:

| Do | Voorbeeld |
| --- | --- |
| <li>Wees specifiek voor het object of de informatie die u wilt ophalen of analyseren. <li>Plaats uw gegevensobjectnamen tussen aanhalingstekens. <li>Als u slechts een deel van de objecten naam kent, kunt u dat ook specificeren in de vraag. | <li>Welke datasets gebruiken het &quot;B2B- Rekening&quot;schema? <li>Toon me het geactiveerde publiek dat &quot;Rekening&quot;in hun naam heeft. Rank ze op aantal leden. |
| <li>Vermijd dubbelzinnigheid en gebruik duidelijke taal. <li>Gebruik nauwkeurige terminologie om betere duidelijkheid in uw vraag te verzekeren. <li>Wanneer u vragen stelt over Adobe Experience Platform en Adobe Journey Optimizer B2B edition, probeert u specifieke terminologie voor Experience Platform of Adobe Journey Optimizer B2B edition te gebruiken om de relevantie van antwoorden te verbeteren. | <li>Hoeveel leden heb ik in &quot;Mijn accountpubliek&quot;? <li>Hoeveel accountreizen gebruiken Accountpubliek &quot;Mijn accountpubliek&quot;? |
| <li>Geef context op of geef criteria op om de resultaten te filteren. <li>Gebruik filtercriteria in de vragen om het volume van gegevens in de reactie te beperken. | <li>Toon mij accountpubliek dat nog niet is geactiveerd en meer dan zes maanden geleden is gemaakt en dat nog nooit is gewijzigd. <li>Stuur mij een accountreis dat in de afgelopen 7 dagen is gepubliceerd en gebruikt een accountpubliek dat meer dan 1000 leden heeft |

| Niet doen | Voorbeeld |
| --- | --- |
| Gebruik een vage of dubbelzinnige taal. | <li>Geef me informatie over datasets. <li>Wat doet reis x? <li>Hoeveel gebruikers heb ik in &quot;ACME Audience&quot;? <li>Segmenten tonen. <li>Lijstkenmerken. |
| Voer onvolledige verzoeken in. | <li>&quot;Luma - Loyalty Dataset&quot; |
| Kennis aannemen zonder context. | <li>Soorten publiek in de laatste zes maanden. <li>Bouw een vraag voor me. <li>Een reis voor mij maken |
| U kunt te complexe query&#39;s opmaken. | <li>Verstrek een uitvoerige analyse van gegevenslijn over alle voorwerpen en hun gebiedsdelen. |
| Criteria of parameters weglaten. | <li>Toon me gegevenssets. |

## Voorbeelden van niet-ondersteunde vragen

De volgende lijst bevat voorbeelden van vragen die momenteel niet worden ondersteund door AI Assistant in Journey Optimizer B2B edition:

* Welk accountpubliek gebruikt het veld workEmail.address van de veldgroep ... in de toestand? 
* Toon me het aantal actieve reizen gebruikend rekeningspubliek van meer dan 10.000, 5000-10.000, 1000-5000, en minder dan 1000, in een distributie visueel
* Wie heeft de laatste actualisering gemaakt op reis x voor rekening?
* Hoeveel actieve reizen voegen het kopen groepsleden voor oplossingsrente x toe?
* Welke actieve reizen voegen het kopen groepsleden voor oplossingsrente x toe?
* Wat is de gemeenschappelijkste titel van besluitvormer van het kopen groepsmalplaatjes?
* Wie zijn de besluitvormers voor het kopen van groepsmalplaatje x?

## Volgende stappen

Voor informatie over hoe te om de AI Hulpeigenschappen tijdens uw werkschema&#39;s te gebruiken, zie [ Medewerker van AI van het Gebruik in Journey Optimizer B2B edition ](./use-ai-assistant.md).
