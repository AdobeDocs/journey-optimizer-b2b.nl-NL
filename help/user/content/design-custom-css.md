---
title: Aangepaste CSS toevoegen voor uw inhoud
description: Leer hoe u aangepaste CSS toevoegt aan uw e-mail en pagina-inhoud landt.
feature: Content Design Tools, Email Authoring, Landing Pages
role: User
exl-id: 5a961190-8a65-41b0-90d0-5dd44e5cdf8a
source-git-commit: 9abb6443a0761070d9864a4bd2243baa9568cdc9
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Aangepaste CSS toevoegen voor uw inhoud

U kunt uw eigen aangepaste CSS rechtstreeks toevoegen binnen de ontwerpruimte van de e-mail- of landingspagina. Gebruik aangepaste CSS om geavanceerde en specifieke stijlen toe te passen, voor meer flexibiliteit en controle over de weergave van uw inhoud.

De aangepaste CSS wordt met het kenmerk `<head>` toegevoegd aan de sectie `<style>` binnen een `data-name="global-custom"` -tag. Deze structuur zorgt ervoor dat de aangepaste stijlen globaal op de inhoud worden toegepast.

+++ Voorbeeldimplementatie

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="content-version" content="3.3.31">
    <meta name="x-apple-disable-message-reformatting">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <style data-name="default" type="text/css">
      td { padding: 0; }
      th { font-weight: normal; }
    </style>
    <style data-name="grid" type="text/css">
      .acr-grid-table { width: 100%; }
    </style>
    <style data-name="acr-theme" type="text/css" data-theme="default" data-variant="0">
      body { margin: 0; font-family: Arial; }
    </style>
    <style data-name="media-default-max-width-500px" type="text/css">
      @media screen and (max-width: 500px) {
        body { width: 100% !important; }
      }
    </style>
    <style data-name="global-custom" type="text/css">
      /* Add you custom CSS here */
    </style>
  </head>
  <body>
    <!-- Minimal content -->
  </body>
</html>
```

+++

>[!NOTE]
>
>De aangepaste CSS wordt niet weerspiegeld of gevalideerd in het deelvenster _[!UICONTROL Styles]_&#x200B;voor een geselecteerde component. Deze is volledig onafhankelijk en kan alleen worden gewijzigd met de optie [!UICONTROL Add Custom CSS] op het niveau van de hoofdcomponent.

## Aangepaste CSS toevoegen

1. Als er ten minste één inhoudscomponent op het canvas is toegevoegd, selecteert u de **[!UICONTROL Body]** -component in de linkernavigatie.

1. Selecteer het _lusje van Stijlen_ op het recht en klik **[!UICONTROL Add custom CSS]**.

   ![ heb toegang tot de lichaamstijlen ](./assets/email-body-styles.png){width="800" zoomable="yes"}

   >[!NOTE]
   >
   >De knop _[!UICONTROL Add custom CSS]_&#x200B;is alleen beschikbaar wanneer de component&#x200B;_[!UICONTROL Body]_ is geselecteerd. U kunt echter aangepaste CSS-stijlen toepassen op alle componenten in de stijl.

   De pop-upeditor van _[!UICONTROL Add custom CSS]_&#x200B;wordt weergegeven met opmerkingen voor plaatsaanduidingscode.

1. Voer uw CSS-code in de editor in.

   Zorg ervoor dat de aangepaste CSS geldig is en de juiste syntaxis volgt. Als de ingevoerde CSS ongeldig is, wordt een foutbericht weergegeven en kan de CSS niet worden opgeslagen. Meer leren, zie [ CSS geldigheid ](#css-validity).

   ![ ga douaneCSS in de redacteur in ](./assets/content-design-add-custom-css.png){width="450"}

1. Klik op **[!UICONTROL Save]** om de aangepaste CSS op te slaan.

   Het aangepaste stijlblad wordt toegepast op de bestaande inhoud. U kunt controleren of uw aangepaste CSS is toegepast naar wens. Voor informatie over hoe te om veranderingen aan te brengen en de toepassing van het stijlblad aan te passen, zie [ het Oplossen van problemen ](#troubleshooting).

   ![ Aangepaste CSS die op inhoud ](assets/email-body-custom-css-applied.png){width="600" zoomable="yes"} wordt toegepast

## CSS-geldigheid

>[!CAUTION]
>
>Gebruikers zijn verantwoordelijk voor de beveiliging van hun aangepaste CSS. Zorg ervoor dat uw CSS geen kwetsbaarheden of conflicten met de bestaande inhoud introduceert.
>
>Vermijd het gebruik van CSS die de lay-out of functionaliteit van de inhoud onbedoeld kan onderbreken.

+++ Voorbeelden van geldige CSS

```css
.acr-component[data-component-id="form"] {
  display: flex;
  justify-content: center;
  background: none;
}

