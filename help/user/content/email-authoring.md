---
title: E-mailberichten schrijven
description: Leer hoe u e-mailinhoud maakt in Adobe Journey Optimizer B2B. Met sjablonen, HTML-import en door AI aangedreven tools kunt u uw e-mailcommunicatie personaliseren en optimaliseren.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 633f23525a6fd2b03460ecbef17379077d6b51d2
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# E-mailbericht schrijven

Nadat u &lbrack; een nieuw <!-- or duplicated --> e-mailmiddel aan een knoop van de reisactie &rbrack;(./add-email.md) toevoegt, kunt u de inhoud voor het e-mailbericht bepalen.

Klik op **[!UICONTROL Edit email content]** op de tab _[!UICONTROL Details]_&#x200B;in het rechterdeelvenster.

![ Klik op E-mailinhoud bewerken ](./assets/add-email-content.png){width="700" zoomable="yes"}

Met deze handeling worden de ontwerpgereedschappen voor e-mail gestart, waarin u kunt kiezen hoe u uw e-mail wilt ontwerpen op basis van de volgende opties:

* [ Ontwerp uw e-mail van kras ](#design-your-email-from-scratch) gebruikend de interface van Designer E-mail.

* [ voer bestaande inhoud van HTML ](#import-existing-html-content) van een dossier of een .zip omslag in.

* [ selecteer een bestaand malplaatje ](#select-a-template) van een lijst van ingebouwde of douane e-mailmalplaatjes.

Nadat u de e-mailinhoud hebt gemaakt en aangepast, kunt u de inhoud exporteren voor validatie of later gebruik. Klik op **[!UICONTROL Export HTML]** om de inhoud op te slaan als een ZIP-bestand dat uw HTML en elementen bevat.

>[!TIP]
>
>Gebruik AI Assistant in Adobe Journey Optimizer B2B edition, aangedreven door generatieve AI om uw inhoud naar het volgende niveau te tillen. Met AI Assistant kunt u de impact van uw leveringen optimaliseren door volledige e-mails, gerichte tekstinhoud en aanbevelingen voor AI Assistant te genereren voor afbeeldingen die op uw publiek zijn afgestemd. [Meer informatie](./ai-assistant-emails.md)

## Ontwerp uw e-mail helemaal zelf {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Structuurcomponenten toevoegen"
>abstract="Structuurcomponenten definiëren de indeling van de bestemmingspagina. De belemmering en laat vallen component van de a **Structuur** in het canvas beginnen de inhoud van uw het landen pagina te ontwerpen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Informatie over contentonderdelen"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een bestemmingspagina te maken."

Gebruik de ruimte voor het ontwerpen van visuele inhoud om de structuur en inhoud van het e-mailbericht te definiëren. Door structurele componenten toe te voegen en te bewegen met eenvoudige belemmering-en-dalingsacties, kunt u de vorm van de herbruikbare e-mailinhoud binnen seconden ontwerpen.

1. Selecteer de optie **[!UICONTROL Design from scratch]** op de startpagina van _[!UICONTROL Design your template]_.
1. [ voegt structuur en inhoud ](#add-structure-and-content) aan het e-mailbericht toe.
1. [ voeg beeldactiva ](#add-assets) aan het e-mailbericht toe.
1. [ personaliseer de e-mailinhoud ](#personalize-content).
1. [ Overzicht en werk verbindingen ](#preview-and-edit-linked-urls) bij.

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

Wanneer de inhoud gereed is, klikt u op **[!UICONTROL Simulate content]** boven om de rendering te controleren. U kunt kiezen voor de weergave Computer of Mobiel.

Als u tevreden bent met de inhoud, klikt u op **[!UICONTROL Save]** .

## Bestaande HTML-inhoud importeren

{{$include /help/_includes/content-design-import.md}}

![ de invoer HTML- inhoud in een ZIP dossier ](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>Als u een `<table>` -tag als eerste laag in een HTML-bestand gebruikt, kan dit leiden tot stijlverlies, zoals de achtergrond- en breedte-instellingen in de bovenste laagtag.

U kunt de geïmporteerde inhoud naar wens aanpassen met de gereedschappen in de visuele e-maileditor.

## Een sjabloon selecteren

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> Op opgeslagen sjablonen kunnen governance-instellingen (inhoudvergrendeling) zijn toegepast op een of meer componenten. De visuele ontwerper verstrekt richtlijnen over gesloten componenten wanneer u [ auteur een e-mail van een geregeerd malplaatje ](./email-authoring-governance.md).

## Structuur en inhoud toevoegen {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Structuurcomponenten toevoegen"
>abstract="Structuurelementen definiëren de indeling van de e-mail. De belemmering en laat vallen component van de a **Structuur** in het canvas beginnen uw e-mailinhoud te ontwerpen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Informatie over contentonderdelen"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een e-mail te maken."

{{$include /help/_includes/content-design-components.md}}

### Fragmenten toevoegen

{{$include /help/_includes/content-design-use-fragments.md}}

Nadat het e-mailbericht is opgeslagen, wordt het weergegeven op de pagina met fragmentdetails wanneer u het tabblad _[!UICONTROL Used By]_&#x200B;in het overzicht selecteert.

### Elementen toevoegen

{{$include /help/_includes/content-design-assets.md}}

### Navigeren door de lagen, instellingen en stijlen

{{$include /help/_includes/content-design-navigation.md}}

### Inhoud personaliseren

{{$include /help/_includes/content-design-personalization.md}}

>[!NOTE]
>
>Als _[!UICONTROL My Tokens]_&#x200B;is gedefinieerd voor de accountreis, kunt u deze reisspecifieke tokens ook gebruiken voor uw e-mailinhoud. Zie [ de tokens van de Douane voor e-mailverpersoonlijking ](./personalization-my-tokens.md) voor meer informatie.

### Gekoppelde URL-tracking bewerken

{{$include /help/_includes/content-design-links.md}}

### Weergaveopties

Gebruik de opties voor weergave- en inhoudsvalidatie die beschikbaar zijn in de visuele e-maileditor.

* Zoom in of uit op de inhoud met de vooraf ingestelde zoomopties.

* Schakel de weergave van de inhoud in op Desktop, Mobiel of Alleen tekst/Onbewerkte tekst.
   * Klik het _pictogram van de Mening_ voor inhoudsvoorproef over apparaten.
   * Selecteer een van de apparaten die buiten het vak vallen of voer aangepaste afmetingen in om een voorvertoning van de inhoud weer te geven.

### Meer opties

Vanuit het menu _[!UICONTROL More ...]_&#x200B;boven aan de ontwerpruimte voor e-mail kunt u de volgende handelingen uitvoeren:

![ klik Meer om tot malplaatjeacties ](./assets/email-designer-more-menu.png){width="500"} toegang te hebben

* **[!UICONTROL Reset email]** - Klik op deze optie om het canvas van de visuele e-mailontwerper op een lege site te wissen en de opbouw van de inhoud opnieuw te starten.
* **[!UICONTROL Save as fragment]** - Sla alle e-mailberichten of delen ervan op als een fragment dat opnieuw moet worden gebruikt in meerdere e-mailsjablonen of e-mailsjablonen. U geeft een naam en beschrijving voor het fragment op en slaat het op in de lijst met beschikbare fragmenten.
* **[!UICONTROL Change your design]** - terugkeer aan het _Ontwerp uw e-mailpagina_. Van daar, kunt u een andere malplaatje kiezen om het ontwerpproces opnieuw te beginnen, of verkiezen om de inhoud van kras op een zwarte canvas te ontwerpen.\
* **[!UICONTROL Save as content template]** - Sla de e-mailtekst op als een e-mailsjabloon die opnieuw moet worden gebruikt in meerdere e-mails of e-mailsjablonen. U geeft een naam en beschrijving voor de sjabloon op en slaat deze op in de lijst met opgeslagen e-mailsjablonen.
* **[!UICONTROL Export HTML]** - Download de inhoud in het visuele canvas naar uw lokale systeem in de HTML-indeling die is verpakt als een zip-bestand.

## E-mail controleren en testen {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Controleren hoe uw inhoud wordt gerenderd"
>abstract="Wanneer uw inhoud is gedefinieerd, kunt u deze voorvertonen en controleren of de rendering correct is voor het kanaal dat u gebruikt."

Wanneer de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om deze voor te vertonen, proefdrukken te verzenden en de weergave ervan in populaire desktops, mobiele clients en webclients te beheren. Als u persoonlijke inhoud hebt ingevoegd, kunt u met testprofielgegevens een voorvertoning weergeven van de weergave van deze inhoud in het bericht.

Als u een voorbeeld van de e-mailinhoud wilt weergeven, klikt u op **[!UICONTROL Simulate content]** en voegt u vervolgens een testprofiel toe om uw bericht te controleren met behulp van de testprofielgegevens.

![ Simuleer de e-mailinhoud om uw ontwerp te controleren ](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
