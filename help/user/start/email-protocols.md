---
title: Protocollen voor bijhouden en e-maillevering
description: Leer hoe u protocollen in Marketo Engage configureert voor gebruik door Journey Optimizer B2B edition voor functies voor bijhouden en e-mailkanalen.
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4bbe641305065888a59b3e77357e9b39fa6d402e
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 0%

---

# Protocollen voor bijhouden en e-maillevering

Adobe Journey Optimizer B2B edition gebruikt de functies van het e-mailkanaal en het bijhouden van gebeurtenissen in Marketo Engage. Om ervoor te zorgen dat de e-maillevering zoals verwacht voor organisaties werkt die beperkende firewall of volmachtsservermontages gebruiken, moet een systeembeheerder bepaalde domeinen en IP adreswaaiers aan de lijst van gewenste personen toevoegen.

>[!NOTE]
>
>Als uw organisatie reeds de aangesloten instantie van Marketo Engage gebruikt om hun marketing verrichtingen in werking te stellen, zouden deze protocollen en configuraties reeds op zijn plaats moeten zijn.

Zorg ervoor dat de volgende domeinen (inclusief de asterisk) aan de lijst van gewenste personen worden toegevoegd om alle Marketo Engage-bronnen en websockets in te schakelen:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Voer de volgende stappen uit om ervoor te zorgen dat de e-mail wordt bijgehouden en verzonden:

