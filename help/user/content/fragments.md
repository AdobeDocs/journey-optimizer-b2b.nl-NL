---
title: Fragmenten
description: Leer hoe u visuele inhoudsfragmenten maakt en gebruikt als herbruikbare onderdelen voor e-mails en e-mailsjablonen in Adobe Journey Optimizer B2B Edition.
feature: Content, Email Authoring
exl-id: 3c1d2ca0-d009-4a2a-9d81-1a838845b7fa
source-git-commit: 8e55e4444a363a5699574c2fa1ed256fdb690dd0
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 0%

---

# Fragmenten

Een fragment is een herbruikbare component waarnaar in een of meer e-mailsjablonen in Adobe Journey Optimizer B2B Edition kan worden verwezen. Het is doorgaans een blok inhoud (tekst, afbeelding of beide) dat u vooraf kunt maken en snel kunt invoegen in een e-mailsjabloon. Met deze functionaliteit kunt u meerdere aangepaste inhoudsblokken vooraf samenstellen voor gebruik door uw leden van uw marketingteam om e-mailinhoud samen te stellen voor een verbeterd ontwerpproces. Veelvoorkomende gebruiksgevallen zijn inhoudsblokken voor kop- en voetteksten voor e-mail, uitnodigingsbanners voor gebeurtenissen en seizoensgebonden begroetingen.

U kunt zo veel mogelijk gebruikmaken van fragmenten in uw workflows:

* _creeer uw eigen fragmenten_ - creeer visuele fragmenten, of van kras of door inhoud als fragment van de visuele inhoudsredacteur op te slaan.
* _hergebruik fragmenten_ - gebruik hen zo vele tijden zoals nodig in uw inhoud.

## Visuele fragmenten

Visuele fragmenten zijn vooraf gedefinieerde visuele blokken die zijn gemaakt met de visuele inhoudeditor die u kunt hergebruiken in meerdere e-mails of e-mailsjablonen. Het huidige bereik van Journey Optimizer B2B Edition en deze documentatie zijn alleen van visuele fragmenten. Op expressie gebaseerde fragmenten worden nog niet ondersteund in Journey Optimizer B2B Edition.

## Fragmenten openen en beheren

Ga naar de linkernavigatie en klik op **[!UICONTROL Content Management]** > **[!UICONTROL Fragments]** om visuele fragmenten te openen in Adobe Journey Optimizer B2B Edition. Met deze actie opent u een pagina met lijsten met alle fragmenten die in de instantie in een tabel zijn gemaakt.

![ heb toegang tot de fragmentbibliotheek ](./assets/fragments-list.png){width="700" zoomable="yes"}

De tabel wordt gesorteerd op de kolom _[!UICONTROL Modified]_, waarbij de meest recente bijgewerkte fragmenten standaard bovenaan staan. Klik op de kolomtitel om te schakelen tussen oplopend en aflopend.

Als u naar een fragment op naam wilt zoeken, voert u in de zoekbalk een tekenreeks in voor een overeenkomst. Klik het _pictogram van de Filter_ om de getoonde punten volgens uw gespecificeerde criteria te filtreren.

![ filter de getoonde fragmenten ](./assets/fragments-list-filtered.png){width="700" zoomable="yes"}

Pas de kolommen aan die u in de lijst wilt tonen door _te klikken aanpassen lijst_ pictogram op het hoogste recht. Selecteer de kolommen die u wilt weergeven en klik op **[!UICONTROL Apply]** .

## Fragmenten maken

U kunt nieuwe visuele fragmenten maken in Journey Optimizer B2B Edition door op **[!UICONTROL Create fragment]** rechtsboven te klikken.

1. Voer in het dialoogvenster _[!UICONTROL Create fragment]_een handige **[!UICONTROL Name]**en **[!UICONTROL Description]**(optioneel) in.

   Fragmentvereisten:

   * Naam - maximaal 100 tekens, moet uniek en hoofdlettergevoelig zijn

   * Beschrijving - Maximaal 300 tekens

   * Alpha, numerieke tekens en speciale tekens zijn toegestaan

   * Gereserveerde karakters zijn **_niet toegestaan_**: `\ / : * ? " < > |`

   ![ creeer fragmentdialoog ](./assets/assets-fragments-create-dialog.png){width="400"}

1. Klik op **[!UICONTROL Create]**.

   De visuele inhoudeditor wordt geopend met een leeg canvas.

<!-- To be linked to the corresponding sections on this page: Adobe Journey Optimizer B2B Edition - Email Templates

Adding structure and content
Adding assets
Navigating the layers
Previewing & editing URLs
View options
More options -->

