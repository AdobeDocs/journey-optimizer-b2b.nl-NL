---
title: E-mailsjablonen
description: Leer hoe u e-mailsjablonen kunt maken en bewerken die u kunt gebruiken voor het eenvoudig en efficiënt maken van e-mails over een accountreis.
feature: Email Authoring, Content
exl-id: 4e146802-e3ef-4528-b581-191e28afe86f
source-git-commit: 16b798f18f72eeb63e68a8d32e69164930aa1e22
workflow-type: tm+mt
source-wordcount: '2523'
ht-degree: 0%

---

# E-mailsjablonen

Voor een versnelde en verbeterde ontwerpprocedure kunt u zelfstandige e-mailsjablonen maken om aangepaste inhoud te hergebruiken voor alle Adobe Journey Optimizer B2B Edition-accountreizen. Via sjablonen kunnen leden van uw inhoudgerichte team buiten de reis aan e-mailinhoud werken. Marketing strategen kunnen deze standalone sjablonen vervolgens hergebruiken en aanpassen binnen hun accountreizen. Eén teamlid is bijvoorbeeld alleen verantwoordelijk voor de inhoud, zonder toegang tot reizen naar de account. Ze kunnen echter een e-mailsjabloon maken die marketers kunnen selecteren als beginpunt voor e-mailcommunicatie en deze kunnen aanpassen aan de vereisten voor de reis.

## E-mailsjablonen openen en beheren

Ga naar de linkernavigatie en klik op **[!UICONTROL Content Management]** > **[!UICONTROL Templates]** om e-mailsjablonen te openen in Adobe Journey Optimizer B2B Edition. Met deze handeling wordt een aanbiedingspagina geopend met alle e-mailsjablonen die zijn gemaakt in het exemplaar dat in een tabel wordt vermeld.

De tabel wordt gesorteerd op de kolom _[!UICONTROL Modified]_. Standaard staan de laatst bijgewerkte sjablonen boven aan de lijst. Klik op de kolomtitel om te schakelen tussen oplopend en aflopend.

Als u naar een sjabloon op naam wilt zoeken, voert u een tekstreeks in de zoekbalk in. Klik het _pictogram van de Filter_ bij de bovenkant verlaten om de lijst volgens verwezenlijking of wijzigingsdata, en malplaatjes te filtreren die u hebt gecreeerd of gewijzigd.

![ heb toegang tot de bibliotheek en de filter van e-mailmalplaatjes door naam en data ](./assets/templates-list-search-filter.png){width="700" zoomable="yes"}

Pas de kolommen aan die u in de lijst wilt tonen door _te klikken aanpassen lijst_ pictogram op het hoogste recht. Selecteer de kolommen die u wilt weergeven en klik op **[!UICONTROL Apply]** .

Vanaf de aanbiedingspagina kun je de in de volgende secties beschreven acties uitvoeren.

## E-mailsjablonen maken

U kunt een nieuwe e-mailsjabloon maken op basis van de pagina met e-mailsjablonen door rechtsboven op **[!UICONTROL Create template]** te klikken.

1. Voer in het dialoogvenster een handige **[!UICONTROL Name]** en **[!UICONTROL Description]** (optioneel) in.

   ![ ga aanvankelijke eigenschappen voor het nieuwe e-mailmalplaatje ](./assets/templates-create-dialog.png){width="400"} in

1. Stel het beginpunt in **[!UICONTROL Image source]** .

   Als u een abonnement op Experience Manager Assets as a Cloud Service hebt samen met de standaard Adobe Marketo Engage Design Studio, kunt u afbeeldingselementen kiezen uit een van beide bronnen. U doet dit door de afbeeldingsbron te selecteren op het moment dat u het bestand maakt voor een e-mailsjabloon of een visueel fragment. U kunt de afbeeldingsbron echter ook selecteren wanneer u de inhoud bewerkt.

   Voor meer informatie over beeldbronnen, zie [ Assets ](./assets-overview.md).

1. Klik op **[!UICONTROL Create]**.

De pagina _[!UICONTROL Design your template]_wordt geopend en bevat meerdere opties voor het maken van de sjabloon:_[!UICONTROL Design from scratch]_ , _[!UICONTROL Import HTML]_of_[!UICONTROL Select design template]_ .

