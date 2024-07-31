---
title: E-mailontwerp
description: Leer hoe u persoonlijke e-mailinhoud maakt die wordt gebruikt in Accountreizen.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: ce38e378ad316fb379cb649a4592ed831250296d
workflow-type: tm+mt
source-wordcount: '1214'
ht-degree: 0%

---

# E-mailontwerp

Gebruik Adobe Journey Optimizer B2B Edition om e-mailberichten naar uw klanten te verzenden. U kunt berichten maken, personaliseren en voorvertonen in de e-mailtoepassing van Designer.

## Een e-mailactie toevoegen aan een accountreis

U kunt e-mailleveringen instellen in een Account Journey wanneer u een _[!UICONTROL Take an action]_-knooppunt toevoegt en het volgende doet:

1. Kies **[!UICONTROL People]** voor het doel _[!UICONTROL Action on]_.
1. Kies **[!UICONTROL Send email]** bij _[!UICONTROL Action on people]_.
1. Kies **[!UICONTROL Create new email]** bij _[!UICONTROL Email source]_.

   U kunt ook de optie _[!UICONTROL Select email from Adobe Marketo Engage]_selecteren om een van de vooraf geschreven e-mails in het Marketo Engage te gebruiken en te verzenden als onderdeel van de Account Journey.

   >[!NOTE]
   >
   >Als u voor het eerst een e-mailbericht maakt, controleert u of het e-mailkanaal is geconfigureerd vanuit Adobe Marketo Engage. Meer leren, zie [ E-mailLeverbaarheid ](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) in de documentatie van het Marketo Engage verzekeren.

   ![ neem een actie - verzend een e-mail ](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. Klik onder aan het deelvenster _[!UICONTROL Take an action]_op **[!UICONTROL Create email]**.

1. Voer in het dialoogvenster een unieke **[!UICONTROL Name]** in voor de e-mail en een **[!UICONTROL Subject line]** .

   ![ creeer nieuwe e-maildialoog ](assets/create-new-email.png){width="400"}

1. Klik op **[!UICONTROL Create]**.

   In de sectie _[!UICONTROL Email properties]_van de pagina met e-mailinhoud zijn de velden_[!UICONTROL From email]_ en _[!UICONTROL Reply to address]_al geconfigureerd. U kunt waarden invoeren voor de velden_[!UICONTROL From name]_ en _[!UICONTROL Description]_(optioneel).

## E-mailinhoud maken

Klik op **[!UICONTROL Add email content]** boven in het voorvertoningsvenster van _[!UICONTROL Email]_.

![ Klik op E-mailinhoud toevoegen ](./assets/add-email-content.png){width="700" zoomable="yes"}

Met deze actie start u de e-mailtoepassing Designer, waarin u kunt kiezen hoe u uw e-mailbericht wilt ontwerpen. Hiervoor kunt u de volgende opties kiezen:

* [ Ontwerp uw e-mail van kras ](#design-your-email-from-scratch) gebruikend de interface van Designer E-mail.

* [ de Inhoud van de Invoer bestaande HTML ](#import-existing-html-content) van een dossier of een .zip omslag.

* [ selecteer een bestaand malplaatje ](#select-a-template) van een lijst van ingebouwde of douane e-mailmalplaatjes.

Om de onderwerpregel met de uitdrukkingsredacteur te vormen en te personaliseren, klik het _pictogram van Personalization_ en voeg om het even welke Marketo Engage tokens toe.

Nadat u de e-mailinhoud hebt gemaakt en aangepast, kunt u de inhoud exporteren voor validatie of later gebruik. Klik op **[!UICONTROL Export HTML]** om de inhoud op te slaan als een ZIP-bestand dat uw HTML en elementen bevat.

>[!TIP]
>
>Gebruik AI Assistant in Adobe Journey Optimizer B2B Edition, aangedreven door generatieve AI om uw inhoud naar het volgende niveau te tillen. Met AI Assistant kunt u de impact van uw leveringen optimaliseren door volledige e-mails, gerichte tekstinhoud en aanbevelingen voor AI Assistant te genereren voor afbeeldingen die op uw publiek zijn afgestemd. [Meer informatie](./ai-assistant-emails.md)

### Ontwerp uw e-mail helemaal zelf

1. Selecteer de optie **[!UICONTROL Design from scratch]** op de startpagina van Designer.

1. Als u het inhoudsontwerp wilt starten, sleept u een item van de **[!UICONTROL Structures]** naar het canvas.

   Herhaal deze stap voor elke structuurcomponent om de lay-out van uw e-mail samen te stellen.

1. Voeg zo vele punten van _Structuren_ toe aangezien u de montages voor elk in de ruit op het recht nodig hebt en uitgeeft.

   Selecteer de n:n kolomcomponent om het aantal kolommen van uw keus (tussen drie en 10) te bepalen. U kunt ook de breedte van elke kolom definiëren door de pijlen onder de kolom te verplaatsen.

   Elke kolomgrootte mag niet kleiner zijn dan 10% van de totale breedte van de structuurcomponent. Alleen lege kolommen kunnen worden verwijderd.

1. Vouw de sectie **[!UICONTROL Contents]** uit en voeg zoveel elementen toe als u nodig hebt in een of meer structuurcomponenten.

1. Indien nodig kunt u aanvullende aanpassingen aanbrengen voor elke component op de tabbladen _[!UICONTROL Settings]_of_[!UICONTROL Style]_ .

   U kunt bijvoorbeeld de tekststijl, opvulling of marge van elke component wijzigen.

1. Vanuit de elementkiezer kunt u rechtstreeks elementen selecteren die zijn opgeslagen in de Assets-bibliotheek.

   Dubbelklik op de map die uw elementen bevat. Sleep de items naar een structuurcomponent.

1. Voeg verpersoonlijkingsgebieden in om uw inhoud van profielattributen, publiekslidmaatschappen, Contextuele attributen, en meer aan te passen.

<!-- 1. Click **[!UICONTROL Enable condition content]** to add dynamic content and adapt the content to the targeted profiles based on conditional rules.
-->
1. Selecteer het tabblad **[!UICONTROL Links]** in het linkerdeelvenster om alle URL&#39;s van de inhoud weer te geven die worden bijgehouden.

   U kunt het _Volgend Type_ of _Etiket_ wijzigen en markeringen toevoegen indien nodig.

Indien nodig kunt u uw e-mail verder aanpassen door in het geavanceerde menu op **[!UICONTROL Switch to code editor]** te klikken. In de code-editor kunt u de broncode van de e-mail bewerken, bijvoorbeeld door tags voor bijhouden of aangepaste HTML toe te voegen.

>[!CAUTION]
>
>U kunt niet terugkeren naar de visuele ontwerper voor deze e-mail na het schakelen naar de coderedacteur.

Wanneer de inhoud gereed is, klikt u op **[!UICONTROL Simulate content]** boven om de rendering te controleren. U kunt kiezen voor de weergave Computer of Mobiel.

Klik op Opslaan als u klaar bent.

### Bestaande HTML-inhoud importeren

Geïmporteerde inhoud kan:

* Een HTML-bestand met een opgenomen stijlblad
* Een ZIP-map met een HTML-bestand, de stijlpagina (.css) en afbeeldingsbestanden

>[!NOTE]
>
>Er gelden geen beperkingen voor de .zip-bestandsstructuur. Verwijzingen moeten echter relatief zijn en passen bij de boomstructuur van de ZIP-map.

_om een dossier in te voeren dat de inhoud van HTML bevat:_

1. Selecteer **[!UICONTROL Import HTML]** op de homepage van E-mail Designer.

1. Sleep het HTML- of ZIP-bestand met de inhoud van uw HTML en klik op [!UICONTROL Import] .

   Wanneer de HTML inhoud uploadt volledig is, is uw inhoud op _wijze van de Verenigbaarheid_. In deze modus kunt u alleen uw tekst aanpassen, koppelingen toevoegen of elementen aan uw inhoud toevoegen.

### Een sjabloon selecteren

U kunt kiezen uit:

* Voorbeeldsjablonen. De Journey Optimizer-interface bevat 20 e-mailsjablonen die u kunt kiezen.

* Opgeslagen sjablonen.

* Een douanemalplaatje dat u of van kras gebruikend het _menu van Malplaatjes_ of van een e-mail in een reis gebruikend de _[!UICONTROL Save as content template]_optie creeerde.

_beginnen uw inhoud met één van de steekproef of bewaarde malplaatjes te bouwen:_

1. Heb toegang tot _E-mail Designer_ van de e-mailinhoud die werkruimte uitgeeft.

   Op de pagina _[!UICONTROL Create your email]_is de tab **[!UICONTROL Sample templates]**standaard geselecteerd.

1. Als u een aangepaste sjabloon wilt gebruiken, selecteert u de tab **[!UICONTROL Saved templates]** .

   De lijst met alle inhoudssjablonen die in de huidige sandbox zijn gemaakt, wordt weergegeven. U kunt ze sorteren op naam, Laatst gewijzigd of Laatst gemaakt.

1. Selecteer de gewenste sjabloon in de lijst.

1. Nadat u een categorie hebt geselecteerd, kunt u met de rechter- en linkerpijltoetsen navigeren tussen alle sjablonen van die categorie (voorbeeld of opgeslagen, afhankelijk van uw selectie).

1. Klik op **[!UICONTROL Use this template]** rechtsboven op de pagina.

1. Bewerk de inhoud zoals nodig in _E-mail Designer_.

## Waarschuwingen controleren

Terwijl u de inhoud van uw e-mailbericht ontwerpt, worden waarschuwingen weergegeven in de interface (rechtsboven op de pagina) wanneer er geen sleutelinstellingen aanwezig zijn.

Als deze knop niet wordt weergegeven, zijn er geen problemen gedetecteerd.

Er kunnen twee soorten waarschuwingen worden gedetecteerd:

* **_Waarschuwingen_** die naar aanbevelingen en beste praktijken, zoals verwijzen:

   * `The opt-out link is not present in the email body`: u kunt het beste een koppeling zonder abonnement toevoegen aan uw e-mailadres.

     >[!NOTE]
     >
     >E-mailberichten in marketingstijl moeten een opt-out-koppeling bevatten, die niet vereist is voor transactieberichten.

   * `Text version of HTML is empty`: vergeet niet een tekstversie van uw e-mailhoofdtekst te definiëren die wordt gebruikt wanneer HTML-inhoud niet kan worden weergegeven.

   * `Empty link is present in email body`: controleer of alle koppelingen in uw e-mail correct zijn.

   * `Email size has exceeded the limit of 100KB`: zorg ervoor dat de grootte van uw e-mail voor optimale levering niet groter is dan 100 kB.

* **_Fouten_** die u verhinderen de reis/de campagne te testen of te activeren zolang zij niet, zoals worden opgelost:

   * `The subject line is missing`: e-mailonderwerpregel is verplicht.

   * `The email version of the message is empty`: deze fout wordt weergegeven wanneer de e-mailinhoud niet is geconfigureerd.

## E-mail controleren en testen

Wanneer de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om deze voor te vertonen, proefdrukken te verzenden en de weergave ervan in populaire desktops, mobiele clients en webclients te beheren. Als u persoonlijke inhoud hebt ingevoegd, kunt u met testprofielgegevens een voorvertoning weergeven van de weergave van deze inhoud in het bericht.

Als u een voorbeeld van de e-mailinhoud wilt weergeven, klikt u op **[!UICONTROL Simulate content]** en voegt u vervolgens een testprofiel toe om uw bericht te controleren met behulp van de testprofielgegevens.

![ Simuleer de e-mailinhoud om uw ontwerp te controleren ](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
