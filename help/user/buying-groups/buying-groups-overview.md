---
title: Groepen kopen
description: Leer meer over het kopen van groepen en hun componenten.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 4%

---


# Koopgroepen

Voor B2B-verkoop- en marketingactiviteiten zijn rekeningen van essentieel belang voor elke strategie. Elke account heeft een groep personen die erbij betrokken zijn, en deze personen kunnen werknemers van de account of contractanten zijn die met de account werken. Accounts zijn hiërarchisch en verschillende producten kunnen op verschillende niveaus in de hiërarchie worden verkocht. Adobe Experience Platform kan bijvoorbeeld op bedrijfsniveau worden verkocht aan een top-level account, terwijl Adobe Photoshop kan worden verkocht aan een account die een afdeling of afdeling binnen een organisatie vertegenwoordigt, zoals een designafdeling binnen een grotere onderneming.

![ diagram van de rollen van de Rekening ](assets/account-roles-diagram.png){width="800"}

Binnen de rekening, zou er een ondergroep van mensen kunnen zijn die uit de _het kopen groep_ bestaan. Deze mensen zijn degenen die uiteindelijk het aankoopbesluit nemen, dus hebben ze speciale aandacht van de markteur nodig en hebben wellicht andere informatie nodig dan de andere mensen die bij de rekening horen. Kopersgroepen kunnen een verschillende groep personen voor verschillende productlijnen of aanbiedingen omvatten. Een product voor cyberbeveiliging kan bijvoorbeeld doorgaans een Chief Information Officer of Chief Security Officer en een vertegenwoordiger van de juridische afdeling vragen een aankoop goed te keuren, maar een product voor het opsporen van fouten kan doorgaans een VP van Engineering en een IT Director als leden van de inkoopgroep hebben.

## Belangrijkste componenten

U kunt de doeltreffendheid van de marketing verhogen door koopgroepen in Journey Optimizer B2B Edition te vestigen die ontbrekende leden voor uw doelrekeningen lijsten identificeren die op de oplossingen worden gebaseerd die uw teams van de Verkoop verantwoordelijk voor het verkopen zijn. Voordat u en uw marketingteam beginnen met het maken van uw inkoopgroepen, moet u controleren of de belangrijkste componenten zijn gedefinieerd. Deze componenten zijn kritiek voor het ontmoeten van uw bedrijfsdoelstellingen en doelstellingen.

| Component | Doel |
| --------- | ------- |
| Oplossingsrente | Deze component geeft het antwoord op: <ul><li>Wat verkoopt u als marketingorganisatie?</li><li>Welk product of welke inzameling van producten richt u om te verkopen?</li></ul>  **_Voorbeeld:_** Het dwars-verkopen van nieuw Product X aan bestaande klanten |
| Accountpubliek | Deze component geeft het antwoord op: <ul><li>Aan wie verkoopt u?</li><li>Wat is de lijst van rekeningen die u richt?</li></ul> **_Voorbeeld:_** segment van de Rekening dat door rekeningen met Product Y wordt bepaald die opbrengst over 1M hebben |
| Rolinesjablonen voor groepen kopen | Deze component geeft het antwoord op: <ul><li>Welke rollen richt u zich?</li><li>Welke reeks regels worden gebruikt om te bepalen wie aan het kopen van groepsrollen wordt toegewezen?</li></ul>  **_Voorbeeld:_** wijs een persoon met de titel van Com aan de rol van de Maker van het Besluit toe |

## Workflow voor groepen kopen

1. Maak koopgroepen.

   Opties:
   * De rente van de oplossing van het gebruik [ ](./solution-interests.md) en [ rolmalplaatje ](./buying-groups-role-templates.md)
   * Importeren van derden gebruiken
   * Genereren op basis van AI/ML

1. Vermiste personen identificeren.

   Analyseer de inkoopgroep met gebruik van filters.

   **_Voorbeeld:_** de rol van de Maker van het Besluit mist en de volledigheidsscore is &lt; 50

1. Vul de definities van inkoopgroepen in.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Gebruik in een rekeningsreis door het bijbehorende oplossingsbelang.

## Toegang tot inkoopgroepen en componenten

Vouw **[!UICONTROL Accounts]** uit in de linkernavigatie en klik op **[!UICONTROL Buying groups]** .

De pagina _[!UICONTROL Buying groups]_is ingedeeld als tabbladen:

