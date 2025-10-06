---
title: Paden splitsen en samenvoegen
description: U kunt padknooppunten splitsen en samenvoegen om accounts en personen met voorwaardelijke logica te segmenteren, filteren door groepen te kopen en paden opnieuw te combineren in Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 563d6a85-504d-4c70-b075-8a9a9e88bd6b
source-git-commit: 2bd5c21221da6b1e747bb133cd17c38225539ada
workflow-type: tm+mt
source-wordcount: '2271'
ht-degree: 0%

---

# Paden splitsen en samenvoegen

Gebruik padknooppunten splitsen en samenvoegen om personen of accounts te segmenteren volgens de voorwaarden die u definieert. Maak paden voor het publiek of de accountlijst volgens de voorwaarden, definieer elk pad met actie- en gebeurtenisknooppunten voor het segment en combineer vervolgens de paden en vervolg de reis.

![ Video ](../../assets/do-not-localize/icon-video.svg){width="30"} [ bekijk de overzichtsvideo ](#overview-video)

A _Gesplitste wegen_ knoop bepaalt één of meerdere gesegmenteerde wegen die op **_worden gebaseerd of_** rekening of personenfilters. Een splitsing op basis van een personenfilter wordt automatisch gesloten met een knooppunt voor samengevoegde paden, zodat alle personen naar de volgende stap kunnen gaan zonder hun accountcontext te verliezen.

>[!NOTE]
>
>Er worden maximaal 25 paden ondersteund.

## Paden splitsen op accounts

Splitsen op basis van accounts kan zowel handelingen als gebeurtenissen voor account en personen bevatten. Deze paden kunnen verder worden gesplitst.

_**hoe een gespleten weg door rekeningsknoop**_ werkt

* Elk pad dat u toevoegt, bevat een eindknooppunt met de mogelijkheid om knooppunten aan elke rand toe te voegen.
* Splitsen op accountknooppunten kan worden genest (u kunt het pad herhaaldelijk splitsen op accounts).
* Evaluatie van elk pad is van boven naar beneden. Als een account overeenkomt met het eerste en tweede pad, gaat deze alleen door langs het eerste pad.
* Twee of meer paden kunnen worden gecombineerd met een samenvoegknooppunt.
* Het knooppunt ondersteunt de definitie van een _[!UICONTROL Other accounts]_-pad, waar u handelingen of gebeurtenissen kunt toevoegen voor accounts die niet overeenkomen met een van de gedefinieerde segmenten/paden.

![ knoop van de Reis - gespleten wegen door rekening ](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

### Padvoorwaarden account

| Padvoorwaarden | Beschrijving |
| --------------- | ----------- |
| Accountkenmerken | Attributen van het accountprofiel, waaronder: <li>Jaarlijkse ontvangsten <li>Stad <li>Land <li>Werknemersgrootte <li>Marktsegment <li>Naam <li>SIC-code <li>Staat |
| [!UICONTROL Special filters] > [!UICONTROL Account has matched buying group] | De account komt overeen met een of meer inkoopgroepen. Deze kan worden beoordeeld aan de hand van een of meer van de volgende beperkingen voor een overeenkomende koopgroep: <li>Belang van oplossing <li>Fase van kopersgroep <li>Status van kopersgroep <li>Engagement Score <li>Complete score <li> Aantal personen in groepsrol kopen |
| [!UICONTROL Special filters] > [!UICONTROL Has Buying Group] | De account heeft al dan niet leden van kopersgroepen. Het kan ook worden beoordeeld aan de hand van een of meer van de volgende criteria: <li>Belang van oplossing <li>Fase van kopersgroep <li>Status van kopersgroep <li>Engagement Score <li>Complete score |

>[!NOTE]
>
>Het filter _[!UICONTROL Has Buying Group]_wordt gemarkeerd voor toekomstige veroudering. Gebruik voor nieuwe ritten het filter_[!UICONTROL Account has matched buying group]_ , dat alle zelfde beperkingen omvat.

### Een gesplitst pad toevoegen per accountknooppunt

1. Navigeer naar de reiskaart.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Split paths]** .

   ![ voeg reisknoop toe - gespleten wegen ](./assets/add-node-split.png){width="300"}

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL Accounts]** voor de spleet.

1. Als u een voorwaarde wilt definiëren die van toepassing is op _[!UICONTROL Path 1]_, klikt u op **[!UICONTROL Apply condition]**.

   ![ Gesplitste wegknoop - voeg voorwaarde ](./assets/node-split-properties-apply-condition.png){width="500"} toe

