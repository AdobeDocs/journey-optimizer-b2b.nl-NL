---
title: Configuratie van externe handelingen
description: Leer hoe ontwikkelaars, beheerders en marketers samenwerken om externe acties te implementeren, te configureren en te gebruiken die Journey Optimizer B2B edition verbinden met externe services tijdens reizen voor accounts.
feature: Setup, Integrations
role: Admin, Developer
source-git-commit: 6d3967babc1bc868fde0c76ac9068e63156070cd
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 2%

---

# Configuratie van externe acties

Met externe maatregelen kunnen reizen van accounts in Journey Optimizer B2B edition rechtstreeks vanaf het canvas verbinding maken met externe systemen. Wanneer een rekeningspubliek een externe actieknoop bereikt, doet het systeem een asynchrone uitgaande vraag aan de gevormde externe dienst, die de gegevens van de publieksattributen voor rekeningen, mensen, of allebei overgaat. De externe dienst verwerkt de gegevens en antwoordt gebruikend callback, terugkerende publieksgegevens en meta-gegevens die kunnen worden gebruikt om reisuitvoering te begeleiden.

Deze eigenschap steunt twee types van wegknooppunten:

* **Externe actie** - roept de externe dienst en gaat langs één enkele uitgaande weg verder. Ideaal voor _brand-en-vergeet_ integratie, zoals het bijwerken van een verslag van CRM of het teweegbrengen van een stroomafwaarts bericht.
* **Externe gespleten wegen** - roept de externe dienst en evalueert de reactie op routerekeningen langs één van verscheidene bepaalde wegen.

>[!NOTE]
>
>De diensten voor extern optreden worden alleen ondersteund voor reizen voor rekening. Deze knooppunttypes zijn niet beschikbaar voor personenreizen.

## Overzicht van implementatie

Voor het opzetten van externe acties is coördinatie nodig over drie opeenvolgende taken:

