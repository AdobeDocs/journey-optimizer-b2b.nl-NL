---
title: Generatieve AI voor inhoud
description: Leer om gepersonaliseerde e-mail en landende pagina's met generatieve AI in  [!DNL Journey Optimizer B2B Edition] tot stand te brengen, met inbegrip van het veroorzaken van beste praktijken.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
source-git-commit: d3238fa94f28c6d7e3fc0dce5b59fd70d8e74e34
workflow-type: tm+mt
source-wordcount: '2482'
ht-degree: 1%

---

# Generatieve AI voor inhoud {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="Genereren van AI-inhoud"
>abstract="Nadat u de lay-out hebt gemaakt, kunt u generatieve AI-gereedschappen in [!DNL Journey Optimizer B2B Edition] gebruiken om de inhoud te verbeteren. Deze functie vereenvoudigt het proces van personalisatie en inhoudverbetering door de inhoud af te stemmen op uw beschrijvende vraag."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="Referentie-inhoud"
>abstract="De inhoud van de Verwijzing van het gebruik _om een activadossier te uploaden dat inhoud bevat die extra context voor generatieve AI in [!DNL Journey Optimizer B2B Edition] verstrekt, of een eerder geupload dossier te selecteren._ Met deze optie zorgt u ervoor dat alle noodzakelijke materialen beschikbaar zijn om de kwaliteit en relevantie van gegenereerde inhoud te verbeteren."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Adobe generatieve AI-termen"
>abstract="Voor toegang tot deze functie moet u akkoord gaan met de Adobe Experience Cloud Generative AI-gebruikersrichtlijnen. Controleer of de uitvoer van deze functie nauwkeurig is en of deze geschikt is voor uw gebruiksscenario."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe Generative AI-gebruikersrichtlijnen"

Generatieve AI voor inhoud in [!DNL Adobe Journey Optimizer B2B Edition], aangedreven door Microsoft Azure OpenAI en Adobe Firefly, biedt proactieve suggesties voor het variëren van inhoud voor tekst en afbeeldingen. Optimaliseer de invloed van uw inhoud door te experimenteren met verschillende hoofdtitels en afbeeldingen.

Met de generatieve AI-functies voor het maken van inhoud in [!DNL Journey Optimizer B2B Edition] kunt u Adobe-generatieve AI-mogelijkheden benutten. Ontwerp gepersonaliseerde tekst en beelden voor e-mails, SMS-berichten, bestemmingspagina&#39;s en meer. Wanneer u een volledige campagne ontwikkelt of gewoon specifieke middelen verfijnt, helpen deze functies u inhoud naadloos aan uw merkrichtlijnen aan te passen en kostbare tijd te besparen.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>Als u toegang wilt krijgen tot deze functies in [!DNL Journey Optimizer B2B Edition] , hebt u de machtiging _[!UICONTROL AI Assistant]_>_[!UICONTROL Generate Content]_ nodig. Voor meer informatie over hoe een productbeheerder eigenschaptoestemmingen kan verlenen, zie [ rollen voor producttoestemmingen ](../admin/user-management.md#edit-roles-for-product-permissions) uitgeven.

De Hulpmiddelen van AI voor inhoudsgeneratie worden gesteund met de volgende activa:

