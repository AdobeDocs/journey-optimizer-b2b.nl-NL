---
title: Assets
description: Meer informatie over middelenbeheer in Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 16b798f18f72eeb63e68a8d32e69164930aa1e22
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 0%

---

# Assets

Assets zijn doorgaans de afbeeldingen die worden gebruikt voor het maken van uw reisinhoud in Adobe Journey Optimizer B2B Edition. U kunt deze afbeeldingen gebruiken in de e-mails, e-mailsjablonen en fragmenten die zijn geschreven in Journey Optimizer B2B Edition via een assetenkiezer of een eenvoudige interface voor slepen en neerzetten in de visuele inhoudeditor.

Adobe Journey Optimizer B2B Edition biedt marketers toegang tot twee typen assets bibliotheken: Adobe Marketo Engage Design Studio en Adobe Experience Manager Assets as a Cloud Service. U kunt alleen de Adobe Marketo Engage Design Studio gebruiken of beide bibliotheken gebruiken die tegelijkertijd zijn geconfigureerd (op basis van de AEM Assets-licentie die u hebt).

## Beheer van bedrijfsmiddelen

Als u een Marketo Engage-account en Adobe Experience Manager als Cloud Servicen hebt ingericht, hebt u toegang tot de opslagruimten voor zowel Marketo Engage DAM als Adobe Experience Manager Assets as a Cloud Service wanneer uw gebruikersaccount de vereiste machtigingen heeft. Deze opslagruimten zijn gescheiden en niet gesynchroniseerd. U kunt afbeeldingen uit een van beide bronnen gebruiken, maar u kunt slechts één afbeelding tegelijk inschakelen in de inhoudseditor. Een beheerder kan de omschakeling van Marketo Engage DAM aan Adobe Experience Manager Assets as a Cloud Service maken. Het item _[!UICONTROL Assets]_in de linkernavigatie geeft de opslagplaats weer die momenteel is ingesteld.

### Adobe Marketo Engage Design Studio

De Adobe Marketo Engage Design Studio Assets-opslagplaats wordt standaard geleverd bij elk Journey Optimizer B2B Edition-abonnement. Dit betekent dat u toegang hebt tot alle afbeeldingselementen die zijn opgeslagen in Adobe Marketo Engage > Design Studio > Afbeeldingen en bestanden. U kunt deze gegevensopslagruimte gebruiken als uw lokale bibliotheek met middelen, zoals functies voor het uploaden, verwijderen en downloaden van middelen. U kunt deze middelen ook gebruiken binnen uw reisinhoud.

Ondersteunde bestandsindelingen: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Maak gebruik van Adobe Experience Manager Assets om marketing- en creatieve workflows samen te brengen. Het is standaard geïntegreerd met Adobe Journey Optimizer B2B Edition, zodat u eenvoudig toegang hebt tot Assets as a Cloud Service om digitale middelen te ontdekken en te gebruiken. Het biedt toegang tot uw Assets-opslagplaats voor elementen die u kunt gebruiken om uw berichten te vullen.

Adobe Experience Manager Assets kan verbinding maken met Adobe Experience Manager Assets as a Cloud Service voor gecentraliseerde werkruimten voor bedrijfsmiddelen, die uw creatieve systeem uitbreiden en digitale middelen verenigen voor beleving. Adobe Experience Manager Assets as a Cloud Service biedt een gebruiksvriendelijke cloudoplossing voor efficiënt beheer van digitale bedrijfsmiddelen en Dynamic Media. Het omvat naadloos geavanceerde eigenschappen, met inbegrip van Kunstmatige Intelligentie en het Leren van de Machine.

Leer meer in de [ documentatie van Adobe Experience Manager as a Cloud Service ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview).

Adobe Experience Manager Assets is rechtstreeks vanuit het **[!UICONTROL Assets]** -item in de linkernavigatie toegankelijk in Adobe Journey Optimizer B2B Edition. U kunt ook elementen en mappen openen tijdens het ontwerpen van e-mailinhoud.