| | Functie | Taak |
| ---- | ---- | ---- |
| 1 | Ontwikkelaar | [&#x200B; voert en publiceert de externe dienst &#x200B;](#implement-service) uit |
| 2 | Beheerder | [&#x200B; vorm de actie in Journey Optimizer B2B edition &#x200B;](#configure-action) |
| 3 | Marketer | [&#x200B; voeg een externe knoop aan een rekeningsreis &#x200B;](#add-journey-node) toe |

## De externe service implementeren {#implement-service}

De ontwikkelaar moet tot stand brengen en publiceren de openbaar-onder ogen ziet Webdienst die aan de [&#x200B; Interface van de Leverancier van de Dienst van de Actie van Adobe Journey Optimizer B2B edition &#x200B;](https://developer.adobe.com/journey-optimizer-b2b-apis/) voldoet.

>[!NOTE]
>
>De callback functie vereist een dragertoken. Haal dit door vestiging [&#x200B; OAuth Server-aan-Server geloofsbrieven in Adobe Developer Console &#x200B;](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation) voor uw organisatie IMS op.

Nadat de service live is, geeft u de URL naar de OpenAPI-specificatie en de verificatiegegevens door aan de productbeheerder die verantwoordelijk is voor het configureren van de handeling.

## De handeling configureren {#configure-action}

Een actie moet worden gevormd en geactiveerd alvorens de verkopers het in een reis kunnen gebruiken. De acties worden gecreeerd in _Laag_ staat en uw veranderingen worden automatisch bewaard. Het blijft een concept totdat u het activeert.

>[!PREREQUISITES]
>
>Haal de URL naar de OpenAPI-specificatie en de verificatiereferenties op van de ontwikkelaar voordat u de configuratie toevoegt.
>
>Om een externe actie te bepalen en te activeren, moet u de _[!UICONTROL Manage B2B Admin Configurations]_[&#x200B; producttoestemming &#x200B;](./user-management.md#b2b-product-permissions) hebben.

1. Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** .

1. Klik op **[!UICONTROL External Actions]** in het middelste deelvenster.

   ![&#x200B; heb toegang tot de Externe de configuratieruimte van Acties &#x200B;](./assets/configuration-external-actions-list.png){width="800" zoomable="yes"}

1. Klik op **[!UICONTROL Create action]** rechtsboven.

1. Voer de URL in naar de OpenAPI-specificatie voor uw externe service en klik op **[!UICONTROL Create]** .

   ![&#x200B; ga de dienst URL &#x200B;](./assets/configuration-external-actions-create-url.png){width="500"} in

   >[!NOTE]
   >
   >Uw externe dienst moet levend en bereikbaar voor deze stap zijn om te slagen.

1. Wanneer de URL is omgezet, controleert u de **[!UICONTROL Service details]** .

   De servicedetails worden rechtstreeks gelezen uit de OpenAPI-specificatie wanneer de handeling wordt gemaakt. U kunt deze eigenschappen niet wijzigen in de configuratie nadat u ze hebt gemaakt.

   | Eigenschap | Beschrijving | De eigenschap OpenAPI Spec |
   | -------- | ----------- | --------------------- |
   | [!UICONTROL Name] | Naam voor de actie | `info.title` |
   | [!UICONTROL Description] | Beschrijving van de actie | `info.description` |
   | [!UICONTROL URL] | URL aan de specificatie OpenAPI die de externe dienst bepaalt | `servers.url` |

1. Voer de **[!UICONTROL Authentication]** referenties voor de externe service in (`components.securitySchemes` ).

   >[!NOTE]
   >
   >De weergegeven referentie-velden zijn afhankelijk van het verificatiemechanisme dat in de externe service is gedefinieerd. Ondersteunde typen zijn API-sleutel, OAuth2 en HTTP Basic-verificatie.

   ![&#x200B; voeg de authentificatiegeloofsbrieven toe &#x200B;](./assets/configuration-external-actions-auth-credentials.png){width="600" zoomable="yes"}

   U kunt de geloofsbrieven veranderen zoals nodig wanneer de gevormde actie in het _Ontwerp_ of _Actieve_ status is.

1. Klik op **[!UICONTROL Next]** .

1. Stel de eigenschappen van **[!UICONTROL Configurations]** in om te bepalen hoe de handeling gegevens uitwisselen met de externe service.

   >[!NOTE]
   >
   >De eigenschappen die als _worden gemerkt Statisch_ zijn niet updatable in configuratietijd en zijn gebaseerd op de de dienstdefinitie.

   * **[!UICONTROL Action type]** (_Statisch_) - het gesteunde type van de wegknoop:

      * [!UICONTROL External action] (`enableSplitPath` = false)
      * [!UICONTROL External action split path] (`enableSplitPath` = true)

     U kunt het actietype niet wijzigen nadat u de actieconfiguratie hebt gemaakt.

   * **[!UICONTROL Accessors]** (_Statisch_) - (De Externe actie gespleten weg slechts) de variabelen die door de externe dienst zijn teruggekeerd om als wegvoorwaarden in een Externe gespleten wegknoop beschikbaar te zijn. (`invocationPayloadDef.accessorsMetadata`)

   * **[!UICONTROL Journey context]** (_Statisch_) - het werkingsgebied van publieksgegevens die in het verzoek (`supportedEntityType` worden verzonden):

      * [!UICONTROL Account] - alleen accounts verzenden

      * [!UICONTROL People] - Verzendt alleen personen

      * [!UICONTROL People in Account] - Hiermee verzendt u accounts en personen die met een account te maken hebben

   * **[!UICONTROL Outgoing Fields]** - kaart elk gebied in de lijst aan een [&#x200B; XDM gebied &#x200B;](../admin/xdm-field-management.md) in kaart. Deze velden worden in de aanvraaginstantie naar de externe service verzonden. Servicedefinitie-eigenschappen: `invocationPayloadDef.accountFields`, `invocationPayloadDef.fields` .

   ![&#x200B; de externe actie van de Kaart uitgaande gebieden &#x200B;](./assets/configuration-external-actions-fields.png){width="600" zoomable="yes"}

   * **[!UICONTROL Incoming Fields]** - kaart elk gebied in de lijst aan een [&#x200B; updatable XDM gebied &#x200B;](../admin/xdm-field-management.md#updatable-fields) in kaart. Deze gebieden worden bevolkt van de externe de dienstreactie. Servicedefinitie-eigenschappen: `callbackPayloadDef.accountFields`, `callbackPayloadDef.fields` . Kan na het maken worden bijgewerkt.

   * **[!UICONTROL Header parameters]** - Voer een waarde in voor elke rij die als HTTP-header in de aanvraag moet worden doorgegeven. Service definition property: `invocationPayloadDef.headers`.

   * **[!UICONTROL Timeout]** - ga het aantal minuten in te wachten op de externe dienst om callback aan te halen alvorens het verzoek als ontbroken wordt beschouwd. Service definition property: `timeout`.

   * **[!UICONTROL Global attributes]** - ga een waarde voor elke rij in om als statisch gebied in het verzoeklichaam op te nemen. Service definition property: `invocationPayloadDef.globalAttributes`.

   ![&#x200B; Externe parameters van de actiekop, onderbreking, en globale attributen &#x200B;](./assets/configuration-external-actions-header-timeout-global.png){width="600" zoomable="yes"}

1. Klik de _Achterpijl_ om aan de lijst terug te keren en de actie in de staat van het a _Ontwerp_ te houden.

   Of, klik **[!UICONTROL Activate]** om de actieconfiguratie in de _Actieve_ staat te veranderen. De geconfigureerde externe actie moet actief zijn om deze beschikbaar te maken voor gebruik tijdens reizen op account.

## Een extern knooppunt aan een reis toevoegen {#add-journey-node}

Nadat een handeling is geactiveerd, kunnen marketers een knooppunt _[!UICONTROL External action]_&#x200B;of&#x200B;_[!UICONTROL External split path]_ toevoegen aan elke accountreis. Voor informatie over hoe te om deze knopen in het canvas van de rekeningsreis toe te voegen en te gebruiken, zie [&#x200B; Externe knopen &#x200B;](../journeys/external-nodes.md).