* [E-mails](../content/ai-assistant-emails.md)
* [!BADGE  Beta ] [ het Bestaan pagina&#39;s ](../content/ai-assistant-landing-pages.md)

## Algemene richtsnoeren en beperkingen {#general-guidelines-and-limitations}

Uw gebruik van generatieve AI eigenschappen is onderworpen aan de [ Generatieve AI Richtlijnen van de Gebruiker van Adobe Experience Cloud ](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Met Adobe verplichting aan transparantie in het gebruik van generatieve hulpmiddelen AI voor media verwezenlijking, past Adobe [ inhoudsgeloofsbrieven ](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} voor om het even welk inhoud of project toe dat a [!DNL Firefly] - geproduceerd activa omvat wanneer het wordt gedownload of uitgevoerd.

Lees de volgende algemene richtlijnen voor het gebruik van generatieve AI voor inhoud in [!DNL Journey Optimizer B2B Edition] :

* Gebruik duidelijk gedefinieerde aanwijzingen voor een nauwkeurige interpretatie van het generatieve AI-model. Het marketingdoel of de vraag die u opgeeft, heeft een sterke invloed op de kwaliteit van de gegenereerde inhoud.

* Upload inhoudsreferentiebestanden met nauwkeurige, on-brand-inhoud. Anders is de inhoud gebaseerd op openbaar beschikbare informatie. De geüploade inhoud kan de volgende bestandsindelingen hebben: PDF, JPEG, PNG of ZIP (met ondersteunde bestandsindelingen). De maximale grootte voor een geüpload bestand is 50 MB. Grotere bestanden of een groot aantal afbeeldingen kunnen werken, maar hierdoor neemt de verwerkingstijd toe.

* Gebruik een merkspecifieke of aangepaste sjabloon om uw e-mailinhoud te maken. E-mailsjablonen met maximaal 8-10 afbeeldingen worden aanbevolen.

* Zorg ervoor dat u eventuele problematische uitvoer meldt met het blokje omhoog, omlaag of de vlagpictogrammen wanneer u varianten selecteert.

## Aanbevolen werkwijzen vragen voor generatieve AI {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="Vragen"
>abstract="Ontdek de documentatie van [!DNL Journey Optimizer B2B Edition] om te leren hoe u effectieve aanwijzingen kunt maken voor het produceren van marketinginhoud die in hoge mate wordt geconverteerd en on-brand wordt verkocht."

Deze gids helpt u uw verzoeken structureren, intent met duidelijkheid communiceren, en ervoor zorgen dat AI overseinen produceert die zich op uw merkrichtlijnen, publieksbehoeften, en campagnedoelstellingen richten.

Leer hoe u effectieve herinneringen schrijft waarmee AI Assistant kwalitatief hoogwaardige, on-brand marketinginhoud kan genereren die is afgestemd op uw doelstellingen.

### Het CO-STAR-kader gebruiken {#costar-framework}

U bereikt de beste resultaten met gegenereerde inhoud door uw vragen te ordenen met behulp van het CO-STAR-framework. Deze gestructureerde aanpak biedt duidelijkheid voor precies wat u nodig hebt.

| Component | Wat het betekent | Waarom het belangrijk is |
| --- | ---- | ------ |
| **C - Context** | Achtergrond van uw campagne, product of situatie | Verstrekt begrip voor het grotere beeld |
| **O - Doelstelling** | Uw specifieke marketingdoelstelling | Stuurt wat de inhoud moet bereiken |
| **S - Stijl** | Hoe u wilt communiceren | Hiermee wordt de methode ingesteld |
| **T - Toon** | Emotionele stijl en stem | Vormt hoe uw bericht zich voelt |
| **A - Publiek** | Het doelpubliek | Zorgt ervoor dat het bericht met de juiste mensen resoneert |
| **R - Vereisten** | Specifieke beperkingen of must-haves | Definieert grenzen en kritieke elementen |

{style="table-layout:fixed"}

### Grondbeginselen {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Do</th>
<th>Niet doen</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>Gebruik van het CO-STAR-kader voor structuur
<li>Wees expliciet over verse versus bestaande inhoud
<li>Focus geven op het gebruik van documenten met specifieke richtlijnen voor extractie
<li>Selecties maken voor toon, strategie en landinstelling
<li>Commerciële doelstellingen afstemmen op inhoudstype-mogelijkheden
<li>Meerdere varianten genereren voor A/B-tests</ul>
</td>
<td>
<ul><li>Vragen om structurele wijzigingen, opmaak of beeldbewerking in aanwijzingen
<li>Meningstoon/strategie in aanwijzingen, indien beschikbaar in opties
<li>Gebruik vage doelstellingen zoals _het product promoten.
<li>Selecties voorwaardelijk element aanvragen
<li>Layoutwijzigingen via vragen verwachten</ul>
</td>
</tr>
</tbody>
</table>

### Inhoud niet ondersteund in aanwijzingen

>[!TIP]
>
>Gebruik de ontwerpgereedschappen of [!DNL Adobe Express] voor visuele/afbeeldingswijzigingen.

De volgende verzoeken worden **_niet gesteund_** en zouden door andere hulpmiddelen moeten worden behandeld:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rood kruisje">  Wijzigingen in e-mailstructuur</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rood kruisje">  Wijzigingen in visuele opmaak</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rood kruisje">  Beeldbewerkingen</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Te wijzigen specifieke secties selecteren</li>
<li>Elementen verwijderen of klonen</li>
<li>Voorwaardelijke selecties</li>
<li>Schermindelingssecties toevoegen of verwijderen</li>
</ul>
</td>
<td>
<ul>
<li>Tekstopmaak (vet, cursief, lettergrootte)</li>
<li>Kleurwijzigingen</li>
<li>Indelingsstijl (randen, opvulling, marges)</li>
<li>Visuele effecten (schaduwen)</li>
</ul>
</td>
<td>
<ul>
<li>Wijzigingen in achtergrond</li>
<li>Tekstbedekkingen of logo's toevoegen</li>
<li>Uitsnijden of vergroten/verkleinen van afbeelding</li>
<li>Kleuraanpassingen</li>
<li>Vervanging afbeelding</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Kwaliteitscontrolelijst {#quality-checklist}

Controleer voordat u inhoud genereert het volgende:

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} **Duidelijke doelstelling**: verklaart duidelijk de actie, het product/de dienst, de waarde, en de context.

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} **Gedefinieerd doelpubliek**: Specificeert de demografisch, de rol, of het segment.

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} **het type van Inhoud groepering**: De doelstelling past het geselecteerde kanaal of het formaat aan.

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} **selecties van het Overzicht**: De toon, de strategie, en de scène worden gekozen, omvatten hen niet in de herinnering.

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} **de nadruk van het Document wordt gespecificeerd**: Hoogtepunten die inhoud of secties aan verwijzing.

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} **toegepaste Merk**: De aangewezen merkrichtlijnen worden geselecteerd.

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} **Realistisch werkingsgebied**: Vermijd verzoeken om lay-outveranderingen, het stileren, of structurele geeft uit.

