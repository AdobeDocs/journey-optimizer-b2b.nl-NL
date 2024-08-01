---
title: Accountsoorten
description: Leer meer over het publiek van uw account en hoe u op uw account gebaseerde reizen mogelijk maakt.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Accountpubliek

Een publiek is een groep personen die vergelijkbare gedragingen en/of kenmerken delen. Journey Optimizer B2B Edition gebruikt de functies voor de segmentatie van de account die in Adobe Real-time Customer Data Platform B2B- en B2P-edities zijn gevonden. Met accountsegmentatie kunnen gebruikers een publiek voor de account genereren door gegevens van een van de B2B-entiteiten in het systeem te gebruiken. Dit accountpubliek fungeert als input voor Journey Optimizer B2B Edition-accountreizen, waardoor u naadloze activering en personalisatie mogelijk maakt.

Leer meer over rekeningspubliek en hoe te om hen in de [ documentatie van de Dienst van de Segmentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences) te bepalen.

## Workflow voor accountpubliek

U kunt Journey Optimizer B2B Edition zien als een AEP-doel (Experience Platform) dat niet in de doelcatalogus wordt weergegeven. Activeer accountpubliek naar Journey Optimizer B2B Edition door de volgende stappen uit te voeren:

1. Maak schema&#39;s voor uw gegevens in AEP.
1. Vermeld uw gegevens in AEP.
1. Maak een accountsegment om uw gegevens te evalueren.
1. Activeer uw geëvalueerde gegevens naar Journey Optimizer B2B Edition.

In Journey Optimizer B2B Edition worden accountpubliek gebruikt als input voor op account gebaseerde reizen, zodat u zich kunt richten op de personen binnen die accounts. U kunt bijvoorbeeld accountpubliek gebruiken om gegevens op te halen van alle accounts die geen contactgegevens hebben voor personen met de titel Chief Operating Officer (COO) of Chief Marketing Officer (CMO).

Met Journey Optimizer B2B Edition kunt u het Adobe Experience Platform-accountpubliek (AEP) rechtstreeks vanaf de linkernavigatie maken en deze opnemen in uw accountreizen.

![ de rekeningspubliek van de Toegang ](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Een publiek voor een account maken

Definieer het accountpubliek door een accountsegmentatie te maken. U hebt de optie om de rekeningssegmentatie direct binnen de toepassing van de Uitgave van Journey Optimizer B2B tot stand te brengen, of u kunt de [ Bouwer UI van het Segment ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder) gebruiken. Hieronder vindt u de stappen waarmee u een accountsegmentatie kunt maken in Journey Optimizer B2B Edition.

1. Kies in de linkernavigatie **[!UICONTROL Accounts]** > **[!UICONTROL Audiences]** .

1. Klik op **[!UICONTROL Create audience]** rechtsboven.

1. Bouw de segmentdefinitie.

   De accountkenmerken en het publiek worden weergegeven op de linkernavigatiebalk. Onder het tabblad _[!UICONTROL Attributes]_kunt u zowel door het platform gemaakte als aangepaste kenmerken toevoegen. Sleep elk attribuut om de logica voor het segment te bouwen.

   >[!TIP]
   >
   >Houd er bij het maken van een accountpubliek rekening mee dat gebeurtenissen onder _[!UICONTROL People]_worden weergegeven, omdat deze kenmerken aan personen zijn gekoppeld.<br/>
   >
   >Onder het tabblad _[!UICONTROL Audiences]_kunt u eerder gemaakte, op personen gebaseerde soorten publiek toevoegen om van af te bouwen bij het maken van uw eigen accountpubliek.

   In het volgende voorbeeld wordt een publiek gedefinieerd dat is gemaakt met `Country Code` , `Revenue Amount` en `Market segment` . De vraag in het Engels zou zijn: &quot;Ik wil alle rekeningen in de V.S. die in het Segment van Financiën zijn waarvan opbrengst $1M overschrijdt.&quot;

   ![ de bouwervoorbeeld van de de segmentbouwer van het rekeningspubliek ](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save and Close]** rechtsboven.

Om uw rekeningspubliek voor de Uitgave van Journey Optimizer te activeren B2B, moet u het [ toevoegen aan een rekeningsreis ](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) en [ de reis ](../journeys/journey-overview.md) publiceren.
