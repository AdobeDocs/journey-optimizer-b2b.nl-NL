---
title: Luisteren naar een gebeurtenis
description: Meer informatie over het type Luisteren naar een gebeurtenisknooppunt dat u kunt gebruiken voor het orchestreren van uw accountreizen in Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 1%

---

# Luisteren naar een gebeurtenis

Voeg _toe luistert naar een gebeurtenis_ knoop om uw publiek naar de volgende stap in de rekeningsreis vooruit te bewegen wanneer een gebeurtenis voorkomt.

![ Video ](../../assets/do-not-localize/icon-video.svg){width="30"} [ bekijk de overzichtsvideo ](#overview-video)

>[!NOTE]
>
>U kunt dit knooppunttype niet toevoegen op gesplitste weg door mensen.

## Accountgebeurtenissen

Luister naar een gebeurtenis op basis van de account wanneer u de account voorwaarts wilt laten gaan tijdens de reis volgens gebeurtenissen die worden geactiveerd door accountactiviteiten.

### Gebeurtenissen en beperkingen

| Gebeurtenis | Restricties |
| ----- | ----------- |
| Account had interessant moment | Het type (E-mail, Mijlsteen, of Web) <br/> Extra beperkingen (facultatief): <li>Beschrijving</li><li>Bron</li><li>Datum van activiteit</li> <br/> Onderbreking (facultatief) |
| Waarde van accountgegevens wijzigen | Kenmerk <br/> Extra beperkingen (facultatief): <li>Nieuwe waarde</li><li>Vorige waarde</li><li>Datum van activiteit</li> <br/> Onderbreking (facultatief) |
| Wijziging in het werkgebied voor kopersgroepen | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe fase</li><li>Vorige fase</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| Status van kopersgroep wijzigen | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe status</li><li>Vorige status</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| Wijziging in de score Volledigheid | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe score</li><li>Vorige score</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| Wijziging van de betrokkenheidsscore | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe score</li><li>Vorige score</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |

### Een accountgebeurtenis toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Listen for an event]** .

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL Accounts]** voor het gebeurtenistype.

   ![ knoop van de Reis - luister aan gebeurtenissen op rekening ](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Selecteer een gebeurtenis in de lijst.

1. Klik op **[!UICONTROL Edit event]** en definieer details voor de gebeurtenis.

## Gebeurtenissen van Mensen

Luister naar een gebeurtenis op basis van mensen wanneer u de account op de reis vooruit wilt laten gaan volgens gebeurtenissen die worden geactiveerd door activiteiten van personen.

### Gebeurtenissen en beperkingen

| Invoertype | Gebeurtenis | Restricties |
| ---------- | ----- | ----------- |
| Journey Optimizer B2B | Toegewezen aan kopersgroep | De rente van de oplossing <br/><br/> Aanvullende beperkingen (facultatief): <li>Functie</li><li>Datum van activiteit</li><br/> Onderbreking (facultatief) |
| | Klik op de koppeling in e-mail | E-mail <br/><br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Koppelings-id</li><li>Is een mobiel apparaat</li><li>Apparaat</li><li>Platform</li><li>Browser</li><li>Is voorspelbare inhoud</li><li>Is beide activiteit</li><li>Bot-activiteitspatroon</li><li>Browser</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | Klik op de koppeling in SMS | E-mail <br/><br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Apparaat</li><li>Platform</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | Wijzigingen in gegevenswaarde | De attributen van de persoon <br/><br/> Aanvullende beperkingen (facultatief): <li>Nieuwe waarde</li><li>Vorige waarde</li><li>Reden</li><li>Bron</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | E-mail wordt geopend | E-mail <br/><br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Koppelings-id</li><li>Is een mobiel apparaat</li><li>Apparaat</li><li>Platform</li><li>Browser</li><li>Is voorspelbare inhoud</li><li>Is beide activiteit</li><li>Bot-activiteitspatroon</li><li>Browser</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | Verwijderd uit kopersgroep | De rente van de oplossing <br/> Datum van activiteit (facultatief) <br/> (facultatieve) Onderbreking |
| | Score is gewijzigd | De naam van de score <br/><br/> Aanvullende beperkingen (facultatief):<li>Wijzigen</li><li>Nieuwe score</li><li>Urgentie</li><li>Prioriteit</li><li>Relatieve score</li><li>Relatieve urgentie</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | SMS Bounces | Het bericht van SMS <br/><br/> Aanvullende beperkingen (facultatief): <li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| Marketo Engage | Bezoek de webpagina | Webpagina <br/> Selecteer een of meer overeenkomende Marketo Engage-pagina&#39;s. <br/><br/> Extra beperkingen (facultatief): <li>Querystring</li><li>IP-adres client</li><li>Referenter</li><li>Gebruikersagent</li><li>Zoekmachine</li><li>Zoekquery</li><li>Token</li><li>Browser</li><li>Platform</li><li>Apparaat</li><li>Datum van activiteit</li> |
| | Formulier invult | Formulier <br/> Selecteer een of meer Marketo Engage-formulieren die met elkaar overeenkomen.  <br/><br/> Extra beperkingen (facultatief): <li>Datum van activiteit</li><li>Querystring</li><li>IP-adres client</li><li>Referenter</li><li>Gebruikersagent</li><li>Platform</li><li>Apparaat</li><br/> Onderbreking (facultatief) |
| Adobe Experience Platform | Gebeurtenisdefinitie | Het type van gebeurtenis <br/><br/> Aanvullende beperkingen (facultatief): <li>Velden</li> <br/> Extra beperkingen (niet gesteund): <li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Time-out (optioneel) |

### Een gebeurtenis Personen toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Listen for an event]** .

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor het gebeurtenistype.

   ![ knoop van de Reis - luister aan gebeurtenissen op mensen ](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Selecteer een gebeurtenis in de lijst.

1. Klik op **[!UICONTROL Edit event]** en definieer details voor de gebeurtenis.

### Luisteren naar Marketo Engage-gebeurtenis

Als u webpagina&#39;s hebt gemaakt in uw verbonden Marketo Engage-exemplaar, kunt u een gebeurtenis activeren op basis van een bezoek aan of geen bezoek aan Marketo Engage-webpagina&#39;s en Marketo Engage-formulieren die niet zijn ingevuld.

1. Selecteer een knooppunt **[!UICONTROL Listen for an event]** in de editor voor de rit.

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor het gebeurtenistype.

1. Klik op de pijl voor de **[!UICONTROL Select people event]** -kiezer en schuif het menu naar de **[!UICONTROL Marketo Engage]** -sectie.

1. Selecteer een type van Markt-activiteit:

   * **[!UICONTROL Visits Web Page]**.
   * **[!UICONTROL Fills Out Form]**

   ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Edit event]** en definieer een of meer webpagina&#39;s die moeten overeenkomen en eventuele extra beperkingen voor de gebeurtenis.

   * (Vereist) Definieer in het dialoogvenster _[!UICONTROL Edit event]_de formulierbeperking **[!UICONTROL Web page]**of Vult uit. Gebruik **[!UICONTROL is]**(standaardwaarde) om overeen te komen op een of meer geselecteerde pagina&#39;s of formulieren. Gebruik **[!UICONTROL is not]**om overeen te komen op alle paginabezoeken/formulieren, met uitzondering van een of meer geselecteerde pagina&#39;s/formulieren. Of gebruik **[!UICONTROL is any]**om een overeenkomst te bereiken op een bezoek of ingevuld formulier op een Marketo Engage-webpagina.

   * (Optioneel) Klik op **[!UICONTROL Add constraint]** en kies het veld dat u voor de restrictie wilt gebruiken. Stel de operator en de waarde voor het veld in.

     ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     U kunt deze actie herhalen om extra gebiedsbeperkingen te omvatten zoals nodig.

   * Klik op **[!UICONTROL Done]** wanneer de beperkingen zijn gedefinieerd.

1. Indien nodig, plaats de **[!UICONTROL Timeout]** optie om de tijdspanne te beperken om op de gebeurtenis (zie [ een onderbreking aan een gebeurtenisknoop ](#add-a-timeout-to-an-event-node) toevoegen) te luisteren.

1. In de reisredacteur, voeg de volgende knoop toe om uit te voeren wanneer de gebeurtenis voorkomt.

### Luisteren naar een Experience Event

De beheerders kunnen op Adobe Experience Platform (AEP)-Gebaseerde gebeurtenisdefinities vormen, die Marketers toelaten om rekeningsreizen tot stand te brengen die op [ de Gebeurtenissen van de Ervaring van AEP ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent) reageren. Het gebruik van AEP-ervaringsgebeurtenissen voor reizen voor rekening is een proces in twee stappen:

1. [ creeer en publiceer een AEP gebeurtenisdefinitie ](../admin/configure-aep-events.md).

2. In een rekeningsreis, voeg a _toe luistert naar een gebeurtenis_ knoop, en selecteert een de gebeurtenisdefinitie van Experience Platform voor een op mensen-gebaseerde gebeurtenis.

_om een Gebeurtenis van de Ervaring in uw reis te omvatten:_

1. Selecteer een knooppunt **[!UICONTROL Listen for an event]** in de editor voor de rit.

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor het gebeurtenistype.

1. Klik op de pijl voor de **[!UICONTROL Select people event]** -kiezer en schuif het menu naar de **[!UICONTROL Adobe Experience Platform]** -sectie.

   ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Selecteer de gebeurtenis.

   Het gebeurtenistype wordt als leeg weergegeven in de details van het knooppunt.

   ![ geef de gebeurtenis ](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"} uit

1. Klik op **[!UICONTROL Edit event]** en definieer de gebeurtenistypen en eventuele extra beperkingen voor de gebeurtenis.

   * (Vereist) Definieer het gebeurtenistype in het dialoogvenster _[!UICONTROL Edit event]_. U kunt de operator **[!UICONTROL is]**default gebruiken om een of meer geselecteerde gebeurtenistypen overeen te laten komen. U kunt ook de operator **[!UICONTROL is not]**gebruiken om op alle gebeurtenistypen overeen te komen, met uitzondering van een of meer geselecteerde gebeurtenistypen.

   * (Optioneel) Klik op **[!UICONTROL Add constraint]** en kies het veld dat u voor de restrictie wilt gebruiken. Stel de operator en de waarde voor het veld in.

     ![ luistert naar een ervaringsgebeurtenis ](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >De beperkingen voor _datum van activiteit_ en _minimumaantal tijden_ worden niet gesteund.

     U kunt deze actie herhalen om extra gebiedsbeperkingen te omvatten zoals nodig.

   * Klik op **[!UICONTROL Done]** wanneer de beperkingen zijn gedefinieerd.

1. Indien nodig, plaats de **[!UICONTROL Timeout]** optie om de tijdspanne te beperken om op de gebeurtenis (zie [ een onderbreking aan een gebeurtenisknoop ](#add-a-timeout-to-an-event-node) toevoegen) te luisteren.

1. In de reisredacteur, voeg de volgende knoop toe om uit te voeren wanneer de gebeurtenis voorkomt.

1. Voltooi de resterende knopen voor uw reis en [ publiceer het ](./journey-overview.md).

   Wanneer de reis (gepubliceerd) levend is en _bereikt luistert naar een gebeurtenis_ knoop, begint het luisteren naar de Gebeurtenissen van de Ervaring AEP.

## Een time-out toevoegen aan een gebeurtenisknooppunt

Indien nodig, bepaal de hoeveelheid tijd de reis op de gebeurtenis wacht. De reis eindigt na een onderbreking tenzij u een onderbrekingspad bepaalt, waar u andere knopen kunt toevoegen.

1. Schakel de optie **[!UICONTROL Timeout]** in.

1. Selecteer de duur gedurende welke de reis op een gebeurtenis wacht om voor het uit te komen.

   U kunt ervoor kiezen om het pad hier te beëindigen of een andere actie uit te voeren door een ander pad in te stellen.

1. Schakel het selectievakje **[!UICONTROL Set timeout path]** in als u een nieuw pad wilt maken in de reis waar u acties en gebeurtenissen kunt toevoegen die van toepassing zijn op accounts wanneer de gebeurtenis niet plaatsvindt.

   ![ de gebeurtenisknoop van de Reis - vastgestelde onderbrekingspad ](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Video over overzicht

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on)
