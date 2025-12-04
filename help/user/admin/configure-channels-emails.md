---
title: E-mailkanaalconfiguraties
description: Configureer de instellingen voor e-maillevering, communicatielimieten en verificatieprotocollen om de prestaties in Journey Optimizer B2B edition te optimaliseren.
feature: Setup, Channels
role: Admin
exl-id: fb16b5e5-f1a5-4e59-b8c6-56985f03225a
source-git-commit: cbd9117daffc3820196c1d8436af2a568e1140b7
workflow-type: tm+mt
source-wordcount: '1596'
ht-degree: 0%

---

# E-mailkanaalconfiguraties

Adobe Journey Optimizer B2B edition gebruikt de kanaalfuncties en gebeurtenistracering in Marketo Engage. De beheerders zouden moeten ervoor zorgen dat de levering en het volgen configuraties op zijn plaats zijn om kanaallevering voor Marketers toe te laten. Voor informatie over de protocollen nodig voor e-maillevering en het volgen door Marketo Engage, zie [ Protocollen voor het volgen en e-maillevering ](../start/email-protocols.md).

## Afleveringsinstellingen

De standaardinstellingen voor e-mailberichten worden gebruikt wanneer marketers een e-mailbericht maken voor een accountreis. Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de instellingen voor e-maillevering te bekijken. Selecteer onder _[!UICONTROL Email]_in het navigatievenster de optie **[!UICONTROL Delivery Settings]**.

![ heb toegang tot de montages van de e-maillevering ](./assets/config-email-delivery-email-header.png){width="800" zoomable="yes"}

De instellingen zijn alleen-lezen in Journey Optimizer B2B edition. Klik op **[!UICONTROL Edit settings]** rechtsboven in het scherm om toegang te krijgen tot de configuratieopties in het aangesloten Marketo Engage-exemplaar.

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

* **[!UICONTROL View as web page HTML]** - HTML (voor gesteunde e-mailcliënten) die voor _Mening als Web-pagina_ wordt gebruikt, die een verbinding verstrekt om een e-mail in browser te tonen.

* **[!UICONTROL View as web page text]** - de gewone die tekst voor _wordt gebruikt Mening als Web-pagina_, die een verbinding verstrekt om e-mail in browser te tonen.

### [!UICONTROL Branding domains] {#branding-domains}

Klik op de tab **[!UICONTROL Branding domains]** om de brandingdomeinen te bekijken.

![ heb toegang tot de brandende domeinen montages ](./assets/config-email-delivery-branding-domains.png){width="700" zoomable="yes"}

