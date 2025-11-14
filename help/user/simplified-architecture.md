---
title: Vereenvoudigde architectuur instellen
description: Stel Journey Optimizer B2B edition in op de vereenvoudigde architectuur. Configureer XDM-schema's, e-mail-/sms-kanalen, Marketo Engage-reishandelingen en gebruikers.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: bbb9ff0deeb55c4cb132c6c97ec04f53a97339c6
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 1%

---

# Vereenvoudigde architectuur instellen

Adobe Journey Optimizer B2B edition is nu verkrijgbaar met een vereenvoudigde architectuur. Met deze bijgewerkte architectuur werken Journey Optimizer B2B edition en Marketo Engage niet meer op hetzelfde systeem en dezelfde gegevensopslag. Journey Optimizer B2B edition ontvangt alleen gegevens van Adobe Experience Platform. Het blijft echter afhankelijk van Marketo Engage-rechten en bepaalde configuratiefuncties voor de levering en configuratie van het systeem.

De vereenvoudigde architectuur vormt de basis die nieuwe mogelijkheden ontsluit in Adobe Journey Optimizer B2B edition:

* **verenigt en schalen gemakkelijk uw gegevens:** het nieuwe platform steunt complexe gegevensmodellen, met inbegrip van douanevoorwerpen, het kopen groepen, en rekeningsgebeurtenissen. 

* **verbind veelvoudige instanties van Adobe Marketo Engage:** beheer en verenigt gegevens van verscheidene milieu&#39;s van Adobe Marketo Engage op één plaats.

* **houdt uw gegevens veilig:** Geavanceerde privacy en veiligheidseigenschappen die helpen uw klanteninformatie beschermen. (_Binnenkort_)

* **Gebouwd voor de toekomst:** Deze verbetering plaatst u voor aan de gang zijnde verbeteringen en innovatie. 

Voor milieu&#39;s die voor deze architectuur provisioned zijn, gebruik de volgende richtlijnen voor configuratie.

## Naamruimten en schema&#39;s

