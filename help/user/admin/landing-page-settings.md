---
title: Configuratie bestemmingspagina
description: Leer hoe u de instellingen van de bestemmingspagina kunt openen en configureren, zodat uw marketingteam webpagina's kan ontwerpen en publiceren ter ondersteuning van hun campagnes.
feature: Setup, Landing Pages, Content
role: Admin
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie"
exl-id: 54b812cb-0129-4253-8e9e-538c25fc4709
source-git-commit: 8bd3d696a52a813b88de9e3b58145b1cbfb3fa32
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Configuratie bestemmingspagina

Beheerders moeten ervoor zorgen dat de instellingen van de bestemmingspagina zijn geconfigureerd voor Marketers die deze pagina&#39;s ontwerpen en publiceren.

## Instellingen

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om de configuratie van de openingspagina te bekijken. Selecteer onder _[!UICONTROL Landing Pages]_in het navigatievenster de optie **[!UICONTROL Settings]**.

![ het Bestaan van pagina montages ](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

### Accounttekenreeks {#account-string}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_account_string"
>title="Reeksen landingspagina&#39;s"
>abstract="De accounttekenreeks identificeert de Adobe Journey Optimizer B2B edition-instantie die de bestemmingspagina&#39;s host."

De accounttekenreeks identificeert de Adobe Journey Optimizer B2B edition-instantie die de bestemmingspagina&#39;s host. Zorg ervoor dat uw team van Systemen de DNS ingang toevoegt en vormt.

### Formulier vooraf invullen {#form-prefill}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_form_prefill"
>title="Voorinstellingen voor vooraf ingevulde formulieren op de startpagina"
>abstract="U kunt de optie voor het vooraf invullen van het formulier inschakelen, zodat formulieren in uw bestemmingspagina&#39;s vooraf ingevulde gegevens kunnen gebruiken voor bekende gebruikers."

Schakel de optie **[!UICONTROL Form prefill]** in als u wilt dat formulieren in uw bestemmingspagina&#39;s vooraf ingevulde gegevens kunnen gebruiken voor bekende gebruikers. Als deze optie is uitgeschakeld, kunnen auteurs van bestemmingspagina geen vooraf ingevulde formuliervelden opnemen.

### DataStream {#datastream}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_datastream"
>title="Gegevensstroomvereiste"
>abstract="DataStream is nodig om pagina-gebeurtenissen te verzamelen van de bestemmingspagina&#39;s op dit domein."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_missing_datastream"
>title="Ontbrekende DataStream-id"
>abstract="Subdomian mist een identiteitskaart DataStream, die voor het juiste verpletteren wordt vereist. Configureer dit in Instellingen om door te gaan"

Stel de optie **[!UICONTROL Datastream]** in om een gegevensstroom voor het starten van een gebeurtenisverzameling op de pagina te configureren.

## Subdomeinen {#add-subdomain}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_add_subdomain"
>title="Subdomein van bestemmingspagina toevoegen"
>abstract="U kunt maximaal 50 subdomeinen toevoegen. Stel een nieuw subdomein in voor elk uniek merk-URL dat u wilt hosten op Adobe Journey Optimizer B2B edition."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_configure_subdomain"
>title="Subdomein van bestemmingspagina configureren"
>abstract="Een geconfigureerd subdomein is vereist om bestemmingspagina&#39;s te publiceren. U kunt een subdomein gebruiken dat al is gedelegeerd aan Adobe of een nieuw subdomein maken."

Een bestemmingspagina subdomain zou moeten helpen om het inhoudstype, de productnaam, of de campagne te identificeren, en de paginaauthenticiteit te versterken. Alvorens u subdomeinen vormt, bepaal één of meerdere CNAMEs voor uw landende pagina&#39;s te gebruiken. Bijvoorbeeld:

* **product**.[ CompanyDomain ].com
* **ga**.[ CompanyDomain ].com
* **signalering**.[ CompanyDomain ].com

In deze voorbeelden is het eerste deel (vet weergegeven) de `LandingPageCNAME` .

Voeg een nieuw subdomein toe voor elk uniek merk-URL dat u wilt hosten op Adobe Journey Optimizer B2B edition. U kunt maximaal 50 subdomeinen toevoegen.

>[!IMPORTANT]
>
>Het delegeren van een ongeldig subdomein naar Adobe is niet toegestaan. Zorg ervoor u geldige subdomain ingaat die uw organisatie, zoals _marketing.yourcompany.com_ bezit.

Ga naar **[!UICONTROL Administration]** > **[!UICONTROL Channels]** als u de subdomeinen wilt bekijken en nieuwe subdomeinen wilt toevoegen. Selecteer onder _[!UICONTROL Landing Pages]_in het navigatievenster de optie **[!UICONTROL Subdomains]**.

![ het Bestaan van pagina subdomeinen ](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

_Een subdomein van een bestemmingspagina toevoegen :_

1. Klik op **[!UICONTROL Add subdomain]** rechtsboven.

1. Voer in de _[!UICONTROL Subdomain details]_de subdomeininformatie in:

   * **[!UICONTROL Subdomain]** - De subdomein-URL die moet worden gebruikt, zoals `marketing.yourcompany.com`
   * **[!UICONTROL Default page]** - De URL voor de standaardsubdomeinpagina, zoals `marketing.yourcompany.com/products`
   * **[!UICONTROL Fallback page]** - De URL voor de fallback-pagina die moet worden gebruikt als een bestemmingspagina op het subdomein niet actief is, zoals `marketing.yourcompany.com/expired`

   ![ voeg het landen pagina subdomain ](./assets/config-landing-pages-add-subdomain.png){width="700" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save]**.
