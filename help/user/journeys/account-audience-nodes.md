---
title: Auditienoten account
description: Meer informatie over het type accountpubliek dat u kunt gebruiken voor het definiëren van de invoer voor uw accountreizen in Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 5ed7e58b7a069c8b436d0d2f7b338072259768be
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Transparante knooppunten voor het publiek

Het het publieksknoop van de Rekening bepaalt de inputrekeningen voor de reis. Wanneer u [ een rekeningsreis ](./journey-overview.md#create-an-account-journey) creeert, begint het altijd met een _het publiek van de Rekening_ knoop die de input voor de reis bepaalt.

Er zijn twee typen invoer die u voor dit knooppunt kunt gebruiken:

* **[het publiek van de Rekening](../audiences/account-audience-overview.md)** - dit is het basispubliek dat van de Dienst van de Segmentatie van Experience Platform wordt gesynchroniseerd.
* **[lijst van de Rekening](../accounts/account-lists.md)** - dit is een inzameling van genoemde rekeningen die u voor gerichte reisorchestratie kunt gebruiken. Een accountlijst bevat benoemde accounts op basis van de gedefinieerde criteria, zoals de industrie, locatie of grootte van het bedrijf.

_om het publiek voor de knoop te plaatsen:_

1. Klik op het knooppunt **[!UICONTROL Account audience]** om de knoopeigenschappen aan de rechterkant weer te geven.

   ![ de publieksknoop van de Rekening ](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Kies het invoertype voor accounts die de rit moeten invoeren:

   * **[!UICONTROL Account audience]**

     Kies dit type en klik op **[!UICONTROL Add account audience]** .

     Selecteer in het dialoogvenster _[!UICONTROL Add audience]_&#x200B;een publiekssegment dat eerder is gemaakt en klik op **[!UICONTROL Add audience]**.

     ![ selecteer een publiekssegment voor de knoop ](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Account list]**

     Kies dit type en klik op **[!UICONTROL Add account list]** .

     Selecteer in het dialoogvenster _[!UICONTROL Select live account list]_&#x200B;een accountlijst die eerder is gepubliceerd en klik op **[!UICONTROL Save]**.

     ![ selecteer een levende rekeningslijst voor de knoop ](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Ga naar [ Lijsten van de Rekening ](../accounts/account-lists.md) voor gedetailleerde informatie over het creëren van en het publiceren van rekeningslijsten.

_om een publiekssegment tot stand te brengen:_

1. Kies in de linkernavigatie **[!UICONTROL Accounts]** > **[!UICONTROL Audiences]** .

1. Klik op **[!UICONTROL Create audience]** rechtsboven.

   ![ creeer een publiekssegment ](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Volg de stappen die in de [ gids van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/nl/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"} worden beschreven.
