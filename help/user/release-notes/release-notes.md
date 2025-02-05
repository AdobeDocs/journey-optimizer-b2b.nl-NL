---
title: Aanvullende informatie
description: Nieuwste aanvullende informatie voor de B2B-editie van Adobe Journey Optimizer
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 9438b1472df38eddc3e1fa6cd5bc3992af0c9eec
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 4%

---

# Opmerkingen bij de release van Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en oplossingen voor problemen.

Journey Optimizer B2B edition is native gebaseerd op [!DNL Adobe Experience Platform] en erft van de nieuwste innovaties en verbeteringen. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest) {target="_blank"}.

Herzie de [ productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html) {target="_blank"} voor informatie over rechten, prestatiegaranties, en beperkingen.

## Opmerkingen bij de release oktober 2024 {#Oct-2024}

**de datum van de Versie**: 29 oktober, 2024

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Nieuwe functie | Voorwaardelijke inhoud in e-mailsjablonen | Pas uw e-mailinhoud aan op basis van de gedrags- en profielkenmerken van de ontvanger, zowel voor de account als voor de lead. <p>Terwijl u een e-mail voor uw accountreis in de e-mailontwerper ontwerpt, gebruikt u voorwaardelijke regels om meerdere varianten voor een inhoudcomponent te definiëren. <a href="../content/conditional-content.md">Meer informatie</a> |
| Nieuwe functie | _voeg aan Lijst_ toe en _verwijder uit lijst_ personenacties in reizen | Pas uw e-mailinhoud aan op basis van de gedrags- en profielkenmerken van de ontvanger, zowel voor de account als voor de lead. <a href="../journeys/action-nodes.md">Meer informatie</a> |
| Nieuwe functie | Inhoud beheren en component vergrendelen | Gebruik de functies voor contentbeheer om de inhoudonderdelen van een e-mailsjabloon te vergrendelen, zodat u zich aan goedgekeurde inhoudsontwerpen kunt houden. Als contentbeheer is geactiveerd in de e-mailsjabloon, kunnen marketers alleen de toegestane elementen wijzigen om deze op één lijn te houden met de inhoudsstrategie. <a href="../content/template-content-governance.md">Meer informatie</a> |
| Nieuwe functie | Groepsfasen voor kopen | Wanneer u een model voor het opvoeren van een aangepaste inkoopgroep definieert en publiceert, kunt u de voortgang van de inkoopgroep bijhouden in de fasen van de levenscyclus van de inkoopgroep. Gebruik deze stappen om de volgende beste acties voor het kopen van groepsleden te identificeren. U vormt de overgangsregels en de wegknopen die de vooruitgang van het werkgebied bepalen en acties teweegbrengen die op veranderingen worden gebaseerd. <a href="../buying-groups/buying-group-stages.md">Meer informatie</a> |
| Verbetering | Nieuwe e-mailsjablonen die buiten de box vallen | De voorbeeldsjabloonbibliotheek bevat nu aanvullende e-mailsjablonen die zijn ontworpen voor B2B-marketers. Gebruik deze steekproefmalplaatjes als uitgangspunt en voeg uw eigen branding en overseinen toe. <a href="../content/email-templates.md#select-a-design-template">Meer informatie</a> |
| Verbetering | Aangepaste velden als persoonlijke kenmerken | Als u aangepaste persoonvelden hebt gedefinieerd in het accountpublieksschema in het Experience Platform, zijn deze velden ook beschikbaar voor gebruik als persoonkenmerken onder bepaalde omstandigheden. Gebruik deze aangepaste kenmerken in: <li>De malplaatjes van rollen <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles"> leren meer </a></li><li>Splitste wegen door de knopen van de personenreis <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node"> leren meer </a></li> |
| Verbetering | E-mailkanaalinstellingen | E-mailinstellingen zijn nu zichtbaar in de Journey Optimizer B2B edition-interface. U kunt de huidige configuraties snel controleren en beheerders kunnen op _[!UICONTROL Edit settings]_klikken om rechtstreeks naar de instellingen in het Marketo Engage te gaan en deze bij te werken volgens de vereisten van uw organisatie. <a href="../admin/configure-channels-emails.md">Meer informatie</a> |

## Opmerkingen bij de release september 2024 {#Sept-2024}