### Effectieve marketingdoelstellingen {#marketing-objectives}

Zorg er bij het ontwerpen van marketingdoelstellingen voor dat deze duidelijk, handelbaar en meetbaar zijn. Vermijd vage of algemene verklaringen.

**Voorbeelden van goede doelstellingen:**

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;de teken-ups van de Aandrijving voor de vrije 30 dagproef van het nieuwe AI-Aangedreven analysedashboard&quot;

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;produceer lood voor B2B webinar op het &quot;Vermindering van de Kosten van de Wolk met 40%&quot;die Maart 15&quot;gebeuren

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;promoeer de beperkte tijd 25% korting op premieabonnementen, die December 25&quot;beëindigen

**Voorbeelden om te vermijden:**

![ rode kruis uit ](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;promoot het product&quot;(te vaag)

![ rood kruis uit ](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;maakt mensen ondertekent overeenkomsten&quot;(onduidelijke waarde)

![ rode kruis uit ](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;E-mail over nieuwe eigenschappen&quot;(gebrek doel)

#### Uw doel structureren

Geef altijd context en waardevoorstel op voor het produceren van relevante inhoud. Gebruik de volgende formule om u te helpen efficiënte doelstellingen schrijven: **Actie + Product/Dienst + Waarde/Voordeel + Urgentie/Context**

**Voorbeelden van goede doelstellingen:**

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Moedig downloads van nieuwe mobiele app aan die gebruikers helpt duurzame levende gewoonten met gepersonaliseerde eco-vriendelijke aanbevelingen volgen&quot;

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;bevordert registratie voor de exclusieve workshop over geavanceerde technieken voor gegevensvisualisatie voor marketing beroeps&quot;

![ Groen vinkje ](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;Aanwezigheid van de Aandrijving aan de gebeurtenis van de productlancering tonen tonend de revolutionaire AI schrijvend medewerker die 5+ uren per week bespaart&quot;

**Voorbeelden om te vermijden:**

![ rode kruis uit ](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;kondigt nieuwe app&quot;(het missen waardevoorstel en context) aan

![ rood kruis uit ](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;krijgt mensen om zich voor workshop&quot;aan te melden&quot; (mist specificiteit over publiek en voordeel)

![ rode kruis uit ](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;bevordert gebeurtenis&quot;(geen duidelijke actie, waarde, of urgentie)

#### Voorbeelden worden per kanaaltype gevraagd {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Kanaal</th>
<th>Voorbeeld</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-mail</strong></td>
<td>"De vooruitzichten van de onderneming van de genezing door drie klanten succesverhalen met gedetailleerde ROI metriek te tonen (Oracle: 45% kostenvermindering, Accenture: 200% loodverhoging, Microsoft: 60% tijdbesparingen). IT-directeuren op bedrijven met meer dan 1000 werknemers</td>
</tr>
<tr>
<td><strong>Landingspagina's</strong></td>
<td>"Zet B2B-bezoekers om in gekwalificeerde leads door aan te tonen hoe de beveiligingsoplossing van het bedrijf 99,9% van de cyberaanvallen voorkomt, met Fortune 500-getuigenissen en een gratis beveiligingscontrole"</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### Nieuwe inhoud versus wijziging van bestaande inhoud {#new-vs-modify}

Geef duidelijk aan of uw verzoek betrekking heeft op het genereren van nieuwe inhoud of het bijwerken van bestaand materiaal. Dit onderscheid is belangrijk omdat het de AI begeleidt bij het kiezen van de juiste aanpak en een nauwkeuriger en bruikbaarder resultaat garandeert.

#### Nieuwe inhoud maken

Pas deze strategie toe wanneer u marketingcampagnes start, nieuwe oplossingen onthult of bijgewerkte/vernieuwde communicatie start. Het zorgt ervoor dat uw bericht sterk begint en zich op uw doelstellingen richt.

**hoe te om** te veroorzaken ➤ wanneer het creëren van nieuwe inhoud, nadruk op uw marketing doelstelling zonder bestaande inhoud van verwijzingen te voorzien.

>[!BEGINSHADEBOX  &quot;Voorbeelden&quot;]

* **proef SaaS**: &quot;Start de nieuwe software van CRM aan kleine bedrijfseigenaars, die 50% tijdbesparingen, 90% snellere loodkwalificatie benadrukken, en het aanbieden van een 30 dagen vrije proef met gepersonaliseerd onboarding&quot;
* **de aankondiging van de Eigenschap**: &quot;kondig nieuwe API integratiemogelijkheden aan die ontwikkelingstijd door 60% voor ondernemingsklanten verminderen, richtend technische besluitvormers&quot;
* **Bevordering van de Gebeurtenis**: &quot;De registraties van de aandrijving voor webinar op &quot;Digitale Marketing Trends 2024&quot;kenmerkend deskundigen van Google, Meta, en Adobe, benadrukkend actionable inzichten en beperkte plaatsen (maximum 500)&quot;

>[!ENDSHADEBOX]

#### Bestaande inhoud wijzigen

>[!TIP]
>
>Voor standaardwijzigingen zoals uitwerken, vatten samen, of vereenvoudigen, uitgezocht **_verfijnen_** in plaats van douaneherinneringen te schrijven.

Gebruik een wijzigingsprompt wanneer u uw huidige marketingcampagnes moet bijwerken, vernieuwen of aanpassen. Deze methode steunt stijgende verbeteringen, die uw overseinen verzekeren relevant blijft zonder van kras te beginnen.

**hoe te om** te veroorzaken ➤ wanneer het wijzigen van bestaande inhoud, specificeer duidelijk wat u en hoe te het veranderen wilt.

>[!BEGINSHADEBOX  &quot;Voorbeelden&quot;]

* **de Campagne verfrist zich**: &quot;wijzig de e-mail van de programmalancering om zich op de eigenschappen van de ondernemingsveiligheid in plaats van algemene productiviteitsvoordelen te concentreren, richtend de besluitvormers van IT met nalevingscertificatie&quot;
* **Pieksprivot van het publiek**: &quot;Pas de uitnodiging van de softwaredemo aan om gezondheidszorg specifiek te richten, die generische voorbeelden met de gevallen van het gezondheidszorggebruik en de nalevingsvoordelen van HIPAA vervangen&quot;
* **seizoensgebonden update**: &quot;Werk Q3 promotiecampagne voor Q4 vakantiewinkelen bij, veranderend nadruk van terug aan school aan vakantiecadeau die met snelle het verschepen nadruk geeft&quot;

>[!ENDSHADEBOX]

## Geavanceerde tekstinstellingen {#text-settings}

Naast het gebruik van een duidelijke en goed gevormde herinnering, omvatten de tekstmontages in de AI Hulp inhoudshulpmiddelen tekstmontages die u kunt gebruiken om de geproduceerde output te optimaliseren.

>[!TIP]
>
>Gebruik de opties _[!UICONTROL Communication strategy]_en_[!UICONTROL Tone]_ in _[!UICONTROL Text settings]_in plaats van deze kenmerken in de vraag te vermelden.

### Typen communicatiestrategie

Uw communicatiestrategie bepaalt hoe u uw boodschap presenteert om de impact te maximaliseren. De verschillende strategieën werken beter voor verschillende doelstellingen, of u urgentie bouwt, vertrouwen vestigt, of drijft directe actie. Kies de strategie die het beste aansluit bij uw campagnedoelstellingen en doelgerichtheid.

| **Strategie** | **Best voor** | **de stijl van het Overseinen** | **Voorbeelden** |
| ------------ | ------------ | ------------------- | ------------ |
| **Dringend** | Tijdgevoelige aanbiedingen, termijnen, onmiddellijke actie | Creeert directe druk met op tijd-gebaseerde taal | <li>&quot;Nu handelen: aanbieding verloopt om middernacht&quot; <li>&quot;Registreer u vandaag nog voordat vlekken opvullen&quot; <li>&quot;De 48-uursverkoop begint nu&quot; |
| **FOMO (Angst om uit te ontbreken)** | Beperkte aanbiedingen, evenementen, exclusieve toegang | Gebruikt aanwijzingen voor urgentie, schaarste en tijdsdruk | <li>&quot;Nog maar 24 uur over! Beperkte voorraad tegen 40% korting&quot; <li>&quot;Laatste kans: Vroege prijsstelling voor vogels eindigt morgen&quot; <li>&quot;Slechts 100 bètavlekken resterend&quot; |
| **Sociale Bewijs** | Betrouwbaarheidsopbouw, getuigenissen, populaire producten | Gebruikt ervaringen en validatie van anderen | <li>&quot;Sluit u aan bij 50.000+ tevreden klanten&quot; <li>&quot;Nominale 4,9/5 sterren door professionals uit de industrie&quot; <li>&quot;Vertrouwd door Fortune 500-ondernemingen&quot; |
| **Scarcity** | Beperkte voorraad, exclusieve releases, producten van hoge vraag | Benadrukt beperkte beschikbaarheid en exclusiviteit | <li>&quot;Slechts 5 in voorraad&quot; <li>&quot;Beperkte uitgave: 100 beschikbare eenheden&quot; <li>&quot;Exclusieve release: First come, first serving&quot; |
| **Stimulerend** | Promoties, beloningsprogramma&#39;s, speciale aanbiedingen | Belangrijkste tastbare voordelen en beloningen | <li>&quot;Maak 20% korting op uw eerste bestelling&quot; <li>&quot;Verdien dubbele punten dit weekend&quot; <li>&quot;Gratis verzending voor bestellingen van meer dan € 50&quot; |
| **Exclusiviteit** | Premium producten, VIP-ervaringen, alleen voor leden | Gebruikt premiumpositionering en taal voor speciale toegang | <li>&quot;Exclusieve uitnodiging voor een privévoorvertoning&quot; <li>&quot;Elite membership ontgrendelt advanced analytics&quot; <li>&quot;Sluit u aan bij geselecteerde Fortune 500-bedrijven die ons al gebruiken&quot; |
| **Gamification** | Betrokkenheidscampagnes, loyaliteitsprogramma&#39;s, interactieve inhoud | Gebruikt spelmechanica en prestatietaal | <li>&quot;Je volgende bonusniveau ontgrendelen&quot; <li>&quot;Volledige uitdagingen om badges te verdienen&quot; <li>&quot;Beklimmen van het spelersbord voor exclusieve prijzen&quot; |
| **Informatief** | Onderwijs, onderzoek, complexe producten, gedachteleiding | Gebruikt feiten, gegevens, inzichten en uitleg | <li>&quot;5 inzichten van het analyseren van 10.000+ interacties&quot; <li>&quot;Nieuw onderzoek onthult 3 doorbraakbenaderingen&quot; <li>&quot;Volledige gids voor de implementatie van AI bij het in de handel brengen&quot; |
| **Onderwijs &amp; Inzichten** | Leerinhoud, trends in de branche, beste praktijken | Biedt waardevolle kennis en activeerbare taken | <li>&quot;Leer geavanceerde technieken met een handleiding voor experts&quot; <li>&quot;Ontdek 7 strategieën die top marketers gebruiken&quot; <li>&quot;Leer hoe u uw workflow in 5 stappen kunt optimaliseren&quot; |

### De juiste toon instellen {#tone}

Tint bepaalt hoe de doelgroep uw boodschap waarneemt en reageert. Selecteer altijd een tint die is afgestemd op uw stem van het merk en het werkgebied van de profielreis.

Bekijk de beschikbare toonopties, inclusief wanneer elke stijl het beste werkt en voorbeelden van inhoud die in elke stijl past.

| Tonaliteit | Best voor | Voorbeeld van inhoud |
| ---- | ----- | ----- |
| Professional | B2B-communicatie, formele aankondigingen | &quot;We zijn blij om ons strategisch partnerschap aan te kondigen...&quot; |
| Empathetisch | Klantenondersteuning, gevoelige onderwerpen | &quot;We begrijpen hoe frustrerend deze kwestie voor u moet zijn...&quot; |
| Enorm | Campagnes, verlichte inhoud | &quot;Waarschuwing: kan tot aanzienlijke productiviteitswinst leiden!&quot; |
| Opwindend | Productlanceringen, gebeurtenispromoties | &quot;Dit is het moment waarop je hebt gewacht!&quot; |
| Inspiratie | Motiviteitscampagnes, merkdoel | &quot;Samen kunnen we een verschil maken in de wereld...&quot; |
| Persuasiet | Verkoopcampagnes, conversies | &quot;Mis deze beperkte kans niet aan...&quot; |
| vriendelijk | Klantenservice, welkomstberichten | &quot;Gelukkig ben je hier met ons!&quot; |
| Formeel | Juridische mededelingen, officiële aankondigingen | &quot;Dit is een melding van de volgende wijzigingen...&quot; |
| Apologetisch | Serviceterugwinning, probleemoplossing | &quot;Bodea verontschuldigt zich oprecht voor elk veroorzaakt ongemak...&quot; |
| Assertief | Leaderinhoud, gezaghebbende overseinen | &quot;Dit is wat je nu moet doen...&quot; |
| Verteller | Merkverhalen, emotionele verbindingen | &quot;Het begon allemaal met een simpele vraag...&quot; |
| Gesprek | Nuratiecampagnes, relatieopbouw | &quot;Laten we praten over hoe dit programma u kan helpen...&quot; |

## Geoptimaliseerde referentie-inhoud {#reference-content}

>[!TIP]
>
>Als u al een element hebt geüpload via het menu **[!UICONTROL Reference content]** , hoeft u er niet naar te verwijzen in de vraag. Het systeem gebruikt automatisch geselecteerde documenten.

De dossiers van de inhoud van de verwijzing verstrekken feitelijke informatie die uw geproduceerde inhoud met specifieke, nauwkeurige details verrijkt. Wanneer u documenten uploadt, zoals productbrochures of whitepapers, wijzigt u uw vraag om op te nemen welke onderdelen focus hebben:

* **in plaats van** _&quot;Gebruik de productbrochure&quot;_ **u** _&quot;concentreert zich op de geavanceerde veiligheidseigenschappen en nalevingscertificatie, specifiek SOC 2 naleving en gegevensencryptie&quot;zou moeten gebruiken_

* **in plaats van** _&quot;Verwijzing de casestudies&quot;_ **u** _zou moeten gebruiken &quot;de resultaten van ROI van het Hoogtepunt van gezondheidszorgcliënten, specifiek de 40% kostenvermindering bij Regionaal Medisch Centrum&quot;_

* **in plaats van** _&quot;omvat technische details&quot;_ **zou u** _moeten gebruiken &quot;Benadruk API integratiemogelijkheden en ontwikkelaarsvoordelen, zich het concentreren op REST API eindpunten en 99.9% uptime SLA&quot;_

### Inhoud verfijnen

Nadat inhoud is gegenereerd, gebruikt u de functie **_[!UICONTROL Refine]_** om deze met de volgende opties te herhalen en te verbeteren:

* **[!UICONTROL Elaborate]** - AI Assistant kan u helpen om meer te doen over specifieke onderwerpen en biedt extra informatie voor een beter begrip en betrokkenheid.

* **[!UICONTROL Summarize]** - langdurige informatie kan paginaviewers overladen. Met AI Assistant kunt u belangrijke punten samenvoegen tot heldere, beknopte samenvattingen die aandacht trekken en hen aanmoedigen om verder te lezen.

* **[!UICONTROL Rephrase]** - herschrijf het bericht terwijl het zijn betekenis behoudt. Met deze optie kunt u alternatieve bewoordingen genereren, de stroom verbeteren of de formulering aanpassen zonder het kernbericht te wijzigen.

* **[!UICONTROL Use simpler language]** - Vereenvoudig de taal en zorg voor helderheid en toegankelijkheid voor een groter publiek.

* **[!UICONTROL Translate]** - Vertaal de tekst naar een andere taal. (Momenteel is Engels de enige ondersteunde taal.)

* **[!UICONTROL Change tone]** - Pas de toon van het bericht aan om zich aan uw communicatie stijl aan te sluiten, zoals het vriendelijker, professioneel, urgente, of inspirerend maken.

* **[!UICONTROL Change Communication strategy]** - Wijzig de berichtenbenadering op basis van uw doelstellingen, zoals het creëren van urgentie, of het benadrukken van opwindende aantrekkingskracht.
