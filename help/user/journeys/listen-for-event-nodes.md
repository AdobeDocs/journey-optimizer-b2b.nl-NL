---
title: Luisteren naar een gebeurtenis
description: Configureer gebeurtenisknooppunten voor account en persoonlijke triggers - luister naar het aanschaffen van groepswijzigingen, het klikken via e-mail, het invullen van formulieren en Experience Platform-gebeurtenissen in Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: f5fc362d52ff83335c71b5efe7ea2915d6a7e330
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 1%

---

# Luisteren naar een gebeurtenis

Voeg _toe luistert naar een gebeurtenis_ knoop om uw publiek naar de volgende stap in de rekeningsreis vooruit te bewegen wanneer een gebeurtenis voorkomt.

![ Video ](../../assets/do-not-localize/icon-video.svg) {width= &quot;30&quot;, verticaal-richt= &quot;midden&quot; [ bekijk de overzichtsvideo ](#overview-video)

>[!NOTE]
>
>U kunt dit knooppunttype niet toevoegen op gesplitste weg door mensen.

## Accountgebeurtenissen

Luister naar een gebeurtenis op basis van de account wanneer u de account voorwaarts wilt laten gaan tijdens de reis volgens gebeurtenissen die worden geactiveerd door accountactiviteiten.

### Gebeurtenissen en beperkingen

| Gebeurtenis | Restricties |
| ----- | ----------- |
| [!UICONTROL Account had interesting moment] | Het type (E-mail, Mijlsteen, of Web) <br/> Extra beperkingen (facultatief): <li>Beschrijving</li><li>Bron</li><li>Datum van activiteit</li> <br/> Onderbreking (facultatief) |
| [!UICONTROL Change in Account Data Value] | Kenmerk <br/> Extra beperkingen (facultatief): <li>Nieuwe waarde</li><li>Vorige waarde</li><li>Datum van activiteit</li> <br/> Onderbreking (facultatief) |
| [!UICONTROL Change in Buying Group Stage] | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe fase</li><li>Vorige fase</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| [!UICONTROL Change in Buying Group Status] | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe status</li><li>Vorige status</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| [!UICONTROL Change in Completeness Score] | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe score</li><li>Vorige score</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| [!UICONTROL Change in Engagement Score] | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe score</li><li>Vorige score</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |

### Een accountgebeurtenis toevoegen

1. Navigeer naar de reiskaart.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Listen for an event]** .

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL Accounts]** voor het gebeurtenistype.

   ![ knoop van de Reis - luister aan gebeurtenissen op rekening ](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Selecteer een gebeurtenis in de lijst.

1. Klik op **[!UICONTROL Edit event]** en definieer details voor de gebeurtenis.

## Gebeurtenissen van Mensen

Luister naar een gebeurtenis op basis van mensen wanneer u de account op de reis vooruit wilt laten gaan volgens gebeurtenissen die worden geactiveerd door activiteiten van personen. U kunt gebeurtenissen ook filteren op basis van kenmerken van personen,

### Gebeurtenissen en beperkingen

| Invoertype | Gebeurtenis | Restricties |
| ---------- | ----- | ----------- |
| Journey Optimizer B2B | [!UICONTROL Assigned to Buying Group] | De rente van de oplossing <br/><br/> Aanvullende beperkingen (facultatief): <li>Functie</li><li>Datum van activiteit</li><br/> Onderbreking (facultatief) |
| | [!UICONTROL Clicks link in email] | E-mail <br/><br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Koppelings-id</li><li>Is een mobiel apparaat</li><li>Apparaat</li><li>Platform</li><li>Browser</li><li>Is voorspelbare inhoud</li><li>Is beide activiteit</li><li>Bot-activiteitspatroon</li><li>Browser</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | [!UICONTROL Clicks link in SMS] | E-mail <br/><br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Apparaat</li><li>Platform</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | [!UICONTROL Data value changes] | De attributen van de persoon <br/><br/> Aanvullende beperkingen (facultatief): <li>Nieuwe waarde</li><li>Vorige waarde</li><li>Reden</li><li>Bron</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | [!UICONTROL Opens email] | E-mail <br/><br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Koppelings-id</li><li>Is een mobiel apparaat</li><li>Apparaat</li><li>Platform</li><li>Browser</li><li>Is voorspelbare inhoud</li><li>Is beide activiteit</li><li>Bot-activiteitspatroon</li><li>Browser</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | [!UICONTROL Removed from Buying Group] | De rente van de oplossing <br/> Datum van activiteit (facultatief) <br/> (facultatieve) Onderbreking |
| | [!UICONTROL Score is changed] | De naam van de score <br/><br/> Aanvullende beperkingen (facultatief):<li>Wijzigen</li><li>Nieuwe score</li><li>Urgentie</li><li>Prioriteit</li><li>Relatieve score</li><li>Relatieve urgentie</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | [!UICONTROL SMS Bounces] | Het bericht van SMS <br/><br/> Aanvullende beperkingen (facultatief): <li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| Marketo Engage | [!UICONTROL Visits Web Page] | Webpagina <br/> Selecteer een of meer overeenkomende Marketo Engage-pagina&#39;s. <br/><br/> Extra beperkingen (facultatief): <li>Querystring</li><li>IP-adres client</li><li>Referenter</li><li>Gebruikersagent</li><li>Zoekmachine</li><li>Zoekquery</li><li>Token</li><li>Browser</li><li>Platform</li><li>Apparaat</li><li>Datum van activiteit</li> |
| | [!UICONTROL Fills out form] | Formulier <br/> Selecteer een of meer Marketo Engage-formulieren die met elkaar overeenkomen. <br/><br/> Extra beperkingen (facultatief): <li>Datum van activiteit</li><li>Querystring</li><li>IP-adres client</li><li>Referenter</li><li>Gebruikersagent</li><li>Platform</li><li>Apparaat</li><br/> Onderbreking (facultatief) |
| Adobe Experience Platform | [!UICONTROL Event definition] | Het type van gebeurtenis <br/><br/> Aanvullende beperkingen (facultatief): <li>Velden</li> <br/> Extra beperkingen (niet gesteund): <li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Time-out (optioneel) |

### Gebeurtenisfilters Personen

| Filters | Beschrijving |
| ------------ | ----------- |
| [!UICONTROL Activity history] > [!UICONTROL Email] | E-mailactiviteiten die zijn gebaseerd op voorwaarden die zijn geëvalueerd aan de hand van een of meer geselecteerde e-mailberichten van eerder in de reis: <li>[!UICONTROL Clicked link in email] <li>E-mail geopend <li>Is per e-mail verzonden <li>Is per e-mail verzonden <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the email activity).--> |
| [!UICONTROL Activity history] > [!UICONTROL SMS Message] | De activiteiten van SMS die op voorwaarden worden gebaseerd die gebruikend één of meerdere geselecteerde SMS berichten van vroeger in de reis worden geëvalueerd: <li>[!UICONTROL Clicked link in SMS] <li>[!UICONTROL SMS Bounced] <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the SMS activity). --> |
| [!UICONTROL Activity history] > [!UICONTROL Data Value Changed] | Voor een geselecteerd persoonkenmerk is een waardewijziging opgetreden. Deze wijzigingstypen zijn onder meer: <li>Nieuwe waarde<li>Vorige waarde<li>Reden<li>Bron<li>Datum van activiteit<li>Min. aantal keren <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have a data value change). --> |
| [!UICONTROL Activity history] > [!UICONTROL Had Interesting Moment] | Interesserende momentactiviteit die in de bijbehorende instantie van Marketo Engage wordt bepaald. Beperkingen zijn: <li>Mijlsteen<li>E-mail<li>Web <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have an interesting moment).--> |
| [!UICONTROL Activity history] > [!UICONTROL Visited web page] | Webpaginageactiviteit die voor een of meer webpagina&#39;s wordt beheerd door de bijbehorende Marketo Engage-instantie. Beperkingen zijn: <li>Webpagina (vereist)<li>Datum van activiteit<li>IP-adres client <li>Querystring <li>Referenter <li>Gebruikersagent <li>Zoekmachine <li>Zoekquery <li>Persoonlijke URL <li>Token <li>Browser <li>Platform <li>Apparaat <li>Min. aantal keren <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not visit the web page). --> |
| [!UICONTROL Person Attributes] | Attributen van het profiel van de persoon, met inbegrip van: <li>Stad <li>Land <li>Geboortedatum <li>E-mailadres <li>E-mail is ongeldig <li>E-mail is geschorst <li>Voornaam <li>Overgenomen deelstaatgebied<li>Functie <li>Achternaam <li>Mobiel telefoonnummer <li>Persoonlijke betrokkenheidsscore <li>Telefoonnummer <li>Postcode <li>Staat <li>Niet geabonneerd <li>Reden waarop geen abonnement is genomen |
| [!UICONTROL Special filters] > [!UICONTROL Member of Buying Group] | De persoon is al dan niet lid van de koopgroep, beoordeeld aan de hand van een of meer van de volgende criteria: <li>Belang van oplossing</li><li>Status van kopersgroep</li><li>Complete score</li><li>Engagement Score</li><li>Functie</li> |
| [!UICONTROL Special filters] > [!UICONTROL Member of List] | De persoon is al dan niet lid van een of meer Marketo Engage-lijsten. |
| [!UICONTROL Special filters] > [!UICONTROL Member of Program] | De persoon is al dan niet lid van een of meer Marketo Engage-programma&#39;s. |

