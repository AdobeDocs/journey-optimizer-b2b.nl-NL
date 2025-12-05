---
title: XDM-veldbeheer
description: Gebruik XDM gebiedbeheer om de gegevens te controleren die aan Journey Optimizer B2B edition beschikbaar zijn.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie van de vereenvoudigde architectuur"
source-git-commit: 7d57fa1154eceff81dedda7e9412a2d57ead3d6b
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---


# XDM-veldbeheer

De gebieden van het Gegevensmodel van de ervaring (XDM) zijn schemaelementen die gegevens aan de [!DNL Journey Optimizer B2B Edition] toepassing verstrekken. Gebruik XDM-velden als filters en beperkingen in reizen, inkoopgroepen en functies, zoals aanpassen van e-mail en voorwaardelijke inhoud.

Schema&#39;s definiëren velden op basis van standaard XDM-klassen. De standaard klassen XDM omvatten Individueel Profiel, BedrijfsRekening, en de Gebeurtenis van de Ervaring. Relationele schema&#39;s bepalen ook gebieden die u toestaan om gestructureerde gegevens te modelleren zo aan traditionele relationele gegevensbanken.

Adobe Experience Platform (AEP)-schema&#39;s bevatten gewoonlijk veel velden in complexe hiërarchieën. Het doorlopen van XDM-schemabomen kost tijd. Het XDM gebiedbeheer stroomlijnt gebiedsselectie door slechts gebieden te tonen relevant voor elke reis. Beheerders bepalen welke velden worden weergegeven voor makers van reizen. Beheerders kunnen velden ook instellen op alleen-lezen of bewerkbaar. Deze acties verbeteren de efficiëntie tijdens het reisontwerp.

Beheerders die XDM begrijpen en samenwerken met gegevensengineers of CDP (Customer Data Platform) gegevens modelleringsbelanghebbenden moeten de volgende stappen gebruiken om XDM-klassen voor [!DNL Journey Optimizer B2B Edition] te configureren.

>[!NOTE]
>
>Het XDM gebiedbeheer is beschikbaar voor de milieu&#39;s van Journey Optimizer B2B edition die op de [&#x200B; vereenvoudigde architectuur &#x200B;](../simplified-architecture.md) provisioned zijn.

## Access XDM-klassen

1. Kies in de linkernavigatie **[!UICONTROL Administration]** > **[!UICONTROL Configuration]** .

