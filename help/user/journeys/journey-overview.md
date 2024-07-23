---
title: Accountreizen
description: Leer meer over accountreizen en hoe u deze kunt maken en beheren.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 59407f21319ff1b84e4fd001c4e92cfff61c57c9
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---


# Accountreizen

Bepaal verkoop-gedreven overeenkomst die e-mail, SMS, en meer binnenrekeningreizen omvat om binnenkomende marketing met uitgaande verkoopactiviteiten voor elk het kopen groepslid te coördineren.

## Accountreizen openen en doorbladeren

1. Klik op de startpagina van Adobe Experience Platform op Adobe Journey Optimizer B2B Edition.

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

U kunt de weergegeven tabel aanpassen door te klikken op het pictogram Kolommen in de rechterbovenhoek en de selectievakjes te selecteren of te wissen.

![ kies de kolommen in de lijst van de rekenentransporten ](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"} te tonen

## Anatomie van een rekeningreis

Klik op de naam (weergegeven als een koppeling) in de lijst van _[!UICONTROL Account journeys]_om de details te bekijken, wijzigingen aan te brengen en handelingen uit te voeren.

![ de werkruimte van de de reisreis van de Rekening ](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

De kopbal van de redacteur van elke reis omvat:

* Naam reis
* Mogelijkheid om de naam uit te geven (_geeft_ pictogram uit)
* Status van de reis

De volgende acties zijn beschikbaar in de koptekst:

* **Publish** - u kunt een reis publiceren als er geen blocker fouten zijn. Wanneer gepubliceerd, verandert de status van een Reis in _Levend_. Als de rit fouten bevat, wordt de knop grijs weergegeven met de inhoudsgegevens: `Resolve errors before publishing` .
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

### Voeg het accountpubliek toe voor uw reis

Een accountreis begint altijd met Accountpubliek waar u input kunt toevoegen aan uw reis.

1. Klik op het knooppunt **[!UICONTROL Account audience]** om de knoopeigenschappen aan de rechterkant weer te geven.

   ![ de publieksknoop van de Rekening ](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Add account audience]**.

   U kunt een publiekssegment selecteren dat eerder is geselecteerd door op _[!UICONTROL Add audiences]_te klikken.

1. Als u een nieuw publiekssegment wilt maken, selecteert u **[!UICONTROL Account audiences]** in de linkernavigatie.

1. Klik **[!UICONTROL Create audience]** en volg de stappen die in de [ gids van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences) worden beschreven {target="_blank"}.

### Bouwstenen van een reis

Het _wegcanvas_ is de centrale streek in de reisontwerper. Het is in deze streek dat u reisknopen kunt toevoegen en hen vormen. Klik op een knooppunt om het deelvenster met eigenschappen rechts van het canvas te openen en stel de eigenschappen in op basis van uw ontwerp.

U kunt uw reis bouwen gebruikend om het even welk van deze knooptypes:

* [Luisteren naar een gebeurtenis](journey-nodes.md#listen-for-an-event)
* [Handeling uitvoeren](journey-nodes.md#take-an-action)
* [Paden splitsen](journey-nodes.md#split-paths)
* [Wachten](journey-nodes.md#wait)
* [Paden samenvoegen](journey-nodes.md#merge-paths)

### Garrails

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

1. In de knoopeigenschappen op het recht, klik het _Schrapping_ (trashcan) pictogram.

1. Klik op **[!UICONTROL Delete]** in het dialoogvenster Conformatie.

### Een pad toevoegen en verwijderen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op het pad en voeg de gesplitste padnode toe.

1. Selecteer **[!UICONTROL Account]** in de knoopeigenschappen aan de rechterkant.

1. Klik op **[!UICONTROL Add path]** als u meer paden wilt toevoegen.

   Bij elk pad dat in de rit wordt gemaakt, wordt een nieuwe padkaart weergegeven in de eigenschappen.

1. Navigeer naar een van de paden in de rit en voeg actie- of gebeurtenisknooppunten toe aan dit pad met het plusteken.

1. Selecteer de gesplitste padnode om de eigenschappen aan de rechterkant te openen.

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
