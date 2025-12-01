---
title: '[!DNL Adobe Target] Extern publiek'
description: Activeer extern publiek aan  [!DNL Adobe Target]  door rekeningsreizen. B2B-webervaringen aanpassen en consistentie tussen platforms behouden.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 0%

---

# [!DNL Adobe Target] extern publiek

U kunt ervaringen voor externe doelgroepen in [!DNL Adobe Target] activeren en personaliseren via accountreizen. Gebruik deze integratie om geavanceerde en op maat gesneden personalisatie te bereiken die de betrokkenheid verhoogt, en om de consistentie tussen de platforms in [!DNL Target] en [!DNL Journey Optimizer B2B Edition] te handhaven. Deze consistentie zorgt ervoor dat teams webkanalen uitlijnen en aanpassen voor het aanschaffen van groepen gedurende de gehele B2B-kopersreis.

Het is een workflow in twee stappen om een extern publiek te activeren via Adobe Target:

1. [ voeg aan extern klantenpubliek ](#add-to-customer-external-audience-from-a-journey) van een reis toe.
2. [ activeer het externe publiek ](#activate-the-external-audience-to-target-as-a-destination) aan [!DNL Target] als bestemming in Experience Platform.

## Toevoegen aan extern publiek van klant van een reis

In uw reis, [ voeg a _toe neemt een actieknooppunt_ ](../journeys/action-nodes.md) om de _[!UICONTROL Add to external customer audience]_actie uit te voeren. Handelingen zijn doorgaans de handelingen die u wilt uitvoeren als gevolg van een of andere trigger, zoals een gebeurtenis of een vorige handeling. De reis voert de actie uit wanneer een kwalificerende rekening met persoonprofielen de knoop bereikt.

>[!NOTE]
>
>Wanneer een kwalificerende rekening met persoonprofielen _toevoegt aan de externe knoop van het klantenpubliek_ in een gepubliceerde reis, kan het tot 48 uren voor die profielen vergen om in het externe publiek te bevolken.

1. Met _neem een actie_ knoop die in het wegcanvas wordt geselecteerd, kies de _[!UICONTROL Action on]_**[!UICONTROL People]**optie.

1. Kies _[!UICONTROL Action on people]_bij **[!UICONTROL Add to external customer audience]**.

   ![ knoop van de Reis - neem een actie op mensen - voeg aan extern klantenpubliek toe ](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. Van de knoopeigenschappen op het recht, plaats het externe publiek.

   * Als er één of meerdere externe reeds gecreeerd publiek zijn, kunt u **[!UICONTROL Select existing]** kiezen en [ het publiek selecteren dat u ](#choose-an-external-audience) wilt gebruiken.

   * Als u [ een publiek ](#create-an-external-audience) wilt creëren om voor de knoop te gebruiken, kies **[!UICONTROL Create new]**.

### Een extern publiek maken

1. Klik op **[!UICONTROL Create new]** nadat u de optie **[!UICONTROL Create external customer audience]** in de knoopeigenschappen hebt gekozen.

   ![ neem een actie op mensen - voeg aan extern klantenpubliek toe - creeer nieuwe optie ](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. Voer in het dialoogvenster een **[!UICONTROL Name]** (vereist) en **[!UICONTROL Description]** (optioneel) voor het nieuwe publiek in.

   ![ creeer externe dialoog van het klantenpubliek ](./assets/create-external-customer-audience-dialog.png){width="400"}

1. Klik op **[!UICONTROL Create]**.

   Het systeem maakt het nieuwe publiek en geeft een bevestigingsbericht weer. Vervolgens kunt u doorgaan en het gebruiken als een bestaand publiek voor de actie node.

### Een extern publiek selecteren

1. Klik op **[!UICONTROL Select existing]** nadat u de optie **[!UICONTROL Select external customer audience]** in de knoopeigenschappen hebt gekozen.

   ![ neem een actie op mensen - voeg aan extern klantenpubliek toe - selecteer bestaande optie ](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. Selecteer in het dialoogvenster _[!UICONTROL Add audience]_het publiek dat u wilt gebruiken.

   U kunt tekst op het _gebied van het Onderzoek_ ingaan om de getoonde punten voor een gelijke van de publieksnaam te filtreren.

   ![ neem een actie op mensen - voeg aan extern klantenpubliek toe - voeg publieksdialoog toe ](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Add audience]**.

## Activeer het externe publiek aan Doel als bestemming

Als u het externe publiek naar Adobe Target wilt activeren, moet u [!DNL Adobe Target] als doel in [!DNL Real-time Customer Data Platform (RTCDP)] hebben geconfigureerd. Voor extra informatie over deze configuratie, verwijs naar de [ documentatie van RTCDP ](https://experienceleague.adobe.com/nl/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}.

>[!IMPORTANT]
>
>Als u de activering van RTCDP doorvoert, moet uw implementatie van e-mailadres als identiteit gebruiken.

Voor het activeringsproces moet u [!DNL Adobe Target] toevoegen als extern publiek of externe bestemming. Eerst bouwt u een [!DNL Target] publiek in de publieksbouwer. U kunt ook een placeholder-publiek maken en de externe publieksfunctie toevoegen.

>[!BEGINSHADEBOX]

![ het pictogram van Toestemmingen van AEP ](../../assets/do-not-localize/icon_permissions-outline.svg) Deze stappen vereisen de volgende toestemmingen voor uw toegewezen gebruikersrol:

* **[!UICONTROL Experience Platform]** - Voor de _[!UICONTROL Destinations]_resource: `Activate Destinations` , `Manage and Activate Dataset Destination` en `View Destination`
* **[!DNL Target]** - `Approver`

>[!ENDSHADEBOX]

1. Ga in Experience Platform naar **[!UICONTROL Connections]** > **[!UICONTROL Destinations]** in de linkernavigatie.

1. Selecteer het tabblad **[!UICONTROL Browse]**. 

1. Bepaal de plaats van de bestemmingsverbinding die u wilt gebruiken om uw segmenten te activeren, klik _Meer menu_ ( **...**) pictogram naast de naam, en kies **[!UICONTROL Activate audiences]**.

   Typ tekst in het veld _[!UICONTROL Search]_om de weergegeven doelen op naam te filteren.

   ![ Experience Platform - bestemmingen - doorblader de bestemmingen van het Doel - meer menu ](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. Selecteer uw externe publiek in de lijst _[!UICONTROL Available audiences]_en klik op **[!UICONTROL Next]**.

   ![ Experience Platform - bestemmingen - doorblader de bestemmingen van het Doel - meer menu ](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. Voer een extra veldtoewijzing uit naar het doel (optioneel) en klik op **[!UICONTROL Next]** .

1. Bekijk de nieuwe publieksparameters en klik op **[!UICONTROL Finish]** .

   ![ Experience Platform - bestemmingen - activeer bestemming - overzicht ](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

Op activering, kunt u het publiek in [ publiek van Adobe Target ](https://experienceleague.adobe.com/en/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"} zien en hen in de activiteiten van Adobe Target gebruiken.

