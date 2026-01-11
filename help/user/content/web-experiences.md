---
title: Webervaringen
description: Maak, ontwerp en publiceer gepersonaliseerde webervaringen voor accountreizen - breng gerichte inhoudwijzigingen aan websitebezoekers in Journey Optimizer B2B edition aan.
feature: Content, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie"
source-git-commit: 30bb44f9c308cd144a53a60b4f420380df5528e4
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Webervaringen

Met het webkanaal in Adobe Journey Optimizer B2B edition kunt u persoonlijke ervaringen rechtstreeks op uw website maken, zodat u op een zinvolle manier verbinding kunt maken met klanten. Deze functie biedt een flexibele toolkit die u kunt gebruiken om de betrokkenheid met op maat gemaakte inhoud te verbeteren en deze naadloos te integreren met andere kanalen, zoals e-mail en SMS.

Dankzij webervaringen kunt u:

* Aangepaste inhoudwijzigingen aan beoogde websitebezoekers leveren
* Website-elementen zoals banners, tekst, afbeeldingen en knoppen aanpassen op basis van accountkenmerken
* Specifieke pagina&#39;s activeren of wijzigingen toepassen op meerdere pagina&#39;s met URL-overeenkomende regels
* Houd betrokkenheid bij en controleer de impact van uw webpersonalisatie-inspanningen

>[!BEGINSHADEBOX]

## Vereisten

Voordat u webervaringen kunt maken, moet u controleren of aan de volgende vereisten is voldaan:

* Een productbeheerder heeft een of meer webkanalen geconfigureerd om de URL&#39;s (pagina&#39;s) te definiëren die moeten worden opgenomen voor een webervaring. Voor meer informatie, zie [&#x200B; het kanaalconfiguraties van het Web &#x200B;](../admin/configure-channels-web.md).

* Uw website heeft [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) die voor bezoekersidentificatie en inhoudslevering wordt uitgevoerd. Zorg ervoor dat de Adobe Experience Platform Web SDK versie 2.16 of hoger is.

