---
title: SMS-authoring
description: Leer hoe u SMS-berichten naar uw klanten op hun mobiele apparaten kunt verzenden en hoe u berichten in tekstindeling kunt personaliseren en voorvertonen vanuit de SMS-editor.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e0d9359560f31b3e66f593426c66e64d31044d54
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# SMS-authoring

Gebruik Adobe Journey Optimizer B2B Edition om SMS-berichten (text messages) naar uw klanten op hun mobiele apparaten te verzenden. U kunt berichten in tekstformaat van de redacteur van SMS tot stand brengen, personaliseren en voorproef.

## SMS-configuraties

Adobe Journey Optimizer B2B Edition verzendt tekstberichten via SMS-serviceproviders (of SMS-gatewayproviders). Voordat u uw SMS-bericht maakt, configureert u uw serviceprovider via de beheerdersinstellingen.

### SMS-gatewayserviceproviders

Adobe Journey Optimizer B2B Edition is momenteel geïntegreerd met externe providers die services voor tekstberichten onafhankelijk aanbieden. Ondersteunde providers voor tekstberichten zijn Sinch, Twilio en Infobip.

Voordat u een SMS-kanaal configureert in Adobe Journey Optimizer B2B Edition, moet u een account met een van deze providers maken om uw API-token en service-id op te halen. Deze referenties zijn vereist om de verbinding tussen Adobe Journey Optimizer B2B Edition en de toepasselijke provider te configureren.

>[!IMPORTANT]
>
>Voor het gebruik van services voor tekstberichten gelden aanvullende voorwaarden van de betreffende provider. Als oplossingen van derden zijn Sinch, Twilio en Infobip via integratie beschikbaar voor Adobe Journey Optimizer B2B Edition-gebruikers. Adobe heeft geen betrekking op producten van derden en is niet verantwoordelijk voor deze producten. Neem contact op met uw provider voor problemen met of verzoeken om assistentie met betrekking tot de SMS-services.

### Een bestaande API-configuratie voor SMS controleren

>[!NOTE]
>
>De beschreven instellingen zijn alleen toegankelijk voor gebruikers met SMS-beheerdersrechten.

Vouw de sectie **[!UICONTROL Administrator]** in de linkernavigatie uit en klik op **[!UICONTROL Configuration]** .

![ heb toegang tot de configuratie van AMA API geloofsbrieven ](./assets/config-sms-api.png){width="800" zoomable="yes"}

De pagina bevat de beschikbare API-configuraties voor uw instantie. U kunt de weergegeven API-referenties filteren door de SMS-serviceprovider of maker.

![ klik het filterpictogram om de lijst van API geloofsbrieven te filtreren ](./assets/config-sms-api-filter.png){width="500"}

### Nieuwe API-referenties maken voor een SMS-serviceprovider

>[!BEGINTABS]

>[!TAB  Sinch ]

_om Sinch als uw leverancier van SMS met de Uitgave van Adobe Journey Optimizer te vormen B2B:_

1. Vouw de sectie **[!UICONTROL Administrator]** in de linkernavigatie uit en klik op **[!UICONTROL Configuration]** .

1. Klik op **[!UICONTROL Create new API credentials]** rechtsboven in de lijst _[!UICONTROL API credentials]_.

