---
title: E-mailberichten schrijven
description: Maak e-mails met visuele ontwerpgereedschappen, HTML-import of sjablonen - gebruik de productie van AI Assistant-inhoud, aangepaste CSS en personalisatie in Journey Optimizer B2B edition.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---

# E-mailbericht schrijven

Nadat u [ een e-mailmiddel aan een knoop van de reisactie ](./add-email.md) toevoegt, kunt u de inhoud voor het e-mailbericht bepalen.

Klik op **[!UICONTROL Edit email content]** op de tab _[!UICONTROL Details]_in het rechterdeelvenster.

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

Gebruik de ruimte voor het ontwerpen van visuele inhoud om de structuur en inhoud van het e-mailbericht te definiëren. Door structurele componenten toe te voegen en te bewegen met eenvoudige belemmering-en-dalingsacties, kunt u de vorm van de herbruikbare e-mailinhoud binnen seconden ontwerpen.

1. Selecteer de optie _[!UICONTROL Design your template]_op de startpagina van **[!UICONTROL Design from scratch]**.

1. Kies in het dialoogvenster _[!UICONTROL Create email]_het type e-mailinhoud dat u wilt ontwerpen.

   * **[!UICONTROL Use Themes]** - kies deze optie om e-mail op _wijze van het Thema_ tot stand te brengen. In deze modus kunt u een gedefinieerd merkthema gebruiken om het ontwerpproces voor inhoud te stroomlijnen en ervoor te zorgen dat het ontwerp wordt afgestemd op gedefinieerde standaarden.

   * **[!UICONTROL Manual Styling]** - kies deze optie om e-mail op _Handmatige wijze_ tot stand te brengen. In deze modus stelt u de opmaak handmatig in voor alle structuur- en inhoudscomponenten die u toevoegt aan het lege canvas.

