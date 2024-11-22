---
title: Groepen kopen
description: Leer hoe kopers in Journey Optimizer B2B edition de doeltreffendheid van marketing kunnen verhogen door leden voor je accountlijsten te identificeren en als doelgroep te kiezen.
feature: Buying Groups
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 02b0e1a50b75dc02afe1b11217729e17583d5f12
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 3%

---


# Koopgroepen

Voor B2B-verkoop- en marketingactiviteiten zijn rekeningen van essentieel belang voor elke strategie. Elke account heeft een groep personen die erbij betrokken zijn, en deze personen kunnen werknemers van de account of contractanten zijn die met de account werken. Accounts zijn hiërarchisch en verschillende producten kunnen op verschillende niveaus in de hiërarchie worden verkocht. Adobe Experience Platform kan bijvoorbeeld op bedrijfsniveau worden verkocht aan een top-level account, terwijl Adobe Photoshop kan worden verkocht aan een account die een afdeling of afdeling binnen een organisatie vertegenwoordigt, zoals een designafdeling binnen een grotere onderneming.

![ diagram van de rollen van de Rekening ](assets/account-roles-diagram.png){width="800"}

Binnen de rekening, zou er een ondergroep van mensen kunnen zijn die uit de _het kopen groep_ bestaan. Dit zijn de mensen die uiteindelijk het aankoopbesluit nemen, dus ze hebben speciale aandacht van de marketeer nodig en hebben mogelijk andere informatie nodig die ze krijgen dan de andere mensen die bij de rekening horen. Kopersgroepen kunnen een verschillende groep personen voor verschillende productlijnen of aanbiedingen omvatten. Een product voor cyberbeveiliging kan bijvoorbeeld doorgaans een Chief Information Officer of Chief Security Officer en een vertegenwoordiger van de juridische afdeling vragen een aankoop goed te keuren, maar een product voor het opsporen van fouten kan doorgaans een VP van Engineering en een IT Director als leden van de inkoopgroep hebben.

![ Video ](../../assets/do-not-localize/icon-video.svg){width="30"} [ bekijk het videooverzicht ](#overview-video)

## Belangrijkste componenten

U kunt de doeltreffendheid van de marketing verhogen door koopgroepen in Journey Optimizer B2B edition te vestigen die ontbrekende leden voor uw doelrekeningen lijsten identificeren die op de oplossingen worden gebaseerd die uw teams van de Verkoop voor de verkoop verantwoordelijk zijn. Voordat u en uw marketingteam beginnen met het maken van uw inkoopgroepen, moet u controleren of de belangrijkste componenten zijn gedefinieerd. Deze componenten zijn kritiek voor het ontmoeten van uw bedrijfsdoelstellingen en doelstellingen.

| Component | Doel |
| --------- | ------- |
| Oplossingsrente | Deze component geeft het antwoord op: <ul><li>Wat verkoopt u als marketingorganisatie?</li><li>Welk product of welke inzameling van producten richt u om te verkopen?</li></ul>  **_Voorbeeld:_** Het dwars-verkopen van nieuw Product X aan bestaande klanten |
| Accountpubliek | Deze component geeft het antwoord op: <ul><li>Aan wie verkoopt u?</li><li>Wat is de lijst van rekeningen die u richt?</li></ul> **_Voorbeeld:_** segment van de Rekening dat door rekeningen met Product Y wordt bepaald die opbrengst over 1M hebben |
| Rolinesjablonen voor groepen kopen | Deze component geeft het antwoord op: <ul><li>Welke rollen richt u zich?</li><li>Welke reeks regels worden gebruikt om te bepalen wie aan het kopen van groepsrollen wordt toegewezen?</li></ul>  **_Voorbeeld:_** wijs een persoon met de titel van Com aan de rol van de Maker van het Besluit toe |
| Groepsfasen voor kopen | (Optioneel) Deze component geeft het antwoord op: Hoe volgt de inkoopgroep op succes of falen? |

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

## Koopgroepen en componenten weergeven

Vouw **[!UICONTROL Accounts]** uit in de linkernavigatie en klik op **[!UICONTROL Buying groups]** .

De pagina _[!UICONTROL Buying groups]_is ingedeeld als tabbladen:

| Tab | Beschrijving |
| --- | ----------- |
| [!UICONTROL Overview] | Dit lusje is het gebrek en toont [ het Kopen groepen dashboard ](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Browse] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken door groepsnaam te kopen. </li><li>Filteren op interesse van oplossing. </li><li>Meld u aan bij het kopen van groepsgegevens. </li><li>Maak een inkoopgroep. Verwijder een inkoopgroep.</li></ul> |
| [!UICONTROL Solution interests] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken door groepsnaam te kopen. </li><li>De toegang en geeft de eigenschappen van oplossingsbelang uit. </li><li>Creëer een oplossingsbelang. </li><li>Verwijder een belang voor de oplossing. </li><li>Groeptaken voor kopen weergeven en verwijderen. </li></ul> |
| [!UICONTROL Roles Templates] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>Bekijk de lijst met bestaande rolmalplaatjes. </li><li>Zoeken op naam van rolsjabloon. </li><li>Toegang tot en geef de eigenschappen en voorwaarden van het rolmalplaatje uit. </li><li>Een rolsjabloon maken. </li><li>Een rolsjabloon verwijderen. </li></ul> |
| [!UICONTROL Stages] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>Bekijk het bestaande model voor inkoopgroepen. </li><li>Open en bewerk het concept groepsfasemodel voor het kopen. </li><li>Maak het model voor de inkoopgroepfasen. </li></ul> |

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

De score voor groepsbetrokkenheid kopen is een getal om de betrokkenheid van de leden van een inkoopgroep te bepalen op basis van de activiteiten die zij uitvoeren. Voor de berekening van de score wordt gebruik gemaakt van binnenkomende activiteiten die de leden van de kopende groep in de laatste 30 dagen hebben uitgevoerd.

Voor elke activiteit geldt een dagelijkse maximale frequentie van 20. Als een lid van een inkoopgroep meer dan 20 keer per dag dezelfde activiteit uitoefent, wordt het aantal activiteiten beperkt tot 20 en niet tot een hoger aantal.

De weergegeven score wordt afgerond. Een score van 75,89999 wordt bijvoorbeeld weergegeven als 76.

#### Weging

De gebruikers kunnen _weging_ aan elke rol in het rolmalplaatje toewijzen om verschillende gewichten voor een rol toe te wijzen om de betrokkenheidsscore te berekenen.

![ plaats weging aan elke rol in het rolmalplaatje ](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Elk wegingsniveau wordt omgezet in een waarde die wordt gebruikt voor het berekenen van de betrokkenheidsscore:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Minor] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Important] = 80
* [!UICONTROL Vital] = 100

