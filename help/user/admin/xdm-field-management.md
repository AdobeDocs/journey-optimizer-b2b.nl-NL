---
title: XDM-veldbeheer
description: Gebruik XDM gebiedbeheer om de gegevens te controleren die aan Journey Optimizer B2B edition beschikbaar zijn.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie"
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---


# XDM-veldbeheer

De gebieden van het Gegevensmodel van de ervaring (XDM) zijn schemaelementen die gegevens aan de [!DNL Journey Optimizer B2B Edition] toepassing verstrekken. U gebruikt XDM-velden als filters en beperkingen in reizen, inkoopgroepen en functies, zoals aanpassen van e-mail en voorwaardelijke inhoud.

Schema&#39;s definiëren velden op basis van standaard XDM-klassen. De standaard klassen XDM omvatten Individueel Profiel, BedrijfsRekening, en de Gebeurtenis van de Ervaring. Relationele schema&#39;s bepalen ook gebieden die u toestaan om gestructureerde gegevens te modelleren zo aan traditionele relationele gegevensbanken.

Adobe Experience Platform (AEP)-schema&#39;s bevatten gewoonlijk veel velden in complexe hiërarchieën. Het doorlopen van XDM-schemabomen kost tijd. Het XDM gebiedbeheer stroomlijnt gebiedsselectie door slechts gebieden te tonen relevant voor elke reis. Beheerders bepalen welke velden worden weergegeven voor makers van reizen. Beheerders kunnen velden ook instellen op alleen-lezen of bewerkbaar. Deze acties verbeteren de efficiëntie tijdens het reisontwerp.

Beheerders die XDM begrijpen en samenwerken met gegevensengineers of CDP-betrokkenen (Customer Data Platform) voor gegevensmodellering volgen de procedures in deze handleiding.

