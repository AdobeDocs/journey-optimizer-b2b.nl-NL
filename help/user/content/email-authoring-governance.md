---
title: Auteur van een beheerde sjabloon
description: Leer hoe u e-mailauthoring kunt gebruiken met een beheerde sjabloon die vergrendelde inhoudsonderdelen bevat.
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Auteur uit een beheerde sjabloon

De ontwerpers van de inhoud kunnen [ bestuur (_inhoudsafsluiten_) ](./template-content-governance.md) toelaten wanneer het creëren van e-mailmalplaatjes. De eigenschappen van het bestuur staan hen toe om de delen van het ontwerp aan te wijzen die niet kunnen worden veranderd wanneer gebruikt in een rekeningsreis. Wanneer u [ een bewaarde malplaatje ](./email-authoring.md#select-a-template) aan auteur een e-mail selecteert, laadt de visuele ontwerper het malplaatje zodat u het als basis voor uw e-mail kunt gebruiken.

Als governance is ingeschakeld voor de sjabloon, wordt een waarschuwing weergegeven in het deelvenster Eigenschappen aan de rechterkant. U kunt **[!UICONTROL Highlight editable areas]** bij de bovenkant van het canvas aanzetten om te zien welke componenten en inhoudselementen voor gebruik in uw reis editable zijn.

![ Mening editable gebieden in een geregeerd malplaatje ](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

U kunt de elementen ook bepalen die gesloten of editable gebruikend de _boom van de Navigatie_ zijn. Klik het _pictogram van de Navigatieboom_ ( ![ pictogram van de Verbinding ](../assets/do-not-localize/icon-navigation-tree.svg)) links van het canvas om de boom te tonen.

![ Mening editable gebieden in een geregeerd malplaatje ](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

De pictogrammen geven de toegepaste vergrendelingsinstellingen voor inhoud aan.

| Pictogram | Naam | Beschrijving |
|------|------|-------------|
| ![ las slechts pictogram ](../assets/do-not-localize/icon-tree-lock.svg) | Alleen-lezen | De component is vergrendeld en kan niet worden bewerkt. Wanneer toegepast op het wortel (_[!UICONTROL Body]_) niveau, zijn alle kindcomponenten gesloten en kunnen niet worden uitgegeven. |
| ![ Inhoud geeft pictogram uit ](../assets/do-not-localize/icon-tree-content-lock.svg) | Inhoud vergrendelen | Inhoudsvergrendeling wordt toegepast op componentniveau. |
| ![ Bewerkbaar pictogram ](../assets/do-not-localize/icon-edit.svg) | Bewerkbaar | De component kan volledig worden bewerkt. Het is echter mogelijk dat u het element niet kunt verwijderen. |
| ![ Inhoud geeft pictogram uit ](../assets/do-not-localize/icon-tree-edit-text.svg) | Bewerkbaar - alleen inhoud | De component en de stijl zijn statisch, maar u kunt de inhoud (zoals tekst of afbeelding) wijzigen. |
