---
title: Inhoud ontwerpen - personalisatie
description: Geherbruikte sectie over het gebruiken van verpersoonlijking voor inhoudcreatie
source-git-commit: d67f44419e09693ec93fd4db7982ec59c672b633
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Inhoud ontwerpen - personalisatie

Journey Optimizer B2B edition gebruikt een inline eenvoudige syntaxis waarmee u expressies kunt maken met gepersonaliseerde inhoud tussen accolades `{}` . U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld.

Voorbeelden:

* `Hello {{lead.firstName}} {{lead.lastName}}`
* `Hello {%= lead.mktoName ?: "Marketer" %}`

>[!NOTE]
>
>Journey Optimizer B2B edition volgt nu _camel geval_ syntaxis voor personalisatietokens in e-mails om de andere toepassingen van Adobe Experience Platform voor een verenigbare ervaring aan te passen. Dit symbolische formaat is volledig compatibel met de [&#x200B; sjabloontaal van Handels &#x200B;](https://handlebarsjs.com/guide/#what-is-handlebars){target="_blank"}. Alle tokens die vóór deze wijziging zijn toegevoegd, worden automatisch bijgewerkt.

Bij het verwerken van de inhoud vervangt Journey Optimizer B2B edition de expressie door de gegevens in de Experience Platform-database. Zo, wordt het eerste voorbeeld _Sint Smit van Hello_.

In het volgende voorbeeld worden stappen beschreven voor het aanpassen van inhoud met behulp van lood-/accountkenmerken en systeemtokens.

1. Selecteer de tekstcomponent en klik _verpersoonlijking_ pictogram in de toolbar toevoegen.

   ![&#x200B; klik het Persoonlijke pictogram &#x200B;](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Deze actie opent _geeft Personalization_ dialoog uit.

1. Voeg een token toe door op de plusknop ( **+** ) naast de token te klikken.

   Als u het token met een fallback wilt toevoegen (standaardtekst die verschijnt wanneer dat veld niet beschikbaar is voor een lead), klikt u op het pictogram _Meer_ ( **..** ) en kiest u **[!UICONTROL Insert with fallback text]** .

   ![&#x200B; construeert gepersonaliseerde tekst gebruikend tokens &#x200B;](../assets/content-design-shared/visual-designer-personalize-dialog-handlebar.png){width="700" zoomable="yes"}

1. Voeg aanvullende tokens of andere statische tekst toe die u wilt opnemen.

1. Klik op **[!UICONTROL Save]**.

   Het verpersoonlijkings scripting wordt getoond in de visuele ontwerpruimte. U kunt deze selecteren om indien nodig wijzigingen aan te brengen.

   ![&#x200B; Uitgezochte verpersoonlijkingsmanuscript &#x200B;](../assets/content-design-shared/visual-designer-select-personalization-script.png){width="600"}
