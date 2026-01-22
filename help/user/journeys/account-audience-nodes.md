---
title: Auditienoten account
description: Configureer de knooppunten voor het accountpubliek met accountsoorten of accountlijsten om de toegangspunten voor reizen voor doelgerichte organisatie in Journey Optimizer B2B edition te definiëren.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 2a676f3cbeb43616a75fa3fa6eb9106230b9fb40
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Transparante knooppunten voor het publiek

De knoop van het rekeningspubliek specificeert welke rekeningen de reis ingaan. Wanneer u [&#x200B; een rekeningsreis &#x200B;](./create-publish-journey.md#create-a-journey) creeert, begint de reis altijd met een knoop van het rekeningspubliek die zijn input bepaalt.

Gebruik een van de volgende invoeropties voor dit transportknooppunt:

* **[het publiek van de Rekening](../audiences/account-audience-overview.md)** - het rekeningspubliek vertegenwoordigt het basispubliek dat van de Dienst van de Segmentatie van Experience Platform synchroniseert.
* **[lijst van de Rekening](../accounts/account-lists.md)** — De rekeningslijst is een inzameling van genoemde rekeningen die u voor gerichte reisorchestratie gebruikt. Een accountlijst richt zich op benoemde accounts met behulp van gedefinieerde criteria, zoals de branche, locatie of bedrijfsgrootte.

## Het publiek voor het accountpubliek instellen

1. Klik op het knooppunt **[!UICONTROL Account audience]** . Deze actie toont de knoopeigenschappen op het recht.

   ![&#x200B; de wegknoop van de het publiek van de Rekening &#x200B;](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Kies het invoertype voor de accounts die de reis ingaan:

   * **[!UICONTROL Account audience]**

     Kies de optie voor het accountpubliek. Klik vervolgens op **[!UICONTROL Add account audience]** .

     Selecteer in het dialoogvenster _[!UICONTROL Add audience]_&#x200B;een eerder gemaakt publiekssegment. Klik vervolgens op **[!UICONTROL Add audience]**.

     ![&#x200B; selecteer een publiekssegment voor de knoop &#x200B;](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Account list]**

     Kies de optie voor de accountlijst. Klik op **[!UICONTROL Add account list]**.

     Selecteer een gepubliceerde accountlijst in het dialoogvenster _[!UICONTROL Select live account list]_. Klik vervolgens op **[!UICONTROL Save]**.

     ![&#x200B; selecteer een levende rekeningslijst voor de knoop &#x200B;](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Voor meer informatie over het creëren van en het publiceren van rekeningslijsten, zie [&#x200B; lijsten van de Rekening &#x200B;](../accounts/account-lists.md).

## Een publiekssegment maken

1. Selecteer **[!UICONTROL Accounts]** > **[!UICONTROL Audiences]** in de linkernavigatie.

1. Klik op **[!UICONTROL Create audience]** in de rechterbovenhoek.

   ![&#x200B; creeer een publiekssegment &#x200B;](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Volg de stappen in de [&#x200B; gids van de Dienst van de Segmentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.
