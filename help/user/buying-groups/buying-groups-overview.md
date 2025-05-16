---
title: Groepen kopen
description: Leer hoe kopersgroepen in Journey Optimizer B2B edition de doeltreffendheid van marketing kunnen verhogen door leden voor uw accountlijsten te identificeren en te richten.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1760'
ht-degree: 6%

---


# Koopgroepen

Voor B2B-verkoop- en marketingactiviteiten zijn rekeningen van essentieel belang voor elke strategie. Elke account heeft een groep personen die erbij betrokken zijn, en deze personen kunnen werknemers van de account of contractanten zijn die met de account werken. Accounts zijn hiërarchisch en verschillende producten kunnen op verschillende niveaus in de hiërarchie worden verkocht. Adobe Experience Platform kan bijvoorbeeld op bedrijfsniveau worden verkocht aan een top-level account, terwijl Adobe Photoshop kan worden verkocht aan een account die een afdeling of afdeling binnen een organisatie vertegenwoordigt, zoals een designafdeling binnen een grotere onderneming.

![ diagram van de rollen van de Rekening ](assets/account-roles-diagram.png){width="800"}

Binnen de rekening, zou er een ondergroep van mensen kunnen zijn die uit de _het kopen groep_ bestaan. Dit zijn de mensen die uiteindelijk het aankoopbesluit nemen, dus ze hebben speciale aandacht van de marketeer nodig en hebben mogelijk andere informatie nodig die ze krijgen dan de andere mensen die bij de rekening horen. Kopersgroepen kunnen een verschillende groep personen voor verschillende productlijnen of aanbiedingen omvatten. Een product voor cyberbeveiliging kan bijvoorbeeld doorgaans een Chief Information Officer of Chief Security Officer en een vertegenwoordiger van de juridische afdeling vragen om een aankoop goed te keuren, maar een product voor het opsporen van fouten kan doorgaans een VP van Engineering en een IT Director hebben als leden van de inkoopgroep.