Deze instelling definieert uw primaire domein voor een of meer werkruimten in de verbonden Marketo Engage-instantie. De nieuwe e-mails gebruiken dit domein als gebrek, maar de marketers kunnen [ het op een per-e-mailbasis ](../content/add-email.md#define-the-email-settings) met voeten treden. Voor meer informatie over het bepalen van het standaard brandende domein, verwijs naar de [ documentatie van Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain){target="_blank"}.

>[!NOTE]
>
>Als u meerdere merken op de markt brengt en u wilt dat elk merk een eigen merktraceringskoppeling heeft, kunt u een extra brandingdomein toevoegen. Voor meer informatie over het toevoegen van veelvoudige brandende domeinen, verwijs naar de [ documentatie van Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain){target="_blank"}.

### [!UICONTROL Custom header options] {#custom-header-options}

Als u de aangepaste koptekstopties wilt bekijken, klikt u op de tab **[!UICONTROL Custom header options]** .

![ heb toegang tot de opties van de douanekopbal ](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

Wanneer _[!UICONTROL Strict Transport Security]_is ingeschakeld, garandeert dit dat koppelingen worden weergegeven via HTTPS (alleen voor abonnementen met koppelingen die zijn beveiligd door SSL).

## Communicatielimieten

Communicatie beperkt het aantal e-mails dat een contactpersoon van uw organisatie ontvangt. De limieten die u instelt, worden gedeeld tussen Journey Optimizer B2B edition en de gekoppelde Marketo Engage-instantie. Door deze limieten in te stellen, kan één lead gedurende een bepaalde periode niet meer dan een maximum aantal e-mails ontvangen.

>[!AVAILABILITY]
>
>De communicatie grenzen zijn beschikbaar voor de milieu&#39;s van Journey Optimizer B2B edition die op de [ vereenvoudigde architectuur ](../simplified-architecture.md) worden voorzien. Neem contact op met Adobe Support of open een ondersteuningsticket om het delen van communicatielimieten tussen Journey Optimizer B2B edition en een of meer Marketo Engage-exemplaren mogelijk te maken.

Met een gedefinieerde limiet van vijf e-mails per dag zorgt het systeem ervoor dat één contactpersoon binnen een dag geen zesde e-mail ontvangt door het zesde e-mailbericht te onderdrukken. Met gedeelde communicatielimieten tussen Journey Optimizer B2B edition en Marketo Engage worden de regels voor communicatielimieten op één locatie gedefinieerd. Het zesde e-mailbericht wordt onderdrukt, ongeacht de verzendactie van Journey Optimizer B2B edition of Marketo Engage.

Alle de productierexemplaren van Marketo Engage hebben communicatie grenzen die door gebrek worden bepaald (zie de [ documentatie van Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits){target="_blank"} voor meer informatie). Als u gedeelde communicatielimieten wilt gebruiken, definieert u de regels in Journey Optimizer B2B edition en breidt u de verdeling van deze limieten uit tot de Marketo Munchkin-codes.

>[!IMPORTANT]
>
>Als u de communicatieregel wilt uitbreiden naar de Marketo Munchkin-codes, neemt u contact op met uw Adobe-accountbeheerteam. Deze configuratie maakt doorgaans deel uit van het instapproces.

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de regels voor de communicatielimiet te bekijken of in te stellen. Onder _[!UICONTROL Email]_in het navigatievenster en selecteer **[!UICONTROL Communication limits]**.

![ heb toegang tot de configuratie van communicatielimieten ](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

Standaard is er een algemene regel ingesteld waarmee u meerdere regels kunt definiëren, activeren en deactiveren. Klik de naam van de regelreeks om de lijst van regels te tonen.

### Een regel maken

1. Klik op **[!UICONTROL Create rule]** rechtsboven.

   ![ heb toegang tot de configuratie van communicatielimieten ](./assets/config-email-communication-limits-create-rule-select.png){width="600" zoomable="yes"}

1. Voer de **[!UICONTROL Rule name]** in.

1. Stel de **[!UICONTROL Capping amount]** in.

   Ga de waarde in, of klik _Omhoog_ of _Omlaag_ pijl bij het recht om de waarde te verhogen of te verminderen.

1. Kies de waarde **[!UICONTROL Reset capping frequency]** op basis van de manier waarop u de tijdsperiode voor de limiet wilt definiëren.

   U kunt _[!UICONTROL Hourly]_,_[!UICONTROL Daily]_, _[!UICONTROL Weekly]_of_[!UICONTROL Monthly]_ kiezen.

   ![ heb toegang tot de configuratie van communicatielimieten ](./assets/config-email-communication-limits-create-rule-settings.png){width="600" zoomable="yes"}

1. Stel de waarde van **[!UICONTROL Every]** in op basis van het aantal frequentie-eenheden dat u in de punt wilt opnemen.

   Bijvoorbeeld, als u _Dagelijks_ als frequentie gebruikt en u deze waarde aan `3` plaatst, wordt de periode bepaald als drie dagen.

1. Klik op **[!UICONTROL Create rule]** rechtsboven.

De nieuwe regel is in de _staat van het Ontwerp_ en wordt niet toegepast op de communicatie grenzen tot u verkiest om het te activeren.

### Regels beheren

Zolang een regel in de _staat van het Ontwerp_ is, kunt u de definitie uitgeven of de regel schrappen. Wanneer u de regel wilt toepassen, kunt u deze activeren. Klik het _Meer menu_ (**..***) pictogram naast de naam van de ontwerpregel in de lijst en kies **[!UICONTROL Activate]**.

![ klik het Meer menu voor een regel van de ontwerpCommunicatie grenzen ](./assets/config-email-communication-limits-draft-more-menu.png){width="400" zoomable="yes"}

Klik vervolgens op **[!UICONTROL Activate]** in het bevestigingsdialoogvenster.

Een actieve regel kan niet worden bewerkt of verwijderd, maar alleen worden gedeactiveerd. Voor een actieve regel die u uit de toegepaste communicatie grenzen wilt verwijderen, klik _Deactivate_ ( ![ pictogram Deactivate ](../assets/do-not-localize/icon-deactivate.svg)) naast de actieve regelnaam.

![ klik het Deactivate pictogram voor een actieve regel van communicatielimieten ](./assets/config-email-communication-limits-active-deactivate.png){width="400" zoomable="yes"}

Klik vervolgens op **[!UICONTROL Deactivate]** in het bevestigingsdialoogvenster.

De regel wordt getoond met een _Inactieve_ status. Het is gelijkaardig aan een ontwerp regel, en u kunt het uitgeven, schrappen of activeren wanneer nodig.

## SPF/DKIM

Verbeter uw tarieven van de e-maillevering door SPF (het Kader van het Beleid van de Afzender) en DKIM (Domain Keys Identified Mail) in uw DNS montages op te nemen. Deze technologieën verzekeren uw ontvangers dat uw e-mails geen spam zijn. Als u wilt voorkomen dat spamfilters van ontvangers e-mailberichten afwijzen, zorgt u ervoor dat SPF en DKIM zijn ingesteld voor uw domeinen.

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de huidige instellingen te bekijken. Selecteer onder _[!UICONTROL Email]_in het navigatievenster de optie **[!UICONTROL SPF/DKIM]**.

![ heb toegang tot SPF/de configuratie van DKIM ](./assets/config-email-spf-dkim.png){width="700" zoomable="yes"}

De instellingen zijn alleen-lezen in Journey Optimizer B2B edition. Klik op **[!UICONTROL Edit settings]** rechtsboven in het scherm om toegang te krijgen tot de configuratieopties in het aangesloten Marketo Engage-exemplaar.

>[!NOTE]
>
>Voor toegang tot en het bewerken van deze instellingen in Adobe Marketo Engage hebt u productbeheerdersmachtigingen nodig.

### SPF-instelling

De netwerkbeheerder zou de volgende lijn aan uw DNS ingangen moeten toevoegen:

`[domain] IN TXT v=spf1 mx ip4:[corpIP] include:mktomail.com ~all`

In deze vermelding vervangt u `[domain]` door het primaire domein van uw website (zoals `company.com` ) en `[corpIP]` door het IP-adres van uw e-mailserver (zoals `255.255.255.255` ). Als u e-mails verzendt vanuit meerdere domeinen via Marketo Engage, voegt u deze gegevens toe voor elk domein op één regel.

Als u reeds een SPF verslag in uw DNS ingang hebt, voeg het volgende aan het toe:

`include:mktomail.com`

### DKIM instellen

DKIM is een verificatieprotocol dat door e-mailontvangers wordt gebruikt om de afzender van het e-mailbericht te valideren. Het verbetert vaak de leverbaarheid van e-mails aan de postbus omdat een ontvanger erop kan vertrouwen dat het bericht geen vervalsing is.

Wanneer u de openbare sleutel in uw DNS verslag en het verzendende domein in de verbonden instantie van Marketo Engage wordt geactiveerd, wordt het ondertekenen van douaneDKIM gebruikt voor uw uitgaande berichten. De aangepaste DKIM-ondertekening omvat een gecodeerde digitale handtekening bij elke e-mail die wordt verzonden. De ontvangers zijn dan in staat om de digitale handtekening te decrypteren door omhoog de _openbare sleutel_ in DNS van uw verzendend domein te kijken. Als de sleutel in de e-mail met de sleutel in het DNS verslag beantwoordt, is de ontvangende postserver waarschijnlijker om e-mail te aanvaarden die door Marketo Engage wordt verzonden.

Voor meer informatie over het vormen van een handtekening van douaneDKIM voor e-maillevering, verwijs naar de [ documentatie van Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}.

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

De instellingen zijn alleen-lezen in Journey Optimizer B2B edition. Klik op **[!UICONTROL Edit settings]** rechtsboven in het scherm om toegang te krijgen tot de configuratieopties in het aangesloten Marketo Engage-exemplaar.

>[!NOTE]
>
>Voor toegang tot en het bewerken van deze instellingen in Adobe Marketo Engage hebt u productbeheerdersmachtigingen nodig.

Voor meer informatie over het vormen van de opties van de beide activiteit, verwijs naar de [ documentatie van Marketo Engage ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type){target="_blank"}.
