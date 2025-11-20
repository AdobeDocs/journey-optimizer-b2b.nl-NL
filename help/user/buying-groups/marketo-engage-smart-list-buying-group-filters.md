---
title: Groepsfilters kopen in Marketo Engage
description: Filter leidt door groepslidmaatschap te kopen in de Slimme Lijsten van Marketo Engage met beperkingen zoals volledigheidsscore om campagnes en lood te optimaliseren scoring.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 1c5a08b293db9287d03b103d794cc17a1c186af0
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Groepsfilters kopen in Marketo Engage

>[!IMPORTANT]
>
>**Veroudering van de Eigenschap**</br></br>
>
>Met de [&#x200B; vereenvoudigde architectuur &#x200B;](../simplified-architecture.md) voor Journey Optimizer B2B edition, zijn de het kopen groepsfilters niet meer beschikbaar in een verbonden instantie van Marketo Engage.</br></br>
>
>Als alternatief, kunt u een statische lijst voor elke oplossingsrente tot stand brengen en dan [&#x200B; gebruiken _toevoegt aan de lijst van Marketo_ actie &#x200B;](../journeys/action-nodes.md#marketo-engage-actions) van een vervoerknoop. Met deze handeling voegt u kopende groepsleden toe aan een bepaalde statische lijst in een verbonden Marketo Engage-instantie. Dan, gebruik de oplossing op rente-geconcentreerde statische lijst voor een slim lijstfilter.

Als marketeer wilt u misschien de campagnes in Marketo Engage onderdrukken voor mensen die deel uitmaken van het kopen van groepen in Journey Optimizer B2B edition. U kunt ook de workflows voor scoren van leads in Marketo Engage informeren aan de hand van informatie over de leads die aan inkoopgroepen zijn gekoppeld. Bijvoorbeeld:

* Maakt dit deel uit van een koopgroep?
* Is de koopgroep volledig en betrokken?

Als deze voorwaarden waar zijn, kunt u ervoor kiezen om de hoogste score te behalen. Als dat niet het geval is, kunt u ervoor kiezen deze niet te markeren als een voor de markt gekwalificeerde lead (MQL).

In uw Marketo Engage-instantie die is verbonden met Journey Optimizer B2B edition, kunt u het filter _[!UICONTROL Member of Buying Group]_&#x200B;in uw slimme lijsten gebruiken om deze leads te identificeren op basis van uw campagnestrategie.

1. Nadat u [&#x200B; een Slimme Lijst in Marketo Engage &#x200B;](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"} creeert, selecteer het **[!UICONTROL Smart List]** lusje om de filterredacteur te openen.

1. Blader in de lijst met filters aan de rechterkant omlaag en vouw de map **[!UICONTROL Special Filters]** uit.

1. Klik op het filter **[!UICONTROL Member of Buying Group]** en sleep het naar het filterdefinitiegebied.

   ![&#x200B; voeg het Lid van het Kopen filter van de Groep aan de Slimme Lijst &#x200B;](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"} toe

1. Stel de optie _[!UICONTROL Member of Buying Group]_&#x200B;in op **[!UICONTROL true]**&#x200B;of **[!UICONTROL false]**.

   Deze beperking is vereist voor de definitie.

1. (Optioneel) Voeg aan het filter andere inkoopgroepsgerelateerde beperkingen toe op basis van de manier waarop u leads voor de slimme lijst wilt identificeren.

   * Klik op **[!UICONTROL Add Constraint]** rechtsboven op de filterkaart.

     ![&#x200B; Uitgezochte een andere beperking &#x200B;](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Selecteer de beperking die u, zoals _Score van de Voltooiing_ of _Interesse van de Oplossing_ wilt toevoegen.

   * Plaats de evaluatie die u voor een gelijke wilt gebruiken. Voor een score kunt u een exacte overeenkomst gebruiken of een bereik dat boven of onder het getal ligt dat u invoert.

     Voor een afzonderlijk item, zoals de belangen van de oplossing die in Journey Optimizer B2B edition zijn gedefinieerd, kunt u een of meer items voor de lijst selecteren.

     ![&#x200B; selecteer een waarde voor de beperking van de lijst &#x200B;](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Selecteer de eerste en klik nogmaals op de kiezer om het dialoogvenster _[!UICONTROL Multiple Value Chooser]_&#x200B;te openen.

     ![&#x200B; Uitgezochte veelvoudige waarden voor de beperking &#x200B;](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Plaats de resterende items naar rechts en klik op **[!UICONTROL OK]** wanneer u de lijst met items hebt die u voor de beperking wilt gebruiken.

   * Herhaal deze handelingen om zoveel beperkingen toe te voegen als u nodig hebt.

   ![&#x200B; Lid van het Kopen filter van de Groep met veelvoudige beperkingen &#x200B;](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
