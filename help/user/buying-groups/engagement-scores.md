---
title: Betrokkenheidsscore voor kopersgroepen
description: Bereken de scores voor inkoopgroep en persoonlijke betrokkenheid met behulp van gewogen activiteiten, op rol gebaseerde berekeningen en 30-daagse scores in Journey Optimizer B2B edition.
feature: Buying Groups, Engagement
role: User
exl-id: 424d9598-92dd-42de-8447-3c7cebc71a73
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 5%

---

# Betrokkenheidsscores {#engagement-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score"
>title="Betrokkenheidsscore"
>abstract="De betrokkenheidsscores bepalen het betrokkenheidsniveau voor het kopen van groepsleden."

Een betrokkenheidsscore is een getal dat het betrokkenheidsniveau voor de leden van een inkoopgroep aangeeft. Deze scores zijn gebaseerd op de activiteiten van de inkoopgroepsleden, de gewogen acties en de gewogen rollen. De resulterende scores worden genormaliseerd binnen een huurder (instantie) om verenigbare vergelijking toe te laten en voor actionable inzichten toe te staan. De berekening van de score begint zodra u de inkoopgroep maakt. Het Journey Optimizer B2B edition-gegevenshubsysteem berekent de scores dagelijks en uploadt deze naar het Multi-Level Marketing (MLM) MySQL-systeem met behulp van de innameservice.

Er zijn twee soorten betrokkenheidsscores:

* **het Kopen de score van de groepsovereenkomst** - de het kopen score van de groepsovereenkomst is een genormaliseerde score tussen 0 tot 100 en is gebaseerd op de betrokkenheidsscore die op het persoonniveau wordt berekend.

  De het kopen score van de groepsovereenkomst wordt getoond in de [ Kopen pagina van groepsdetails ](./buying-group-details.md). U kunt ook de meest betrokken inkoopgroepen bekijken op het intelligente dashboard.

  ![ het meest betrokken kopen groepen ](./assets/person-engagement-score-attribute-filtering.png){width="700" zoomable="yes"}

