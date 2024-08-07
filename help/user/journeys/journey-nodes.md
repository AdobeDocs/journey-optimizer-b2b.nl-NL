---
title: Rekeningjournalen
description: Leer over de knooppunttypes die u kunt gebruiken om uw rekeningsreizen te construeren.
feature: Account Journeys
exl-id: 4edb87d9-cdf8-47a4-968b-6dc76d97b89c
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 0%

---

# Rekeningknooppunten

Nadat u [ een rekeningsreis ](journey-overview.md#create-an-account-journey) creeert en [ het publiek ](journey-overview.md#add-the-account-audience-for-your-journey) toevoegt, bouwt de reis uit gebruikend knopen. De reiskaart biedt een canvas waar u meerdere stappen B2B-marketinggebruiksscenario&#39;s kunt maken.

Bouw de reis van uw rekening door de verschillende actie, gebeurtenis, en orchestration knopen als multi-step, dwars-kanaalscenario te combineren. Elk knooppunt van een puzzel vertegenwoordigt een stap langs een logisch pad.

## Account Audience-knooppunt

De ](journey-overview.md#add-the-account-audience-for-your-journey) knoop van het Publiek van de Rekening [ bepaalt het publiek van de inputrekening (die in Adobe Experience Platform wordt gecreeerd en wordt geleid) voor de reis. Dit knooppunt is altijd het eerste knooppunt en wordt standaard automatisch gemaakt.

## Handeling uitvoeren

Voer een handeling uit zoals een e-mail verzenden, de score wijzigen, enzovoort.

**Actie op rekeningen**: De actie wordt toegepast op alle mensen die deel van rekeningen op deze weg uitmaken.

**Actie op mensen**: De actie wordt toegepast op alle mensen op deze weg. Een handeling voor personen kan binnen het splitsingspad door personen worden gebruikt of door accounts worden gesplitst.

| Knooppuntcontext | Functie | Restricties |
| ------------ | -------- | ----------- |
| [ Mensen ](#add-a-people-action) | Toewijzen aan kopersgroep | Selecteer oplossingsrente <br/> Uitgezochte rol |
| | Verwijderen uit kopersgroep | Belang van oplossing selecteren |
| | SMS verzenden | SMS maken |
| | Toevoegen aan Marketo Engage-aanvraagcampagne | Selecteer de werkruimte van het Marketo Engage <br/> Uitgezochte campagne van het Verzoek |
| | Partitie met personen in Marketo Engage wijzigen | Nieuwe partitie |
| | Interessant moment persoon | Type <br/> Beschrijving |
| | Score wijzigen | Score naam <br/> Verandering |
| | E-mail verzenden | Creeer nieuwe e-mail <br/> Uitgezochte e-mail van Marketo Engage |
| [ Rekeningen ](#add-an-account-action) | Waarschuwing over verkoop verzenden | Selecteer oplossingsrente <br/> verzendt e-mail naar |
| | Account toevoegen aan (andere) reis | Reis live account selecteren |
| | Status van kopersgroep bijwerken | De Rente van de oplossing <br/> Status (vereist, maximaal 50 karakters) |
| | Account verwijderen uit (huidige) reis | Reis live account selecteren |
| | Interessant moment voor account | Het type (e-mail, mijlpaal, of Web) <br/> Beschrijving (facultatief) |
| | Gegevenswaarde account wijzigen | Selecteer attribuut <br/> Nieuwe waarde |

### Een accounthandeling toevoegen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Take an action]** .

   ![ voeg reisknoop toe - gespleten wegen ](./assets/add-node-action.png){width="400"}

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

| Knooppuntcontext | Functie | Restricties |
| ------------ | -------- | ----------- |
| [ Mensen ](#add-a-people-event) | Wijzigingen gegevenswaarde | Attribuut <br/> Extra beperkingen (facultatief) <br/> Onderbreking (facultatief) |
| | Klik op de koppeling in e-mail | E-mail <br/> Extra beperkingen (facultatief) <br/> Onderbreking (facultatief) |
| | Toegewezen aan kopersgroep | De rente van de oplossing <br/> Aanvullende beperkingen (facultatieve) <br/> (facultatieve) Onderbreking |
| | Hiermee opent u e-mail | E-mail <br/> Extra beperkingen (facultatief) <br/> Onderbreking (facultatief) |
| | Score is gewijzigd | De naam van de score <br/> Extra beperkingen (facultatieve) <br/> (facultatieve) Onderbreking van de score |
| | Verwijderd uit kopersgroep | De rente van de oplossing <br/> Datum van activiteit (facultatief) <br/> (facultatieve) Onderbreking |
| [ Rekeningen ](#add-an-account-event) | Status van kopersgroep wijzigen | De rente van de oplossing <br/> Aanvullende beperkingen (facultatieve) <br/> (facultatieve) Onderbreking |
| | Wijziging in de score Volledigheid | De rente van de oplossing <br/> Aanvullende beperkingen (facultatieve) <br/> (facultatieve) Onderbreking |
| | Account had interessant moment | Het type <br/> Extra beperkingen (facultatief) <br/> Onderbreking (facultatief) |
| | Wijziging van de betrokkenheidsscore | De rente van de oplossing <br/> Aanvullende beperkingen (facultatieve) <br/> (facultatieve) Onderbreking |
| | Waarde van accountgegevens wijzigen | Attribuut <br/> Extra beperkingen (facultatief) <br/> Onderbreking (facultatief) |

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

Indien nodig, bepaal de hoeveelheid tijd de reis op de gebeurtenis wacht. De reis eindigt na timeout.

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

**Gesplitste wegen door rekeningen**: De wegen die door rekeningen worden gesplitst kunnen zowel rekening als menselijke acties en gebeurtenissen omvatten, en deze wegen kunnen verder worden gesplitst.

_hoe werkt een gespleten weg door rekeningsknoop?_

* Wanneer u een gespleten wegknoop toevoegt en _Rekening_ kiest, omvat elke weg die wordt toegevoegd een eindknoop met de capaciteit om knopen aan elke rand toe te voegen.
* Het pad kan herhaaldelijk worden opgesplitst op rekeningen, bijvoorbeeld op geneste wijze. Een gesplitst pad bevat een optie om het standaardpad niet toe te voegen.
* Rekeningen/personen die niet in aanmerking komen voor een van de gesplitste paden gaan niet verder op de reis.
* Deze paden kunnen worden gecombineerd met een samenvoegknooppunt.

![ knoop van de Reis - gespleten wegen door rekening ](./assets/node-split-paths-account.png){width="700" zoomable="yes"}

**Gesplitste wegen door mensen**: De wegen die door mensen worden gesplitst en kunnen slechts personenacties omvatten, en deze wegen kunnen niet opnieuw worden gesplitst. Paden worden automatisch achter elkaar geplaatst.

_hoe werkt een gespleten weg door mensen knoop?_

* Pad splitsen op basis van knooppunten is gegroepeerde knooppunten. Ze worden automatisch samengevoegd, zodat alle mensen in het publiek verder kunnen gaan naar de volgende stap zonder de context te verliezen van de accounts waartoe ze behoren.
* Pad splitsen voor personen kan niet worden genest. U kunt geen gesplitst pad toevoegen voor personen op een pad dat zich in dit gegroepeerde knooppunt bevindt.
* Pad splitsen bevat een optie waarmee u geen standaardpad kunt toevoegen. Rekeningen/personen die niet in aanmerking komen, gaan niet verder op de reis.

![ knoop van de Reis - gespleten wegen door mensen ](./assets/node-split-paths-people.png){width="700" zoomable="yes"}

| Knooppuntcontext | Padvoorwaarden | Beschrijving |
| ------------ | -------- | ----------- |
| [ Mensen ](#add-a-split-path-by-people-node) | Persoonskenmerken | |
| | Gewijzigde gegevenswaarde (zoals filter op activiteitengeschiedenis) | |
| | Geopende e-mail | |
| | Op koppeling in e-mail klikken | |
| | Klikte koppeling op webpagina | |
| | Interessant moment | |
| | Lid van de kopersgroep | |
| [ Rekeningen ](#add-a-split-path-by-account-node) | Verandering in de Waarde van de Gegevens van de Rekening (zoals filter op activiteitengeschiedenis) | |

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

     ![ Gesplitste wegknoop - logica van het voorwaardenfilter ](./assets/node-split-conditions.png){width="700" zoomable="yes"}

   * Klik op **[!UICONTROL Done]**.

1. Als u meer paden wilt toevoegen, klikt u op **[!UICONTROL Add path]** en herhaalt u de vorige stappen om voorwaarden toe te voegen die van toepassing zijn op dit pad.

   U kunt ook elk pad labelen op basis van deze voorwaarden of de standaardlabels gebruiken.

1. (Optioneel) Voeg een standaardpad toe voor accounts die niet voor de andere paden zijn gekwalificeerd. Zo niet, dan eindigt de reis voor deze rekeningen.

   ![ Gesplitste eigenschappen van de wegknoop - andere rekeningen ](./assets/node-split-properties-other-accounts.png){width="700" zoomable="yes"}

### Een gesplitst pad toevoegen aan een knooppunt met personen

1. Navigeer naar de reiseditor.

1. Klik op de plusknop ( **+** ) op een pad en kies **[!UICONTROL Split paths]** .

   ![ voeg reisknoop toe - gespleten wegen ](./assets/add-node-split.png){width="300"}

1. In de knoopeigenschappen op het recht, kies **[!UICONTROL People]** voor de spleet.

1. Als u een voorwaarde wilt definiëren die van toepassing is op _[!UICONTROL Path 1]_, klikt u op **[!UICONTROL Apply condition]**.

1. Voeg in de Conditions-editor een of meer filters toe om het gesplitste pad te definiëren.

   * Filterkenmerken slepen en neerzetten vanuit de linkernavigatie en de overeenkomende definitie voltooien.

   * Pas de condities aan door de **[!UICONTROL Filter logic]** aan de bovenkant toe te passen. U kiest ervoor om alle kenmerkvoorwaarden of een voorwaarde aan te passen.

   * Klik op **[!UICONTROL Done]**.

1. Als u meer paden wilt toevoegen, klikt u op **[!UICONTROL Add path]** en herhaalt u de vorige stappen om voorwaarden toe te voegen die van toepassing zijn op dit pad.

   U kunt ook elk pad labelen op basis van deze voorwaarden of de standaardlabels gebruiken.

1. Ten slotte kunt u een standaardpad toevoegen voor personen die niet zijn gekwalificeerd voor de bovenstaande paden. Zo niet, dan eindigt de reis voor deze mensen

Wanneer u voorwaarden hebt bepaald voor elk weg dat u uw publiek op het personenniveau splitst, kunt u acties toevoegen die u mensen wilt nemen.

>[!NOTE]
>
>Wanneer u het publiek splitst naar personen, kunt u alleen acties voor personen toevoegen.

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

1. Selecteer in de eigenschappen van het samenvoegknooppunt de paden die u wilt samenvoegen.

   ![ knoop van de Reis - fusiepaden ](./assets/node-merge-select-paths.png){width="600" zoomable="yes"}

   U zou nu moeten zien dat de wegen worden samengevoegd zodat de rekeningen van de geselecteerde wegen aan één enkele weg combineren en door de reis kunnen blijven voortgaan.

1. Indien nodig, kunt u wegen unmerge door terug naar de eigenschappen van de fusieknoop te navigeren en checkbox voor om het even welke wegen te ontruimen die u wilt verwijderen.
