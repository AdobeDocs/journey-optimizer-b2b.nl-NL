---
title: Volledige score voor kopersgroepen
description: Bereken volledigheidsscores voor inkoopgroepen aan de hand van op rol gebaseerde drempels, aanpasbare lidvereisten en volledigheidsinstellingen in Journey Optimizer B2B edition.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 2%

---


# Volledigheidsscores {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="Volledigheidsscore"
>abstract="De volledigheidsscores weerspiegelen hoe goed het het kopen groepslidmaatschap voor een verkoopklaar koopgroep wordt gericht."

Een volledigheidsscore is een percentage dat erop wijst hoe goed een het kopen groep met de vereiste leden over zijn bepaalde rollen bevolkt is. Deze scores zijn gebaseerd op de drempels van het rollid die u in het rolmalplaatje en het daadwerkelijke aantal leden vormt die aan elke rol in de het kopen groep worden toegewezen. De resulterende scores helpen marketers verkoopbereidheid evalueren en hiaten in het kopen van groepssamenstelling identificeren. De berekening van de score wordt automatisch uitgevoerd wanneer het gekochte groepslidmaatschap wordt gewijzigd.

![ het Kopen de scores van de groepsvolledigheid ](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

Er zijn twee typen volledigheidsscores:

* **het Kopen de score van de groepsvolledigheid** - de het kopen groep volledigheidsscore is een percentage tussen 0% tot 100% en vertegenwoordigt de algemene volledigheid van de het kopen groep die op rol-niveau volledigheidsberekeningen wordt gebaseerd.

  De het kopen score van de groepsvolledigheid wordt getoond in de [ Kopen pagina van groepsdetails ](./buying-group-details.md). Deze score geeft een overzicht van de vraag of de inkoopgroep over de vereiste belanghebbenden beschikt voor de verkoopbetrokkenheid.

* **de volledigheidsscore van de Rol** - de score van de rolvolledigheid is een percentage voor elke individuele rol binnen een het kopen groep, die op het aantal leden wordt gebaseerd aan die rol wordt toegewezen.

  De volledigheidsscore van de rol voor elke rol wordt getoond in de het kopen pagina van groepsdetails wanneer u rollen uitgeeft en volledigheidsmontages aanpast. Deze scores helpen u identificeren welke specifieke rollen extra leden vereisen om de verkoop-klaar drempel te bereiken.

  De detailspagina toont de eerste twee rolvolledigheidsscores met een n_+ verbinding voor om het even welke extra rollen. Klik op de koppeling om de aanvullende volledigheidsscores voor de rol weer te geven.

De volledigheidsscores weerspiegelen de huidige staat van het kopen groepslidmaatschap en werken automatisch bij aangezien de leden worden toegevoegd of verwijderd. Weergegeven scores worden weergegeven als hele percentages (een score van 66,67% wordt bijvoorbeeld weergegeven als 67%).

## Gereedheid voor verkoop evalueren

Adobe Journey Optimizer B2B edition voorziet marketers van instrumenten die ervoor zorgen dat inkoopgroepen worden afgestemd op echte besluitvormingsprocessen. U kunt volledige het kopen groepen bepalen gebruikend klantgerichte drempels van het rollid die op de verkoopmethodologie van uw organisatie wijzen. Door minimum en maximumlidvereisten voor elke rol te bepalen, bepaalt u duidelijke criteria voor wat een verkoopklaar koopgroep vormt.

De volledigheidsscore van de koopgroep biedt een nauwkeurige maatstaf voor de verkoopgereedheid voor de groep. Als u bijvoorbeeld een kans voor een specifieke oplossing wilt aangrijpen, hebt u mogelijk minstens twee besluitvormers nodig, één beïnvloedende instantie en ten minste één arts. De berekening van de volledigheidsscore is gebaseerd op elk van deze rolspecifieke vereisten en geeft een overzicht van de algemene gereedheid van de inkoopgroep.

## De doeltreffendheid van de reis meten

De volledigheid van de inkoopgroep fungeert als een prestatiekernindicator (KPI) voor de doeltreffendheid van de reis. Het doel voor een specifieke reis kan zijn de volledigheid van de koopgroep met een bepaald percentage te verhogen of een minimumdrempel te bereiken alvorens verkoopklaar alarm in werking te stellen.

In een grote onderneming, zou u één persoon per rol kunnen identificeren. Nochtans, kan die persoon niet het juiste contact voor de verkoop zijn, of u kunt veelvoudige contacten in kritieke rollen nodig hebben. Een grote organisatie kan bijvoorbeeld verschillende besluitvormers op het gebied van informatietechnologie (IT) hebben die over afdelingen of bedrijfseenheden worden verspreid. Het identificeren van één besluitvormer is wellicht niet voldoende voor een complexe bedrijfsverkoop.

Nadat u de huidige het kopen groepsvolledigheid analyseert, kunt u het vereiste aantal contacten voor elke rol in het rolmalplaatje aanpassen. Met deze aanpassingen kunt u de strategie voor uw inkoopgroep afstemmen op basis van echte patronen en verkoopresultaten.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## Berekening van de rolvolledigheid {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="Berekening van de rolvolledigheid"
>abstract="De scores voor de volledigheid van de rol worden berekend als een percentage gebaseerd op het aantal leden dat aan een rol wordt toegewezen."

Journey Optimizer B2B edition berekent de volledigheidsscore voor elke afzonderlijke rol van de inkoopgroep als een percentage. Baseer deze score op hoeveel leden aan de rol worden toegewezen, vergeleken met [ het aantal dat in het rolmalplaatje ](./buying-groups-role-templates.md#change-the-completeness-score-settings) voor voltooiing wordt vereist.

De rolvolledigheidsberekening is een lineair percentage tussen nul en de gespecificeerde drempel (vereiste leden):

* Als het aantal toegewezen leden **nul** is, is de rolvolledigheid **0%**.
* Als het aantal toegewezen leden **bij of boven de drempel** is, is de rolvolledigheid **100%**.
* Als het aantal toegewezen leden **tussen één en de drempel** is, wordt de volledigheid proportioneel berekend.

### Formule voor volledigheid van rollen

Het percentage voor volledigheid van de rol wordt berekend met behulp van de volgende formule:

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

Waarbij:

* `Assigned Members` = Huidig aantal leden in de rol
* `Threshold` = De vereiste waarde voor leden is ingesteld in de rolsjabloon

### Voorbeelden van rollenvolledigheid

De volgende voorbeelden illustreren rolvolledigheidsberekeningen met verschillende drempelconfiguraties:

| Functie | Vereiste leden | Toegewezen leden | Berekening | Volledige rol |
|------|------------------|------------------|-------------|-------------------|
| Beslissingsmaker | 3 | 0 | Geen | 0% |
|  |  | 1 | 1/3 × 100 | 33% |
|  |  | 2 | 2/3 × 100 | 66% |
|  |  | 3 | Bij de drempel | 100% |
|  |  | 4 | Boven de drempel | 100% |
| Influencer | 5 | 0 | Geen | 0% |
|  |   | 1 | 1/5 × 100 | 20% |
|  |   | 2 | 2/5 × 100 | 40% |
|  |   | 3 | 3/5 × 100 | 60% |
|  |   | 4 | 4/5 × 100 | 80% |
|  |   | 5 | Bij de drempel | 100% |
|  |   | 6 | Boven de drempel | 100% |

## Berekening van de volledigheid van de koopgroep {#buying-group-completeness-calculation}

De volledigheidsscore van de koopgroep bestaat uit een aggregatie van de individuele volledigheidsscores voor rollen. Deze berekening verstrekt een holistische mening van het kopen van groepsbereidheid over alle bepaalde rollen.

### Volledige formule voor inkoopgroep

Het volledigheidspercentage van de koopgroep wordt berekend aan de hand van de volgende formule:

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

Waarbij:

* `Role Completeness %` = percentage van de individuele rolvolledigheid (0-100%)
* `Σ` = som over alle rollen in de het kopen groep

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->