1. [DNS-records maken voor ](#create-dns-records-for-landing-pages-and-email)
1. [SPF en DKIM instellen](#set-up-spf-and-dkim)
1. [DMARC instellen](#set-up-dmarc)
1. [MX-records instellen voor uw domein](#set-up-mx-records-for-your-domain)
1. [Voeg Uitgaande IP adressen aan lijsten van gewenste personen toe](#outbound-ip-addresses)

## DNS-records maken voor <!-- landing pages and --> e-mail

Door een CNAME-record te verbinden, kunnen marketers webversies van e-mails, bestemmingspagina&#39;s en blogs hosten met consistente branding die het verkeer en de conversies verbetert. Het wordt ten zeerste aanbevolen CNAME&#39;s toe te voegen aan de host van het hoofddomein, zodat Marketo Engage uw marketinggeoriënteerde webelementen kan hosten. Als beheerder, zou u met uw team van de Marketing moeten samenwerken om een verslag van CNAME voor de het volgen verbindingen te plannen en uit te voeren die in de e-mail inbegrepen zijn die door Marketo Engage wordt verzonden.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### CNAME toevoegen voor koppelingen voor het bijhouden van e-mail

Voeg de e-mailNAAM toe, zodat `[YourEmailCNAME]` naar `[MktoTrackingLink]` wijst. Dit is de standaardkoppeling voor bijhouden die Marketo Engage heeft toegewezen, in de notatie:

`[YourEmailCNAME].[YourDomain].com` IN CNAME `[MktoTrackingLink]`

Bijvoorbeeld:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>De `[MktoTrackingLink]` waarde moet het standaard [ brandend domein ](../admin/configure-channels-emails.md#branding-domains) zijn.

### Het SSL-certificaat leveren

De Steun van Adobe van het contact [&#128279;](https://experienceleague.adobe.com/home?lang=nl-NL&support-tab=home#support){target="_blank"} om het proces te beginnen van levering een SSL Certificaat.

Dit proces kan maximaal drie werkdagen duren.

## SPF en DKIM instellen

Uw marketingteam moet de DKIM (Domain Keys Identified Mail)-informatie opgeven die aan uw DNS-resourcerecord moet worden toegevoegd. Volg deze stappen om DKIM en SPF (het Kader van het Beleid van de Afzender) te vormen, en dan uw team van de Marketing op de hoogte te brengen wanneer het wordt bijgewerkt.

1. Aan opstelling SPF, voeg de volgende lijn aan de DNS ingangen toe:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Als u reeds een bestaand SPF- verslag in de DNS ingang hebt, voeg eenvoudig het volgende aan het toe:

   ```
   include: mktomail.com
   ```

   Vervang `CompanyDomain` door het hoofddomein van uw website (zoals `company.com/` ) en `CorpIP` door het IP-adres van uw e-mailserver (zoals `255.255.255.255` ). Als u e-mail van meerdere domeinen via Marketo Engage wilt verzenden, voegt u deze regel voor elk domein (op één regel) toe.

1. Voor DKIM maakt u DNS-resourcerecords voor elk domein.

   Voeg de gastheerverslagen en TXT-waarden voor elk domein toe:

   `[DKIMDomain1]`: Hostrecord is `[HostRecord1]` en de TXT-waarde is `[TXTValue1]` .

   `[DKIMDomain2]`: Hostrecord is `[HostRecord2]` en de TXT-waarde is `[TXTValue2]` .

   Kopieer `HostRecord` en `TXTValue` voor elk domein van DKIM na het volgen van de [ instructies ](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in de documentatie van Marketo Engage. U kunt de domeinen in Journey Optimizer B2B edition (zie [ SPF/DKIM ](../admin/configure-channels-emails.md#spfdkim)) verifiëren.

## DMARC instellen

DMARC (Domain-based Message Authentication, Reporting, and Conformance) is een verificatieprotocol dat wordt gebruikt om organisaties te helpen hun domein te beschermen tegen ongeoorloofd gebruik. Het breidt de bestaande authentificatieprotocollen, zoals SPF en DKIM uit, om ontvankelijke servers over de te nemen acties te informeren als een authentificatiemislukking op hun domein voorkomt. DMARC is optioneel, maar wordt ten zeerste aanbevolen omdat het uw merk en reputatie helpt beschermen. Belangrijke aanbieders, zoals Google en Yahoo, begonnen met het gebruik van DMARC voor bulkafzenders vanaf februari 2024.

DMARC werkt alleen als u ten minste een van de volgende DNS TXT-records hebt:

* Een geldige SPF
* Een geldige DKIM-record voor uw FROM:-domein (aanbevolen voor Marketo Engage en Journey Optimizer B2B edition)

U moet ook een DMARC-specifieke DNS TXT-record hebben voor uw `FROM:` -domein. U kunt desgewenst een e-mailadres definiëren dat aangeeft waar DMARC-rapporten binnen uw organisatie moeten worden geplaatst voor rapportcontrole.

### Voorbeeld DMARC-workflow

>[!TIP]
>
>Het is beste praktijken om DMARC als a _langzame uitlooptraject uit te voeren_. Escaleer uw beleid van DMARC van `p=none`, aan `p=quarantine`, en dan aan `p=reject` aangezien u inzicht in de potentiële invloed krijgt, en plaats uw beleid van DMARC aan ontspannen groepering op SPF en DKIM.

Als je DMARC-rapporten ontvangt, moet je het volgende doen:

1. Gebruik `p=none` en analyseer de feedback en rapporten die u ontvangt. De rapporten vertellen de ontvanger om geen acties tegen berichten uit te voeren die authentificatie ontbreken, en e-mailrapporten naar de afzender te verzenden.

   * Als de wettige berichten authentificatie ontbreken, herzie en los de kwesties met SPF/DKIM op.

   * Bepaal of SPF of DKIM is uitgelijnd en of verificatie voor alle geldige e-mailberichten wordt doorgestuurd.

   * Controleer de rapporten om ervoor te zorgen dat de resultaten zijn wat wordt verwacht gebaseerd op uw SPF/DKIM beleid.

1. Pas het beleid aan `p=quarantine` aan, dat de ontvangende e-mailserver aan quarantainemails vertelt die authentificatie ontbreken (typisch het plaatsen van die berichten in de spamomslag).

   Controleer rapporten om ervoor te zorgen dat de resultaten zijn wat u verwacht.

1. Als u tevreden bent met het gedrag van berichten op `p=quarantine` niveau, kunt u beleid aan (`p=reject`) aanpassen.

   Het afwijzingsbeleid vertelt de ontvanger om het even welke e-mail voor het domein te ontkennen (stuit) dat authentificatie ontbreekt. Als dit beleid is ingeschakeld, heeft alleen e-mail die voor 100% is geverifieerd en die door uw domein is geverifieerd, een kans bij plaatsing in het postvak.

   >[!CAUTION]
   >
   >Gebruik dit beleid met voorzichtigheid en bepaal als het voor uw organisatie aangewezen is.

### DMARC-rapportage

DMARC biedt de mogelijkheid om rapporten te ontvangen over e-mailberichten die niet voldoen aan SPF/DKIM. Er zijn twee verschillende die rapporten door ISP diensten als deel van het authentificatieproces worden geproduceerd. Afzenders kunnen deze rapporten ontvangen via de tags RUA/RUF in hun DMARC-beleid.

* **samengevoegde Rapporten (RUA)**: Bevat geen PII (Persoonlijk Identificeerbare Informatie) die gevoelig GDPR (Algemene Verordening van de Bescherming van Gegevens) zou kunnen zijn.

* **Forensische Rapporten (RUF)** - bevat e-mailadressen die gevoelig GDPR zijn. Voordat u dit rapport implementeert, controleert u het organisatiebeleid voor de verwerking van informatie die compatibel moet zijn met GDPR.

Deze rapporten worden vooral gebruikt om een overzicht te krijgen van e-mails die spoofing proberen te maken. Het zijn zeer technische rapporten en kunnen het best via een extern instrument worden verspreid.

### Voorbeeld DMARC-records

* Standaardrecord: `v=DMARC1; p=none`

* Neem op dat u naar een e-mailadres stuurt om rapporten te ontvangen: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC-tags

De verslagen van DMARC hebben veelvoudige componenten genoemd _markeringen van DMARC_. Elke tag heeft een waarde die een bepaald aspect van DMARC opgeeft.

| Tagnaam | Gebruiken | Functie | Voorbeeld | Standaardwaarde |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Vereist | Specifies the version. Er is slechts één versie, dus de versie heeft een vaste waarde `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Vereist | Specificeert het beleid van DMARC, dat de ontvanger aan rapport, quarantaine, of verwerpt e-mail leidt die authentificatiecontroles ontbreekt. | `p=none` , `p=quarantine` of `p=reject` | - |
| `fo` | Optioneel | Staat de domeineigenaar toe om rapporteringsopties te specificeren. | `0`: rapport genereren als zowel SPF als DKIM mislukken <br> `1` - Rapport genereren als SPF of DKIM mislukt <br> `d` - Rapport genereren als DKIM mislukt <br> `s` - Rapport genereren als SPF mislukt | `1` (aanbevolen voor DMARC-rapporten) |
| `pct` | Optioneel | Hiermee geeft u het percentage op van de berichten die worden gefilterd. | `pct=20` | `100` |
| `rua` | Optioneel (aanbevolen) | Hiermee geeft u aan waar samengevoegde rapporten worden geleverd. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | Optioneel (aanbevolen) | Hiermee geeft u aan waar forensische rapporten worden geleverd. | `ruf=mailto:authfail@example.com` | - |
| `sp` | Optioneel | Geeft het DMARC-beleid voor subdomeinen van het bovenliggende domein aan. | `sp=reject` | - |
| `adkim` | Optioneel | Specificeert of een strikte (`s`) of ontspannen (`r`) groepering. De verbrekende groepering betekent dat het domein in de handtekening van DKIM wordt gebruikt en een subdomein van het `From:` adres kan zijn. Strikte uitlijning houdt in dat het domein wordt gebruikt in de DKIM-handtekening en exact moet overeenkomen met het domein dat wordt gebruikt in het `From:` -adres. | `adkim=r` | `r` |
| `aspf` | Optioneel | Kan strikt zijn (`s`) of ontspannen (`r`). De ontspannen wijze betekent dat het terugkeer-weg domein een subdomein van het `From:` adres kan zijn. De strikte wijze betekent dat het terugkeer-weg domein een nauwkeurige gelijke met het `From:` adres moet zijn. | `aspf=r` | `r` |

Voor gedetailleerde informatie over DMARC en elk van zijn opties, verwijs naar [ https://dmarc.org/ ](https://dmarc.org/){target="_blank"}.

### DMARC-implementatie voor Marketo Engage

Er zijn twee typen uitlijning voor DMARC:

* **DKIM** (Domain Keys Identified Mail) groepering: Het domein dat in 2&rbrace; kopbal van e-mail &lbrace;met de DKIM-Handtekening wordt gespecificeerd past aan. `From:` De DKIM-handtekening bevat een `d=` -waarde waarbij het domein is opgegeven voor overeenkomst met het `From:` -headerdomein.

  DKIM-uitlijning valideert als de afzender e-mailberichten van het domein mag verzenden en controleert of er geen inhoud is gewijzigd tijdens de e-maildoorvoer. DKIM-uitgelijnde DMARC implementeren:

   * Stel DKIM in voor het MAIL FROM-domein van uw bericht. Gebruik de [ instructies ](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} in de documentatie van Marketo Engage.

   * Configureer DMARC for the DKIM MAIL FROM domain.

  >[!NOTE]
  >
  >DKIM-uitlijning wordt aanbevolen voor Marketo Engage.

* **SPF** (het Kader van het Beleid van de Afzender) groepering: Het domein in de `From:` kopbal moet het domein in terugkeer-Weg aanpassen: kopbal. Als beide DNS domeinen het zelfde zijn, SPF past (richt) aan en geeft een voldoende resultaat. DMARC met SPF-uitlijning implementeren:

   * Opstelling het branded terugkeer-Weg domein.

      * Vorm het aangewezen SPF verslag.
      * Wijzig de MX-record om terug te verwijzen naar de standaard MX voor het datacenter waarvan uw e-mail is verzonden

   * Configureer DMARC voor het branded Return-Path-domein.

  >[!NOTE]
  >
  >Strikte SPF-uitlijning wordt niet ondersteund of aanbevolen voor Marketo Engage.

### Specifieke IP&#39;s en gedeelde pool

Als u post door Marketo Engage over specifieke IP verzendt en geen branded terugkeer-weg (of niet zeker bent als u) hebt uitgevoerd, open een kaartje met [ Steun van Adobe ](https://experienceleague.adobe.com/home?lang=nl-NL&support-tab=home#support){target="_blank"}.

Vertrouwde IPs is een gedeelde pool van IPs die voor lagere volumegebruikers gereserveerd zijn die minder dan 75k per maand verzenden en niet voor specifieke IP kwalificeren. Deze gebruikers moeten ook aan beste praktijkvereisten voldoen.

* Als u post door Marketo Engage verzendt gebruikend een gedeelde pool van IPs, kunt u controleren als u voor Vertrouwde IPs door [ van toepassing zijnde voor Vertrouwde IP die waaierprogramma ](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"} verzendt. Het branded terugkeer-weg is inbegrepen wanneer het verzenden van Marketo Engage Vertrouwde IPs. Als dit programma is goedgekeurd, vraagt u Adobe Support om het retourpad van het merk in te stellen.

* Als u meer dan 100.000 berichten per maand verzendt en via Marketo Engage e-mail wilt verzenden via gedeelde IP&#39;s, neemt u contact op met het Adobe-accountteam (uw accountmanager) om een toegewezen IP aan te schaffen.

## MX-records instellen voor uw domein

Met een MX-record kunt u e-mail ontvangen naar het domein waarvan u e-mail verzendt om reacties en auto-responders te verwerken. Als u van uw collectief domein verzendt, wordt het waarschijnlijk reeds gevormd. Als niet, kunt u het gewoonlijk plaatsen aan kaart aan uw collectieve domein MX verslag.

## Uitgaande IP adressen

Een uitgaande verbinding wordt gemaakt door Marketo Engage met een server op internet namens u. Uw organisatie van IT en sommige partners/verkopers kunnen lijsten van gewenste personen gebruiken om toegang tot servers te beperken. Als zo, moet u hen van uitgaande IP van Marketo Engage adresblokken verstrekken om aan hun lijsten van gewenste personen toe te voegen.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Uitgaande IP adresblokken

De volgende lijsten behandelen alle servers van Marketo Engage die uitgaande vraag maken. Verwijs naar deze lijsten voor het vormen van een IP lijst van gewenste personen, server, firewall, toegangsbeheerlijst, veiligheidsgroep, of derdedienst om uitgaande verbindingen van Marketo Engage te ontvangen.

| IP-blok (CIDR-notatie) | Individueel IP adres |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
