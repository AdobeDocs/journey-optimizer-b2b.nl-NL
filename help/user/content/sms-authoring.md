---
title: SMS Authoring
description: Leer hoe u SMS-berichten naar uw klanten op hun mobiele apparaten kunt verzenden en hoe u berichten in tekstindeling kunt personaliseren en voorvertonen vanuit de SMS-editor.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: eea4afcf352eeefbd5a67c4bfff6a4c2ec559319
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# SMS-authoring

Gebruik Adobe Journey Optimizer B2B Edition om SMS-berichten (text messages) naar uw klanten op hun mobiele apparaten te verzenden. U kunt berichten in tekstformaat van de redacteur van SMS tot stand brengen, personaliseren en voorproef.

## SMS-configuraties

Adobe Journey Optimizer B2B Edition verzendt tekstberichten via SMS-serviceproviders (of SMS-gatewayproviders). Alvorens uw bericht van SMS te creëren, vorm uw dienstverlener van de _montages van de Beheerder_.

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

1. **voegt URLs aan het tekstbericht** toe.

   Na het bepalen van uw inhoud, kunt u URLs aan uw bericht toevoegen door het _pictogram van de Verbinding_ te klikken.

   Met deze handeling wordt een dialoogvenster geopend waarin u een van de volgende twee typen URL&#39;s kunt kiezen:

   * **[!UICONTROL External URL]** - Dit type is een externe URL die u in het tekstvak invoert.
   * **[!UICONTROL Landing Page]** - Kies deze optie als u een van de goedgekeurde Adobe Marketo Engage Design Studio-bestemmingspagina&#39;s van uw Marketo Engage wilt selecteren.

   Het dialoogvenster bevat ook opties voor de URL-koppelingen:

   * **[!UICONTROL Shorten URL]** - selecteer dit checkbox aan _verkort_ URL, die voor het volgen noodzakelijk is. Voor een landingspagina wordt het subdomein Marketo Engage gebruikt voor de verkorte URL. Er wordt een voorbeeld van de verkorte URL-indeling weergegeven. De daadwerkelijke URL wordt gecreeerd wanneer SMS wordt verzonden naar de ontvanger.

   * **[!UICONTROL Include mkt_tok]** - Schakel dit selectievakje in om de activiteit van een gebruiker bij te houden.

   Wanneer de koppelingsopties zijn voltooid, klikt u op **[!UICONTROL Add]** om de wijzigingen op te slaan en de URL-koppeling toe te voegen aan het SMS-bericht.

## De SMS-eigenschappen instellen

1. Voer in de sectie _[!UICONTROL SMS properties]_een **[!UICONTROL Name]**(vereist, maximaal 100 tekens) en **[!UICONTROL Description]**(optioneel, maximaal 300 tekens) voor uw bericht in.

   Alpha, numerieke, speciale tekens zijn toegestaan voor deze velden. De volgende gereserveerde tekens zijn **niet toegestaan** : `\` , `/` , `:` , `*`, `?` , `"` , `<` , `>` en `|` .

1. Kies de **[!UICONTROL SMS Type]** :

   * Gebruik `Marketing` voor promotietekstberichten waarvoor toestemming van de gebruiker is vereist.
   * Gebruik `Transactional` voor niet-commerciële berichten, zoals orderbevestiging, wachtwoordherstelmeldingen of leveringsgegevens.

1. Kies bij **[!UICONTROL SMS configuration]** een van de vooraf gedefinieerde API-configuraties.

   Dit het plaatsen bepaalt welke de gatewaydienstverlener en rekening van SMS wordt gebruikt om het bericht te leveren.

1. Voer de **[!UICONTROL Sender number]** &#x200B; in die u voor uw communicatie wilt gebruiken.

   ![ neem een actie - verzend sms ](./assets/sms-properties.png){width="700" zoomable="yes"}

   Het nummer van de ontvanger wordt altijd toegewezen aan het veld `Lead.mobilePhone` in het Marketo Engage.