![ kies hoe u met uw ontwerp van het e-mailmalplaatje wilt beginnen ](./assets/templates-create-design.png){width="800" zoomable="yes"}

### Ontwerpen vanaf nul

Gebruik de e-mailontwerper om de structuur van uw e-mailinhoud te definiëren. Door structurele componenten toe te voegen en te bewegen met eenvoudige belemmering-en-dalingsacties, kunt u de vorm van de herbruikbare e-mailinhoud binnen seconden ontwerpen.

1. Selecteer de optie **[!UICONTROL Design from scratch]** op de startpagina van _[!UICONTROL Design your template]_.

1. Begin met het ontwerpen van uw inhoud door componenten naar het canvas te slepen en neer te zetten om de structurele lay-out van de e-mail te bepalen.

   De beschikbare ontwerphulpmiddelen zijn gelijkwaardig aan de hulpmiddelen die voor [ worden gebruikt e-mailauthoring ](./email-authoring.md). Het verschil is dat deze inhoud vervolgens wordt opgeslagen als een sjabloon die opnieuw kan worden gebruikt voor meerdere verzendknooppunten in een accountreis.

### HTML importeren

Met Adobe Journey Optimizer B2B Edition kunt u bestaande HTML-inhoud importeren om uw e-mailsjablonen te ontwerpen. Deze inhoud kan:

* Een HTML-bestand met een opgenomen stijlblad.
* Een ZIP-bestand dat een HTML-bestand, de stijlpagina (.css) en afbeeldingen bevat

  >[!NOTE]
  >
  >Er gelden geen beperkingen voor de .zip-bestandsstructuur. Verwijzingen moeten echter relatief zijn en passen bij de boomstructuur van de ZIP-map.

_om een dossier in te voeren dat de inhoud van HTML bevat:_

1. Selecteer de optie **[!UICONTROL Import HTML]** op de startpagina van _[!UICONTROL Design your template]_.

1. Sleep het HTML- of ZIP-bestand met de inhoud van uw HTML en klik op **[!UICONTROL Import]** .

   Nadat de inhoud van de HTML wordt geupload, is uw inhoud op _wijze van de Verenigbaarheid_. In deze modus kunt u alleen uw tekst aanpassen, koppelingen toevoegen of elementen aan uw inhoud toevoegen.

1. Als u de inhoudcomponenten van de e-mailontwerper wilt gebruiken, klikt u op het tabblad **[!UICONTROL HTML converter]** en klikt u op **[!UICONTROL Convert]** .

>[!NOTE]
>
>Als u een `<table>` -tag als eerste laag in een HTML-bestand gebruikt, kan dit leiden tot stijlverlies, zoals de achtergrond- en breedte-instellingen in de bovenste laagtag.

U kunt de geïmporteerde inhoud naar wens aanpassen met de gereedschappen in de visuele e-maileditor.

### Een ontwerpsjabloon selecteren

Op de startpagina van _[!UICONTROL Design your template]_gebruikt u de sectie Ontwerpsjabloon selecteren om uw inhoud op te bouwen op basis van een sjabloon. U kunt een voorbeeldsjabloon of een opgeslagen e-mailsjabloon uit uw Journey Optimizer B2B Edition-exemplaar gebruiken.

>[!BEGINTABS]

>[!TAB  Bewaarde malplaatjes ]

Op het _Ontwerp uw malplaatje_ homepage, wordt het _malplaatjes van de Steekproef_ lusje geselecteerd door gebrek. Als u een aangepaste sjabloon wilt gebruiken, selecteert u de tab **[!UICONTROL Saved templates]** .

De lijst met alle e-mailsjablonen die in de huidige sandbox zijn gemaakt, wordt weergegeven. U kunt ze sorteren op _[!UICONTROL Name]_,_[!UICONTROL Last modified]_ en _[!UICONTROL Last created]_.

![ kies een bewaard malplaatje ](./assets/templates-design-saved-sort-by.png){width="800" zoomable="yes"}

Selecteer de gewenste sjabloon in de lijst.

