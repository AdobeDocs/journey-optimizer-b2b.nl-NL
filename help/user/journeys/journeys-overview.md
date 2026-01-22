---
title: Reisbeheer
description: Stroomlijn het genereren van de vraag met reizen - creeer, publiceer, beheer het kopen groepbetrokkenheid over e-mail, SMS, en gebeurtenissen in Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 6511f40329df34db665ed6f971fa20670be0ae32
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---


# Reisbeheer

In Journey Optimizer B2B edition zijn ritten geautomatiseerd, meerstappenplan voor accounts en marketingplannen op basis van leads waarmee gepersonaliseerde ervaringen via verschillende kanalen worden geordend als reactie op afspraken, zakelijke gebeurtenissen of geplande campagnes. Bepaal verkoop-gedreven overeenkomst die e-mail, SMS, en meer binnen omvat om binnenkomende marketing met uitgaande verkoopactiviteiten voor elk het kopen groepslid te coördineren.

Journey Optimizer B2B edition ondersteunt twee soorten reizen:

* **reizen van de Rekening** - stroomlijnt vraaggeneratie en het kopen groepskwalificatie en drijft meer gekwalificeerde vraag voor uw aankoop, upsell/cross-sell, en behoudprogramma&#39;s. Stuur uw reizen voor elke groep die objecten koopt en elk lid van de groep die deze koopt met automatische betrokkenheid over e-mail, SMS, gebeurtenissen en meer.

  ![&#x200B; Video &#x200B;](../../assets/do-not-localize/icon-video.svg){width="30"} [&#x200B; bekijk de video van het overzicht van de rekeningsreis &#x200B;](#overview-video)

* **de reizen van de Persoon** - (Beta) Orchestrate lood-gebaseerde marketing gebruikend het publiek en de gegevens van Experience Platform. Bij persoonlijke reizen zijn uw marketingactiviteiten niet afhankelijk van Marketo Engage of een oplossing voor Adobe Campaign/B2C-gereedschapsketens, zodat ze met B2B-gebruiksgevallen kunnen werken.

  Wanneer een reis per persoon in overleg met rekeningreizen en inkoopgroepen wordt gebruikt, kan deze de marketers de bevoegdheid geven om volledige orchestratie op de koopreis toe te passen.

  +++Huidige beperkingen voor personenreizen

  Er zijn beperkingen die bepaalde gebruiksgevallen kunnen blokkeren of die het moeilijk maken om persoonlijke reizen te maken. Veel problemen zijn het gevolg van de eerste bètaprogramma-implementatie, die in de toekomst moet worden aangepakt.

   * Gebeurtenissen kunnen niet met profielkenmerken worden gecombineerd om de publieksdefinities te beperken.
   * De context van de gebeurtenis die een profiel voor een reis kwalificeert, kan niet worden gebruikt voor personalisatie of orkest.
   * Voor reizen kunnen momenteel niet zowel de entry-criteria voor een gebeurtenis als het profielsegment worden gebruikt.
   * Gebeurtenislisteners kunnen niet luisteren naar meerdere gebeurtenissen.
   * De knopen van de wachttijd hebben momenteel geen volledige reeks opties voor dag van de week of de tijd van dag uitgangscriteria.
   * De e-maileditor verwijst onjuist naar mogelijkheden en kenmerken die alleen beschikbaar zijn voor accountreizen
   * De steun voor de tokens van de douanereis (_Mijn Tokens_) is nog niet beschikbaar.
   * Toevoegen aan en verwijderen uit persoonlijke reisknooppunten is momenteel niet beschikbaar voor beide soorten reizen.
   * Gebeurtenisgeschiedenis kan niet worden gebruikt voor orkestatie of personalisatie.
   * Verwante objecten (zoals account, inkoopgroep, opportuniteit en aangepaste objecten) kunnen niet worden gebruikt voor orchestratie of personalisatie.
   * Web-, SMS- en advertentieplatformkanalen worden momenteel niet ondersteund.

  +++

## Aan de slag met een reis

Aan de slag met je eerste reis:

1. [&#x200B; creeer een reis &#x200B;](./create-publish-journey.md#create-a-journey).
1. [&#x200B; voeg de knopen &#x200B;](./create-publish-journey.md#add-a-node) toe en [&#x200B; bepaal de reisstroom &#x200B;](./create-publish-journey.md#add-and-delete-a-path) in de reiskaart.
1. [&#x200B; publiceer de reis &#x200B;](./create-publish-journey.md#publish-a-journey).

## Uw reizen openen en doorbladeren

>[!BEGINTABS]

>[!TAB  reizen van de Rekening ]

Vouw **[!UICONTROL Journey Management]** uit in de linkernavigatie en klik op **[!UICONTROL Account journeys]** .

Ga tekst in het _hulpmiddel van het Onderzoek_ bij de bovenkant van de lijst in om de getoonde lijst door naam te filtreren.

![&#x200B; filter de lijst van de rekeningsreizen &#x200B;](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!TAB  Persoonlijke reizen (Beta) ]

[!BADGE Bèta]{type=Informative tooltip="Beschikbaar als bètafunctie op de vereenvoudigde architectuur"}

Vouw **[!UICONTROL Journey Management]** uit in de linkernavigatie en klik op **[!UICONTROL Person journeys]** .

Ga tekst in het _hulpmiddel van het Onderzoek_ bij de bovenkant van de lijst in om de getoonde lijst door naam te filtreren.

![&#x200B; filter de lijst van personenreizen &#x200B;](./assets/person-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!ENDTABS]

### Kolommen met reislijsten

De pagina met de lijst met ritten bevat de volgende kolommen:

* [!UICONTROL Name] (klik op de naam om de rit te openen voor bewerking)
* [!UICONTROL Status]
* [!UICONTROL Creation date]
* [!UICONTROL Created by]
* [!UICONTROL Last update]
* [!UICONTROL Last updated by]
* [!UICONTROL Published on]
* [!UICONTROL Published by]
* [!UICONTROL Start date]
* [!UICONTROL End date]

U kunt de lijst sorteren op _[!UICONTROL Status]_,_[!UICONTROL Creation date]_ of _[!UICONTROL Last update]_&#x200B;door op de kolomkop te klikken.

Om (toon/verberg) de kolommen aan te passen die in de lijst worden getoond, klik _aanpassen lijst_ ( ![&#x200B; aanpassen lijst &#x200B;](../assets/do-not-localize/icon-column-settings.svg) ) pictogram in de hoger-juiste hoek. Schakel de selectievakjes in het dialoogvenster in of uit en klik op **[!UICONTROL Apply]** .

![&#x200B; kies de kolommen in de reislijst &#x200B;](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"} te tonen

### Reisstatus

De status van een reis kan veranderen op basis van de acties die u toepast. Gebaseerd op de status van een reis, zijn bepaalde acties niet beschikbaar van de rechterkant van de kopbal.

| Status | Beschrijving | Beschikbare acties |
| ------ | ----------- | ----------------- |
| _&#x200B;**Ontwerp**&#x200B;_ | Een niet-gepubliceerde reis die bewerkbaar is. | <li>[&#x200B; publiceer &#x200B;](./create-publish-journey.md#publish-a-journey)<li>[&#x200B; Dupliceren &#x200B;](#duplicate-journey) <li>[&#x200B; Schrapping &#x200B;](#delete-journey) |
| _&#x200B;**Levend**&#x200B;_ | De statusveranderingen van de reis van _Ontwerp_ in _Levend_ wanneer een reis wordt gepubliceerd. In deze status kan het bestand niet meer worden bewerkt. | <li>[&#x200B; Dupliceren &#x200B;](#duplicate-journey)<li>[&#x200B; dicht aan nieuwe ingangen &#x200B;](#close-to-new-entries) <li>[&#x200B; afbreken &#x200B;](#abort-journey) |
| _&#x200B;**Gesloten aan nieuwe ingangen**&#x200B;_ | De veranderingen van de reisstatus van _Levend_ in _Gesloten aan nieuwe ingangen_ wanneer u [!UICONTROL Close to new entries] in de hoogste navigatie klikt. | <li>[&#x200B; Dupliceren &#x200B;](#duplicate-journey) <li>[&#x200B; afbreken &#x200B;](#abort-journey) |
| _&#x200B;**Geaborteerd**&#x200B;_ | De statusveranderingen van de reis van _Levend_ of _Gesloten aan nieuwe ingangen_ wanneer u een reis afbreekt. Een afgebroken reis kan niet opnieuw worden gestart. | <li>[&#x200B; Dupliceren &#x200B;](#duplicate-journey) <li>[&#x200B; Schrapping &#x200B;](#delete-journey) |
| _&#x200B;**Voltooid**&#x200B;_ | Wanneer al rekening of de leden van het persoonpubliek in een reis de reis voltooien, verandert de status van _Levend_ of _Gesloten aan nieuwe ingangen_ aan _Voltooid_. | <li>[&#x200B; Dupliceren &#x200B;](#duplicate-journey) <li>[&#x200B; Schrapping &#x200B;](#delete-journey) |

## Reiskaarten

Klik op de naam (weergegeven als een koppeling) in de lijst met ritten om de details te bekijken, wijzigingen aan te brengen en acties te ondernemen.

![&#x200B; de werkruimte van de de reisreis van de Rekening &#x200B;](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

De koptekst van elke reiskaart omvat:

* Naam reis
* Bewerk hulpmiddel voor de reisnaam ( ![&#x200B; geeft pictogram &#x200B;](../assets/do-not-localize/icon-edit.svg) uit __ pictogram uitgeeft)
* [&#x200B; Status &#x200B;](#journey-status) van de reis

Van de reiskaart, kunt u [&#x200B; toevoegen de knopen &#x200B;](./create-publish-journey.md#add-a-node) en [&#x200B; de reisstroom &#x200B;](./create-publish-journey.md#add-and-delete-a-path) bepalen.

## Reisacties

De pagina met de lijst met reizen bevat alle accounts of persoonlijke reizen in uw Journey Optimizer B2B edition-exemplaar. Vanuit de lijstpagina kunt u een aantal acties op een reis toepassen.

### Reis afbreken

Als u een live of geplande reis afbreekt (stopt), stoppen rekeningen of mensen op de reis onmiddellijk hun voortgang en kunnen er geen verdere reizen meer plaatsvinden. Een afgebroken reis kan niet opnieuw worden gestart.

>[!IMPORTANT]
>
>Wanneer de reis in een andere reis van a _wordt gebruikt neem een actie_ knoop met de _[!UICONTROL Add Account to (other) Journey]_&#x200B;actie, die de wegblokkades aborteert die actie in die reis.

1. Klik op de naam van de reis om deze te openen.

1. Klik op het menu **[!UICONTROL More...]** rechtsboven en kies **[!UICONTROL Abort]** .

   ![&#x200B; klik meer bij het hoogste recht &#x200B;](./assets/account-journey-live-more-menu.png){width="450"}

1. Klik op **[!UICONTROL Abort]** in het bevestigingsdialoogvenster.

### Sluiten met nieuwe items

Als je een live reis afsluit, gaan de rekeningen die op dit moment op reis zijn, door op die reis en kan er geen verdere reis plaatsvinden. Een gesloten reis kan niet opnieuw worden gestart. U kunt een gesloten reis dupliceren.

>[!IMPORTANT]
>
>Wanneer de reis in een andere reis van a _wordt gebruikt neem een actie_ knoop met de _[!UICONTROL Add Account to (other) Journey]_&#x200B;actie, die het sluit aan nieuwe ingangen blokkeert die actie van die reis.

1. Klik op de naam van de reis om deze te openen.

1. Klik op het menu **[!UICONTROL More...]** rechtsboven en kies **[!UICONTROL Close to new entries]** .

1. Klik op **[!UICONTROL Close to new entries]** in het bevestigingsdialoogvenster.

### Een reis dupliceren

Een dubbele actie is vergelijkbaar met een kloonfunctie, maar een gedupliceerde reis bevat geen gemaakte transportinhoudselementen. U kunt de details voor de reis, of enkel een eenvoudig _skelet_ van de stroom en wegstructuur dupliceren.

>[!NOTE]
>
>Deze actie is momenteel niet beschikbaar voor personenreizen.

1. Klik het _Meer_ pictogram (**..**) naast de reisnaam en kies **[!UICONTROL Duplicate]**.

   ![&#x200B; klik het... pictogram en kies Dupliceren &#x200B;](./assets/account-journeys-list-more-menu.png){width="450"}

   Afhankelijk van de status van de reis hebt u ook toegang tot de dubbele actie van de reisgegevens of de reiskaart:

   * Klik voor een conceptrit rechtsboven in het menu **[!UICONTROL More...]** en kies **[!UICONTROL Duplicate]** .

   * Voor alle andere reisstatussen klikt u op **[!UICONTROL Duplicate]** rechtsboven.

     ![&#x200B; klik Dupliceren bij het hoogste recht &#x200B;](./assets/account-journey-duplicate-button.png){width="450"}

1. In de _Dubbele dialoog van de Reis_, plaats **[!UICONTROL Name]** en **[!UICONTROL Description]** voor de nieuwe reis.

   Door gebrek, gebruikt de dialoog de naam van de gedupliceerde reis die met _ _wordt toegevoegd exemplaar_. Voer desgewenst een andere unieke naam voor de rit in.

   ![&#x200B; Dupliceer de dialoog van de Reis &#x200B;](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Kies de duplicatie **[!UICONTROL Type]** :

   * **[!UICONTROL Partial content duplication]** - Gebruik dit type om alles tijdens de reis te kopiëren, met uitzondering van gemaakte e-mails of SMS-berichten. Nodes die verwijzen naar een Marketo Engage-bericht via e-mail of SMS, zijn volledig intact.

   * **[!UICONTROL Duplicate without details]** - Met dit type kopieert u alleen de knooppuntstructuur en -paden. Alle knoopmontages en wegvoorwaarden zijn undefined (gebrek), zodat u de basisstroom met verschillende publiek, acties, en de montages van de wegsegmentatie kunt opnieuw gebruiken. Al _wacht_ knopen gebruiken het gebrek van vijf dagen.

1. Klik op **[!UICONTROL Duplicate]**.

   De gedupliceerde reis wordt geopend in de reiskaart, waar u de details kunt plaatsen en reis inhoud tot stand kunt brengen zoals nodig.

### Een rit verwijderen

Gebruik een verwijderactie om een reis permanent te verwijderen. U kunt een live of geplande reis niet verwijderen.

1. Klik het _Meer_ pictogram (**..**) naast de reisnaam en kies **[!UICONTROL Delete]**.

   Afhankelijk van de status van de reis hebt u ook toegang tot de verwijderactie van de reisgegevens of de reiskaart:

   * Klik voor een conceptrit rechtsboven in het menu **[!UICONTROL More...]** en kies **[!UICONTROL Delete]** .

   * Voor andere reisstatussen, zoals _Voltooid_ of _Geaborteerd_, klik **[!UICONTROL Delete]** bij het hoogste recht.

1. Klik op **[!UICONTROL Delete]** in het bevestigingsdialoogvenster.

## Voortgang van account controleren

Voor een gepubliceerde rekeningsreis die in a _Levend_ is, _Gesloten aan nieuwe ingangen_, _Geaborteerd_, of _Voltooide_ status, kunt u de reiskaart openen om de rekeningsvooruitgang voor de vervoerknopen te herzien. Elk knooppunt op de kaart geeft het aantal accounts weer dat dat knooppunt moet bereiken en, voor live reizen, het aantal accounts dat zich momenteel op dat knooppunt bevindt.

![&#x200B; de informatie van de de rekeningsprogressie van de de knooppuntrekening van de Reis &#x200B;](./assets/node-account-progression-observability.png){width="400"}

Wanneer u de knoop selecteert, klik het aantal om een lijst van rekeningen te bekijken die de knoop ingegaan of momenteel bij die stap van de reis zijn.

![&#x200B; de informatie van de de rekeningsprogressie van de de knooppuntrekening van de Reis &#x200B;](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Video over reisoverzicht van accounts {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443213/?captions=dut&learn=on)