![ Video ](../../assets/do-not-localize/icon-video.svg){width="30"} [ bekijk het videooverzicht ](#overview-video)

## Belangrijkste componenten

U kunt de doeltreffendheid van marketing verhogen door in Journey Optimizer B2B edition inkoopgroepen op te richten die ontbrekende leden voor uw doelaccountlijsten identificeren op basis van de oplossingen die uw verkoopteams verantwoordelijk zijn voor de verkoop. Voordat u en uw marketingteam beginnen met het maken van uw inkoopgroepen, moet u controleren of de belangrijkste componenten zijn gedefinieerd. Deze componenten zijn kritiek voor het ontmoeten van uw bedrijfsdoelstellingen en doelstellingen.

| Component | Doel |
| --------- | ------- |
| Oplossingsrente | Deze component geeft het antwoord op: <ul><li>Wat verkoopt u als marketingorganisatie?</li><li>Welk product of welke inzameling van producten richt u om te verkopen?</li></ul>  **_Voorbeeld:_** Het dwars-verkopen van nieuw Product X aan bestaande klanten |
| Accountpubliek | Deze component geeft het antwoord op: <ul><li>Aan wie verkoopt u?</li><li>Wat is de lijst van rekeningen die u richt?</li></ul> **_Voorbeeld:_** segment van de Rekening dat door rekeningen met Product Y wordt bepaald die opbrengst over 1M hebben |
| Rolinesjablonen voor groepen kopen | Deze component geeft het antwoord op: <ul><li>Welke rollen richt u zich?</li><li>Welke reeks regels worden gebruikt om te bepalen wie aan het kopen van groepsrollen wordt toegewezen?</li></ul>  **_Voorbeeld:_** wijs een persoon met de titel van Com aan de rol van de Maker van het Besluit toe |
| Groepsfasen voor kopen | (Optioneel) Deze component geeft het antwoord op: Hoe volgt de inkoopgroep op succes of falen? |

## Workflow voor groepen kopen

1. Maak koopgroepen.

   * Bepaal [ oplossingsrente ](./solution-interests.md) en [ rolmalplaatje ](./buying-groups-role-templates.md)
   * [ creeer de het kopen groep ](./buying-groups-create.md#create-buying-groups) en wijs [ het kopen groepsstadia ](./buying-group-stages.md) toe.

1. Vermiste personen identificeren.

   Analyseer de inkoopgroep met gebruik van filters.

   **_Voorbeeld:_** de rol van de Maker van het Besluit mist en de volledigheidsscore is &lt; 50

1. Vul de definities van inkoopgroepen in.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Gebruik de koopgroep voor reizen naar je account.

## Koopgroepen en componenten weergeven

Vouw **[!UICONTROL Accounts]** uit in de linkernavigatie en klik op **[!UICONTROL Buying groups]** .

De pagina _[!UICONTROL Buying groups]_&#x200B;is ingedeeld als tabbladen:

| Tab | Beschrijving |
| --- | ----------- |
| [!UICONTROL Overview] | Dit lusje is het gebrek en toont [ het Kopen groepen dashboard ](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Browse] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken door groepsnaam te kopen. </li><li>Filteren op interesse van oplossing. </li><li>Meld u aan bij het kopen van groepsgegevens. </li><li>Maak een inkoopgroep. </li></ul> |
| [!UICONTROL Solution interests] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken door groepsnaam te kopen. </li><li>De toegang en geeft de eigenschappen van oplossingsbelang uit. </li><li>Creëer een oplossingsbelang. </li><li>Verwijder een belang voor de oplossing. </li><li>Groeptaken voor kopen weergeven en verwijderen. </li></ul> |
| [!UICONTROL Roles Templates] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>Bekijk de lijst met bestaande rolmalplaatjes. </li><li>Zoeken op naam van rolsjabloon. </li><li>Toegang tot en geef de eigenschappen en voorwaarden van het rolmalplaatje uit. </li><li>Een rolsjabloon maken. </li><li>Een rolsjabloon verwijderen. </li></ul> |
| [!UICONTROL Stages] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>Bekijk het bestaande model voor inkoopgroepen. </li><li>Open en bewerk het concept groepsfasemodel voor het kopen. </li><li>Maak het model voor de inkoopgroepfasen. </li></ul> |

## Zoeken en filteren van groepen

Gebruik het tabblad _[!UICONTROL Browse]_&#x200B;om de lijst met inkoopgroepen weer te geven. U kunt op naam zoeken en de lijst door oplossingsbelang filtreren.

![ Kopende groep doorbladert pagina ](assets/buying-groups-browse.png){width="800" zoomable="yes"}

## Gegevens van groep kopen

Klik op de naam van de inkoopgroep op het tabblad _[!UICONTROL Browse]_&#x200B;als u details voor een inkoopgroep wilt weergeven. [Meer informatie](./buying-group-details.md)

![ het Kopen groepdetails ](assets/buying-group-details.png){width="600" zoomable="yes"}

### Volledige score van inkoopgroep

De volledigheidsscore wordt gebruikt om te bepalen als de het kopen groep volledig is, zo betekent het dat het de juiste leden heeft die aan de rollen worden toegewezen en klaar is om in een rekeningsreis te worden gebruikt. Deze score is een percentage gebaseerd op het aantal rollen binnen de het kopen groep en hoeveel rollen met minstens één lood worden toegewezen.

Als er bijvoorbeeld vier rollen binnen een inkoopgroep zijn en drie van de vier rollen zijn toegewezen aan ten minste één lead, is de inkoopgroep 75% voltooid.

De volledigheidsscore van de inkoopgroep wordt telkens opnieuw berekend wanneer een inkoopgroep wordt gemaakt of bijgewerkt.

### Betrokkenheidsscore voor groep kopen

De score voor groepsbetrokkenheid kopen is een getal om de betrokkenheid van de leden van een inkoopgroep te bepalen op basis van de activiteiten die zij uitvoeren.

* De berekening van de betrokkenheidsscore begint zodra de inkoopgroep is gegenereerd.
* Voor de berekening van de score wordt gebruik gemaakt van binnenkomende activiteiten die de leden van de kopende groep in de laatste 30 dagen hebben uitgevoerd.
* Met het venster van 30 dagen en aangezien de activiteiten verlopen, kon de score dalen.
* Voor elke activiteit geldt een dagelijkse maximale frequentie van 20. Als een lid van een inkoopgroep meer dan 20 keer per dag dezelfde activiteit uitoefent, wordt het aantal activiteiten beperkt tot 20 en niet tot een hoger aantal.
* De weergegeven score wordt afgerond. Een score van 75,89999 wordt bijvoorbeeld weergegeven als 76.

+++Activiteiten die worden gebruikt voor scores

| Naam activiteit | Beschrijving | Type betrokkenheid | Maximale dagelijkse frequentie | Activiteitsgewicht |
| --- | --- | --- | --- | --- |
| Registreren voor gebeurtenis | Registreert voor een gebeurtenis die aan een campagne is gekoppeld | Gebeurtenis | 20 | 60 |
| Gebeurtenis bijwonen | Voert een campagnegebeurtenis bij | Gebeurtenis | 20 | 90 |
| E-mail openen | Hiermee opent u een e-mail | E-mail | 20 | 30 |
| Klik op E-mail | Klik op een koppeling in een e-mailbericht | E-mail | 20 | 30 |
| Verkoopbericht openen | Hiermee wordt een e-mail geopend | E-mail | 20 | 30 |
| Klik op E-mail verkoop | Klik op een koppeling in een e-mailbericht voor verkopen | E-mail | 20 | 30 |
| Interessant moment | Heeft een interessant moment | Gekromd | 20 | 60 |
| Tik op pushmelding | Hiermee wordt een pushmelding ontvangen | Mobiel | 20 | 30 |
| Mobiele toepassingsactiviteit | Hiermee wordt een activiteit uitgevoerd op een mobiele app | Mobiel | 20 | 30 |
| Mobiele App-sessie | Is actief op mobiele toepassingssessie | Mobiel | 20 | 30 |
| Formulier Advertentie Facebook invullen | Vult een formulier voor advertentieplaatsen in en verzendt het op een Facebook-pagina | Sociaal | 20 | 30 |
| Klik de Vraag van RTP aan Actie | Klik een gepersonaliseerde vraag aan actie | Web | 20 | 60 |
| Bericht in app weergeven | Hiermee wordt een bericht in de app weergegeven | Mobiel | 20 | 30 |
| Tik in-app-bericht | Tapt op een bericht in de app | Mobiel | 20 | 30 |
| SMS abonneren | Abonneren op SMS-communicatie | SMS | 20 | 90 |
| Reageren op e-mail over verkoop | Reageert op een e-mail met verkopen | E-mail | 20 | 30 |
| Bij een dialoogvenster | Afbeeldingen met een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| Interactie met document in dialoogvenster | Interacties maken met een document in een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| Geplande vergadering in dialoogvenster | Hiermee wordt een afspraak in een Dynamic Chat-dialoogvenster opgenomen | Chat | 20 | 90 |
| Dialoogvenster bereikt | Hiermee wordt een doel bereikt in een Dynamic Chat-dialoogvenster |  | 20 | 90 |
| Reageerd op een opiniepeiling in webinar | Hiermee wordt gereageerd op een opiniepeiling in een webinar-gebeurtenis | Chat | 20 | 90 |
| Aanroep van handeling geklikt in webinar | Klik een vraag-aan-actie verbinding in een webinar gebeurtenis | Bellen | 20 | 30 |
| Downloads van bedrijfsmiddelen in webinar | Hiermee wordt een bestand/middel gedownload in een webinar-gebeurtenis | Gebeurtenis | 20 | 60 |
| Vragen in webinar | Hiermee worden vragen gesteld in een webinar-gebeurtenis | Gebeurtenis | 20 | 60 |
| Heeft gebeurtenis bijgewoond | Heeft een gebeurtenis bijgewoond | Gebeurtenis | 20 | 60 |
| Betrokken met een Agent in Dialoog | Betrokkenen bij een agent in een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| Klikte koppeling in chatvenster | Klik op een koppeling in een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| Gegenereerd met een gespreksstroom | Beelden met een Dynamic Chat-gespreksstroom | Chat | 20 | 90 |
| Geplande vergadering in Conversational Flow | Hiermee wordt een afspraak in een Dynamic Chat-gespreksstroom gepland | Chat | 20 | 90 |
| Het bereikte doel van de discussiestroom | Hiermee wordt een doel bereikt in een Dynamic Chat-gespreksstroom | Chat | 20 | 90 |
| Werkt met Document in Gesprek Stroom | Communiceert met een document in een Dynamic Chat-gespreksstroom | Chat | 20 | 90 |
| Betrokken met een Agent in de Conversationele Stroom | Ondersteunt een agent in een Dynamic Chat-gespreksstroom | Chat | 20 | 90 |
| Klikte koppeling in chat in omschakelingsstroom | Klik op een koppeling in een Dynamic Chat-gespreksstroom | Chat | 20 | 90 |
| Klik op Koppeling in SMS V2 | Klik op een koppeling in een SMS-bericht | SMS | 20 | 90 |

>[!NOTE]
>
>De de scoreactiviteiten van het engagement worden geregistreerd in het de activiteitenlogboek van Marketo Engage [ voor een persoon ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"}.

+++

#### Weging

De gebruikers kunnen _weging_ aan elke rol in het rolmalplaatje toewijzen om verschillende gewichten voor een rol toe te wijzen om de betrokkenheidsscore te berekenen.

![ plaats weging aan elke rol in het rolmalplaatje ](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

Elk wegingsniveau wordt omgezet in een waarde die wordt gebruikt voor het berekenen van de betrokkenheidsscore:

* [!UICONTROL Trivial] = 20
* [!UICONTROL Minor] = 40
* [!UICONTROL Normal] = 60
* [!UICONTROL Important] = 80
* [!UICONTROL Vital] = 100

Een rolmalplaatje met drie rollen gewogen zoals _[!UICONTROL Vital]_,_[!UICONTROL Important]_, en _[!UICONTROL Normal]_&#x200B;zet in de volgende gewogen percentages om:

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
