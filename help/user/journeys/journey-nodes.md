---
title: Rekeningjournalen
description: Meer informatie over de knooppunttypen die u kunt gebruiken voor het maken van uw accountreizen in Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: af72f5183cb1de56804340cbc9148de82faeca35
workflow-type: tm+mt
source-wordcount: '2337'
ht-degree: 0%

---

# Rekeningknooppunten

Nadat u [ een rekeningsreis ](journey-overview.md#create-an-account-journey) creeert en [ het publiek ](journey-overview.md#add-the-account-audience-for-your-journey) toevoegt, bouwt de reis uit gebruikend knopen. De reiskaart biedt een canvas waar u meerdere stappen B2B-marketinggebruiksscenario&#39;s kunt maken.

Bouw de reis van uw rekening door de verschillende actie, gebeurtenis, en orchestration knopen als multi-step, dwars-kanaalscenario te combineren. Elke knoop van een reis vertegenwoordigt een stap langs een logische weg. Gebruik de volgende knooppunttypes om een rekeningsreis te construeren:

* [Accountpubliek](#account-audience-node)
* [Handeling uitvoeren](#take-an-action)
* [Luisteren naar een gebeurtenis](#listen-for-an-event)
* [Paden splitsen](#split-paths)
* [Wachten](#wait)
* [Paden samenvoegen](#merge-paths)

## Account Audience-knooppunt

De ](journey-overview.md#add-the-account-audience-for-your-journey) knoop van het Publiek van de Rekening [ bepaalt het publiek van de inputrekening (die in Adobe Experience Platform wordt gecreeerd en wordt geleid) voor de reis. Dit knooppunt is altijd het eerste knooppunt en wordt standaard automatisch gemaakt.

## Handeling uitvoeren

Voer een handeling uit zoals een e-mail verzenden, een score wijzigen, toewijzen aan een inkoopgroep, enzovoort.

**Actie op rekeningen**: De actie wordt toegepast op alle mensen die deel van rekeningen op deze weg uitmaken.

**Actie op mensen**: De actie wordt toegepast op alle mensen op deze weg. Een handeling voor personen kan binnen het splitsingspad door personen worden gebruikt of door accounts worden gesplitst.

### Handelingen en beperkingen {#action-nodes}

| Knooppuntcontext | Handeling | Restricties |
| ------------ | ------ | ----------- |
| [ Mensen ](#add-a-people-action) | Toevoegen aan lijst | Selecteer de werkruimte van het Marketo Engage <br/> Naam van de Lijst |
| | Toevoegen aan Marketo Engage-aanvraagcampagne | Selecteer de werkruimte van het Marketo Engage <br/> Uitgezochte campagne van het Verzoek |
| | Toewijzen aan kopersgroep | Selecteer oplossingsrente <br/> Uitgezochte rol |
| | Partitie met personen in Marketo Engage wijzigen | Nieuwe partitie |
| | Score wijzigen | Score naam <br/> Verandering |
| | Interessant moment persoon | Type <br/> Beschrijving |
| | Verwijderen uit kopersgroep | Belang van oplossing selecteren |
| | Verwijderen uit lijst | Selecteer de werkruimte van het Marketo Engage <br/> Naam van de Lijst |
| | E-mail verzenden | Creeer nieuwe e-mail <br/> Uitgezochte e-mail van Marketo Engage |
| | SMS verzenden | SMS maken |
| [ Rekeningen ](#add-an-account-action) | Gegevenswaarde account wijzigen | Selecteer attribuut <br/> Nieuwe waarde |
| | Interessant moment voor account | Het type (E-mail, Mijlsteen, of Web) <br/> Beschrijving (facultatief) |
| | Account toevoegen aan (andere) reis | Reis live account selecteren |
| | Account verwijderen van reis | Reis live account selecteren |
| | Waarschuwing over verkoop verzenden | Selecteer oplossingsrente <br/> verzendt e-mail naar |
| | Het werkgebied van de kopersgroep bijwerken | Selecteer oplossingsrente <br/> Uitgezochte het kopen groepsstadium |
| | Status van kopersgroep bijwerken | Selecteer oplossingsrente <br/> Status (vereist, maximaal 50 karakters) |

### Een accounthandeling toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Take an action]** .

   ![ voeg reisknoop toe - neem een actie ](./assets/add-node-action.png){width="400"}

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL Accounts]** voor de actie.

1. Selecteer een actie in de lijst en stel de waarden voor de actie in.

   ![ knoop van de Reis - neem een actie op een rekening ](./assets/node-take-action-account.png){width="700" zoomable="yes"}

### Handeling Personen toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Take an action]** .

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor de actie.

1. Selecteer een actie in de lijst en stel de waarden voor de actie in.

![ knoop van de Reis - neem een actie op mensen ](./assets/node-take-action-people.png){width="700" zoomable="yes"}

## Luisteren naar een gebeurtenis

Verplaats uw publiek naar de volgende stap in de reis wanneer een gebeurtenis plaatsvindt.

* U kunt ook bepalen hoeveel tijd de reis wacht op deze gebeurtenis. De reis eindigt na een timeout.
* Bovendien kunt u ervoor kiezen andere knooppunten toe te voegen aan het time-outpad.

**luistert aan gebeurtenissen op rekeningen**: Als minstens één persoon van een rekening een gebeurtenis teweegbrengt, gaat de rekening vooruit naar de volgende stap op de reis.

**luistert aan gebeurtenissen op mensen**: De gebeurtenissen op mensen kunnen slechts op een rekeningsweg worden toegepast; het is niet beschikbaar voor een spleet door personenknoop.

### Gebeurtenissen en beperkingen {#event-nodes}

| Knooppuntcontext | Gebeurtenis | Restricties |
| ------------ | ----- | ----------- |
| [ Mensen ](#add-a-people-event) | Toegewezen aan kopersgroep | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Functie</li><li>Datum van activiteit</li><br/> Onderbreking (facultatief) |
| | Klik op de koppeling in e-mail | E-mail <br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Koppelings-id</li><li>Is een mobiel apparaat</li><li>Apparaat</li><li>Platform</li><li>Browser</li><li>Is voorspelbare inhoud</li><li>Is beide activiteit</li><li>Bot-activiteitspatroon</li><li>Browser</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | Klik op de koppeling in SMS | E-mail <br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Apparaat</li><li>Platform</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | Wijzigingen in gegevenswaarde | De attributen van de persoon <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe waarde</li><li>Vorige waarde</li><li>Reden</li><li>Bron</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | E-mail wordt geopend | E-mail <br/> Extra beperkingen (facultatief): <li>Koppeling</li><li>Koppelings-id</li><li>Is een mobiel apparaat</li><li>Apparaat</li><li>Platform</li><li>Browser</li><li>Is voorspelbare inhoud</li><li>Is beide activiteit</li><li>Bot-activiteitspatroon</li><li>Browser</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | Verwijderd uit kopersgroep | De rente van de oplossing <br/> Datum van activiteit (facultatief) <br/> (facultatieve) Onderbreking |
| | Score is gewijzigd | De naam van de score <br/> Aanvullende beperkingen (facultatief):<li>Wijzigen</li><li>Nieuwe score</li><li>Urgentie</li><li>Prioriteit</li><li>Relatieve score</li><li>Relatieve urgentie</li><li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| | SMS Bounces | Het bericht van SMS <br/> Aanvullende beperkingen (facultatief): <li>Datum van activiteit</li><li>Min. aantal keren</li><br/> Onderbreking (facultatief) |
| [ Rekeningen ](#add-an-account-event) | Account had interessant moment | Het type (E-mail, Mijlsteen, of Web) <br/> Extra beperkingen (facultatief): <li>Beschrijving</li><li>Bron</li><li>Datum van activiteit</li> <br/> Onderbreking (facultatief) |
| | Waarde van accountgegevens wijzigen | Kenmerk <br/> Extra beperkingen (facultatief): <li>Nieuwe waarde</li><li>Vorige waarde</li><li>Datum van activiteit</li> <br/> Onderbreking (facultatief) |
| | Wijziging in het werkgebied voor kopersgroepen | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe fase</li><li>Vorige fase</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| | Status van kopersgroep wijzigen | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe status</li><li>Vorige status</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| | Wijziging in de score Volledigheid | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe score</li><li>Vorige score</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |
| | Wijziging van de betrokkenheidsscore | De rente van de oplossing <br/> Aanvullende beperkingen (facultatief): <li>Nieuwe score</li><li>Vorige score</li><li>Datum van activiteit</li><br/> Time-out (optioneel) |

### Een accountgebeurtenis toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Listen for an event]** .

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL Accounts]** voor het gebeurtenistype.

   ![ knoop van de Reis - luister aan gebeurtenissen op rekening ](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Selecteer een gebeurtenis in de lijst.

1. Klik op **[!UICONTROL Edit event]** en definieer details voor de gebeurtenis.

### Een gebeurtenis Personen toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Listen for an event]** .

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor het gebeurtenistype.

   ![ knoop van de Reis - luister aan gebeurtenissen op mensen ](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Selecteer een gebeurtenis in de lijst.

1. Klik op **[!UICONTROL Edit event]** en definieer details voor de gebeurtenis.

### Een time-out toevoegen aan een gebeurtenisknooppunt

Indien nodig, bepaal de hoeveelheid tijd de reis op de gebeurtenis wacht. De reis eindigt na een timeout.

1. Schakel de schakeloptie voor de time-out in.

1. Selecteer de duur gedurende welke de reis op een gebeurtenis wacht om voor het uit te komen.

   U kunt ervoor kiezen om het pad hier te beëindigen of een andere actie uit te voeren door een ander pad in te stellen.

1. Schakel het selectievakje **[!UICONTROL Set timeout path]** in als u een nieuw pad wilt maken in de reis waar u acties en gebeurtenissen kunt toevoegen die van toepassing zijn op accounts wanneer de gebeurtenis niet plaatsvindt.

   ![ de gebeurtenisknoop van de Reis - vastgestelde onderbrekingspad ](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Paden splitsen

Splits de doelgroep op basis van filtervoorwaarden.

>[!NOTE]
>
>Er worden maximaal 25 paden ondersteund.

**Gesplitste wegen door rekeningen**: De wegen die door rekeningen worden gesplitst kunnen zowel rekening als menselijke acties en gebeurtenissen omvatten. Deze paden kunnen verder worden gesplitst.

_hoe werkt een gespleten weg door rekeningsknoop?_

* Wanneer u een gespleten wegknoop toevoegt en _Rekening_ kiest, omvat elke weg die wordt toegevoegd een eindknoop met de capaciteit om knopen aan elke rand toe te voegen.
* Het pad kan herhaaldelijk worden opgesplitst op rekeningen, bijvoorbeeld op geneste wijze. Een gesplitst pad bevat een optie om het standaardpad niet toe te voegen.
* Als een rekening/persoon niet in aanmerking komt voor een van de gesplitste paden, gaat hij niet verder op de reis.
* Deze paden kunnen worden gecombineerd met een samenvoegknooppunt.

![ knoop van de Reis - gespleten wegen door rekening ](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Gesplitste wegen door mensen**: De wegen die door mensen worden gesplitst en kunnen slechts personenacties omvatten. Deze paden kunnen niet opnieuw worden gesplitst en automatisch met elkaar worden verbonden.

_hoe werkt een gespleten weg door mensen knoop?_

* Pad splitsen op basis van knooppunten is gegroepeerde knooppunten. De paden worden automatisch samengevoegd, zodat alle mensen in het publiek verder kunnen gaan naar de volgende stap zonder hun accountcontext te verliezen.
* Pad splitsen voor personen kan niet worden genest. U kunt geen gesplitst pad toevoegen voor personen op een pad dat zich in dit gegroepeerde knooppunt bevindt.
* Een pad splitsen bevat een optie waarmee u een standaardpad kunt weglaten. Accounts/people without a match for a defined path are not move forward in the Journey.
* De gespleten weg door mensen steunt het gebruik van _rekening-persoon verhoudingen_, die u toestaat om mensen te filtreren die op hun rol (zoals contractant of voltijdwerknemer) worden gebaseerd zoals die in de rolmalplaatjes wordt bepaald.

![ knoop van de Reis - gespleten wegen door mensen ](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

### Padvoorwaarden {#path-conditions}

| Knooppuntcontext | Padvoorwaarden | Beschrijving |
| ------------ | --------------- | ----------- |
| [ Rekeningen ](#add-a-split-path-by-account-node) | Accountkenmerken | Attributen van het accountprofiel, waaronder: <li>Jaarlijkse ontvangsten</li><li>Stad</li><li>Land</li><li>Werknemersgrootte</li><li>Marktsegment</li><li>Naam</li><li>SIC-code</li><li>Staat</li> |
| | [!UICONTROL Special filters] > [!UICONTROL Has Buying Group] | Op de rekening worden leden van inkoopgroepen al dan niet beoordeeld aan de hand van een of meer van de volgende criteria: <li>Belang van oplossing</li><li>Status van kopersgroep</li><li>Complete score</li><li>Engagement Score</li> |
| [ Mensen ](#add-a-split-path-by-people-node) > [!UICONTROL People attributes only] | [!UICONTROL Person Attributes] | Attributen van het profiel van de persoon, met inbegrip van: <li>Stad</li><li>Land</li><li>Geboortedatum</li><li>E-mailadres</li><li>E-mail is ongeldig</li><li>E-mail is geschorst</li><li>Voornaam</li><li>Overgenomen deelstaatgebied</li><li>Functie</li><li>Achternaam</li><li>Mobiel telefoonnummer</li><li>Telefoonnummer</li><li>Postcode</li><li>Staat</li><li>Niet geabonneerd</li><li>Reden waarop geen abonnement is genomen</li> |
| | [!UICONTROL Activity history] > [!UICONTROL Email] | E-mailactiviteiten in verband met de reis: <li>[!UICONTROL Clicked link in email]</li><li>Geopende e-mail</li><li>Is per e-mail verzonden</li><li>Is per e-mail verzonden</li> Deze voorwaarden worden geëvalueerd aan de hand van een geselecteerd e-mailbericht uit een eerdere reis. |
| | [!UICONTROL Activity history] > [!UICONTROL Data Value Changed] | Voor een geselecteerd persoonkenmerk is een waardewijziging opgetreden. Deze wijzigingstypen zijn onder meer: <li>Nieuwe waarde</li><li>Vorige waarde</li><li>Reden</li><li>Bron</li><li>Datum van activiteit</li><li>Min. aantal keren</li> |
| | [!UICONTROL Activity history] > [!UICONTROL Had Interesting Moment] | Interesserende tijdactiviteit die in de bijbehorende instantie van het Marketo Engage wordt bepaald. Beperkingen zijn: <li>Mijlsteen</li><li>E-mail</li><li>Web</li> |
| | [!UICONTROL Special filters] > [!UICONTROL Member of Buying Group] | De persoon is al dan niet lid van de koopgroep, beoordeeld aan de hand van een of meer van de volgende criteria: <li>Belang van oplossing</li><li>Status van kopersgroep</li><li>Complete score</li><li>Engagement Score</li><li>Functie</li> |
| [ Mensen ](#add-a-split-path-by-people-node) > [!UICONTROL Account-person attributes only] | Rol in accountkenmerken | Aan de persoon wordt al dan niet een rol in de account toegewezen. Optionele beperkingen: <li>Rolnaam invoeren</li> |

### Een gesplitst pad toevoegen per accountknooppunt

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Split paths]** .

   ![ voeg reisknoop toe - gespleten wegen ](./assets/add-node-split.png){width="300"}

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL Accounts]** voor de spleet.

1. Als u een voorwaarde wilt definiëren die van toepassing is op _[!UICONTROL Path 1]_, klikt u op **[!UICONTROL Apply condition]**.

   ![ Gesplitste wegknoop - voeg voorwaarde ](./assets/node-split-properties-apply-condition.png){width="500"} toe

1. Voeg in de Conditions-editor een of meer filters toe om het gesplitste pad te definiëren.

   * Filterkenmerken slepen en neerzetten vanuit de linkernavigatie en de overeenkomende definitie voltooien.

   * Pas de condities aan door de **[!UICONTROL Filter logic]** aan de bovenkant toe te passen. U kiest ervoor om alle kenmerkvoorwaarden of een voorwaarde aan te passen.

     ![ Gesplitste wegknoop - de logica van de voorwaardenrekeningen ](./assets/node-split-conditions-accounts.png){width="700" zoomable="yes"}

   * Klik op **[!UICONTROL Done]**.

1. Als u meer paden wilt toevoegen, klikt u op **[!UICONTROL Add path]** en herhaalt u de vorige stappen om voorwaarden toe te voegen die van toepassing zijn op dit pad.

   U kunt ook elk pad labelen op basis van deze voorwaarden of de standaardlabels gebruiken.

1. Indien nodig wijzigt u de volgorde van de paden op basis van de gewenste prioriteit voor de splitsing.

   Het filtreren van de weg wordt geëvalueerd in top-down orde. Elke account gaat verder langs het eerste pad dat overeenkomt.

   Klik op de pijl-omhoog of -omlaag rechtsboven in elke padkaart om deze hoger of lager in de lijst met paden te plaatsen.

   ![ Gesplitste wegknoop - orde wegen ](./assets/node-split-reorder-paths-accounts.png){width="500" zoomable="yes"} opnieuw

1. Schakel de optie **[!UICONTROL Other accounts]** in om een standaardpad toe te voegen voor accounts die niet overeenkomen met de gedefinieerde paden. Zo niet, dan eindigt de reis voor deze mensen.

### Een gesplitst pad toevoegen aan een knooppunt met personen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Split paths]** .

   ![ voeg reisknoop toe - gespleten wegen ](./assets/add-node-split.png){width="300"}

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor de spleet.

1. Stel de **[!UICONTROL Attributes used for conditions]** in.

   * Kies **[!UICONTROL People attributes only]** om voorwaarden te gebruiken die betrekking hebben op het profiel van de persoon en de gebeurtenissen.
   * Kies **[!UICONTROL Account-person attributes only]** om voorwaarden te gebruiken die betrekking hebben op het rollidmaatschap van een persoon binnen een account.

1. Als u een voorwaarde wilt definiëren die van toepassing is op _[!UICONTROL Path 1]_, klikt u op **[!UICONTROL Apply condition]**.

1. Voeg in de Conditions-editor een of meer filters toe om het gesplitste pad te definiëren.

   * Sleep een van de personentekenmerken van de linkernavigatie naar een andere plaats en voltooi de overeenkomende definitie.

     >[!NOTE]
     >
     >Als u aangepaste persoonvelden hebt gedefinieerd in het accountpublieksschema in het Experience Platform, zijn deze velden ook beschikbaar voor gebruik als persoonkenmerken onder bepaalde omstandigheden.

   * Pas de condities aan door de **[!UICONTROL Filter logic]** aan de bovenkant toe te passen. U kiest ervoor om alle kenmerkvoorwaarden of een voorwaarde aan te passen.

     ![ Gesplitste wegknoop - de logica van de voorwaardenfilter ](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Klik op **[!UICONTROL Done]**.

1. Als u meer paden wilt toevoegen, klikt u op **[!UICONTROL Add path]** en herhaalt u de vorige stappen om voorwaarden toe te voegen die van toepassing zijn op dit pad.

   U kunt ook elk pad labelen op basis van deze voorwaarden of de standaardlabels gebruiken.

1. Indien nodig wijzigt u de volgorde van de paden op basis van de gewenste prioriteit voor de splitsing.

   Het filtreren van de weg wordt geëvalueerd in top-down orde. Elke persoon gaat langs de eerste weg die aanpast.

   Klik op de pijl-omhoog of -omlaag rechtsboven in elke padkaart om deze hoger of lager in de lijst met paden te plaatsen.

   ![ Gesplitste wegknoop - orde wegen ](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} opnieuw

1. Schakel de optie **[!UICONTROL Other people]** in om een standaardpad toe te voegen voor mensen die niet overeenkomen met de gedefinieerde paden. Zo niet, dan eindigt de reis voor deze mensen.

Wanneer u voorwaarden voor elk pad hebt gedefinieerd om uw publiek op personenniveau te splitsen, kunt u acties toevoegen die u aan personen wilt overnemen.

>[!NOTE]
>
>Wanneer u het publiek splitst naar personen, kunt u alleen acties voor personen toevoegen totdat de paden worden gesloten of samengevoegd.

## Wachten

Wacht een bepaalde duur voordat u naar de volgende stap gaat.

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Wait]** .

1. In de knoopeigenschappen op het recht, plaats **[!UICONTROL Duration]** van tijd te wachten alvorens de reis aan de volgende knoop in de weg te werk gaat.

![ knoop van de Reis - wacht ](./assets/node-wait.png){width="700" zoomable="yes"}

## Paden samenvoegen

Met dit knooppunt kunt u verschillende paden samenvoegen en samenvoegen.

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Split paths]** .

1. Klik op het gesplitste knooppunt om de eigenschappen ervan aan de rechterkant te openen.

1. Klik op [!UICONTROL Add path] om drie paden te maken.

1. Voeg een combinatie van handelingen en gebeurtenissen toe aan elk pad.

1. Klik op de plusknop ( **+** ) voor een van deze paden en kies **[!UICONTROL Merge]** in de weergegeven opties.

   ![ knoop van de Reis - fusiepaden ](./assets/node-plus-icon-merge-paths.png){width="400"}

1. Selecteer in de eigenschappen van de knooppunt Paden samenvoegen de paden die u wilt samenvoegen.

   ![ knoop van de Reis - fusiepaden ](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   Op dit punt worden de paden samengevoegd, zodat de accounts van de geselecteerde paden worden gecombineerd tot één pad dat door de rit kan gaan.

1. Indien nodig, kunt u de samenvoegen van wegen ongedaan maken door terug naar de eigenschappen van de de knooppunten van samenstellingswegen te navigeren en checkbox voor om het even welke wegen te ontruimen die u wilt verwijderen.
