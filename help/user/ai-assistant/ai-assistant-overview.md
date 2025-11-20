---
title: AI Assistant in Journey Optimizer B2B edition
description: 'Versnel workflows met AI-assistent: ontvang productkennis, hulp bij het oplossen van problemen en operationele inzichten voor Journey Optimizer B2B Edition.'
feature: AI Assistant
role: User, Admin
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
source-git-commit: dc6495a65b89cb3993c4b72706298181a3b555db
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 2%

---

# AI Assistant in Journey Optimizer B2B edition

AI Medewerker in Journey Optimizer B2B edition wordt gecreeerd van de zelfde technologiestichting van [&#x200B; AI Medewerker in Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/ai-assistant/home){target="_blank"}. Het is een conversatie-ervaring die u kunt gebruiken om uw workflows in Adobe Journey Optimizer B2B edition te versnellen. U kunt AI Assistant gebruiken om meer inzicht te krijgen in de productmogelijkheden, problemen op te lossen of informatie te doorzoeken en operationele inzichten voor Journey Optimizer B2B edition te zoeken.

>[!IMPORTANT]
>
>Een overeenkomst aan de [&#x200B; gebruikersrichtlijnen &#x200B;](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) wordt vereist alvorens u AI Medewerker in Journey Optimizer B2B edition kunt gebruiken. Deze overeenkomst bevat ook de openbare bètaovereenkomst, zodat u aanvullende AI Assistant-functies kunt gebruiken wanneer deze in bètacapaciteit worden geïmplementeerd.

+++De interface van de gebruikersovereenkomst weergeven

![&#x200B; de eerste pagina van de gebruikersovereenkomst.](./assets/user-agreement-1.png)

![&#x200B; De laatste pagina van de gebruikersovereenkomst.](./assets/user-agreement-2.png)

+++

## AI Assistant-mogelijkheden in Journey Optimizer B2B edition

Om een antwoord op uw voorgelegde vragen te formuleren, vraagt de Medewerker van AI een gegevensbestand en vertaalt gegevens van het gegevensbestand in een leesbaar antwoord. Deze reactie is een interne vertegenwoordiging van onderliggende gegevens, en is ook genoemd geworden _&#x200B;**_Grafiek van de Kennis_**&#x200B;_ - een uitvoerig Web van concepten, gegevens, en meta-gegevens voor een bepaald antwoord. De Kennisgrafiek bestaat uit subgrafieken waarnaar wordt verwezen wanneer query&#39;s worden verzonden:

* Experience League-documentatie.
* Operationele artefacten, zoals schema&#39;s, velden, publiek en reizen.

Overweeg welk type van onderzoek u nodig hebt alvorens u een AI Hulp vraag voorlegt:

### Productkennis

Productkennis verwijst naar concepten en onderwerpen die zijn gebaseerd op de Journey Optimizer B2B edition-documentatie op Adobe Experience League. Vragen over productkennis kunnen nader worden omschreven in de volgende subgroepen:

| Productkennis | Voorbeelden |
| --- | --- |
| Aanbevolen lessen | <li>Wat is een koopgroep? <li> Een voorbeeld weergeven van een sjabloon voor het kopen van groepsrollen? |
| Openbare detectie | <li>Wat zijn de stappen om inkoopgroepen te creëren? <li>Hoe gebruik ik douanevelden in een het kopen rolmalplaatjes van een groep? |
| Problemen oplossen | <li>Waarom kochten we geen Groepen voor mijn reis gemaakt? <li>Waarom kan ik geen Experience Events vinden om naar te luisteren in de reis? |

### Operationele inzichten

_Operationele inzichten_ verwijzen naar antwoorden die AI Medewerker over uw voorwerpen van meta- gegevens (attributen, rekeningspubliek, dataflows, datasets, bestemmingen, rekeningsreizen, schema&#39;s, bronnen, het kopen groepsmalplaatjes, en oplossingsbelangen) produceert. Deze inzichten omvatten tellingen, raadplegingen, en lijneffect. Ze kijken niet naar gegevens in de sandbox.

* Welk publiek van de rekening heeft de grootste publieksgrootte en wat is die grootte?
* Hoeveel accountpubliek is er nooit gebruikt bij reizen?
* Welke actieve reizen gebruiken oplossingsrente _x_?

U kunt AI Assistant-vragen stellen over uw operationele inzichten in de volgende domeinen:

| Domein | Ondersteunde metagegevens | Niet-ondersteunde metagegevens |
| --- | --- | --- |
| Kenmerken/velden | <li>Zoeken naar kenmerknaam <li>Kenmerk - schemaverhouding <li>Kenmerk - gegevenssetrelatie <li>Kenmerk - publieksrelatie <li>Kenmerk - bestemmingsverhouding | <li>Kenmerkklasse <li>Audit <li>Vervalstatus <li>Labels <li>Waarde opgeslagen in kenmerken |
| Accountsoorten <br><br>**_Note:_** In de Journey Optimizer B2B edition-context kan AI Assistant alleen publieksvragen beantwoorden voor accountsoorten. In de Experience Platform-context kan AI Assistant alleen vragen beantwoorden voor Person Audiences. | <li>Aantal deelnemers <li>Type publiek (streaming of batch) <li>Aanmaakdatum/wijzigingsdatum <li>Activeringsstatus <li>Aantal leden <li>Soorten publiek dupliceren <li>Naam en id zoeken | <li>Overlap door publiek <li>Activering publiek <li>Audit <li>Maken/wijzigen <li>Labels <li>Kwalificatietrends van de lidstaten |
| Gegevensstromen | <li>Aantal gegevensstromen <li>Status DataFlow <li>Dataflow - relatie gegevensset <li>Dataflow - bronrelatie | <li>Maken/wijzigen <li>Dataflow-batch-relaties <li>Aantal hoogste profielen |
| Gegevenssets | <li>Aantal gegevenssets <li>Status profiel inschakelen <li>Aanmaakdatum/wijzigingsdatum <li>Gegevensset - schema-relatie <li>Gegevensset - publieksrelatie <li>Gegevensset - kenmerkrelatie <li>Dataset - gegevensstroomrelatie <li>Naam zoeken <li>Naam en id zoeken | <li>Audit <li>Gemaakt door <li>Gegevensset - batch-relatie <li>Maken en wijzigen van gegevensset <li>Gegevensgrootte <li>Aantal profielen <li>Aantal rijen <li>Waardezoekopdracht |
| Bestemmingen | <li>Gevormde doelaantallen <li>Doel - publieksrelatie <li>Relatie doelkenmerk | <li>Account instellen <li>Accountreferentie-informatie <li>Unieke profielen geactiveerd |
| Reizen (rekeningreizen) | <li>Aantal <li>Naam en id zoeken <li>Reisstatus <li>Aanmaakdatum/wijzigingsdatum | <li>Attributen - reisrelaties Audit <li>Maken/wijzigen <li>Gemaakt door |
| Schema&#39;s | <li>Schema aantallen <li>Aanmaakdatum/wijzigingsdatum <li>Schema - kenmerkrelatie <li>Schema - gegevenssetrelatie <li>Schema - publieksrelatie <li>Status profiel inschakelen <li>Naam zoeken <li>Naam en id zoeken | <li>Audit <li>Maken/wijzigen <li>Gemaakt door <li>Veldgroepen <li>Identiteiten <li>Identiteitsnaamruimten <li>Labels <li>Aantal profielen |
| Bronnen | <li>Rekentelling <li>Accountstatus <li>Actieve/inactieve gegevensstromen voor elke rekening <li>Source-connector - gegevensstroomrelatie <li>Source-account - gegevensstroomrelatie | <li>Accountverificatiegegevens <li>Metriek voor gegevensinvoer van account instellen <li>Aantal profielenBron - partijverhoudingen |
| Groepssjabloon voor kopen | <li>Aantal <li>Status <li>Rollen <li>Naam en id zoeken | <li>Rolregels |
| Belang van oplossing | <li>Aantal <li>Status <li>Belang van oplossing - De relatie van het Malplaatje van de Groep van de Kopen <li>Naam en id zoeken | <li>Belang van oplossing - Groepsrelatie voor kopers |

{style="table-layout:fixed"}

Voor vragen over operationele inzichten weerspiegelen de antwoorden mogelijk niet de huidige status van de gebruikersinterface. De gegevens die deze vragen ondersteunen, worden om de 24 uur bijgewerkt. Zo worden wijzigingen die gebruikers overdag aanbrengen in Real-Time CDP gesynchroniseerd met de gegevensopslag &#39;s nachts, waarna ze &#39;s ochtends beschikbaar komen voor vragen van gebruikers. Meld u aan bij een sandbox voor informatie over specifieke gegevens die betrekking hebben op objecten.

### Functiebereik

Momenteel is het bereik van AI Assistant als volgt:

* **de kennis van het Product**: De Medewerker van AI kan de vragen van de productkennis voor Real-Time Customer Data Platform en Adobe Journey Optimizer B2B edition beantwoorden.

* **Operationele inzichten**: U kunt AI Hulp vragen voor operationele inzichten voor de volgende gegevensvoorwerpen: attributen, rekeningspubliek, dataflows, datasets, bestemmingen, rekeningsreizen, schema&#39;s, bronnen, het kopen groepsmalplaatjes, en oplossingsbelangen.

### Privacy, veiligheid en bestuur

AI Assistant in Journey Optimizer B2B edition is gebouwd met privacy, beveiliging en bestuur als voorsprong. Bekijk de volgende informatie om over de klant te leren vertrouwen-geconcentreerde mogelijkheden die u van AI Medewerker kunt verwachten:

* De AI Assistant gebruikt momenteel geen persoonsgegevens, zelfs niet voor opleidingsdoeleinden.

* AI Assistant is niet op de hoogte van klantgegevens, zoals personen, accounts, mogelijkheden en inkoopgroepen.

* U moet expliciete toestemming hebben om met AI Medewerker in wisselwerking te staan.

   * Een beheerder kan toestemmingen plaatsen gebruikend [&#x200B; Toestemmingen UI &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} en [&#x200B; Admin Console &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/access-control/ui/browse){target="_blank"}.

   * De toestemmingen zijn korrelig en uw zandbakbeheerder kan vormen welke gebruikers verschillende vraagcategorieën (product kennisgebaseerde vragen met AI Medewerker of vragen over operationele inzichten) kunnen stellen.

* U kunt een logboek van uw vorige interactie met AI Medewerker met een beleid van het 30 dagbehoud bekijken.

* AI Assistant wordt geaard in sandboxspecifieke gegevens en openbare Adobe-documentatie wanneer wordt gereageerd op vragen van gebruikers. Gegevens worden niet gedeeld door sandboxen.

* Prompts die u aan AI Assistant verstrekt, worden niet gedeeld met andere klanten.

### Veelgestelde vragen

Hieronder volgt een lijst met antwoorden op veelgestelde vragen over AI Assistant in Journey Optimizer B2B edition.

**wordt de informatie van AI Medewerker verstrekt in real time?**

De gegevens in de antwoorden van AI Assistant worden dagelijks bijgewerkt. Deze cyclus houdt in dat de gegevens die in reacties zijn opgenomen, 24 uur ouder kunnen zijn dan de gegevens die op het moment van de reactie in de gebruikersinterface worden weergegeven.

**wat zijn de mogelijkheden van AI Medewerker?**

AI Assistant kan vragen over productkennis van Adobe beantwoorden en vragen beantwoorden over operationele inzichten van uw operationele artefacten.

**kan AI Medewerker informatie over klantengegevens verstrekken?**

Nee. AI Assistant heeft geen toegang tot klantgegevens en wordt daarom niet door AI Assistant bekeken of gebruikt.

**is mijn persoonlijke die informatie in de opleidingsgegevens van AI Medewerker wordt gebruikt?**

AI Assistant gebruikt geen persoonlijke gegevens voor opleidingsdoeleinden. Geef geen persoonlijke gegevens over uzelf (inclusief uw naam of contactgegevens) of andere partijen bij AI Assistant op.

## Volgende stappen

Als u een algemeen begrip hebt van AI Assistant, gaat u verder om AI Assistant in te schakelen en te gebruiken tijdens uw workflows. Raadpleeg de volgende documentatie voor meer informatie:

* [Toegang tot AI-assistent inschakelen](./enable-ai-assistant-access.md)
* [Richtlijnen voor vragen](./question-guidance.md)
* [AI-assistent gebruiken](./use-ai-assistant.md)