1. Klik op **[!UICONTROL XDM Classes]** in het middelste deelvenster.

   * Gebruik de tabbladen **[!UICONTROL Standard]** en **[!UICONTROL Relational]** om nieuwe velden toe te voegen en beschikbaar te maken in Journey Optimizer B2B edition.

   * Gebruik het **lusje van Gebeurtenissen** aan [&#x200B; uitgezochte specifieke Gebeurtenissen van de Ervaring van AEP en hun bijbehorende gebieden &#x200B;](./configure-aep-events.md) voor de knopen van de reisgebeurtenis te gebruiken.

## Veldselecties

>[!IMPORTANT]
>
>U kunt de veldselectie op elk gewenst moment bijwerken door nieuwe velden te selecteren of velden die u niet meer nodig hebt, uit te schakelen. Wanneer u een reis gebruikend dit schema publiceert, sluit u de schemastructuur. Het verwijderen of hernoemen van het schema, het toevoegen van nieuwe gebieden, of het veranderen van gebiedstypes wordt niet gesteund en kan reismislukkingen veroorzaken.

Gebruik de volgende richtlijn voor het maken van gebiedsselecties:

* U kunt nieuwe gebieden slechts toevoegen nadat een schema actief in een reis wordt gebruikt.
* Het schrappen van, het anders noemen van, of het veranderen van gebiedstypes kunnen kwesties van de reisfunctionaliteit veroorzaken. Wees voorzichtig bij het manipuleren van schema&#39;s.
* Wijzig de naam van schema&#39;s niet en verwijder ze niet en wijzig de sleutels in relationele schema&#39;s.

### Standaardklassen

In het _[!UICONTROL Standard]_&#x200B;lusje, kunt u_ Beheerde gebieden _uitgeven en_ Updatable gebieden _voor de standaardklassen:

* Beheerde velden worden weergegeven in reizen, inkoopgroepen en personalisatiefuncties.
* De updatable gebieden dienen als beperkingen voor het _Profiel van de Rekening van de Update_ en _de 3&rbrace; wegknopen van het Profiel van de Persoon van de Update &lbrace;._

![&#x200B; Standaard klassen tabel die XDM klassenconfiguratie &#x200B;](assets/xdm-standard.png){width="600" zoomable="yes"} tonen

De lijst bevat twee klassen:

* **[!UICONTROL XDM Individual Profile]**
* **[!UICONTROL XDM Business Account]**

De weergegeven klassengegevens omvatten:

* Aantal beheerde velden
* Aantal velden voor bijwerken
* Laatste updatetijd

Om gebieden van het verenigingsschema voor standaardXDM klassen te selecteren, klik de klassennaam om de _Beheerde de selectiedialoog van gebieden_ te openen, of _te klikken Meer menu_ ( **..**) pictogram om tussen _[!UICONTROL Managed fields]_&#x200B;en&#x200B;_[!UICONTROL Updatable fields]_ te kiezen.

![&#x200B; klik het Meer menupictogram om tussen beheerde gebieden en updatable gebieden te kiezen &#x200B;](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>Een gebied moet eerst _Beheerd_ zijn alvorens het _Updatable_ kan zijn. De _Updatable gebieden_ die u selecteert moeten in uw user-provided schema bestaan. Uw schema bevat mogelijk geen vereiste velden, behalve velden die door het systeem zijn gedefinieerd.

#### Beheerde velden

Wanneer u **[!UICONTROL Managed fields]** kiest, maakt de _Uitgezochte gebieden_ dialoog een lijst van alle configureerbare gebieden.

1. Selecteer maximaal 100 velden voor elke XDM-klasse.

   Gebruik het veld _[!UICONTROL Search]_&#x200B;om de weergegeven lijst op naam te filteren. Gebruik de schuifregelaar **[!UICONTROL Only show selected fields]**&#x200B;om de huidige selecties te bekijken.

   ![&#x200B; Beheerde dialoog van de gebiedsselectie voor standaardXDM klassen die configureerbare gebiedsopties tonen &#x200B;](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** om uw selecties te bevestigen.

#### Bijwerkbare velden

Alvorens u updatable gebieden vormt, moeten zij in een douane dataset verblijven. Voor een analyse van het werkschema van de douanedataset, zie [&#x200B; datasets creëren en gegevens &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data#){target="_blank"} invoeren, en de **[!UICONTROL Create dataset from schema]** optie gebruiken. Deze dataset wordt gebruikt om updatable gebieden te isoleren. Alle updatable gebieden moeten in deze dataset zijn.

Maak een gegevensset voor Individueel profiel en een andere voor Zakelijke account. Selecteer elke nieuwe dataset tijdens het configuratieproces:

1. Selecteer bij **[!UICONTROL Datasets]** de nieuwe gegevensbron die u hebt gemaakt.
1. Kies de gebieden van de geselecteerde dataset.

   ![&#x200B; Dialoog voor het selecteren van updatable gebieden van datasets in XDM schemaconfiguratie &#x200B;](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. Klik op **[!UICONTROL Save]** om de wijzigingen toe te passen.

### Relationele schema&#39;s

Met relationele schema&#39;s kunt u aangepaste gegevensklassen maken. Met toegang tot veelvoudige datasets, kunt u klassen tot stand brengen die specifiek aan uw gegevensbehoeften worden aangepast. Gebruik relationele schema&#39;s voor bedrijfsentiteiten zoals aankopen, licenties en registraties van gebeurtenissen bij reisbeslissingen en e-mailpersonalisatie. U kunt maximaal 50 schema&#39;s en maximaal 100 gebieden per schema selecteren.

Voor informatie over hoe u de geselecteerde gebieden voor geavanceerde e-mailverpersoonlijking kunt gebruiken, zie [&#x200B; verpersoonlijking van de Inhoud &#x200B;](../content/personalization.md#custom-datasets). Voor informatie over hoe u de geselecteerde gebieden voor reisbeslissing (gespleten wegen door rekening) kunt gebruiken, zie [&#x200B; Gegevens die van de Douane &#x200B;](../journeys/split-merge-paths-nodes.md#custom-data-filtering) filtreren. <!-- add link to split path by people in M 1.5 GA release -->

>[!NOTE]
>
>De [&#x200B; Relationele schema&#39;s &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) zijn beschikbaar voor [!DNL Journey Optimizer B2B Edition] als beperkte beschikbaarheidsversie. Data Mirror- en relationele schema&#39;s zijn beschikbaar voor [!DNL Journey Optimizer Orchestrated Campaigns] -licentiehouders. Relationele schema&#39;s zijn ook beschikbaar als een beperkte release voor [!DNL Customer Journey Analytics] -gebruikers, afhankelijk van uw licentie en functionaliteit. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

>[!NOTE]
>
>Deze functie biedt momenteel ondersteuning voor gebruiksgevallen van aangepaste objecten die betrekking hebben op accounts, met plannen om in de toekomst meer gebruiksgevallen voor objecten die buiten de box vallen, te ondersteunen.

U kunt relationele schema&#39;s maken met de schema-editor (ga naar **[!UICONTROL Data Management]** > **[!UICONTROL Schemas]** in de linkernavigatie).

Wanneer u een schema maakt voor gebruik met [!DNL Journey Optimizer B2B Edition] , zijn de volgende configuratiewaarden vereist:

* Gedrag: Opnemen
* Segmentatie: Ingeschakeld
* Relatietype: veel-op-één
* Referentieschema: B2B-account
* Vereiste velden: primaire sleutel, externe sleutel en versiedescriptor
* Bijbehorende dataset: Gedefinieerd en toegewezen aan het schema

Als u relationele schemavelden wilt selecteren voor gebruik in [!DNL Journey Optimizer B2B Edition] :

1. Selecteer het tabblad **[!UICONTROL Relational]** om uw schema&#39;s weer te geven.

   ![&#x200B; Relationele schema&#39;s lusje in de Redacteur van het Schema die bedrijfsentiteitgebieden voor Adobe Journey Optimizer B2B edition tonen &#x200B;](assets/xdm-relational.png){width="600" zoomable="yes"}

1. Klik op **[!UICONTROL Select relational XDM schema]**.

   >[!NOTE]
   >
   >In deze bètaeigenschapversie, slechts worden de _Rekening veel-aan-één Voorwerpen van de Douane_ gesteund.

1. Selecteer een relationeel schema en klik op **[!UICONTROL Next]** .

   >[!NOTE]
   >
   >In deze bètafunctieversie kunt u geen schema uit de lijst verwijderen nadat u het hebt geselecteerd.

   ![&#x200B; selecteer een relationeel schema in de dialoog &#x200B;](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. Voer een naamruimte in of gebruik de standaardnaamruimte. Klik op **[!UICONTROL Next]**.

   U kunt de naamruimte slechts eenmaal instellen en deze handeling niet omkeren.

   ![&#x200B; standaardnamespace in Create namespace dialoog &#x200B;](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. Controleer de velden voor het relationele schema.

   Klik het _pictogram van Info_ ![&#x200B; Info &#x200B;](../assets/do-not-localize/icon-info-light.svg) pictogram om de gebiedsmeta-gegevens te bekijken.

1. Selecteer de velden die u wilt inschakelen voor reizen en personalisatie.

   Het platform selecteert automatisch de volgende vereiste velden:

   * Externe sleutel
   * Primaire sleutel
   * Versiebeschrijving

   Gebruik het veld _[!UICONTROL Search]_&#x200B;om de weergegeven lijst op naam te filteren. Gebruik de schuifregelaar **[!UICONTROL Only show selected fields]**&#x200B;om de huidige selecties te bekijken.

   ![&#x200B; Uitgezochte gebieden voor het relationele schema in de dialoog &#x200B;](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.
