---
title: E-mailinstelling
description: Configureer Marketo Engage-opties voor de verzending van Journey Optimizer B2B-e-mailberichten, zoals standaardinstellingen, afmelden, webweergave, limieten voor objecten Snelheid, kopteksten bijhouden en beide filteren.
feature: Setup, Channels
role: Admin
exl-id: 5b28d8f2-a3a4-420a-ab03-d1115cf3ab61
source-git-commit: 0a9cff812d0631a34a09cca059ffb8496248c2b4
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 82%

---

# E-mailinstelling

Stel de volgende e-mailopties in om de infrastructuur voor het leveren van e-mail te ondersteunen die door het bijgevoegde Marketo Engage-exemplaar wordt geboden. Een Marketo Engage-productbeheerder kan deze instellingen configureren door naar het gebied **[!UICONTROL Admin]** in de Marketo Engage-instantie te navigeren en **[!UICONTROL Email]** te selecteren.

## E-mailinstellingen

Als u standaardwaarden voor e-mail wilt instellen voor de bijgevoegde Marketo Engage-instantie, wijzigt u de geconfigureerde waarden om het gebruik door uw marketingorganisatie weer te geven.

### Van e-mail en label

Wijzig de waarden voor Van e-mail en label zodat nieuwe e-mails automatisch met deze standaardwaarden worden gevuld.

>[!NOTE]
>
>De wijziging is alleen van toepassing op e-mailberichten die u maakt en niet op andere Marketo Engage- of Journey Optimizer B2B edition-gebruikers.

1. Ga naar het gebied **[!UICONTROL Admin]** in de bijgevoegde Marketo Engage-instantie en selecteer **[!UICONTROL Email]** .

