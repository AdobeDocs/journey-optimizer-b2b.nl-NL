---
title: Optimalisatie van e-mailverzendtijd
description: Met Send-Time Optimization (STO) in Adobe Journey Optimizer wordt de levering van e-mailberichten voor persoonlijke reizen gepersonaliseerd. Leer hoe u STO kunt inschakelen en de betrokkenheid kunt verbeteren.
feature: Person Journeys, Channels
role: User
source-git-commit: 55cfcd3b4ee777ee8945ea9a1cd1429625ee61c3
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Optimalisatie van e-mailverzendtijd

Gebruik de Send-Time optimalisering (STO) eigenschap om e-mailleveringstiming voor [&#x200B; personenreizen &#x200B;](../journeys/journeys-overview.md) te personaliseren door te voorspellen wanneer elk profiel het meest waarschijnlijk zal in dienst nemen. In plaats van een vaste verzendtijd gebruikt STO historische e-mailbetrokkenheidssignalen om de levering op het optimale tijdstip voor elke ontvanger te plannen, waardoor de totale betrokkenheid verbetert.

De STO analyseert de historische betrokkenheid van elk profiel met behulp van een groot taalmodel. Het voorspelt en rangschikt potentieel verzendt tijden, dan planning levering bij de hoogste-gerangschikte tijd binnen het optimaliseringsvenster.

## Huidige beschikbaarheid en bereik

Optimalisatie bij verzenden wordt momenteel ondersteund voor:

* **Type van Reis**: De Reizen van de persoon
* **Kanaal**: E-mail
* **Configuratie**: _verzendt e-mail_ actieknooppunt
* **Meldend**: AI Medewerker door de vaardigheid van de Waarneming van de Journey

  De inzichten van prestaties, zoals gebruik, betrokkenheidslift, en STO vs. niet-STO vergelijkingen, zijn beschikbaar door vragen van de natuurlijke taal in de Medewerker AI.

>[!BEGINSHADEBOX]

Er zijn vele **_toekomstige verhogingen_** gepland voor STO:

* Steun voor _de Reizen van de Rekening_
* Algemene STO-configuratie in het gebied _[!UICONTROL Admin]_
* STO-activering op reisniveau
* Configureerbare splitsingen in test/controle
* Een speciaal STO-rapporteringsdashboard

>[!ENDSHADEBOX]

## Configuratie

U kunt send-time optimalisering vormen wanneer u [&#x200B; a _[!UICONTROL Take an action]_&#x200B;knoop &#x200B;](../journeys/action-nodes.md) aan een persoonreis toevoegt.

1. Kies **[!UICONTROL Send email]** bij _[!UICONTROL Select action]_.

1. Schakel de functie in met de schakeloptie **[!UICONTROL Send-time Optimization]** .

1. Stel de STO-opties in om het venster en de testdistributie op te geven:

   * **[!UICONTROL Send within next]** - Deze waarde bepaalt het optimalisatievenster (in dagen). Dit is het tijdbereik waarin e-mails kunnen worden bezorgd. Bijvoorbeeld, voor een webinar die in vijf dagen voorkomt, zou u een venster van vier of van vijf dagen kunnen plaatsen. De STO selecteert de best voorspelde verzendtijd voor elk profiel binnen dit venster.

   * **STO/Vaste distributie** - STO leidt automatisch tot a _test en controle spleet_ om in aanmerking komende profielen tussen geoptimaliseerde en vaste verzendtijden te verdelen. De splitsing maakt directe prestatievergelijking mogelijk. (Toekomstige verbeteringen zijn gepland om aangepaste splitsingspercentages toe te staan.)

   >[!NOTE]
   >
   >Profielen met een sterke betrokkenheidsgeschiedenis worden gelijkmatig verdeeld in controle- en testgroepen om de invloed van de STO te meten. Om statistisch betrouwbare resultaten te verzekeren, wordt de verdeling van de STO vs. niet-STO beperkt tussen 30% en 70%. Hierdoor wordt voorkomen dat kleinere cohorten de resultaten scheeftrekken en zijn zinvolle vergelijkingen mogelijk.

   ![&#x200B; verzend de knoop van de e-mailreis - de opties van de Optimalisering van de Send-tijd &#x200B;](./assets/email-node-send-time-optimization.png){width="700" zoomable="no"}

1. Direct na de _[!UICONTROL Send email]_&#x200B;knoop, [&#x200B; voeg a_ toe wacht _knoop &#x200B;](../journeys/wait-nodes.md).

   Een wachttijdknooppunt moet onmiddellijk een e-mailactie met STO-functionaliteit volgen. Het toevoegen van deze knoop zorgt ervoor dat de profielen in de reis blijven tot het volledige optimaliseringsvenster wordt ontruimd en alle STO verzendt volledig is. Als u dit knooppunt weglaat, geeft het systeem aan dat de configuratie ongeldig is.

1. Nadat u de rest van de persoonreis voltooit, ga [&#x200B; te werk publiceren &#x200B;](../journeys/create-publish-journey.md#publish-a-journey).

## STO-inzichten

STO de inzichten worden geleverd door de _AI Medewerker_ gebruikend de 2&rbrace; de vaardigheid van de Waarneming van Journey Agent _[&#128279;](../agents/journey-agent.md#journey-observability-skill)._ U kunt vragen naar gebruik, betrokkenheidsmetriek, test-/besturingsresultaten, knooppuntprestaties en algemene invloed op de reis.
