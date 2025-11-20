---
title: Persona-toewijzing
description: Leer hoe u persoonlijke toewijzingen instelt voor B2B-marketing. Wijs persoonattributen in Journey Optimizer B2B edition toe om rolmalplaatjes tot stand te brengen en het kopen groepgericht te optimaliseren.
feature: Setup, Buying Groups
role: Admin
source-git-commit: 278add74cc8d1aedd7809fd4675627f26501b0df
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 0%

---

# Persona-toewijzing

Personeelszaken zijn een belangrijk aspect in een op account gebaseerde marketing (ABM)-benadering omdat ze marketers helpen hun strategieën aan te passen aan de specifieke behoeften, voorkeuren en pijnpunten van individuen binnen doelaccounts. Marketers kunnen gedetailleerde profielen maken voor elke persoon, waaronder de achtergrond, verantwoordelijkheden, pijnpunten en voorkeurscommunicatiekanalen. Met deze definities, kunnen de beheerders persona&#39;s volgens persoonattributen in Journey Optimizer B2B edition vormen zodat de rolmalplaatjes gestroomlijnde en verenigbare rolvoorwaarden kunnen gebruiken die deze karakters vangen.

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
Definitie en gebruiksbeperkingen van personen:

* U kunt maximaal 20 personen opgeven die in de lijst van _[!UICONTROL Persona mapping]_worden gedefinieerd.
* Elke persoon kan maximaal vijf kenmerken in zijn definitie opnemen.
* Voor alle gedefinieerde personen kunt u maximaal tien verschillende persoonkenmerken gebruiken.

>[!BEGINSHADEBOX]

**geval van het Gebruik: de variaties van de baantitel**

Veel marketing- en verkoopteams gebruiken taaktitels om verschillende personen binnen een account te identificeren. Maar titels voor contacten kunnen inconsistent zijn en gebruiken talrijke variaties voor gelijkaardige rollen. Wanneer het bouwen van het kopen van de malplaatjes van groepsrollen, kan het vereisen dat u elke mogelijke verwante baantitel voor een bepaalde rol bepaalt. U kunt deze definities vereenvoudigen en mensen met vergelijkbare functies onder één afgeleid persoon brengen, die u vervolgens kunt gebruiken voor verschillende rolsjablonen voor het kopen van groepen.

Bijvoorbeeld, zou u een persoon kunnen vormen genoemd _Beheer van het Product_ en het bepalen gebruikend de attributen van de baantitel voor waarden van _Manager van het Product_, _Sr. De Manager van het product_, _Hogere Manager van het Product_, _PM_, _Sr. PM_, _Belangrijkste PM_, en _Belangrijkste Manager van het Product_. Dan, gebruik dit persona in een malplaatje van Rollen waar de voorwaarde op _Persoonlijk het Beheer van het Product_ aanpast. Gebruikend gevormde persoonlijkheid, wordt het creëren van elke rolmalplaatje gestroomlijnd en vereist geen ingewikkelde voorwaarde die met elke mogelijke baantitel kan aanpassen.

>[!ENDSHADEBOX]

## Heb toegang tot de gevormde karakters

1. Kies in de linkernavigatie **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** .