1. Vorm uw geloofsbrieven van SMS API:

   ![ vorm de Sinch SMS API geloofsbrieven ](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL SMS vendor]** - Kies `Sinch` als SMS-provider.

   * **[!UICONTROL Name]** - Voer een naam in voor uw API-referentie.

   * **[!UICONTROL Service ID]** en **[!UICONTROL API Token]** - Ga naar de pagina met API&#39;s van uw Sinch-account (u vindt uw gegevens onder het tabblad SMS).

   Voor meer informatie over het vinden van deze informatie voor uw rekening van Sinch, zie de [ de ontwikkelaarsdocumentatie van Sinch ](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Klik op **[!UICONTROL Submit]** wanneer de configuratiegegevens van de API-referenties zijn voltooid.

>[!TAB  Twilio ]

_om Twilio als uw leverancier van SMS met de Uitgave van Adobe Journey Optimizer te vormen B2B:_

1. Vouw de sectie **[!UICONTROL Administrator]** in de linkernavigatie uit en klik op **[!UICONTROL Configuration]** .

1. Klik op **[!UICONTROL Create new API credentials]** rechtsboven in de lijst _[!UICONTROL API credentials]_.

1. Vorm uw geloofsbrieven van SMS API:

   ![ vorm de geloofsbrieven van TwilioSMS API ](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL SMS vendor]** - Kies `Twilio` als SMS-provider.

   * **[!UICONTROL Name]** - Voer een naam in voor uw API-referentie.

   * **[!UICONTROL Account SID]** en **[!UICONTROL Auth Token]** - toegang tot de _ruit van Info van de Rekening_ van uw pagina van het dashboard van de Console van Twilio om uw geloofsbrieven te vinden.

   Voor meer informatie over het vinden van deze informatie voor uw rekening van Twilio, zie het [ Centrum van de Hulp van Twilio ](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Klik op **[!UICONTROL Submit]** rechtsboven op de pagina wanneer de configuratiegegevens van de API-referenties zijn voltooid.

>[!TAB  Infobip ]

_om Infobip als uw leverancier van SMS met de Uitgave van Adobe Journey Optimizer te vormen B2B:_

1. Vouw de sectie **[!UICONTROL Administrator]** in de linkernavigatie uit en klik op **[!UICONTROL Configuration]** .

1. Klik op **[!UICONTROL Create new API credentials]** rechtsboven in de lijst _[!UICONTROL API credentials]_.

1. Vorm uw geloofsbrieven van SMS API:

   ![ vorm de Inkoopip API geloofsbrieven ](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL SMS vendor]** - Kies `Infobip` als SMS-provider.

   * **[!UICONTROL Name]** - Voer een naam in voor uw API-referentie.

   * **[!UICONTROL API base URL]** en **[!UICONTROL API key]** - Ga naar de webinterface-homepage of de API-sleutelbeheerpagina voor uw Infobip-account om uw referenties te vinden.

   Voor meer informatie over het vinden van deze informatie voor uw Infobip rekening, zie de [ documentatie Infobip ](https://www.infobip.com/docs/api/_blank).

1. Klik op **[!UICONTROL Submit]** rechtsboven op de pagina wanneer de configuratiegegevens van de API-referenties zijn voltooid.

>[!ENDTABS]

Wanneer u op _[!UICONTROL Submit]_klikt, worden de referenties direct gevalideerd en opgeslagen en wordt u omgeleid naar de pagina met_[!UICONTROL API credentials]_ -lijsten. Als de verzonden referenties ongeldig zijn, wordt een foutbericht weergegeven op de pagina met lijsten. In dit geval kunt u de configuratie annuleren of deze bijwerken en opnieuw verzenden.

## Een SMS-actie toevoegen aan een accountreis

U kunt tekstberichtenleveringen instellen in een Account Journey wanneer u een _[!UICONTROL Take an action]_-knooppunt toevoegt en het volgende doet:

1. Kies **[!UICONTROL People]** voor het doel _[!UICONTROL Action on]_.

1. Kies **[!UICONTROL Send SMS]** bij _[!UICONTROL Action on people]_.

   ![ neem een actie - verzend sms ](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Klik onder aan het deelvenster _[!UICONTROL Take an action]_op **[!UICONTROL Create SMS]**.

1. Voer in het dialoogvenster een unieke **[!UICONTROL Name]** in voor de e-mail en een **[!UICONTROL Subject line]** .

   ![ creeer nieuwe dialoog van SMS ](assets/create-new-sms.png){width="500"}

## Het SMS-bericht maken

>[!IMPORTANT]
>
>**de toestemmingsbeheer van SMS**<br/>
><br/>
>In overeenstemming met de normen en voorschriften van de branche moeten alle SMS-marketingberichten een manier bevatten om de abonnees gemakkelijk af te melden. Om dit te doen, kunnen de ontvangers van SMS met opt-in en opt-out sleutelwoorden antwoorden. Alle standaardtrefwoorden voor aanmelden en weigeren worden ondersteund en gerespecteerd. Daarnaast worden aangepaste trefwoorden die voor uw SMS-serviceprovider zijn geconfigureerd, ondersteund en gerespecteerd.

1. Voer in het veld **[!UICONTROL Message]** de tekst in die u wilt verzenden.

   U kunt een bericht van maximaal 1600 karakters tot stand brengen, met elke 160 karakters die als één enkel SMS-bericht worden beschouwd.

1. **Personaliseer het tekstbericht**.

   Op om het even welk ogenblik terwijl het ontwerpen van het tekstbericht, klik _personaliseren_ pictogram rechts van het tekstberichtvakje.

   ![ klik het Persoonlijke pictogram om tokens aan het bericht toe te voegen ](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   De weergegeven pagina biedt toegang tot uw Adobe Marketo Engage Lead- en System-tokens. Zowel standaard als aangepaste tokens zijn inbegrepen. U kunt de bar van het Onderzoek gebruiken om van het teken de plaats te bepalen u wenst, of door de omslagboom navigeren om het even welke lood/systeemtekenen te vinden en te selecteren.

   Plaats de cursor op de locatie in het bericht waar u het token wilt toevoegen. Voeg een token toe door op de plusknop ( **+** ) naast de token te klikken. Als u het token wilt toevoegen met een fallback (standaardwaarde die wordt weergegeven als dat veld niet beschikbaar is voor een lead), klikt u op de ellips ( **...** ) en kiest u **[!UICONTROL Insert with fallback text]** .

   ![ klik de ellipsen om een reserve voor het teken ](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"} te gebruiken

   Voer in het dialoogvenster _[!UICONTROL Enter fallback value]_de tekst in die als fallback wordt weergegeven en klik op **[!UICONTROL Add]**.

   ![ ga de reservetekst voor het teken ](./assets/sms-message-personalize-fallback-text.png){width="400"} in

   Wanneer uw personalisatietokens worden geplaatst, klik **[!UICONTROL Save]** om veranderingen te bewaren en aan de belangrijkste het auteurswerkruimte van SMS terug te keren. U kunt het bericht desgewenst blijven bewerken met de tokens.

<!-- 1. **Add URLs to text message**.

   After defining your content, you can add URLs to your message by clicking the _Link_ icon.
   
   You can add two types of URLs: 

   External URLs - This is ANY external URL that can be directly typed into/ pasted into the input text box
   Adobe Marketo Engage Design Studio Landing Pages - Selecting this option, you will see a 'Landing Page picker' from which you can select any of the listed approved Landing Pages from Marketo Engage

   You can choose to 'shorten' either of these URLs by selecting the checkbox
   Note that the URL shortening function, uses the Marketo subdomain for shortening
   The shortened URL appears as a read-only field within the modal
   You can optionally track clicks on the URL
   You can also choose to include 'mkt_tok' for tracking activity against a user
   Click on Add to save changes & add the chosen URL to the SMS message
-->

## De SMS-eigenschappen instellen

1. Voer in de sectie _[!UICONTROL SMS properties]_een **[!UICONTROL Name]**(vereist, maximaal 100 cha\racter) en **[!UICONTROL Description]**(optioneel, maximaal 300 tekens) in voor uw bericht.

   Alpha, numerieke, speciale tekens zijn toegestaan voor deze velden. De volgende gereserveerde tekens zijn **niet toegestaan** : `\` , `/` , `:` , `*`, `?` , `"` , `<` , `>` en `|` .

1. Kies de **[!UICONTROL SMS Type]** :

   * Gebruik `Marketing` voor promotietekstberichten waarvoor toestemming van de gebruiker is vereist.
   * Gebruik `Transactional` voor niet-commerciële berichten, zoals orderbevestiging, wachtwoordherstelmeldingen of leveringsgegevens.

1. Kies bij **[!UICONTROL SMS configuration]** een van de vooraf gedefinieerde API-configuraties.

   Dit het plaatsen bepaalt welke de gatewaydienstverlener en rekening van SMS wordt gebruikt om het bericht te leveren.

1. Voer de **[!UICONTROL Sender number]** &#x200B; in die u voor uw communicatie wilt gebruiken.

   ![ neem een actie - verzend sms ](./assets/sms-properties.png){width="700" zoomable="yes"}

   Het nummer van de ontvanger wordt altijd toegewezen aan het veld `Lead.MainPhone` in het Marketo Engage.

<!-- ## Preview the text message content

When your message content is defined, you can use test profiles to preview its content. If you inserted personalized content, you can check how this content is displayed in the message, using test profile data.

1. Click **[!UICONTROL Simulate Content]** at the top of the SMS authoring workspace.

1. From the _[!UICONTROL Simulate Content]_ page, click **[!UICONTROL Add People]**.

1. Use the # page to manage the leads used for your test profile.

   In the displayed list, you can search for and add any of the leads (up to 10 leads at a time) from the Marketo Engage lead database.

   To search, enter the whole email address and click enter. The corresponding lead profile shows up for selection.

   The preview updated to the personalization fields for the selected profile.

   All the added leads appear on the left rail of the 'Simulate Content' page

   You can manage this list by adding more people and deleting individual leads from the profile listing (it does not remove them from the database).

1. Simulate content for a lead.

   Select any of the leads listed on the left rail of the Simulate Content page and the SMS preview on the page updates for the corresponding lead.

   You can also select a lead from the 'drop-down' box above the preview space and the SMS preview on the page updates for the corresponding lead

1. To exit the _[!UICONTROL Simulate Content]_ page and return back to the SMS authoring workspace, click Close. -->
