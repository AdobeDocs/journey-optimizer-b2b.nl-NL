---
title: Een e-mail toevoegen aan uw reis
description: Leer e-mailhandelingen toe te voegen, te definiëren en te optimaliseren in Adobe Journey Optimizer B2B. Verbeter uw accountreizen met gerichte e-mailcommunicatie.
feature: Email Authoring, Content
source-git-commit: 6517a953692a56bd31c5b0f2fa5f15f40c6743b5
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Voeg een e-mail aan uw reis toe

Gebruik Adobe Journey Optimizer B2B edition om e-mailberichten naar uw klanten te verzenden via een accountreis. U kunt ervoor kiezen om berichten te maken, aan te passen en voor te vertonen in de ontwerpruimte voor e-mail. U kunt er ook voor kiezen een e-mail te verzenden die al is gedefinieerd in het gekoppelde Marketo Engage-exemplaar.

>[!NOTE]
>
>Als u een e-mail voor het eerst verzendt, zorg ervoor dat het e-mailkanaal van binnen Adobe Marketo Engage wordt gevormd. Meer leren, zie [ Protocollen voor het volgen en e-maillevering ](../start/email-protocols.md).

## Een e-mailactieknooppunt toevoegen tijdens een rit

U kunt opstelling e-mailleveringen in een reis plaatsen wanneer u [ a _[!UICONTROL Take an action]_knoop ](../journeys/action-nodes.md) toevoegt en het volgende doet:

1. Kies **[!UICONTROL People]** voor het doel _[!UICONTROL Action on]_.

1. Kies **[!UICONTROL Send email]** bij _[!UICONTROL Action on people]_.