1. Voer in het deelvenster _[!UICONTROL Settings]_&#x200B;de gewenste standaardwaarden in voor **[!UICONTROL From Email]**&#x200B;en **[!UICONTROL From Label]**.

   ![&#x200B; E-mailmontages - van E-mail en van etiket standaardwaarden &#x200B;](./assets/me-admin-email-settings-from.png){width="500"}

1. Klik op **[!UICONTROL Save Changes]** .

### Abonnement opzeggen

Voor niet-operationele marketinge-mails worden onderaan tekst en koppelingen toegevoegd. Als productbeheerder, zou u het gebrek HTML en de tekst moeten vormen die wordt bevolkt wanneer een telleraar e-mail niet als operationeel markeert.

1. Ga naar het gebied **[!UICONTROL Admin]** in de bijgevoegde Marketo Engage-instantie en selecteer **[!UICONTROL Email]** .

1. Voer in het deelvenster _[!UICONTROL Settings]_&#x200B;de gewenste standaardwaarden in voor **[!UICONTROL Unsubscribe HTML]**&#x200B;en **[!UICONTROL Unsubscribe Text]**.

   >[!TIP]
   >
   >Marketers kunnen de positie van de HTML die zich afmeldt in hun e-mail wijzigen met behulp van systeemtokens.

   ![&#x200B; E-mailmontages - Unsubscribe HTML en Unsubscribe de standaardwaarden van de Tekst &#x200B;](./assets/me-admin-email-settings-unsubscribe.png){width="500"}

   >[!CAUTION]
   >
   >De volgende variabelen zijn van essentieel belang. **Verwijder** ze niet.
   >
   >* `%mkt_opt_out_prefix%`
   >* `mkt_unsubscribe=1&mkt_tok=##MKT_TOK##`

1. Klik op **[!UICONTROL Save Changes]** .

Als u ooit de standaardsysteeminhoud moet terugkeren, kopieert en plakt u het volgende:

+++ Standaardtekst voor abonnement op systeem

```
<p><font face="Verdana" size="1">If you no longer wish to receive these emails, click on the following link: <a href="%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##">Unsubscribe</a><br/></font></p>` [!UICONTROL Unsubscribe Text]:
%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##
```

+++

### Weergeven als webpagina

E-mailinhoud heeft beperkte weergavemogelijkheden (beperkte CSS en geen JavaScript of formulieren). De verkopers kunnen de _Mening als Web-pagina_ optie gebruiken om een koekje voor de e-mailontvanger toe te passen gebruikend Marketo Munchkin. Als productbeheerder, zou u het gebrek HTML en de tekst moeten vormen die wordt bevolkt wanneer een teller deze optie kiest.

1. Ga naar het gebied **[!UICONTROL Admin]** in de bijgevoegde Marketo Engage-instantie en selecteer **[!UICONTROL Email]** .

1. Wijzig in het deelvenster _[!UICONTROL Settings]_&#x200B;de inhoud in de velden **[!UICONTROL View as Web Page HTML]**&#x200B;en **[!UICONTROL View as Web Page Text]**&#x200B;om de tint en het bericht weer te geven.

   ![&#x200B; e-mailmontages - Mening als Web-pagina HTML en Mening als de standaardwaarden van de Tekst van de Web-pagina &#x200B;](./assets/me-admin-email-settings-view-as-web-page.png){width="500"}

   >[!CAUTION]
   >
   >De volgende variabelen zijn van essentieel belang. **Verwijder** ze niet.
   >
   >`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
   >
   >Het tweede deel `##MKT_TOK##` is het Munchkin-cookie van die persoon. Hiermee zorgt u ervoor dat cookies correct worden toegepast wanneer de e-mailontvanger op de koppeling klikt.
   >
   >Zorg ervoor dat u:
   >
   >* Extra URL&#39;s toevoegen aan een van de HTML-vakken
   >* HTML in de tekstversie plaatsen

1. Klik op **[!UICONTROL Save Changes]** .

Als u ooit de standaardsysteeminhoud moet terugkeren, kopieert en plakt u het volgende:

+++ Standaardwebpagina van systeem HTML

```
<div style="text-align: center"><font face="Verdana" size="1">To view this email as a web page, <a href="%mkt_webview_url%?mkt_tok=##MKT_TOK##">click here</a></font></div>
```

+++

+++ Standaardwebpaginatekst van systeem

```
To view this email as a web page, go to the following address:
`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
```

+++

## Ophaallimieten voor aangepaste objecten

Als u [!DNL Velocity Script] gebruikt om aangepaste objectgegevens in e-mails weer te geven, past u de ophaallimiet van aangepaste bovenliggende objecten aan. Standaard biedt de limiet toegang tot 10 aangepaste bovenliggende objecten vanuit het snelheidsscript. U kunt deze limiet indien nodig verhogen.

[[!DNL Apache Velocity] &#x200B;](https://velocity.apache.org/) is een taal die op [!DNL Java] wordt voortgebouwd die voor het malplaatjes en scripting van de inhoud van HTML wordt ontworpen. De e-mailinfrastructuur van Marketo Engage ondersteunt het gebruik ervan in e-mailberichten via scripttokens, die toegang bieden tot gegevens die zijn opgeslagen in aangepaste objecten.

U kunt naar bovenliggende en onderliggende aangepaste objecten verwijzen die rechtstreeks met de lead zijn verbonden, of naar contactpersonen, maar niet naar aangepaste objecten op het derde niveau. Voor elk aangepast object zijn de 10 meest recente bijgewerkte records per persoon/contactpersoon beschikbaar bij uitvoering en worden deze geordend van de meest recente update (op `0` ) tot de oudste update (op `9` ).

_De limiet wijzigen :_

1. Ga naar het gebied **[!UICONTROL Admin]** in de bijgevoegde Marketo Engage-instantie en selecteer **[!UICONTROL Email]** .

1. Blader naar het deelvenster _[!UICONTROL Custom Object Retrieval Limits]_&#x200B;en voer een nieuwe waarde in in het dialoogvenster **[!UICONTROL Parent Retrieval Limit]**&#x200B;veld.

   ![&#x200B; Marketo Engage e-mailadmin - het Terugwinnen van Objecten van de Douane de standaardwaarden van Limieten &#x200B;](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   Waarden tussen 10 en 100 worden ondersteund. _[!UICONTROL Child Retrieval Limit]_&#x200B;wordt automatisch geplaatst door 1000 door de oudergrens te verdelen. Als u bijvoorbeeld de bovenliggende limiet instelt op 50, wordt de onderliggende limiet berekend als 20 (1000:50 = 20).

1. Klik op **[!UICONTROL Save Changes]** .

## Aangepaste koptekstopties

Wijzig _[!UICONTROL Custom Header Options]_&#x200B;voor e-mail om koppelingkoppen voor het bijhouden van e-mail te configureren. Schakel deze opties in om veilige koppelingen voor tekstspatiëring te implementeren met behulp van HTTPS via Strikt vervoer.

1. Ga naar het gebied **[!UICONTROL Admin]** in de bijgevoegde Marketo Engage-instantie en selecteer **[!UICONTROL Email]** .

1. Blader naar het deelvenster _[!UICONTROL Custom Header Options]_&#x200B;en wijzig de instelling volgens het beleid voor het bijhouden van koppelingen:

   ![&#x200B; Marketo Engage e-mailadmin - de standaardmontages van de Opties van de Kopbal van de Douane &#x200B;](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   * **[!UICONTROL Strict Transport Security]** - Stel deze optie in op Ingeschakeld om te garanderen dat koppelingen altijd via HTTPS worden verzonden (moet alleen worden ingesteld voor abonnementen met volgkoppelingen die zijn beveiligd door SSL).
   * **[!UICONTROL Max-age]** - Dit veld ondersteunt de verplichte instructie om in seconden de tijd op te geven die de browser moet onthouden om alleen via HTTPS toegang te krijgen tot het domein.
   * **[!UICONTROL IncludeSubDomains]** - Gebruik deze optie om de richtlijn op te nemen die het beleid HSTS op alle subdomeinen van de gastheer toepast.

   >[!IMPORTANT]
   >
   >Controleer deze instellingen met uw IT-team om ervoor te zorgen dat ze zijn afgestemd op het beleid van uw organisatie. Onjuiste instellingen kunnen voorkomen dat sommige bezoekers uw e-mailkoppelingen openen.

1. Klik op **[!UICONTROL Save Changes]** .

## De activiteit van de e-mail filteren {#filter-email-bots}

E-mail beide activiteit, die ook als niet-menselijke interactie (NHI) wordt bedoeld, kan uw e-mail _openen_ en _klikt_ gegevens, die uw betrokkenheidsmetriek vervormen en op gebeurtenis-gebaseerde reisvooruitgang teweegbrengen. Gebruik filtering van e-mailfilters om de integriteit van maatgegevens en inzichten voor betrokkenheid van klikken te behouden. Er zijn twee methoden om vermoedelijke beide activiteiten te identificeren:

* _&#x200B;**[!UICONTROL Match with IAB Bot list]**&#x200B;_- De activiteiten die met om het even wat op de [&#x200B; Interactieve de bot van het Bureau van Advertising &#x200B;](https://www.iab.com/guidelines/iab-abc-international-spiders-bots-list/){target="_blank"} (het adres van de Agent/IP van de Gebruiker) aanpassen zijn duidelijk als bots.
* _&#x200B;**[!UICONTROL Match with Proximity Pattern]**&#x200B;_- Twee of meer activiteiten die tegelijkertijd (in minder dan een seconde) plaatsvinden, worden aangeduid als bots. Kenmerken die in aanmerking worden genomen tijdens de vergelijking zijn:
   * ID lead (moet hetzelfde zijn)
   * E-mailmiddel (moet hetzelfde zijn)
   * Klik op Koppelen of e-mail openen

Voor e-mailkoppelingen klik en e-mail open activiteit, worden de attributen gevuld met de volgende waarden:

* Activiteiten die als bots worden geïdentificeerd - _Bot Activiteit_ = `true` en _het Patroon van de Activiteit van de Bot_ = geïdentificeerd patroon/methode
* Activiteiten die als niet bots worden geïdentificeerd - _Bot Activiteit_ = `false` en _Bot het Patroon van de Activiteit_ = `n/a`

### Filters instellen

1. Ga naar het gebied **[!UICONTROL Admin]** in de bijgevoegde Marketo Engage-instantie en selecteer **[!UICONTROL Email]** .

1. Selecteer de tab **[!UICONTROL Bot Activity]** .

   ![&#x200B; Marketo Engage e-mailadmin - de Bodemactiviteiten tabel &#x200B;](./assets/me-admin-email-bot-activity.png){width="700" zoomable="yes"}

   In het paneel Bodemactiviteitidentificatie worden twee schuifregelaars weergegeven waarmee u beide activiteiten kunt identificeren.

1. Schakel de schuifregelaar in of uit.

   Kies _[!UICONTROL Log Bot Activity]_&#x200B;of&#x200B;_[!UICONTROL Filter Bot Activity]_ voor elke methode die u inschakelt.

   >[!IMPORTANT]
   >
   >Als u [!UICONTROL Filter Bot Activity] kiest, wordt mogelijk een druppel in het e-mailbericht weergegeven en wordt op de knop geklikt omdat er geen onjuiste handelingen meer worden uitgevoerd.

   ![&#x200B; Marketo Engage e-mailadmin - de opties van de Identificatie van de Activiteit van de Bot &#x200B;](./assets/me-admin-email-bot-activity-set-filters.png){width="500"}

   Voor _[!UICONTROL Match with Proximity Pattern]_&#x200B;kunt u ook het aantal seconden instellen voor **[!UICONTROL Duration Between Activities]**(de standaardwaarde is `0` , de maximale waarde is `3` ).

   >[!NOTE]
   >
   >Met _Duur tussen Activiteiten_ die aan `0` seconden wordt geplaatst, identificeert Marketo Engage e-mailactiviteiten die bij die nauwkeurige seconde gebeuren. Als er meerdere e-mailactiviteiten plaatsvinden binnen het opgegeven aantal seconden, wordt dit aangegeven als beide activiteiten.

   Als u een van de filtermethoden wilt uitschakelen, schakelt u de schuifregelaar naar links. Als u dat wel doet, worden de gegevens niet opnieuw ingesteld.

### IP LIJST VAN GEWEZEN PERSONEN

Adobe heeft een lijst met IP-adressen geïdentificeerd die verantwoordelijk zijn voor het genereren van miljoenen nepcontracten, aangezien dergelijke betrokkenheid die wordt ontvangen van een van de volgende IP&#39;s automatisch wordt uitgefilterd en niet wordt toegevoegd aan uw Marketo Engage-instantie. Dit filteren kan resulteren in een vermindering van e-mail opent, klikt, en andere verwante activiteiten. Deze lijst kan periodiek worden bijgewerkt.

+++ Geblokkeerde IP-adressen

* 40.94.34.52
* 40.94.34.86
* 52.34.76.65
* 54.70.53.60
* 54.71.187.124
* 60.28.2.248
* 64.235.150.252
* 64.235.153.10
* 64.235.153.2
* 64.235.154.105
* 64.235.154.109
* 64.235.154.140
* 64.74.215.1
* 64.74.215.100
* 64.74.215.138
* 64.74.215.139
* 64.74.215.142
* 64.74.215.146
* 64.74.215.150
* 64.74.215.154
* 64.74.215.158
* 64.74.215.162
* 64.74.215.164
* 64.74.215.166
* 64.74.215.170
* 64.74.215.174
* 64.74.215.176
* 64.74.215.178
* 64.74.215.51
* 64.74.215.56
* 64.74.215.58
* 64.74.215.59
* 64.74.215.86
* 64.74.215.98
* 65.154.226.101
* 66.249.91.149
* 70.42.131.106
* 74.125.217.116
* 74.217.90.250
* 104.129.41.4
* 104.47.55.126
* 104.47.58.126
* 104.47.70.126
* 104.47.73.126
* 104.47.73.254
* 104.47.74.126
* 128.220.160.1
* 155.70.39.101
* 162.129.251.14
* 162.129.251.42
* 208.52.157.204

>[!NOTE]
>
>Elk IP adres wordt zorgvuldig geanalyseerd en onderzocht alvorens het in deze lijst wordt opgenomen, die ervoor zorgen dat slechts de meest kritieke en schadelijke IPs wordt geblokkeerd.

+++