### Een gebeurtenis Personen toevoegen

1. Navigeer naar de reiskaart.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Listen for an event]** .

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor het gebeurtenistype.

   ![ knoop van de Reis - luister aan gebeurtenissen op mensen ](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Selecteer een gebeurtenis in de lijst.

1. Klik op **[!UICONTROL Edit event]** en definieer details voor de gebeurtenis.

### Luisteren naar een Marketo Engage-gebeurtenis

Als u webpagina&#39;s hebt in een Marketo Engage-exemplaar dat is verbonden, kunt u een gebeurtenis activeren op basis van een bezoek aan of geen bezoek aan deze webpagina&#39;s en Marketo Engage-formulieren die niet zijn ingevuld.

1. Selecteer een knooppunt **[!UICONTROL Listen for an event]** in het reisoverzicht.

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor het gebeurtenistype.

1. Klik op de pijl voor de **[!UICONTROL Select people event]** -kiezer en schuif het menu naar de **[!UICONTROL Marketo Engage]** -sectie.

1. Selecteer een type van Markt-activiteit:

   * **[!UICONTROL Visits Web Page]**.
   * **[!UICONTROL Fills Out Form]**

   ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Edit event]** en definieer een of meer webpagina&#39;s die moeten overeenkomen en eventuele extra beperkingen voor de gebeurtenis.

   * (Vereist) Definieer in het dialoogvenster _[!UICONTROL Edit event]_de **[!UICONTROL Web page]**- of **[!UICONTROL Fills out form]**-beperking. Gebruik **[!UICONTROL is]**(standaardwaarde) om overeen te komen op een of meer geselecteerde pagina&#39;s of formulieren. Gebruik **[!UICONTROL is not]**om overeen te komen op alle paginabezoeken/formulieren, met uitzondering van een of meer geselecteerde pagina&#39;s/formulieren. Of gebruik **[!UICONTROL is any]**om een overeenkomst te bereiken op een bezoek of ingevuld formulier op een Marketo Engage-webpagina.

   * (Optioneel) Klik op **[!UICONTROL Add constraint]** en kies het veld dat u voor de restrictie wilt gebruiken. Stel de operator en de waarde voor het veld in.

     ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     U kunt deze actie herhalen om extra gebiedsbeperkingen te omvatten zoals nodig.

   * Indien nodig, selecteer het **[!UICONTROL Filters]** lusje aan [ voegt filters voor de gebeurtenis ](#add-a-filter-to-the-people-event) toe.

   * Klik op **[!UICONTROL Done]** wanneer de beperkingen en filters zijn gedefinieerd.

1. Indien nodig, plaats de **[!UICONTROL Timeout]** optie om de tijdspanne te beperken om op de gebeurtenis (zie [ een onderbreking aan een gebeurtenisknoop ](#add-a-timeout-to-an-event-node) toevoegen) te luisteren.

1. Voeg in het reisoverzicht het volgende knooppunt toe dat moet worden uitgevoerd wanneer de gebeurtenis plaatsvindt.

### Luisteren naar een Experience Event

De beheerders kunnen op Adobe Experience Platform (AEP)-Gebaseerde gebeurtenisdefinities vormen, die Marketers toelaten om rekeningsreizen tot stand te brengen die aan [ de Gebeurtenissen van de Ervaring van AEP ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} reageren. Het gebruik van AEP Experience Events voor reizen in rekening is een proces in twee stappen:

1. [ creeer en publiceer een de gebeurtenisdefinitie van AEP ](../admin/configure-aep-events.md).

2. In een rekeningsreis, voeg a _toe luistert naar een gebeurtenis_ knoop, en selecteert een de gebeurtenisdefinitie van Experience Platform voor een op mensen-gebaseerde gebeurtenis.

![ Video ](../../assets/do-not-localize/icon-video.svg) {width= &quot;30&quot;, verticaal-richt= &quot;midden&quot; [ bekijk het videooverzicht ](../admin/configure-aep-events.md#overview-video)

_Om een Gebeurtenis van de Ervaring in uw reis te omvatten :_

1. Selecteer een knooppunt **[!UICONTROL Listen for an event]** in het reisoverzicht.

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor het gebeurtenistype.

1. Klik op de pijl voor de **[!UICONTROL Select people event]** -kiezer en schuif het menu naar de **[!UICONTROL Adobe Experience Platform]** -sectie.

   ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Selecteer de gebeurtenis.

   Het gebeurtenistype wordt als leeg weergegeven in de details van het knooppunt.

   ![ geef de gebeurtenis ](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"} uit

1. Klik op **[!UICONTROL Edit event]** en definieer de gebeurtenistypen en eventuele extra beperkingen voor de gebeurtenis.

   * (Vereist) Definieer het gebeurtenistype in het dialoogvenster _[!UICONTROL Edit event]_. U kunt de operator **[!UICONTROL is]**default gebruiken om een of meer geselecteerde gebeurtenistypen overeen te laten komen. U kunt ook de operator **[!UICONTROL is not]**gebruiken om op alle gebeurtenistypen overeen te komen, met uitzondering van een of meer geselecteerde gebeurtenistypen.

   * (Optioneel) Klik op **[!UICONTROL Add constraint]** en kies het veld dat u voor de restrictie wilt gebruiken. Stel de operator en de waarde voor het veld in.

     ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >De beperkingen voor _datum van activiteit_ en _minimumaantal tijden_ worden niet gesteund.

     U kunt deze actie herhalen om extra gebiedsbeperkingen te omvatten zoals nodig.

   * Indien nodig, selecteer het **[!UICONTROL Filters]** lusje aan [ voegt filters voor de gebeurtenis ](#add-a-filter-to-the-people-event) toe.

   * Klik op **[!UICONTROL Done]** wanneer de beperkingen en filters zijn gedefinieerd.

1. Indien nodig, plaats de **[!UICONTROL Timeout]** optie om de tijdspanne te beperken om op de gebeurtenis (zie [ een onderbreking aan een gebeurtenisknoop ](#add-a-timeout-to-an-event-node) toevoegen) te luisteren.

1. Voeg in het reisoverzicht het volgende knooppunt toe dat moet worden uitgevoerd wanneer de gebeurtenis plaatsvindt.

1. Voltooi de resterende knopen voor uw reis en [ publiceer het ](./journey-overview.md).

   Wanneer de reis (gepubliceerd) levend is en _bereikt luistert naar een gebeurtenis_ knoop, begint het luisteren naar de Gebeurtenissen van de Ervaring van AEP.

### Filters toevoegen aan de gebeurtenis people

1. Nadat u de gebeurtenis hebt gedefinieerd, selecteert u de tab **[!UICONTROL Filters]** in het dialoogvenster _[!UICONTROL Edit Event]_.

   ![ luistert naar de knoop van de Gebeurtenis door mensen - Uitgezochte het lusje van Filters voor het uitgeven van de gebeurtenis ](./assets/node-listen-event-people-edit-event-filters.png){width="700" zoomable="yes"}

1. Voeg een of meer filters toe om de personen voor de gebeurtenis als doel in te stellen.

   * De belemmering en laat vallen om het even welke [ personenfilters ](#people-event-filters) van de linkernavigatie en voltooien de gelijke definitie.

     >[!NOTE]
     >
     >Als u aangepaste persoonvelden hebt gedefinieerd in het accountpublieksschema in Experience Platform, zijn deze velden ook beschikbaar onder **[!UICONTROL Attributes]** voor gebruik als persoonkenmerken in filters.

   * Verfijn uw filter door **[!UICONTROL Filter logic]** bij de bovenkant toe te passen. U kiest ervoor om alle filters of een filter aan te passen.

     ![ de filters van de Persoon die in een gebeurtenisdefinitie ](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} worden gebruikt

   * Klik op **[!UICONTROL Done]**.

## Een time-out toevoegen aan een gebeurtenisknooppunt

Indien nodig, bepaal de hoeveelheid tijd de reis op de gebeurtenis wacht. De reis eindigt na een onderbreking tenzij u een onderbrekingspad bepaalt, waar u andere knopen kunt toevoegen.

1. Schakel de optie **[!UICONTROL Timeout]** in.

1. Selecteer de duur gedurende welke de reis op een gebeurtenis wacht om voor het uit te komen.

   U kunt ervoor kiezen om het pad hier te beëindigen of een andere actie uit te voeren door een ander pad in te stellen.

1. Schakel het selectievakje **[!UICONTROL Set timeout path]** in als u een nieuw pad wilt maken in de reis waar u acties en gebeurtenissen kunt toevoegen die van toepassing zijn op accounts wanneer de gebeurtenis niet plaatsvindt.

   ![ de gebeurtenisknoop van de Reis - vastgestelde onderbrekingspad ](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Video over overzicht

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on)