Na de selectie wordt een voorbeeld van de sjabloon weergegeven. In de voorvertoningsmodus kunt u met de rechter- en linkerpijltoets navigeren tussen alle sjablonen van één categorie (voorbeeld of opgeslagen, afhankelijk van uw selectie).

![ Voorproef het bewaarde malplaatje ](./assets/templates-design-saved-preview.png){width="800" zoomable="yes"}

Wanneer de weergave overeenkomt met wat u wilt gebruiken, klikt u op **[!UICONTROL Use this template]** rechtsboven in het voorvertoningsvenster.

Met deze actie kopieert u de inhoud naar de visuele ontwerper van de inhoud, waar u de inhoud desgewenst kunt bewerken.

>[!TAB  malplaatje van de Steekproef ]

De Uitgave van Adobe Journey Optimizer B2B biedt een selectie van e-mailmalplaatjes aan die _worden aangeboden uit-van-de-doos_, die voor het creëren van e-mails en e-mailmalplaatjes kan worden gebruikt.

![ kies een malplaatje dat door Adobe ](./assets/templates-design-samples.png){width="800" zoomable="yes"} wordt verstrekt

>[!ENDTABS]

## Structuur en inhoud toevoegen

Begin met het ontwerpen van uw inhoud door structuren van het menu **[!UICONTROL Components]** naar het canvas te slepen om de lay-out van uw e-mail te definiëren.

Voeg zoveel structuren toe als u nodig hebt en bewerk de instellingen in de elementeigenschappen aan de rechterkant.

Selecteer de component _[!UICONTROL n:n column]_om het aantal kolommen van uw keuze (tussen drie en 10) te definiëren. Definieer de breedte van elke kolom door de pijlen onderaan te verplaatsen.

>[!NOTE]
>
>Elke kolomgrootte mag niet kleiner zijn dan 10% van de totale breedte van de structuurcomponent. U kunt alleen lege kolommen verwijderen.

Vouw de sectie **[!UICONTROL Contents]** uit en voeg zoveel elementen toe als u nodig hebt in een of meer structuurcomponenten.



Elke component kan verder worden aangepast met de tabbladen _[!UICONTROL Settings]_of_[!UICONTROL Style]_ in het rechterdeelvenster. U kunt bijvoorbeeld de tekststijl, opvulling of marge van elke component wijzigen.

### Navigeren door de lagen, instellingen en stijl

In het volgende voorbeeld worden de stappen beschreven voor het aanpassen van de opvulling en de verticale uitlijning binnen een structuurcomponent die uit drie kolommen bestaat.

1. Selecteer de structuurcomponent rechtstreeks in de e-mail of met behulp van de navigatiestructuur die beschikbaar is in het linkermenu.

1. Klik in de werkbalk op **[!UICONTROL Select a column]** en kies de werkbalk die u wilt bewerken.

   ![ n:n kolomcomponent die in het canvas ](./assets/visual-designer-n-n-column.png){width="800" zoomable="yes"} wordt getoond

   U kunt deze ook selecteren in de boomstructuur. De bewerkbare parameters voor die kolom worden weergegeven op het tabblad _[!UICONTROL Styles]_.

1. Onder **[!UICONTROL Alignment]**, selecteer de _Hoogste_, _Midden_, of _Onderste_ pictogram.

1. Definieer onder **[!UICONTROL Padding]** de opvulling voor alle zijden.

   Selecteer **[!UICONTROL Different padding for each side]** als u de opvulling wilt verfijnen. Klik op het vergrendelingspictogram om de synchronisatie te verbreken.

1. Pas indien nodig de uitlijning en opvulling voor de andere kolommen aan.

1. Sla uw wijzigingen op.

### Inhoud personaliseren

In het volgende voorbeeld worden stappen beschreven voor het aanpassen van sjablooninhoud met behulp van lood-/accountkenmerken en systeemtokens.

1. Selecteer de tekstcomponent en klik _verpersoonlijking_ pictogram in de toolbar toevoegen.

   ![ klik het Persoonlijke pictogram ](./assets/visual-designer-personalize-icon.png){width="500"}

   Deze actie opent _geeft Personalization_ dialoog uit.