* **de betrokkenheidsscore van de Persoon** - de score van de personenbetrokkenheid is gebaseerd op de activiteiten van een individueel het kopen groepslid.

  De score van de personenovereenkomst voor elk het kopen groepslid wordt getoond in de het kopen pagina van de details van de groep [_[!UICONTROL Members]_&#x200B;tabel ](./buying-group-details.md#buying-group-members). Deze scores worden ook weergegeven in pagina&#39;s en dashboards die leden van het hoogste niveau en overlappende contactinformatie bevatten.

  ![ het meest betrokken kopen groepsleden ](./assets/top-engaged-buying-group-members.png){width="550" zoomable="yes"}

>[!BEGINSHADEBOX]

De score van de personenovereenkomst is een attribuut dat voor het filtreren in [ rolmalplaatjes ](./buying-groups-role-templates.md#add-the-template-roles) en [ reis versplintering-weg-door-mensen knopen ](../journeys/split-merge-paths-nodes.md#people-path-conditions) beschikbaar is.

![ heb toegang tot de gevormde gebeurtenisdefinities ](./assets/most-engaged-buying-groups.png){width="550" zoomable="yes"}

>[!ENDSHADEBOX]

Voor de berekening van de scores wordt elke op betrokkenheid gewogen activiteit gebruikt die de leden van de inkoopgroep in de laatste 30 dagen hebben uitgevoerd. In het venster van 30 dagen verlopen activiteiten en kunnen scores omlaag worden verplaatst (score wordt afgenomen). Weergegeven scores zijn afgerond (de score wordt bijvoorbeeld 75,89999 weergegeven als 76).

## Activiteiten die worden gebruikt voor het scoren van betrokkenheid

Het kopen van groep het scoren is niet _getriggerd-gebaseerd_. Het is een dagelijks proces dat de activiteit over alle leden van de het kopen groep evalueert en de score opnieuw berekent. De activiteiten gebruiken _gewichten_ om het kopen groepsscore volgens het actieve wegingsmodel te informeren, dat bepaalt hoe elke activiteit gewogen is.

Voor elke activiteit geldt een dagelijkse maximale frequentie van 20. Als een lid van een inkoopgroep dezelfde activiteit meer dan 20 keer op één dag uitoefent, wordt het aantal voor de activiteit beperkt tot 20.

| Naam activiteit | Beschrijving | Type betrokkenheid | Maximale dagelijkse frequentie | Standaardactiegewicht van model |
|---------------|-------------|-----------------|---------------------------|-------------------------------|
| Gebeurtenis bijwonen | Een lid woonde een gebeurtenis bij | Gebeurtenis | 20 | 60 |
| E-mail geklikt | Een lid klikt op een koppeling in een e-mailbericht | E-mail | 20 | 30 |
| E-mail geopend | Een lid opent een e-mail | E-mail | 20 | 30 |
| Formulier ingevuld | Een lid vult een formulier in en verzendt het op een webpagina | Web | 20 | 40 |
| Interessant moment | Een lid heeft een interessant moment | Gekromd | 20 | 60 |
| Koppelingsklikken | Een lid klikt op een koppeling op een webpagina | Web | 20 | 40 |
| Paginaweergaven | Een lid bekijkt een webpagina | Web | 20 | 40 |
| Registreren voor gebeurtenis | Een lid dat is geregistreerd voor een gebeurtenis | Gebeurtenis | 20 | 60 |

<!-- old list

| Activity name | Description | Engagement type | Max daily frequency count | Activity weight |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visit Webpage]| A member visits a web page | Web | 20 | 40 |
| [!UICONTROL Fill Out Form]| A member fills and submits a form on a web page | Web | 20 | 40 |
| [!UICONTROL Click Link] | A member clicks a link on a web page | Web | 20 | 40 |
| [!UICONTROL Open Email] | A member opens an email | Email | 20 | 30 |
| [!UICONTROL Click Email] | A member clicks a link in an email | Email | 20 | 30 |
| [!UICONTROL Open Sales Email] | A member opens a sales email | Email | 20 | 30 |
| [!UICONTROL Click Sales Email] | A member clicks a link in a sales email | Email | 20 | 30 |
| [!UICONTROL Interesting Moment] | A member has an interesting moment | Curated | 20 | 60 |
| [!UICONTROL Tap Push Notification] | A member receives a push notification | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Activity] | A member performs an activity on a mobile app | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Session] | A member is active on a mobile app session | Mobile | 20 | 30 |
| [!UICONTROL Fill Out Facebook Lead Ads Form] | A member fills and submits a Lead Ads form on a Facebook page | Social | 20 | 30 |
| [!UICONTROL Click RTP Call to Action] | A member clicks a personalized call to action | Web | 20 | 60 |
| [!UICONTROL View In-App Message] | A member views an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Tap In-App Message] | A member taps an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Subscribe SMS] | A member subscribes to SMS communications | SMS | 20 | 90 |
| [!UICONTROL Reply to Sales Email] | A member replies to a sales email | Email | 20 | 30 |
| [!UICONTROL Engaged with a Dialogue] | A member engages with a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Dialogue] | A member interacts with a document in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Dialogue] | A member schedules an appointment in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Reached Dialogue Goal] | A member reaches a goal in a Dynamic Chat dialogue |  |20 | 90 |
| [!UICONTROL Responded to a poll in webinar] | A member responds to a poll in a webinar event | Chat | 20 | 90 |
| [!UICONTROL Call to action clicked in webinar] | A member clicks a call-to-action link in a webinar event | Call | 20 | 30 |
| [!UICONTROL Asset downloads in webinar] | A member downloads a file/asset in a webinar event | Event | 20 | 60 |
| [!UICONTROL Asks questions in webinar] | A member asks questions in a webinar event | Event | 20 | 60 |
| [!UICONTROL Has attended event] | A member attended an event | Event | 20 | 60 |
| [!UICONTROL Engaged with an Agent in Dialogue] | A member engages with an agent in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Dialogue] | A member clicks a link in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Engaged with a Conversational Flow] | A member engages with a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Conversational Flow] | A member schedules an appointment in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Reached Conversational Flow Goal] | A member reaches a goal in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Conversational Flow] | A member interacts with a document in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Engaged with an Agent in Conversational Flow] | A member engages with an Agent in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Conversational Flow] | A member clicks a link in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Click Link in SMS V2] | A member clicks a link in an SMS message | SMS | 20 | 90 | -->