1. Kies in het tekstvak _[!UICONTROL Email source]_hoe u de e-mail die u wilt verzenden, wilt verzenden.

   ![ neem een actie - verzend een e-mail ](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Kies **[!UICONTROL Create new email]** om het e-mailbericht zelf te maken in Journey Optimizer B2B edition.

     Met deze optie kunt u de e-mailinhoud zelf beheren in Journey Optimizer B2B edition. Klik **[!UICONTROL Create email]** om _te openen creeer nieuwe e-mail_ dialoog. U kunt een nieuw element van de e-mailinhoud <!-- or duplicate an existing email content asset--> tot stand brengen.

     Voer in het dialoogvenster een unieke **[!UICONTROL Name]** voor de e-mail en een **[!UICONTROL Subject line]** in en klik vervolgens op **[!UICONTROL Create]** .

     ![ creeer nieuwe e-maildialoog - nieuwe e-mail ](assets/create-new-email-no-duplicate.png){width="400"}

     In de sectie _[!UICONTROL Email properties]_van de pagina met e-mailinhoud zijn de velden_[!UICONTROL From email]_ en _[!UICONTROL Reply to address]_al geconfigureerd. U kunt waarden invoeren voor de velden_[!UICONTROL From name]_ en _[!UICONTROL Description]_(optioneel).

     Bepaal de e-mail [ montages ](#define-the-email-settings) en klik **[!UICONTROL Edit email content]** om [ de inhoud ](./email-authoring.md) te ontwerpen.

     <!-- +++New email {#new-email}
     When you want to create an email using an empty canvas or an email template, use the _[!UICONTROL New email]_ option. 

     1. In the dialog, choose **[!UICONTROL New email]**.

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - new email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

       In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. Click **[!UICONTROL Edit email]** to define the email [settings](#define-the-email-settings) and design the [content](./email-authoring.md).

     +++

     +++Duplicate existing email {#duplicate-email}
     When you want to create an email using an existing email from the current journey or from another journey, use the Duplicate existing journey option. You can make changes to the duplicated email according to your objective for the journey node.

     1. In the dialog, choose **[!UICONTROL Duplicate existing email]**.

     1. For **[!UICONTROL Existing email to duplicate]**, click the _Select email_ icon and select the email you want to duplicate and use for the journey node.

      You can filter the list of emails by entering a text string in the search field to match the email name.

      ![Select email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

      Select the checkbox for the email that you want to duplicate and click **[!UICONTROL Select]**. 

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - duplciate existing email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

        In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. If needed, click **[!UICONTROL Edit email]** to modify the email [settings](#define-the-email-settings) and [content](./email-authoring.md).

     +++
   —>
   * Kies **[!UICONTROL Select email from Adobe Marketo Engage]** om een van de vooraf geschreven e-mails in Marketo Engage te gebruiken en te verzenden als onderdeel van de reis.

     ![ Uitgezochte Marketo Engage e-mail ](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Met deze optie wordt het knooppunt ingesteld en hoeft de e-mailinhoud tijdens de rit niet verder te worden gedefinieerd.

## De e-mailinstellingen definiëren

Met het **[!UICONTROL Details]** lusje dat in het _Summiere_ paneel op het recht wordt geselecteerd, scrol aan de bodem om de e-mailopties te bekijken en te plaatsen.

![ E-mailmontages ](./assets/email-summary-details-settings.png){width="600" zoomable="yes"}

| Optie | Beschrijving |
| ------ | ----------- |
| [!UICONTROL From name] | De naam van de afzender die in de e-mailkoptekst wordt gebruikt. Ga de naam van de afzender in aangezien u het aan de ontvanger wilt verschijnen. Klik _personaliseren_ pictogram ( ![ Persoonlijk pictogram ](../assets/do-not-localize/icon-personalize.svg)) om een verpersoonlijkingstoken op het gebied te gebruiken. |
| [!UICONTROL From email] | Het adres van de afzender dat in de e-mailkopbal wordt gebruikt. De standaardwaarde wordt bevolkt van de [ montages van de e-mailkanaallevering ](../admin/configure-channels-emails.md#delivery-settings). Klik _personaliseren_ pictogram ( ![ Persoonlijk pictogram ](../assets/do-not-localize/icon-personalize.svg)) om een verpersoonlijkingstoken op het gebied te gebruiken. |
| [!UICONTROL Reply-to address] | Het adres van de afzender dat in de e-mailkopbal wordt gebruikt. De standaardwaarde wordt bevolkt van de [ montages van de e-mailkanaallevering ](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL From Label]). Voer het e-mailadres in dat u wilt invullen als de ontvanger de antwoordfunctie gebruikt (deze kan anders zijn of hetzelfde zijn als het afzenderadres). Klik _personaliseren_ pictogram ( ![ Persoonlijk pictogram ](../assets/do-not-localize/icon-personalize.svg)) om een verpersoonlijkingstoken op het gebied te gebruiken. |
| [!UICONTROL Subject line] | De tekst die in het onderwerpveld voor de e-mail wordt weergegeven. De standaardwaarde wordt gevuld met de tekst die u hebt ingevoerd in het dialoogvenster _[!UICONTROL Create new email]_. U kunt de tekst desgewenst wijzigen. Klik_ personaliseren _pictogram ( ![ personaliseer pictogram ](../assets/do-not-localize/icon-personalize.svg)) om een verpersoonlijkingstoken op het gebied te gebruiken.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Operational email] | Schakel het selectievakje in als u de e-mail als operationeel wilt aanmerken. Operationele e-mails zijn uitgesloten van de lijst met niet-geabonneerde of niet-geabonneerde e-mails en van de communicatielimieten. Selecteer deze optie alleen als de ontvanger het e-mailbericht niet als een ongevraagd commercieel bericht (SPAM) kan beschouwen. |
| [!UICONTROL Include view as web page] | Schakel het selectievakje in om een koppeling op te nemen naar een webpagina die wordt gegenereerd op basis van de inhoud van het e-mailbericht. E-mailberichten hebben meer mogelijkheden dan webpagina&#39;s, zodat het handig is voor JavaScript, uitgebreide CSS en formulieren. De tekst die wordt gebruikt om de verbinding te produceren wordt gevormd in de [ montages van de e-mailkanaallevering ](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL View as web page HTML] en [!UICONTROL View as web page text]). |
| [!UICONTROL Disable open tracking] | Schakel het selectievakje in als u de activiteiten voor het openen van e-mail niet wilt bijhouden. Als de functie is uitgeschakeld, worden het aantal geopende e-mailactiviteiten alleen verhoogd wanneer een unieke persoon het e-mailbericht opent. U kunt het volgen voor de verbindingen van de e-mailinhoud ](./email-authoring.md#content-authoring---link-tracking) beheren wanneer u de inhoud van het e-maillichaam ontwerpt.[ |
| [!UICONTROL Preheader] | Schakel het selectievakje in om een voorheader op te nemen. Een preheader is de korte samenvattingstekst die na de onderwerpregel in sommige e-mailclients wordt weergegeven. Het verstrekt gewoonlijk een korte samenvatting van e-mail, en is typisch één enkele zin. Ga de summiere tekst op het gebied <!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content --> in. |
| [!UICONTROL Fields used as CC addresses] | Selecteer, indien beschikbaar, maximaal 25 velden voor leads of bedrijven die in Marketo Engage zijn ingesteld met het type `Email` . |

## Waarschuwingen controleren

Terwijl u de inhoud van uw e-mailbericht ontwerpt, worden waarschuwingen weergegeven in de interface (rechtsboven op de pagina) wanneer er geen sleutelinstellingen aanwezig zijn. Als deze knop niet wordt weergegeven, zijn er geen problemen gedetecteerd.

![ E-mailalarm ](./assets/email-alerts.png){width="600" zoomable="yes"}

Er kunnen twee soorten waarschuwingen worden gedetecteerd:

* **_Waarschuwingen_** die naar aanbevelingen en beste praktijken, zoals verwijzen:

   * `The opt-out link is not present in the email body`: u kunt het beste een koppeling zonder abonnement toevoegen aan uw e-mailadres.

     >[!NOTE]
     >
     >E-mailberichten in marketingstijl moeten een opt-out-koppeling bevatten, die niet vereist is voor transactieberichten.

   * `Text version of HTML is empty`: vergeet niet een tekstversie van uw e-mailhoofdtekst te definiëren die wordt gebruikt wanneer HTML-inhoud niet kan worden weergegeven.

   * `Empty link is present in email body`: controleer of alle koppelingen in uw e-mail correct zijn.

   * `Email size has exceeded the limit of 100KB`: zorg ervoor dat de grootte van uw e-mail voor optimale levering niet groter is dan 100 kB.

* **_Fouten_** die u verhinderen de reis/de campagne te testen of te activeren zolang zij niet, zoals worden opgelost:

   * `The subject line is missing`: e-mailonderwerpregel is verplicht.

   * `The email version of the message is empty`: deze fout wordt weergegeven wanneer de e-mailinhoud niet is geconfigureerd.
