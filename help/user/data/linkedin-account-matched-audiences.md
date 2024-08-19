---
title: LinkedIn-account met passend publiek
description: Leer hoe u verbinding maakt met een LinkedIn-account en een gegevensstroom activeert voor inkoopgroepen.
hidefromtoc: true
hide: true
source-git-commit: 63bf202e179895d72cd8b3f40e1bf5333bcd4c48
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%

---

# LinkedIn-account met passend publiek

Journey Optimizer B2B Edition biedt de mogelijkheid om LinkedIn Ad-publiek te genereren via een accountgericht publiek en is ontworpen om u te helpen lege rollen in uw inkoopgroepen te vullen. Als u een set koopgroepsfilters definieert, kunt u een met LinkedIn overeenstemmende doelgroep bijhouden voor de doelvooruitzichten die overeenkomen met de parameters van uw inkoopgroep. Deze functie gebruikt Experience Platform Doelen om sommige aspecten van de integratie te beheren. Er geldt een limiet van tien gegevensstromen.

Alvorens u een dataflow van de Uitgave van Journey Optimizer B2B in werking stelt, moet u minstens één geval van de [ (Bedrijven) LinkedIn Gelijke de bestemmingsschakelaar van de Publiek ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/social/linkedin#connect) met een rekening van de Manager van de Campagne van LinkedIn hebben die in uw Experience Platform toepassing wordt gevormd.

## Een nieuwe LinkedIn-accountverbinding configureren {#linkedin-destination-setup}

>[!CONTEXTUALHELP]
>id="ajo-b2b_linkedin_destination_setup"
>title="LinkedIn-doelinstelling is vereist"
>abstract="Verzend accounts die zijn gefilterd door groepen te kopen naar een LinkIn-bestemming om contact op te nemen met potentiële koopgroepsleden. U kunt maximaal 10 gegevensstromen voor 10 verschillende groepen gefilterde rekeningen tot stand brengen. Om met deze eigenschap te beginnen, voeg eerst een doel Linkedin toe."

1. Ga in het Experience Platform naar **[!UICONTROL Connections]** > **[!UICONTROL Destinations]** in de linkernavigatie en selecteer de tab **[!UICONTROL Catalog]** .

1. Zoek in de catalogus de **[!UICONTROL (Companies) LinkedIn Matched Audience]** -connector en klik op **[!UICONTROL Set Up]** .

   ![ heb toegang tot de (Bedrijven) LinkedIn Verwante schakelaar van het Publiek ](./assets/aep-destinations-catalog-linkedin.png){width="800" zoomable="yes"}

1. Selecteer **[!UICONTROL New Account]** > **[!UICONTROL Connect to LinkedIn]** .

1. Geef uw LinkedIn-gegevens op en meld u aan.

   De LinkedIn-account is verbonden als een doel.

## Accountgegevens bijwerken

De naam en beschrijving van de LinkedIn-account zijn zichtbaar voor inkoopgroepen in Journey Optimizer B2B Edition. Het is aan te raden deze gegevens bij te werken zodat ze gemakkelijk herkenbaar zijn voor kopers die met inkoopgroepen werken. U kunt de accountgegevens wijzigen in de gebruikersinterface van het Experience Platform of de Journey Optimizer B2B Edition.

1. Ga naar **[!UICONTROL Connections]** > **[!UICONTROL Destinations]** in de linkernavigatie en selecteer de tab **[!UICONTROL Accounts]** .

1. Voor de nieuwe rekening die u creeerde, klik _Meer_ (**..**) menu en kies **[!UICONTROL Edit details]**.

   ![ geef rekeningsdetails ](./assets/aep-destinations-accounts-edit-details.png){width="800" zoomable="yes"} uit

1. Werk de naam en beschrijving bij in het dialoogvenster.

   ![ geef de naam en de beschrijving ](./assets/destinations-linkedin-account-edit-details-dialog.png){width="500"} uit

1. Klik op **[!UICONTROL Save]**.

## Account activeren voor kopersgroepen

>[!NOTE]
>
>Als u al tien gegevensstromen hebt, kunt u geen andere creëren. Als het maximale aantal Experience Platforms is bereikt, verwijdert u er een voordat u een nieuwe maakt in Journey Optimizer B2B Edition.

1. Ga in Journey Optimizer B2B Edition naar **[!UICONTROL Accounts]** > **[!UICONTROL Buying groups]** in de linkernavigatie.

1. Selecteer de tab **[!UICONTROL Browse]** .

1. Klik op **[!UICONTROL Activate to LinkedIn Destination]** rechtsboven.

   ![ geef rekeningsdetails ](./assets/activate-linkedin-destination.png){width="800" zoomable="yes"} uit

1. Geef de gegevensstroom een beschrijvende naam en beschrijving (optioneel).

   Nadat u het bewaart, wordt de naam die u voor dataflow specificeert prepended met _AJOB2B_ aan hulp in het identificeren van dataflow in Experience Platform.

1. Ga [ identiteitskaart van de Rekening van uw Rekening van de Manager van de Campagne van LinkedIn ](https://www.linkedin.com/help/lms/answer/a424270) in.

   U kunt uw account-id vinden op basis van uw accountnaam in de gebruikersinterface van Campagnebeheer.

   ![ voeg de gegevens dataflow ](./assets/destinations-linkedin-activate-details.png){width="700" zoomable="yes"} toe

1. Klik op **[!UICONTROL Select buying group filters]** en definieer de parameters van het publiek van uw account.

   >[!IMPORTANT]
   >
   >Op dit moment kunnen filters niet worden bewerkt nadat de gegevensstroom is geactiveerd. Controleer uw werk voordat u de gegevensstroom activeert.

   ![ specificeer het rekeningspubliek die volgens het kopen groepen filtreren ](./assets/destinations-linkedin-activate-buying-group-filters.png){width="400"}

   Voor **[!UICONTROL Engagement score]** is de operator `Between` inclusief, evenals percentagebereiken. Bijvoorbeeld, zijn 5.1 en 5 zowel _tussen_ 5 en 6.

   Lege voorwaarden worden behandeld als `Is Any` .

   Klik op **[!UICONTROL Save]** om de opgegeven filters toe te voegen.

1. Klik **[!UICONTROL Select LinkedIn destination]** en kies de gevormde bestemming van LinkedIn die u wilt gebruiken.

   Op activering, leidt dit het plaatsen tot dataflow gebruikend de bestemmingsconfiguratie en een overeenkomstig virtueel segment.

1. Controleer de instellingen en klik op **[!UICONTROL Activate]** rechtsboven.

   Klik nogmaals op **[!UICONTROL Activate]** in het bevestigingsdialoogvenster.

   Een banner wordt weergegeven met een koppeling naar het menu met gegevensstromen in het Experience Platform, zodat u de gegevensstroomrecord kunt controleren.