* U hebt de noodzakelijke [&#x200B; toestemmingen &#x200B;](../admin/user-management.md#b2b-product-permissions) om Webervaringen in een reis tot stand te brengen en te beheren:
   * _[!UICONTROL Campaigns]_>_[!UICONTROL Manage Campaigns]_ - Vereist om een actieknooppunt voor webpersonalisatie toe te voegen of bij te werken.
   * _[!UICONTROL Campaigns]_>_[!UICONTROL View Campaigns]_ - Vereist om details voor de actieknooppunten van een webpersonalisatie weer te geven.
   * _[!UICONTROL Campaigns]_>_[!UICONTROL Approve and Publish Campaigns]_ - Vereist om een reis te publiceren die één of meerdere knopen van de de verpersoonlijkingsactie van het Web heeft.

* U hebt Adobe Experience Cloud [&#x200B; Visuele die Helper browser uitbreiding van de Uitgevende van de Helper &#x200B;](#install-the-visual-editing-helper-extension) voor uw Webbrowser wordt geïnstalleerd. U hebt deze extensie nodig als u uw webpagina&#39;s betrouwbaar wilt openen, ontwerpen en voorvertonen in de ontwerpruimte voor Journey Optimizer B2B edition-inhoud.

  >[!NOTE]
  >
  >Google Chrome en Microsoft Edge zijn momenteel de enige browsers die ontwerpwebpagina&#39;s in Journey Optimizer B2B edition ondersteunen.

>[!ENDSHADEBOX]

## De extensie Visuele bewerkingshulp installeren

1. Open een nieuw tabblad in uw browser ([!DNL Google Chrome] of [!DNL Microsoft Edge] ).

1. Ga naar de [&#x200B; Opslag van het Web van Google Chrome &#x200B;](https://chromewebstore.google.com/category/extensions).

   Als u [!DNL Microsoft Edge] gebruikt, _uitgezochte uitbreidingen_ van andere opslag op de hoogste banner toestaat. Als u deze optie inschakelt, kunt u extensies toevoegen van de extensies [!DNL Chrome Web Store] t/m [!DNL Microsoft Edge] .

1. Zoek en navigeer naar de browserextensie van _[!DNL Adobe Experience Cloud Visual Editing Helper]_.

   ![&#x200B; Adobe Experience Cloud Visuele het Uitgeven de uitbreiding van de Helper voor Google Chrome &#x200B;](./assets/web-experience-google-chrome-adobe-visual-editing-extension.png){width="800" zoomable="yes"}

1. Klik op **[!UICONTROL Add to Chrome]** en vervolgens op **[!UICONTROL Add Extension]** in het bevestigingsdialoogvenster.

   Als u [!DNL Microsoft Edge] gebruikt, voegt deze handeling de extensie toe aan [!DNL Edge] .

1. Controleer of de browserextensie van [!DNL Visual Editing Helper] correct is ingeschakeld op de werkbalk van de browser.

   ![&#x200B; Adobe Experience Cloud het Visuele Uitgeven de uitbreidingspictogram van de Helper in de toolbar van Chrome van Google &#x200B;](./assets/web-experience-google-chrome-adobe-visual-editing-extension-icon.png){width="450"}

[!DNL Adobe Experience Cloud Visual Editing Helper] wordt nu automatisch ingeschakeld wanneer een website wordt geopend in de visuele editor van Journey Optimizer B2B edition voor webervaringen. De extensie heeft geen voorwaardelijke instellingen en verwerkt alle instellingen automatisch, inclusief de instellingen voor Cookies van SameSite.

>[!NOTE]
>
>Sommige websites kunnen om een van de volgende redenen niet betrouwbaar worden geopend in de Journey Optimizer B2B edition-webeditor:
>
>* De website heeft een strikt beveiligingsbeleid.
>* De website bevindt zich in een iframe.
>* De klant-kwaliteitscontrole of de werkgebiedsite is niet extern beschikbaar (de site is intern).

## Een webervaring maken

U kunt opstellingsWeb ervaringen in een reis wanneer u [&#x200B; a _[!UICONTROL Take an action]_&#x200B;knoop &#x200B;](../journeys/action-nodes.md) toevoegt en het volgende doet:

1. Kies _[!UICONTROL Action on]_&#x200B;voor het doel **[!UICONTROL People]**.

1. Kies _[!UICONTROL Action on people]_&#x200B;bij **[!UICONTROL Personalize web experience]**.

![&#x200B; neem een actie - personaliseer Webervaring &#x200B;](./assets/web-experience-add-journey-node.png){width="500"}

1. Klik op **[!UICONTROL Create web experience]**.

1. Voer in het dialoogvenster _[!UICONTROL Create web experience]_&#x200B;een handige **[!UICONTROL Name]**&#x200B;en **[!UICONTROL Description]**(optioneel) in.

   * Naam - maximaal 100 tekens, moet uniek en hoofdlettergevoelig zijn

   * Beschrijving - Maximaal 300 tekens

   >[!NOTE]
   >
   >Naam- en beschrijvingsvelden ondersteunen alfakanalen, numerieke en speciale tekens. Gereserveerde karakters (`\ / : * ? " < > |`) worden **_niet toegestaan_**.

   ![&#x200B; creeer de dialoog van de Webervaring &#x200B;](./assets/web-experience-create-dialog.png){width="400"}

<!-- What is this for? 1. Properties? -->

1. Voer op het tabblad **[!UICONTROL Properties]** de beschrijving voor de webervaring in.

1. Klik op het tabblad **[!UICONTROL Actions]** en selecteer de **[!UICONTROL Web channel]** die u voor een webervaring wilt gebruiken.

   De configuratie van het Webkanaal bepaalt waar de inhoudwijzigingen worden toegepast gebaseerd op de gevormde pagina passende regels. Zie [&#x200B; de kanaalconfiguraties van het Web &#x200B;](../admin/configure-channels-web.md) voor meer informatie.

   ![&#x200B; Geselecteerde configuratie van het Webkanaal &#x200B;](./assets/web-experience-journey-node-actions-tab.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Edit content]** om de webwijzigingen te definiëren.

   De editor wordt geopend op het tabblad _[!UICONTROL Content]_, waar u de wijzigingen voor uw webervaring kunt definiëren. Zie [&#x200B; de ervaringsontwerp van het Web &#x200B;](./web-experience-design.md) voor gedetailleerde informatie over het gebruiken van de ontwerphulpmiddelen om de veranderingen van de Web ervaringsinhoud toe te voegen.

1. Stel in het rechterdeelvenster de eigenschappen voor de webervaring in op basis van de manier waarop u deze wilt definiëren en beheren.

   * **[!UICONTROL Visual editor]** - knevel tussen de [&#x200B; visuele en niet-visuele redacteur &#x200B;](./web-experience-design.md#web-design-tools) voor het ontwerp van de Webervaringswijziging.
   * **[!UICONTROL Visitor redirection]** - laat deze optie toe [&#x200B; bezoekers aan een andere bestaande URL &#x200B;](#redirect-to-url) eerder dan het ontwerpen van een nieuwe variatie in de inhoudstafel om te leiden.

   ![&#x200B; knevel eigenschappen voor de visuele redacteur en richt URL &#x200B;](./assets/web-experience-journey-node-content-properties.png){width="700" zoomable="yes"} om

1. Klik **[!UICONTROL Edit web page]** aan [&#x200B; ontwerp uw Webwijzigingen &#x200B;](./web-experience-design.md).

1. Wanneer de wijzigingen zijn voltooid, klikt u op de pijl naar links boven de editor om terug te keren naar het tabblad Inhoud en naar de eigenschappen van de knooppunt voor gepersonaliseerde webervaring.

   U kunt op de pijl naar links helemaal boven klikken om terug te keren naar het canvas.

## Een webervaring bewerken

1. Open de rit en selecteer het actieknooppunt **[!UICONTROL Personalize web experience]** .

1. Klik op **[!UICONTROL Edit web experience]** als u wijzigingen wilt aanbrengen in de webkanaalconfiguratie of -inhoud.

1. Selecteer het tabblad **[!UICONTROL Actions]** en wijzig zo nodig de webconfiguratie.

1. Selecteer het tabblad **[!UICONTROL Content]** en gebruik de gereedschappen voor visueel ontwerp naar wens.

   * _Visuele redacteur_ - klik **[!UICONTROL Edit Content]**.
   * _niet-visuele redacteur_ - klik **[!UICONTROL Add a modification]**.

   Zie [&#x200B; de ervaringsontwerp van het Web &#x200B;](./web-experience-design.md) voor gedetailleerde informatie.

1. Wanneer de wijzigingsdefinities zijn voltooid, klikt u op de pijl naar links boven de editor om terug te keren naar het tabblad Inhoud en de eigenschappen voor webbeleving.

   U kunt op de pijl naar links helemaal boven klikken om terug te keren naar het canvas.

## Omleiden naar URL

Wanneer u een webervaring maakt, kunt u bezoekers omleiden naar een andere bestaande URL in plaats van een nieuwe variatie in de inhoudeditor te ontwerpen. Deze optie is handig wanneer u een inhoudexperiment wilt uitvoeren waarbij twee verschillende ervaringen worden vergeleken in plaats van slechts enkele elementen binnen een pagina te wijzigen.

Maak bijvoorbeeld een webcampagne met twee behandelingen:

In Behandeling A ontwerpt u een webervaring met de inhoudeditor voor de helft van de doelpopulatie.

Selecteer in Behandeling B de optie _[!UICONTROL Redirect to URL]_&#x200B;voor de andere helft van de doelpopulatie. Voer de URL in van een pagina met een ander ontwerp dat u buiten Journey Optimizer B2B edition hebt gemaakt.

![&#x200B; plaats de bezoekersomleiding om bezoekers aan specifieke URL &#x200B;](./assets/web-experience-journey-node-content-visitor-redirection.png){width="500" zoomable="yes"} om te leiden

>[!NOTE]
>
>Als deze optie is geselecteerd, wordt de voorvertoning van de website niet weergegeven en wordt de schakeloptie _[!UICONTROL Visual editor]_&#x200B;uitgeschakeld.

Wanneer uw webcampagne live is, kunt u bijhouden hoe de webervaring die u in Journey Optimizer B2B edition hebt gedefinieerd, functioneert op basis van webervaringen die een omleiding naar de alternatieve pagina hebben gebruikt.

## De webervaring testen

Nadat het inhoudsontwerp volledig voor de Webervaring is, kunt u _gebruiken de inhoud_ simuleren eigenschap om uw Webpagina wijzigingen voor te vertonen. Als u persoonlijke inhoud hebt ingevoegd, kunt u de gegevens van het testprofiel gebruiken om te controleren hoe de inhoud wordt gerenderd. De simulatiegereedschappen zijn beschikbaar op het tabblad _[!UICONTROL Content]_&#x200B;voor webervaring of in de visuele ontwerpeditor voor inhoud.

1. Klik op **[!UICONTROL Simulate content]** rechtsboven.

1. Selecteer een testprofiel.

1. Voeg een testprofiel toe om uw webpagina te controleren aan de hand van de gegevens van het testprofiel.

<!-- This works differently than emails (rely on Marketo data), currently. Will expand when we figure it out -->

## Uw webervaring activeren

Uw Webervaring wordt geactiveerd en zichtbaar gemaakt aan het publiek wanneer u [&#x200B; de reis &#x200B;](../journeys/create-publish-journey.md#publish-an-account-journey) publiceert. Overweeg het volgende voordat u een webervaring activeert tijdens een rit:

* Als u een reis met een Webervaring publiceert die de zelfde pagina&#39;s zoals een andere reis beïnvloedt die reeds levend is, worden alle veranderingen toegepast op de Web-pagina&#39;s.

* Als meerdere reizen dezelfde elementen van uw website bijwerken, heeft de laatst toegepaste wijziging voorrang.

### Leveringsvereisten

Voor het uitvoeren van een webbeleving moeten de volgende instellingen worden gedefinieerd:

* Controleer in de Adobe Experience Platform-gegevensverzameling of u een gegevensstroom hebt gedefinieerd waarbij de Adobe Journey Optimizer B2B edition-optie is ingeschakeld onder de Adobe Experience Platform-service.

  Deze configuratie zorgt ervoor dat de Adobe Experience Platform Edge de binnenkomende gebeurtenissen correct kan verwerken. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)

* Controleer in Adobe Experience Platform of u één samenvoegbeleid hebt met de optie _[!UICONTROL Active-On-Edge Merge Policy]_&#x200B;ingeschakeld.

  Selecteer een beleid in het menu Klant > Profielen > Beleid voor samenvoegen in Experience Platform. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide#configure)

  Dit samenvoegbeleid wordt door de binnenkomende kanalen van Journey Optimizer B2B edition gebruikt om binnenkomende Webervaringen op de rand correct te activeren en te publiceren. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide)

### Problemen oplossen

U kunt de Edge Delivery-weergave in Adobe Experience Platform Assurance gebruiken om problemen op te lossen met de levering van Journey Optimizer B2B edition Web-ervaringen. Met deze insteekmodule kunt u aanvraagaanroepen in detail controleren, de verwachte randaanroepen controleren en profielgegevens controleren. Deze profielgegevens omvatten identiteitskaarten, segmentlidmaatschap, en toestemmingsmontages. U kunt ook de gekwalificeerde en ongekwalificeerde activiteiten voor het verzoek controleren.

Voor meer informatie over de mening van Edge Delivery in Assurance, zie de [&#x200B; documentatie van Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery).