1. [ voegt structuur en inhoud ](./email-authoring.md#add-structure-and-content) aan het malplaatje toe.

1. [ Overzicht en werk verbindingen ](#preview-and-edit-linked-urls) bij.

1. [ Test e-mail ](#check-and-test-the-email).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual design space for this email after switching to the code editor. -->

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
> Op opgeslagen sjablonen kunnen governance-instellingen (inhoudvergrendeling) zijn toegepast op een of meer componenten. De visuele ontwerpruimte verstrekt richtlijnen over gesloten componenten wanneer u [ auteur een e-mail van een geregeerd malplaatje ](./email-authoring-governance.md).

## Structuur en inhoud toevoegen {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Aangepaste CSS toevoegen

U kunt uw eigen aangepaste CSS rechtstreeks toevoegen binnen de ontwerpruimte van de e-mail. Gebruik aangepaste CSS om geavanceerde en specifieke stijlen toe te passen, voor meer flexibiliteit en controle over de weergave van uw inhoud. Het wordt aanbevolen deze opmaak op het hoogste niveau toe te voegen voordat u inhoudcomponenten zoals afbeeldingen, knoppen en tekst opneemt.

Selecteer met ten minste één inhoudscomponent op het canvas de component **[!UICONTROL Body]** in de linkernavigatiestructuur voor toegang tot de aangepaste CSS-editor.

>[!NOTE]
>
>Als uw e-mailbericht gebruikend a [ malplaatje met gesloten inhoud ](./template-content-governance.md) wordt ontworpen, kunt u geen douaneCSS aan uw inhoud toevoegen. Het knoplabel verandert in **[!UICONTROL View custom CSS]** en eventuele aangepaste CSS die al in de inhoud aanwezig is, is alleen-lezen.

![ heb toegang tot de lichaamstijlen ](./assets/email-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Fragmenten toevoegen

>[!NOTE]
>
>De fragmenten zijn niet dwars-compatibel tussen de _wijze van het Thema_ en _Handmatige wijze_ in de e-mailinhoud. Om een fragment in e-mailinhoud te gebruiken waar een thema wordt toegepast, moet het fragment ook op _wijze van het Thema_ worden gecreeerd.

{{$include /help/_includes/content-design-use-fragments.md}}

Nadat het e-mailbericht is opgeslagen, wordt het weergegeven op de pagina met fragmentdetails wanneer u het tabblad _[!UICONTROL Used By]_in het overzicht selecteert.

### Elementen toevoegen

{{$include /help/_includes/content-design-assets.md}}

### Navigeren door de lagen, instellingen en stijlen

{{$include /help/_includes/content-design-navigation.md}}

### Inhoud personaliseren

{{$include /help/_includes/content-design-personalization-email.md}}

>[!NOTE]
>
>Als _[!UICONTROL My Tokens]_is gedefinieerd voor de accountreis, kunt u deze reisspecifieke tokens ook gebruiken voor uw e-mailinhoud. Zie [ de tokens van de Douane voor e-mailverpersoonlijking ](./personalization-my-tokens.md) voor meer informatie.

### Gekoppelde URL-tracking bewerken

{{$include /help/_includes/content-design-links.md}}

### Weergaveopties

Gebruik de opties voor weergave- en inhoudsvalidatie die beschikbaar zijn in de visuele e-maileditor.

* Zoom in of uit op de inhoud met de vooraf ingestelde zoomopties.

* Schakel de weergave van de inhoud in op Desktop, Mobiel of Alleen tekst/Onbewerkte tekst.
   * Klik het _pictogram van de Mening_ voor inhoudsvoorproef over apparaten.
   * Selecteer een van de apparaten die buiten het vak vallen of voer aangepaste afmetingen in om een voorvertoning van de inhoud weer te geven.

## Meer opties

Vanuit het menu _[!UICONTROL More ...]_boven aan de visuele ontwerpruimte kunt u de volgende handelingen uitvoeren:

![ klik Meer om tot malplaatjeacties ](./assets/email-designer-more-menu.png){width="500"} toegang te hebben

* **[!UICONTROL Reset email]** - Klik op deze optie om het canvas voor het e-mailontwerp op een lege site te wissen en de opbouw van de inhoud opnieuw te starten.
* **[!UICONTROL Save as fragment]** - Sla alle e-mailberichten of delen ervan op als een fragment dat opnieuw moet worden gebruikt in meerdere e-mailsjablonen of e-mailsjablonen. U geeft een naam en beschrijving voor het fragment op en slaat het op in de lijst met beschikbare fragmenten.
* **[!UICONTROL Change your design]** - terugkeer aan het _Ontwerp uw e-mailpagina_. Vervolgens kunt u een andere sjabloon kiezen om het ontwerpproces opnieuw te starten. U kunt ook verkiezen om de inhoud van kras met een leeg canvas (_Klassieke wijze_) te ontwerpen of a [ merkthema ](./brand-themes.md) te gebruiken (_wijze van het Thema_).
* **[!UICONTROL Save as content template]** - Sla de e-mailtekst op als een e-mailsjabloon die opnieuw moet worden gebruikt in meerdere e-mails of e-mailsjablonen. U geeft een naam en beschrijving voor de sjabloon op en slaat deze op in de lijst met opgeslagen e-mailsjablonen.
* **[!UICONTROL Export HTML]** - Download de inhoud in het visuele canvas naar uw lokale systeem in de HTML-indeling die is verpakt als een zip-bestand.

## E-mail controleren en testen {#email-testing}

Wanneer de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om deze voor te vertonen, proefdrukken te verzenden en de weergave ervan in hoogte-breedteverhoudingen voor desktops en mobiele apparaten te bekijken. Als u persoonlijke inhoud hebt ingevoegd, kunt u met testprofielgegevens een voorvertoning weergeven van de weergave van deze inhoud in het bericht.

Om [ voorproef de e-mailinhoud ](./email-simulate-content.md), klik **[!UICONTROL Simulate content]** en selecteer een testprofiel om uw bericht te controleren gebruikend de gegevens van het persoonprofiel.

![ Simuleer de e-mailinhoud om uw ontwerp te controleren ](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}

U hebt toegang tot aanvullende gereedschappen voor het valideren en reviseren van de e-mailinhoud:

* [Een proefdruk verzenden](./email-simulate-content.md#send-proofs)
* [Rendering testen in e-mailclients](./email-test-rendering.md)
<!-- * Generate a spam report -->