Zie [&#x200B; B2B namespaces en schema&#39;s &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces) in de documentatie van Experience Platform voor een overzicht.

### Omgevingsinstelling

Stel een Postman-omgeving in ter ondersteuning van het hulpprogramma voor automatisch genereren van B2B-naamruimten en schema.

* U kunt namespace en schema auto-generatie nutsinzameling en milieu van de [&#x200B; bewaarplaats GitHub &#x200B;](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility) downloaden.

* Voor informatie over het gebruiken van Experience Platform APIs, met inbegrip van details voor hoe te om waarden voor vereiste kopballen te verzamelen en steekproefAPI vraag te lezen, zie [&#x200B; begonnen worden met Experience Platform APIs &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/platform-apis/api-guide) gids.

* Voor informatie over hoe te om uw geloofsbrieven voor Experience Platform APIs te produceren, zie het leerprogramma op [&#x200B; voor authentiek verklaren en tot Experience Platform APIs toegang heeft &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/platform-apis/api-authentication).

* Voor informatie over vestiging Postman voor Experience Platform APIs, zie de gedetailleerde stappen in [&#x200B; Postman in Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/platform-apis/postman).

Met een Experience Platform-ontwikkelaarsconsole en Postman-configuratie kunt u nu de juiste omgevingswaarden toepassen op uw Postman-omgeving.

### Scripts uitvoeren

Met uw Postman-verzameling en omgeving kunt u het script uitvoeren via de Postman-interface.

In de interface van Postman, selecteer de wortelomslag van het auto-generatornut en selecteer dan **Looppas** van de hoogste kopbal.

Wanneer de Runner interface wordt getoond, zorg ervoor dat alle checkboxes worden geselecteerd en selecteer dan **Namespaces van de Looppas en het Nut van de Autogeneratie van Schema&#39;s**.

Een succesvol verzoek leidt tot namespaces en schema&#39;s die voor B2B worden vereist.

## XDM-veldselectie

U kunt de XDM-velden beheren die in de hele toepassing beschikbaar zijn in de gebruikersinterface van Journey Optimizer B2B edition. Deze gebieden helpen om uw instantie te stroomlijnen door slechts de gebieden bloot te stellen die voor de bouw van **_reizen_**, **_het kopen groepen_**, of **_e-mailverpersoonlijkingen_** relevant zijn.

### XDM-klassen

#### Standaardklassen

Gebruik de onderstaande stappen om velden te definiëren voor standaard XDM-klassen:

1. Ga naar **[!UICONTROL Administration]>[!UICONTROL Configurations]**.

1. Selecteer **[!UICONTROL XDM Classes]** in het navigatievenster.

1. Selecteer het tabblad **[!UICONTROL Standard]** om de beschikbare XDM-klassen weer te geven:

   * Afzonderlijk XDM-profiel

   * XDM Business Account

#### Beheerde velden

Bepaal welke velden beschikbaar zijn in de hele toepassing.

1. Klik het _Meer menu_ (**..**) pictogram en selecteer **[!UICONTROL Edit managed fields]**.

1. Herzie de lijst van beschikbare gebieden (klik het _pictogram van de Informatie_ voor gebiedsmeta-gegevens).

1. Selecteer de velden die u wilt opnemen en wis selecties voor de velden die u niet nodig hebt.

1. Gebruik de schuifregelaar **[!UICONTROL Only show selected fields]** om de selecties te bekijken.

1. Klik op **[!UICONTROL Save]**.

#### Bijwerkbare velden

Kies welke velden kunnen worden gewijzigd via **[!UICONTROL Update Account Profile]** - of **[!UICONTROL Update Person Profile]** -acties.

1. Klik het _Meer menu_ (**..**) pictogram en selecteer **[!UICONTROL Edit updatable fields]**.

1. Selecteer **[!UICONTROL Schema]** en vervolgens **[!UICONTROL Dataset]** .

   Deze schema&#39;s en datasets worden verstrekt door uw organisatie.

1. Herzie de lijst van updatable gebieden (klik het _pictogram van de Informatie_ voor meta-gegevens).

   Alleen de beheerde velden kunnen worden bewerkt.

1. Selecteer de velden die u beschikbaar wilt maken voor updates tijdens reizen.

1. Klik **sparen**

### Relationele schema&#39;s

Selecteer [&#x200B; relationele schema&#39;s &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/schema/relational) voor gebruik in **_reisbeslissing_** en **_verpersoonlijking_**. Deze schema&#39;s zijn momenteel bedoeld voor gebruik door aangepaste objecten. In de toekomst kunnen relationele schema&#39;s ook worden gebruikt voor andere gevallen van objectgebruik.

1. Selecteer het tabblad **[!UICONTROL Relational]**. 

1. Klik op **[!UICONTROL Select relational XDM class]**.

   Momenteel wordt alleen het aangepaste object Account veel-op-één ondersteund.

1. Herzie de lijst van schemagebieden (klik het _informatie_ pictogram om de meta-gegevens te bekijken).

1. Selecteer de velden die u wilt opnemen.

1. Gebruik de schuifregelaar **[!UICONTROL Only show selected fields]** om de selecties te bekijken.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Merk op dat de relationele schema&#39;s de volgende configuraties moeten hebben:
>
><li>Gedrag: Opnemen
>&gt; <li>Segmentatie: Ingeschakeld
>&gt; <li>Relatietype: veel-op-één
>&gt; <li>Referentieschema: [B2B-account - XDM Business Account-schema](https://experienceleague.adobe.com/nl/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data)
>&gt; <li>Vereiste velden: primaire sleutel, externe sleutel en versiebeschrijving
>&gt; <li>Gekoppelde gegevensset: gedefinieerd en toegewezen aan het schema

### Gebeurtenissen

Selecteer de Gebeurtenissen van de Ervaring in **_reisbeslissing_** te gebruiken.

1. Selecteer het tabblad **[!UICONTROL Events]**. 

1. Klik op **[!UICONTROL Select experience event]**.

1. Klik op **[!UICONTROL Select event type]** , kies het gebeurtenistype en klik op **[!UICONTROL Select]** .

1. Klik op **[!UICONTROL Select fields]**, kies de gewenste velden en klik op **[!UICONTROL Select]** .

1. Klik op **[!UICONTROL Save]**.

## E-mailconfiguratie

Het volgende moet zijn geconfigureerd voor het verzenden van e-mails vanuit Journey Optimizer B2B edition.  

[&#x200B; https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### Protocollen voor bijhouden en e-maillevering

1. [&#x200B; creeer DNS verslagen voor e-mail &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [&#x200B; Opstelling SPF en DKIM &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [&#x200B; Opstelling DMARC &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [&#x200B; de verslagen van de opstelling MX voor uw domein &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. [&#x200B; voeg Uitgaande IP adressen aan lijsten van gewenste personen &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses) toe

1. Als u de specifieke IP pool moet delen, bereik aan het leveringsteam op de haalbaarheid en de gesteunde opstelling.

### E-mailkanaalconfiguraties

In de vereenvoudigde architectuur worden e-mailinstellingen geconfigureerd via de gebruikersinterface van Marketo Engage. Voltooi de e-mail verwante opstellingsstappen: [&#x200B; https://experienceleague.adobe.com/nl/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/nl/docs/marketo/using/getting-started/initial-setup/setup-steps)

[&#x200B; https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### Communicatielimieten

1. Kies in de linkernavigatie **[!UICONTROL Administration]** > **[!UICONTROL Channels]** .

1. Selecteer **[!UICONTROL Communication Limit]** in het navigatievenster.

1. Maak een algemene regelset voor communicatielimieten (deze regelset wordt standaard gemaakt in elke Journey Optimizer B2B edition-instantie).

   Er is geen communicatielimiet als de algemene regelset niet wordt gemaakt.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### Limieten voor gedeelde communicatie

Binnen de nieuwe architectuur hebben Journey Optimizer B2B edition en Marketo Engage standaard onafhankelijke communicatielimieten.

Als u wilt dat de Marketo Engage-instantie de communicatielimiet deelt die in de Journey Optimizer B2B edition-instantie is ingesteld, neemt u contact op met Adobe Support voor hulp bij de configuratie of opent u een ondersteuningsticket. Op verzoek kan het team van de Techniek het delen van communicatie grenzen tussen Journey Optimizer B2B edition en één of meerdere instanties van Marketo Engage toelaten.

Momenteel moet de gedeelde communicatielimiet in de Marketo Engage-instantie worden ingesteld via een API-aanroep.

Bijvoorbeeld wanneer:

* De munchkinId van de Journey Optimizer B2B edition-instantie is `JKL-567-MNO` .
* De munchkinId van de Marketo Engage-instantie is `ABC-123-DEF` en bevindt zich in het SJ-datacenter

De API-aanvraag moet er ongeveer als volgt uitzien:

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```

## SMS-kanaalconfiguratie

Zie {de configuraties van 0} SMS [__ voor gedetailleerde informatie.](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms)

## Acties van Marketo Engage tijdens reizen

U kunt één of meerdere verre **_Marketo Engage_** instanties voor gebruik met de volgende reisacties vormen:

* Toevoegen aan Marketo-lijst
* Verwijderen uit Marketo-lijst
* Toevoegen aan Marketo-aanvraagcampagne

Voer de volgende stappen uit om deze verbindingen te configureren:

1. Ga naar **[!UICONTROL Administration]>[!UICONTROL Configurations]**.

1. Selecteer **[!UICONTROL XDM Classes]** in het navigatievenster.

1. Selecteer het tabblad **[!UICONTROL Integrations]**. 

1. Klik op **[!UICONTROL Create connection]**.

1. Voer de **[!UICONTROL Name]** en **[!UICONTROL Description]** in.

1. Selecteer **[!UICONTROL Update policy]** voor overeenkomende persoonrecords.

1. Voer **[!UICONTROL Munchkin ID]** , **[!UICONTROL Client ID]** , **[!UICONTROL Client Secret]** in en klik op **[!UICONTROL Connect to Marketo]** .

1. Klik op **[!UICONTROL Create]**.

## Gebruiker aan boord

Zie de [&#x200B; pagina van het Beheer van de Gebruiker &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/admin/user-management) voor een overzicht.

### Bestaande gebruikersgroepen

Als alle bestaande Journey Optimizer B2B edition-gebruikers toegang tot de nieuwe architectuur nodig hebben, gebruikt u de bestaande Journey Optimizer B2B edition-gebruikersgroep. Een systeembeheerder of productbeheerder kan de volgende stappen uitvoeren.

1. Maak een productprofiel in de toegewezen Marketo Engage.

1. Voeg een bestaande gebruikersgroep toe aan het gemaakte productprofiel.

De profielen verlenen alle rollen en toestemmingen die reeds aan die gebruikersgroep worden toegewezen, die reeds voor de gebruikers zouden moeten worden gevormd om tot Journey Optimizer B2B edition toegang te hebben. Als alleen een subset gebruikers toegang moet krijgen tot de nieuwe architectuur, voert u de onderstaande stappen uit. Meer details in de [&#x200B; huidige documentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/admin/user-management).

### Een nieuwe gebruikersgroep maken

1. Maak een productprofiel in de toegewezen Marketo Engage-instantie.
1. Maak een gebruikersgroep voor nieuwe gebruikers.
1. Selecteer de vereiste productprofielen en wijs deze toe aan de gebruikersgroep:

   * Marketo Engage-profiel dat u hebt gemaakt
   * Adobe Experience Platform-profielen
      * AEP-Default-All-Users
      * Adobe Experience Platform-gegevensverzameling
      * Alle toegang tot gegevensverzameling

1. Voeg de gebruikers toe aan de gebruikersgroep.
1. Voeg een nieuwe gebruikersgroep toe aan Journey Optimizer B2B edition-rollen in Experience Platform.
