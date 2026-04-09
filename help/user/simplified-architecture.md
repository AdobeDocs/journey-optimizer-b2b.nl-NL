---
title: Vereenvoudigde architectuur instellen
description: Stel Journey Optimizer B2B edition in op de vereenvoudigde architectuur. Configureer XDM-schema's, e-mail-/sms-kanalen, Marketo Engage-reishandelingen en gebruikers.
feature: Setup, Administration
role: Admin, Developer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
source-git-commit: 8073984ced07e86a3fa500c5bf0bd393abbe0990
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 100%

---

# Vereenvoudigde architectuur instellen

Adobe Journey Optimizer B2B edition is nu verkrijgbaar met een vereenvoudigde architectuur. Met deze architectuur zijn Journey Optimizer B2B edition en Marketo Engage niet meer op hetzelfde systeem en dezelfde gegevensopslag. Journey Optimizer B2B edition ontvangt alleen gegevens van Adobe Experience Platform. De toepassing blijft echter afhankelijk van Marketo Engage-rechten en bepaalde back-endfuncties, zoals e-maillevering, voor de levering en configuratie van het systeem.

De vereenvoudigde architectuur vormt de basis die nieuwe mogelijkheden ontsluit in Journey Optimizer B2B edition:

* **verenigt en schalen gemakkelijk uw gegevens:** het nieuwe platform steunt complexe gegevensmodellen, met inbegrip van douanevoorwerpen, het kopen groepen, en rekeningsgebeurtenissen.

* **verbind veelvoudige instanties van Adobe Marketo Engage:** beheer en verenigt gegevens van verscheidene milieu&#39;s van Marketo Engage op één plaats.

* **houdt uw gegevens veilig:** Geavanceerde privacy en veiligheidseigenschappen die helpen uw klanteninformatie beschermen. (_Binnenkort_)

* **Gebouwd voor de toekomst:** Deze verbetering plaatst u voor aan de gang zijnde verbeteringen en innovatie.

Voor milieu&#39;s die voor deze architectuur provisioned zijn, gebruik de volgende richtlijnen voor configuratie.

Gebruik deze controlelijst om de installatie van Journey Optimizer B2B edition op de vereenvoudigde architectuur te voltooien.

## &#x200B;1. B2B-naamruimten en -schema&#39;s genereren

<table>
<thead>
<tr>
<th colspan="2">Taak</th>
<th>Details en instructies</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Omgeving instellen:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Download het namespace en schema auto-generatienut van GitHub.</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Verzamel Experience Platform API-referenties en vereiste headers.</td>
<td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-guide">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Pas omgevingswaarden toe op uw Postman-omgeving.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">Meer informatie</a></td>
</tr>
<tr>
<td colspan="2"><strong>Voer de scripts uit:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Stel het <em> Namen en van Schema's </em> generatienut in Postman in werking en bevestig namespaces en schema's worden gecreeerd.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">Meer informatie</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. XDM-velden en -gebeurtenissen configureren

<table>
<thead>
<tr>
<th colspan="2">Taak</th>
<th>Details en instructies</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong> Standaardklassen XDM </strong>: De klassen van het Profiel van XDM Individueel en van XDM Bedrijfs van de Rekening opstelling.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Selecteer beheerde velden om beschikbaar te maken voor reizen, inkoopgroepen en personalisatie via e-mail.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Bewerk de velden die u kunt bijwerken voor schema's.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">Meer informatie</a></td>
</tr>
<tr>
<td colspan="2"><strong> Relationele schema's </strong>: Selecteer relationele klasse XDM (het vele-aan-één Voorwerp van de Douane van de Rekening).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Zorg ervoor dat de schema's de vereiste configuratiewaarden hebben.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">Meer informatie</a></td>
</tr>
<tr>
<td colspan="2"><strong> Gebeurtenissen </strong>: Vorm de gebeurtenistypen en de gebieden van Experience Platform.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Configureer elk Experience Platform-gebeurtenistype met velden die worden ondersteund in paden voor het bepalen of splitsen van reizen.</td>
<td><a href="./admin/configure-aep-events.md">Meer informatie</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. Tracking en e-maillevering configureren

Als u e-mailberichten wilt verzenden vanuit [!DNL Journey Optimizer B2B Edition] op de vereenvoudigde architectuur, configureert u de mogelijkheden voor het bijhouden en leveren van e-mailberichten in de bijgevoegde [!DNL Marketo Engage] -productieinstantie en in de [!DNL Journey Optimizer B2B Edition] -app.

