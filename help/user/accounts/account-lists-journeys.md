---
title: Accountlijsten gebruiken voor reizen en programma's
description: Gebruik accountlijsten in de reisorchestratie, voeg dynamisch accounts toe of verwijder deze en filterde Marketo Engage Smart Lists in Journey Optimizer B2B edition.
feature: Account Lists, Account Journeys
role: User
exl-id: 7cda080d-6263-4ccd-b144-432e4e78c298
source-git-commit: 937101d6570a8217ff11037822c414350c6026ae
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Accountlijsten gebruiken voor reizen en programma&#39;s

Er zijn meerdere manieren waarop u lijsten met Live (gepubliceerde) accounts kunt opnemen in uw accountreizen.

## Knop voor accountpubliek

Al rekeningsritten beginnen met een [_knoop_ van het publiek van de Rekening 0&rbrace;. ](../journeys/account-audience-nodes.md) Wanneer u deze knoop plaatst om een rekeningslijst te gebruiken, bewegen de lidrekeningen zich door de reis wanneer het (gepubliceerd) live gaat.

1. Selecteer de **[!UICONTROL Account list]** optie voor de beginnende _2&rbrace; knoop van het publiek van de Rekening._

   ![ Uitgezochte optie van de rekeningslijst voor de knoop van het rekeningspubliek ](../journeys/assets/node-audience-account-list.png){width="500"}

1. Klik op **[!UICONTROL Add accounts list]**.

1. Schakel het selectievakje voor de accountlijst in en klik op **[!UICONTROL Save]** .

   ![ Uitgezochte optie van de rekeningslijst voor de knoop van het rekeningspubliek ](../journeys/assets/node-audience-account-list-select-dialog.png){width="600" zoomable="yes"}

## Een actieknooppunt maken - Toevoegen aan account

**_Statische rekeningslijsten slechts_**

Binnen een rekeningsreis, voeg rekeningen aan een statische rekeningslijst toe gebruikend [ a _neem een 2&rbrace; knoop van de Actie_.](../journeys/action-nodes.md)

U hebt bijvoorbeeld een reispad waar u een e-mail verzendt en sommige accounts verschillende acties uitvoeren als reactie. U beschouwt deze activiteit als een kwalificatiepunt op de reis. Met de kwalificatie, wilt u hen aan een rekeningslijst toevoegen die als publiek voor een andere reis met een verschillende stroom voor gekwalificeerde rekeningen wordt gebruikt.

>[!NOTE]
>
>Als een account al in de lijst staat wanneer het knooppunt wordt uitgevoerd, wordt de handeling genegeerd.

1. Selecteer de optie _[!UICONTROL Action on]_&#x200B;**[!UICONTROL Accounts]**.

1. Kies _[!UICONTROL Action on accounts]_&#x200B;bij **[!UICONTROL Add to account list]**.

   ![ Uitgezochte Add aan rekeningslijst ](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. Kies bij **[!UICONTROL Select live static account list]** de accountlijst waaraan u accounts wilt toevoegen.

   ![ Uitgezochte Add aan rekeningslijst ](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

## Een actieknooppunt maken - Verwijderen uit account

**_Statische rekeningslijsten slechts_**

Binnen een rekeningsreis, verwijder rekeningen uit een statische rekeningslijst gebruikend [ a _neemt een 2&rbrace; knoop van de Actie_.](../journeys/action-nodes.md)

U hebt bijvoorbeeld een reispad waar u een e-mail verzendt en sommige accounts verschillende acties uitvoeren als reactie. U beschouwt deze activiteit als een kwalificatiepunt op de reis. Met deze kwalificatie, wilt u hen uit een rekeningslijst verwijderen die als publiek voor een andere reis wordt gebruikt die extra e-mails verzendt zodat u uw kwalificatiemededelingen niet dupliceert.

>[!NOTE]
>
>Als een account niet in de lijst staat waar deze moet worden verwijderd, wordt de handeling genegeerd.

1. Selecteer de optie _[!UICONTROL Action on]_&#x200B;**[!UICONTROL Accounts]**.

1. Kies _[!UICONTROL Action on accounts]_&#x200B;bij **[!UICONTROL Remove from account list]**.

   ![ Uitgezochte Add aan rekeningslijst ](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. Kies bij **[!UICONTROL Select live static account list]** de accountlijst waarin u accounts wilt verwijderen.

   ![ Uitgezochte Add aan rekeningslijst ](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}

## Marketo Engage-programma - Lijst van lidstaten

Als Marketer wilt u wellicht programma&#39;s in Marketo Engage onderdrukken voor mensen die deel uitmaken van accountlijsten in Journey Optimizer B2B edition.

In de Marketo Engage-instantie die is verbonden met Journey Optimizer B2B edition, kunt u het filter _[!UICONTROL Member of Account List]_&#x200B;in uw slimme lijsten gebruiken om deze leads te identificeren op basis van uw campagnestrategie. Voor meer informatie over Slimme Lijsten, verwijs naar de [ documentatie van Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"}.

### Het filter toevoegen aan een slimme lijst

1. Selecteer in Marketo Engage een campagne en klik op de tab **[!UICONTROL Smart List]** .

1. Typ `Member` in de lijst met filters rechts in het scherm en zoek het filter **[!UICONTROL Member of Account List]** .

1. Sleep het filter naar het canvas Slimme lijst.

1. Stel op het canvas Slimme lijst de waarde van de **[!UICONTROL Member of account]** lijst in.

   Klik op de pijl-omlaag om alle accountlijsten weer te geven of voer een deel van de naam van de accountlijst in om de accountlijst te zoeken die u nodig hebt.

   ![ Marketo Engage slimme lijstfilter voor het lidmaatschap van de rekeningslijst ](./assets/account-lists-marketo-engage-smart-list.png){width="800" zoomable="yes"}

1. Voeg in de campagnestroom de stap **[!UICONTROL Add to List]** toe en kies de lijst waar u de personen wilt vullen in de accountlijst van Journey Optimizer B2B edition.

   Verwijs naar _[een stap van de Stroom aan een slimme campagne ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/add-a-flow-step-to-a-smart-campaign){target="_blank"}_ in de documentatie van Marketo Engage voor gedetailleerde informatie over het toevoegen van stappen aan een stroom toevoegen.

### De leden controleren

Nadat de stroom loopt, kunt u de lijst van mensen bekijken die in de lijst worden bevolkt. Open de lijst en selecteer het tabblad Personen.

![ Marketo Engage campagnemelijst bevolkt van een rekeningslijst ](./assets/account-lists-marketo-engage-smart-list-people.png){width="800" zoomable="yes"}
