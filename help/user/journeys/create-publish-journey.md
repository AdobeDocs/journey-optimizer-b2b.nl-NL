---
title: Een accountreis maken en publiceren
description: Leer hoe u accountreizen maakt en publiceert.
feature: Account Journeys
role: User
exl-id: f536b1a1-8dfe-437f-a84d-b66879529621
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Een accountreis maken en publiceren

Om met een rekeningreis te beginnen, creeer de reis en bouw dan de knopen en de reisstroom in de reiskaart.

![ Video ](../../assets/do-not-localize/icon-video.svg){width="30"} [ bekijk de overzichtsvideo ](#overview-video)

## Een accountreis maken

1. Klik in de linkernavigatie op **[!UICONTROL Account journeys]** .

1. Klik op **[!UICONTROL Create Account Journey]** rechtsboven op de pagina.

1. Voer in het dialoogvenster een uniek **[!UICONTROL Name]** (vereist) en **[!UICONTROL Description]** (optioneel) in.

   ![ creeer de dialoog van de Reis van de Rekening ](./assets/account-journey-create-dialog.png){width="400"}

1. Klik op **[!UICONTROL Create]**.

## Bouwstenen van een reis

De _reiskaart_ is de centrale streek in de reisontwerper. Het is in deze streek dat u reisknopen kunt toevoegen en hen vormen. Klik op een knooppunt om het deelvenster met eigenschappen rechts van het canvas te openen en stel de eigenschappen in op basis van uw ontwerp. Een rekeningsreis begint altijd met een [ knoop van het Publiek van de Rekening ](./account-audience-nodes.md) waar u input aan uw reis kunt toevoegen.

Nadat u een reis van de rekening creeert en het publiek toevoegt, bouwt de reis uit gebruikend knopen. De reiskaart verstrekt een canvas, waar u uw multi-step B2B het marketing gebruiksgevallen kunt bouwen gebruikend de volgende knooptypes om een rekeningsreis te construeren:

* [Handeling uitvoeren](./action-nodes.md)
* [Luisteren naar een gebeurtenis](./listen-for-event-nodes.md)
* [Paden splitsen](./split-merge-paths-nodes.md)
* [Wachten](./wait-nodes.md)
* [Paden samenvoegen](./split-merge-paths-nodes.md)

## Guardrails

Om u te helpen een reis bouwen zonder in fouten te lopen, zijn de volgende veiligheidstralen op zijn plaats:

* _het Schrappen van een Gesplitste wegknoop_: Het schrappen van een knoop vereist het schrappen van alle verdere knopen in elk weg.
* _het Schrappen van een knoop van de Fusie_: Een fusieknoop kan worden geschrapt slechts wanneer er één weg verbonden met het is. Als u een samenvoegknooppunt wilt verwijderen, laat u slechts één pad geselecteerd.
* _Schakelt tussen rekening en mensen_: U kunt niet de selectie van rekeningen aan mensen veranderen zonder alle verdere knopen in elke weg te schrappen.

## Een knooppunt toevoegen

1. Navigeer naar de reiskaart.

1. Klik op de plusknop ( **+** ) op het pad en selecteer het knooppunttype.

1. Stel de knoopeigenschappen rechts in.

## Een knooppunt verwijderen

1. Navigeer naar de reiskaart.

1. In de knoopeigenschappen op het recht, klik _Schrapping_ ( ![ pictogram van de Schrapping ](../assets/do-not-localize/icon-delete.svg)) pictogram.

1. Klik op **[!UICONTROL Delete]** in het dialoogvenster Conformatie.

## Een pad toevoegen en verwijderen

1. Navigeer naar de reiskaart.

1. Klik plus ( **+**) pictogram op de weg en voeg de [ gespleten wegknoop ](./split-merge-paths-nodes.md#split-paths) toe.

1. Selecteer **[!UICONTROL Account]** in de knoopeigenschappen aan de rechterkant.

1. Klik op **[!UICONTROL Add path]** als u meer paden wilt toevoegen.

   Bij elk pad dat in de rit wordt gemaakt, wordt een nieuwe padkaart weergegeven in de eigenschappen.

1. Navigeer aan één van de wegen in de reis en voeg [ actie ](./action-nodes.md) of [ gebeurtenis ](./listen-for-event-nodes.md) knopen aan deze weg toe gebruikend het plus pictogram.

1. Selecteer de [ gespleten weg ](./split-merge-paths-nodes.md) knoop om de eigenschappen op het recht te openen.

   De paden met knooppunten kunnen niet worden verwijderd.

1. Als u deze paden wilt verwijderen, moet u eerst alle knooppunten op dat pad verwijderen.

## Een reis plannen

Wanneer u een reis publiceert, kan het onmiddellijk of op een geplande toekomstige datum beginnen. De einddatum mag maximaal drie jaar na de begindatum zijn. Nadat een reis wordt gepubliceerd (_Levende_ status), kunt u de einddatum van de reis maar niet de begindatum bijwerken.

1. Navigeer naar de reiskaart.

1. Plan uw reis door **[!UICONTROL Journey settings]** in de kopbal te klikken.

1. Stel in het dialoogvenster de planningsopties in:

   * Kies een type schema.

     Kies **[!UICONTROL Immediately]** als u de rit tijdens het publiceren wilt activeren.

     Om de reis op een toekomstige datum te activeren, verkies **[!UICONTROL On a specific date]** en klik het _pictogram van de Kalender_ om de datum te selecteren.

     ![ de instellingendialoog van de Reis ](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Geef de **[!UICONTROL End date]** voor de rit op. Deze kan maximaal drie jaar na de begindatum zijn (dit veld moet worden gepubliceerd).

1. Klik op **[!UICONTROL Save]**.

   Wanneer u klaar bent om uw reis te publiceren, kunt u deze montages herzien wanneer u _[!UICONTROL Publish]_klikt.

## Een accountreis publiceren

U kunt een reis publiceren als er geen blocker fouten zijn. Wanneer gepubliceerd, verandert de reisstatus in _Levend_. Als de rit fouten bevat, wordt de knop _[!UICONTROL Publish]_grijs weergegeven met de inhoudsgegevens: `Resolve errors before publishing` .

1. Klik in de rechterbovenhoek van het reisoverzicht op **[!UICONTROL Publish]** .

1. Stel in het dialoogvenster _[!UICONTROL Review journey settings]_de startopties voor de rit in.

   Als u reeds de reismontages plaatst om een programma te bepalen, herzie de montages.

   Als u de activering van de reis moet instellen, kiest u een type schema:

   * Kies **[!UICONTROL Immediately]** als u de rit tijdens het publiceren wilt activeren.

   * Om de reis op een toekomstige datum te activeren, verkies **[!UICONTROL On a specific date]** en klik het _pictogram van de Kalender_ om de datum te selecteren.

1. Geef indien nodig de **[!UICONTROL End date]** voor de rit op.

   ![ de instellingendialoog van de Reis ](./assets/journey-publish-dialog.png){width="400" zoomable="no"}

   Deze kan maximaal drie jaar na de begindatum zijn (dit veld moet worden gepubliceerd).

1. Klik op **[!UICONTROL Next]**.

1. Klik op **[!UICONTROL Publish]** in het bevestigingsdialoogvenster.

## Video over overzicht

>[!VIDEO](https://video.tv.adobe.com/v/3443204/?learn=on)