.acr-Form {
  width: 100%;
  padding: 20px 100px;
  border-spacing: 0px 8px;
  box-sizing: border-box;
  margin: 0;
}

.acr-Form .spectrum-FieldLabel {
  width: 20%;
}

.acr-Form.spectrum-Form--labelsAbove .spectrum-FieldLabel,
.acr-Form [data-form-item="checkbox"] .spectrum-FieldLabel {
  width: auto;
}

.acr-Form .spectrum-Textfield {
  width: 100%;
}

#acr-form-error,
#acr-form-confirmation {
  width: 100%;
  padding: var(--spectrum-global-dimension-static-size-500);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: var(--spectrum-global-dimension-static-size-200);
}

.spectrum-Form-item.is-required .spectrum-FieldLabel:after{
  content: '*';
  font-size: 1.25rem;
  margin-left: 5px;
  position: absolute;
}

/* Error field placeholder */
.spectrum-HelpText {
  display: none !important;
}

.spectrum-HelpText.is-invalid,
.is-invalid ~ .spectrum-HelpText {
  display: flex !important;
}
```

```css
@media only screen and (min-width: 600px) {
  .acr-paragraph-1 {
    width: 100% !important;
  }
}
```

+++

+++ Voorbeelden van ongeldige CSS

Het gebruik van `<style>` -tags wordt niet geaccepteerd:

```html
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```

Ongeldige syntaxis, zoals ontbrekende accolades, wordt niet geaccepteerd:

```css
body {
  background: red;
```

+++

## CSS in geïmporteerde inhoud

Houd rekening met het volgende als u aangepaste CSS wilt gebruiken met inhoud die is geïmporteerd in de ontwerpruimte van de e-mail- of landingspagina:

* Als u externe HTML-inhoud, inclusief CSS, importeert, wordt deze <!-- unless converting that content, --> gevuld in [!UICONTROL Compatibility mode] en is de sectie [!UICONTROL CSS styles] niet beschikbaar.

* Als u inhoud importeert die oorspronkelijk is gemaakt in de ontwerpruimte van de e-mail- of landingspagina, inclusief CSS die is toegepast via de optie [!UICONTROL Add custom CSS] , is de toegepaste CSS zichtbaar en bewerkbaar vanuit dezelfde optie.

## Problemen oplossen

Als uw aangepaste CSS niet wordt toegepast zoals u had verwacht, gebruikt u de browserontwikkelaarsgereedschappen om de inhoud te inspecteren en te controleren of uw CSS zich richt op de juiste kiezers. Overweeg het volgende terwijl u de opmaakcode bekijkt:

* Controleer of uw CSS geldig is en geen syntaxisfouten bevat (zoals ontbrekende accolades, onjuiste eigenschapsnamen).

* Controleer of uw CSS is toegevoegd aan de tag `<style>` met het kenmerk `data-name="global-custom"` .

* Controleer of het kenmerk `global-custom` is ingesteld op true voor de stijltag `data-disabled` , zoals:

  `<style data-name="global-custom" type="text/css" data-disabled="true"> body: { color: red; } </style>`

* Controleer of uw CSS niet ergens in de inhoud wordt overschreven, zoals toegepaste inline styling.

* Voeg `!important` toe aan uw declaraties om ervoor te zorgen dat deze prioriteit krijgen, zoals:

  ```
  .acr-Form {
  background: red !important;
  }
  ```