Een rolmalplaatje met drie rollen gewogen zoals _[!UICONTROL Vital]_,_[!UICONTROL Important]_, en _[!UICONTROL Normal]_zet in de volgende gewogen percentages om:

| Functie | Weging | Systeemwaarde | Waarde berekenen | Percentage |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| Beslissingsmaker | Vital | 100 | 240-100 | 41,67% |
| Influencer | Belangrijk | 80 | 240-80 | 33,33% |
| Praktijkster | Normaal | 60 | 240-60 | 25% |
|               | Totaal | 240 |                   |           |

#### Berekeningsvoorbeeld

In het volgende voorbeeld wordt de berekening van de betrokkenheidsscore weergegeven aan de hand van het gewichtspercentage van de omgezette rol, het aantal inkomende activiteiten voor elk lid van de inkoopgroep en een dagelijks maximum van 20 graden voor elke gebeurtenis (als dit meerdere keren is gebeurd).

| Functie | Lid | Type activiteit | Aantal van gisteren | Aantal vandaag | Berekening | Totale score |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| Beslissingsmaker | Adam | Bezochte website | 37 | 15 | 20 + 15 | 35 |
|               |          | Geplikte e-mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Markeren | Bezochte website | 5 | 3 | 5 + 3 | 8 |
|               |          | Geplikte e-mail | 1 | 1 | 1 + 1 | 2 |
|               |          | Gedownloade publicatie | 3 | 2 | 3 + 2 | 5 |
| **Totale score van Makers van het Besluit** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| Influencer | John | Bezochte website | 19 | 9 | 19 + 9 | 28 |
| **totale score van Influencers** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| Praktijkster | Bob | Geplikte e-mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | Geplikte e-mail | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | Geplikte e-mail | 1 | 1 | 1 + 1 | 2 |
|               |          | Bezochte website | 1 | 7 | 1 + 7 | 8 |
|               |          | Gedownloade publicatie | 1 | 2 | 1 + 2 | 3 |
| **totale score van Praktijken** |         |             |                 |             |      | **17** |

De uiteindelijke betrokkenheidsscore wordt berekend door de weging toe te passen voor elk van de rolscores:

| Functie | Rol totale score | Rolgewicht % | Score X-gewicht % |
|-------------- |---------------- |------------- |---------------- |
| Beslissingsmakers | 52 | 41,67% | 21,67 |
| Influencers | 28 | 33,33% | 9,33 |
| Praktijken | 17 | 25% | 4,25 |
| **Definitieve betrokkenheidsscore** |                |             | **35.25** |

## Video over overzicht

>[!VIDEO](https://video.tv.adobe.com/v/3433078/?learn=on)
