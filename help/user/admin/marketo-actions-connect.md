---
title: Marketo Engage activeren om reisacties te ondersteunen
description: Activeer Marketo Engage-verbindingen om reisacties te ondersteunen, zodat marketers campagnes tussen Marketo Engage en Journey Optimizer B2B edition kunnen coördineren.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---


# Marketo Engage-instanties activeren om acties te ondersteunen

De acties van Marketo Engage zijn _op mensen-gebaseerde_ acties die u toestaan om uw _op rekening-gebaseerde_ marketing organisatie tussen Journey Optimizer B2B edition en uw _op lood-gebaseerde_ marketing inspanningen in Marketo Engage te coördineren. Gebruik deze acties om het lidmaatschap van een statische lijst te ordenen en om mensen in campagnes te plaatsen.

Om de acties van Marketo Engage te gebruiken, creeert een beheerder eerst de douanedienst van de a [ ](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#) in Marketo Engage, die de geloofsbrieven nodig voor authentificatie verstrekt.
Vervolgens maakt een productbeheerder voor Journey Optimizer B2B edition een verbinding met Marketo Engage door de gegevens in te voeren.
De gebruikers van Journey Optimizer B2B edition kunnen dan de verbinding van verwijzingen voorzien om de acties van Marketo Engage in <!-- Person and --> rekeningsreizen te vormen, zoals het toevoegen van of het verwijderen van mensen uit Marketo Engage lijsten of het toevoegen van hen aan verzoekcampagnes.

De zichtbaarheid van Marketo Engage-werkruimten voor elementen, zoals lijsten en campagnes, wordt bepaald door de rolinstellingen die zijn toegewezen in de aangepaste service.

Dezelfde verbinding kan meerdere keren worden gebruikt binnen een reis en verschillende Marketo Engage-verbindingen kunnen in één reis naast elkaar bestaan.

Wanneer een actie wordt uitgevoerd, gebruikt het het Beleid van de Selectie om te bepalen welke persoon in Marketo Engage registreert om te selecteren als de veelvoudige herkenningstekens in het verenigde persoonsprofiel bestaan. U kunt onder andere de oudste, nieuwste of alle overeenkomende Marketo Engage-records kiezen. Mensen gaan de reis door ongeacht een overeenkomst, behalve wanneer een fout optreedt.

## Een Marketo Engage-verbinding configureren

Configureer een Marketo Engage-instantie op afstand voor gebruik met Marketo Engage-reishandelingen.

### De aangepaste Marketo Engage-service maken

1. Meld u als beheerder aan bij Marketo Engage en maak een aangepaste service.
1. Neem de volgende waarden op die u voor de verbinding wilt gebruiken:

   * Munchkin-id
   * Client-id
   * Clientgeheim

### Integratie toevoegen

![ voeg integratiedetails ](assets/integration-connection-details.png) toe

1. In Journey Optimizer B2B edition, navigeer aan **Beleid** > **Configuraties**.
1. Selecteer aan de **Integraties** tabel.
1. Klik op **[!UICONTROL Create a connection]**.
1. Voer een naam (vereist) en beschrijving (optioneel) in.
1. Selecteer het beleid van de a **Selectie** voor passende persoonverslagen.
1. Voer uw Munchkin-id, client-id en clientgeheim in.
1. Klik op **[!UICONTROL Connect to Marketo]**.
1. Klik op **[!UICONTROL Create]**.

Wanneer een markeerteken een Marketo Engage-handeling tijdens een rit gebruikt, kunnen ze het knooppunt configureren met de naam van de verbinding.

Met de voltooide integratie, zijn de acties van Marketo Engage beschikbaar van **Acties op:** in de knoopeigenschappen.

![ de actielijst van Marketo ](assets/marketo-actions-list.png)