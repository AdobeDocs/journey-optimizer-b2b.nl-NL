---
title: Marketo Engage activeren om reisacties te ondersteunen
description: Activeer Marketo Engage-verbindingen om reisacties te ondersteunen, zodat marketers campagnes tussen Marketo Engage en Journey Optimizer B2B edition kunnen coördineren.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---


# Marketo Engage-instanties activeren om acties te ondersteunen

De acties van Marketo Engage zijn _op mensen-gebaseerde_ acties die u toestaan om uw _op rekening-gebaseerde_ marketing organisatie tussen Journey Optimizer B2B edition en uw _op lood-gebaseerde_ marketing inspanningen in Marketo Engage te coördineren. Gebruik deze acties om het lidmaatschap van een statische lijst te ordenen en om mensen in campagnes te plaatsen.

Om de reisacties van Marketo Engage te gebruiken, creeert een beheerder eerst de douanedienst van de a [&#x200B; &#x200B;](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} in Marketo Engage, die de geloofsbrieven nodig voor authentificatie verstrekt. Vervolgens gebruikt een productbeheerder voor Journey Optimizer B2B edition de referenties om een verbinding met Marketo Engage te maken. De gebruikers van Journey Optimizer B2B edition kunnen dan de verbinding van verwijzingen voorzien om de acties van Marketo Engage in <!-- person and --> rekeningsreizen te vormen, zoals het toevoegen van of het verwijderen van mensen uit Marketo Engage lijsten of het toevoegen van hen aan verzoekcampagnes.

## Een Marketo Engage-verbinding configureren {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Externe Marketo Engage-verbindingen"
>abstract="Productbeheerders kunnen verbindingen met externe Marketo Engage-instanties configureren, zodat deze beschikbaar zijn voor reishandelingen."

Voer de volgende taken uit om een externe Marketo Engage-instantie te configureren voor gebruik met reishandelingen.

### De aangepaste Marketo Engage-service maken

1. Login aan Marketo Engage als beheerder en [&#x200B; creeer een douanedienst &#x200B;](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Kopieer de volgende waarden voor de Journey Optimizer B2B edition-verbinding:

   * Munchkin-id
   * Client-id
   * Clientgeheim

De werkruimtezicht van Marketo Engage voor activa, zoals lijsten en campagnes, wordt geregeerd door de [&#x200B; roltoestemmingen die in de douanedienst &#x200B;](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"} worden toegewezen. De verkopers kunnen de zelfde verbinding veelvoudige tijden binnen een reis gebruiken, en verschillende verbindingen van Marketo Engage binnen de zelfde reis gebruiken.

### Integratie toevoegen

![&#x200B; voeg integratiedetails &#x200B;](assets/integration-connection-details.png){width="800" zoomable="yes"} toe

1. Navigeer in Journey Optimizer B2B edition naar **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** .
1. Selecteer deze optie op de tab **[!UICONTROL Integrations]** .
1. Klik op **[!UICONTROL Create a connection]**.
1. Voer een **[!UICONTROL Name]** (vereist) en **[!UICONTROL Description]** (optioneel) in.
1. Selecteer het updatebeleid dat wordt gebruikt voor het toepassen van een handeling op een overeenkomende persoonrecord.

   Wanneer een actie voor de verbonden instantie van Marketo Engage loopt, bepaalt het geselecteerde _updatebeleid_ de persoonverslagen in Marketo Engage om te selecteren als de veelvoudige herkenningstekens in het verenigde persoonsprofiel bestaan.

   * **[!UICONTROL Update all matching records]**
   * **[!UICONTROL Update only the oldest matching record]**
   * **[!UICONTROL Update only the newest matching record]**

   >[!NOTE]
   >
   >Mensen gaan de reis door ongeacht een overeenkomst, behalve wanneer een fout optreedt.

1. Voer de Munchkin-id, de client-id en het clientgeheim in voor de service die in de externe Marketo Engage-instantie is gemaakt.
1. Klik op **[!UICONTROL Connect to Marketo]**.
1. Klik op **[!UICONTROL Create]**.

## De verbinding gebruiken in een reishandeling

Wanneer een markeerteken een Marketo Engage-handeling tijdens een rit gebruikt, kunnen ze het knooppunt configureren met de naam van de verbinding.

Met de voltooide integratie, zijn de acties van Marketo Engage beschikbaar van **Acties op:** in de knoopeigenschappen.

![&#x200B; de actielijst van Marketo &#x200B;](assets/marketo-actions-list.png){width="800" zoomable="yes"}