>[!NOTE]
>
>AEM Assets als Cloud Service, en de vergunningen van Dynamic Media zijn vereist voor deze integratie.<br/>
>Afhankelijk van uw contract en configuratie kunt u Adobe Experience Manager Assets as a Cloud Service rechtstreeks vanuit Adobe Journey Optimizer B2B Edition openen via de sectie Assets van het linkermenu. U kunt ook elementen en mappen openen tijdens het ontwerpen van e-mailinhoud.

Op dit moment kunt u alleen afbeeldingen uit Adobe Experience Manager Assets gebruiken in Adobe Journey Optimizer B2B Edition.

## Elementen gebruiken voor het ontwerpen van inhoud

Gebruik elementen bij het ontwerpen van uw e-mails, e-mailsjablonen en visuele fragmenten. De interface van de visuele inhoudeditor biedt toegang tot de afbeeldingen in de gekoppelde opslagruimten voor elementen.

### Een elementbron kiezen

Als u een abonnement op Experience Manager Assets as a Cloud Service hebt samen met de standaard Adobe Marketo Engage Design Studio, kunt u afbeeldingselementen kiezen uit een van beide bronnen. Hiervoor moet u de afbeeldingsbron selecteren op het moment dat u het bestand maakt voor een nieuw e-mailbericht, een e-mailsjabloon of een visueel fragment. U kunt ook de afbeeldingsbron selecteren wanneer u de inhoud bewerkt. De selectie is alleen van toepassing voor bewerking en u kunt de afbeeldingsbron zo nodig wijzigen dat deze toegang heeft tot elementen uit een andere bibliotheek.

_**Creërend een inhoudsmiddel**_ - om een beeldbron te kiezen wanneer u een e-mail, een e-mailmalplaatje, of een fragment creeert, plaats **[!UICONTROL Image source]** in de dialoog wanneer u het creeert.

_**Uitgevend een inhoudsmiddel**_ - om een bron van de beeldactiva in de visuele redacteur te kiezen, gebruik de **[!UICONTROL Select image source]** selecteur bij de bovenkant van het canvas.

### Elementen toevoegen aan uw inhoud

U kunt een afbeeldingselement toevoegen terwijl u de inhoud ontwerpt, afhankelijk van de geselecteerde bron van afbeeldingselementen.

>[!BEGINTABS]

>[!TAB  voeg de beeldactiva van de Studio van het Ontwerp van het Marketo Engage toe ]

U kunt de activa van de Studio van het Ontwerp van het Marketo Engage toevoegen gebruikend één van beide volgende methodes:

* Voeg een structuurelement toe en sleep vervolgens elementen van de linkernavigatie naar het visuele canvas.
* Voeg een structureel element toe, dan belemmering-en-daling het _beeld_ inhoudstype in de structuur. In de eigenschappeninstellingen aan de rechterkant zijn er twee manieren om de afbeelding op te geven:
   * Klik op **[!UICONTROL Browse]** om de elementenkiezer te openen, waar u een afbeelding kunt kiezen in de Adobe Marketo Engage Design Studio-middelenbibliotheek.
   * Klik op **[!UICONTROL Import media]** om een element uit uw lokale systeem te importeren. Het geïmporteerde element wordt opgeslagen in de Assets-hoofdmap van uw Adobe Marketo Engage Design Studio-bibliotheek.

Als u de afbeelding wilt wijzigen, kunt u de bron-URL voor de afbeelding bijwerken in de eigenschappen aan de rechterkant.

>[!TAB  voeg de beelden van Experience Manager Assets toe]

1. Tijdens het ontwerpen van uw e-mailinhoud in de e-mailontwerper sleept u een afbeeldingselement naar het canvas.

   De eigenschappen aan de rechterkant weerspiegelen de selectie van afbeeldingselementen.

1. Klik op **[!UICONTROL Select an asset]** om de Experience Manager Asset-kiezer te openen.

   Hier kunt u zoeken, filteren en toegang krijgen tot uw gewenste inhoudselement om aan uw marketingmiddel toe te voegen. Op deze pagina vindt u meer informatie over het gebruik van de kiezer.

   >[!NOTE]
   >
   >Als er meer dan één opslagplaats is geconfigureerd, kunt u de repository switch gebruiken op de Asset Selector

1. Selecteer het element dat u in de e-mail wilt invoegen.

>[!ENDTABS]
