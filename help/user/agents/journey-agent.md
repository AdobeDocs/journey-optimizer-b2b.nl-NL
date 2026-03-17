---
title: Journey Agent B2B
description: Leer hoe u de door AI aangedreven Journey Agent en zijn vaardigheden kunt gebruiken om robuuste B2B-reizen te bouwen, te beheren en waar te nemen.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
exl-id: 5d2945ab-4f6c-4d9c-b0a1-1a93dc1849f3
source-git-commit: 51bb47fe4f494095f1c598639f02f273b9a125ae
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# Journey Agent B2B

Journey Agent B2B is een door AI aangedreven assistent in Adobe Journey Optimizer B2B edition die u helpt bij het ontwerpen, uitvoeren, optimaliseren en bewaken van B2B-reizen in natuurlijke taal. Het vermindert de tijd en de ingewikkeldheid betrokken bij de bouw van en het beheer van klantenreizen door automatisering, gegeven-gedreven aanbevelingen, en real-time observability te combineren.

![&#x200B; Journey Agent B2B Vragen &#x200B;](./assets/journey-agent-prompt.png)

De Journey Agent B2B biedt een reeks AI-vaardigheden, elk gericht op een ander aspect van de levenscyclus van de B2B-reis. De momenteel beschikbare vaardigheden zijn:

* **[Reis bouwt vaardigheid](#journey-build-skill)** - creeer, werk, en optimaliseer reizen van natuurlijke taalherinneringen bij
* **[de vaardigheid van de Waarneming van de Reis](#journey-observability-skill)** - stel vragen over hoe de rekeningen en de mensen zich door actieve reizen bewegen

## Vaardigheid voor het maken van een reis

De vaardigheid van de Bouwstijl van de Reis zet uw marketing doelstellingen, betrokkenheidsstrategie, en KPIs in volledige B2B klantenreizen om. Het pakt drie belangrijke uitdagingen aan waarmee B2B-marketers vandaag worden geconfronteerd:

* Het behandelen van meer en meer complexe klantenreizen (ingewikkeldheid in publiek, inhoud en overseinen, en omnichannel)
* Efficiënter maken in het licht van strengere budgetten
* Bepalen hoe de optimale reis van de klant moet worden gestructureerd

Als teller, kunt u deze vaardigheid gebruiken om:

* **creeer** - vertaal uw marketing doelstellingen, producten, betrokkenheidsstrategie, en KPIs in een gepersonaliseerde klantenreis met automatisering en voorwaarden
* **adviseer** - hefboomwerking voorbij marketing overeenkomst en andere historische gegevens om reisverwezenlijking te optimaliseren
* **optimaliseer** - analyseer, pas, en optimaliseer actieve reizen aan die op voorspellingen of daadwerkelijke prestaties worden gebaseerd
* **beheer** - Prioriteit, beheer, en orkestreer overlappende reizen en berichtlevering

### Basisgebruik

Als u de Journey Agent Build-vaardigheid wilt gebruiken, typt u in het venster met de vraag wat u wilt maken met behulp van een natuurlijke taal:

&quot;Maak een B2B-reis om besluitvormers uit te nodigen voor een routekaart voor een rekening in loondienst, die naar alle waarschijnlijkheid een nieuwe pijpleiding zal openen.&quot;

![&#x200B; agent B2B van de Reis herinnering voor de vaardigheid van de Bouwstijl &#x200B;](./assets/journey-agent-tasks.png)

Hoe meer details u kunt verstrekken, hoe beter het antwoord zal zijn. Als u bestaande marketing materialen hebt die de gebeurtenis, of uw product, enz. beschrijven, kleef dat in de herinnering, zodat heeft de Agent een beter gevoel van het doel.

&quot;Doe dienst als B2B reisstrategist om een multi-stage reis van de klantenrekening tot stand te brengen die beleidsmakers en marketing persoonlijkheden in de vroege exploratiefase van `<Solution Name>` voedt en aangaat. Het doel is om anonieme bezoekers om te zetten in bekende contacten, de betrokkenheid met relevante inhoud op `<domain>`.com te verdiepen en voorgekwalificeerde leads voor `<Product Name>` -verkoopactiviteiten. Gebruik kanalen zoals e-mail en betaalde media, die bestaande publiekssegmenten en inhoud gebruiken. Structuur de reis over voorlichting, overweging, en evaluatiestappen over 4 tot 6 weken, met duidelijke trekkers, acties, en doelstellingen voor elke fase. Neem KPI&#39;s op zoals conversiekoersen, betrokkenheidsscores en demoverzoeken en retourneer de uitvoer als een gestructureerde transportstroom.&quot;

Deze gedetailleerde herinnering verstrekt:

* **Duidelijke Intentie**: Wat wilt u AI doen? Wees specifiek over de taak of het resultaat.
* **context-Rich**: Verstrek relevante achtergrond of beperkingen. Voeg indien mogelijk voorbeelden of verwijzingen toe.
* **Gestructureerd Formaat**: De kogelpunten van het gebruik, genummerde stappen, of malplaatjes.
* **Taak Toewijzing van de Rol**: Specificeer de rol van AI - &quot;Akte als gegevensanalist...&quot;

Gebruik de agent om verfijning te herhalen: Begin eenvoudig, verfijn dan uw herinnering die op de resultaten wordt gebaseerd. Feedbackloops verbeteren de resultaten in de loop der tijd.

### Eind-tot-eind B2B-reiscreatie

De vaardigheid van de Bouwstijl van de Reis kan een reis van begin tot eind (rekening of persoonreis) van natuurlijke taaltekstherinneringen en meta-gegevens, door een gesprekservaring eerder dan een traditioneel gebruikersinterface produceren.

Voorbeelden van end-to-end Reis-prompt:

* Maak een reis over het kanaal naar accounts die de afgelopen 30 dagen niet met mijn inhoud zijn gemoeid.
* Creeer een reis om een oplossing aan rekeningen over te brengen die hoge intentie zonder open pijpleiding tonen door gepersonaliseerde inhoud voor de belangrijkste het kopen groeprollen te verstrekken.
* Een B2B-reis maken om besluitvormers uit te nodigen voor een routekaart voor een rekening in dienst genomen rekeningen die naar alle waarschijnlijkheid een nieuwe pijpleiding zullen openen.
* Maak een reis naar whitespace-accounts met de intentie voor mijn oplossing, waarbij u zich richt op mensen die zich bezighouden met inhoud op de website.

### Meerfasentransporten

U kunt als B2B reisontwerper handelen om een multi-stadium reis van de klantenrekening tot stand te brengen die besluitvormers en marketing persoonlijkheden reeds in de exploratiefase informeert.
Het doel is anonieme bezoekers om te zetten in bekende contacten, de betrokkenheid met relevante inhoud te verdiepen, en primordiale gekwalificeerde leads voor verkoopbevordering.

* Gebruik kanalen zoals `Email` , `Paid media` , `Personalized web experiences` om bestaande publiekssegmenten en -inhoud te benutten.
* Structuur de reis over `awareness`, `consideration`, en `evaluation` stadia over 4-6 weken, met duidelijke trekkers, acties, en doelstellingen voor elk stadium.
* Neem KPI&#39;s op, zoals `conversion rates` , `engagement scores` en `demo requests` , en retourneer de uitvoer als een gestructureerde transportstroom.

## Reiswaarneming

De vaardigheid van de Waarneming van de Reis laat u natuurlijke taalvragen stellen over hoe de rekeningen en de mensen zich door uw B2B reis-zonder het graven door reiskaarten, logboeken, of dashboards bewegen. Het bestrijkt twee hoofdgebieden: voortgang van de reis en waarneming van gegevenssynchronisatie.

U hebt toegang tot dit bestand op twee plaatsen in Journey Optimizer B2B edition:

* **Recht-spoorMedewerker in de reiskaart** - stel reis-specifieke vragen direct van de reiskaart. De reisnaam wordt automatisch in context ingespoten.

* **volledig-scherm Hulp pagina** - een grotere gespreksmening geschikt voor complexe of dwars-rekeningsvragen en het onderzoeken van veelvoudige reizen.

### Reis op accountniveau insight

Traceer hoe een specifieke account een reis heeft doorlopen door vragen te stellen zoals:

* &quot;Geef me basisinformatie over account ACME Industries.&quot;
* &quot;Vertel me hoe Northstar Services de reis ABM Nurture Strategy heeft doorlopen.&quot;
* &quot;Wanneer is de rekening Contoso LLC deze reis begonnen?&quot;

### Splitsen-knoop weg redeneren en tellingen

Begrijp waarom een tak werd genomen en hoeveel mensen of rekeningen elke weg volgden:

* &quot;Waarom ging account QiDemoAccount24 naar het kleine Amerikaanse technische pad naar Californië bij gesplitst knooppunt c764a9?&quot;
* &quot;Geef me de mensen tellen voor elk weg in gespleten knoop-459c7c.&quot;
* &quot;Toon me mensen in de weg van San Jose voor Rekening8.&quot;

De agent inspecteert gespleten logica, rekeningsattributen, en activiteiten om het verpletteren van besluiten en terugkeer per-weg tellingen of personenlijsten te verklaren.

### Reisresultaten op individueel niveau

De individuele resultaten binnen een rekening of over een volledige reis-vooral nuttig voor het kopen van groepsanalyse en het vinden besluitvormer versus beïnvloedingsgedrag analyseren:

* &quot;Geef mij mensen tellen in elk pad voor dit gesplitste knooppunt voor Account123.&quot;
* &quot;Maak een lijst van de mensen in het verborgen overslaan pad.&quot;
* &quot;Toon mij mensen in het San Diego locatiepad voor dit account.&quot;

### Levenscyclus en timing van reizen

De belangrijkste tijdstempels voor een reis of specifieke rekeningen terugwinnen:

* &quot;Wanneer ging deze reis live?&quot;
* &quot;Wanneer is de eerste account deze reis binnengekomen?&quot;
* &quot;Wanneer is QiDemoAccount50 met deze reis gestart?&quot;

### Extern publiek en zichtbaarheid van activering

Voor reizen die naar externe kanalen zoals LinkedIn duwen, kunt u activeringsstatus controleren:

* &quot;Is bsmith@acme.com in het externe publiek?&quot;
* &quot;Lijst alle mensen die aan LinkedIn door ObservabilityExtAudience01 worden geactiveerd.&quot;

### Gegevenssynchronisatie en waarneming via pijpleidingen

De vaardigheid van de Waarnembaarheid kan de gezondheidsinformatie van de gegevenssynchronisatie ook oppervlakte helpen problemen oplossen waarom een rekening of een lood niet in een reis kunnen zijn omvat:

* Metriek en status van taken voor exporteren van externe doelgroepen
* Batchsegmentatieschema&#39;s en voltooiingstijden
* Onderhoudsplanning voor inkoopgroepen
* Taakbeheerstatus (voltooid/mislukt)