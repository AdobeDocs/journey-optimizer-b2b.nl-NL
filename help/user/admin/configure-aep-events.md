---
title: Ervingsgebeurtenissen en velden selecteren
description: Selecteer Experience Platform-gebeurtenissen en -velden om real-time beslissingen te activeren tijdens reizen op basis van klantgedrag.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een bètaversie"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 5f3d7bb8eb72c48409273de43b03114d273cb80c
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Erviteitsgebeurtenissen en velden selecteren

De beheerders kunnen specifieke [&#x200B; Gebeurtenissen van de Ervaring van AEP &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} en hun bijbehorende gebieden binnen het de unieschema van de Gebeurtenis van de Ervaring selecteren. Na selectie, kunnen de gebruikers beslissingsregels vormen om aan die Gebeurtenissen van de Ervaring te luisteren om dynamische en gerichte campagneacties toe te laten die op dichtbij gebeurtenisgegevens in real time worden gebaseerd.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
Het gebruik van ervaringen met AEP tijdens reizen is een proces in twee stappen:

1. Een beheerder [&#x200B; voegt de ervaringsgebeurtenissen en gebieden van AEP &#x200B;](#add-an-event) in de configuraties van B2B edition van Journey Optimizer toe.

2. In een reis, voegt een teller a _toe luistert naar een gebeurtenis_ knoop en [&#x200B; selecteert een Gebeurtenis van de Ervaring &#x200B;](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Selecteert de gebeurtenis die in de knoop moet worden gebruikt.
   * Hiermee selecteert u de velden die u als restricties wilt gebruiken.

>[!BEGINSHADEBOX]

## Richtlijnen en beperkingen

Houd rekening met het volgende wanneer u gebeurtenissen selecteert om uw organisatorische doelen te bereiken:

* U kunt maximaal 50 gebeurtenissen en maximaal 100 velden per gebeurtenis selecteren.

* De reizen kunnen aan de Gebeurtenissen van de Ervaring luisteren die gebruikend Experience Platform het stromen mogelijkheden, zoals Web SDK of HTTP API worden opgenomen.

* U kunt de Gebeurtenissen van de Ervaring voor beslissingsdoeleinden binnen een reis gebruiken, maar zij worden niet behouden. Daarom kunt u geen historisch overzicht van Experience Events gebruiken binnen Journey Optimizer B2B edition.

* Wanneer u een Experience Event gebruikt en de reis publiceert, kunt u meer velden toevoegen, maar u kunt geen velden verwijderen die eerder waren geselecteerd.

* U kunt verwijzen naar een Experience Event tijdens meerdere reizen of één keer gebruiken binnen dezelfde reis.

>[!ENDSHADEBOX]

## Experience Events beheren

1. Kies in de linkernavigatie **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** .

1. Klik op **[!UICONTROL XDM Classes]** in het tussenliggende deelvenster en klik vervolgens op de tab **[!UICONTROL Events]** om de lijst met beschikbare gebeurtenissen weer te geven.

   ![&#x200B; heb toegang tot de geselecteerde Gebeurtenissen van de Ervaring &#x200B;](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   De tabel wordt gesorteerd op de kolom _[!UICONTROL Last update]_. De meest recente bijgewerkte gebeurtenissen worden standaard bovenaan weergegeven.

   Van deze pagina, kunt u [&#x200B; selecteren en &#x200B;](#add-an-event) [&#x200B; gebeurtenissen voor gebruik in reizen uitgeven.](#edit-an-event)

   Klik op de naam van een gebeurtenis om de gegevens voor een geselecteerde gebeurtenis te openen.

### De gebeurtenislijst filteren

Typ tekst in het veld _[!UICONTROL Search]_&#x200B;om de weergegeven gebeurtenissen te filteren op een overeenkomst met de naam van de gebeurtenis.

![&#x200B; filter de lijst van geselecteerde gebeurtenissen door naam &#x200B;](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Een gebeurtenis toevoegen

Om een Gebeurtenis van de Ervaring beschikbaar te maken voor a _luistert naar een gebeurtenis_ knoop in een reis, selecteer de gebeurtenis en de gesteunde gebieden.

>[!NOTE]
>
>In de bètaversie kunt u geen gebeurtenissen uit de lijst verwijderen. Zorg ervoor dat elke gebeurtenis die u toevoegt één is die uw organisatie van plan is te gebruiken.

1. Klik op **[!UICONTROL Select experience event]** rechtsboven.

   De pagina met gebeurtenisdetails wordt weergegeven. Op deze pagina kunt u het gebeurtenistype en de velden kiezen.

   ![&#x200B; de details van de Gebeurtenis voor een nieuwe gebeurtenis &#x200B;](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Kies het gebeurtenistype.

   * Klik op **[!UICONTROL Select event type]**.

   * Kies het gebeurtenistype in het dialoogvenster.

     Gebruik het veld _[!UICONTROL Search]_&#x200B;om de weergegeven lijst op naam te filteren. Gebruik de schuifregelaar **[!UICONTROL Only show selected fields]**&#x200B;om de huidige selecties te bekijken.

     ![&#x200B; Uitgezochte dialoog van het gebeurtenistype &#x200B;](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Klik op **[!UICONTROL Select]**.

1. Kies een of meer velden voor het gebeurtenistype.

   * Klik op **[!UICONTROL Select fields]**.

   * Selecteer in het dialoogvenster de velden die u wilt gebruiken als beperkingen voor overeenkomende gebeurtenissen.

     Gebruik het veld _[!UICONTROL Search]_&#x200B;om de weergegeven lijst op naam te filteren. Gebruik de schuifregelaar **[!UICONTROL Only show selected fields]**&#x200B;om de huidige selecties te bekijken.

     ![&#x200B; Uitgezochte gebieden dialoog &#x200B;](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Klik op **[!UICONTROL Select]**.

1. Klik op **[!UICONTROL Save]** op de pagina met gebeurtenisdetails.

De opgeslagen gebeurtenis wordt weergegeven in de lijst op het tabblad _[!UICONTROL Events]_.

### Een gebeurtenis bewerken

Bewerk de gebeurtenisdetails om de velden te wijzigen.

1. Klik de gebeurtenisnaam, of klik _Meer menu_ ( **..**) pictogram en kies **[!UICONTROL Edit]**.

   ![&#x200B; klik het Meer menupictogram &#x200B;](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Klik op **[!UICONTROL Edit fields]** om meer velden toe te voegen of bestaande selecties uit het dialoogvenster _[!UICONTROL Select fields]_&#x200B;te verwijderen.

1. Klik op **[!UICONTROL Select]** om de selecties op te slaan.

### Een gebeurtenis verwijderen

>[!NOTE]
>
>Voor de Beta-versie van deze functie kunt u geen gebeurtenis verwijderen uit de lijst met geselecteerde gebeurtenissen. De gebeurtenis wordt verwijderd voor de GA-release.

## Gebeurtenissen en velden

Voor [!DNL Journey Optimizer B2B Edition] worden bepaalde activiteiten op personenniveau vastgelegd als [!DNL Experience Platform] Experience Events. Deze gebeurtenissen worden opgeslagen in een systeemdataset die het schema van de Gebeurtenis van de Ervaring XDM gebruikt en reis-specifieke gebiedsgroepen omvat. U kunt deze gebeurtenissen in [!UICONTROL Journey Optimizer B2B Edition] gebruiken zoals elke andere Experience Event.

Elke gebeurtenis stelt een bepaalde reeks gebieden bloot die in reis _kunnen worden gebruikt luisteren naar een gebeurtenis_ knopen (besluit dat op gebeurtenissen wordt gebaseerd). Bekijk de beschikbare gebeurtenistypen en de bijbehorende velden om te bepalen welke gebeurtenis en velden moeten worden gebruikt in deze transportknooppunten:

### E-mail verzonden

Deze gebeurtenis wordt bijgehouden wanneer een marketingbericht naar een persoon is verzonden.

Type gebeurtenis: `directMarketing.emailSent`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| E-mailbron-id | `directMarketing.emailSent.mailingKey.sourceID` |
| Type e-mailbron | `directMarketing.emailSent.mailingKey.sourceType` |
| E-mailbroninstantie-id | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| E-mailbronsleutel | `directMailing.emailSent.mailingKey.sourceKey` |
| Postnaam | `directMarketing.emailSent.mailingName` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail bezorgd

Deze gebeurtenis wordt bijgehouden wanneer een e-mailbericht correct is verzonden naar de e-mailservice van een persoon.

Type gebeurtenis: `directMarketing.emailDelivered `

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Id van mailbron | `directMarketing.mailingKey.sourceID` |
| Brontype voor verzending | `directMarketing.mailingKey.sourceType` |
| Id van broninstantie mailen | `directMarketing.mailingKey.sourceInstanceID` |
| Bronsleutel mailen | `directMarketing.mailingKey.sourceKey` |
| Postnaam | `directMarketing.mailingName` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail geopend

Deze gebeurtenis wordt bijgehouden wanneer een persoon een marketingbericht heeft geopend.

Type gebeurtenis: `directMarketing.emailOpened`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Id van mailbron | `directMarketing.mailingKey.sourceID` |
| Brontype voor verzending | `directMarketing.mailingKey.sourceType` |
| Id van broninstantie mailen | `directMarketing.mailingKey.sourceInstanceID` |
| Bronsleutel mailen | `directMarketing.mailingKey.sourceKey` |
| Postnaam | `directMarketing.mailingName` |
| Is een mobiel apparaat | `device.isMobileDevice` |
| Apparaatmodel | `device.model` |
| Gebruikersagent | `environment.browserDetails.userAgent` |
| Besturingssysteem | `environment.operatingSystem` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail geklikt

Deze gebeurtenis wordt bijgehouden wanneer iemand op een koppeling in een marketingmail heeft geklikt.

Type gebeurtenis: `directMarketing.emailClicked`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Id van mailbron | `directMarketing.mailingKey.sourceID` |
| Brontype voor verzending | `directMarketing.mailingKey.sourceType` |
| Id van broninstantie mailen | `directMarketing.mailingKey.sourceInstanceID` |
| Bronsleutel mailen | `directMarketing.mailingKey.sourceKey` |
| Postnaam | `directMarketing.mailingName` |
| URL van koppeling | `directMarketing.linkURL` |
| Is een mobiel apparaat | `device.isMobileDevice` |
| Model | `device.model` |
| Gebruikersagent | `environment.browserDetails.userAgent` |
| Besturingssysteem | `environment.operatingSystem` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail teruggestuurd

Deze gebeurtenis wordt bijgehouden wanneer een e-mail naar een persoon wordt teruggestuurd.

Type gebeurtenis: `directMarketing.emailBounced`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Id van mailbron | `directMarketing.mailingKey.sourceID` |
| Brontype voor verzending | `directMarketing.mailingKey.sourceType` |
| Id van broninstantie mailen | `directMarketing.mailingKey.sourceInstanceID` |
| Bronsleutel mailen | `directMarketing.mailingKey.sourceKey` |
| Postnaam | `directMarketing.mailingName` |
| E-mail | `directMarketing.email` |
| Gepubliceerde code e-mail | `directMarketing.emailBouncedCode` |
| Verzonden gegevens via e-mail | `directMarketing.emailBouncedDetails` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail is zacht

Deze gebeurtenis wordt bijgehouden wanneer een e-mail naar een persoon met een elektronische vorm wordt verzonden.

Type gebeurtenis: `directMarketing.emailBouncedSoft`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Id van mailbron | `directMarketing.mailingKey.sourceID` |
| Brontype voor verzending | `directMarketing.mailingKey.sourceType` |
| Id van broninstantie mailen | `directMarketing.mailingKey.sourceInstanceID` |
| Bronsleutel mailen | `directMarketing.mailingKey.sourceKey` |
| Postnaam | `directMarketing.mailingName` |
| E-mail | `directMarketing.email` |
| Gepubliceerde code e-mail | `directMarketing.emailBouncedCode` |
| Verzonden gegevens via e-mail | `directMarketing.emailBouncedDetails` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-mail niet geabonneerd

Deze gebeurtenis wordt bijgehouden wanneer een persoon zich niet meer heeft geabonneerd op een marketingmail.

Type gebeurtenis: `directMarketing.emailUnsubscribed `

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Id van mailbron | `directMarketing.mailingKey.sourceID` |
| Brontype voor verzending | `directMarketing.mailingKey.sourceType` |
| Id van broninstantie mailen | `directMarketing.mailingKey.sourceInstanceID` |
| Bronsleutel mailen | `directMarketing.mailingKey.sourceKey` |
| Postnaam | `directMarketing.mailingName` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Webpagina bezoeken

Dit gebeurtenistype is de standaardmethode voor het markeren van de hit als paginaweergave.

Type gebeurtenis: `web.webpagedetails.pageViews`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Bron-id webpagina | `web.webPageDetails.webPageKey.sourceID` |
| Brontype webpagina | `web.webPageDetails.webPageKey.sourceType` |
| Bron webpagina-instantie-id | `web.webPageDetails.webPageKey.sourceInstanceID` |
| Broncode webpagina | `web.webPageDetails.webPageKey.sourceKey` |
| Naam webpagina | `web.webPageDetails.name` |
| URL webpagina | `web.webPageDetails.URL` |
| Parameters webpaginaquery | `web.webPageDetails.queryParameters` |
| Webpagina-id | `web.webPageDetails.webPageID` |
| Gebruikersagent | `environment.browserDetails.userAgent` |
| Referrer-URL | `web.webReferrer.URL` |

+++

### Formulier ingevuld

Deze gebeurtenis volgt wanneer een persoon een formulier op een webpagina heeft ingevuld.

Type gebeurtenis: `web.formFilledOut`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Bron-id voor webformulier | `web.fillOutForm.webFormKey.sourceID` |
| Brontype voor webformulier | `web.fillOutForm.webFormKey.sourceType` |
| Instantie-id van webformulier | `web.fillOutForm.webFormKey.sourceInstanceID` |
| Broncode voor webformulier | `web.fillOutForm.webFormKey.sourceKey` |
| Webformulier-id | `web.fillOutForm.webFormID` |
| Webformuliernaam | `web.fillOutForm.webFormName` |
| Parameters webpaginaquery | `web.webPageDetails.queryParameters` |
| Webpagina-id | `web.webPageDetails.webPageID` |
| Gebruikersagent | `environment.browserDetails.userAgent` |
| Referrer-URL | `web.webReferrer.URL` |

+++

### Klikte webkoppeling

De gebeurtenissignalen dat SDK van het Web automatisch een verbindingsklik registreerde.

Type gebeurtenis: `web.webinteraction.linkClicks`

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Bron-id voor webinteractie | `web.webInteraction.webInteractionKey.sourceID` |
| Brontype voor webinteractie | `web.webInteraction.webInteractionKey.sourceType` |
| Instantie-id van webinteractiebron | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| Bronsleutel voor webinteractie | `web.webInteraction.webInteractionKey.sourceKey` |
| Koppelings-id voor webinteractie | `web.webInteraction.linkID` |
| URL webinteractiekoppeling | `web.webInteraction.linkURL` |
| Parameters webpaginaquery | `web.webPageDetails.queryParameters` |
| Webpagina-id | `web.webPageDetails.webPageID` |
| Gebruikersagent | `environment.browserDetails.userAgent` |
| Referrer-URL | `web.webReferrer.URL` |

+++

### Interessant moment

Deze gebeurtenis volgt wanneer een interessant moment voor een persoon werd opgenomen.

Type gebeurtenis: `leadOperation.interestingMoment `

+++Velden

| Veld | Veldtype |
| ----- | ---------- |
| Id | `_id` |
| Het type Event | `eventType` |
| Tijdstempel | `timestamp` |
| Persoon-id | `personID` |
| Bron-id persoon | `personKey.sourceID` |
| Brontype persoon | `personKey.sourceType` |
| Id van broninstantie van persoon | `personKey.sourceInstanceID` |
| Persoonlijke bronsleutel | `personKey.sourceKey` |
| Datum van tijdstip | `leadOperation.interestingMoment.date` |
| Momentbeschrijving | `leadOperation.interestingMoment.description` |
| Momentbron | `leadOperation.interestingMoment.source` |
| Het type Moment | `leadOperation.interestingMoment.type` |
| Reis-id | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Knooppunt-id | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->