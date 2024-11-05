---
title: E-mailconfiguraties
description: Leer om tot de e-mailmontages toegang te hebben en te herzien die in Marketo Engage worden gevormd.
feature: Setup
source-git-commit: f097f535237fe6b27322e2c325e59daa8a54ee2f
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# E-mailconfiguraties

Adobe Journey Optimizer B2B edition gebruikt de kanaalfuncties en gebeurtenistracering in Market Engage. De beheerders zouden moeten ervoor zorgen dat de levering en het volgen configuraties op zijn plaats zijn om kanaallevering voor Marketers toe te laten.

## Afleveringsinstellingen

De standaardinstellingen voor e-mailberichten worden gebruikt wanneer marketers een e-mailbericht maken voor een accountreis. Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de instellingen voor e-maillevering te bekijken. Selecteer onder _[!UICONTROL Email]_in het navigatievenster de optie **[!UICONTROL Delivery Settings]**.

![ heb toegang tot de montages van de e-maillevering ](./assets/config-email-delivery-email-header.png){width="800" zoomable="yes"}

De instellingen zijn alleen-lezen in Journey Optimizer B2B edition. Klik op **[!UICONTROL Edit settings]** rechtsboven in het scherm om toegang te krijgen tot de configuratieopties in het aangesloten Marketo Engage.

>[!NOTE]
>
>Voor toegang tot en het bewerken van deze instellingen in Adobe Marketo Engage hebt u productbeheerdersmachtigingen nodig.

Selecteer elk van de volgende tabbladen om de huidige instellingen te bekijken.

### [!UICONTROL Email header parameters] {#email-header}

De parameters van de e-mailkopbal bepalen de standaardwaarden voor het volgende:

* **[!UICONTROL From Email]** - het e-mailadres dat in het _van_ gebied in de e-mailkopbal wordt vermeld.

* **[!UICONTROL From Label]** - De weergegeven naam voor het e-mailadres van de afzender.

* **[!UICONTROL Unsubscribe HTML]** - De HTML (voor ondersteunde e-mailclients) die wordt weergegeven in niet-operationele e-mailberichten om uit te leggen waarom acties niet zijn geabonneerd op de ontvanger. Deze tekst en koppelingen worden onderaan toegevoegd.

* **[!UICONTROL Unsubscribe Text]** - De onbewerkte tekst die wordt weergegeven in niet-operationele e-mails om uit te leggen waarom acties niet zijn geabonneerd op de ontvanger. Deze tekst en koppelingen worden onderaan toegevoegd.

* **[!UICONTROL View as web page HTML]** - de HTML (voor gesteunde e-mailcliënten) die voor _Mening als Web-pagina_ wordt gebruikt, die een verbinding verstrekt om e-mail in browser te tonen.

* **[!UICONTROL View as web page text]** - de gewone die tekst voor _wordt gebruikt Mening als Web-pagina_, die een verbinding verstrekt om e-mail in browser te tonen.

### [!UICONTROL Branding domains] {#branding-domains}

Klik op de tab **[!UICONTROL Branding domains]** om de brandingdomeinen te bekijken.

![ heb toegang tot de brandende domeinen montages ](./assets/config-email-delivery-branding-domains.png){width="700" zoomable="yes"}

Deze instelling definieert het primaire domein voor een of meer werkruimten in het Marketo Engage. Nieuwe e-mailberichten gebruiken dit domein als standaard, maar marketeers kunnen dit domein per e-mail overschrijven. Voor meer informatie, verwijs naar de [ documentatie van het Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain) {target="_blank"}.

>[!NOTE]
>
>Als u meerdere merken uit Journey Optimizer B2B edition en het aangesloten Marketo Engage-exemplaar op de markt brengt en u wilt dat elk merk een eigen merktraceringskoppeling heeft, kunt u een extra brandingdomein toevoegen. Voor meer informatie, verwijs naar de [ documentatie van het Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain) {target="_blank"}.


### [!UICONTROL Custom header options] {#custom-header-options}

Als u de aangepaste koptekstopties wilt bekijken, klikt u op de tab **[!UICONTROL Custom header options]** .

