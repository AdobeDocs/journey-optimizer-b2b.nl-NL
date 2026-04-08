---
title: Geavanceerde HTML-modus voor e-mailsjabloonontwerp
description: Gebruik de modus Geavanceerde HTML om de onbewerkte HTML-bron van uw e-mailsjablooninhoud rechtstreeks weer te geven en te bewerken in de ontwerpruimte voor e-mail in Journey Optimizer B2B edition.
feature: Email Authoring, Templates, Content Design Tools
level: Experienced
role: User
source-git-commit: 95dba963e08125370f998cf3960d51ede94c2fb9
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Geavanceerde HTML-modus voor e-mailsjabloonontwerp

_Geavanceerde wijze van HTML_ verstrekt een mening die ervaren gebruikers de ruwe broncode voor e-mailmalplaatjeinhoud direct bekijken en laat uitgeven. Deze modus is ideaal wanneer u geavanceerde expressies, zoals voorwaardelijke logica, rechtstreeks in de bron wilt invoegen. Het is ook handig om structurele aanpassingen te maken die verder gaan dan wat de visuele ontwerpgereedschappen beschikbaar maken.

<!-- We don't have the code editor at this point 
>[!NOTE]
>
>_Advanced HTML mode_ is different from the code editor option that is available when you start a new design. The code editor does not allow you to change to the visual design space. With _advanced HTML mode_, you can toggle back and forth between the HTML source view and the visual design view at any time. -->

>[!AVAILABILITY]
>
>Deze eigenschap is momenteel in _Beperkte Beschikbaarheid_ en is niet beschikbaar aan alle gebruikers.

## Belangrijke beperkingen

Alvorens u geavanceerde wijze van HTML voor [&#x200B; e-mailmalplaatje creatie &#x200B;](./email-template-authoring.md) gebruikt, zorg ervoor dat u de volgende beperkingen begrijpt:

* **Geen bevestiging** — De redacteur van HTML voert syntaxiscontrole of lay-outcontrole niet uit. Controleer de code zorgvuldig voordat u deze opslaat.

* **de updates van de Inhoud** — De toekomstige systeemveranderingen kunnen wijzigingen beïnvloeden of overschrijven die aan standaardprijsverhoging op geavanceerde wijze van HTML worden aangebracht. Controleer uw inhoud na productupdates om ervoor te zorgen dat het zoals verwacht teruggeeft.

* **Beperkte steun** — Adobe kan het teruggeven problemen of inhoudsfouten niet oplossen die uit de wijzigingen van de douanecode voortvloeien die op de geavanceerde wijze van HTML worden aangebracht.

* **de beperkingen van de Voorproef** — De simulatie van de inhoud (voorproef met profielen) is slechts beschikbaar in Desktopmening, niet direct van de HTML bronmening.

### Geavanceerde HTML-modus openen

De geavanceerde HTML-modus is toegankelijk vanaf de werkbalk boven aan de ruimte voor visueel ontwerp wanneer u een e-mailsjabloon op het canvas hebt geladen.

1. Open of [&#x200B; creeer een e-mailmalplaatje &#x200B;](./email-templates.md#create-an-email-template) en open de ontwerpruimte om de inhoud uit te geven.

1. In de ontwerpruimte, klik het _[!UICONTROL HTML]_( ![&#x200B; pictogram van HTML &#x200B;](../assets/do-not-localize/icon-code.svg)) pictogram in de toolbar.

   ![&#x200B; klik het pictogram van HTML in de werkbalk van de het ontwerpruimte van het e-mailmalplaatje &#x200B;](./assets/email-template-advanced-html-mode-toolbar.png){width="750" zoomable="yes"}

   Als dit de eerste keer is dat de geavanceerde HTML-modus wordt geopend (of als een maand of meer is verstreken), wordt een waarschuwingsbericht weergegeven. Controleer de gegevens en klik op **[!UICONTROL OK]** om door te gaan.

   ![&#x200B; herzie de Geavanceerde de wijzewaarschuwing van HTML en klik O.K. om &#x200B;](./assets/email-template-html-mode-warning.png){width="500"} verder te gaan

   Het ontwerpcanvas schakelt over naar de onbewerkte HTML-bronweergave.

1. Controleer de code en voeg de gewenste wijzigingen toe aan de e-mailinhoud.

   Op _Geavanceerde wijze van HTML_, hebt u directe toegang tot de volledige bron van HTML van uw e-mailmalplaatjeinhoud:

   * Een deel van de onbewerkte HTML-markeringen weergeven en wijzigen.
   * Tussenvoegsel geavanceerde [&#x200B; verpersoonlijkingsuitdrukkingen &#x200B;](./personalization.md) direct in de bron.
   * Voeg [&#x200B; voorwaardelijke inhoud &#x200B;](./conditional-content.md) logica toe gebruikend uitdrukkingssyntaxis.
   * Voeg aangepaste HTML-kenmerken, trackingtags of andere markeringen toe die niet beschikbaar zijn via de besturingselementen voor visuele editors.

   ![&#x200B; Geavanceerde wijze van HTML met ruwe bron van HTML van de e-mailinhoud &#x200B;](./assets/email-template-advanced-html-mode.png){width="800" zoomable="yes"}

   >[!IMPORTANT]
   >
   >Zorg ervoor dat u de juiste HTML- en CSS-code invoert. Adobe biedt geen syntaxisvalidatie of ondersteuning voor aangepaste code.

   Vanwege compatibiliteitsredenen zijn simulatie en opslaan van inhoud niet beschikbaar in de geavanceerde HTML-modus. U kunt terugschakelen naar de bureaubladweergave om een voorvertoning van uw inhoud weer te geven en de sjabloon op te slaan. Alle bewerkingen die u aanbrengt, blijven behouden wanneer u schakelt tussen de HTML-bronweergave en de visuele ontwerpweergave.

   Als u in de geavanceerde HTML-modus op **[!UICONTROL Save]** of **[!UICONTROL Save & close]** rechtsboven klikt, verschijnt er een waarschuwingsvenster waarin u wordt gewaarschuwd dat u de geavanceerde HTML-modus moet verlaten voordat u de sjabloon opslaat en de ontwerpruimte verlaat.

   ![&#x200B; Alert dialoog die sparen wordt onbruikbaar gemaakt op geavanceerde wijze van HTML &#x200B;](./assets/email-template-advanced-html-save-disabled-alert.png){width="500"}

1. Klik het _[!UICONTROL Desktop]_( ![&#x200B; pictogram van de Desktop &#x200B;](../assets/do-not-localize/icon-desktop-spectrum-1.svg)) pictogram in de toolbar om van geavanceerde wijze van HTML (de HTML bronmening) aan het visuele ontwerpcanvas over te schakelen.

   Uw bewerkingen blijven behouden wanneer u van weergave verandert.