**de datum van de Versie**: 7 Oktober, 2024

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Verbetering | Centrale elementenbibliotheek | De verbeterde _centrale activa bibliotheek_ staat u toe om alle beeldactiva in uw instantie van het Marketo Engage, over de werkruimten van de Studio van het Ontwerp te gebruiken. Er zijn ingebouwde instructies die voorkomen dat de Marketo&#39;s Engage van Journey Optimizer B2B edition worden bewerkt en dat bewerkingen worden verwijderd en verplaatst. Deze bescherming zorgt ervoor dat de bronactiva (de Studio van het Ontwerp van het Marketo Engage) worden gehandhaafd terwijl het toestaan van naadloos lees en hergebruik in Journey Optimizer B2B edition.<p>Voor elementen die uitsluitend voor gebruik in Journey Optimizer B2B edition bestemd zijn, biedt een specifieke werkruimte volledige functies voor middelenbeheer. <a href="../content/marketo-engage-design-studio.md">Meer informatie</a> |
| Nieuwe functie | Onlangs geopende elementen | De startpagina in de Journey Optimizer B2B edition-app bevat nu de sectie _[!UICONTROL Recently accessed]_, die een lijst bevat met de meest recent geopende elementen voor de markator of de beheerder. Met deze lijst kunt u rechtstreeks naar het element gaan waarmee u onlangs hebt gewerkt, zonder door een reeks elementpagina&#39;s te navigeren en te zoeken. <p>De lijst bevat aanvullende informatie over de wijziging, zodat u kunt bepalen welke elementen vanaf de laatste sessie verder moeten worden gewijzigd. Voor e-mailmiddelen wordt de accountreis weergegeven waar het e-mailmiddel wordt gebruikt. <a href="../home-page.md">Meer informatie</a> |
| Verbetering | Reis split node - reorder paths | Bij gesplitste padknooppunten wordt het filteren van paden geëvalueerd in de volgorde van boven naar beneden. Elke persoon of account gaat verder langs het eerste pad dat overeenkomt. U kunt de gedefinieerde paden opnieuw rangschikken door op de pijl-omhoog of -omlaag rechtsboven in elke padkaart te klikken om de paden hoger of lager in de lijst te plaatsen. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Meer informatie</a> |
| Verbetering | Knooppunt &quot;Journey split&quot; - Extra kenmerken van de activiteithistorie | Wanneer het gebruiken van voorwaarden om de weg te bepalen die voor een gespleten knoop door mensen filtreren, zijn er twee extra attributen: _Geopende e-mail_ en _werd geleverd e-mail_. Deze toevoegingen bieden meer flexibiliteit voor het filteren van mensen tijdens de reis op basis van e-mailactiviteiten. <a href="../journeys/journey-nodes.md#split-paths">Meer informatie</a> |

## Opmerkingen bij de release augustus 2024 {#Aug-2024}

**de datum van de Versie**: 29 augustus, 2024

Deze release bevat de volgende nieuwe mogelijkheden en verbeteringen:

| Type | Item | Beschrijving |
| ---- | ---- | ----------- |
| Nieuwe functie | LinkedIn-account met passend publiek | Genereer LinkedIn Ad-publiek via accountgroepen die aan bod komen, zodat u lege rollen in uw inkoopgroepen kunt vullen. Als u een set koopgroepsfilters definieert, kunt u een met LinkedIn overeenstemmende doelgroep bijhouden voor de doelvooruitzichten die overeenkomen met de parameters van uw inkoopgroep. <p>Deze functie gebruikt Experience Platform Doelen om sommige aspecten van de integratie te beheren. <a href="../data/linkedin-account-matched-audiences.md">Meer informatie</a> |
| Verbetering | De levenscyclus van de status voor visuele inhoudsfragmenten | Visuele fragmenten worden nu beheerd met behulp van een levenscyclus van de status. De fragmentstatus bepaalt de beschikbaarheid voor gebruik in een e-mail- of e-mailsjabloon en de wijzigingen die u daarin kunt aanbrengen. <p>Dankzij deze verbeterde workflow kunt u hergebruikte inhoud eenvoudig beheren op basis van uw promotie- en communicatieschema. <a href="../content/fragments.md#fragment-status-and-lifecycle">Meer informatie</a> |