1. Klik op **[!UICONTROL Persona mapping]** in het tussenliggende deelvenster om de lijst met personen weer te geven.

   ![ heb toegang tot de gevormde persona&#39;s ](./assets/configuration-persona-mapping.png){width="800" zoomable="yes"}

   Van deze pagina, kunt u [ creëren ](#create-a-persona) uitgeven [, of ](#edit-a-persona) schrappen [ personas.](#delete-a-persona)

   De Persona-toewijzingslijst is ingedeeld als een tabel en geeft de meest recente bijgewerkte personen bovenaan weer (gesorteerd op _[!UICONTROL Last update]_). U kunt de getoonde lijst aanpassen door de_ montages van de Kolom _te klikken ( ![ montages van de Kolom ](../assets/do-not-localize/icon-column-settings.svg)) pictogram in de hoger-juiste hoek en het selecteren of ontruimen van kolomcheckboxes.

![ Kolommen aan vertoning in de lijst van de persona afbeelding ](./assets/configuration-persona-mapping-list-columns.png){width="300"}

1. Klik op de naam om de gegevens van een persoon te openen.

### Standaardvoorkeuren

De _lijst van de afbeelding van 0} Persona omvat vijf standaardkarakters die volgens de attributen van de baantitel worden bepaald._ U kunt elk van deze standaardpersona&#39;s bewerken op basis van de behoeften van uw organisatie:

| Persona | Functies |
| ------- | ---------- |
| CXO / EVP - CXO / Executive Vice - President | CEO, CIO, CTO, CMO, CFO, Executive Vice President of Strategy |
| SVP / VP - Senior Vice President / Vice President | SVP of Marketing, VP of Sales, SVP of Operations, VP of Product, VP of IT |
| Hoge directeur / directeur - Senior directeur / directeur | Directeur Engineering, Senior Director of Product, Director of Finance, Director of Customer Success |
| Senior Manager / Manager - Senior Manager / Manager | Senior Marketing Manager, IT Manager, Operations Manager, Sales Manager, HR Manager |
| Individuele contribuant - Individuele contribuant | Account Executive, Software Engineer, Marketing Specialist, Customer Success Vertegenwoordiger |
| Analyst - Analyst | Business Analyst, Data Analyst, Market Research Analyst, Financial Analyst, Operations Analyst |
| Ontwikkelaar - Ontwikkelaar | Front-end ontwikkelaar, Back-end Ontwikkelaar, Full-Stack Ontwikkelaar, Mobiele App Developer, DevOps Engineer |
| Professioneel personeel - Professioneel personeel | HR-specialist, juridisch adviseur, compliance officer, projectmanager, aanbestedingsspecialist |
| Consultant: consultant | Beheerconsultant, IT-consultant, bedrijfsprocesconsultant, marketingconsultant |
| Overige | Specialist, onafhankelijke adviseur, Freelance Consultant, onderwerp deskundige |

### Filteren op List

Als u de gewenste persoon wilt zoeken, typt u een tekstreeks in de zoekbalk die overeenkomt met de naam van de persoon,

![ Filter de getoonde persona afbeeldingen ](./assets/configuration-persona-mapping-search.png){width="700" zoomable="yes"}

## Een persona maken

1. Kies in de linkernavigatie **[!UICONTROL Administration]** > **[!UICONTROL Configuration]** .

1. Klik op **[!UICONTROL Persona mapping]** in het middelste deelvenster.

1. Klik op **[!UICONTROL Create persona]**.

1. Voer een unieke eigenschap **[!UICONTROL Name]** en **[!UICONTROL Description]** (optioneel) in voor de persoon.

   ![ creeer een persona afbeelding ](./assets/configuration-persona-mapping-new.png){width="700" zoomable="yes"}

1. Selecteer de kenmerken die u wilt gebruiken voor het afstemmen van de persoon.

   * Klik op **[!UICONTROL Select person attributes]**.

   * Selecteer in het dialoogvenster het selectievakje voor elk kenmerk dat u wilt toewijzen (maximaal vijf).

     U kunt de getoonde lijst aanpassen door de _montages van de Kolom_ ( ![ montages van de Kolom ](../assets/do-not-localize/icon-column-settings.svg)) te klikken pictogram in de hoger-juiste hoek.

     Als u de kenmerkenlijst op naam wilt filteren, voert u een tekstreeks in op de zoekbalk. U kunt het _pictogram van de Filter_ ( ![ pictogram van de Filter ](../assets/do-not-localize/icon-filter.svg)) bij de bovenkant links ook klikken om de getoonde lijst door type, _Standaard_ of _Douane_ te filtreren.

     ![ Uitgezochte de dialoog van persona attributen ](./assets/configuration-persona-mapping-select-attributes.png){width="700" zoomable="yes"}

   * Klik op **[!UICONTROL Save]**.

     De geselecteerde kenmerken worden ingevuld in de sectie _[!UICONTROL Persona attributes]_.

1. Voer voor elk kenmerk de door komma&#39;s gescheiden waarden in die u voor het kenmerk wilt gebruiken.

   In plaats van een waarde kunt u ook een vraag toevoegen die kan worden gebruikt om een overeenkomst te identificeren. U kunt bijvoorbeeld

1. Klik op **[!UICONTROL Submit]**.

## Een persona bewerken

Klik op de naam van de persoon om de gegevens voor de persoon te openen en te bewerken.

U kunt de naam of beschrijving wijzigen, kenmerken toevoegen of de kenmerkwaarden bijwerken. Klik op **[!UICONTROL Submit]** wanneer de wijzigingen zijn voltooid.

## Een persona verwijderen

Het schrappen van een persona verwijdert het uit de _Persoonlijke afbeelding_ lijst en het is niet meer beschikbaar voor gebruik in rolmalplaatjes.

1. Zoek op de pagina _[!UICONTROL Persona mapping]_de persoon die u wilt verwijderen.

1. Klik naast de naam op het pictogram voor ovalen (**...** ) en kies **[!UICONTROL Delete]** .

1. Klik op **[!UICONTROL Delete]** in het bevestigingsdialoogvenster.
