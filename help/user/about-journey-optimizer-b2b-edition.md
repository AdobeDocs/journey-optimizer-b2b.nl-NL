---
title: Adobe Journey Optimizer B2B edition - Overzicht
description: Ontdek de belangrijkste functies, gebruiksscenario's en structurering van de B2B-edititie van Adobe Journey Optimizer.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Adobe Journey Optimizer B2B edition - overzicht

Met Adobe Journey Optimizer B2B Edition kunt u account- en inkoopgroepentrajecten orkestreren met behulp van ingebouwde generatieve AI en toonaangevende automatisering om de vraag naar specifieke aanbiedingen te maximaliseren met behulp van marketinggekwalificeerde inkoopgroepen.

## Accountreizen met inkoopgroepen

Bij het vergelijken van Adobe Journey Optimizer B2B edition met Marketo Engage en Adobe Journey Optimizer is het belangrijkste onderscheid dat reizen op een rekening door de Reis gaan, niet door mensen. Een persoon die met een account is geassocieerd, heeft doorgaans een niet-lineaire progressie die is gebaseerd op de voortgang van de rekening door de reis, en niet op hun individuele acties. Wanneer een account zich bijvoorbeeld in een vroeg stadium van de koopreis bevindt, kan de verzonden informatie over algemene mogelijkheden of functies van de oplossing gaan. Verder tijdens het aankoopproces kan de inhoud zich meer richten op bepaalde aanbiedingen of andere objecten die op het sluiten van een verkoop zijn gericht. Nadat de oplossing is aangeschaft, kan de informatie opnieuw veranderen om hoe te gidsen, beste praktijken, of informatie over aanstaande gebeurtenissen, of met inhoud over extra upsells te verstrekken. Zelfs als een individu niet met de inhoud van de vroege fase heeft gecommuniceerd, wilt u hen nog tot de huidige fase leiden die niet op hun eigen acties wordt gebaseerd, maar op de acties van de andere mensen binnen hun rekening of het kopen groep.

## Architectuur op hoog niveau

Adobe Journey Optimizer B2B edition gebruikt _Soorten van de Rekening_ en _Soorten publiek van Mensen_ van Adobe Experience Platform aan macht een rekeningsreis, die binnen van Marketo Engage loopt. Experience Platform is altijd de bron van de waarheid voor deze gegevens, maar alle uitvoering en verwerking van de rekeningreis gebeurt binnen de marketinginfrastructuur van Marketo Engage B2B. Het orchestration brengt gegevens terug naar Experience Platform in bijna real time door de bestaande Marketo Engage - Adobe Real-Time CDP B2B edition-bronconnector, die gegevenswijzigingen van Marketo Engage naar Experience Platform stroomt.

![ de architectuur van Gegevens op hoog niveau ](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Controleer uw vergunningsrechten en de overeenkomstige [ productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html) {target="_blank"} over prestatiesbegeleiding en statische beperkingen.

### Abonnementsmodel

Een Journey Optimizer B2B edition abonnement wordt bepaald door een paar zandbakken van Experience Platform (AEP) met een Marketo Engage _Munchkin_ abonnement. Het is niet mogelijk dat één Marketo Engage-abonnement aan meerdere AEP-sandboxen wordt gekoppeld. Als u er niet voor kiest om een bestaand Marketo Engage-abonnement te koppelen aan Journey Optimizer B2B edition, krijgt u een nieuw, leeg Marketo Engage-abonnement voor gebruik met Journey Optimizer B2B edition.

Het doel van Experience Platform in deze opstelling is een verenigde mening in de gegevens van de instanties van Marketo Engage (en om het even welke aangesloten systemen van CRM) te verstrekken, en dan op de verenigde gegevens te kunnen actie ondernemen gebruikend een rekeningsreis.

### Reiskosten voor rekening

Accountreizen worden gemaakt in Journey Optimizer B2B edition en opgeslagen in het Marketo Engage-exemplaar dat bij het abonnement hoort. Hoewel het in de gegevensopslag van Marketo Engage wordt opgeslagen, is het niet zichtbaar van de UI van Marketo Engage, en het is slechts ooit bruikbaar van Journey Optimizer B2B edition.

Een accountreis begint altijd met de selectie van een accountsegment dat u wilt gebruiken als het accountpubliek voor de reis. De selectie van de doelgroep maakt gebruik van de standaard Experience Platform-publieksselectorcomponent. De verkopers kunnen dan de rekeningreis uitvoeren door de wegen van de reis volgens hun eigen criteria te verdelen, die rekeningscriteria, personencriteria, of het kopen groepscriteria kunnen omvatten. Voor elke tak, kunnen de acties worden genomen om de reis uit te voeren, zoals het verzenden van een e-mail of het wachten op een gebeurtenis om voor te komen.

Nadat de reis van de rekening wordt gecreeerd, moet het worden gepubliceerd. Op het moment van publicatie wordt de accountreis gevalideerd en omgezet in een reeks Marketo Engage-campagnes die de reis-ervaring implementeren. De Diensten van de Integratie van gegevens worden gecontacteerd om de gegevensstroom te beginnen die, beurtelings, de verrichtingen van de rekeningsreis begint. De eerste stap bestaat uit het maken van de segmenten voor de personen van de account.

### Gegevensstroom

Journey Optimizer B2B edition gebruikt de Real-Time CDP-accountsegmentatie voor zowel het definiëren als uitvoeren van accountsegmenten en gerelateerde accountpersoonsegmenten die vereist zijn voor reizen. Tijdens een gepubliceerde reis kunnen gegevens over mensen en accounts veranderen. Er worden gegevens verzameld over de mensen die met de reis communiceren. Journey Optimizer B2B edition vertrouwt op de Marketo Engage-bronaansluiting voor Real-Time CDP B2B edition om gegevenswijzigingen terug te sturen naar de Experience Platform-sandbox, de bron van de waarheid.  Deze gegevens worden in real-time aan AEP geleverd.

Alleen de bestaande gegevenstypen die worden ondersteund door de Marketo Engage-bronconnector (accounts, mensen en mogelijkheden) gaan terug naar Real-Time CDP. Dit betekent dat het kopen van groepsgegevens niet naar AEP stroomt en in plaats daarvan in het Marketo Engage-exemplaar verblijft dat door het abonnement van Journey Optimizer B2B edition wordt gebruikt.