>[!NOTE]
>[ Relationele schema&#39;s ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) zijn beschikbaar voor [!DNL Journey Optimizer B2B Edition] als beperkte versie. Data Mirror en relationele schema&#39;s zijn beschikbaar voor houders van een door Journey Optimizer geordende licentie voor campagnes. Relationele schema&#39;s zijn ook beschikbaar als een beperkte release voor Customer Journey Analytics-gebruikers, afhankelijk van uw licentie en functionaliteit. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

## XDM-klassen openen

Om het XDM gebied van het gebiedsbeheer te openen, navigeer aan **Configuraties** > VESTIGING > **klassen XDM**.

* U kunt nieuwe gebieden slechts toevoegen nadat een schema actief in een reis wordt gebruikt.
* Het schrappen van, het anders noemen van, of het veranderen van gebiedstypes kunnen kwesties van de reisfunctionaliteit veroorzaken. Wees voorzichtig bij het manipuleren van schema&#39;s.
* Wijzig de naam van schema&#39;s niet en verwijder ze niet en wijzig de sleutels in relationele schema&#39;s.

>[!IMPORTANT]
>U kunt de veldselectie op elk gewenst moment bijwerken door nieuwe velden te selecteren of velden die u niet meer nodig hebt, uit te schakelen. Zodra u een reis gebruikend dit schema publiceert, sluit u de schemastructuur. Het verwijderen of hernoemen van het schema, het toevoegen van nieuwe gebieden, of het veranderen van gebiedstypes wordt niet gesteund en kan reismislukkingen veroorzaken.

## Standaardklassen

In het Standaardklassenlusje, kunt u _Beheerde gebieden_ uitgeven en _Bijwerkbare gebieden_.

* Beheerde velden worden weergegeven in reizen, inkoopgroepen en personalisatiefuncties.
* De updatable gebieden dienen als beperkingen voor het _Profiel van de Rekening van de Update_ en _de 3} wegknopen van het Profiel van de Persoon van de Update {._

![ Standaard klassen tabel die beheerde en updatable gebieden voor XDM klassenconfiguratie tonen ](assets/xdm-standard.png){width="600" zoomable="yes"}

Ga als volgt te werk om velden in het vakschema voor standaard XDM-klassen te selecteren:

1. Ga naar **Beleid** > **Configuraties** > **Klassen XDM**.
1. Open het **Standaard** lusje. Kies een van de volgende klassen:

   * Afzonderlijk XDM-profiel
   * XDM Business Account

De tabel bevat informatie zoals:

* Aantal beheerde velden
* Aantal velden voor bijwerken
* Laatste updatetijd

Klik de klassennaam om de _Beheerde gebieden_ selectiedialoog te openen.

![ Beheerde dialoog van de gebiedsselectie voor standaardXDM klassen die configureerbare gebiedsopties tonen ](assets/xdm-standard-managed-fields.png){width="600" zoomable="yes"}

1. Klik op het menu **...** om te schakelen tussen _[!UICONTROL Managed fields]_en_[!UICONTROL Updatable fields]_ . In het dialoogvenster worden alle configureerbare velden weergegeven.
1. Selecteer maximaal 100 velden voor elke XDM-klasse.
1. Klik op **[!UICONTROL Save]** om uw selecties te bevestigen.

Gebruik het filter [!UICONTROL Only show selected fields] om alleen actieve velden weer te geven.

Voor _Updatable gebieden_, hebt toegang u tot een afzonderlijke dialoog die u gebieden van andere gegevensbronnen laat kiezen:

1. Selecteer in het vervolgkeuzemenu Datasets de gegevensbron die u wilt configureren.
1. Bewerk de velden uit de geselecteerde dataset.
1. Klik op **[!UICONTROL Save]** om wijzigingen toe te passen.

![ Dialoog voor het selecteren van updatable gebieden van datasets in XDM schemaconfiguratie ](assets/xdm-select-updateable.png){width="600" zoomable="yes"}

Het gebied moet eerst _Beheerd_ zijn alvorens zij _Updatable_ kunnen zijn. De _Updatable gebieden_ die u selecteert moeten in uw user-provided schema bestaan.

## Relationele schema&#39;s

Met relationele schema&#39;s kunt u aangepaste gegevensklassen maken. Met toegang tot veelvoudige datasets, kunt u klassen tot stand brengen die specifiek aan uw gegevensbehoeften worden aangepast.
Gebruik relationele schema&#39;s voor bedrijfsentiteiten zoals aankopen, licenties en registraties van gebeurtenissen bij reisbeslissingen en e-mailpersonalisatie. U kunt maximaal 50 schema&#39;s en maximaal 100 gebieden per schema selecteren.

![ Relationele schema&#39;s lusje in de Redacteur van het Schema die bedrijfsentiteitgebieden voor Adobe Journey Optimizer tonen ](assets/xdm-relational.png)

>[!NOTE]
>Deze functie biedt momenteel ondersteuning voor gebruik van aangepaste objecten die betrekking hebben op accounts, met plannen om in de toekomst meer gebruiksgevallen voor objecten die buiten de box vallen, te ondersteunen.

Creeer relationele schema&#39;s gebruikend de Redacteur van het Schema in **het Beheer van Gegevens** > **Schema&#39;s**.

Deze configuratiewaarden moeten worden opgenomen wanneer u een schema maakt voor gebruik met [!DNL Journey Optimizer B2B Edition] :

* Gedrag: Opnemen
* Segmentatie: Ingeschakeld
* Relatietype: veel-op-één
* Referentieschema: B2B-account
* Vereiste velden: primaire sleutel, externe sleutel en versiedescriptor
* Bijbehorende dataset: Gedefinieerd en toegewezen aan het schema

### Een relationeel schema maken

Voer de volgende stappen uit om velden te selecteren voor gebruik in [!DNL Journey Optimizer B2B Edition] :

1. Ga naar **Beleid** > **Configuraties** > **Klassen XDM**.
1. Open het **Relationele** lusje om uw schema&#39;s te bekijken.
1. Klik op **[!UICONTROL Select relational XDM schema]**.

   * In de bètaversie, slechts worden de _Rekening veel-aan-één Voorwerpen van de Douane_ gesteund.

1. Selecteer een relationeel schema en klik op **[!UICONTROL Next]** .

   * In de bètaversie kunt u een schema niet meer uit de lijst verwijderen als u het eenmaal hebt geselecteerd.

1. Voer een naamruimte in of gebruik de standaardnaamruimte. Klik op **[!UICONTROL Next]**.

   * U kunt de naamruimte slechts eenmaal instellen en deze handeling niet omkeren.

1. Controleer de velden voor het relationele schema. Klik het ![ pictogram van Info ](../assets/do-not-localize/icon-info-light.svg) [!UICONTROL Info] pictogram om de gebiedsmeta-gegevens te bekijken.
1. Selecteer de velden die u wilt inschakelen voor reizen en personalisatie. Het platform selecteert automatisch de volgende vereiste velden:

   * Externe sleutel
   * Primaire sleutel
   * Versiebeschrijving

1. Gebruik de schuifregelaar [!UICONTROL Only show selected fields] om een voorvertoning van de selecties weer te geven.
1. Gebruik de zoekbalk om velden op naam te filteren.
1. Klik op **[!UICONTROL Save]**.

## Gebeurtenissen

De Gebeurtenissen van de Ervaring van het gebruik en hun bijbehorende gebieden in reisbesluiten. U kunt maximaal 50 gebeurtenissen en maximaal 100 velden per gebeurtenis selecteren.

![ het lusje van Gebeurtenissen die de selectie van de Gebeurtenissen van de Ervaring en schemagebieden voor reizen en verpersoonlijking tonen ](assets/xdm-events.png){width="700" zoomable="yes"}

Klik op de naam van een gebeurtenis om details weer te geven en de geconfigureerde velden te bewerken.

Ga als volgt te werk om Experience Events en schemavelden te selecteren:

1. Ga naar **Beleid** > **Configuraties** > **Klassen XDM**.
1. Open **Gebeurtenissen** tabel.
1. Als u velden voor een gebeurtenis wilt selecteren, klikt u op **[!UICONTROL Select experience event]** .
1. Klik op de pagina Details op **[!UICONTROL Select event type]** .
1. Kies uw gebeurtenis in de lijst Gebeurtenis.
1. Klik op **[!UICONTROL Select]** om het dialoogvenster te sluiten.

   * In de bètaversie kunt u geselecteerde gebeurtenissen niet verwijderen.

1. Klik op **[!UICONTROL Select fields]**.
1. Gebruik de schuifregelaar [!UICONTROL Only show selected fields] om de huidige selecties weer te geven.
1. Selecteer de velden die u wilt gebruiken in [!DNL Journey Optimizer B2B Edition] . Klik op **[!UICONTROL Select]** om het dialoogvenster te sluiten.
1. Klik op [!UICONTROL Save].