### Structuur en inhoud toevoegen {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Structuurcomponenten toevoegen"
>abstract="Structuurcomponenten definiëren de indeling van het fragment. De belemmering en laat vallen component van de a **Structuur** in het canvas beginnen de inhoud van uw fragment te ontwerpen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Informatie over inhoudscomponenten"
>abstract="Inhoudscomponenten zijn lege plaatsaanduidingen voor inhoud die u kunt gebruiken om de lay-out van een fragment te maken."

{{$include /help/_includes/content-design-components.md}}

### Elementen toevoegen

{{$include /help/_includes/content-design-assets.md}}

### Navigeren door de lagen, instellingen en stijlen

{{$include /help/_includes/content-design-navigation.md}}

### Inhoud personaliseren

{{$include /help/_includes/content-design-personalization.md}}

### Gekoppelde URL-tracking bewerken

{{$include /help/_includes/content-design-links.md}}

## Fragmentdetails weergeven

Klik op de naam van een fragment in de lijstpagina om de pagina met fragmentdetails te openen. U kunt het fragment bewerken, de naam van het fragment wijzigen of de fragmentbeschrijving bijwerken. Voer updates uit en klik buiten het naam- of beschrijvingsveld om wijzigingen automatisch op te slaan.

>[!NOTE]
>
>Als een gepubliceerd fragment wordt gebruikt door een e-mailsjabloon, kunt u de naam niet wijzigen of de inhoud niet bewerken. U kunt een conceptversie maken als u wijzigingen in het fragment wilt aanbrengen.

![ de details van de Mening voor een gepubliceerd fragment ](./assets/fragment-details-published.png){width="600" zoomable="yes"}

Klik op **[!UICONTROL Edit fragment]** om het fragment te openen in de visuele inhoudeditor.