| Tab | Beschrijving |
| --- | ----------- |
| [!UICONTROL Overview] | Dit lusje is het gebrek en toont [ het Kopen groepen dashboard ](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Browse] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken door groepsnaam te kopen. </li><li>Filteren op interesse van oplossing. </li><li>Meld u aan bij het kopen van groepsgegevens. </li><li>Maak een inkoopgroep. Verwijder een inkoopgroep.</li></ul> |
| [!UICONTROL Solution interests] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken door groepsnaam te kopen. </li><li>De toegang en geeft de eigenschappen van oplossingsbelang uit. </li><li>Creëer een oplossingsbelang. </li><li>Verwijder een belang voor de oplossing. </li><li>Groeptaken voor kopen weergeven en verwijderen. </li></ul> |
| [!UICONTROL Roles Templates] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>Bekijk de lijst met bestaande rolmalplaatjes. </li><li>Zoeken op naam van rolsjabloon. </li><li>Toegang tot en geef de eigenschappen en voorwaarden van het rolmalplaatje uit. </li><li>Een rolsjabloon maken. </li><li>Een rolsjabloon verwijderen. </li></ul> |

## Zoeken en filteren van groepen

Gebruik het tabblad _[!UICONTROL Browse]_om de lijst met inkoopgroepen weer te geven. U kunt op naam zoeken en de lijst door oplossingsbelang filtreren.

![ Kopende groep doorbladert pagina ](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Gegevens van groep kopen

Klik op de naam van de inkoopgroep op het tabblad _[!UICONTROL Browse]_als u details voor een inkoopgroep wilt weergeven.

![ het Kopen groepdetails ](assets/buying-group-details.png){width="600" zoomable="yes"}

### Volledige score van inkoopgroep

De volledigheidsscore wordt gebruikt om te bepalen als de het kopen groep volledig is, zo betekent het dat het de juiste leden heeft die aan de rollen worden toegewezen en klaar is om in een rekeningsreis te worden gebruikt. Deze score is een percentage gebaseerd op het aantal rollen binnen de het kopen groep en hoeveel rollen met minstens één lood worden toegewezen.

Als er bijvoorbeeld vier rollen binnen een inkoopgroep zijn en drie van de vier rollen zijn toegewezen aan ten minste één lead, is de inkoopgroep 75% voltooid.

De volledigheidsscore van de inkoopgroep wordt telkens opnieuw berekend wanneer een inkoopgroep wordt gemaakt of bijgewerkt.

### Betrokkenheidsscore voor groep kopen

De betrokkenheidsscore wordt gebruikt om de effectiviteit van uw marketingprogramma&#39;s te evalueren op basis van groepsgedragsactiviteiten die over reizen worden bijgehouden. Deze score is afgeleid van activiteit in de afgelopen 30 dagen. Om het even welke rolverandering in een malplaatje vereist herberekening van de betrokkenheidsscore voor alle koopgroepen die gebruikend dat malplaatje worden gecreeerd. Alleen binnenkomende activiteiten worden geëvalueerd bij het berekenen van een betrokkenheidsscore.

De weergegeven score is afgerond (een score van 75,89999 wordt weergegeven als 76), er is geen bovengrens voor de score voor GA en er is een dagelijkse frequentiegrens van 20.

De volgende voorbeelden demonstreren de berekening van de betrokkenheidsscore:

**het Kopen groep 1** - betrokkenheidsscore = 22.15

| Gebruiker | Functie | Rolgewicht | Handeling | Vandaag | Gisteren | Dikte van handeling | Score |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Adam | Beslissingsmaker | 80% | Bezochte website | 1000 | 2 | 1 | 22 |
| | | | Op e-mail geklikt | 1 | 0 | 1 | 1 |
| | | | Gedownloade Pub | 1 | 3 | 1 | 4 |
| Bob | Influencer | 15% | Bezochte website | 1 | 2 | 1 | 3 |
| Calvin | Praktijkster | 5% | Bezochte website | 1 | 1 | 1 | 2 |

**het Kopen groep 2** - betrokkenheidsscore = 8.55

| Gebruiker | Functie | Rolgewicht | Handeling | Vandaag | Gisteren | Dikte van handeling | Score |
| ---- | ---- | ----------- | ------ | ----- | --------- | ------------- | ----- |
| Alvin | Beslissingsmaker | 80% | Bezochte website | 3 | 2 | 1 | 5 |
| | | | Op e-mail geklikt | 1 | 0 | 1 | 1 |
| | | | Gedownloade Pub | 1 | 3 | 1 | 4 |
| Bret | Influencer | 15% | Bezochte website | 1 | 2 | 1 | 3 |
| Cam | Praktijkster | 5% | Bezochte website | 1 | 1 | 1 | 2 |
