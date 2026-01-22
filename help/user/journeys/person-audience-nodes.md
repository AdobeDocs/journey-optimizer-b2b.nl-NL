---
title: Persoonlijke audioniedagen
description: Vorm de knopen van het persoonpubliek met segment of op gebeurtenis-gebaseerde publiek om de punten van de persoonreis voor gerichte orchestratie in Journey Optimizer B2B edition te bepalen.
feature: Audiences
role: User
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie"
source-git-commit: f5170767a6df14874fab5de203264a5a5e3e245a
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Persoonlijke reisknooppunten

De _knoop van het publiek van 0&rbrace; persoon specificeert welke personenprofielen de reis ingaan._ Wanneer u [&#x200B; een persoonreis &#x200B;](./create-publish-journey.md#create-a-journey) creeert, begint de reis altijd met een knoop van het persoonpubliek die zijn input bepaalt. De knoop van het persoonpubliek kan één van twee types van publieksinput hebben: CDP segmenten of op gebeurtenis-gebaseerd lidmaatschap. Segment- en op gebeurtenissen gebaseerde publieksdefinities kunnen niet worden gecombineerd.

Gebruik één van de volgende inputopties voor de knoop van de personenreis van het publiek:

* **het publiek van het Profiel** - het segmentpubliek van het Gebruik dat in CDP wordt bepaald. Alle profielen die voor het publiek in aanmerking komen, worden als leden aan de reis toegevoegd. Nieuw kwalificerende profielen voor het segment worden toegevoegd aan de reis tijdens de dagelijkse [&#x200B; profielopname &#x200B;](#profile-ingestion) taken. Als een profiel niet meer voor het segment kwalificeert, wordt het **_niet_** verwijderd uit de reis.

* **het publiek van de Gebeurtenis** - Gebruik het kwalificeren gebeurtenissen om het publiek te bepalen. Deze gebeurtenissen worden bepaald in de knoopconfiguratie en moeten [&#x200B; gebeurtenissen gebruiken XDM die in de beleidsmontages &#x200B;](../admin/configure-aep-events.md) worden gevormd. Maximaal 10 gebeurtenissen worden ondersteund voor een op gebeurtenissen gebaseerd publiekslidmaatschap. Een profiel komt direct in aanmerking voor de reis na de eerste overeenkomende gebeurtenis die hun profiel maakt.

  >[!NOTE]
  >
  >Gebeurtenissen kunnen niet met profielkenmerken worden gecombineerd om de publieksdefinities te beperken. Verbeteringen om deze beperking aan te pakken zijn gepland voor toekomstige releases.

## Profielopname

In Journey Optimizer B2B edition worden de profielen tijdens een nachtelijke gebruikershandeling gesynchroniseerd met Experience Platform. Hoewel persoonlijke reizen op basis van gebeurtenissen profielen kunnen kwalificeren die geen deel uitmaken van een profiel of accountpubliek dat door Journey Optimizer B2B edition wordt ingenomen/in gebruik is, resulteert dit in opgenomen profielen die stabiel blijven, tenzij ze deel uitmaken van een publiek dat wordt gebruikt door een persoonlijke reis, accountreis of koopgroep. Als een profiel wordt opgenomen en later aan een publiek wordt toegevoegd, wordt het stitching van het profiel uitgevoerd en het profiel blijft synchroon met Experience Platform. De verbeteringen aan deze synchronisatie van profielgegevens zijn gepland voor toekomstige versies.

Een nieuw gemaakt profiel dat is opgenomen door een op een gebeurtenis gebaseerde reis van een persoon, beschikt mogelijk niet over de bijgewerkte profielinformatie op het moment van inname. Als bijvoorbeeld een profiel wordt gemaakt via een gebeurtenis voor het invullen van formulieren en een reis van een persoon deze opneemt van de gebeurtenis voor het invullen van formulieren die in aanmerking komen, worden de gegevens die in het formulier zijn ingediend, mogelijk nog niet gesynchroniseerd met het profiel op het moment dat de reis deze heeft ingepakt. Het resultaat kan onvolledige gegevens voor personalisatie zijn (zoals in e-mailinhoud). Verbeteringen in de synchronisatie van gebeurtenisprofielgegevens zijn gepland voor toekomstige releases.

Persoonlijke reizen op basis van gebeurtenissen kunnen profielen kwalificeren die nog steeds anoniem zijn/geen e-mailadressen bevatten en alleen ECID&#39;s bevatten. Dit gebeurt meestal wanneer u kwalificatielogica voor webpaginageactiviteit hebt. De te brede, op gebeurtenissen gebaseerde publiekslogica zou in de instantie kunnen resulteren die het 40 miljoen profielmaximum bereikt als teveel profielen kwalificeren. Beperk het mogelijke werkingsgebied van uw publiek om dit scenario te verhinderen.

>[!IMPORTANT]
>
>Tijdens het huidige bètaprogramma is het ideale gebruik van persoonlijke reizen om alleen profielen te kwalificeren die u ook gebruikt voor reizen voor rekening en het aanschaffen van groepsdefinities. Dit gebruik zorgt voor een volledig profiel dat synchroon blijft met Experience Platform.

## Het publiek instellen voor het knooppunt voor het personenpubliek

1. Klik op het knooppunt **[!UICONTROL Person audience]** .

   Deze actie toont de knoopeigenschappen op het recht.

   ![&#x200B; de knoop van de het publiekstrij van de Persoon &#x200B;](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"}

1. Kies het invoertype voor mensen die de reis betreden:

   * **[!UICONTROL Profile audience]**

     Kies de optie _[!UICONTROL Profile audience]_. Klik vervolgens op **[!UICONTROL Add profile audience]**.

     Selecteer in het dialoogvenster _[!UICONTROL Add audience]_&#x200B;een eerder gemaakt publiekssegment. Klik vervolgens op **[!UICONTROL Add audience]**.

     ![&#x200B; selecteer een profielpubliek voor de knoop &#x200B;](./assets/node-person-audience-add-audience-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Event audience]**

     Kies de optie _[!UICONTROL Event audience]_. Klik vervolgens op **[!UICONTROL Add event criteria]**.

     Voeg in het dialoogvenster _[!UICONTROL Edit event criteria]_&#x200B;een of meer gebeurtenissen toe die u wilt gebruiken voor de kwalificatie van het publiekslid. Voor elke gebeurtenis die u toevoegt, klikt u op **[!UICONTROL Add constraint]**&#x200B;om een gebeurteniskenmerk voor een overeenkomst te kiezen. Plaats de evaluatie die u voor een gelijke wilt gebruiken. U kunt meerdere beperkingen toevoegen die overeenkomen met de gebeurtenis.

     ![&#x200B; voegt gebeurtenissen toe en past criteria voor het kwalificeren van een persoonprofiel &#x200B;](./assets/node-person-audience-edit-event-criteria-dialog.png){width="700" zoomable="yes"} aan

     Klik op **[!UICONTROL Save]** wanneer de gebeurteniscriteria zijn gedefinieerd.

     Voor meer informatie over configuratie voor reis-gesteunde gebeurtenissen, zie [&#x200B; de Gebeurtenissen van de Ervaring beheren &#x200B;](../admin/configure-aep-events.md#manage-experience-events).