<table>
<thead>
<tr>
<th colspan="2">Taak</th>
<th>Details en instructies</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong> Aanvankelijke opstelling </strong> voor de instantie van Marketo Engage in bijlage</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm nieuwe NAAM voor het Volgen van Verbindingen in DNS verslagen</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Brandingdomeinen configureren voor de bijgevoegde Marketo Engage-instantie</td>
<td><a href="./start/branding-domains.md">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>DKIM en SPF configureren naar de bijgevoegde Marketo Engage-instantie</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>DMARC instellen</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>MX-records instellen voor uw domein</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Voeg uitgaande IP adressen aan lijsten van gewenste personen toe</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">Meer informatie</a></td>
</tr>
<tr>
<td colspan="2"><strong> E-mailopstelling </strong> voor de instantie in bijlage Marketo Engage</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm <em> van E-mail </em> en <em> van Etiket </em> (facultatief)</td>
<td><a href="./start/email-setup.md#from-email-and-label">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm <em> Unsubscribe HTML </em> en <em> Unsubscribe Tekst </em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm <em> Mening als Web-pagina HTML </em> en <em> Mening als Tekst van de Web-pagina </em></td>
<td><a href="./start/email-setup.md#view-as-web-page">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm <em> Teruggewonnen Limieten van het Voorwerp van de Douane </em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm <em> Opties van de Kopbal van de Douane </em></td>
<td><a href="./start/email-setup.md#custom-header-options">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm <em> Bot Activiteit </em> het filtreren</td>
<td><a href="./start/email-setup.md#filter-email-bots">Meer informatie</a></td>
</tr>
<tr>
<td colspan="2"><strong> Configuratie van het E-mailkanaal </strong> voor Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm <em> Communicatie Limieten </em> in Journey Optimizer B2B edition</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">Meer informatie</a></td>
</tr>
</tbody>
</table>

<!--
 TBD for later

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. Aanvullende inhoudskanalen configureren

Om marketers voor het opnemen van andere kanalen in hun reizen te steunen, vorm extra kanalen.

<table>
<thead>
<tr>
<th colspan="2">Taak</th>
<th>Details en instructies</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"></strong> kanaalconfiguratie 0} van SMS {voor Journey Optimizer B2B edition.<strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vorm elke rekening van SMS die u wilt steunen.</td>
<td><a href="./admin/configure-channels-sms.md">Meer informatie</a></td>
</tr>
<tr>
<td colspan="2"><strong> het Bestaan pagina's </strong> (Beta) kanaalconfiguratie voor Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Vul de instellingen van de bestemmingspagina in ter ondersteuning van marketers die deze pagina's ontwerpen en publiceren</td>
<td><a href="./admin/landing-page-settings.md">Meer informatie</a></td>
</tr>
<tr>
<td colspan="2"><strong> het kanaalconfiguratie van het Web </strong> (Beta) voor Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Configureer uw bedrijfswebsite ter ondersteuning van de Adobe Experience Platform Web SDK.</td>
<td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Voeg wegeigenschappen toe aan een URL waar de inhoud wordt geleverd.</td>
<td><a href="./admin/configure-channels-web.md">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Geef auteurs van webervaringen de opdracht om de Adobe Experience Cloud Visual Editing Helper-browserextensie te installeren.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">Meer informatie</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Connect Marketo Engage-exemplaar ter ondersteuning van reishandelingen (optioneel)

Als u de Journey Optimizer B2B edition-mogelijkheden wilt aanvullen met campagnes en programma&#39;s in Marketo Engage, stelt u ondersteuning in voor Marketo Engage-acties. Deze actie staat uw marketing teams toe om hun _op rekening-gebaseerde_ marketing in Journey Optimizer B2B edition en _op lood-gebaseerde_ marketing inspanningen in Marketo Engage te coördineren.

<table>
<thead>
<tr>
<th colspan="2">Taak</th>
<th>Details en instructies</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong> voor elke instantie van Marketo Engage </strong> om reisacties te steunen</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>De aangepaste Marketo Engage-service maken</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Voeg de integratie toe aan Journey Optimizer B2B edition</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">Meer informatie</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. Gebruikerstoegang inschakelen

Wanneer de levering volledig is, zijn de zandbakken verbindend, en de aanvankelijke opstellingstaken zijn voltooid, vorm Journey Optimizer B2B edition en de toegang van Marketo Engage voor uw team en gebruikers.

<table>
<thead>
<tr>
<th colspan="2">Taak</th>
<th>Details en instructies</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong> verstrek producttoegang en toestemmingen </strong> voor gebruikers</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Een Marketo Engage-productprofiel maken in de Adobe Admin Console (alleen nieuw Marketo Engage-exemplaar)</td>
<td><a href="./admin/user-management.md#marketo-engage-profile">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Een gebruikersgroep toevoegen voor het profiel</td>
<td><a href="./admin/user-management.md#add-user-group">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>B2B-gebruikersrollen configureren</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">Meer informatie</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Selectievakje"/></td>
<td>Gebruikers of groepen toevoegen aan de rollen</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">Meer informatie</a></td>
</tr>
</tbody>
</table>