Ga de mening op elk ogenblik weg door de _Achter_ pijl bij de hoogste linkerzijde te klikken, die u aan de _pagina van de de 3} lijst van Fragmenten {terugkeert._

## Fragment weergeven dat wordt gebruikt door verwijzingen

Klik op het tabblad **[!UICONTROL Used By]** op de pagina met fragmentdetails om details weer te geven over waar het fragment momenteel wordt gebruikt in Journey Optimizer B2B Edition, in e-mails, e-mailsjablonen en fragmenten.

>[!IMPORTANT]
>
>Elk fragment dat momenteel wordt gebruikt door een e-mailsjabloon of e-mailsjabloon, kan niet worden verwijderd.

De verwijzingen worden getoond volgens categorie: _E-mail_ of _E-mailmalplaatje_. E-mails in Journey Optimizer B2B Edition worden ingesloten en geschreven binnen accountreizen, zodat de bovenliggende reis van de e-mail die het fragment gebruikt, in verwijzingen wordt weergegeven.

![ Gebruikt door verwijzingen voor het fragment ](./assets/fragment-used-by-published.png){width="600" zoomable="yes"}

Klik op de koppeling om de bijbehorende sjabloon voor e-mail of e-mail te openen waarin het fragment wordt gebruikt.

## Fragmenten verwijderen

Om het even welk fragment dat momenteel in gebruik door om het even welk e-mail of e-mailmalplaatje is kan niet worden geschrapt, zodat controleert u _gebruikt-door_ verwijzingen alvorens een fragmentverwijdering in werking te stellen. Een verwijdering kan ook niet ongedaan worden gemaakt. Controleer dit voordat u een verwijderactie start.

U kunt een fragment op een van de volgende manieren verwijderen:

* Klik op **[!UICONTROL Delete]** in de fragmentdetails aan de rechterkant.
* Klik op de aanbiedingspagina van _[!UICONTROL Fragments]_op de ovaal naast het fragment en kies **[!UICONTROL Delete]**.

Met deze handeling wordt een bevestigingsvenster geopend. U kunt het proces afbreken door op **[!UICONTROL Cancel]** te klikken of op **[!UICONTROL Delete]** te klikken om het verwijderen te bevestigen.

![ de fragmentdialoog van de Schrapping ](./assets/fragment-delete-dialog.png){width="400"}

Als het fragment momenteel in gebruik is, wordt een informatief dialoogvenster geopend waarin u wordt gewaarschuwd dat het fragment niet kan worden verwijderd. Klik op **[!UICONTROL OK]** om het verwijderen af te breken.

![ de fragmentdialoog van de Schrapping - kan geen in-gebruiks fragment schrappen ](./assets/fragment-delete-dialog-in-use.png){width="400"}

## Fragmenten bewerken

U kunt een fragment op een van de volgende manieren bewerken:

* Klik op **[!UICONTROL Edit]** in de fragmentdetails aan de rechterkant.
* Klik op de aanbiedingspagina van _[!UICONTROL Fragments]_op de ovaal naast het fragment en kies **[!UICONTROL Edit]**.

Deze actie opent het fragment in een visuele inhoudsredacteur, waar u het fragment kunt uitgeven gebruikend om het even welke eigenschappen voor [ creërend een fragment ](#create-fragments).

## Fragmenten dupliceren

U kunt een fragment op een van de volgende manieren dupliceren:

* Van de _[!UICONTROL Fragments]_lijstpagina, klik_ Meer _(**...**) pictogram naast de fragmentnaam en kies **[!UICONTROL Duplicate]**.
* Klik rechtsboven op de pagina met fragmentdetails op **[!UICONTROL ... More]** en kies **[!UICONTROL Duplicate]** .

![ dupliceer het fragment ](./assets/fragment-details-duplicate.png){width="600" zoomable="yes"}

Voer in het dialoogvenster een nuttige naam (uniek) en beschrijving in. Klik op **[!UICONTROL Duplicate]** om de handeling te voltooien.

![ ga een naam en een beschrijving voor het gedupliceerde fragment ](./assets/fragment-duplicate-dialog.png){width="400"} in

Het gedupliceerde (nieuwe) fragment verschijnt dan in de _lijst van Fragmenten_.

## Een fragment opslaan vanuit e-mail- of sjablooninhoud

Wanneer u een e-mail- of e-mailsjabloon maakt/bewerkt in de visuele inhoudeditor, kunt u de inhoud geheel of gedeeltelijk opslaan als een fragment, zodat deze opnieuw kan worden gebruikt.

1. Wanneer u inhoud als een fragment wilt opslaan, klikt u op **[!UICONTROL More]** en kiest u **[!UICONTROL Save as Fragment]** .

1. Selecteer de verschillende elementen die u in het fragment wilt opnemen.

   Selecteer meerdere structuren door de knop Shift of Control ingedrukt te houden.

   U kunt alleen structuren selecteren die aan elkaar grenzen en met de interface kunt u geen niet-aangrenzende elementen selecteren.

1. Selecteer de inhoud en klik op **[!UICONTROL Create]** rechtsboven.

1. Voer in het dialoogvenster een nuttige naam en beschrijving voor het fragment in. Klik vervolgens op **[!UICONTROL Create]** .

   Het nieuwe fragment wordt dan getoond in de _Fragmenten_ het vermelden pagina en is ook beschikbaar voor gebruik binnen e-mail en e-mailmalplaatjes.

## Visuele fragmenten toevoegen aan uw e-mail- of sjablooninhoud

Fragmenten zijn ontworpen voor hergebruik en kunnen worden ingevoegd voor het ontwerpen van sjablonen voor e-mail en e-mail. U kunt maximaal 30 fragmenten in een e-mail of sjabloon toevoegen. Fragmenten kunnen tot één niveau worden genest.

>[!BEGINTABS]

>[!TAB  voegt fragmenten aan e-mail ] toe

1. Navigeer naar **[!UICONTROL Account Journeys]** en open een bestaande reis of maak een nieuwe reis.

1. Creeer een [_[!UICONTROL Send Email]_knoop ](./email-authoring.md#add-an-email-action-in-an-account-journey).

1. Creeer of geef [ e-mailinhoud voor de knoop ](./email-authoring.md#create-the-email-content) uit.

1. De belemmering en laat vallen een punt van het **[!UICONTROL Components]** menu om a _structuur_ voor het fragment te verstrekken.

1. Om de lijst van gepubliceerde fragmenten te openen, klik het _pictogram van Fragmenten_.

   U kunt:
   * Sorteer de aanbieding.
   * Blader naar de lijst, zoek de lijst en filter deze.
   * Schakelen tussen kaart- (miniatuur) en lijstweergaven.
   * Vernieuw de lijst om een van de onlangs gemaakte fragmenten weer te geven.

   ![ Onderzoek naar een fragment in de visuele ontwerper ](./assets/fragments-list-designer-search.png){width="600"}

1. Sleep een van de fragmenten naar de tijdelijke aanduiding voor het structuuronderdeel.

   De editor geeft het fragment weer binnen de sectie/het element van de e-mailstructuur.

De inhoud van het fragment wordt dynamisch bijgewerkt binnen de structuur om een visuele weergave te geven van hoe de inhoud in de e-mail wordt weergegeven.

>[!TIP]
>
>Als u wilt dat het fragment de volledige horizontale lay-out binnen de e-mail in beslag neemt, voegt u een [!UICONTROL 1:1 column] -structuur toe en sleept u het fragment er vervolgens in.

Nadat het e-mailbericht is opgeslagen, wordt het weergegeven op de pagina met fragmentdetails wanneer het tabblad _[!UICONTROL Used By]_is geselecteerd. Fragmenten die aan een e-mail zijn toegevoegd, kunnen niet worden bewerkt in de e-mail of sjabloon. Het gepubliceerde bronfragment definieert de inhoud.

>[!TAB  voegt fragmenten aan een e-mailmalplaatje ] toe

1. Klik in de linkernavigatie op **[!UICONTROL Content Management]** > **[!UICONTROL Templates]** .

1. Maak een nieuwe sjabloon of open een bestaande e-mailsjabloon en klik op **[!UICONTROL Edit Email Template]** .

1. De belemmering en laat vallen een punt van het **[!UICONTROL Components]** menu om a _structuur_ voor het fragment te verstrekken.

1. Om de fragmenten lijst te openen, klik het _pictogram van Fragmenten_.

   U kunt:
   * Sorteer de aanbieding.
   * Blader naar de lijst, zoek de lijst en filter deze.
   * Schakelen tussen kaart- (miniatuur) en lijstweergaven.
   * Vernieuw de lijst om een van de onlangs gemaakte fragmenten weer te geven.

   ![ Onderzoek naar een fragment in de visuele ontwerper ](./assets/fragments-list-designer-search.png){width="600"}

1. Sleep een van de fragmenten naar de tijdelijke aanduiding voor het structuuronderdeel.

   De editor geeft het fragment weer binnen de sectie/het element van de sjabloonstructuur voor e-mail.

1. Sleep een van de fragmenten naar de tijdelijke aanduiding voor het structuuronderdeel.

   De editor geeft het fragment weer binnen de sectie/het element van de sjabloonstructuur voor e-mail.

>[!TIP]
>
>Als u wilt dat het fragment de volledige horizontale lay-out binnen de e-mailsjabloon beslaat, voegt u een _[!UICONTROL 1:1 column]_-structuur toe en sleept u het fragment er vervolgens in.

Nadat de e-mailsjabloon is opgeslagen, wordt deze weergegeven op de pagina met fragmentdetails wanneer het tabblad _[!UICONTROL Used By]_is geselecteerd. Fragmenten die aan een e-mailsjabloon zijn toegevoegd, kunnen niet worden bewerkt in de sjabloon. Het gepubliceerde bronfragment definieert de inhoud.

>[!ENDTABS]

## Fragmentacties tijdens het ontwerpen van e-mail- en sjablonen

Wanneer een fragment aan een e-mailsjabloon of e-mailsjabloon wordt toegevoegd, kan de fragmentinhoud niet worden bewerkt in de e-mail of sjabloon. U kunt echter de volgende handelingen toepassen:

* **[!UICONTROL Delete]** - Deze actie verwijdert het fragment uit de huidige e-mail- of e-mailsjablooninhoud (de fragmentbron blijft ongewijzigd).
* **[!UICONTROL Refresh]** - Met deze handeling wordt de inhoud van het fragment in de huidige e-mailsjabloon of de huidige e-mailsjabloon vernieuwd. Vernieuwen is handig als u recente bewerkingen aan het fragment wilt spiegelen nadat u het fragment hebt toegevoegd aan de e-mailsjabloon of de e-mailsjabloon.
* **[!UICONTROL Duplicate]** - Met deze actie wordt het fragment binnen dezelfde e-mail- of e-mailsjabloon in de editor gedupliceerd, met dezelfde afmetingen en net eronder toegevoegd.
* **[!UICONTROL Open Fragment]** - Met deze actie opent u een nieuw browsertabblad met de pagina voor de fragmenteditor en details.
* **[!UICONTROL Break inheritance]** - Met deze actie wordt de overerving van het fragment (en de wijzigingen ervan) van de bron verbroken. Gebruik deze handeling om de fragmentinhoud beschikbaar te maken als onafhankelijke en bewerkbare inhoud binnen de e-mail- of e-mailsjabloon. Deze actie verwijdert ook het e-mail of e-mailmalplaatje uit _Gebruikt door_ verwijzing voor het originele fragment.

Wanneer u het fragment op de editorpagina selecteert, zijn deze acties beschikbaar bij de contexttoolbar en het eigenschappenpaneel op het recht.

![ pas acties op het geselecteerde fragment ](./assets/fragment-actions-email-authoring.png){width="600" zoomable="yes"} toe