1. Voeg in de Conditions-editor een of meer filters toe om het gesplitste pad te definiëren.

   * Filterkenmerken slepen en neerzetten vanuit de linkernavigatie en de overeenkomende definitie voltooien.

   * Pas de condities aan door de **[!UICONTROL Filter logic]** aan de bovenkant toe te passen. U kiest ervoor om alle filters of een filter aan te passen.

     ![ Gesplitste wegknoop - de logica van de voorwaardenrekeningen ](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Klik op **[!UICONTROL Done]**.

1. Als u meer paden wilt toevoegen, klikt u op **[!UICONTROL Add path]** en herhaalt u de vorige stappen om voorwaarden toe te voegen die van toepassing zijn op dit pad.

   U kunt ook elk pad labelen op basis van deze voorwaarden of de standaardlabels gebruiken.

1. Indien nodig wijzigt u de volgorde van de paden op basis van de gewenste prioriteit voor de splitsing.

   Het filtreren van de weg wordt geëvalueerd in top-down orde. Elke account gaat verder langs het eerste pad dat overeenkomt.

   Klik op de pijl-omhoog of -omlaag rechtsboven in elke padkaart om deze hoger of lager in de lijst met paden te plaatsen.

   ![ Gesplitste wegknoop - orde wegen ](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"} opnieuw

1. Schakel de optie **[!UICONTROL Other accounts]** in om het standaardpad te definiëren voor accounts die niet overeenkomen met de gedefinieerde segmenten/paden.

   Wanneer deze optie niet wordt toegelaten, eindigt de reis voor rekeningen die geen bepaald segment/weg binnen de splitsing aanpassen.

### Groepfiltering voor accounts kopen {#buying-group-filtering-accounts}

U kunt een pad definiëren voor accounts die aan inkoopgroepen zijn gekoppeld en het pad filteren aan de hand van criteria voor inkoopgroepen. Gebruik het filter **[!UICONTROL Account has matched buying group]** om het padsegment te definiëren met behulp van een overeenkomende inkoopgroep. Dit filter omvat ook die optie om rekeningen te identificeren die op het aantal toegewezen rollen binnen een overeenkomende het kopen groep worden gebaseerd.

U wilt bijvoorbeeld de gereedheid van de inkoopgroep evalueren op basis van de diepte (aantal personen) die het opneemt in verschillende rollen, zoals drie besluitvormers en twee beïnvloedende instanties. In dit geval stelt u de voorwaarde in om de rekeningen te richten op ten minste drie (3) Besluitvormers en twee (2) Influencers in een gematchte koopgroep:

1. Klik op **[!UICONTROL Add filter]** en kies het filter **[!UICONTROL Number of people in buying group role]** .

   ![ voeg filter voor Rekening toe heeft het kopen groep aangepast en kies Aantal mensen in het kopen van groepsrol ](./assets/node-split-account-condition-matched-buying-group-number-people-role.png){width="700" zoomable="yes"}

1. Definieer de eerste rolparameter.

   * Stel het aantal personen dat wordt geëvalueerd in op `at least` met de waarde `3` .
   * Stel de rolevaluatie in op `is` en kies `Decision Maker` in de lijst met rollen.

1. Herhaal stap 1 om nog een inkoopgroeprolparameter toe te voegen.

1. Definieer de tweede rolparameter.

   * Stel het aantal personen dat wordt geëvalueerd in op `at least` met de waarde `2` .
   * Stel de rolevaluatie in op `is` en kies `Influencer` in de lijst met rollen.

   ![ Voorwaarden voorbeeld voor roldiepte in het weerspiegelen het kopen groep voor een rekening ](./assets/node-split-account-condition-matched-buying-group-role-depth-example.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Done]** als u alle voorwaarden voor het pad hebt gedefinieerd.

Voor de geïdentificeerde accounts kunt u een actieknooppunt toevoegen aan het pad om de status van de inkoopgroep of het aankoopstadium bij te werken of een e-mail met een verkoopwaarschuwing te verzenden.

## Paden splitsen op personen

Paden splitsen op basis van personen kunnen alleen acties voor personen bevatten. Deze paden kunnen niet opnieuw worden gesplitst en automatisch met elkaar worden verbonden.

_**hoe een gespleten weg door de knoop van mensen**_ werkt

* Splitsen door de functie van personenknopen binnen a _gegroepeerde knoop_ spleet-fusie combinatie. De gesplitste paden worden automatisch samengevoegd, zodat alle mensen naar de volgende stap kunnen gaan zonder hun accountcontext te verliezen.
* Splitsen op basis van knooppunten kan niet worden genest (u kunt geen gesplitst pad toevoegen voor personen op een pad dat zich in dit gegroepeerde knooppunt bevindt).
* Evaluatie van elk pad is van boven naar beneden. Als een persoon overeenkomt met het eerste en tweede pad, gaat hij alleen verder langs het eerste pad.
* De knoop steunt het gebruik van _rekening-persoon verhoudingen_, die u toestaat om mensen te filtreren die op hun rol (zoals contractant of voltijdwerknemer) worden gebaseerd zoals die in de verhouding wordt bepaald.
* Het knooppunt ondersteunt de definitie van een _[!UICONTROL Other people]_-pad, waar u handelingen of gebeurtenissen kunt toevoegen voor personen die niet overeenkomen met een van de gedefinieerde segmenten/paden.

![ knoop van de Reis - gespleten wegen door mensen ](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Padfilters voor personen

| Filters | Beschrijving |
| ------------ | ----------- |
| [!UICONTROL Activity history] > [!UICONTROL Email] | E-mailactiviteiten die zijn gebaseerd op voorwaarden die zijn geëvalueerd aan de hand van een of meer geselecteerde e-mailberichten van eerder in de reis: <li>[!UICONTROL Clicked link in email] <li>E-mail geopend <li>Is per e-mail verzonden <li>Is verzonden via e-mail <br>**[!UICONTROL Switch to inactivity filter]**- Gebruik deze optie om te filteren op basis van een gebrek aan activiteit (een persoon had de e-mailactiviteit niet). |
| [!UICONTROL Activity history] > [!UICONTROL SMS Message] | De activiteiten van SMS die op voorwaarden worden gebaseerd die gebruikend één of meerdere geselecteerde SMS berichten van vroeger in de reis worden geëvalueerd: <li>[!UICONTROL Clicked link in SMS] <li>[!UICONTROL SMS Bounced] <br>**[!UICONTROL Switch to inactivity filter]**- Gebruik deze optie om te filteren op basis van een gebrek aan activiteit (een persoon had de SMS-activiteit niet). |
| [!UICONTROL Activity history] > [!UICONTROL Data Value Changed] | Voor een geselecteerd persoonkenmerk is een waardewijziging opgetreden. Deze wijzigingstypen zijn onder meer: <li>Nieuwe waarde<li>Vorige waarde<li>Reden<li>Bron<li>Datum van activiteit<li>Min. aantal keren <br>**[!UICONTROL Switch to inactivity filter]**- Gebruik deze optie om te filteren op basis van een gebrek aan activiteit (een persoon had geen wijziging in de gegevenswaarde). |
| [!UICONTROL Activity history] > [!UICONTROL Had Interesting Moment] | Interesserende momentactiviteit die in de bijbehorende instantie van Marketo Engage wordt bepaald. Beperkingen zijn: <li>Mijlsteen<li>E-mail<li>Web <br>**[!UICONTROL Switch to inactivity filter]**- Gebruik deze optie om te filteren op basis van een gebrek aan activiteit (een persoon had geen interessant moment). |
| [!UICONTROL Activity history] > [!UICONTROL Visited web page] | Webpaginageactiviteit die voor een of meer webpagina&#39;s wordt beheerd door de bijbehorende Marketo Engage-instantie. Beperkingen zijn: <li>Webpagina (vereist)<li>Datum van activiteit<li>IP-adres client <li>Querystring <li>Referenter <li>Gebruikersagent <li>Zoekmachine <li>Zoekquery <li>Persoonlijke URL <li>Token <li>Browser <li>Platform <li>Apparaat <li>Min. Aantal keren <br>**[!UICONTROL Switch to inactivity filter]**- Gebruik deze optie om te filteren op basis van een gebrek aan activiteit (een persoon heeft de webpagina niet bezocht). |
| [!UICONTROL Person Attributes] | Attributen van het profiel van de persoon, met inbegrip van: <li>Stad <li>Land <li>Geboortedatum <li>E-mailadres <li>E-mail is ongeldig <li>E-mail is geschorst <li>Voornaam <li>Overgenomen deelstaatgebied<li>Functie <li>Achternaam <li>Mobiel telefoonnummer <li>Persoonlijke betrokkenheidsscore <li>Telefoonnummer <li>Postcode <li>Staat <li>Niet geabonneerd <li>Reden waarop geen abonnement is genomen |
| [!UICONTROL Special filters] > [!UICONTROL Member of Buying Group] | De persoon is al dan niet lid van de koopgroep, beoordeeld aan de hand van een of meer van de volgende criteria: <li>Belang van oplossing</li><li>Status van kopersgroep</li><li>Complete score</li><li>Engagement Score</li><li>Functie</li> |
| [!UICONTROL Special filters] > [!UICONTROL Member of List] | De persoon is al dan niet lid van een of meer Marketo Engage-lijsten. |
| [!UICONTROL Special filters] > [!UICONTROL Member of Program] | De persoon is al dan niet lid van een of meer Marketo Engage-programma&#39;s. |

### Padvoorwaarden voor account-personen

| Padvoorwaarden | Beschrijving |
| --------------- | ----------- |
| [!UICONTROL Role in account] | Aan de persoon wordt al dan niet een rol in de account toegewezen. Optionele beperkingen: <li>Rolnaam |

### Een gesplitst pad toevoegen aan een knooppunt met personen

>[!NOTE]
>
>Wanneer u wegen door mensen splitst, wordt de a _Dichte gespleten wegen_ knoop automatisch opgenomen om de splitsing te beëindigen. Een spleet-door-mensen weg staat slechts _toe neemt een actie_ op personenknopen.

1. Navigeer naar de reiskaart.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Split paths]** .

   ![ voeg reisknoop toe - gespleten wegen ](./assets/add-node-split.png){width="300"}

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor de spleet.

1. Stel de **[!UICONTROL Attributes used for conditions]** in.

   * Kies **[!UICONTROL People attributes only]** om voorwaarden te gebruiken die betrekking hebben op het profiel van de persoon.
   * Kies **[!UICONTROL Account-person attributes only]** om voorwaarden te gebruiken die betrekking hebben op het rollidmaatschap van een persoon binnen een account.

1. Als u een voorwaarde wilt definiëren die van toepassing is op _[!UICONTROL Path 1]_, klikt u op **[!UICONTROL Apply condition]**.

1. Voeg in de Conditions-editor een of meer filters toe om het gesplitste pad te definiëren.

   * Sleep een van de personenfilters van de linkernavigatie en vul de overeenkomende definitie in.

     >[!NOTE]
     >
     >Als u aangepaste persoonvelden hebt gedefinieerd in het accountpublieksschema in Experience Platform, zijn deze velden ook beschikbaar voor gebruik als persoonkenmerken in voorwaarden.

   * Pas de condities aan door de **[!UICONTROL Filter logic]** aan de bovenkant toe te passen. U kiest ervoor om alle kenmerkvoorwaarden of een voorwaarde aan te passen.

     ![ Gesplitste wegknoop - de logica van de voorwaardenfilter ](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Klik op **[!UICONTROL Done]**.

1. Als u meer paden wilt toevoegen, klikt u op **[!UICONTROL Add path]** en herhaalt u de vorige stappen om voorwaarden toe te voegen die van toepassing zijn op dit pad.

   U kunt ook elk pad labelen op basis van deze voorwaarden of de standaardlabels gebruiken.

1. Indien nodig wijzigt u de volgorde van de paden op basis van de gewenste prioriteit voor de splitsing.

   Het filtreren van de weg wordt geëvalueerd in top-down orde. Elke persoon gaat langs de eerste weg die aanpast.

   Klik op de pijl-omhoog of -omlaag rechtsboven in elke padkaart om deze hoger of lager in de lijst met paden te plaatsen.

   ![ Gesplitste wegknoop - orde wegen ](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} opnieuw

1. Schakel de optie **[!UICONTROL Other people]** in om een standaardpad toe te voegen voor mensen die niet overeenkomen met de gedefinieerde paden.

   Als deze optie niet is ingeschakeld, worden personen die niet overeenkomen met een gedefinieerd segment/pad, verplaatst na de splitsing en gaan ze verder met de volgende stap in de rit.

   Wanneer u voorwaarden voor elk pad hebt gedefinieerd om uw publiek op personenniveau te splitsen, kunt u acties toevoegen die u aan personen wilt overnemen.

### Activiteitenfiltering

Voor een gesplitst pad naar personen kunt u een pad definiëren op basis van de activiteit van de persoon die betrekking heeft op:

* E-mailberichten van eerdere reizen
* SMS-berichten uit eerdere reizen
* Verandering in gegevenswaarde in het persoonprofiel
* Een interessant moment (bijgehouden in Marketo Engage) dat is gekoppeld aan een e-mail, webpagina of mijlpaal
* Ga naar een webpagina die is bijgehouden in Marketo Engage

>[!BEGINSHADEBOX  &quot;Inactiviteit het filtreren&quot;]

Voor elk van de _[!UICONTROL Activity history]_-filters kunt u de optie **[!UICONTROL Switch to inactivity filter]**inschakelen. Met deze optie wijzigt u het filter in een evaluatie omdat dat type activiteit ontbreekt. Bijvoorbeeld, als u een weg voor mensen wilt tot stand brengen die _****_geen e-mail van vroeger in de reis open, voeg_[!UICONTROL Email]_ > _[!UICONTROL Opened email]_filter toe. Schakel de optie Inactiviteit in en geef de e-mail op. U kunt het beste de_[!UICONTROL Date of activity]_ -beperking gebruiken om een tijdsperiode voor de inactiviteit te definiëren.

![ Gesplitste weg door mensen voorwaarde voor het kopen van groepslidmaatschap ](./assets/node-split-people-condition-inactivity.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

### Deelnemerfiltering

Binnen de sectie _[!UICONTROL Special Filters]_zijn er meerdere filters waarmee u het lidmaatschap van een persoon in een inkoopgroep of Marketo Engage-lijst kunt evalueren. Als u bijvoorbeeld een pad wilt maken voor mensen die lid zijn van een inkoopgroep en een bepaalde rol hebben toegewezen, voegt u het filter_[!UICONTROL Special filters]_ > _[!UICONTROL Member of Buying group]_toe. Voor de filter, plaats het lidmaatschap als_ waar _, selecteer a_[!UICONTROL Solution interest]_ dat met één of meerdere het kopen groepen wordt geassocieerd, en plaats _[!UICONTROL Role]_die u wilt aanpassen.

![ Gesplitste weg door mensen voorwaarde voor het kopen van groepslidmaatschap ](./assets/node-split-people-condition-buying-group-membership.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX  &quot;Marketo Engage list membership&quot;]

In Marketo Engage, _Slimme Campagnes_ controlelidmaatschap van programma&#39;s om ervoor te zorgen dat de leads geen dubbele e-mail ontvangen en niet leden van veelvoudige stromen van e-mails tezelfdertijd zijn. In Journey Optimizer B2B kunt u controleren op Marketo Engage-lidmaatschap als voorwaarde voor uw gesplitste pad door mensen om dubbel werk in reisactiviteiten te voorkomen.

Als u een lidmaatschap van een lijst wilt gebruiken in een gesplitste voorwaarde, vouwt u **[!UICONTROL Special Filters]** uit en sleept u de voorwaarde **[!UICONTROL Member of List]** naar de filterruimte. Voltooi de filterdefinitie om lidmaatschap in één of meerdere lijsten van Marketo Engage te evalueren.

![ Gesplitste weg door personenvoorwaarde voor het lijstlidmaatschap van Marketo Engage ](./assets/node-split-paths-conditions-people-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

## Paden samenvoegen

Voeg de wegen van de a _Fusie_ knoop toe om verschillende gespleten wegen door rekening in uw reis te combineren.

1. Navigeer naar de reiskaart.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Split paths]** .

1. Klik op het gesplitste knooppunt om de eigenschappen ervan aan de rechterkant te openen.

1. Klik op [!UICONTROL Add path] om drie paden te maken.

1. Voeg een combinatie van handelingen en gebeurtenissen toe aan elk pad.

1. Klik op de plusknop ( **+** ) voor een van deze paden en kies **[!UICONTROL Merge]** in de weergegeven opties.

   ![ knoop van de Reis - fusiepaden ](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Selecteer in de eigenschappen van de knooppunt Paden samenvoegen de paden die u wilt samenvoegen.

   ![ knoop van de Reis - fusiepaden ](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Op dit punt worden de paden samengevoegd, zodat de accounts van de geselecteerde paden worden gecombineerd tot één pad dat door de rit kan gaan.

1. Indien nodig, kunt u de samenvoegen van wegen ongedaan maken door terug naar de eigenschappen van de de knooppunten van samenstellingswegen te navigeren en checkbox voor om het even welke wegen te ontruimen die u wilt verwijderen.

## Video over overzicht

>[!VIDEO](https://video.tv.adobe.com/v/3443231/?learn=on)