1. Klik **+** of **..** om een teken aan de lege ruimte toe te voegen.

   ![ construeert gepersonaliseerde tekst gebruikend tokens ](./assets/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.

### Fragmenten toevoegen

In de visuele inhoudsredacteur, wordt het _pictogram van Fragmenten_ getoond op de linkerzijde. In het volgende voorbeeld worden de stappen beschreven die moeten worden uitgevoerd om fragmenten toe te voegen aan de sjablooninhoud.

1. Om de fragmenten lijst te openen, klik het _pictogram van Fragmenten_.

   U kunt:

   * Sorteer de aanbieding.
   * Blader door de lijst, zoek de lijst of filter deze.
   * Schakelen tussen de miniatuur- en lijstweergave.
   * Vernieuw de lijst om een van de onlangs gemaakte fragmenten weer te geven.

   ![ selecteer een fragment van de lijst ](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Sleep een van de fragmenten naar de tijdelijke aanduiding voor het structuuronderdeel.

   De editor geeft het fragment weer binnen de sectie/het element van de e-mailstructuur.

De inhoud van het fragment wordt dynamisch bijgewerkt binnen de structuur om een visuele weergave te geven van hoe de inhoud in de e-mail wordt weergegeven.

Als u het fragment wilt toevoegen zodat het de volledige horizontale lay-out binnen e-mail bezet, voeg een 1:1 kolomstructuur toe en sleep en zet dan het fragment in het.

Nadat het e-mailbericht is opgeslagen, wordt het weergegeven op de pagina met fragmentdetails wanneer u het tabblad _[!UICONTROL Used By]_in het overzicht selecteert. Fragmenten die aan een e-mailsjabloon worden toegevoegd, kunnen niet worden bewerkt in de sjabloon. De inhoud wordt gedefinieerd door het bronfragment.

### Elementen toevoegen

In de visuele inhoudsredacteur, selecteer het _Assets_ pictogram dat op de linkerzijde wordt getoond.

>[!NOTE]
>
>Als u een abonnement op Experience Manager Assets as a Cloud Service hebt samen met de standaard Adobe Marketo Engage Design Studio, kunt u afbeeldingselementen kiezen uit de bron die is geselecteerd op de pagina met sjabloondetails.

In het volgende voorbeeld worden de stappen beschreven waarmee elementen aan de sjablooninhoud worden toegevoegd:

1. Om de activa bibliotheek te openen, klik het _Assets_ pictogram.

   Vanuit de elementenkiezer kunt u rechtstreeks in de bronbibliotheek opgeslagen elementen selecteren.

1. Voeg een nieuw element toe door het afbeeldingselement naar een structuurcomponent te slepen.

1. Vervang een afbeeldingselement door dit op het canvas te selecteren en klik op **[!UICONTROL Select an asset]** in de brongereedschappen van de afbeelding.

   ![ Uitgezocht een middel van de bronbibliotheek ](./assets/visual-designer-select-an-asset.png){width="700" zoomable="yes"}

### URL&#39;s voorvertonen en bewerken

1. Klik op het pictogram _[!UICONTROL Links]_aan de linkerkant om alle URL&#39;s weer te geven van de inhoud die u wilt bijhouden.

1. Indien nodig, klik _uitgeven_ (potlood) pictogram en wijzig het _Volgend Type_ of _Etiket_ en voeg _Markeringen_ voor een verbinding toe.

![ klik Meer om tot malplaatjeacties ](./assets/visual-designer-links.png){width="500"} toegang te hebben

### Weergaveopties

Gebruik de opties voor weergave- en inhoudsvalidatie die beschikbaar zijn in de visuele e-maileditor.

* Zoom in of uit op de inhoud met de vooraf ingestelde zoomopties.

* Schakel de weergave van de inhoud in op Desktop, Mobiel of Alleen tekst/Onbewerkte tekst.
   * Klik het _Oog_ pictogram voor inhoudsvoorproef over apparaten.
   * Selecteer een van de apparaten die buiten het vak vallen of voer aangepaste afmetingen in om een voorvertoning van de inhoud weer te geven.

### Meer opties

Van _Meer opties_ selecteur in de visuele inhoudsredacteur, kunt u de volgende acties nemen:

![ klik Meer om tot malplaatjeacties ](./assets/visual-designer-more-menu.png){width="500"} toegang te hebben

* **malplaatje van het Terugstellen** - klik deze optie om het visuele e-maildesigner canvas aan een lege lei te ontruimen en de bouwende inhoud opnieuw te beginnen.
* **sparen als Fragment** - sparen alles of gedeelten van het als fragment dat over veelvoudige e-mail of e-mailmalplaatjes moet worden opnieuw gebruikt. U geeft een naam en een beschrijving voor de fragmenten op en geeft deze aan in de lijst met beschikbare fragmenten.
* **verander uw ontwerp** - terugkeer aan het _Ontwerp uw malplaatje_ pagina. Vanaf hier kunt u elke gewenste actie ondernemen zoals beschreven in de sectie &#39;E-mailsjablonen maken&#39;.
* **de HTML van de Uitvoer** - Download de inhoud in het visuele canvas aan uw lokaal systeem in HTML formaat dat als zip dossier wordt verpakt.

## E-mailsjabloondetails weergeven

Klik in de pagina Sjablonen op de naam van een e-mailsjabloon om de pagina met details van de e-mailsjabloon te openen. Vanaf hier kunt u de basiseigenschappen van de e-mailsjabloon bekijken en de visuele inhoudeditor openen om wijzigingen aan te brengen in de sjablooninhoud.

![ heb toegang tot de bibliotheek en de filter van e-mailmalplaatjes door naam en data ](./assets/template-details.png){width="700" zoomable="yes"}

* Geef de details van de e-mailsjabloon weer, zoals naam en beschrijving. Deze instellingen kunnen worden bewerkt. Klik buiten het beschrijvingsvak om de wijzigingen automatisch op te slaan.

* Bekijk de eigenschappen van de e-mailsjabloon, zoals gemaakt door, gemaakt op, laatst bijgewerkt op en gewijzigd door.

* Klik **[!UICONTROL More]** bij het hoogste recht om snelle acties op het e-mailmalplaatje, zoals _te voeren Dupliceert_ en _Schrapping_.

* Als er actieve waarschuwingen zijn (fouten en waarschuwingen voor de e-mailsjabloon), klikt u op **[!UICONTROL Alerts]** rechtsboven om de informatie weer te geven.

  Hoewel deze waarschuwingen het gebruik van de e-mailsjabloon voor het maken van e-mailberichten niet verbieden, biedt deze informatie de marketers in uw team inzicht in wat mogelijk niet werkt en de vereiste updates voordat deze voor levering kunnen worden gebruikt.

## E-mailsjabloon weergeven die wordt gebruikt door verwijzingen

Klik op het tabblad **[!UICONTROL Used By]** op de pagina met details over e-mailsjablonen om de details weer te geven van de plaats waar deze e-mailsjabloon wordt gebruikt in e-mailberichten over reizen van accounts.

![ klik Gebruikt door lusje om malplaatjegebruik ](./assets/template-details-used-by.png){width="400"} te controleren

E-mails in Journey Optimizer B2B Edition worden ingesloten en geschreven binnen reizen, zodat de bovenliggende reis van de e-mail die de sjabloon gebruikt, in verwijzingen wordt weergegeven.

* Als u op de koppeling klikt, gaat u naar het bijbehorende e-mailadres waar de e-mailsjabloon wordt gebruikt.

* Sluit de weergave op elk gewenst moment af door op de pijl Terug te klikken. Hiermee keert u terug naar de aanbiedingspagina.

## E-mailsjablonen bewerken

Deze actie kan worden uitgevoerd op:

* De detailpagina - klik **[!UICONTROL Edit email template]**.
* De lijstpagina - klik de ellips (**...**) naast een e-mailmalplaatje en kies **[!UICONTROL Edit]**.

Deze actie neemt u aan het _Ontwerp uw malplaatje_ pagina of de visuele pagina van de inhoudsredacteur die op het laatste bewaarde statuut van het e-mailmalplaatje wordt gebaseerd. Vanaf hier kunt u de inhoud van uw e-mailsjabloon naar wens bewerken. Zie [ E-mailmalplaatjes ](#create-email-templates) voor informatie over de het uitgeven opties creëren.

## E-mailsjablonen dupliceren

U kunt een e-mailsjabloon op een van de volgende manieren dupliceren:

* Vouw **[!UICONTROL More]** uit en klik op **[!UICONTROL Duplicate]** in de sjabloongegevens voor e-mail aan de rechterkant.

  ![ klik Meer om tot Schrapping toegang te hebben en acties te dupliceren ](./assets/template-details-more-menu.png){width="400"}

* Van de _E-mailMalplaatjes_ het vermelden pagina, klik de ellips (...) naast het malplaatje en kies **[!UICONTROL Duplicate]**.

Voer in het dialoogvenster een nuttige naam (uniek) en beschrijving in. Klik op **[!UICONTROL Duplicate]** om de handeling te voltooien.

Het gedupliceerde (nieuwe) e-mailmalplaatje verschijnt dan in de _E-mailMalplaatjes_ lijst.

## E-mailsjablonen verwijderen

Het verwijderen van een e-mailsjabloon kan niet ongedaan worden gemaakt. Controleer dit voordat u een verwijderactie start. U kunt een e-mailsjabloon op een van de volgende manieren verwijderen:

* Vouw **[!UICONTROL More]** uit en klik op **[!UICONTROL Delete]** in de sjabloondetails aan de rechterkant.
* Van de _E-mailMalplaatjes_ het vermelden pagina, klik de ellips (...) naast het malplaatje en kies **[!UICONTROL Delete]**.

  ![ klik... om tot de Acties van het Dupliceren en van de Schrapping ](./assets/templates-list-more-menu.png){width="500"} toegang te hebben

Met deze handeling wordt een bevestigingsvenster geopend. U kunt het proces afbreken door op **[!UICONTROL Cancel]** te klikken of op **[!UICONTROL Delete]** te klikken om het verwijderen te bevestigen.

## Handelingen bulksgewijs uitvoeren

Selecteer meerdere sjablonen tegelijk in de aanbiedingspagina van e-mailsjablonen door de selectievakjes links te selecteren. Onderaan wordt een banner weergegeven wanneer u meerdere sjablonen selecteert.

![ de banner van A toont het aantal geselecteerde malplaatjes en het pictogram van de Schrapping ](./assets/templates-multi-select-banner.png){width="600"}

**[!UICONTROL Delete]** — U kunt maximaal 20 sjablonen tegelijk verwijderen. In een bevestigingsvenster kunt u de handeling afbreken of bevestigen dat de sjablonen zijn verwijderd.

## Een e-mail ontwerpen op basis van een opgeslagen sjabloon

Van _creeer uw e-mail_ scherm, gebruik _Uitgezochte ontwerpmalplaatje_ sectie beginnen uw inhoud van een malplaatje te bouwen.

Voer de volgende stappen uit om uw inhoud te bouwen met een van de gemaakte e-mailsjablonen:

1. Heb toegang tot E-mail Designer van _inhoud_ pagina uitgeven.

   Op _creeer uw e-mail_ pagina, wordt het _malplaatjes van de Steekproef_ lusje geselecteerd door gebrek.

1. Als u een aangepaste e-mailsjabloon wilt gebruiken, selecteert u de tab **[!UICONTROL Saved templates]** .

   Op dit tabblad wordt een lijst weergegeven met alle e-mailsjablonen die in de sandbox zijn gemaakt. U kunt hen _sorteren door naam_, _Laatst gewijzigd_, en _laatst gecreeerd_.

1. Selecteer de gewenste sjabloon in de lijst.

   Na de selectie wordt een voorbeeld van de sjabloon weergegeven. In de voorvertoningsmodus kunt u met de rechter- en linkerpijltoets navigeren tussen alle sjablonen van één categorie (voorbeeld of opgeslagen, afhankelijk van uw selectie).

1. Klik op **[!UICONTROL Use this template]** rechtsboven.

1. Bewerk de inhoud zo nodig vanuit de visuele ontwerper.