![ heb toegang tot de opties van de douanekopbal ](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

Wanneer _[!UICONTROL Strict Transport Security]_is ingeschakeld, garandeert dit dat koppelingen worden weergegeven via HTTPS (alleen voor abonnementen met koppelingen die zijn beveiligd door SSL).

## Communicatielimieten

Communicatielimieten bepalen de hoeveelheid e-mail die uw organisatie verzendt. Het is aan te raden om limieten in te stellen zodat u ontvangers niet te veel e-mails van uw organisatie ontvangt.

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de huidige instellingen te bekijken. Selecteer onder _[!UICONTROL Email]_in het navigatievenster de optie **[!UICONTROL Communication limits]**.

![ heb toegang tot de montages van communicatielimieten ](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

De instellingen zijn alleen-lezen in Journey Optimizer B2B edition. Klik op **[!UICONTROL Edit settings]** rechtsboven in het scherm om toegang te krijgen tot de configuratieopties in het aangesloten Marketo Engage.

>[!NOTE]
>
>Voor toegang tot en het bewerken van deze instellingen in Adobe Marketo Engage hebt u productbeheerdersmachtigingen nodig.

Voor meer informatie over het vormen van de communicatie grenzen, verwijs naar de [ documentatie van het Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits) {target="_blank"}.

## SPF/DKIM

Verbeter uw tarieven van de e-maillevering door SPF (het Kader van het Beleid van de Afzender) en DKIM (de Sleutels van het Domein Identificeerde Post) in uw DNS montages op te nemen. Deze technologieën verzekeren uw ontvangers dat uw e-mails geen spam zijn. Om te helpen voorkomen dat spamfilters van ontvangers e-mailberichten afwijzen, zorgt u ervoor dat SPF en DKIM zijn ingesteld voor uw domeinen.

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de huidige instellingen te bekijken. Selecteer onder _[!UICONTROL Email]_in het navigatievenster de optie **[!UICONTROL SPF/DKIM]**.

![ heb toegang tot SPF/DKIM configuratie ](./assets/config-email-spf-dkim.png){width="700" zoomable="yes"}

De instellingen zijn alleen-lezen in Journey Optimizer B2B edition. Klik op **[!UICONTROL Edit settings]** rechtsboven in het scherm om toegang te krijgen tot de configuratieopties in het aangesloten Marketo Engage.

>[!NOTE]
>
>Voor toegang tot en het bewerken van deze instellingen in Adobe Marketo Engage hebt u productbeheerdersmachtigingen nodig.

### SPF-instelling

De netwerkbeheerder zou de volgende lijn aan uw DNS ingangen moeten toevoegen:

`[domain] IN TXT v=spf1 mx ip4:[corpIP] include:mktomail.com ~all`

In deze vermelding vervangt u `[domain]` door het primaire domein van uw website (zoals `company.com` ) en `[corpIP]` door het IP-adres van uw e-mailserver (zoals `255.255.255.255` ). Als u e-mails van meerdere domeinen via het Marketo Engage verzendt, voegt u deze gegevens voor elk domein op één regel toe.

Als u reeds een SPF verslag in uw DNS ingang hebt, voeg het volgende aan het toe:

`include:mktomail.com`

### DKIM instellen

DKIM is een verificatieprotocol dat door e-mailontvangers wordt gebruikt om de afzender van het e-mailbericht te valideren. Het verbetert vaak de leverbaarheid van e-mails aan de postbus omdat een ontvanger erop kan vertrouwen dat het bericht geen vervalsing is.

Met de openbare sleutel in uw DNS verslag en het verzendende domein dat in de verbonden instantie van het Marketo Engage wordt geactiveerd, wordt het ondertekenen van douane DKIM gebruikt voor uw uitgaande berichten. De aangepaste DKIM-ondertekening omvat een gecodeerde digitale handtekening bij elke e-mail die wordt verzonden. De ontvangers zijn dan in staat om de digitale handtekening te decrypteren door omhoog de _openbare sleutel_ in DNS van uw verzendend domein te kijken. Als de sleutel in e-mail met de sleutel in het DNS verslag beantwoordt, is de ontvangende postserver waarschijnlijker om e-mail goed te keuren die door Marketo Engage wordt verzonden.

Voor meer informatie over het vormen van een handtekening van douane DKIM voor e-maillevering, verwijs naar de [ documentatie van het Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature) {target="_blank"}.

## Bot-activiteit

E-mailbot-activiteit kan ten onrechte uw e-mail opblazen en op gegevens klikken.

Marketo Engage gebruikt twee methoden om beide activiteiten te bevestigen:

* **Gelijke met Interactieve lijst van het Bureau van Advertising (IAB)** - De Activiteiten die om het even wat op IAB UA/IP (het adres van de Agent/IP van de Gebruiker) aanpassen zijn duidelijk als bots.

* **Gelijke met het Patroon van de Nabijheid** - wanneer twee of meer activiteiten tezelfdertijd (binnen een seconde) gebeuren, worden zij geïdentificeerd als bots. Bij deze methode worden de volgende vergelijkingskenmerken in aanmerking genomen:

   * ID lead (moet hetzelfde zijn)
   * E-mailmiddel (moet hetzelfde zijn)
   * Klik op Koppelen of e-mail openen
   * Tijdverschil (zou minder dan één seconde moeten zijn)

Voor e-mailkoppelingen en open activiteiten via e-mail worden nieuwe kenmerken gevuld met de volgende waarden:

* De activiteiten die als bots worden geïdentificeerd hebben _BodemActiviteit_ als `True` en _het Patroon van de Activiteit van de Bot_ als geïdentificeerd patroon/methode.
* De activiteiten die als niet zijn worden geïdentificeerd hebben _Bot Activiteit_ als `False` en _het Patroon van de Activiteit van de Bot_ als `N/A`.
* De activiteiten die gebeuren alvorens de attributen werden geïntroduceerd hebben _Bot Activiteit_ als leeg (ongeldig) en _het Patroon van de Activiteit van de Bot_ als leeg (ongeldig)

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de huidige instellingen te bekijken. Selecteer onder _[!UICONTROL Email]_in het navigatievenster de optie **[!UICONTROL Bot activity]**.

![ heb toegang tot de configuratie van de beide activiteit voor e-maillevering ](./assets/config-email-bot-activity.png){width="700" zoomable="yes"}

De instellingen zijn alleen-lezen in Journey Optimizer B2B edition. Klik op **[!UICONTROL Edit settings]** rechtsboven in het scherm om toegang te krijgen tot de configuratieopties in het aangesloten Marketo Engage.

>[!NOTE]
>
>Voor toegang tot en het bewerken van deze instellingen in Adobe Marketo Engage hebt u productbeheerdersmachtigingen nodig.

Voor meer informatie over het vormen van de opties van de beide activiteit, verwijs naar de [ documentatie van het Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type) {target="_blank"}.

