---
title: Inhoud ontwerpen - personalisatie
description: Geherbruikte sectie over het gebruiken van verpersoonlijking voor inhoudcreatie
source-git-commit: 3791beb98068a56882bb0a96fbc6b192e85130bb
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---

# Inhoud ontwerpen - personalisatie

Journey Optimizer B2B edition gebruikt een inline eenvoudige syntaxis waarmee u expressies kunt maken met gepersonaliseerde inhoud die wordt ingesloten door dubbele accolades `{}` . U kunt meerdere expressies zonder beperkingen toevoegen in dezelfde inhoud of hetzelfde veld.

Voorbeelden:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Bij het verwerken van de inhoud vervangt Journey Optimizer B2B edition de expressie door de gegevens in de database van het Experience Platform. Zo, wordt het eerste voorbeeld _Sint Smit van Hello_.

In het volgende voorbeeld worden stappen beschreven voor het aanpassen van inhoud met behulp van lood-/accountkenmerken en systeemtokens.

1. Selecteer de tekstcomponent en klik _verpersoonlijking_ pictogram in de toolbar toevoegen.

   ![ klik het Persoonlijke pictogram ](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Deze actie opent _geeft Personalization_ dialoog uit.

1. Klik **+** of **..** om een teken aan de lege ruimte toe te voegen.

   ![ construeert gepersonaliseerde tekst gebruikend tokens ](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Save]**.
