---
title: Groepen kopen
description: Leer hoe kopersgroepen in Journey Optimizer B2B edition de doeltreffendheid van marketing kunnen verhogen door leden voor uw accountlijsten te identificeren en te richten.
feature: Buying Groups
role: User
exl-id: ddcd7b62-6a76-4f5e-b6d3-a20944ca8332
source-git-commit: ada98f505aad848f958cf8325ed90d66692a6cac
workflow-type: tm+mt
source-wordcount: '1988'
ht-degree: 6%

---


# Koopgroepen

Voor B2B-verkoop- en marketingactiviteiten zijn rekeningen van essentieel belang voor elke strategie. Elke account heeft een groep personen die erbij betrokken zijn, en deze personen kunnen werknemers van de account of contractanten zijn die met de account werken. Accounts zijn hiërarchisch en verschillende producten kunnen op verschillende niveaus in de hiërarchie worden verkocht. Adobe Experience Platform kan bijvoorbeeld op bedrijfsniveau worden verkocht aan een top-level account. En Adobe Photoshop kan worden verkocht aan een rekening die een afdeling of afdeling binnen een organisatie vertegenwoordigt, zoals een ontwerpafdeling binnen een grotere onderneming.

![ diagram van de rollen van de Rekening ](assets/account-roles-diagram.png){width="800"}

Binnen de rekening, zou er een ondergroep van mensen kunnen zijn die uit de _het kopen groep_ bestaan. Deze mensen nemen uiteindelijk het aankoopbesluit, dus ze hebben speciale aandacht van de marketeer nodig en hebben mogelijk andere informatie nodig die ze ontvangen dan de andere personen die bij de rekening horen. Kopersgroepen kunnen een verschillende groep personen voor verschillende productlijnen of aanbiedingen omvatten. Een product voor cyberbeveiliging kan bijvoorbeeld gewoonlijk een Chief Information Officer of Chief Security Officer vereisen, en een vertegenwoordiger van de Juridische Dienst om een aankoop goed te keuren. Een insectenvolgend product zou typisch een VP van Techniek en een Directeur van IT als leden van de het kopen groep kunnen hebben.

