---
title: Rekeningreizen
description: Leer meer over accountreizen en hoe u deze kunt maken en beheren.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 279bc07b90da96c3d497f67a14596a3bed308984
workflow-type: tm+mt
source-wordcount: '1095'
ht-degree: 0%

---


# Accountreizen

Bouw en voer reizen uit die voor elke het kopen groep en het kopen groepslid worden gemaakt gebruikend geautomatiseerde betrokkenheid over e-mail, SMS, gebeurtenissen, en meer. Met accountreizen kunt u de productie van vraag en het kopen van groepskwalificaties stroomlijnen en een meer gekwalificeerde vraag naar uw aankoop-, upsell- en cross-sell-programma&#39;s stimuleren.

Bepaal verkoop-gedreven overeenkomst die e-mail, SMS, en meer binnenrekeningreizen omvat om binnenkomende marketing met uitgaande verkoopactiviteiten voor elk het kopen groepslid te coördineren.

## Accountreizen openen en doorbladeren

1. Klik op Adobe Journey Optimizer B2B edition op de startpagina van Adobe Experience Platform.

1. Klik in de linkernavigatie op **[!UICONTROL Account journeys]** .

   ![ de rekeningsreizen van de Toegang ](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   De weergegeven pagina voor ritten bevat de volgende kolommen:

   * [!UICONTROL Name] (klik op de naam om de accountreis te openen voor bewerking)
   * [!UICONTROL Status]
   * [!UICONTROL Description]
   * [!UICONTROL Created by]
   * [!UICONTROL Last updated at]
   * [!UICONTROL Last updated by]
   * [!UICONTROL Published on]
   * [!UICONTROL Published by]

Deze tabel bevat de mogelijkheid te zoeken op naam en is gemaakt door. Sorteren is momenteel niet beschikbaar.

U kunt de getoonde lijst aanpassen door het _pictogram van Kolommen_ in de hoger-juiste hoek te klikken en checkboxes te selecteren of te ontruimen.

![ kies de kolommen in de lijst van de rekenentransporten ](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"} te tonen

## Anatomie van een rekeningreis

Klik op de naam (weergegeven als een koppeling) in de lijst van _[!UICONTROL Account journeys]_om de details te bekijken, wijzigingen aan te brengen en handelingen uit te voeren.

![ de werkruimte van de de reisreis van de Rekening ](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

De koptekst van de editor voor elke accountreis bevat:

* Naam reis
* Mogelijkheid om de naam uit te geven (_geeft_ pictogram uit)
* Status van de reis

De volgende acties zijn beschikbaar in de koptekst:

* **Publish** - u kunt een reis publiceren als er geen blocker fouten zijn. Wanneer gepubliceerd, verandert de reisstatus in _Levend_. Als de rit fouten bevat, wordt de knop grijs weergegeven met de inhoudsgegevens: `Resolve errors before publishing` .
* **Dupliceer** - Deze actie is gelijkaardig aan een kloonfunctie, maar de gedupliceerde reis omvat geen activa.
* **dicht bij nieuwe ingangen** - als u een reis sluit, zetten de rekeningen momenteel in de reis hun weg in de reis voort en geen verdere reisingang kan gebeuren. Een gesloten reis kan niet opnieuw worden gestart. U kunt een gesloten reis dupliceren.
* **verlaat** - als u een reis tegenhoudt, de rekeningen in de reis onmiddellijk hun vooruitgang tegenhouden en geen verdere reisingang kan gebeuren. Een stopreis kan niet opnieuw worden gestart. Als je nieuwe ingangen blokkeert zonder de vooruitgang van mensen tegen te houden, kun je overwegen de reis te sluiten.
* **Schrapping** - Deze actie schrapt permanent de reis.

De status van een Reis verandert op basis van de acties die u toepast. Gebaseerd op de status van een reis, zijn bepaalde acties niet beschikbaar in de kopbal.

| Status | Beschrijving | Beschikbare acties |
| ------ | ----------- | ----------------- |
| _**Ontwerp**_ | Een niet-gepubliceerde reis die bewerkbaar is. | <ul><li>Publish</li><li>Dupliceren </li><li>Verwijderen </li></ul> |
| _**Levend**_ | De reisstatus verandert van Concept in Live wanneer een reis wordt gepubliceerd. In deze status kan het bestand niet meer worden bewerkt. | <ul><li>Dupliceren </li><li>Sluiten met nieuwe items </li><li>Afbreken </li></ul> |
| _**Gesloten aan nieuwe ingangen**_ | De veranderingen van de reisstatus van _Levend_ in _Gesloten aan nieuwe ingangen_ wanneer u [!UICONTROL Close to new entries] in de hoogste navigatie klikt. | <ul><li>Dupliceren </li><li>Afbreken </li></ul> |
| _**Geaborteerd**_ | De statusveranderingen van de reis van _Levend_ of _Gesloten aan nieuwe ingangen_ wanneer u een reis afbreekt. Een afgebroken reis kan niet opnieuw worden gestart. | <ul><li>Dupliceren </li><li>Verwijderen </li></ul> |
| _**Voltooid**_ | Wanneer alle accounts in een rit de rit hebben voltooid, verandert de status van Live of Gesloten in Nieuwe berichten in Voltooid. | <ul><li>Dupliceren </li><li>Verwijderen </li></ul> |

## Aan de slag met een reis

Om met een rekeningreis te beginnen, creeer de reis en bouw dan de knopen en de reisstroom in de reisredacteur.

### Een accountreis maken

1. Klik in de linkernavigatie op **[!UICONTROL Account journeys]** .

1. Klik op **[!UICONTROL Create Account Journey]** rechtsboven op de pagina.

1. Voer in het dialoogvenster een uniek **[!UICONTROL Name]** (vereist) en **[!UICONTROL Description]** (optioneel) in.

   ![ creeer de dialoog van de Reis van de Rekening ](./assets/account-journey-create-dialog.png){width="400"}

1. Klik op **[!UICONTROL Create]**.

### Bouwstenen van een reis

De _reiskaart_ is de centrale streek in de reisontwerper. Het is in deze streek dat u reisknopen kunt toevoegen en hen vormen. Klik op een knooppunt om het deelvenster met eigenschappen rechts van het canvas te openen en stel de eigenschappen in op basis van uw ontwerp. Een rekeningsreis begint altijd met een [ knoop van het Publiek van de Rekening ](./account-audience-nodes.md) waar u input aan uw reis kunt toevoegen.

Nadat u een reis van de rekening creeert en het publiek toevoegt, bouwt de reis uit gebruikend knopen. De reiskaart verstrekt een canvas, waar u uw multi-step B2B het marketing gebruiksgevallen kunt bouwen gebruikend de volgende knooptypes om een rekeningsreis te construeren:

* [Handeling uitvoeren](./action-nodes.md)
* [Luisteren naar een gebeurtenis](./listen-for-event-nodes.md)
* [Paden splitsen](./split-merge-paths-nodes.md)
* [Wachten](./wait-nodes.md)
* [Paden samenvoegen](./split-merge-paths-nodes.md)

### Guardrails

Om u te helpen een reis bouwen zonder in fouten te lopen, zijn de volgende veiligheidstralen op zijn plaats:

* _het Schrappen van een Gesplitste wegknoop_: U kunt geen knoop schrappen zonder alle verdere knopen in elk weg te schrappen.
* _het Schrappen van een knoop van de Fusie_: Een fusieknoop kan worden geschrapt slechts wanneer er één weg verbonden met het is. Als u een samenvoegknooppunt wilt verwijderen, laat u slechts één pad geselecteerd.
* _Schakelt tussen rekening en mensen_: U kunt niet de selectie van rekeningen aan mensen veranderen zonder alle verdere knopen in elke weg te schrappen.

### Een knooppunt toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op het pad en selecteer het knooppunttype.

1. Stel de knoopeigenschappen rechts in.

### Een knooppunt verwijderen

1. Navigeer naar de reiseditor.

1. In de knoopeigenschappen op het recht, klik _Schrapping_ ( ![ pictogram van de Schrapping ](../assets/do-not-localize/icon-delete.svg)) pictogram.

1. Klik op **[!UICONTROL Delete]** in het dialoogvenster Conformatie.

### Een pad toevoegen en verwijderen

1. Navigeer naar de reiseditor.

1. Klik plus ( **+**) pictogram op de weg en voeg de [ gespleten wegknoop ](./split-merge-paths-nodes.md#split-paths) toe.

1. Selecteer **[!UICONTROL Account]** in de knoopeigenschappen aan de rechterkant.

1. Klik op **[!UICONTROL Add path]** als u meer paden wilt toevoegen.

   Bij elk pad dat in de rit wordt gemaakt, wordt een nieuwe padkaart weergegeven in de eigenschappen.

1. Navigeer aan één van de wegen in de reis en voeg [ actie ](./action-nodes.md) of [ gebeurtenis ](./listen-for-event-nodes.md) knopen aan deze weg toe gebruikend het plus pictogram.

1. Selecteer de [ gespleten weg ](./split-merge-paths-nodes.md) knoop om de eigenschappen op het recht te openen.

   De paden met knooppunten kunnen niet worden verwijderd.

1. Als u deze paden wilt verwijderen, moet u eerst alle knooppunten op dat pad verwijderen.

### Een reis plannen

Wanneer u een reis publiceert, kan het onmiddellijk of op een geplande toekomstige datum beginnen. De einddatum mag maximaal drie jaar na de begindatum zijn. Nadat een reis wordt gepubliceerd (_Levende_ status), kunt u de einddatum van de reis maar niet de begindatum bijwerken.

1. Navigeer naar de reiseditor.

1. Plan uw reis door [!UICONTROL Journey settings] in de kopbal te klikken.

1. Stel in het dialoogvenster de planningsopties in:

   * Kies een type schema.

     Kies **[!UICONTROL Immediately]** als u de rit tijdens het publiceren wilt activeren.

     Om de reis op een toekomstige datum te activeren, verkies **[!UICONTROL On a specific date]** en klik het _pictogram van de Kalender_ om de datum te selecteren.

     ![ de instellingendialoog van de Reis ](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Geef de **[!UICONTROL End date]** voor de rit op. Deze kan maximaal drie jaar na de begindatum zijn (dit veld is verplicht).

1. Klik op **[!UICONTROL Save]**.

   Wanneer u klaar bent om uw reis te publiceren, kunt u deze montages herzien wanneer u _[!UICONTROL Publish]_klikt.

### Publish: een rekeningreis


