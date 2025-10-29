---
title: Audience Agent voor B2B
description: Audience Agent B2B in Journey OptimizerB2B Edition maakt gebruik van intentanalyse en persona mapping om inkoopgroepen te maken en B2B-marketingworkflows te versnellen.
feature: Audiences, AI Assistant
role: User
source-git-commit: fa53458db4576af037dcf4b16ab1bf7b103b2fdd
workflow-type: tm+mt
source-wordcount: '3066'
ht-degree: 0%

---

# Audience Agent voor B2B

Aangedreven door [ Adobe Experience Platform Agent Orchestrator ](https://experienceleague.adobe.com/nl/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator), is Audience Agent B2B beschikbaar in Journey Optimizer B2B edition. Het gebruik van deze agent verbetert de efficiëntie en effectiviteit bij het verkennen en schalen van doelgroepen, versnelt het aanschaffen van groepen en naadloze workflows voor het activeren van de reis:

* **_geeft voorrang aan doelpubliek door intent_**: haal persona&#39;s binnen die op productintentie voor diverse publiek worden gebaseerd en stroomlijnt campagneplanning, die tijd die aan publieksbevestiging wordt doorgebracht.

* **_Leverage AI om het kopen groepen_** te ontdekken: AI van het gebruik, gestructureerde, ongestructureerde gegevens, en verenigde eerstepartijgegevens om het kopen groepsontdekking en verwezenlijking te stroomlijnen.

![ Audience Agent voor B2B op volledige paginamodus ](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>Om Audience Agent voor B2B te gebruiken, zijn er vereiste gegevensdefinities en afbeeldingen:<br/>
>
>* [ de gegevenstaxonomie/afbeelding van de Intentie ](../admin/intent-data.md)
>* [ XDM gebiedtaxonomie/afbeelding ](#xdm-data-prerequisites)

## Audience Agent for B2B-mogelijkheden

| Gebied | Wat doet het? | Bedrijfswaarde |
| ---- | ------------ | -------------- |
| Intentieanalyse | <li> De rekeningsintentsterkte van de meting (zoals laag, middelgroot, en hoog) voor specifieke producten. <li>Vergelijk de tendensen van de productrente in tijd (zoals hoogste producten in de laatste _n_ dagen). <li>Rekeningen identificeren die actief belangstelling tonen voor specifieke producten. <li>Oppervlaktebetrokkenheidspatronen die accountactiviteiten combineren met persoonlijke dekking. | <li>Help teams zich op het juiste moment te richten op de juiste accounts. <li>Verbetert pijpleidingskwaliteit door rekeningen met echte aankoopsignalen voorrang te geven. <li>Laat pro-actieve betrokkenheid toe alvorens de concurrenten handelen. |
| Persona-toewijzing | <li>Bepaal en rangschik de hoogste persona&#39;s door productintentie. <li>Identificeer persona&#39;s betrokken bij het kopen van één of meerdere producten. <li>De persona&#39;s van de kaart aan functionele rollen (zoals _Champion_, _de Maker van het Besluit_, en _Influencer_) met rechtvaardiging. <li>Valideer waarom een bepaalde persoon als kampioen wordt beschouwd. | <li>Zorgt ervoor dat het verkoopteam de echte besluitvormers en invloedrijvers betrekt. <li>Vermindert verspilde inspanning op laag-effect contacten. <li>Verhoogt de win-snelheden door de outreach af te stemmen op de dynamiek van de kopersmacht. |
| Evaluatie van inkoopgroep | <li>Beoordeel het kopen groepsgrootte (bijvoorbeeld, groepen met meer dan _n_ leden). <li>De persoonlijke dekking van de maatregel over rekeningen (bijvoorbeeld, onder _x_%). <li>Houd roldistributie en dekkingshiaten binnen het kopen groepen bij. <li>Markeer accounts met kampioenen die in recente deals zijn geïdentificeerd. | <li>Geeft dekkingshiaten weer die deals zouden kunnen blokkeren. <li>Versterkt multi-threading strategieën door volledige rolvertegenwoordiging te verzekeren. <li>Verbetert de gezondheid van deals via inzichten in de betrokkenheid op groepsniveau. |

## Vragen, voorbeelden

Deze snelle steekproeven tonen enkele manieren aan dat u de agent kunt gebruiken:

* Het venster Tendens weergeven: de oudste en meest recente update voor de intentie van het accountproduct per product.
* Maak voor `<product>` een lijst met inkoopgroepen met productintentie en scores.
* Voor `<product>`, maak een lijst van persona&#39;s en rollen met hun opportuniteitsmetriek (win tarief, lidmaatschapstarief, aantallen).
* Wat is voor accounts in `<industry>` de gemiddelde persoonlijke dekking van een account voor `<product>`?
* Welke rekeningen hebben een lage intentie voor om het even welk product maar hebben nog open kansen (het waard zijn te voeden)?
* Welke accounts hebben deze week nieuwe intentsignalen voor `<account_name>` toegevoegd?

## Concepten

| Concept | Toelichting |
| ------- | ----------- |
| Detectie van doelgroepen | Achter de schermen bekijkt de agent de intentsignalen van de eerste partij op basis van twee dingen: hoe betrokken mensen zijn bij je merk, en de soorten personen die ze vertegenwoordigen. In de analyse wordt de afgelopen 18 maanden van activiteit teruggezocht op het detecteren van de intentie van het product voor iedereen in de account, vooral in de periode voorafgaand aan een opportuniteitssluiting. Deze analyse helpt de agent om de personas te benadrukken het meest waarschijnlijk om de overeenkomst te beïnvloeden.<br/><br/> soms hebben de rekeningen niet al hun opportuniteitsgegevens in perfecte vorm, wat fijn is en de agent kan productintentie slechts van betrokkenheidspatronen nog ontdekken. |
| Persona | Persoonlijke personen vertegenwoordigen de typen personen die zich binnen een account engageren. De agent bouwt het door baantitel, functie, en anciënniteitsniveau te bekijken, en dan die informatie te normaliseren zodat is het verenigbaar over verschillende rekeningen. Op die manier kunt u in plaats van te verliezen in rommelige titels, snel zien of u besluitvormers, invloeden of steunrollen bereikt. Persoonlijke medewerkers helpen u te begrijpen wie interesse toont, niet alleen hoeveel interesse er is. <br/><br/> wanneer de agent karakters aan het kopen groepsrollen in kaart brengt, neemt het het type van geïdentificeerde die persoon, op hun baantitel, functie, anciënniteit, en een ander attribuut wordt gebaseerd u verkiest toe te voegen, en hen aan de rollen te richten die zij het meest waarschijnlijk in een aankoopbesluit, zoals _besluitvormer_, _beïnvloedingsreiziger_, of _kampioen_ spelen. Deze rollen zijn relevant voor het specifieke product in kwestie, zodat u kunt zien wie voor die kans het belangrijkst is. De agent toont ook dekking voor elke rol, die u helpt snel begrijpen welke rollen goed vertegenwoordigd zijn en waar er hiaten kunnen zijn om uw betrokkenheidsstrategie te vullen. |
| Groeprollen toewijzen aan inkoopordergroepen | Nadat persona&#39;s aan rollen in kaart worden gebracht, brengt u hen samen in een het kopen groep. Beschouw het als het volledige team binnen de account dat waarschijnlijk invloed zal hebben op of beslist over de aankoop. Elke rol (zoals _besluitvormer_, _invloedrijver_, of _kampioen_) voegt een stuk van het beeld toe, zodat u een duidelijke mening van het volledige comité hebt die de overeenkomst drijft. <br/><br/> wanneer u persona&#39;s aan het kopen groepsrollen in kaart brengt, neemt u het type van geïdentificeerde persoon, die op hun baantitel, functie, anciënniteit, en een ander attribuut wordt gebaseerd u verkiest om toe te voegen, en hen aan de rol te richten die zij hoogstwaarschijnlijk in een aankoopbesluit, zoals _besluitvormer_, _beïnvloedingsreiziger_, of _kampioen_ spelen. Deze rollen zijn relevant voor het specifieke product in kwestie, zodat u kunt zien wie voor die kans het belangrijkst is. De agent toont dekking voor elke rol, die u snel helpt begrijpen welke rollen goed vertegenwoordigd zijn en waar er hiaten kunnen zijn om uw betrokkenheidsstrategie te vullen. |
| Koopgroepen | Met kopersgroepen kunnen marketers de ware complexiteit van inkoopcomités beheren, niet de geïsoleerde leads of accounts. Adobe Journey Optimizer B2B edition biedt de tools (AI-gestuurde inzichten, rolgebaseerde reizen en volledigheid bijhouden) om structuur, personalisatie en analytische helderheid in dat proces te brengen, waardoor marketing en verkoop uiteindelijk beter op elkaar worden afgestemd ten opzichte van de inkomstenresultaten.<br/><br/> Creërend een het kopen groep is werkelijk over het brengen van drie zeer belangrijke dingen: het juiste publiek, de productcontext, en de het kopen groepsrollen. Hier volgt een stapsgewijze voorvertoning van hoe het werkt: <ol><li>**identificeer uw publiek** <ul><li>Ten eerste, ontdekt de agent de rekeningen die voor uw product het meest relevant zijn. Deze ontdekking omvat rekeningen die reeds interesse en rekeningen met potentieel tonen.<li>In deze accounts worden de personen (uw belangrijkste personen) geïdentificeerd die invloed kunnen uitoefenen op of deel kunnen uitmaken van het aankoopbesluit.<li>Deze optie kiest van de accounts naar de pagina: een accountlijst of een accountpubliek.</ul><li>**overweeg de productcontext**<ul><li>Vervolgens wordt gekeken naar het product of de oplossing waarop u zich richt, zodat de geïdentificeerde personen daadwerkelijk relevant zijn voor wat u wilt verkopen of promoten.<li>Het helpt ook om het even welke hiaten in dekking te benadrukken (misschien ontbreken bepaalde rollen voor het product) zodat weet u waar te om zich te concentreren.</ul> <li>**persona&#39;s van de Kaart aan het kopen van groepsrollen** <ul><li>Tot slot brengt de agent die mensen aan specifieke het kopen groeprollen, zoals besluitvormers, invloeden, en kampioenen in kaart.<li>Gebaseerd op deze afbeelding, kan de agent een het kopen groepssamenstelling voor u adviseren, die u kunt herzien, aanpassen of bevestigen.</ul> </ol> Wanneer deze drie componenten samenkomen, leidt het tot uw het kopen groep, volledig met liddetails, rollen, en inzichten klaar om te gebruiken. |
| Groepen kopen op reis | Binnen een reis, kan een koopgroep als centrale eenheid van orchestratie worden gebruikt, die marketers toestaat om ervaringen te ontwerpen die aan de dynamiek van de groep aanpassen eerder dan leden afzonderlijk te behandelen. Bijvoorbeeld, kunt u de volledige groep met gecoördineerd overseinen richten, terwijl ook het maken van rol-specifieke inhoud aan besluitvormers, invloeden, of eind - gebruikers. Aangezien de intent signalen en de stroom van betrokkenheidsgegevens binnen, reizen zich op groepsbereidheid, oppervlaktealarm voor verkoop kunnen vertakken wanneer de kritieke rollen in dienst nemen, of automatisch boompingsstappen teweegbrengen als de belangrijkste personen ontbreken. Deze stroom zorgt ervoor dat elk aanraakpunt (van e-mails tot advertenties op basis van account tot verkoopbereik) samenwerkt om de groep vooruit te helpen in het aankoopproces, de consensus te versnellen en de wrijving op het kooppad te verminderen. |
| Reizen in Journey Optimizer B2B edition | Een reis kan met of zonder een koopgroep worden gebouwd, maar de mate van nauwkeurigheid en impact verandert aanzienlijk:<ul><li>**zonder een het kopen groep**, worden de reizen typisch gebouwd rond rekeningen. Marketers kunnen signalen zoals intent, gedrag of product interest nog steeds gebruiken om de voedingsstromen en outreach te activeren. Deze methode werkt bij eenvoudiger bewegingen of wanneer u beperkte gegevens over een account hebt. Het risico bestaat echter dat de bredere groep belanghebbenden die invloed hebben op de deal, wordt genegeerd, wat de conversie kan vertragen of ruimte in betrokkenheid kan veroorzaken.<li>**met een het kopen groep**, worden de reizen georganiseerd rond de volledige reeks personen betrokken bij een aankoopbesluit. U kunt stappen uitlijnen op mijlpalen op groepsniveau (bijvoorbeeld wanneer de commissie een volledigheidsscore bereikt of collectieve betrokkenheid toont), terwijl u ook aanraakpunten voor elke rol kunt aanpassen. Met deze methode kunt u gecoördineerde multi-threaded betrokkenheid ontwerpen: een besluitvormer kan strategische ROI-inhoud ontvangen, terwijl invloedrijke gebruikers diepgaande duiken van producten ontvangen, en de verkoop wordt gealarmeerd wanneer kritieke rollen in werking treden. Door zowel de individuele als de collectieve reis in kaart te brengen, kunnen marketeers en verkopers consensusvorming versnellen en kansen efficiënter vooruit helpen. </ul> |
| Gebruik opportuniteitsgegevens om persona te detecteren | Om u het nauwkeurigste beeld te geven van wie en waar hun belangen liggen, nadert de agent persona rangschikking en productintentie volgens het volgende: <ul><li>Het beste geval scenario: Als u gegevens als _het Stadium van de Kans van 0} kunt verstrekken,_ de Dichte Datum van de Kans _, en een duidelijke_ Kans-aan-product Afbeelding _, kan de agent karakters per product vertrouwelijk rangschikken._<li>Deze rangschikking geeft een exact inzicht in betrokkenheid en interesse in de hele account. </ul>Maar de agent weet dat de gegevens niet altijd volledig zijn, wat OK is. Het omvat slimme fallbacks om dingen in beweging te houden:<ul><li>De agent analyseert het volume van de activiteiten, waardoor er meer gewicht wordt gegeven aan de recente activiteiten die gebruikmaken van tijdverlies.<li>Deze weging staat de agent toe om persona&#39;s te onderscheiden en te rangschikken, zelfs zonder volledige opportuniteitsgegevens. </ul>Wanneer het over het verbinden van kansen aan producten komt, is hier hoe de agent het behandelt:<ul><li>_Ideaal_: U verstrekt of helpt de agent creeert de mappinglijst.<li>_als niet beschikbaar_: de agent gebruikt vage aanpassing om de punten aan te sluiten.<li>_Geen verbinding bij allen_: De intentie van de agenteninfers product die op recente activiteiten voorafgaand aan de dichte datum wordt gebaseerd.</ul>Deze gelaagde benadering zorgt ervoor dat de agent nog zinvolle inzichten kan leveren, zelfs wanneer de gegevens niet perfect zijn. |
| Opportuniteitsanalyse | De agent kijkt naar historische opportuniteitsgegevens om te begrijpen welke factoren het sterkst een win voorspellen, en het gebruikt drie kerndimensies om dat te doen:<ol><li>Win tarief: toont hoe vaak de overeenkomsten met succes worden gesloten wanneer bepaalde mensen betrokken zijn. Als accounts met een specifiek persoonlijk patroon (zoals een technische beoordelaar of een besluitvormer op VP-niveau) vaker converteren, krijgt dat patroon meer gewicht. Deze informatie is een percentage van totale kansen, zoals kansen die worden gesloten of gewonnen.<li>Lidmaatschapspercentage: Hiermee wordt gemeten hoe vaak een personentype wordt getoond in verschillende mogelijkheden voor een bepaald product. Als bepaalde personen consequent in succesvolle deals worden getoond, geeft dit aan dat zij een cruciale rol spelen in het aankoopproces.<li>Persoonsinvloed: kwantificeert hoeveel een bepaalde persoon bijdraagt aan het resultaat, niet alleen of hij aanwezig is, maar hoe zijn betrokkenheid of activiteitsniveau correleert met wins.</ol>Samen helpen deze signalen om af te leiden welke personen de sterkste invloed hebben op de aankoopresultaten, zelfs wanneer de opportuniteitsgegevens onvolledig zijn. In tijd, staat het het systeem toe om high-impact persona&#39;s en patronen te oppervlakten die het meest voorspellend van overeenkomstensucces zijn, die dan rekeningsintent, persona afbeelding, en het kopen van groepsaanbevelingen informeren. |
| Intentie | Wanneer iemand een Web-pagina bezoekt of een e-mailverbinding met betrekking tot een product klikt, is het een signaal dat zij geinteresseerd zijn, en dat wordt genoemd _intent_.<br/><br/> de agent begint met een taxonomie, die fundamenteel een lijst van de producten van de klant en de sleutelwoorden is die hen beschrijven. Deze informatie helpt de agent te begrijpen waar elk stuk van inhoud of interactie over is.<br/><br/> daarna, gebruikt de agent die taxonomie om bezoekersactiviteit, zoals te etiketteren welke sleutelwoorden of producten hun acties betrekking hebben op.<br/><br/> dan, bekijkt de agent hoe diep iemand, zoals hoeveel pagina&#39;s aangaat zij of hoe vaak zij interactie aangaan. Deze informatie wordt gebruikt om de score van de afzonderlijke intentie te berekenen voor specifieke trefwoorden, producten of productcategorieën. Het bedekt elke intentscore in _Hoog_, _Medium_, of _Lage_ intent om op de rentesterkte te wijzen. (Lage intent: `<=0.2`, de intent van Medium: `0.2 < score <= 0.6`, Hoge intent: `0.6 < score <= 1`) <br/><br/> tot slot combineert de agent de intentscores van alle mensen van het zelfde bedrijf (rekening) om de algemene rekening-vlakke intent te zien, die toont welke producten of onderwerpen dat bedrijf het meest geinteresseerd in lijkt. |
| Rollen die een inkoopgroep beïnvloeden | Elke het kopen groep bestaat uit rollen die verschillend aan het aankoopbesluit, zoals _de Maker van het Besluit_, _Influencer_, _Champion_ bijdragen, en _Eind gebruiker_. Elke rol heeft een verschillende mate van effect.<br/><br/> de Makers van het Besluit hebben de meeste invloed en controleren typisch begrotingsgoedkeuringen. Influencers vormen evaluatie en aanbevelingen. Met Champions kunt u een interne consensus tot stand brengen, terwijl eindgebruikers de geschiktheid van het product valideren.<br/><br/> door u deze rollen te tonen, helpt de agent u begrijpen wie de het kopen beslissing drijft, waar uw betrokkenheid het sterkst is, en waar de dekkingshiaten zouden kunnen bestaan. Deze informatie laat u toe om zich op de rollen te concentreren die het belangrijkst voor dit product zijn. |
| Person- of roldekking | Voor om het even welk bepaald product, is er gewoonlijk een reeks zeer belangrijke rollen en persona&#39;s die gekend zijn om de aankoop (_N_ te beïnvloeden personas of rollen).<br/><br/> voor elke rekening, berekent de agent dekking door te controleren hoeveel van die _N_ rollen door minstens één persoon binnen die rekening worden vertegenwoordigd.<br/><br/> als alle _N_ rollen aanwezig zijn, heeft de rekening volledige dekking. Als slechts enkele rollen worden vertegenwoordigd, is de dekking gedeeltelijk.<br/><br/> in eenvoudige termen, rol en personadekkingsmaatregel hoe volledig uw het kopen groep voor een product is, die op wordt gebaseerd of alle belangrijke besluitvormers, beïnvloedende factoren, en kampioenen inbegrepen zijn. |

## XDM-gegevensvereisten

Audience Agent biedt inzichten in accounts met de intentie van de eerste partij voor producten en verwerkt persona&#39;s en rollen op basis van de gedefinieerde gegevens. Zorg ervoor dat de volgende vereiste gegevens zijn geconfigureerd voor het gebruik van Audience Agent-mogelijkheden:

### XDM-veldtoewijzing

<table>
  <tbody>
    <tr>
      <th>XDM-veld</th>
      <th>Entiteit</th>
      <th>Bedrijfsdefinitie</th>
      <th>Aanvullende details</th>
    </tr>
    <tr>
      <td>
        <p>
          <span> b2b.accountKey.sourceKey </span>
        </p>
      </td>
      <td>
        <p>
          <span> Profielen </span>
        </p>
      </td>
      <td>Account-id, gebruikt in samenvoeging tot opportuniteits-, gebeurtenis- en intentiegegevens</td>
      <td rowspan="2">De analyse van de kans {de Verkenning van de 0} Rekening <br/>
        <br/><br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> b2b.personKey.sourceKey </span>
        </p>
      </td>
      <td>
        <p>
          <span> Profielen </span>
        </p>
      </td>
      <td>Persoon-id, gebruikt in samenvoegingen met gebeurtenisgegevens om profielgegevens te maken</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> extendedWorkDetails.departementen </span>
        </p>
      </td>
      <td>
        <p>
          <span>  Profielen </span>
        </p>
      </td>
      <td>Functieafdeling van profiel/persoon</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Persona-toewijzing</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span> extendedWorkDetails.jobTitle </span>
        </p>
      </td>
      <td>
        <p>
          <span>  Profielen </span>
        </p>
      </td>
      <td>Functietitel van profiel/persoon gebruikt in persoonlijke berekening</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> person.name.firstName </span>
        </p>
      </td>
      <td>
        <p>
          <span > Profielen </span>
        </p>
      </td>
      <td>Voornaam van persoon, die door Audience Agent wordt gebruikt om namen in UI te tonen wanneer voldaan aan om het even welke criteria</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span> person.name.fullName </span>
        </p>
      </td>
      <td>
        <p>
          <span> Profielen </span>
        </p>
      </td>
      <td>Volledige naam van persoon, die door Audience Agent wordt gebruikt om namen in UI te tonen wanneer voldaan aan om het even welke criteria</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span> person.name.lastName </span>
        </p>
      </td>
      <td>
        <p>
          <span> Profielen </span>
        </p>
      </td>
      <td>Achternaam van de persoon die door Audience Agent wordt gebruikt om namen weer te geven in de gebruikersinterface wanneer aan een van de criteria wordt voldaan</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> accountKey.sourceKey </span>
        </p>
      </td>
      <td>
        <p>
          <span> Accounts </span>
        </p>
      </td>
      <td>Account-id, gebruikt in samenvoeging tot opportuniteits-, gebeurtenis- en intentiegegevens</td>
      <td>De analyse van de kans <br/> Exploratie van de Rekening</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> accountName </span>
        </p>
      </td>
      <td>
        <p>
          <span> Rekeningen </span>
        </p>
      </td>
      <td>Naam van account die door Audience Agent wordt gebruikt om in de gebruikersinterface weer te geven wanneer wordt voldaan aan de criteria die in de gebruikersquery worden voorgesteld</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Accountoverkenning</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> accountDescription </span>
        </p>
      </td>
      <td>
        <p>
          <span> Rekeningen </span>
        </p>
      </td>
      <td>Beschrijving van account/bedrijf dat door Audience Agent wordt gebruikt om filter toe te passen op accounts die zijn gebaseerd op gebruikersquery in gebruikersinterface </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> accountOrganization.industrie </span>
        </p>
      </td>
      <td>
        <p>
          <span>  Accounts </span>
        </p>
      </td>
      <td>De industrie van Rekening/Bedrijf die door Audience Agent wordt gebruikt om filter op rekeningen toe te passen die op gebruikersvraag in UI worden gebaseerd </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> accountBillingAddress.region </span>
        </p>
      </td>
      <td>
        <p>
          <span>  Accounts </span>
        </p>
      </td>
      <td>Factureringsadres van account/bedrijf dat door Audience Agent wordt gebruikt om filter toe te passen op accounts die zijn gebaseerd op gebruikersquery in UI </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> accountKey.sourceKey </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Account-id, gebruikt in samenvoeging tot opportuniteits-, gebeurtenis- en intentiegegevens</td>
      <td rowspan="2">
        <p>De Analyse van de opportuniteit <br/> de Exploratie van de Rekening</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> OpportunityKey.sourceKey </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Opportunity-id, gebruikt in verbindingen met accountgegevens</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> opportunityName </span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunity </span>
        </p>
      </td>
      <td>Naam van opportunity die wordt gebruikt door Audience Agent </td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Opportuniteitsanalyse</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> isWon </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Bepaalt of de opportuniteit wordt gewonnen (binair)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> opportunityDescription </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Beschrijving van de door Audience Agent gebruikte opportunity </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> OpportunityAmount </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Bedrag van $ betrokken bij Opportunity</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span> OpportunityType </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Type kans</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> opportunityStage </span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunity </span>
        </p>
      </td>
      <td>Stage of Opportunity (gesloten gewonnen of gesloten, verloren of een van de tussenstadia) </td>
      <td rowspan="4">
        <p>De analyse van de kans <br/> Exploratie van de Rekening</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> actualCloseDate </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Werkelijke gesloten datum van de opportuniteit</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> expectedCloseDate </span>
        </p>
      </td>
      <td>
        <p>
          <span> Opportunity </span>
        </p>
      </td>
      <td>Datum van opportuniteit verwacht</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> extSourceSystemAudit.createdDate </span>
        </p>
      </td>
      <td>
        <p>
          <span> Kans </span>
        </p>
      </td>
      <td>Aanmaakdatum voor deze mogelijkheid</td>
    </tr>
  </tbody>
</table>

### Taxonomiegegevens

Audience Agent maakt gebruik van de eerste-partijintentie die is gedetecteerd in Journey Optimizer B2B edition:

1. Voor het berekenen van intenties zijn taxonomiegegevens (klantproducten en bijbehorende trefwoorden) van klanten > Taxonomie vereist
1. Taxonomy data wordt gebruikt om gebeurtenisgegevens (activa etiketteren) te etiketteren. Deze gegevens geven inzicht in welke trefwoorden en producten bezoekers willen gebruiken op basis van hun gebeurtenisgegevens > Asset Labels 
1. Gelabelde elementen (gebeurtenisgegevens) worden gecombineerd met bezoekersgedrag (aantal bezochte pagina&#39;s) om een bezoekersintentie te bepalen op trefwoord-, product- en productcategorieniveau → Intentberekening
1. Intentscores op het niveau van het bezoekersprofiel worden samengevoegd op accountniveau om de accountintentie in een bepaald trefwoord, product en productcategorie > Intentaccount aggregeren te bepalen

De volgende gebieden worden vereist naast [ vormend de intenttaxonomie ](../admin/intent-data.md):

<table>
  <tbody>
    <tr>
      <th>XDM-veld</th>
      <th>Entiteit</th>
      <th>Bedrijfsdefinitie</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>persoonsprofiel</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Profiel </span>
        </p>
      </td>
      <td>Helpt een persoon (e-mail of b2b_person)-id te identificeren</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Profiel </span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>keyword_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Wordt gebruikt als een taxonomie om elementen te labelen (ervaringsgebeurtenissen, zoals geklikte e-mails, bezochte webpagina's)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> timestamp </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Wordt gebruikt voor tijd om back-up en incrementele uitvoering te maken</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> eventType </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Krijg het type van gebeurtenis aangezien de agent slechts vier gebeurtenissen verwerkt (<span> directMarketing.emailClicked, directMarketing.emailOpened, directMarketing.emailUnsubscribed, web.webpagedetails.pageViews) </span>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> directMarketing.mailingName </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Alleen ter referentie/boekhouding; informatie over de naam van de campagne</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> directMarketing.mailingKey.sourceID </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Alleen ter referentie/boekhouden; informatie over de bron-id waarvoor de e-mail bestemd is</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> directMarketing.mailingKey.sourceInstanceID <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Alleen ter referentie/boekhouding; informatie over de broninstantie waarvoor de e-mail bestemd is</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> directMarketing.mailingKey.sourceKey <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Wordt gebruikt om de e-mailinhoud op te halen uit het Marketo Engage-datacenter; het bestaat uit (SourceID@SourceInsatceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> directMarketing.mailingKey.sourceType <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Alleen ter referentie/boekhouding; informatie over het type bron of waar de bron afkomstig is </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Informatie over de bron waarvoor de e-mail bestemd is</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails.name <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Werkelijke URL voor ophalen van inhoud</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails.queryParameters </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Aanvullende queryparameter voor de URL waarmee de doelinhoud wordt opgehaald </td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails.isPersonalizedURL </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>alleen ter referentie/boekhouding</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails.webPageKey.sourceID <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Alleen ter referentie/boekhouden; informatie over de bron-id waarvoor de e-mail bestemd is</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails.webPageKey.sourceInstanceID <br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span> Gebeurtenis van de Ervaring </span>
        </p>
      </td>
      <td>Alleen ter referentie/boekhouding; informatie over de broninstantie waarvoor de e-mail is bestemd</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span> web.webPageDetails.webPageKey.sourceKey <br/>
          </span>
        </p>
      </td>
      <td>
        <span> Gebeurtenis van de Ervaring </span>
      </td>
      <td>Alleen ter referentie/boekhouden; het bestaat uit (SourceID@SourceInsatceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails.webPageKey.sourceType </span>
        </p>
      </td>
      <td>
        <span> Gebeurtenis van de Ervaring </span>
      </td>
      <td>Alleen ter referentie/boekhouden; informatie voor het type bron of waar de bron afkomstig is</td>
    </tr>
    <tr>
      <td>
        <p>
          <span> web.webPageDetails.webPageKey.URL </span>
        </p>
      </td>
      <td>
        <span> Gebeurtenis van de Ervaring </span>
      </td>
      <td>Wordt gebruikt om werkelijke URL op te halen als web.webPageDetails.name deze niet heeft.</td>
    </tr>
  </tbody>
</table>
