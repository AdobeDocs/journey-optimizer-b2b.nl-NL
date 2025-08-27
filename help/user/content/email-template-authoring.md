---
title: E-mailsjabloonontwerp
description: Leer hoe u e-mailsjablonen voor inhoud kunt ontwerpen die u kunt gebruiken voor e-mails over een account, zodat u uw ontwerpen eenvoudig en efficiënt kunt hergebruiken.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: f8d70f2e1cff6055ff353bad0c5a0f625d426db8
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# E-mailsjabloonontwerp

Nadat u [ een e-mailmalplaatje ](./email-templates.md#create-an-email-template) creeert, gebruik de visuele ontwerpruimte aan auteur de structuur en inhoudscomponenten in uw e-mailmalplaatje.

## Structuur en inhoud toevoegen {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Aangepaste CSS toevoegen

U kunt uw eigen aangepaste CSS rechtstreeks toevoegen binnen de ontwerpruimte van de e-mailsjabloon. Gebruik aangepaste CSS om geavanceerde en specifieke stijlen toe te passen, voor meer flexibiliteit en controle over de weergave van uw inhoud. Het wordt aanbevolen deze opmaak op het hoogste niveau toe te voegen voordat u componenten zoals afbeeldingen, knoppen en tekst opneemt.

Selecteer met ten minste één inhoudscomponent op het canvas de component **[!UICONTROL Body]** in de linkernavigatiestructuur voor toegang tot de aangepaste CSS-editor.

![ heb toegang tot de lichaamstijlen ](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Fragmenten toevoegen

>[!NOTE]
>
>De fragmenten zijn niet dwars-compatibel tussen de _wijze van het Thema_ en _Handmatige wijze_ in de e-mailinhoud. Om een fragment in e-mailinhoud te gebruiken waar een thema wordt toegepast, moet het fragment ook op _wijze van het Thema_ worden gecreeerd.

{{$include /help/_includes/content-design-use-fragments.md}}

Nadat de sjabloon is opgeslagen, wordt deze weergegeven op de pagina met fragmentdetails wanneer u het tabblad _[!UICONTROL Used By]_&#x200B;in het overzicht selecteert.

### Elementen toevoegen

{{$include /help/_includes/content-design-assets.md}}

### Navigeren door de lagen, instellingen en stijlen

{{$include /help/_includes/content-design-navigation.md}}

### Inhoud personaliseren

{{$include /help/_includes/content-design-personalization-email.md}}

### Gekoppelde URL-tracking bewerken

{{$include /help/_includes/content-design-links.md}}

## Weergaveopties

Gebruik de opties voor weergave- en inhoudsvalidatie die beschikbaar zijn in de ruimte van het visuele ontwerp.

* Zoom in of uit op de inhoud met de vooraf ingestelde zoomopties.

* Schakel de weergave van de inhoud in op Desktop, Mobiel of Alleen tekst/Onbewerkte tekst.
   * Klik het _Oog_ pictogram voor inhoudsvoorproef over apparaten.
   * Selecteer een van de apparaten die buiten het vak vallen of voer aangepaste afmetingen in om een voorvertoning van de inhoud weer te geven.

### Meer opties

Vanuit het menu _[!UICONTROL More ...]_&#x200B;boven aan de ontwerpruimte voor e-mail kunt u de volgende handelingen uitvoeren:

![ klik Meer om tot malplaatjeacties ](./assets/visual-designer-more-menu.png){width="500"} toegang te hebben

* **[!UICONTROL Reset template]** - Klik op deze optie om het ontwerpcanvas op een lege site te wissen en de bouwinhoud opnieuw te starten.
* **[!UICONTROL Save as fragment]** - Sla de sjabloon geheel of gedeeltelijk op als een fragment dat opnieuw moet worden gebruikt in meerdere e-mails of e-mailsjablonen. U geeft een naam en beschrijving voor het fragment op en slaat het op in de lijst met beschikbare fragmenten.
* **[!UICONTROL Change your design]** - terugkeer aan het _Ontwerp uw e-mailpagina_. Vervolgens kunt u een andere sjabloon kiezen om het ontwerpproces opnieuw te starten. U kunt ook verkiezen om de inhoud van kras met een leeg canvas (_Klassieke wijze_) te ontwerpen of a [ merkthema ](./brand-themes.md) te gebruiken (_wijze van het Thema_).
* **[!UICONTROL Export HTML]** - Download de inhoud in het visuele canvas naar uw lokale systeem in de HTML-indeling die is verpakt als een zip-bestand.
