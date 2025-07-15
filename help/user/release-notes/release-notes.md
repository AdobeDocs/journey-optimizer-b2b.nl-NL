---
title: Release-rotaties van Journey Optimizer B2B edition
description: Meer informatie over de nieuwste functies en verbeteringen in Adobe Journey Optimizer B2B Edition.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 7e9396a7ac029c173fe3d9b0b1bab6b7c4521ee0
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 6%

---

# Opmerkingen bij de release van Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen.

Journey Optimizer B2B edition is native gebaseerd op [!DNL Adobe Experience Platform] en erft van de nieuwste innovaties en verbeteringen. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest){target="_blank"}.

Herzie de [ productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} voor informatie over rechten, prestatiegaranties, en beperkingen.

## Opmerkingen bij de release 2025.5

**Datum van de Plaatsing**: 3 Juni, 2025

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Functie | E-mailtesten met Litmus | Met a [ rekening van de Samenhang ](https://www.litmus.com/email-testing){target="_blank"}, kunt u uw e-mailteruggevende voorproef in populaire e-mailcliënten van Journey Optimizer B2B edition nu. Dankzij deze integratie kunt u ervoor zorgen dat uw e-mailinhoud er goed uitziet en werkt zoals deze in elk Postvak IN is ontworpen. [Meer informatie](../content/email-test-rendering.md) |
| Verbetering | E-mail dupliceren | Wanneer u een e-mailbericht toevoegt voor een knooppunt voor de rit, kunt u nu een bestaande e-mail dupliceren. Wijzig het plaatsen of de inhoud voor gedupliceerde e-mail, of verlaat het intact.  [Meer informatie](../content/add-email.md#add-an-email-to-your-journey) |
| Verbetering | Opmaak voor token op de afspeelbalk voor e-mail | Personalization-tokens voor e-mailinhoud gebruiken nu een bijgewerkte indeling die volledig compatibel is met Handlebar-scripts. Dit formaat gebruikt _camel geval_ of onderstrepingen, die ruimten elimineren. [Meer informatie](../content/email-authoring.md#content-authoring---personalization) |
| Verbetering | Totaal aantal weergeven voor lijsten | De lijstpagina&#39;s _[!UICONTROL Solution Interests]_en_[!UICONTROL Account Journeys]_ worden uitgebreid met de weergave van het totale aantal naast de zoekbalk. |

## Opmerkingen bij de release 2025.4

**Datum van de Plaatsing**: 29 april, 2025

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Functie | Accountlijsten | U kunt nu een statische of dynamische accountlijst maken om benoemde accounts als doel in te stellen op basis van uw gedefinieerde criteria, zoals de industrie, locatie of grootte van het bedrijf. <a href="../accounts/account-lists.md">Meer informatie</a> |
| Functie | Reisorchestratie van rekeninglijsten | De knopen van de reisactie van het gebruik om rekeningen voor statische rekeningslijsten toe te voegen en te verwijderen. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">Meer informatie</a> |
| Verbetering | Reislidmaatschap filteren in Marketo Engage | De de rekeningslijsten van Adobe Journey Optimizer B2B edition van het gebruik voor het reispubliek en gebruiken dan het _Lid van een 1} filter van de rekeningslijst in Marketo Engage slimme lijsten._ <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">Meer informatie</a> |
| Functie | Inactiviteitsfilters | Orchestreer reizen op basis van inactiviteit in Marketo Engage-campagnes en -programma&#39;s, waaronder inactiviteit via e-mail, interessante momenten, wijzigingen in gegevenswaarde en bezochte webpagina&#39;s. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">Meer informatie</a> |
| Verbetering | Bezochte webpaginacilter | Reizen ordenen op basis van activiteiten voor bezochte webpagina&#39;s in verband met Marketo Engage-campagnes en -programma&#39;s. <a href="../journeys/split-merge-paths-nodes.md#people-path-conditions">Meer informatie</a> |
| Verbetering | Lijst met e-mails | Een algemene lijst met actieve en concept-e-mails weergeven die u wilt doorzoeken, controleren en bijwerken tijdens de bijbehorende accountreizen. <a href="../content/emails-list.md">Meer informatie</a> |

## Opmerkingen bij de release 2025.3

**Datum van de Plaatsing**: 1 April, 2025

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Functie | Accountreizen dupliceren | Er is nu een dubbele handeling beschikbaar voor reizen naar de account. U kunt de details voor de rekeningsreis dupliceren, of enkel een eenvoudig skelet van de stroom en wegstructuur. <a href="../journeys/journey-overview.md#duplicate-journey">Meer informatie</a> |
| Functie | Mijn tokens voor reizen voor rekening | U kunt nu een set aangepaste tokens definiëren met waarden die specifiek zijn voor de accountreis. Deze reeks douanetokens wordt genoemd _Mijn Tokens_ en om het even welk van deze douanetokens zijn voor verpersoonlijking wanneer het ontwerpen van reis e-mails. <a href="../content/personalization-my-tokens.md">Meer informatie</a> |
| Functie | Groepsfasen voor kopen verwijderen | U kunt het model voor de inkoopgroepfasen verwijderen wanneer dit zich in een concept of een gepubliceerde status bevindt. Als het (levend) wordt gepubliceerd, kunt u het schrappen slechts wanneer het niet met een oplossingsbelang wordt geassocieerd. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Meer informatie</a> |
| Verbetering | Aantal wegknooppunten | Verbeterde zichtbaarheid in gepubliceerde tellingen voor reisleden op knooppuntniveau. In de _kaart van de Reis_, tonen de knopen _[!UICONTROL Total accounts entered]_. Wanneer u een actieknooppunt selecteert, bevatten de gegevens aan de rechterkant ook_[!UICONTROL Accounts not yet actioned on]_ . En de details voor _luisteren naar een gebeurtenis_ knopen omvatten _[!UICONTROL Accounts at this step]_. Gebruik deze informatie om de voortgang van uw account in uw live, voltooide en afgebroken reizen te valideren. |

## Opmerkingen bij de release 2025.2

**Datum van de Plaatsing**: 11 Maart, 2025

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Functie | Aanpasbare velden - inhoudsfragmenten | Tijdens visueel fragmentontwerp kunt u parameters voor een component in het fragment toewijzen als bewerkbaar. Met deze functie kan de auteur van een e-mail of sjabloon een aangepaste veldwaarde opgeven die specifiek is voor zijn of haar behoeften. Deze aanpassingsvlag is beperkt tot beeld, tekst, en knoop visuele componenten. <a href="../content/fragment-authoring.md#enable-fragment-customization">Meer informatie</a> |
| Functie | Reisduplicatietypen | Wanneer u een accountreis dupliceert, kunt u knooppuntgegevens opnemen, exclusief e-mails en SMS-berichten die in Journey Optimizer B2B edition zijn gemaakt. Als alternatief kunt u een skelet-kopie maken van de structuur en padstromen, zonder knoopdetails en instellingen. <a href="../journeys/journey-overview.md#duplicate-journey">Meer informatie</a> |
| Verbetering | Vier extra e-mailvoorbeeldsjablonen | De voorbeeldsjabloonbibliotheek voor e-mailsjablonen bevat nu vier SecureFinacial-sjablonen als voorbeelden voor het opnieuw toewijzen, informeren, voeden en feedback geven van inhoudsvoorbeelden |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Opmerkingen bij de release 2025.1 {#Jan-2025}

**Datum van de Plaatsing**: 6 februari, 2025

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Functie | Experience Event door:sturen | Beheerders kunnen op Adobe Experience Platform (AEP) gebaseerde gebeurtenisdefinities configureren. Met deze configuraties kunnen markeertekens accountreizen maken die reageren op AEP Experience Events.  <a href="../admin/configure-aep-events.md">Meer informatie</a> |
| Functie | Betaalde mediabestemmingen | Bekende personen kwalificeren voor betaalde mediacampagnes vanaf een accountreis, zodat u ze verder kunt gebruiken op reclameplatforms, zoals LinkedIn. Gebruik een gesplitste padnode in een accountreis om accountpubliek te segmenteren op basis van specifiek gedrag en geef accounts aan die extra betrokkenheid rechtvaardigen. Dan, voeg mensen van die rekeningen aan een extern klantenpubliek door CDP in real time aan een gesteunde betaalde media bestemming toe. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Meer informatie</a> |
| Functie | Intelligent dashboard | Bekijk de progressie van het kopen van groepen door hun rekeningsreizen, met inbegrip van AI-Gegenereerde inzichten voor intelligentere analyse en nauwkeurige rekeningsprioriteitstelling. <a href="../dashboards/intelligent-dashboard.md">Meer informatie</a> |
| Functie | Gegevens van groep en account voor kopen | Bekijk inzichten op de koopgroep en account-niveau om meer context en historische gegevens te hebben wanneer u met een klant begint in gesprek te gaan.<p>De gegevens van de inkoopgroep omvatten alle gevonden intenties van de eerste partij. <a href="../buying-groups/buying-group-details.md">Meer informatie</a><p>In de accounts met accountdetails wordt de sterke toename in de betrokkenheid gemarkeerd die wordt gedetecteerd, zodat u de verkoop kunt waarschuwen voor accounts die klaar zijn voor een aangepaste, op de verkoop gerichte service.  <a href="../accounts/account-details.md">Meer informatie</a> |
| Functie | Overzicht van reizen | Wanneer u accountreizen opent, biedt het tabblad Overzicht een uitgebreide momentopname van uw actieve accountreizen, waarin de voortgang van uw account wordt beschreven aan de hand van cirkeldiagrammen en staafdiagrammen die voltooide accounts categoriseren en kwantificeren, en betrokkenheidsactiviteiten.  <a href="../dashboards/journeys-dashboard.md">Meer informatie</a> |
| Functie | Adobe Express-beeldbewerking | Met Snelle acties van Adobe Express kunt u eenvoudige bewerkingen (zoals uitsnijden en vergroten of verkleinen) uitvoeren op afbeeldingen voor een gepolijder uiterlijk in uw inhoud. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Meer informatie</a>  <p>Voor een uitgebreidere set ontwerpgereedschappen maakt deze integratie een volledige Adobe Express-licentie mogelijk in Journey Optimizer B2B edition. Met deze installatie wordt de volledige Adobe Express-gebruikersinterface toegankelijk in de werkruimte voor lokale middelen. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Meer informatie</a> |
| Functie | Intentiefilters voor het kopen van groepsrollen | Wanneer u uw intentsleutelwoorden indient, voorspelt het model van de Detectie van de Intentie een oplossing/product van belang met hoog genoeg vertrouwen die op de activiteit van een lood wordt gebaseerd. <a href="../admin/intent-data.md">Meer informatie</a> <p>Deze intentgegevens zijn beschikbaar voor het bepalen van het kopen van de rolvoorwaarden van de groep <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles"> Leer meer </a> |
| Verbetering | Ondersteuning van Marketo Engage-gebeurtenissen tijdens reizen | _luistert naar de 1} reisknoop van de Gebeurtenis {nu steunt twee gebeurtenissen van Marketo Engage op het personenniveau:_ bezoekt Web-pagina _en_ Vult vorm _uit._ <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Meer informatie</a> |
| Verbetering | Groepsfilters voor slimme Marketo Engage-lijsten kopen | Slimme lijsten weergeven en maken met groepsfilters kopen in Marketo Engage. Met deze toegevoegde filters kunt u de aanschaf van groepsleden in Marketo Engage-campagnes en -programma&#39;s onderdrukken en opnemen voor reizen van accounts binnen Journey Optimizer B2B edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Meer informatie</a> |
| Verbetering | Marketo Engage-lijstlidmaatschapsfilter voor reizen en rollen | In Journey Optimizer B2B, controleer het de lijstlidmaatschap van Marketo Engage als voorwaarde voor a _gespleten weg door mensen_ knoop helpen duplicatie in reisactiviteiten elimineren. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Meer informatie</a> <p> Voor het kopen van de malplaatjes van groepsrollen, gebruik lijstlidmaatschap als rolvoorwaarde. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Meer informatie</a> |
| Verbetering | Dashboard met overzicht van betrokkenheid | Dit dashboard wordt bijgewerkt om een uitgebreide weergave van de betrokkenheid te bieden. Het toont metriek in real time van rekening en individuele interactie door grafieken van de momentopnamecirkel en trendonthullende lijngrafieken in tijd. <a href="../dashboards/engagement-dashboard.md">Meer informatie</a> |

## 2024 releases

Vouw de volgende lijsten uit voor de functies en verbeteringen voor Journey Optimizer B2B edition die in 2024 zijn uitgebracht.

+++Opmerkingen bij de release van oktober 2024

**Datum van de Plaatsing**: 29 oktober, 2024

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Functie | Voorwaardelijke inhoud in e-mailsjablonen | Pas uw e-mailinhoud aan op basis van de gedrags- en profielkenmerken van de ontvanger, zowel voor de account als voor de lead. <p>Terwijl u een e-mail voor uw accountreis in de visuele ontwerpruimte voor e-mail ontwerpt, gebruikt u voorwaardelijke regels om meerdere varianten voor een inhoudscomponent te definiëren. <a href="../content/conditional-content.md">Meer informatie</a> |
| Functie | _voeg aan Lijst_ toe en _verwijder uit lijst_ personenacties in reizen | Pas uw e-mailinhoud aan op basis van de gedrags- en profielkenmerken van de ontvanger, zowel voor de account als voor de lead. <a href="../journeys/action-nodes.md">Meer informatie</a> |
| Functie | Inhoud beheren en component vergrendelen | Gebruik de functies voor contentbeheer om de inhoudonderdelen van een e-mailsjabloon te vergrendelen, zodat u zich aan goedgekeurde inhoudsontwerpen kunt houden. Als contentbeheer is geactiveerd in de e-mailsjabloon, kunnen marketers alleen de toegestane elementen wijzigen om deze op één lijn te houden met de inhoudsstrategie. <a href="../content/template-content-governance.md">Meer informatie</a> |
| Functie | Groepsfasen voor kopen | Wanneer u een model voor het opvoeren van een aangepaste inkoopgroep definieert en publiceert, kunt u de voortgang van de inkoopgroep bijhouden in de fasen van de levenscyclus van de inkoopgroep. Gebruik deze stappen om de volgende beste acties voor het kopen van groepsleden te identificeren. U vormt de overgangsregels en de wegknopen die de vooruitgang van het werkgebied bepalen en acties teweegbrengen die op veranderingen worden gebaseerd. <a href="../buying-groups/buying-group-stages.md">Meer informatie</a> |
| Verbetering | Nieuwe e-mailsjablonen die buiten de box vallen | De voorbeeldsjabloonbibliotheek bevat nu aanvullende e-mailsjablonen die zijn ontworpen voor B2B-marketers. Gebruik deze steekproefmalplaatjes als uitgangspunt en voeg uw eigen branding en overseinen toe. <a href="../content/email-templates.md#select-a-design-template">Meer informatie</a> |
| Verbetering | Aangepaste velden als persoonlijke kenmerken | Als u aangepaste persoonvelden hebt gedefinieerd in het accountpublieksschema in Experience Platform, zijn deze velden ook beschikbaar voor gebruik als persoonkenmerken in voorwaarden. Gebruik deze aangepaste kenmerken in: <li>De malplaatjes van rollen <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles"> leren meer </a></li><li>Splitste wegen door de knopen van de personenreis <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node"> leren meer </a></li> |
| Verbetering | E-mailkanaalinstellingen | E-mailinstellingen zijn nu zichtbaar in de Journey Optimizer B2B edition-interface. U kunt snel de huidige configuraties controleren en beheerders kunnen op _[!UICONTROL Edit settings]_klikken om rechtstreeks naar de instellingen in Marketo Engage te gaan en deze bij te werken volgens de vereisten van uw organisatie. <a href="../admin/configure-channels-emails.md">Meer informatie</a> |

+++

+++Release-aantekeningen van september 2024

**Datum van de Plaatsing**: 7 Oktober, 2024

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Verbetering | Centrale elementenbibliotheek | De verbeterde _centrale activa bibliotheek_ staat u toe om alle beeldactiva in uw instantie van Marketo Engage, over de werkruimten van de Studio van het Ontwerp te gebruiken. Er zijn ingebouwde instructies die voorkomen dat de Marketo Engage-middelen vanuit Journey Optimizer B2B edition worden bewerkt en dat bewerkingen worden verwijderd en verplaatst. Deze beveiligingsvoorzieningen zorgen ervoor dat de bronelementen (Marketo Engage Design Studio) behouden blijven en zorgen ervoor dat deze naadloos kunnen worden gelezen en hergebruikt in Journey Optimizer B2B edition.<p>Voor elementen die uitsluitend voor gebruik in Journey Optimizer B2B edition bestemd zijn, biedt een specifieke werkruimte volledige functies voor middelenbeheer. <a href="../content/marketo-engage-design-studio.md">Meer informatie</a> |
| Functie | Onlangs geopende elementen | De startpagina in de Journey Optimizer B2B edition-app bevat nu de sectie _[!UICONTROL Recently accessed]_, die een lijst bevat met de meest recent geopende elementen voor de markator of de beheerder. Met deze lijst kunt u rechtstreeks naar het element gaan waarmee u onlangs hebt gewerkt, zonder door een reeks elementpagina&#39;s te navigeren en te zoeken. <p>De lijst bevat aanvullende informatie over de wijziging, zodat u kunt bepalen welke elementen vanaf de laatste sessie verder moeten worden gewijzigd. Voor e-mailmiddelen wordt de accountreis weergegeven waar het e-mailmiddel wordt gebruikt. <a href="../home-page.md">Meer informatie</a> |
| Verbetering | Reis split node - reorder paths | Bij gesplitste padknooppunten wordt het filteren van paden geëvalueerd in de volgorde van boven naar beneden. Elke persoon of account gaat verder langs het eerste pad dat overeenkomt. U kunt de gedefinieerde paden opnieuw rangschikken door op de pijl-omhoog of -omlaag rechtsboven in elke padkaart te klikken om de paden hoger of lager in de lijst te plaatsen. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Meer informatie</a> |
| Verbetering | Knooppunt &quot;Journey split&quot; - Extra kenmerken van de activiteithistorie | Wanneer het gebruiken van voorwaarden om de weg te bepalen die voor een gespleten knoop door mensen filtreren, zijn er twee extra attributen: _Geopende e-mail_ en _werd geleverd e-mail_. Deze toevoegingen bieden meer flexibiliteit voor het filteren van mensen tijdens de reis op basis van e-mailactiviteiten. <a href="../journeys/journey-nodes.md#split-paths">Meer informatie</a> |

+++

+++Opmerkingen bij de release van augustus 2024

**Datum van de Plaatsing**: 29 augustus, 2024

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Functie | Gekoppeld publiek voor account gekoppeld | Genereer LinkedIn Ad-publiek via het publiek dat hoort bij de account om u te helpen lege rollen in uw inkoopgroepen te vullen. Door een reeks het kopen groepsfilters te bepalen, kunt u een LinkedIn Gelijke Publiek aan doelvooruitzichten handhaven die uw het kopen groepsparameters aanpassen. <p>Deze functie gebruikt Experience Platform Destination om bepaalde aspecten van de integratie te beheren. <a href="../data/linkedin-account-matched-audiences.md">Meer informatie</a> |
| Verbetering | De levenscyclus van de status voor visuele inhoudsfragmenten | Visuele fragmenten worden nu beheerd met behulp van een levenscyclus van de status. De fragmentstatus bepaalt de beschikbaarheid voor gebruik in een e-mail- of e-mailsjabloon en de wijzigingen die u daarin kunt aanbrengen. <p>Dankzij deze verbeterde workflow kunt u hergebruikte inhoud eenvoudig beheren op basis van uw promotie- en communicatieschema. <a href="../content/fragments.md#fragment-status-and-lifecycle">Meer informatie</a> |

+++