>[!NOTE]
>
>Activiteiten met betrekking tot de betrokkenheidsscore worden vastgelegd in het Marketo Engage-activiteitenlogboek voor een persoon. U hebt toegang tot dit logbestand in de verbonden Marketo Engage-instantie. Voor meer informatie, zie [ plaats van het Logboek van de Activiteit voor een Persoon ](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"} in de documentatie van Marketo Engage.

## weging rolsjabloon {#engagement-score-weighting}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score_weighting"
>title="weging van de betrokkenheidsscore"
>abstract="Gebruik rolweging om de berekening van de betrokkenheidsscore aan te passen."

De gebruikers kunnen _weging_ aan elke rol in het [ rolmalplaatje ](./buying-groups-role-templates.md) toewijzen om verschillende gewichten voor een rol toe te wijzen.

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

## Voorbeeld van score-berekening

In het volgende voorbeeld wordt de berekening van de betrokkenheidsscore weergegeven. Het gebruikt het geschetste percentage van het rolgewicht, het aantal binnenkomende activiteiten voor elk kopend groepslid, en een dagelijks maximum van 20 voor elke gebeurtenis voorkomen.

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

## Scorelogica

Naast de berekeningslogica die in het berekeningsvoorbeeld wordt geschetst, is er een beduidend complexe normalisatie van scores die in het systeem, over alle mensen, koopgroepen, en rekeningen in uw geval voorkomt. Een betrokkenheidsscore voor een inkoopgroep is afhankelijk van de persoonlijke betrokkenheidsscores, volgens de volgende geordende logica:

### Berekening van persoonlijke betrokkenheidsscore

1. Identificeer alle _verbindings-gewogen_ activiteitstypes die een bijbehorend gewicht en een dagelijks quotum, zoals websitebezoeken, e-mailklikken, en webinar aanwezigheid hebben.

1. Identificeer alle persoon _op betrokkenheid-gewogen_ acties die binnen het activiteitenterugblik-achtervenster worden uitgevoerd, die momenteel hard-gecodeerd aan 30 dagen is.

1. Normaliseer de activiteitstypegewichten over alle _op overeenkomst-gewogen_ die het type van activiteit in stap 1 wordt geïdentificeerd, negerend degenen die niet binnen het terugblik-achtervenster voorkwamen.

   Deze stap hefboomwerkingen _Min-Max Normalisatie_ en vermindert beduidend de kunstmatige verdunning van activiteitentype gewicht voor een huurder die hefboomwerking niet de meesten van hen.

1. Pas het dagelijkse quota filtreren per persoon en activiteitstype toe.

   Deze stap beperkt het hebben van zeer grote uitschieters door lager waarde/hoog volume activiteiten te vermijden die de scores scheeftrekken.

1. Bereken de score voor de onbewerkte persoonlijke betrokkenheid door de dagelijkse activiteit per type activiteit op te tellen, vermenigvuldigd met het bijbehorende gewicht, en dan de resultaten voor alle dagen van het terugkijkvenster op te tellen.

1. Gebruik de transformatie van de Transformatie van de a _Macht_ (Vierkante Wortel) om variatie te stabiliseren door mogelijke uitschieters te verminderen.

   Deze transformaties helpen schuine kanten te verminderen en patronen in de gegevens lineair te maken.

1. Pas een extra _Geschaalde transformatie van de Normalisatie_ toe om ervoor te zorgen dat de scores hefboomwerking de volledige waaier van 0 tot 100.

### Berekening van de betrokkenheidsscore voor groepen kopen

1. Pas een genormaliseerd gewicht op elk het kopen groepslid door rol toe, volgens het gewicht dat in het rolmalplaatje wordt gevormd.

1. Normaliseer het gewicht van de inkoopgroep voor elke inkoopgroep.

   Deze normalisatie vermijdt onnodige verdunning van het rolgewicht als een inkoopgroep niet alle rollen gebruikt.

1. Alle betrokkenheidsscores van de persoon van de koopgroep samenvoegen door de score van de persoonlijke betrokkenheid te vermenigvuldigen met de rol van de persoon genormaliseerde rolgewicht, en deze bij elkaar op te tellen.

1. Pas de transformatie van de Transformatie van de a _Macht_ (Vierkante Wortel) toe om variatie te stabiliseren door mogelijke uitschieters, vooral voor zeer grote het kopen groepen te verminderen.

1. Pas een extra _Geschaalde transformatie van de Normalisatie_ toe om ervoor te zorgen dat de scores hefboomwerking de volledige waaier van 0 tot 100.