## Inhoud van tekstberichten simuleren {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Controleren hoe uw inhoud wordt gerenderd"
>abstract="Wanneer uw inhoud is gedefinieerd, kunt u deze voorvertonen en controleren of de rendering correct is voor het kanaal dat u gebruikt."

Wanneer de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om de inhoud ervan te simuleren (voor een voorvertoning). Als u persoonlijke inhoud hebt ingevoegd, kunt u met testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

>[!IMPORTANT]
>
>Sla uw SMS-bericht op voordat u het tekstbericht gaat simuleren.

1. Klik op **[!UICONTROL Simulate Content]** boven aan de werkruimte voor het schrijven van SMS.

1. Klik op **[!UICONTROL Add People]** op de pagina _[!UICONTROL Simulate Content]_.

1. Gebruik de _Simulate Inhoud_ pagina om de lood te beheren die voor uw testprofiel worden gebruikt.

   In de getoonde lijst, kunt u naar om het even welke lood zoeken en toevoegen (tot 10 lood tegelijk) van het Marketo Engage loodgegevensbestand.

   Om te zoeken, ga het volledige e-mailadres in en het drukken _gaat_ binnen. Het bijbehorende hoofdprofiel wordt weergegeven voor selectie.

   De voorvertoning wordt bijgewerkt naar de aanpassingsvelden voor het geselecteerde profiel.

   Alle toegevoegde leads worden links weergegeven.

   U kunt deze lijst beheren door meer personen toe te voegen en afzonderlijke leads te verwijderen uit de profiellijst (deze worden niet verwijderd uit de database).

1. Inhoud voor een geselecteerde lead simuleren.

   Selecteer een van de links vermelde leads en de SMS-voorvertoning op de pagina-updates voor de bijbehorende lead.

   U kunt ook een lead selecteren in de kiezer boven de voorvertoningsruimte om de SMS-voorvertoning op de pagina voor de bijbehorende lead bij te werken.

1. Als u de pagina _[!UICONTROL Simulate Content]_wilt afsluiten en wilt terugkeren naar de werkruimte voor het schrijven van SMS, klikt u op **[!UICONTROL Close]**rechtsboven.

## Beheer van SMS-toestemmingen

Het is een wettelijke vereiste om ontvangers de mogelijkheid te bieden zich niet meer te abonneren op het ontvangen van communicatie van een merk en deze keuze te respecteren. Als u deze regels niet naleeft, brengt u juridische risico&#39;s met zich mee voor uw merk. Deze functie helpt u ook vermijden verzendend ongevraagde mededelingen naar uw ontvangers, die hen kunnen veroorzaken om uw berichten als spam te merken en uw reputatie te schaden.

Wanneer u deze optie aanbiedt, kunnen SMS-ontvangers reageren met de trefwoorden opt-in en opt-out. Alle standaard opt-in en opt-out sleutelwoorden worden gesteund en gehonoreerd, en om het even welke douanesleutelwoorden die bij de dienstverlener van SMS worden gevormd. Als u geen abonnement hebt, worden de profielen automatisch verwijderd uit het publiek van toekomstige marketingberichten.

Journey Optimizer B2B Edition biedt de mogelijkheid om de optie om te weigeren in SMS-berichten te beheren met behulp van de volgende logica:

* Als een lead ervoor heeft gekozen geen communicatie van u te ontvangen, wordt het bijbehorende profiel standaard uitgesloten van daaropvolgende SMS-leveringen

* Deze toestemming voor leads die afkomstig is van verschillende bronnen (zoals AEP of de SMS-serviceprovider) wordt gesynchroniseerd met Journey Optimizer B2B Edition. Momenteel ondersteunt het slechts één enkele toestemmingsstaat per lood op instantieniveau (een lood &quot;Jan Smit&quot; wordt geabonneerd op of afgemeld van alle promotionele SMS in het geval). Momenteel biedt het geen ondersteuning voor dubbele opt-in op merkniveau/toestemming op het niveau van individuele abonnementenlijsten.
