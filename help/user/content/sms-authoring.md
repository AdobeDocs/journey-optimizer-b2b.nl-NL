---
title: SMS Authoring
description: Maak sms-berichten voor accountreizen met personalisatie, koppelingen en toestemmingsbeheer - bekijk de inhoud en configureer leveringsinstellingen in Journey Optimizer B2B edition.
feature: SMS Authoring, Content, Channels
role: User
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: aa79e0655737541f122801f28db73d9f31ebb2f7
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 0%

---

# SMS-authoring

Met Adobe Journey Optimizer B2B edition kunt u SMS-berichten (text messages) naar uw klanten verzenden op hun mobiele apparaten. U kunt berichten in tekstformaat van de redacteur van SMS tot stand brengen, personaliseren en voorproef.

Alvorens de berichten van SMS voor rekeningsreizen te creëren, zorg ervoor dat de [&#x200B; dienstverlener van SMS &#x200B;](../admin/configure-channels-sms.md) van de _[!UICONTROL Administrator]_&#x200B;montages wordt gevormd.

## Een SMS-actie toevoegen aan een accountreis

U kunt tekstberichtenleveringen instellen tijdens een accountreis wanneer u een knooppunt _[!UICONTROL Take an action]_&#x200B;toevoegt en het volgende doet:

1. Kies _[!UICONTROL Action on]_&#x200B;voor het doel **[!UICONTROL People]**.

1. Kies _[!UICONTROL Action on people]_&#x200B;bij **[!UICONTROL Send SMS]**.

   ![&#x200B; neem een actie - verzend sms &#x200B;](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Klik onder aan het deelvenster _[!UICONTROL Take an action]_&#x200B;op **[!UICONTROL Create SMS]**.

1. Voer in het dialoogvenster een unieke **[!UICONTROL Name]** voor het SMS-bericht in.

   ![&#x200B; creeer nieuwe dialoog van SMS &#x200B;](assets/create-new-sms.png){width="400"}

1. Klik op **[!UICONTROL Create]**.

   De _kaart van de Reis_ opent en u kunt het bericht tot stand brengen en de eigenschappen van SMS plaatsen om het bericht te verzenden.

### Het SMS-bericht maken

>[!IMPORTANT]
>
>**de toestemmingsbeheer van SMS**<br/>
>
>In overeenstemming met de normen en voorschriften van de branche moeten alle SMS-marketingberichten een manier bevatten om de abonnees gemakkelijk af te melden. Om dit te doen, kunnen de ontvangers van SMS met opt-in en opt-out sleutelwoorden antwoorden. Alle standaardtrefwoorden voor aanmelden en weigeren worden ondersteund en gerespecteerd. Daarnaast worden aangepaste trefwoorden die voor uw SMS-serviceprovider zijn geconfigureerd, ondersteund en gerespecteerd.

Voer in het veld **[!UICONTROL Message]** de tekst in die u wilt verzenden.

U kunt een bericht van maximaal 1600 karakters tot stand brengen, met elke 160 karakters die als één enkel SMS-bericht worden beschouwd.

![&#x200B; stel het bericht van SMS samen &#x200B;](./assets/sms-message-compose.png){width="800" zoomable="yes"}

#### Het tekstbericht aanpassen

1. Plaats uw curseur bij de plaats in het bericht waar u het verpersoonlijkingstoken wilt toevoegen.

1. Klik _personaliseren_ pictogram ( ![&#x200B; Persoonlijk pictogram &#x200B;](../assets/do-not-localize/icon-personalize.svg)) rechts van het tekstberichtvakje.

   Het dialoogvenster biedt toegang tot de accounttokens, persoonlijke tokens en systeemtokens. Zowel standaard als aangepaste tokens zijn inbegrepen. U kunt de _bar van het Onderzoek_ gebruiken om van het teken de plaats te bepalen u wenst, of door de omslagboom te navigeren om het even welke tokens te vinden en te selecteren.

1. Voeg een token toe door op de plusknop ( **+** ) naast de token te klikken.

   Als u het teken met een reserve (gebrek wilt toevoegen dat in het geval verschijnt dat het gebied niet beschikbaar voor een lood) is, klik het _Meer_ pictogram ( **..**) en kies **[!UICONTROL Insert with fallback text]**.

   ![&#x200B; klik de ellipsen om een reserve voor het teken &#x200B;](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"} te gebruiken

1. Voer in het dialoogvenster _[!UICONTROL Enter fallback value]_&#x200B;de tekst in die als fallback wordt weergegeven en klik op **[!UICONTROL Add]**.

   ![&#x200B; ga de reservetekst voor het teken &#x200B;](./assets/sms-message-personalize-fallback-text.png){width="400"} in

1. Wanneer uw personalisatietokens worden geplaatst, klik **[!UICONTROL Save]** om veranderingen te bewaren en aan de belangrijkste het auteurswerkruimte van SMS terug te keren.

   U kunt het bericht desgewenst blijven bewerken met de tokens.

#### Koppelingen (URL&#39;s) toevoegen aan het tekstbericht

1. Na het ingaan van uw berichttekst, klik het _pictogram van de Verbinding_ ( ![&#x200B; pictogram van de Verbinding &#x200B;](../assets/do-not-localize/icon-link.svg)) rechts van het tekstberichtvakje.

1. Voer de **[!UICONTROL URL]** in voor de koppeling.
<!--    
1. In the dialog, choose the type of URLs to link:

   * **[!UICONTROL Landing Page]** - Choose this option to select any of the approved Adobe Marketo Engage landing pages from your Marketo Engage instance. Select the workspace, and then select the landing page.

   * **[!UICONTROL External URL]** - This type is any external URL that you enter in the text box. -->

1. Als u een Marketo Engage-landingspagina wilt gebruiken, stelt u de volgende opties in.

   * **[!UICONTROL Enable tracking]** - selecteer dit checkbox om het volgen toe te laten, die _het verkorten_ URL vereist. Voor een landingspagina wordt het Marketo Engage-subdomein gebruikt voor de verkorte URL. Er wordt een voorbeeld van de verkorte URL-indeling weergegeven. De daadwerkelijke URL wordt gecreeerd wanneer SMS wordt verzonden naar de ontvanger.

   * **[!UICONTROL Include mkt_tok]** - Schakel dit selectievakje in om de activiteit van een gebruiker bij te houden.

     >[!NOTE]
     >
     >Wanneer u tekstspatiëring toestaat maar _[!UICONTROL Include mkt_tok]_&#x200B;uitschakelt, bevat de doel-URL na omleiding niet de parameter voor de `mkt_tok` querytekenreeks. Deze parameter wordt gebruikt door Marketo Engage landingspagina&#39;s en Munchkin om ervoor te zorgen dat het volgen van persoonactiviteiten (zoals wanneer een persoon van een e-mail afmeldt). Schakel deze optie alleen uit als de parameter problemen veroorzaakt op uw website.<br/>
     >Voor meer informatie over het gebruiken van het volgen van Munchkin codes op uw website, verwijs naar de [&#x200B; documentatie van Marketo Engage &#x200B;](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website){target="_blank"}.

   ![&#x200B; voeg verbindingsdialoog voor SMS bericht toe &#x200B;](./assets/sms-add-link-dialog.png){width="470"}

1. Wanneer de koppelingsopties zijn voltooid, klikt u op **[!UICONTROL Add]** om de wijzigingen op te slaan en de URL-koppeling toe te voegen aan het SMS-bericht.

### De SMS-eigenschappen instellen

1. Voer in de sectie _[!UICONTROL SMS properties]_&#x200B;een **[!UICONTROL Name]**(vereist, maximaal 100 tekens) en **[!UICONTROL Description]**(optioneel, maximaal 300 tekens) voor uw bericht in.

   Alpha, numerieke, speciale tekens zijn toegestaan voor deze velden. De volgende gereserveerde tekens zijn **niet toegestaan** : `\` , `/` , `:` , `*`, `?` , `"` , `<` , `>` en `|` .

1. Kies de **[!UICONTROL SMS Type]** :

   * Gebruik `Marketing` voor promotietekstberichten waarvoor toestemming van de gebruiker is vereist.
   * Gebruik `Transactional` voor niet-commerciële berichten, zoals orderbevestiging, wachtwoordherstelmeldingen of leveringsgegevens.

1. Voor **[!UICONTROL SMS configuration]**, kies één van de vooraf bepaalde [&#x200B; configuraties van SMS API &#x200B;](../admin/configure-channels-sms.md#create-new-api-credentials-for-an-sms-service-provider).

   Dit het plaatsen bepaalt welke de gatewaydienstverlener en rekening van SMS wordt gebruikt om het bericht te leveren.

1. Voer de **[!UICONTROL Sender number]** &#x200B; in die u voor uw communicatie wilt gebruiken.

   ![&#x200B; het berichteigenschappen van SMS &#x200B;](./assets/sms-properties.png){width="700" zoomable="yes"}

   Het nummer van de ontvanger wordt altijd toegewezen aan het veld `profile.mobilePhone.number` in Experience Platform.

### Inhoud van tekstberichten simuleren {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Controleren hoe uw inhoud wordt gerenderd"
>abstract="Wanneer uw inhoud is gedefinieerd, kunt u de rendering voorvertonen en controleren voor het kanaal dat u gebruikt."

Wanneer de inhoud van uw bericht is gedefinieerd, kunt u testprofielen gebruiken om de inhoud ervan te simuleren (voor een voorvertoning). Als u persoonlijke inhoud hebt ingevoegd, kunt u met testprofielgegevens controleren hoe deze inhoud in het bericht wordt weergegeven.

>[!IMPORTANT]
>
>Sla uw SMS-bericht op voordat u het tekstbericht gaat simuleren.

1. Klik op **[!UICONTROL Simulate Content]** boven aan de werkruimte voor het schrijven van SMS.

1. Klik op _[!UICONTROL Simulate Content]_&#x200B;op de pagina **[!UICONTROL Add People]**.

1. Gebruik de _Simulate Inhoud_ pagina om de lood te beheren die voor uw testprofiel worden gebruikt.

   In de weergegeven lijst kunt u de leads (maximaal 10 leads tegelijk) zoeken en toevoegen vanuit de Marketo Engage lead-database.

   Om te zoeken, ga het volledige e-mailadres in en het drukken _gaat_ binnen. Het bijbehorende hoofdprofiel wordt weergegeven voor selectie.

   De voorvertoning wordt bijgewerkt naar de aanpassingsvelden voor het geselecteerde profiel.

   Alle toegevoegde leads worden links weergegeven.

   U kunt deze lijst beheren door meer personen toe te voegen en afzonderlijke leads te verwijderen uit de profiellijst (deze worden niet verwijderd uit de database).

1. Inhoud voor een geselecteerde lead simuleren.

   Selecteer een van de links vermelde leads. De SMS-voorvertoning op de pagina wordt bijgewerkt voor de geselecteerde lead.

   U kunt ook een lead selecteren in de kiezer boven de voorvertoningsruimte om de SMS-voorvertoning op de pagina voor de bijbehorende lead bij te werken.

1. Als u de pagina _[!UICONTROL Simulate Content]_&#x200B;wilt afsluiten en wilt terugkeren naar de werkruimte voor het schrijven van SMS, klikt u op **[!UICONTROL Close]**&#x200B;rechtsboven.

## Beheer van SMS-toestemmingen

Het is een wettelijke vereiste om ontvangers de mogelijkheid te bieden zich niet meer te abonneren op het ontvangen van communicatie van een merk en deze keuze te respecteren. Als u deze regels niet naleeft, brengt u juridische risico&#39;s met zich mee voor uw merk. Deze functie helpt u ook vermijden verzendend ongevraagde mededelingen naar uw ontvangers, die hen kunnen veroorzaken om uw berichten als spam te merken en uw reputatie te schaden.

Wanneer u deze optie aanbiedt, kunnen SMS-ontvangers reageren met de trefwoorden opt-in en opt-out. Alle standaard opt-in en opt-out sleutelwoorden worden gesteund en gehonoreerd, en om het even welke douanesleutelwoorden die met de dienstverlener van SMS worden gevormd. Als u geen abonnement hebt, worden de profielen automatisch verwijderd uit het publiek van toekomstige marketingberichten.

Journey Optimizer B2B edition biedt de mogelijkheid om de optie om te weigeren in SMS-berichten te beheren aan de hand van de volgende logica:

* Als een lead ervoor heeft gekozen geen communicatie van u te ontvangen, wordt het bijbehorende profiel standaard uitgesloten van daaropvolgende SMS-leveringen

* Deze leidende toestemming uit verschillende bronnen (zoals AEP of de dienstverlener van SMS) wordt gesynchroniseerd aan Journey Optimizer B2B edition. Momenteel ondersteunt het slechts één enkele toestemmingsstaat per lood op instantieniveau (een lood &quot;Jan Smit&quot; wordt geabonneerd op of afgemeld van alle promotionele SMS in het geval). Momenteel biedt het geen ondersteuning voor dubbele opt-in op merkniveau/toestemming op het niveau van individuele abonnementenlijsten.
