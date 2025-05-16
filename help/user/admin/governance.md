---
title: Governance-functies
description: Meer informatie over de governancefuncties die momenteel beschikbaar zijn in Journey Optimizer B2B edition.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Functies voor bestuur

Journey Optimizer B2B edition is een geïntegreerde Adobe Experience Platform-app. Het gebruikt verscheidene hulpmiddelen en de diensten die controle van uw verzamelde ervaringsgegevens in overeenstemming met uw bedrijfspraktijken, wettelijke verplichtingen, en ontwikkelingsprocessen verstrekken. In de volgende secties wordt een overzicht gegeven van elk van deze bestuurskenmerken.

## Privacy - GDPR

Journey Optimizer B2B edition gebruikt de bestaande Marketo Engage GDPR-governancefuncties die door Privacy Service en Marketo Privacy Broker Service worden geboden.

## Rolgebaseerde toegangscontrole (RBAC)

Met Journey Optimizer B2B edition en de toegang tot Adobe Admin Console, kunnen de beheerders een gebruikerstoestemmingen op een Type van Entiteit (mening-segmenten, leiden-segmenten, leiden-reizen, etc.) verlenen. Dit vermogen maakt deel uit van het Verenigde Kader van Toestemmingen (UPF) dat alle klanten van Adobe Experience Platform toestaat om rollen en toestemmingen voor hun organisatie te bepalen en te beheren.

## Gegevenscodering

**_Encryptie voor gegevens in rust_** - Alle rekeningen en de gegevens van persoonprofielen die van Adobe Experience Platform in Journey Optimizer B2B edition worden overgebracht worden gecodeerd om de bestaande naleving van Experience Platform te handhaven. Alle entiteiten uit Journey Optimizer B2B edition, zoals reizen en inkoopgroepen, worden ook gecodeerd.

**_Encryptie voor gegevens in doorvoer_** (over een openbaar netwerk) - Alle Journey Optimizer B2B edition APIs en de entiteiten worden gecodeerd in doorvoer gebruikend TLS 1.2.

## Aanvaardbare opt-in/opt-out

De opt-in/opt-out van de toestemming is een vorm van bestuur waar een profiel van een communicatiekanaal, zoals e-mail of SMS, kan opteren en een profiel wordt dan uitgesloten van het communicatiekanaal.

Met Journey Optimizer B2B edition kunt u abonnements- en niet-geabonneerde gebruiksgevallen voor het gebruik van e-mail- en SMS-berichten maken en beheren. Deze toestemmingsvoorkeur wordt opgeslagen binnen de Groep van het Gebied van de Toestemming van het Profiel XDM, en wordt gesynchroniseerd in en uit Journey Optimizer B2B edition als deel van het Kader van de Synchronisatie van Gegevens. Deze voorkeuren worden tijdens de levering gebruikt om profielen die zijn uitgeschakeld, uit te sluiten van leveringen.

## Sandbox opnieuw instellen

Het terugstellen van zandbak wordt **momenteel niet gesteund** voor Adobe Journey Optimizer B2B edition. Als u een sandbox die is toegewezen aan Journey Optimizer B2B edition opnieuw instelt of verwijdert, kan dit leiden tot een permanent gegevensverlies in Journey Optimizer B2B edition en kan het nodig zijn een nieuwe Journey Optimizer B2B edition-instantie in te stellen.

## Nog niet beschikbaar

De volgende governancefuncties zijn nog niet beschikbaar:

* Beleid voor gegevensgebruikslabels (DULE) / gebruiksbeleid
* Gegevenshygiëne
* Toestemmingsbeleid
* Toegangsbeheer op veldniveau (FLAC)
* Object-vlakke toegangsbeheer (OLAC)
* CMK-codering voor gegevens in rust
* Platformauditservice
