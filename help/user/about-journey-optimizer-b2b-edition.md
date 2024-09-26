---
title: Overzicht van Adobe Journey Optimizer B2B Edition
description: Ontdek de belangrijkste functies, gebruiksscenario's en structurering van de B2B-edititie van Adobe Journey Optimizer.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 1%

---

# Overzicht van Adobe Journey Optimizer B2B Edition

Met Adobe Journey Optimizer B2B Edition kunt u met behulp van geïntegreerde generatieve AI en toonaangevende automatisering accounts accounts organiseren en groepsreizen kopen om de vraag naar specifieke aanbiedingen te maximaliseren met behulp van marketinggekwalificeerde inkoopgroepen.

## Accountreizen met inkoopgroepen

Bij het vergelijken van Adobe Journey Optimizer B2B Edition met de norm Marketo Engage en Adobe Journey Optimizer, is het belangrijkste onderscheid dat rekeningreizen rekeningen door de Reis bewegen, niet mensen. Een persoon die geassocieerd is met een rekening heeft waarschijnlijk een niet-lineaire progressie, gebaseerd op de voortgang van de rekening door de reis, niet gebaseerd op hun individuele acties. Wanneer een account zich bijvoorbeeld in een vroeg stadium van de koopreis bevindt, kan de verzonden informatie over algemene mogelijkheden of functies van de oplossing gaan. Verder tijdens het aankoopproces kan de inhoud zich meer richten op bepaalde aanbiedingen of andere objecten die op het sluiten van een verkoop zijn gericht. Nadat de oplossing is aangeschaft, kan de informatie opnieuw veranderen om hoe te gidsen, beste praktijken, of informatie over aanstaande gebeurtenissen, of met inhoud over extra upsells te verstrekken. Zelfs als een individu niet met de inhoud van de vroege fase heeft gecommuniceerd, wilt u hen nog tot de huidige fase leiden die niet op hun eigen acties wordt gebaseerd, maar op de acties van de andere mensen binnen hun rekening of het kopen groep.

## Architectuur op hoog niveau

De Uitgave van Adobe Journey Optimizer B2B gebruikt _Soorten van de Rekening_ en 2} Soorten publiek van de Mensen van de rekening _van Adobe Experience Platform aan macht een rekeningsreis, die binnen van Marketo Engage in werking wordt gesteld._ Experience Platform is altijd de bron van de waarheid voor deze gegevens, maar alle uitvoering en verwerking van de rekeningreis gebeurt binnen de marketinginfrastructuur van Marketo Engage B2B. Het orchestration brengt gegevens terug naar Experience Platform in bijna echt - tijd door het bestaande Marketo Engage - Adobe Real-Time CDP B2B de bronschakelaar van de Uitgave, die gegevensveranderingen van Marketo Engage aan Experience Platform stroomt.

![ de architectuur van Gegevens op hoog niveau ](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

### Abonnementsmodel

Een Journey Optimizer B2B het abonnement van de Uitgave wordt bepaald door een paar zandbakken van het Experience Platform (AEP) met een Marketo Engage _munchkin_ abonnement. Het is niet mogelijk om één abonnement op een Marketo Engage te koppelen aan meerdere AEP-sandboxen. Als u er niet voor kiest om een bestaand abonnement op een Marketo Engage te gebruiken met Journey Optimizer B2B Edition of als u momenteel geen Marketo Engage gebruikt, krijgt u een nieuw, leeg abonnement op een Marketo Engage voor gebruik met Journey Optimizer B2B Edition.

Het doel van Experience Platform in deze opstelling is een verenigde mening in de gegevens van de instanties van het Marketo Engage (en om het even welke systemen van CRM in bijlage) te verstrekken, en dan op de verenigde gegevens te kunnen actie gebruikend een rekeningsreis.

### Reiskosten voor rekening

Accountreizen worden gemaakt in Journey Optimizer B2B Edition en worden opgeslagen in het exemplaar van het Marketo Engage dat bij het abonnement hoort. Hoewel het in de opslagplaats van de gegevens van het Marketo Engage wordt opgeslagen, is het niet zichtbaar van het Marketo Engage UI, en het is slechts ooit bruikbaar van de Uitgave van Journey Optimizer B2B.

Een accountreis begint altijd met de selectie van een accountsegment dat u wilt gebruiken als het accountpubliek voor de reis. Voor de selectie van de doelgroep wordt de standaardpubliekselectorcomponent van het Experience Platform gebruikt. De verkopers kunnen dan de rekeningreis uitvoeren door de wegen van de reis volgens hun eigen criteria te verdelen, die rekeningscriteria, personencriteria, of het kopen groepscriteria kunnen omvatten. Voor elke tak, kunnen de acties worden genomen om de reis uit te voeren, zoals het verzenden van een e-mail of het wachten op een gebeurtenis om voor te komen.

Nadat de reis van de rekening wordt gecreeerd, moet het worden gepubliceerd. Op publicatietijd, wordt de rekeningsreis bevestigd en in een reeks campagnes van het Marketo Engage omgezet die de reiservaring uitvoeren, en de Diensten van de Integratie van Gegevens worden gecontacteerd om de gegevensstroom te beginnen die, beurtelings, de verrichtingen van de rekeningsreis begint. De eerste stap bestaat uit het maken van de segmenten voor de personen van de account.

### Gegevensstroom

Journey Optimizer B2B Edition gebruikt de Real-Time CDP-accountsegmentatie voor zowel het definiëren als uitvoeren van accountsegmenten en gerelateerde accountpersoonsegmenten die vereist zijn voor reizen. Tijdens een gepubliceerde reis kunnen gegevens over mensen en accounts veranderen. Er worden gegevens verzameld over de mensen die met de reis communiceren. Journey Optimizer B2B Edition vertrouwt op de Marketo Engage bronaansluiting voor Real-Time CDP B2B Edition om gegevenswijzigingen terug te sturen naar de Experience Platform sandbox, de bron van de waarheid.  Deze gegevens worden in real time aan AEP verstrekt.

Alleen de bestaande gegevenstypen die worden ondersteund door de bronaansluiting van het Marketo Engage (accounts, mensen en mogelijkheden) vloeien terug naar Real-Time CDP. Dit betekent dat het kopen van groepsgegevens niet naar AEP stroomt en in plaats daarvan in de instantie van het Marketo Engage verblijft die door het abonnement van de Uitgave van Journey Optimizer B2B wordt gebruikt.
