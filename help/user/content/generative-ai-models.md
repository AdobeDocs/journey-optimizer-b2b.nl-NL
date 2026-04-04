---
title: Generatieve AI-modellen
description: Maak en beheer generatieve AI-afbeeldingsmodellen die marketeers kunnen selecteren voor het genereren van afbeeldingen voor e-mail- en landingspagina-inhoud.
topic: Artificial Intelligence
feature: Generative AI, Brand Identity, Content
role: User
level: Beginner, Intermediate
source-git-commit: 0612c3caa0673a7eb65a0aac0010edcf12c5d553
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Generatieve AI-modellen voor merkuitlijning

Breid uw mogelijkheden voor het maken van AI-afbeeldingen uit met ingebouwde modellen, aangepaste Firefly-modellen en externe leveranciers van images om aan uw specifieke behoeften te voldoen en de uitlijning van uw merk te verbeteren:

- **[!UICONTROL Adobe model]** , aangedreven door Firefly Image Model 4, wordt uit de doos geleverd en klaar voor gebruik voor directe beeldgeneratie zonder extra opstelling.
- **[!UICONTROL Partner model]**, aangedreven door Gemini 2.5 Flash, biedt gespecialiseerde mogelijkheden voor specifieke gebruiksgevallen.
- **[!UICONTROL Custom models]** zijn merkspecifieke modellen die op uw eigen middelen zijn getraind en door uw organisatie zijn toegevoegd.

Leer over douanemodellen in de [ documentatie van Adobe Firefly ](https://helpx.adobe.com/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html){target="_blank"}.

Marketers kunnen elk van de ingeschakelde generatieve modellen selecteren wanneer ze afbeeldingen genereren voor hun e-mail- of landingspagina-inhoud.

## Generatieve modellen beheren

Vanuit een centrale locatie kunt u alle beschikbare modellen bekijken, filteren en zoeken om specifieke modellen te zoeken en modelinstellingen voor uw merken te configureren.

1. Ga in de linkernavigatie naar **[!UICONTROL Content Management]** > **[!UICONTROL Brands]** .

1. Selecteer de tab **[!UICONTROL Generative models]** op de pagina.

![ toegang tot de generatieve lijst van modellen ](./assets/brands-gen-models-list.png){width="800" zoomable="yes"}

### De lijst filteren en doorzoeken

Klik het _pictogram van de Filter_ ![ ](../../assets/do-not-localize/icon-react-filter.svg) om tot het filtermenu toegang te hebben. Filtermodellen op **[!UICONTROL Type]** of **[!UICONTROL Status]** .

![ filter de generatieve lijst van modellen ](./assets/brands-gen-models-filter.png){width="700" zoomable="yes"}

U kunt de zoekbalk ook gebruiken om een specifiek generatief model op naam te zoeken.

### Modelacties

Voor een douanemodel in de lijst, klik het _Meer menu_ ![ Meer menupictogram ](../../assets/do-not-localize/icon-more-menu.svg) pictogram. U kunt **[!UICONTROL Enable]** of **[!UICONTROL Disable]** kiezen om de beschikbaarheidsstatus van het model te wijzigen of **[!UICONTROL Delete]** kiezen om het model uit de lijst te verwijderen.

![ Meer menu in de generatieve lijst van modellen ](./assets/brands-gen-models-more-menu.png){width="450"}

Voor een ingebouwd model, klik _toelaten_ ( ![ laat pictogram ](../../assets/do-not-localize/icon-enable.svg) toe) of _maak_ onbruikbaar ( ![ onbruikbaar maken pictogram ](../../assets/do-not-localize/icon-disable.svg)) pictogram om de modelbeschikbaarheid voor beeldgeneratie te veranderen.

>[!NOTE]
>
>Alleen aangepaste modellen kunnen worden verwijderd.

## Een generatief model toevoegen

Maak aangepaste Firefly-modellen of verbind externe leveranciers van beeldgeneratie met elkaar om uw generatieve AI-mogelijkheden uit te breiden.

>[!NOTE]
>
>Voor het maken van aangepaste Firefly-modellen is een Firefly ETLA-overeenkomst vereist.

1. Klik op het tabblad _[!UICONTROL Generative models]_op **[!UICONTROL Add model]**.

1. Voer een **[!UICONTROL Name]** in voor uw model.

<!-- 1. Select a **[!UICONTROL Model provider]**. future development -->

1. Voer de **[!UICONTROL Model ID]** in.

   Ga naar de Firefly-website en navigeer naar uw getrainde modellen om uw model-id te zoeken. De unieke id is beschikbaar in de beheersectie van het model nadat deze is gepubliceerd. Voor meer informatie, verwijs naar de [ documentatie van de douanemodellen van Firefly ](https://helpx.adobe.com/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html){target="_blank"}.

1. Voer desgewenst een **[!UICONTROL Description]** in om het model en het beoogde gebruik te identificeren.

   ![ voeg Model toe - generatieve modellen ](./assets/brands-gen-models-add-model.png){width="550" zoomable="yes"}

1. Klik op **[!UICONTROL Test connection]** om de modelconfiguratie te controleren.

1. Wanneer de verbindingstest succesvol is, klik **[!UICONTROL Save]** om uw modelconfiguratie te bewaren.

   Als u het model opslaat, wordt het toegevoegd aan de lijst met generatieve modellen, waar u het kunt inschakelen voor gebruik door marketers. U kunt het op elk ogenblik ook onbruikbaar maken of schrappen.

   ![ Selecterend een generatief model voor beeldgeneratie ](./assets/gen-ai-model-selection.png){width="600" zoomable="yes"}
