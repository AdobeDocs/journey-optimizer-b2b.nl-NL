---
title: Wacht knooppunten
description: Gebruik wachtknooppunten om de voortgang van de reis te pauzeren en de timing van de uitgang te regelen op duur, datum of geavanceerde dag- en tijdinstellingen.
feature: Account Journeys, Person Journeys
role: User
exl-id: fecab788-4e8e-490a-bcca-bc3ab43411d9
source-git-commit: 7a05e6aed76d15aa6d0d0a7dd244bf299d549782
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Wachten op knooppunten

Gebruik a _wacht_ knoop wanneer u de reisvooruitgang voor een bepaalde duur wilt pauzeren alvorens aan de volgende stap te bewegen.

U kunt de wachttijd op twee manieren definiëren:

* Een specifieke datum wanneer u naar de volgende knoop in de reis wilt vooruitgaan
* Een relatieve duur (aantal minuten, uren, dagen, weken of maanden)

## De wachttijdnode toevoegen

1. Navigeer naar de reiskaart.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Wait]** .

   ![ voeg reisknoop toe - wacht ](./assets/add-node-wait.png){width="440"}

1. In de knoopeigenschappen op het recht, plaats **[!UICONTROL Type]** van tijd te wachten alvorens de reis aan de volgende knoop in de weg te werk gaat.

   * **[!UICONTROL Duration]** - Bepaal een specifiek aantal dagen, uren, of notulen om tussen ingang en uitgang van de wachttijdknoop te verstrijken.
   * **[!UICONTROL Date]** - Geef een specifieke datum en tijd op voor het afsluiten.

   ![ knoop van de Reis - wacht ](./assets/node-wait.png){width="500"}

## Geavanceerde wachtinstellingen

Laat de **[!UICONTROL Must end on]** optie toe om een _geavanceerde wachtstap_ te vormen en ervoor te zorgen dat uw berichten mensen en rekeningsleden op het optimale moment bereiken. Deze configuratie geeft u nauwkeurige controle over wanneer een persoon of een rekening een wachttijdstap weggaat en aan de volgende knoop in de reis te werk gaat. In plaats van een vast aantal uren of dagen vanaf het binnenkomen tot het verlaten, kunt u acties plannen die op specifieke tijden en op specifieke dagen van de week plaatsvinden.

Met een _geavanceerd wacht stap_, bepaalt u **_wanneer_** de persoon of de rekening zou moeten weggaan, niet alleen hoe lang zij zouden moeten wachten.

![ knoop van de Reis - geavanceerd wacht stap ](./assets/node-wait-advanced.png){width="500"}

>[!AVAILABILITY]
>
>De geavanceerde wachttijdmontages zijn beschikbaar voor [!DNL Journey Optimizer B2B Edition] milieu&#39;s die provisioned op de [ vereenvoudigde architectuur ](../simplified-architecture.md) zijn.

### Wacht types

| Wachten, type | Beschrijving | Configuratie |
| --------- | ----------- | ------------- |
| **Specifieke tijd van dag** | Wacht tot een specifieke tijd (zoals 9 :00 AM) | Stel de tijd (uur en minuut) in. Sluit af bij de volgende instantie van die tijd (voor de geselecteerde tijdzone). |
| **Specifieke dag van week** | Wacht tot een bepaalde dag (zoals Dinsdag) | Selecteer een weekdag. Als er geen tijd is opgegeven, wordt de gebeurtenis om middernacht (voor de geselecteerde tijdzone) afgesloten op de volgende overeenkomende dag. |
| **waaier of combinatie van de Dag** | Houd de muisknop ingedrukt tot een van de opgegeven dagen binnen een bereik (zoals maandag-vrijdag) | Selecteer uw doeldagen. Als er geen tijd is opgegeven, wordt de gebeurtenis om middernacht (voor de geselecteerde tijdzone) afgesloten op de volgende overeenkomende dag. |
| **Tijd + de combinatie van de Dag** | Combineer zowel voor nauwkeurige het plannen (zoals Dinsdag bij 10 :00 AM) | Selecteer de doeldagen en stel de doeltijd in. Sluit bij de volgende dag/tijdinstantie (voor de geselecteerde tijdzone) af. |

### Algemene scenario&#39;s

De volgende scenario&#39;s illustreren hoe u typische scenario&#39;s op uw wachttijdknoopconfiguratie kunt toepassen:

+++E-mailaankomst tijdens kantooruren

**Scenario:** u aan klanten B2B in de handel brengt die e-mails bij het werk lezen. Je wilt dat alle e-mails tijdens de kantooruren aankomen.

**Oplossing:** vorm uw wachttijdstap om lood bij 9 :00 AM op weekdagen (maandag-vrijdag) vrij te geven. Geen kwestie wanneer een lood de wachttijdknoop ingaat, ontvangen zij uw e-mail tijdens kantooruren.

+++

+++Consistente verzendtijden voor dynamisch publiek

**Scenario:** Uw publiek verandert dagelijks aangezien de nieuwe rekeningen of de lood kwalificeren. U wilt dat alle leads de eerste e-mail tegelijkertijd ontvangen, ongeacht wanneer ze gekwalificeerd zijn.

**Oplossing:** plaats uw wachttijdstap om in een specifieke tijd (zoals 10 :00 AM) te beëindigen. Alle lood, of zij om middernacht of middag kwalificeerden, weggaan samen de wachtstap bij 10 :00 AM.

+++

+++SLA-compatibele vervolgtaken

**Scenario:** Uw team van de Verkoop heeft twee-zaken-dag SLA om op marketing-gekwalificeerde rekeningslood te volgen. Weekends tellen niet.

**Oplossing:** vorm de wachttijdstap om lood slechts op bedrijfsdagen vrij te geven. Een lead die op vrijdag is gekwalificeerd, wordt op maandag of dinsdag naar de follow-up gerouteerd, niet tijdens het weekend.

+++

### Voorbeelden van toegang en vertrek

| Wachten op configuratie | Account/lead-items | Afsluiten van account/lead |
| ------------------ | ------------------- | ------------------ |
| 9 :00 AM, Om het even welke dag | Maandag 11 :00 AM | Dinsdag 9 :00 AM |
| 9 :00 AM, Om het even welke dag | Maandag 7 :00 | Maandag 9 :00 AM |
| Dinsdag, geen tijd ingesteld | Vrijdag 3 :00 | Dinsdag 12 :00 AM |
| 10:00 AM, maandag-vrijdag | Zaterdag 2 :00 PM | Maandag 10 :00 AM |
| 10:00 AM, maandag-vrijdag | Woensdag 8 :00 AM | Woensdag 10 :00 AM |
