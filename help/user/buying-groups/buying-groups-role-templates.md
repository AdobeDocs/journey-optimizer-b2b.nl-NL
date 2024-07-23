---
title: Rolinesjablonen voor groepen kopen
description: Meer informatie over het definiëren van een rolsjabloon die moet worden gebruikt als onderdeel van een inkoopgroep.
feature: Buying Groups
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: 8afc432e7caeb2bf7e632276a7432d0a010f9ab2
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# Rolinesjablonen voor groepen kopen

Op een B2B-markt worden aankoopbeslissingen meestal door meerdere personen genomen. Deze personen nemen deel aan het besluitvormingsproces overeenkomstig hun rol binnen de organisatie. Creëer de rolmalplaatjes van de Groep van de Koophandel die deze roldefinities volgens elk product bevatten die type of rekeningsgebruik aanbieden geval.

## Rolsjablonen openen en doorbladeren

1. Klik op de startpagina van Adobe Experience Platform op Adobe Journey Optimizer B2B Edition.

1. Klik in de linkernavigatie op **[!UICONTROL Buying groups]** .

1. Selecteer op de pagina _[!UICONTROL Buying groups]_de tab **[!UICONTROL Roles Templates]**.

   ![ het lusje van Malplaatjes van Rollen ](assets/roles-templates-tab.png){width="700" zoomable="yes"}

   Het tabblad bevat een overzicht van alle bestaande rolsjablonen met de volgende kolommen:

   * [!UICONTROL Name]
   * [!UICONTROL Status]
   * [!UICONTROL Creation date]
   * [!UICONTROL Created by]
   * [!UICONTROL Last update]
   * [!UICONTROL Last updated by]
   * [!UICONTROL Published on]
   * [!UICONTROL Published by]

   De lijst wordt standaard gesorteerd op de kolom _[!UICONTROL Last update]_.

   Het aantal _levende_ (gepubliceerde) rolmalplaatjes wordt getoond bij het hoogste recht van de pagina. Alle rolmalplaatjes hebben een status van `Draft` of `Live`.

1. Als u de lijst op naam wilt filteren, gebruikt u het zoekveld boven aan de lijst.

   Voer de eerste paar tekens van de naam in om de weergegeven lijst te beperken tot de overeenkomende items.

   ![ het filtreren van Malplaatjes van Rollen door onderzoekskoord ](assets/roles-templates-search.png){width="700" zoomable="yes"}

## Een rolsjabloon maken

1. Klik in het tabblad _[!UICONTROL Roles Templates]_op **[!UICONTROL Create template]**in de rechterbovenhoek.

1. Voer in het dialoogvenster een unieke **[!UICONTROL Name]** (vereist) en **[!UICONTROL Description]** (optioneel) voor de sjabloon in.

   ![ creeer de dialoog van het Malplaatje van Rollen ](assets/roles-template-create-dialog.png){width="400"}

1. Voeg een regel toe voor elke rol die u voor het malplaatje wilt bepalen.

   Voor de huidige release zijn er zes rollen: `Decision Maker`, `Influencer`, `Practitioner`, `Executive Steering Committee`, `Champion` en `Other` .

   ![ het Kopen lijst van groepsrollen ](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * Kies een rol in de lijst.

   * Klik op **[!UICONTROL Add Condition]**.

   * Vouw in het dialoogvenster Voorwaarde de lijst met **[!UICONTROL Person attributes]** uit en zoek een kenmerk dat u wilt gebruiken om de rol aan te passen. Sleep het naar rechts en zet het neer in de filterruimte.

     ![ het malplaatje van Rollen voegt voorwaarde belemmeringsattributen toe ](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

   * Gebruik het kenmerk om een overeenkomend filter te maken met een of meer waarden.

     In het volgende voorbeeld, wordt het attribuut van de Titel van de Baan gebruikt om een gelijke voor de Maker van het Besluit te identificeren. Elke waarde voor een titel die begint met `Director` of `Sr Director` wordt als true beschouwd voor de voorwaarde.

     ![ het voorbeeld van de het malplaatjevoorwaarde van Rollen gebruikend baantitel ](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

   * Voeg zo nodig een ander kenmerk en een andere voorwaarde toe die de criteria voor een overeenkomst met de rol verder verfijnen.

   * Klik op **[!UICONTROL Done]**.

   Voor elke aanvullende rol die u voor de sjabloon wilt opnemen, klikt u op **[!UICONTROL Add another role]** en definieert u een of meer voorwaarden die met de rol moeten overeenkomen.

   ![ het malplaatje van Rollen met veelvoudige bepaalde rollen ](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

1. Als de sjabloon gereed is voor gebruik, klikt u op **[!UICONTROL Publish]** rechtsboven.

   Het publiceren van het malplaatje plaatst het aan a _Levende_ status en maakt het beschikbaar om met een Rente van de Oplossing te associëren. Er moet minstens één bepaalde rol zijn om het rolmalplaatje te publiceren.

   Uw veranderingen worden auto-bewaard in de _status van het Ontwerp_. Als u niet bereid bent om het rolmalplaatje te publiceren, klik de linker (rug) pijl bij de bovenkant van de pagina en terugkeer aan de lijst van de Malplaatjes van Roles.
<!-- 
< PM -- the Required for completion checkbox is not available to clear. Is this functional for Beta? >

Required for completion checkbox - select this for a role if it is required to calculate the completeness score. -->

## Een sjabloon voor conceptrollen bewerken

Wanneer een rolmalplaatje in de staat van het Ontwerp van het a __ is, kunt u de bepaalde rollen blijven uitgeven. Wijzigingen die u aanbrengt, worden automatisch opgeslagen.

Wijzig een van de instellingen in de koptekst van de rolkaart, inclusief de rol van de inkoopgroep, weging, automatische toewijzing en de vereiste voor het bijhouden van volledigheid.

![ Verandering die de eigenschappen van de groepsrol koopt ](./assets/roles-template-role-properties.png){width="600"}

### Filters voor een rol wijzigen

Om de het filtreren logica voor om het even welke rollen te veranderen, klik _uitgeven_ (potlood) pictogram bij hoogste recht van de rolkaart. Met deze actie opent u de werkruimte van _[!UICONTROL Conditions]_waar u een bestaand filter kunt wijzigen, een ander filter kunt toevoegen, een filter kunt verwijderen of de filterlogica kunt wijzigen.

### Een rolkaart verwijderen

Als u een rol uit het malplaatje wilt verwijderen, klik _Schrapping_ (trashcan) pictogram in de rolkaart.

### De prioriteit voor rollen instellen

U kunt de rollen binnen het malplaatje opnieuw in orde brengen, dat de prioriteit voor het toewijzen bepaalt leidt tot een rol. Rechts van elke rolkaart wordt een **[!UICONTROL Priority]** -controller weergegeven. Klik _Omhoog_ of _Omlaag_ pijl bij het recht om de rolkaart omhoog of neer in prioriteit te bewegen.

![ de rolprioriteit van de Verandering ](./assets/roles-template-role-priority.png){width="700"}

## Een rolsjabloon verwijderen

U kunt een rolmalplaatje schrappen als het in de _status van het Ontwerp_ is.

1. Selecteer de rolmalplaatje van de lijst om het te openen.

1. Klik op **[!UICONTROL Delete]** rechtsboven.

   ![ de rolprioriteit van de Verandering ](./assets/roles-template-delete.png){width="700"}

1. Klik in het dialoogvenster op **[!UICONTROL Delete]** om te bevestigen.
