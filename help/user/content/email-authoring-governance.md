---
title: Auteur van een beheerde sjabloon
description: 'E-mails van auteurs van beheerde sjablonen met vergrendelde inhoud: identificeer bewerkbare gebieden en werk binnen beheerbeperkingen in Journey Optimizer B2B edition.'
feature: Email Authoring, Content
role: User
exl-id: 1af996a6-a010-4899-96e9-bad76f93865c
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Auteur uit een beheerde sjabloon

De ontwerpers van de inhoud kunnen [&#x200B; bestuur (_inhoudsafsluiten_) &#x200B;](./template-content-governance.md) toelaten wanneer het creëren van e-mailmalplaatjes. De eigenschappen van het bestuur staan hen toe om de delen van het ontwerp aan te wijzen die niet kunnen worden veranderd wanneer gebruikt in een rekeningsreis. Wanneer u [&#x200B; een bewaarde malplaatje &#x200B;](./email-authoring.md#select-a-template) aan auteur een e-mail selecteert, laadt de visuele ontwerpruimte het malplaatje zodat u het als basis voor uw e-mail kunt gebruiken.

Als governance is ingeschakeld voor de sjabloon, wordt een waarschuwing weergegeven in het deelvenster Eigenschappen aan de rechterkant. U kunt **[!UICONTROL Highlight editable areas]** bij de bovenkant van het canvas aanzetten om te zien welke componenten en inhoudselementen voor gebruik in uw reis editable zijn.

![&#x200B; Mening editable gebieden in een geregeerd malplaatje &#x200B;](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

U kunt de elementen ook bepalen die gesloten of editable gebruikend de _boom van de Navigatie_ zijn. Klik het _pictogram van de Navigatieboom_ ( ![&#x200B; pictogram van de Verbinding &#x200B;](../assets/do-not-localize/icon-navigation-tree.svg)) links van het canvas om de boom te tonen.

![&#x200B; Mening editable gebieden in een geregeerd malplaatje &#x200B;](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

De pictogrammen geven de toegepaste vergrendelingsinstellingen voor inhoud aan.

| Pictogram | Naam | Beschrijving |
|------|------|-------------|
| ![&#x200B; las slechts pictogram &#x200B;](../assets/do-not-localize/icon-tree-lock.svg) | Alleen-lezen | De component is vergrendeld en kan niet worden bewerkt. Wanneer toegepast op het wortel (_[!UICONTROL Body]_) niveau, zijn alle kindcomponenten gesloten en kunnen niet worden uitgegeven. |
| ![&#x200B; Inhoud geeft pictogram uit &#x200B;](../assets/do-not-localize/icon-tree-content-lock.svg) | Inhoud vergrendelen | Inhoudsvergrendeling wordt toegepast op componentniveau. |
| ![&#x200B; Bewerkbaar pictogram &#x200B;](../assets/do-not-localize/icon-edit.svg) | Bewerkbaar | De component kan volledig worden bewerkt. Het is echter mogelijk dat u het element niet kunt verwijderen. |
| ![&#x200B; Inhoud geeft pictogram uit &#x200B;](../assets/do-not-localize/icon-tree-edit-text.svg) | Bewerkbaar - alleen inhoud | De component en de stijl zijn statisch, maar u kunt de inhoud (zoals tekst of afbeelding) wijzigen. |
