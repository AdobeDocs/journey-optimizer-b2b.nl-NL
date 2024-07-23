---
title: Functies voor bestuur
description: Meer informatie over de governancefuncties die momenteel beschikbaar zijn in Journey Optimizer B2B Edition.
source-git-commit: 1353defe804947617a4d7489592d380bf372c7df
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Functies voor bestuur

Als geïntegreerde Adobe Experience Platform-app maakt Journey Optimizer B2B Edition gebruik van verschillende services en tools waarmee u uw verzamelde ervaringsgegevens op een betrouwbare manier kunt beheren om te voldoen aan uw bedrijfspraktijken, wettelijke verplichtingen en ontwikkelingsprocessen. In de volgende secties wordt een overzicht gegeven van elk van deze bestuurskenmerken.

## Privacy - GDPR

Journey Optimizer B2B Edition gebruikt de bestaande GDPR-governancefuncties voor Marketo&#39;s Engage die door de Privacy Service en Marketo Privacy Broker Service worden geboden.

## Rolgebaseerde toegangscontrole (RBAC)

Met Journey Optimizer B2B Edition en toegang tot de Adobe Admin Console kunnen beheerders gebruikersmachtigingen verlenen voor een Type entiteit (weergavesegmenten, segmenten beheren, ritten beheren enzovoort). Dit vermogen maakt deel uit van het Verenigde Kader van Toestemmingen (UPF) dat alle klanten van Adobe Experience Platform toestaat om rollen en toestemmingen voor hun organisatie te bepalen en te beheren.

## Gegevenscodering

**_Encryptie voor gegevens in rust_** - Alle rekeningen en de gegevens van de persoonprofielen die van Adobe Experience Platform in de Uitgave van Journey Optimizer B2B worden overgebracht worden gecodeerd om de bestaande naleving van Experience Platform te handhaven. Alle entiteiten uit Journey Optimizer B2B Edition, zoals reizen en inkoopgroepen, worden ook gecodeerd.

**_Encryptie voor gegevens in doorvoer_** (over een openbaar netwerk) - Alle Uitgave APIs en de entiteiten van de Uitgave van Journey Optimizer B2B worden gecodeerd in doorvoer gebruikend TLS 1.2.

## Aanvaardbare opt-in/opt-out

De opt-in/opt-out voor toestemming is een vorm van bestuur waarbij een profiel kan weigeren van een communicatiekanaal, zoals e-mail of SMS, en een profiel moet dan van een dergelijk communicatiekanaal worden uitgesloten.

Met Journey Optimizer B2B Edition kunt u abonnements- en niet-geabonneerde gebruiksscenario&#39;s voor het gebruik van e-mail- en SMS-berichten maken en beheren. Deze toestemmingsvoorkeur wordt opgeslagen binnen de Groep van het Gebied van de Toestemming van het Profiel XDM, en wordt gesynchroniseerd in en uit de Uitgave van Journey Optimizer B2B als deel van het Kader van de Synchronisatie van Gegevens. Deze voorkeuren worden tijdens de levering gebruikt om profielen die zijn uitgeschakeld, uit te sluiten van leveringen.

## Nog niet beschikbaar

De volgende governancefuncties zijn nog niet beschikbaar, maar zijn opgenomen in de routekaart voor producten:

* Beleid voor gegevensgebruikslabels (DULE) / gebruiksbeleid
* Gegevenshygiëne
* Sandbox opnieuw instellen
* Toestemmingsbeleid
* Toegangsbeheer op veldniveau (FLAC)
* Object-vlakke toegangsbeheer (OLAC)
* CMK-codering voor gegevens in rust
* Platformauditservice
