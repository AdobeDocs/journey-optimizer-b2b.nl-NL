---
title: WhatsApp Channel Setup
description: Sluit uw WhatsApp Business-account aan via de Meta Cloud-API om WhatsApp-berichten in te schakelen voor Journey Optimizer B2B edition-accountreizen.
feature: Setup, Channels
role: Admin
source-git-commit: 6313d097634af92450e6dd107fc5ba8040170e88
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 0%

---

# WhatsApp-kanaalinstelling

Adobe Journey Optimizer B2B edition verzendt WhatsApp-berichten via de Meta Cloud-API. Voordat marketeers WhatsApp-berichten voor accountreizen kunnen maken, moet een productbeheerder een WhatsApp-kanaal configureren.

![&#x200B; whatsApp taakstroom voor Journey Optimizer B2B edition &#x200B;](./assets/whatsapp-flow-diagram.png)

## Vereisten

Voordat u het WhatsApp-kanaal configureert, moet u het volgende doen:

* [Een Meta Business Manager-account](https://business.facebook.com/)
* [Een whatsApp Business-account met een geverifieerde gebruikersnaam en telefoonnummer](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Een Meta-verificatietoken voor gebruikers met de juiste machtigingen](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Goedgekeurde berichtsjablonen in uw whatsApp Business-account](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

>[!IMPORTANT]
>
>Voor uw gebruik van WhatsApp-communicatieservices gelden de bepalingen en voorwaarden van Meta. Door tot het overseinen WhatsApp door Journey Optimizer B2B edition toegang te hebben, erkent u dat u hebt herzien en ermee akkoord gegaan om aan [&#x200B; Van Bedrijfs Meta te voldoen WhatsApp beleid &#x200B;](https://www.whatsapp.com/legal/business-policy/).

## Beperkingen {#limitations}

De volgende beperkingen gelden voor het WhatsApp-kanaal:

* Adobe Journey Optimizer B2B edition is volgzaam niet HIPAA **en niet HIPAA-klaar**. Bovendien vallen derde verkopers niet onder Adobe BAA. Klanten zijn verantwoordelijk voor hun eigen compatibiliteit en validatie van leveranciers.

* Geautomatiseerde of vooraf gedefinieerde antwoordberichten worden nog niet ondersteund.

* Vanaf april 2025 heeft Meta de levering tijdelijk opgeschort van alle marketingsjabloonberichten aan WhatsApp-gebruikers die een Amerikaans telefoonnummer hebben (een nummer dat bestaat uit een +1-kiescode en een Amerikaanse netnummer). [&#x200B; leer meer in de documentatie van Meta &#x200B;](https://developers.facebook.com/documentation/business-messaging/whatsapp/templates/marketing-templates/per-user-limits/)

* De native integratiefunctionaliteit staat geen integratie met een externe Business Service Provider (BSP) toe.

## De kanaalconfiguratie voltooien

Voordat u uw WhatsApp-bericht verzendt, moet u de Journey Optimizer B2B edition-omgeving configureren en deze verbinden met uw WhatsApp-account.

Voer de volgende taken uit:

1. [De whatsApp API-referenties maken](#create-whatsapp-api-credentials)
1. [De whatsApp-webhaken toevoegen](#configure-webhooks)
1. [De WhatsApp-kanaalconfiguratie maken](#create-channel-configuration)

### WhatsApp API-referenties maken

>[!NOTE]
>
>De beschreven instellingen zijn alleen toegankelijk voor gebruikers met beheerdersrechten.

1. Vouw de sectie **[!UICONTROL Administration]** in de linkernavigatie uit en klik op **[!UICONTROL Channels]** .

1. Vouw **[!UICONTROL WhatsApp Settings]** uit in het deelvenster en selecteer **[!UICONTROL API Credentials]** .

   ![&#x200B; Beleid > Kanalen met de montages WhatsApp uitgevouwen &#x200B;](./assets/config-whatsapp-channels.png){width="800" zoomable="yes"}

1. Klik op **[!UICONTROL Create new API credentials]** rechtsboven.

1. Configureer uw API-referenties, zoals hieronder wordt beschreven:

   * **[!UICONTROL Name]** - Voer een unieke naam in voor de referenties
   * **[!UICONTROL API Token]** - Voer uw API-token in. Voor informatie, verwijs naar de [&#x200B; Documentatie van Meta &#x200B;](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/).
   * **[!UICONTROL Business Account ID]** - Voer het unieke nummer in dat aan uw bedrijfsportefeuille is gekoppeld. Voor informatie, verwijs naar de [&#x200B; Documentatie van Meta &#x200B;](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![&#x200B; WhatsApp instellingen API-referenties &#x200B;](./assets/config-whatsapp-channels-api-credentials.png){width="500" zoomable="yes"}

1. Klik op **[!UICONTROL Continue]** .

1. Kies de **[!UICONTROL WhatsApp Business Account]** die u wilt verbinden met uw whatsApp API-referenties.

   ![&#x200B; WhatsApp montages API geloofsbrieven selecteren bedrijfsrekening &#x200B;](./assets/config-whatsapp-channels-api-credentials-details.png){width="500" zoomable="yes"}

1. Selecteer de **[!UICONTROL Sender name]** die u wilt gebruiken voor het verzenden van WhatsApp-berichten.

   De instellingen voor het telefoonnummer worden automatisch ingevuld:

   * **Classificatie van de Kwaliteit** - wijst op klant terugkoppelt voor berichten die in de afgelopen 24 uren worden verzonden.
      * Groen: Hoge kwaliteit
      * Geel: Medium-kwaliteit
      * Rood: lage kwaliteit

     Voor meer informatie, zie {de classificatie van de Kwaliteit 0} _[&#128279;](https://www.facebook.com/business/help/766346674749731#) in de documentatie van Meta._

   * **Output** - wijst op het tarief waaraan uw telefoonaantal berichten kan verzenden.

1. Klik op **[!UICONTROL Submit]** wanneer u de configuratie van uw API-referenties hebt voltooid.

Wanneer u op _[!UICONTROL Submit]_&#x200B;klikt, worden de referenties direct gevalideerd en opgeslagen en wordt u omgeleid naar de pagina met&#x200B;_[!UICONTROL API credentials]_ -lijsten.

Als de ingediende referenties ongeldig zijn, geeft het systeem een HTTP 500-foutbericht weer. In dat geval kunt u de configuratie annuleren of bijwerken en opnieuw verzenden.

+++Problemen met HTTP 500-fouten oplossen

Als er een HTTP 500-fout optreedt bij het configureren van WhatsApp API-referenties, voert u de volgende stappen voor het oplossen van problemen uit:

1. Verifieer uw rechten van Adobe - bevestig dat uw organisatie _cjm_ whatsapp _ provisioned bevoegdheid heeft. Zonder deze machtiging kan het WhatsApp-kanaal niet worden geconfigureerd.

1. Valideer de velden voor uw zakelijke account - zorg ervoor dat alle verplichte velden juist zijn:

   * API Token - moet een geldig [&#x200B; toegangstoken van Meta met aangewezen toestemmingen &#x200B;](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/) zijn.
   * Bedrijfs identiteitskaart van de Rekening - moet uw [&#x200B; Van Bedrijfs Meta identiteitskaart &#x200B;](https://www.facebook.com/business/help/1181250022022158?id=180505742745347) precies aanpassen.

1. Test de referenties extern - Controleer uw gegevens rechtstreeks met de Meta API om te controleren of het probleem met de referenties is of met de aanmeldingsgegevens van Journey Optimizer B2B edition.

<!-- 1. Enable advanced logging - To identify internal server or authentication misconfigurations, enable advanced logs in your Journey Optimizer B2B Edition environment to provide detailed information about the API call failures. 
do we have advanced logs? How are they enabled?-->

1. Neem contact op met Adobe: als de omgeving en rechten geldig zijn en de HTTP 500-fout zich blijft voordoen, neemt u contact op met uw Adobe-vertegenwoordiger.

+++

### De whatsApp-webhaken toevoegen {#configure-webhooks}

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin-whatsapp-webhook-inbound-keyword-category"
>title="Binnenkomende trefwoordcategorie"
>abstract="<b> Opt-binnen </b>: verzendt uw bepaalde auto-reactie wanneer een gebruiker intekent. <br/><b> Opt-uit </b>: verzendt uw bepaalde auto-reactie wanneer een gebruiker afmeldt. <br/><b> Hulp </b>: verzendt uw bepaalde auto-reactie wanneer een gebruiker om hulp of steun verzoekt. <br/><b> Gebrek </b>: verzendt uw fallback auto-reactie wanneer geen sleutelwoorden aanpassen."

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin_whatsapp-webhook-inbound-keyword"
>title="Trefwoorden invoeren"
>abstract="U kunt trefwoorden definiëren om specifieke automatische reacties te activeren op basis van de gebruikerstekst. Trefwoorden zijn niet hoofdlettergevoelig (stop en STOP worden op dezelfde manier behandeld)."

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin-whatsapp-webhook-webhook-url"
>title="URL voor terugbellen"
>abstract="De validatieaanvraag en webhaakmeldingen voor dit object worden naar de opgegeven URL verzonden."

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin-whatsapp-webhook-verify-token"
>title="Token verifiëren"
>abstract="Het token dat Meta terugweergeeft om de callback-URL tijdens het verificatieproces te bevestigen en te verifiëren."

Met webhaks kan Journey Optimizer B2B edition binnenkomende berichten, toestemmingsreacties en leveringsmeldingen van uw WhatsApp Business-account ontvangen. Webhaken configureren om te zorgen voor een correct beheer van de toestemming en het bijhouden van berichten.

>[!NOTE]
>
>Zonder opgegeven opt-in- of opt-out-trefwoorden zijn standaardtoestemmingsberichten niet ingeschakeld.

Wanneer de whatsApp API-referenties zijn gemaakt, kunt u de webhooks configureren.

1. Selecteer **[!UICONTROL WhatsApp Webhooks]** in het navigatievenster.

1. Klik op **[!UICONTROL Create Webhook]** .

1. Voer een **[!UICONTROL Name]** in voor de configuratie van de webhaak.

1. Selecteer voor **[!UICONTROL Configuration]** de API-referenties (die in de vorige taak zijn gemaakt) die u aan de webhaak wilt koppelen.

1. Kies voor **[!UICONTROL Inbound keyword category]** een categorie om trefwoorden en het antwoordbericht te definiëren:

   * **[!UICONTROL Opt-in]** - Gebruikers moeten actief overeenkomen WhatsApp-berichten te ontvangen, die vaak via formulieren op uw website of app worden beheerd.
   * **[!UICONTROL Opt-out]** - Configureer uw webhaak om te luisteren naar uitdrukkingen zoals `Stop` of `No Message` om gebruikers automatisch te markeren als &#39;opted-out&#39;.
   * **[!UICONTROL Help]** - Sta geautomatiseerde systemen toe om te ontdekken wanneer een gebruiker `HELP` (of gelijkaardige sleutelwoorden zoals `Unknown`) verzendt en automatisch met specifieke informatie, zoals de dienstinstructies te antwoorden.
   * **[!UICONTROL Default]** - Binnenkomende berichten verwerken die niet overeenkomen met specifiek gedefinieerde trefwoorden. Het dient als reservecategorie om volgende gebeurtenissen (zoals opent en leveringsrapporten) in de datasets van Adobe Experience Platform toe te laten.

   Wanneer u de trefwoordcategorie selecteert, worden de standaardtrefwoorden ingevuld.

1. Voor **[!UICONTROL Enter a keyword]**, kunt u een douanesleutelwoord ingaan en _klikken toevoegt_ ( **+** ).

   U kunt meerdere trefwoorden per categorie toevoegen.

   >[!NOTE]
   >
   >Trefwoorden zijn niet hoofdlettergevoelig (`stop` en `STOP` worden op dezelfde manier behandeld).

1. Voer de **[!UICONTROL Reply message]** in om automatisch te verzenden wanneer een ontvangen bericht overeenkomt met een trefwoord in deze categorie.

   ![&#x200B; whatsApp montageswebhooks met Opt-in sleutelwoorden en antwoordbericht &#x200B;](./assets/config-whatsapp-channels-webhooks.png){width="500" zoomable="yes"}

1. Voor elke extra sleutelwoordcategorie wilt u vormen, _toevoegen_ (**+**) bij de hoogste juiste hoek en herhalen stappen 5-7.

1. Klik op **[!UICONTROL Submit]** om de configuratie van de website op te slaan.

### Token en URL kopiëren

Nadat de website is verzonden, kunt u de token- en URL-waarden ophalen en deze vervolgens registreren in Meta.

1. In de **[!UICONTROL WhatsApp Webhooks]** lijst, klik uitgeven ( ![&#x200B; pictogram &#x200B;](../assets/do-not-localize/icon-edit.svg) uitgeeft) pictogram voor de webhaak u creeerde.

1. Kopieer de waarden **[!UICONTROL Verify Token]** en **[!UICONTROL Webhook URL]** .

   ![&#x200B; WhatsApp montages webhaak montages om URL te kopiëren en teken te verifiëren &#x200B;](./assets/config-whatsapp-channels-webhooks-copy-token-url.png){width="500" zoomable="yes"}

1. In [&#x200B; Meta voor het portaal van Ontwikkelaars &#x200B;](https://developers.facebook.com/), navigeer aan uw WhatsApp toepassingsmontages en vorm webhaak gebruikend de waarden die u kopieerde.

### Kanaalconfiguratie maken {#create-channel-configuration}

Een kanaalconfiguratie bepaalt de leveringsmontages die worden gebruikt wanneer het verzenden van berichten WhatsApp van een knoop van de reisactie.

1. Selecteer **[!UICONTROL Channel configurations]** onder _[!UICONTROL General settings]_&#x200B;in het navigatievenster.

   ![&#x200B; de configuratielijst van het Kanaal &#x200B;](./assets/config-whatsapp-channels-general.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Create channel configuration]** rechtsboven.

1. Voer een **[!UICONTROL Name]** en **[!UICONTROL Description]** (optioneel) in voor de configuratie.

   >[!NOTE]
   >
   >De naam moet met een brief (a-z) beginnen en kan slechts alfanumerieke karakters, onderstrepingstekens (`_`), punten (`.`), en koppeltekens (`-`) bevatten.

1. Kies `WhatsApp` bij **[!UICONTROL Select channel]** .

<!-- 1. For **[!UICONTROL Marketing action]**, select one or more marketing actions to associate consent policies with this configuration.

   Make sure to include all applicable marketing actions to ensure compliance with customer preferences.

   All consent policies associated with a selected marketing action are automatically leveraged in order to respect the preferences of your customers. For example, any WhatsApp message using that configuration in a journey is only sent to the profiles who have consented to receive WhatsApp messages from you. Profiles who have not consented to receive these communications are excluded. -->

1. Selecteer onder _[!UICONTROL WhatsApp Settings]_&#x200B;de **[!UICONTROL WhatsApp configuration]**(API-referenties) die u in de vorige taak hebt gemaakt.

1. Voer de **[!UICONTROL Sender phone number]** in die u wilt gebruiken voor het verzenden van berichten.

   ![&#x200B; WhatsApp details van de kanaalconfiguratie &#x200B;](./assets/config-whatsapp-channels-general-create.png){width="500" zoomable="yes"}

1. (Momenteel niet van toepassing op Journey Optimizer B2B edition) Selecteer voor **[!UICONTROL WhatsApp Execution Field]** het profielkenmerk dat u als prioritair telefoonnummer wilt gebruiken wanneer meerdere telefoonnummers beschikbaar zijn voor een ontvanger.

1. Klik op **[!UICONTROL Submit]** om de configuratie op te slaan of op **[!UICONTROL Save as draft]** om de configuratie later te voltooien en te verzenden.

De configuratie toont aanvankelijk met de status van de a _Verwerking_ terwijl de bevestigingscontroles in werking stellen. Wanneer alle controles overgaan, verandert de status in **_Actief_** en de configuratie is klaar om te worden geselecteerd wanneer de auteur WhatsApp van marketers berichten in reisacties.