![ Video ](../../assets/do-not-localize/icon-video.svg){width="30"} [ bekijk het videooverzicht ](#overview-video)

## Belangrijkste componenten

U kunt de doeltreffendheid van marketing verhogen door koopgroepen in Journey Optimizer B2B edition te vestigen die leden voor uw doelaccountlijsten identificeren die op de oplossingen worden gebaseerd die uw teams van de Verkoop voor de verkoop verantwoordelijk zijn. Voordat u en uw marketingteam beginnen met het maken van uw inkoopgroepen, moet u controleren of de belangrijkste componenten zijn gedefinieerd. Deze componenten zijn kritiek voor het ontmoeten van uw bedrijfsdoelstellingen en doelstellingen.

| Component | Doel |
| --------- | ------- |
| Oplossingsrente | Deze component geeft het antwoord op: <ul><li>Wat verkoopt u als marketingorganisatie?</li><li>Welk product of welke inzameling van producten richt u om te verkopen?</li></ul>  **_Voorbeeld:_** Het dwars-verkopen van nieuw Product X aan bestaande klanten |
| Accountpubliek | Deze component geeft het antwoord op: <ul><li>Aan wie verkoopt u?</li><li>Wat is de lijst van rekeningen die u richt?</li></ul> **_Example:_** het segment van de Rekening die door rekeningen met Product Y wordt bepaald die opbrengst over 1M hebben |
| Rolinesjablonen voor groepen kopen | Deze component geeft het antwoord op: <ul><li>Welke rollen richt u zich?</li><li>Welke reeks regels worden gebruikt om te bepalen wie aan het kopen van groepsrollen wordt toegewezen?</li></ul>  **_Voorbeeld:_** Wijs een persoon met de titel van Com aan de rol van de Maker van het Besluit toe |
| Groepsfasen voor kopen | (Optioneel) Deze component geeft het antwoord op: Hoe volgt de inkoopgroep op succes of falen? |

## Lidopdracht

Er zijn drie manieren waarop leden worden toegewezen aan of verwijderd uit een inkoopgroep. In de volgende lijst worden deze methoden voor toevoegen en verwijderen in de volgorde van prioriteit beschreven. De bovenste methode heeft de hoogste prioriteit en een lagere methode kan deze niet overschrijven.

1. **_Handmatige actie_** - een handboek voegt lid toe of verwijdert lidactie die door een verkoopgebruiker voor de het kopen groep wordt uitgevoerd
2. **_actie van de Reis_** - Reis [ actieknooppunten voor het kopen van groepslidmaatschap ](../journeys/action-nodes.md#add-a-people-based-action) (_wijs aan het Kopen groep_ toe of _verwijder uit het Kopen groep_)
3. **_de banen van het Systeem_** - het Kopen groep [ creatie ](../buying-groups/buying-groups-create.md#buying-group-creation-jobs) en onderhoudstaken.

Om ervoor te zorgen dat de lidtoewijzing in een koopgroep niet verkeerd wordt met voeten getreden, is deze lijst in de orde van belangrijkheid die in het systeem wordt gevolgd om nauwkeurige lidtoewijzing te verzekeren. Wanneer een verkoopgebruiker bijvoorbeeld handmatig een lid aan de inkoopgroep toevoegt, wil hij niet dat een onderhoudstaak die toevoeging wijzigt. Gebruikend de belangrijkheidsorde, worden de volgende scenario&#39;s afgedwongen:

* Als een gebruiker manueel een lid aan een het kopen groep toewijst, en dit door een het kopen baan van het groepsonderhoud wordt gevolgd die het zelfde lid uit de het kopen groep verwijdert, verwijdert de onderhoudstaak **niet** dat lid en kan niet de handtaak met voeten treden.
* Als een gebruiker manueel een lid aan een het kopen groep toewijst, en dit door een teweeggebrachte reisknoop wordt gevolgd die het zelfde lid uit de het kopen groep verwijdert, verwijdert de knoopactie **niet** dat lid en kan niet de handtaak met voeten treden.
* Als een teweeggebrachte knoop van de reisactie een lid aan een het kopen groep toevoegt, en dit door een het kopen baan van het groepsonderhoud wordt gevolgd die het zelfde lid uit de het kopen groep verwijdert, verwijdert de onderhoudstaak **niet** dat lid en kan niet de taak van de reisactie met voeten treden.

## Workflow voor groepen kopen

1. Maak koopgroepen.

   * Bepaal [ oplossingsrente ](./solution-interests.md) en [ rolmalplaatje ](./buying-groups-role-templates.md)
   * [ creeer de het kopen groep ](./buying-groups-create.md#create-buying-groups) en wijs [ het kopen groepsstadia ](./buying-group-stages.md) toe.

1. Ontbrekende personen volledig identificeren.

   Analyseer de inkoopgroep met gebruik van filters.

   **_Example:_** de rol van de Maker van het Besluit mist en de volledigheidsscore is &lt; 50

1. Vul de definities van inkoopgroepen in.
<!--
   * Acquire missing people
   * Send to LinkedIn Destination
   * Enrich with Zoominfo -->

1. Voeg groepsacties voor kopen toe aan uw accountreizen.

## Koopgroepen en componenten weergeven

Vouw **[!UICONTROL Accounts]** uit in de linkernavigatie en klik op **[!UICONTROL Buying groups]** .

De pagina _[!UICONTROL Buying groups]_&#x200B;is ingedeeld als tabbladen:

| Tab | Beschrijving |
| --- | ----------- |
| [!UICONTROL Overview] | Dit lusje is het gebrek en toont [ het Kopen groepen dashboard ](../dashboards/buying-groups-dashboard.md). |
| [!UICONTROL Browse] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken op de naam van de inkoopgroep. </li><li>Filteren op interesse van oplossing. </li><li>Meld u aan bij het kopen van groepsgegevens. </li><li>Maak een inkoopgroep. </li></ul> |
| [!UICONTROL Solution interests] | Dit tabblad biedt ondersteuning voor de volgende activiteiten: <ul><li>De lijst met bestaande inkoopgroepen weergeven. </li><li>Zoeken op de naam van de inkoopgroep. </li><li>De toegang en geeft de eigenschappen van oplossingsbelang uit. </li><li>Creëer een oplossingsbelang. </li><li>Verwijder een belang voor de oplossing. </li><li>Groeptaken voor kopen weergeven en verwijderen. </li></ul> |
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
| [!UICONTROL Visit Webpage] | Een lid bezoekt een webpagina | Web | 20 | 40 |
| [!UICONTROL Fill Out Form] | Een lid vult een formulier in en verzendt het op een webpagina | Web | 20 | 40 |
| [!UICONTROL Click Link] | Een lid klikt op een koppeling op een webpagina | Web | 20 | 40 |
| [!UICONTROL Open Email] | Een lid opent een e-mail | E-mail | 20 | 30 |
| [!UICONTROL Click Email] | Een lid klikt op een koppeling in een e-mailbericht | E-mail | 20 | 30 |
| [!UICONTROL Open Sales Email] | Een lid opent een e-mail over verkopen | E-mail | 20 | 30 |
| [!UICONTROL Click Sales Email] | Een lid klikt op een koppeling in een e-mailbericht voor verkopen | E-mail | 20 | 30 |
| [!UICONTROL Interesting Moment] | Een lid heeft een interessant moment | Gekromd | 20 | 60 |
| [!UICONTROL Tap Push Notification] | Een lid ontvangt een pushmelding | Mobiel | 20 | 30 |
| [!UICONTROL Mobile App Activity] | Een lid voert een activiteit uit op een mobiele app | Mobiel | 20 | 30 |
| [!UICONTROL Mobile App Session] | Een lid is actief op een mobiele app-sessie | Mobiel | 20 | 30 |
| [!UICONTROL Fill Out Facebook Lead Ads Form] | Een lid vult een formulier voor advertentieplaatsen in en verzendt dit op een Facebook-pagina | Sociaal | 20 | 30 |
| [!UICONTROL Click RTP Call to Action] | Een lid klikt op een gepersonaliseerde call to action | Web | 20 | 60 |
| [!UICONTROL View In-App Message] | Een lid bekijkt een bericht in de app | Mobiel | 20 | 30 |
| [!UICONTROL Tap In-App Message] | Een lid tikt op een bericht in de app | Mobiel | 20 | 30 |
| [!UICONTROL Subscribe SMS] | Een lid abonneert op SMS-communicatie | SMS | 20 | 90 |
| [!UICONTROL Reply to Sales Email] | Een lid antwoordt op een e-mail over verkopen | E-mail | 20 | 30 |
| [!UICONTROL Engaged with a Dialogue] | Een lid maakt deel uit van een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Dialogue] | Een lid communiceert met een document in een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Dialogue] | Een lid plant een afspraak in een Dynamic Chat-dialoog | Chat | 20 | 90 |
| [!UICONTROL Reached Dialogue Goal] | Een lid bereikt een doel in een Dynamic Chat-dialoog |  | 20 | 90 |
| [!UICONTROL Responded to a poll in webinar] | Een lid reageert op een opiniepeiling in een webinar-gebeurtenis | Chat | 20 | 90 |
| [!UICONTROL Call to action clicked in webinar] | Een lid klikt op een call-to-action-koppeling in een webinar-gebeurtenis | Bellen | 20 | 30 |
| [!UICONTROL Asset downloads in webinar] | Een lid downloadt een bestand/middel in een webinar-gebeurtenis | Gebeurtenis | 20 | 60 |
| [!UICONTROL Asks questions in webinar] | Een lid stelt vragen in een webinar-gebeurtenis | Gebeurtenis | 20 | 60 |
| [!UICONTROL Has attended event] | Een lid woonde een gebeurtenis bij | Gebeurtenis | 20 | 60 |
| [!UICONTROL Engaged with an Agent in Dialogue] | Een lid maakt verbinding met een agent in een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Dialogue] | Een lid klikt op een koppeling in een Dynamic Chat-dialoogvenster | Chat | 20 | 90 |
| [!UICONTROL Engaged with a Conversational Flow] | Een lid werkt met een Dynamic Chat-gespreksstroom | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Conversational Flow] | Een lid plant een benoeming in een de gespreksstroom van Dynamic Chat | Chat | 20 | 90 |
| [!UICONTROL Reached Conversational Flow Goal] | Een lid bereikt een doel in een Dynamic Chat-gespreksstroom | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Conversational Flow] | Een lid communiceert met een document in een Dynamic Chat gespreksstroom | Chat | 20 | 90 |
| [!UICONTROL Engaged with an Agent in Conversational Flow] | Een lid gaat met een Agent in een Dynamic Chat gespreksstroom in dienst | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Conversational Flow] | Een lid klikt op een koppeling in een Dynamic Chat-omzettingsstroom | Chat | 20 | 90 |
| [!UICONTROL Click Link in SMS V2] | Een lid klikt op een koppeling in een SMS-bericht | SMS | 20 | 90 |

>[!NOTE]
>
>De de scoreactiviteiten van het engagement worden geregistreerd in het de activiteitenlogboek van Marketo Engage [ voor een persoon ](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"}.

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

>[!VIDEO](https://video.tv.adobe.com/v/3452939/?learn=on&captions=dut)
