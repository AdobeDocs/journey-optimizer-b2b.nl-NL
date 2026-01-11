---
title: Web Experience Design
description: 'Webervaringen ontwerpen met visuele en niet-visuele editors: wijzigingen toevoegen, updates van inhoud beheren, klikken bijhouden inschakelen en inhoud personaliseren in Journey Optimizer B2B edition.'
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2234'
ht-degree: 0%

---

# Webervaringsontwerp

Nadat u [&#x200B; een Webervaring &#x200B;](./web-experiences.md#create-a-web-experience) creeert, gebruik de ruimte van het inhoudsontwerp om de wijzigingen te bepalen die u op uw Web-pagina&#39;s wilt toepassen.

>[!BEGINSHADEBOX]

**Eerste vereisten**

Voordat u webervaringen kunt ontwerpen, moet u ervoor zorgen dat aan de volgende vereisten wordt voldaan:

* Een productbeheerder heeft een of meer webkanalen geconfigureerd om de URL&#39;s (pagina&#39;s) te definiëren die moeten worden opgenomen voor een webervaring. Voor meer informatie, zie [&#x200B; het kanaalconfiguraties van het Web &#x200B;](../admin/configure-channels-web.md).

* Uw website heeft [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/collection/js/js-overview) (`alloy.js`) die voor bezoekersidentificatie en inhoudslevering wordt uitgevoerd. Adobe Experience Platform Web SDK versie 2.16 of hoger is vereist.

* U hebt de noodzakelijke [&#x200B; toestemmingen &#x200B;](../admin/user-management.md#b2b-product-permissions) om Webervaringen in een reis tot stand te brengen en te beheren:
   * _[!UICONTROL Campaigns]_>_[!UICONTROL Manage Campaigns]_ - Vereist om een actieknooppunt voor webpersonalisatie toe te voegen of bij te werken.
   * _[!UICONTROL Campaigns]_>_[!UICONTROL View Campaigns]_ - Vereist om details voor de actieknooppunten van een webpersonalisatie weer te geven.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Voordat u een webervaring ontwerpt, moet de browserextensie van de Adobe Experience Cloud Visual Editing Helper zijn geïnstalleerd voor uw webbrowser. Deze extensie is vereist voor het op betrouwbare wijze openen, schrijven en voorvertonen van uw webpagina&#39;s in de Journey Optimizer B2B edition-webervaringsontwerpruimte.<br/>
>
>Google Chrome en Microsoft Edge zijn momenteel de enige browsers die de extensie en het ontwerpen van webtoepassingen in Journey Optimizer B2B edition ondersteunen. Voor meer informatie, zie [&#x200B; de Visuele Uitgevende uitbreiding van de Helper installeren &#x200B;](./web-experiences.md#install-the-visual-editing-helper-extension).

## Webervaringseditors

Journey Optimizer B2B edition biedt twee typen editors voor het ontwerpen van webwijzigingen:

| Editor | Beschrijving | Best voor |
| ------ | ----------- | -------- |
| [&#x200B; Visuele redacteur &#x200B;](#visual-editor) | Een redacteur van WYSIWYG (_What You See Is What You Get_) die uw website toont en u toestaat om elementen direct te selecteren en te wijzigen. Het vereist de [&#x200B; Visuele het Uitgeven uitbreiding van de Helper &#x200B;](./web-experiences.md#install-the-visual-editing-helper-extension) in Google Chrome of het Webbrowser van Microsoft Edge. | Visuele wijzigingen aanbrengen in zichtbare pagina-elementen, zoals tekst, afbeeldingen, knoppen en banners. |
| [&#x200B; niet-visuele redacteur &#x200B;](#non-visual-editor) | Een op code-gebaseerde redacteur voor het toepassen van wijzigingen die niet door de visuele redacteur kunnen worden gemaakt. | Elementen aanwijzen die moeilijk visueel kunnen worden geselecteerd, geavanceerde CSS-wijzigingen toepassen of verborgen elementen aanpassen. |

Gebruik in de webervaringseigenschappen de optie **[!UICONTROL Visual editor]** om het type editor te bepalen. Schakel de optie in om de visuele editor te gebruiken of schakel deze uit om de niet-visuele editor te gebruiken.

![&#x200B; Toegelaten Visuele editoroptie &#x200B;](./assets/web-experience-design-visual-editor-option.png){width="400"}

## Visuele editor {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="De modus Bladeren gebruiken"
>abstract="In deze modus navigeert u naar de exacte pagina die u wilt aanpassen aan de geselecteerde webkanaalconfiguratie."

De visuele editor laadt de webpagina&#39;s in een iframe, waar u elementen kunt selecteren en wijzigingen rechtstreeks in de voorvertoning van de pagina kunt toepassen. Voer de volgende stappen uit om de visuele editor te gebruiken voor het ontwerpen van uw webervaring:

1. Klik op _[!UICONTROL Content]_&#x200B;in het rechterdeelvenster terwijl het tabblad **[!UICONTROL Edit web experience]**&#x200B;wordt weergegeven op de pagina met webervaringsdetails.

   De visuele editor laadt uw website op basis van de webkanaalconfiguratie.

   ![&#x200B; de ervarings visuele redacteur van het Web &#x200B;](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. Klik indien nodig rechtsboven op **[!UICONTROL Browse]** en gebruik de sitenavigatiebalk om de specifieke pagina te laden die u wilt wijzigen.

   U kunt de pagina-URL ook invoeren in het veld bovenaan.

   >[!NOTE]
   >
   >Zorg ervoor dat de geladen pagina overeenkomt met de URL-patronen die in de webkanaalconfiguratie zijn gedefinieerd. Klik op **[!UICONTROL View configuration details]** rechtsboven in het scherm om de URL- of pagina-overeenkomende regels voor de geselecteerde webkanaalconfiguratie weer te geven.

   ![&#x200B; doorbladert wijze in de visuele redacteur &#x200B;](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   Klik op **[!UICONTROL Design]** rechtsboven om de pagina in de ontwerpruimte te laden.

1. Als u wilt definiëren hoe de weergegeven pagina moet worden aangepast voor een webervaring, kunt u:

   * [&#x200B; Tussenvoegsel nieuwe componenten &#x200B;](#insert-new-components) (verdeler, HTML, beeld, rubriek, paragraaf, of verbinding) aan de pagina voor de Webervaring.

   * Selecteer om het even welk bestaand element van de pagina, zoals een beeld, een knoop, een paragraaf, tekst, een container, een rubriek, of een verbinding, en [&#x200B; wijzigen het voor de Webervaring &#x200B;](#modify-elements).

   * [&#x200B; voeg klik het volgen &#x200B;](#click-tracking-for-web-experiences) voor elementen toe om overeenkomst te meten en inzichten te verzamelen.

1. Herhaal stap 2 om de andere pagina&#39;s te laden die u wilt opnemen in de webervaring en herhaal stap 3 om de paginawijzigingen te definiëren.

1. [&#x200B; herzie uw wijzigingen &#x200B;](#manage-modifications) en maak om het even welke aanpassingen die nodig zijn.

1. Wanneer de wijzigingen zijn voltooid, klikt u op de pijl naar links boven de editor om terug te keren naar de eigenschappen van de webervaring.

### Elementen wijzigen

Klik op een element op de weergegeven pagina om deze te selecteren. Een blauwe rand geeft het geselecteerde element aan en een contextafhankelijke werkbalk wordt weergegeven met wijzigingsopties.

![&#x200B; selecteer een element om te wijzigen &#x200B;](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

De werkbalkopties zijn afhankelijk van het geselecteerde componenttype:

| Handeling | Beschrijving |
| ------ | ----------- |
| **[!UICONTROL Text options]** | Wijzig de klasse of tekstopmaak van het geselecteerde element. |
| **[!UICONTROL Choose image]** | Vervang de afbeeldingsbron of voeg een afbeelding toe aan het element. |
| **[!UICONTROL Edit link / Add link]** | Wijzig of voeg een verbinding URL toe. |
| **[!UICONTROL Arrange]** | Verplaats het geselecteerde element naar achteren of naar voren in de weergave. |
| **[!UICONTROL Add personalization]** | Voeg personalisatie in. |
| **[!UICONTROL Click track element]** | Klik op bijhouden toevoegen voor het element. |
| **[!UICONTROL Delete]** | Verwijder het geselecteerde element van de pagina. |

Voor een geselecteerd element worden de eigenschappen in het rechterdeelvenster aangepast aan de beschikbare opmaak en handelingen. Klik op een actiepictogram boven in het deelvenster om het geselecteerde element te dupliceren, te klikken op bijhouden, te verwijderen of te verbergen.

![&#x200B; klik een actiepictogram voor het geselecteerde element &#x200B;](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++Tekstelementen

1. Selecteer een tekstelement op de pagina.

1. Voer nieuwe tekstinhoud in of selecteer een tekenreeks en voer de vervangende tekst in.

1. (Facultatief) gebruik de [&#x200B; tekst het formatteren opties &#x200B;](./content-components.md#text), zoals gewaagd, cursief, en groepering.

1. Klik buiten het tekstelement om de wijziging toe te passen.

Voor meer informatie over tekst het stileren opties voor tekstcomponenten, zie [&#x200B; componenten van de Inhoud &#x200B;](./content-components.md#text).

+++

+++Afbeeldingselementen

1. Selecteer een afbeelding op de pagina.

1. Klik op het pictogram _[!UICONTROL Choose image]_&#x200B;op de contextafhankelijke werkbalk of in het rechterdeelvenster.

1. Blader naar een afbeelding in de bibliotheek met elementen en selecteer deze.

1. Gebruik de [&#x200B; beeld het stileren opties &#x200B;](./content-components.md#image) in het juiste paneel zoals nodig.

+++

+++Knopelementen

1. Selecteer een knopelement op de pagina.

1. (Optioneel) Voer nieuwe tekst in voor de knop of selecteer de tekenreeks en voer de vervangende tekst in.

   U kunt personalisatie gebruiken om de knooptekst te veranderen gebruikend gegevens van rekening of persoonprofielen.

1. Gebruik de [&#x200B; knoop het stileren opties &#x200B;](./content-components.md#button) in het juiste paneel zoals nodig.

+++

+++ Containerelementen

1. Selecteer een containerelement op de pagina.

1. Gebruik de [&#x200B; container het stileren opties &#x200B;](./content-components.md#container) in het juiste paneel zoals nodig.

+++

### Nieuwe componenten invoegen

Wanneer u het pictogram **+** in de ontwerp linkernavigatie voor de visuele redacteur selecteert, kunt u de volgende componententypes aan de pagina als verandering van de Webervaring toevoegen:

* **[!UICONTROL Divider]** - Gebruik deze component om een scheidingslijn in te voegen om de lay-out en inhoud van uw e-mail te ordenen. U kunt opmaakkenmerken zoals de lijnkleur, stijl en hoogte aanpassen vanuit de eigenschappen in het rechterdeelvenster. Zie [&#x200B; Scheider &#x200B;](./content-components.md#divider) in _componenten van de Inhoud_ voor meer informatie.
* **[!UICONTROL HTML]** - Gebruik deze component om HTML-code in de bestaande structuur te kopiëren en te plakken. Zo kunt u gratis modulaire HTML-componenten maken om externe inhoud opnieuw te gebruiken. Zie [&#x200B; HTML &#x200B;](./content-components.md#html) in _componenten van de Inhoud_ voor meer informatie.
* **[!UICONTROL Image]** - Gebruik deze component om een afbeeldingsbestand in te voegen in de pagina. U kunt de opmaakkenmerken, zoals de breedte en hoogte, aanpassen aan de hand van de eigenschappen in het rechterdeelvenster. Zie [&#x200B; Beeld 0&rbrace; in &#x200B;](./content-components.md#image) componenten van de Inhoud _voor meer informatie._
* **[!UICONTROL Heading]** - Gebruik deze component om kopklassetekst in te voegen. U kunt de opmaakkenmerken, zoals de tekstkleur, stijl, lettertype en grootte, aanpassen met de eigenschappen in het rechterdeelvenster. Zie [&#x200B; Tekst van 0&rbrace; &lbrace;in &#x200B;](./content-components.md#text) componenten van de Inhoud _voor meer informatie._
* **[!UICONTROL Paragraph]** - Gebruik deze component om een standaardtekstelement in te voegen. U kunt de opmaakkenmerken, zoals de tekstkleur, stijl, lettertype en grootte, aanpassen met de eigenschappen in het rechterdeelvenster. Zie [&#x200B; Tekst van 0&rbrace; &lbrace;in &#x200B;](./content-components.md#text) componenten van de Inhoud _voor meer informatie._
* **[!UICONTROL Link]** - Gebruik deze component om een vrije tekstkoppeling in te voegen naar een opgegeven URL. U kunt opmaakkenmerken zoals de tekstkleur, stijl, uitlijning en grootte aanpassen aan de hand van de eigenschappen in het rechterdeelvenster.

Selecteer een componenttype aan de linkerkant en houd de muisaanwijzer boven een element dat grenst aan de plaats waar u het wilt toevoegen.

![&#x200B; Visuele redacteursinterface - nieuwe component &#x200B;](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

Klik op een van de weergegeven knoppen om de component te plaatsen:

* ***[!UICONTROL Insert before]** - neem de component vóór het geselecteerde element op.
* ***[!UICONTROL Insert after]** - neem de component na het geselecteerde element op.

Als u de selectie van een componenttype voor invoeging wilt opheffen, klikt u op **[!UICONTROL ESC]** in de contextafhankelijke blauwe banner die boven aan de pagina wordt weergegeven.

## Niet-visuele editor {#non-visual-editor}

Gebruik de niet-visuele redacteur wanneer u wijzigingen moet maken die niet gemakkelijk in de visuele redacteur kunnen worden verwezenlijkt. Deze op code-gebaseerde benadering geeft u nauwkeurige controle over element het richten en de wijziging. Voer de volgende stappen uit om de niet-visuele editor te gebruiken voor het ontwerpen van uw webervaring:

1. Klik op _[!UICONTROL Content]_&#x200B;in het rechterdeelvenster terwijl het tabblad **[!UICONTROL Add modification]**&#x200B;wordt weergegeven op de pagina met webervaringsdetails.

   De niet-visuele editor laadt een pagina op basis van de webkanaalconfiguratie.

   ![&#x200B; Niet-visuele editorinterface &#x200B;](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. Definieer de eerste wijziging die u wilt maken.

   In het linkerdeelvenster wordt een lijst met bestaande wijzigingen (indien van toepassing) weergegeven. Klik op **[!UICONTROL Add]** om een nieuwe wijziging te definiëren. Als er geen wijzigingen zijn gedefinieerd, worden in het deelvenster standaard de opties voor _[!UICONTROL Add Modification]_&#x200B;gebruikt.

   * Kies de **[!UICONTROL Modification type]** :

     | Type | Beschrijving |
     | ---- | ----------- |
     | [**[!UICONTROL CSS Selector]**](#css-selector-modifications) | Doelelementen met gebruik van een CSS-kiezerreeks. |
     | [**[!UICONTROL Page]**](#page-modifications) | Voeg aangepaste HTML, CSS of JavaScript toe aan elementen op paginaniveau, zoals `<head>` of `<body>` . |

   * Configureer de wijzigingsparameters op basis van het type:

      * **[!UICONTROL CSS Selector]** - Voer een geldige CSS-kiezer in om specifieke elementen als doel in te stellen.
      * **[!UICONTROL Action type]** - Kies de handeling die u wilt uitvoeren (bewerken, verbergen, verwijderen, invoegen, vervangen).
      * **[!UICONTROL Content]** - Geef de inhoud of opmaak op die u wilt toepassen.

1. Klik op **[!UICONTROL Save]** om de wijziging toe te passen.

### Wijzigingen in CSS-kiezer

Met CSS-selectorwijzigingen kunt u elementen nauwkeurig als doel instellen met de standaard CSS-selectorsyntaxis.

1. Kies **[!UICONTROL CSS Selector]** als wijzigingstype.

1. Voer de kiezer in het veld **[!UICONTROL CSS Element Selector]** in.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **Voorbeelden van kiezers:**
    
    | Kiezer | Doelen |
    | — | — |
    | `#hero-banner` | Element met ID &quot;hero-banner&quot; |
    | `.cta-button` | Alle elementen met de klasse &grave; cta-button&#39; |
    | &quot;header nav a&grave; | Koppelingen binnen de navigatie, binnen de koptekst |
    | `[data-offer=&quot;premium&quot;]` | Elementen met een specifiek gegevenskenmerk |

1. Kies een **[!UICONTROL Action Type]** en geef de vereiste informatie/inhoud op.

   * **[!UICONTROL Set Content]** - Voer de tekst in het **[!UICONTROL Content]** -veld in voor het element dat door de _[!UICONTROL CSS Element Selector]_-waarde wordt geïdentificeerd.

   * **[!UICONTROL Set Attribute]** - Geef een kenmerk op dat aan de huidige CSS-kiezer moet worden gekoppeld, zodat het element door dit kenmerk kan worden geïdentificeerd. Typ een naam in het veld **[!UICONTROL Attribute name]** en een waarde in het veld **[!UICONTROL Content]** . Als het kenmerk al bestaat, wordt de waarde bijgewerkt; anders wordt een nieuw kenmerk toegevoegd met de opgegeven naam en waarde.

   ![&#x200B; de niet-visuele redacteur css selecteerswijziging &#x200B;](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (Facultatief) klik **[!UICONTROL Add personalization]** en gebruik de [&#x200B; verpersoonlijkingsredacteur &#x200B;](./personalization.md#personalization-editor) om een aangepaste verpersoonlijking voor de inhoud tot stand te brengen.

### Paginawijzigingen

U kunt aangepaste code toevoegen met het wijzigingstype Pagina `<head>` . Het element `<head>` is een container voor metagegevens (gegevens over gegevens) en wordt tussen de tag `<html>` en de tag `<body>` geplaatst. In dit geval wacht de code niet op gebeurtenissen voor het laden van de hoofdtekst of de pagina. Deze wordt uitgevoerd aan het begin van het laden van de pagina.

Het element `<head>` wordt doorgaans gebruikt om JavaScript- of CSS-code boven aan de pagina toe te voegen. Kiezers voor volgende visuele handelingen zijn afhankelijk van de HTML-elementen die op dit tabblad zijn toegevoegd.

>[!NOTE]
>
>Aangepaste code wordt uitgevoerd in de browser van de bezoeker. Zorg ervoor dat uw code veilig is, getest is en geen negatieve invloed heeft op de paginaprestaties of gebruikerservaring.

1. Kies **[!UICONTROL Page `<head>`]** als wijzigingstype.

1. Voeg uw aangepaste code toe in het vak **[!UICONTROL Content]** .

   >[!CAUTION]
   >
   >U kunt alleen `<script>` - en `<style>` -elementen toevoegen aan de sectie `<head>` . Als u `<div>` -tags en andere elementen toevoegt, kunnen de resterende `<head>` -elementen binnen de `<body>` -tag worden gevuld.

   ![&#x200B; niet-visuele redacteur pagina-hoofd wijziging &#x200B;](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (Facultatief) klik **[!UICONTROL Add personalization]** en gebruik de [&#x200B; verpersoonlijkingsredacteur &#x200B;](./personalization.md#personalization-editor) om een aangepaste verpersoonlijking voor de inhoud tot stand te brengen.

## Wijzigingen beheren {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="Eenvoudig al uw wijzigingen beheren"
>abstract="In dit deelvenster kunt u door alle aanpassingen en toevoegingen navigeren die voor de webpagina zijn gedefinieerd en deze beheren."

Alle wijzigingen die u maakt, worden bijgehouden en kunnen worden beheerd vanuit het deelvenster **[!UICONTROL Modifications]** van zowel de visuele editor als de niet-visuele editor. Klik op het pictogram _[!UICONTROL Modifications]_<!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) --> op de linkerwerkbalk om alle wijzigingen weer te geven.

Elke wijzigingsrecord bevat:

* Het doelelement of -kiezer
* Het wijzigingstype (zoals bewerken, verbergen of invoegen)
* Een voorvertoning van de wijziging

![&#x200B; het paneel van Wijzigingen &#x200B;](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### Een wijziging bewerken

1. Zoek in de lijst _[!UICONTROL Modifications]_&#x200B;naar de wijziging die u wilt bewerken.

1. Klik het _Meer menu_ ( **..**) pictogram en kies **[!UICONTROL Edit]**.

1. Werk indien nodig de eigenschappen van de wijziging bij.

1. Klik op **[!UICONTROL Save]** om de wijzigingen op te slaan.

### Een wijziging verwijderen

1. Zoek in de lijst _[!UICONTROL Modifications]_&#x200B;naar de wijziging die u wilt verwijderen.

1. Klik het _Meer menu_ ( **..**) pictogram en kies **[!UICONTROL Delete modification]**.

1. Bevestig de verwijdering wanneer daarom wordt gevraagd.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## Voorbeeld van uw wijzigingen bekijken

Bekijk voordat u publiceert hoe uw wijzigingen er uitzien voor bezoekers.

Gebruik de voorvertoningsopties voor apparaten boven aan de visuele editor om de wijzigingen weer te geven op:

* Desktop
* Tablet
* Mobiel

![&#x200B; verander het apparaat het rangschikken voor de voorproef &#x200B;](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

De voorvertoning wordt bijgewerkt om te tonen hoe wijzigingen op elke apparaatgrootte worden gerenderd.

Gebruik de URL-balk om naar verschillende pagina&#39;s in uw webkanaalconfiguratie te navigeren. Controleer vervolgens of de wijzigingen correct worden toegepast op de doelpagina&#39;s op basis van de overeenkomende URL-regels.

## Klik op bijhouden voor webervaringen {#web-click-tracking}

Houd gebruikersinteractie met elementen bij om betrokkenheid te meten en inzichten te verzamelen. De gegevens voor het bijhouden van klikken zijn beschikbaar in uw betrokkenheidsrapporten en kunnen worden gebruikt om de effectiviteit van uw webervaringswijzigingen te meten.

Wanneer uw webervaring wordt geactiveerd (live), kunt u ook rapporten samenstellen met de Adobe Customer Journey Analytics (waarvoor een productabonnement is vereist). Om uw webervaringscontrole te verbeteren, kunt u ook de klikken op elk specifiek element van uw website bijhouden. Met Volgen kunt u het aantal klikken voor dat element weergeven in de webrapporten.

Voor meer informatie over Customer Journey Analytics en het bouwen van Webrapporten, zie de [&#x200B; documentatie van Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-landing).

1. Selecteer een element in de webervaringseditor, zoals een afbeelding of koppeling.

1. Klik op het pictogram _[!UICONTROL Click track element]_&#x200B;in de elementeigenschappen of de contextafhankelijke werkbalk.

   ![&#x200B; laat klik het volgen voor de elementen van de Webervaring toe &#x200B;](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. Open de lijst Track klikken in het linkerdeelvenster en wijzig de waarde **[!UICONTROL Tracked actions]** om deze interactie in uw rapporten te identificeren.

   ![&#x200B; plaats klik volgende identificatie voor Webervaring &#x200B;](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
