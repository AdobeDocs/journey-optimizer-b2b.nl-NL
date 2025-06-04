---
title: Rekeningreizen
description: Ga aan de slag met uw accountritten en leer hoe u deze kunt beheren met de lijst Accountreizen.
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: a67ab8268676050f0c5f34b94d4aebfd46aaf601
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---


# Accountreizen

Met accountreizen kunt u de productie van vraag stroomlijnen en groepskwalificatie kopen en een meer gekwalificeerde vraag naar uw aankoop-, upsell- en retentieprogramma&#39;s stimuleren. Stuur uw reizen voor elke groep die objecten koopt en elk lid van de groep die deze koopt met automatische betrokkenheid over e-mail, SMS, gebeurtenissen en meer.

Bepaal verkoop-gedreven overeenkomst die e-mail, SMS, en meer binnenrekeningreizen omvat om binnenkomende marketing met uitgaande verkoopactiviteiten voor elk het kopen groepslid te coördineren.

![ Video ](../../assets/do-not-localize/icon-video.svg){width="30"} [ bekijk de overzichtsvideo ](#overview-video)

## Aan de slag met een reis

Ga als volgt te werk om aan de slag te gaan met reizen:

1. [ creeer een reis ](./create-publish-journey.md#create-an-account-journey).
1. [ voeg de knopen ](./create-publish-journey.md#add-a-node) toe en [ bepaal de reisstroom ](./create-publish-journey.md#add-and-delete-a-path) in de reiskaart.
1. [ publiceer de reis ](./create-publish-journey.md#publish-an-account-journey).

## Accountreizen openen en doorbladeren

Vouw **[!UICONTROL Account Management]** uit in de linkernavigatie en klik op **[!UICONTROL Account journeys]** .

Ga tekst in het _hulpmiddel van het Onderzoek_ bij de bovenkant van de lijst in om de getoonde lijst door naam te filtreren.

![ filter de lijst van de rekeningsreizen ](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

De lijstpagina _[!UICONTROL Account Journeys]_&#x200B;bevat de volgende kolommen:

* [!UICONTROL Name] (klik op de naam om de rit te openen voor bewerking)
* [!UICONTROL Status]
* [!UICONTROL Description]
* [!UICONTROL Created by]
* [!UICONTROL Last updated at]
* [!UICONTROL Last updated by]
* [!UICONTROL Published on]
* [!UICONTROL Published by]

U kunt de lijst sorteren door _[!UICONTROL Status]_&#x200B;te klikken op de kolomkop.

U kunt de kolommen aanpassen die in de lijst door _worden getoond te klikken aanpassen lijst_ ( ![ aanpassen lijst ](../assets/do-not-localize/icon-column-settings.svg)) pictogram in de hoger-juiste hoek. Schakel de selectievakjes in het dialoogvenster in of uit en klik op **[!UICONTROL Apply]** .

![ kies de kolommen in de lijst van de rekenentransporten ](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"} te tonen

## Anatomie van een rekeningreis

Klik op de naam (weergegeven als een koppeling) in de lijst van _[!UICONTROL Account journeys]_&#x200B;om de details te bekijken, wijzigingen aan te brengen en handelingen uit te voeren.

![ de werkruimte van de de reisreis van de Rekening ](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

De koptekst van elk rekeningoverzicht bevat:

* Naam reis
* Bewerk hulpmiddel voor de reisnaam ( ![ geeft pictogram ](../assets/do-not-localize/icon-edit.svg) uit __ pictogram uitgeeft)
* Status van de reis

De status van een reis kan veranderen op basis van de acties die u toepast. Gebaseerd op de status van een reis, zijn bepaalde acties niet beschikbaar van de rechterkant van de kopbal.

| Status | Beschrijving | Beschikbare acties |
| ------ | ----------- | ----------------- |
| _&#x200B;**Ontwerp**&#x200B;_ | Een niet-gepubliceerde reis die bewerkbaar is. | <li>[ publiceer ](./create-publish-journey.md#publish-an-account-journey)<li>[ Dupliceren ](#duplicate-journey) <li>[ Schrapping ](#delete-journey) |
| _&#x200B;**Levend**&#x200B;_ | De reisstatus verandert van Concept in Live wanneer een reis wordt gepubliceerd. In deze status kan het bestand niet meer worden bewerkt. | <li>[ Dupliceren ](#duplicate-journey)<li>[ dicht aan nieuwe ingangen ](#close-to-new-entries) <li>[ afbreken ](#abort-journey) |
| _&#x200B;**Gesloten aan nieuwe ingangen**&#x200B;_ | De veranderingen van de reisstatus van _Levend_ in _Gesloten aan nieuwe ingangen_ wanneer u [!UICONTROL Close to new entries] in de hoogste navigatie klikt. | <li>[ Dupliceren ](#duplicate-journey) <li>[ afbreken ](#abort-journey) |
| _&#x200B;**Geaborteerd**&#x200B;_ | De statusveranderingen van de reis van _Levend_ of _Gesloten aan nieuwe ingangen_ wanneer u een reis afbreekt. Een afgebroken reis kan niet opnieuw worden gestart. | <li>[ Dupliceren ](#duplicate-journey) <li>[ Schrapping ](#delete-journey) |
| _&#x200B;**Voltooid**&#x200B;_ | Wanneer alle rekeningen in een reis de reis voltooien, verandert de status van _Levend_ of _Gesloten aan nieuwe ingangen_ aan _Voltooid_. | <li>[ Dupliceren ](#duplicate-journey) <li>[ Schrapping ](#delete-journey) |

## Reizen beheren

De _Reizen van de Rekening_ lijst omvat alle reizen in uw instantie van Journey Optimizer B2B edition.

### Reis afbreken

Als u een live of geplande reis afbreekt (stopt), stoppen de accounts in de reis onmiddellijk hun voortgang en kunnen er geen verdere reizen meer plaatsvinden. Een afgebroken reis kan niet opnieuw worden gestart.

>[!IMPORTANT]
>
>Wanneer de rekeningsreis in een andere reis van a _wordt gebruikt neem een actie_ knoop met _voeg Rekening aan (andere) Reis_ actie toe, die de wegblokkades aborteert die actie in die reis.

1. Klik op de naam van de reis om deze te openen.

1. Klik op het menu **[!UICONTROL More...]** rechtsboven en kies **[!UICONTROL Abort]** .

   ![ klik meer bij het hoogste recht ](./assets/account-journey-live-more-menu.png){width="450"}

1. Klik op **[!UICONTROL Abort]** in het bevestigingsdialoogvenster.

### Sluiten met nieuwe items

Als je een live reis afsluit, gaan de rekeningen die op dit moment op reis zijn, door op die reis en kan er geen verdere reis plaatsvinden. Een gesloten reis kan niet opnieuw worden gestart. U kunt een gesloten reis dupliceren.

>[!IMPORTANT]
>
>Wanneer de rekeningsreis in een andere reis van a _wordt gebruikt neem een actie_ knoop met _voeg Rekening aan (andere) Reis_ actie toe, die het sluit aan nieuwe ingangsblokken die actie van die reis.

1. Klik op de naam van de reis om deze te openen.

1. Klik op het menu **[!UICONTROL More...]** rechtsboven en kies **[!UICONTROL Close to new entries]** .

1. Klik op **[!UICONTROL Close to new entries]** in het bevestigingsdialoogvenster.

### Reis dupliceren

Een dubbele actie is vergelijkbaar met een kloonfunctie, maar een gedupliceerde reis bevat geen gemaakte transportinhoudselementen. U kunt de details voor de rekeningsreis dupliceren, of enkel een eenvoudig _skelet_ van de stroom en weg structure.s

1. Klik het _Meer_ pictogram (**..**) naast de reisnaam en kies **[!UICONTROL Duplicate]**.

   ![ klik het... pictogram en kies Dupliceren ](./assets/account-journeys-list-more-menu.png){width="450"}

   Afhankelijk van de status van de accountreis kunt u ook de dubbele actie openen vanuit de reisgegevens of de reiskaart:

   * Klik voor een conceptrit rechtsboven in het menu **[!UICONTROL More...]** en kies **[!UICONTROL Duplicate]** .

   * Voor alle andere reisstatussen klikt u op **[!UICONTROL Duplicate]** rechtsboven.

     ![ klik Dupliceren bij het hoogste recht ](./assets/account-journey-duplicate-button.png){width="450"}

1. In de _Dubbele dialoog van de Reis_, plaats **[!UICONTROL Name]** en **[!UICONTROL Description]** voor de nieuwe reis.

   Door gebrek, gebruikt de dialoog de naam van de gedupliceerde reis die met _ _wordt toegevoegd exemplaar_. Voer desgewenst een andere unieke naam voor de rit in.

   ![ Dupliceer de dialoog van de Reis ](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Kies de duplicatie **[!UICONTROL Type]** :

   * **[!UICONTROL Partial content duplication]** - Gebruik dit type om alles tijdens de reis te kopiëren, met uitzondering van gemaakte e-mails of SMS-berichten. Nodes die verwijzen naar een Marketo Engage-bericht via e-mail of SMS, zijn volledig intact.

   * **[!UICONTROL Duplicate without details]** - Met dit type kopieert u alleen de knooppuntstructuur en -paden. Alle knoopmontages en wegvoorwaarden zijn undefined (gebrek), zodat u de basisstroom met verschillende publiek, acties, en de montages van de wegsegmentatie kunt opnieuw gebruiken. Al _wacht_ knopen gebruiken het gebrek van vijf dagen.

1. Klik op **[!UICONTROL Duplicate]**.

   De gedupliceerde accountreis wordt geopend in het reisoverzicht, waar u de details kunt instellen en zo nodig reisinhoud kunt maken.

### Reis verwijderen

Gebruik een verwijderactie om een reis permanent te verwijderen. U kunt een live of geplande reis niet verwijderen.

1. Klik het _Meer_ pictogram (**..**) naast de reisnaam en kies **[!UICONTROL Delete]**.

   Afhankelijk van de status van de accountreis kunt u ook de verwijderactie openen vanuit de reisgegevens of de reiskaart:

   * Klik voor een conceptrit rechtsboven in het menu **[!UICONTROL More...]** en kies **[!UICONTROL Delete]** .

   * Voor andere reisstatussen, zoals _Voltooid_ of _Geaborteerd_, klik **[!UICONTROL Delete]** bij het hoogste recht.

1. Klik op **[!UICONTROL Delete]** in het bevestigingsdialoogvenster.

## Video over overzicht

>[!VIDEO](https://video.tv.adobe.com/v/3443213/?learn=on&captions=dut)
