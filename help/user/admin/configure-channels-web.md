---
title: Webkanaalconfiguraties
description: Leer hoe u webkanaalinstellingen configureert om wegeigenschappen en pagina-overeenkomsten voor de levering van inhoud in Journey Optimizer B2B edition te definiëren.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 0%

---

# Webkanaalconfiguraties

Een webconfiguratie is een webeigenschap die wordt geïdentificeerd door een URL waar de inhoud wordt geleverd. Deze kan overeenkomen met een URL of meerdere pagina&#39;s van één pagina, zodat webervaringen wijzigingen kunnen aanbrengen op een of meerdere webpagina&#39;s. Deze configuraties worden vereist voor marketers om [&#x200B; de knopen van de de actiegeleiding van het Web in reizen &#x200B;](../content/web-experiences.md#create-a-web-experience) toe te voegen en [&#x200B; de ervaringsaanpassingen &#x200B;](../content/web-experience-design.md) voor een campagne te ontwerpen.

>[!BEGINSHADEBOX]

**Eerste vereisten**

Om Webkanalen te gebruiken, moet uw website [&#x200B; Adobe Experience Platform Web SDK &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/collection/js/js-overview) (`alloy.js`) hebben die voor bezoekersidentificatie en inhoudslevering wordt uitgevoerd. Zorg ervoor dat de Adobe Experience Platform Web SDK versie 2.16 of hoger is.

De kanaalconfiguratie van het Web in Journey Optimizer B2B edition vereist de volgende [&#x200B; toestemmingen &#x200B;](../admin/user-management.md#b2b-product-permissions):

* _[!UICONTROL Channel Configurations]_>_[!UICONTROL Manage Messages Presets]_ - Vereist voor het maken, bijwerken en verwijderen van webkanaalconfiguraties.
* _[!UICONTROL Channel Configurations]_>_[!UICONTROL View Messages Presets]_ - Vereist om webkanaalconfiguraties weer te geven.

>[!ENDSHADEBOX]

## Webkanaalconfiguratie maken

1. Ga in de linkernavigatie naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** .

1. Selecteer onder _[!UICONTROL Web]_&#x200B;in het navigatievenster de optie **[!UICONTROL Channel configurations]**.

   ![&#x200B; heb toegang tot de configuraties van het Webkanaal &#x200B;](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. Klik op **[!UICONTROL Create channel configuration]** rechtsboven.

1. Voer een **[!UICONTROL Name]** (vereist) en een **[!UICONTROL Description]** (optioneel) voor de configuratie in.

   >[!NOTE]
   >
   >Namen moeten beginnen met een letter (A-Z) en mogen alleen alfanumerieke tekens bevatten. U kunt ook onderstrepingsteken `_` -, stip `.` - en afbreekstreepjes `-` gebruiken.

1. Selecteer in de sectie **[!UICONTROL Web settings]** een van de volgende opties:

   * **[!UICONTROL Single page]** - Als u de wijzigingen alleen op één pagina wilt toepassen, voert u een **[!UICONTROL Page URL]** in of selecteert u deze.

     ![&#x200B; Selecterend een pagina URL voor een enig-pagina configuratie van het Webkanaal &#x200B;](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL Pages matching rule]** - om veelvoudige URLs te richten die de zelfde regel aanpassen, a [&#x200B; pagina&#39;s die regel &#x200B;](#build-a-pages-matching-rule) aanpassen en a **[!UICONTROL Default authoring and preview URL]** ingaan.

1. Klik op **[!UICONTROL Submit]** om de wijzigingen op te slaan.

Nadat u de configuratie opslaat, is het in de status van het a _Ontwerp_ en is beschikbaar aan marketers wanneer zij een Webkanaal in hun reizen gebruiken. U kunt de configuratie blijven bewerken zolang deze in de conceptstatus blijft. U kunt een configuratie van het ontwerpWebkanaal ook schrappen door het _Meer_ pictogram (**te klikken...**) naast de naam en het kiezen **[!UICONTROL Delete]**.

Zodra het Webkanaal in een reis wordt gebruikt, beweegt het zich aan een _Actieve_ status. In deze status kunt u de naam en beschrijving van de configuratie bewerken. U kunt de webinstellingen niet wijzigen of de configuratie verwijderen.

## Regels voor overeenkomsten met pagina&#39;s {#pages-matching-rule}

Wanneer u een webconfiguratie maakt, kunt u een _[!UICONTROL Pages matching rule]_&#x200B;maken om meerdere URL&#39;s met dezelfde regel als doel in te stellen. Met deze regels kunt u dezelfde inhoudswijzigingen op meerdere pagina&#39;s toepassen.

U kunt bijvoorbeeld wijzigingen aanbrengen in een hoofdbanner op een hele website of een bovenste afbeelding toevoegen die op alle productpagina&#39;s wordt weergegeven.

### Een regel maken

1. Wanneer u [&#x200B; creeert een configuratie van het Webkanaal &#x200B;](#create-a-web-channel-configuration), kies **[!UICONTROL Page matching rule]**.

1. Definieer de criteria voor de velden **[!UICONTROL Domain]** en **[!UICONTROL Page]** met de verschillende operatoren in elke sectie om de regel samen te stellen.

   +++Domeinoperatoren

   Gebruik de volgende operatoren voor overeenkomende domeinen volgens de tekenreekswaarde die u invoert:

   | Operator | Beschrijving | Voorbeelden |
   | --- | --- | --- |
   | [!UICONTROL Equals] | Exacte overeenkomst van het domein. | |
   | [!UICONTROL Starts with] | Komt overeen met alle domeinen (inclusief subdomeinen) die beginnen met de ingevoerde tekenreeks. | `Starts with: dev` komt overeen met alle domeinen en subdomeinen die beginnen met `dev` , zoals `dev.example.com` , `dev.products.example.com` en `developer.example.com` |
   | [!UICONTROL Ends with] | Komt overeen met alle domeinen (inclusief subdomeinen) die eindigen met de ingevoerde tekenreeks. | `Ends with: example.com` komt overeen met alle domeinen en subdomeinen die eindigen met `example.com` , zoals `stage.example.com` , `prod.example.com` en `myexample.com` |
   | [!UICONTROL Wildcard matching] | Hiermee kunt u een jokertekenovereenkomst definiëren in het midden van de tekenreeks, zoals `dev.*.example.com` . De bevestigingsregels vereisen dat de waarde één en slechts één vervanging (asterisk) bevat wanneer de exploitant _vervangingsaanpassing_ is. | `Wildcard matching: dev.*.example.com` komt overeen met domeinen zoals `dev.products.example.com` , `dev.mytest.products.example.com` en `dev.blog.example.com` |
   | [!UICONTROL Any] | Komt overeen met alle domeinen. Dit is handig wanneer u een bepaald pad over domeinen test. | |

   +++

   +++Padoperatoren

   Gebruik de volgende operatoren voor overeenkomende paden op basis van de tekenreekswaarde die u invoert:

   | Operator | Beschrijving | Voorbeelden |
   | --- | --- | --- |
   | [!UICONTROL Equals] | Exacte overeenkomst van het pad. | |
   | [!UICONTROL Starts with] | Komt overeen met alle paden (inclusief subpaden) die met de tekenreeks beginnen. | |
   | [!UICONTROL Ends with] | Komt overeen met alle paden (inclusief subpaden) die eindigen met de tekenreeks. | |
   | [!UICONTROL Any] | Komt overeen met alle paden. Dit is handig wanneer u alle paden aanwijst in een of meerdere domeinen. | |
   | [!UICONTROL Wildcard matching] | Hiermee kunt u een intern jokerteken in het pad definiëren, zoals `/products/*/detail` . Het jokerteken `*` in de padcomponent komt overeen met een willekeurige reeks tekens tot het eerste `/` -teken.  En `/*/` komt overeen met een willekeurige reeks tekens (inclusief subpaden). | `Wildcard matching: /products/*/detail` komt overeen met paden zoals `example.com/products/yoga/detail` , `example.com/products/surf/detail` , `example.com/products/tennis/detail` en `example.com/products/yoga/pants/detail` |
   | [!UICONTROL Contains] | De waarde wordt omgezet in een jokerteken, zoals `*mystring*` , en komt overeen met alle paden die de reeks tekens bevatten. | `Contains: product` komt overeen met alle paden die de tekenreeks `product` bevatten, zoals `example.com/products` , `example.com/yoga/perfproduct` , `example.com/surf/productdescription` en `example.com/home/product/page` |

   +++

   Bijvoorbeeld, om inhoudsveranderingen op alle _LumaSecure_ oplossingspagina&#39;s van uw _Bodea_ website te steunen, selecteer **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `bodea` en **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `lumasecure`.

   ![&#x200B; het bepalen van een pagina passende regel voor een configuratie van het Webkanaal &#x200B;](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. Als voor uw gebruik meerdere regels nodig zijn, klikt u op **[!UICONTROL Add another page rule]** en herhaalt u de vorige stap.

   * U kunt maximaal 10 regels definiëren.

   * Gebruik de operatoren **[!UICONTROL Or]** of **[!UICONTROL Exclude]** tussen de verschillende regels.

     _[!UICONTROL Or]_&#x200B;is de standaardoperator voor het definiëren van meerdere regels en is handig voor het toevoegen van meerdere criteria aan definities die kunnen worden aangepast.

     _[!UICONTROL Exclude]_&#x200B;is nuttig wanneer een van de pagina&#39;s die aan de gedefinieerde regel voldoen, niet als doelpagina mag worden gebruikt. U kunt bijvoorbeeld alle `bodea.com` -pagina&#39;s aanwijzen die `lumasecure` bevatten, maar geen blogpagina&#39;s (zoals `bodea.com/blogs/lumasecure/latest-release` ).

   ![&#x200B; Pagina&#39;s die regels met uitsluiting aanpassen &#x200B;](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. Voer de **[!UICONTROL Default authoring and preview URL]** in.

   Met deze stap zorgt u ervoor dat de pagina&#39;s die door de regel worden gegenereerd of waaraan de regel is gekoppeld, een specifieke URL hebben voor het ontwerpen van inhoud en voorvertoningen van webervaringen.

## Een webkanaal dupliceren

U kunt een bestaande webkanaalconfiguratie dupliceren en deze wijzigen om een nieuw webkanaal te maken op basis van een bestaande configuratie. Een actieve webkanaalconfiguratie die is opgeslagen in de bibliotheek kan niet worden gewijzigd.

1. Klik het _Meer menu_ pictogram (**...**) voor de variant en kies **[!UICONTROL Duplicate]**.

   ![&#x200B; klik het meer nenupictogram om een bestaande configuratie van het Webkanaal te dupliceren &#x200B;](./assets/config-web-channels-more-menu.png){width="450"}

   Met deze actie maakt u een gedupliceerd webkanaal waaraan `_Copy_nnn` is toegevoegd.

1. Klik op de naam van het gedupliceerde webkanaal om de parameters te bewerken.

   * Wijzig de naam en beschrijving zodat deze overeenkomen met het doel of de items in de regel.
   * Wijzig zo nodig de URL van één pagina.
   * Wijzig zo nodig de overeenkomende regel voor pagina&#39;s.

1. Klik op **[!UICONTROL Submit]** wanneer de configuratie is voltooid.
