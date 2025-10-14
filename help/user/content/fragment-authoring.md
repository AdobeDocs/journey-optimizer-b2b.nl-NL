---
title: Fragmentauthoring
description: Auteur herbruikbare inhoudsfragmenten met visuele ontwerpgereedschappen - voeg componenten, personalisatie, voorwaardelijke inhoud en aanpasbare velden toe voor e-mails en sjablonen in Journey Optimizer B2B edition.
feature: Fragments, Content Design Tools
role: User
exl-id: d29754cf-6721-489c-bff8-cde034456db2
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Fragmentauthoring

Nadat u [&#x200B; een fragment &#x200B;](./fragments.md#create-fragments) creeert, gebruik de visuele ontwerpruimte aan auteur de structuur en inhoudscomponenten in uw fragment.

## Structuur en inhoud toevoegen {#design-fragment}

{{$include /help/_includes/content-design-components.md}}

## Elementen toevoegen

{{$include /help/_includes/content-design-assets.md}}

## Navigeren door de lagen, instellingen en stijlen

{{$include /help/_includes/content-design-navigation.md}}

## Inhoud personaliseren

{{$include /help/_includes/content-design-personalization.md}}

## Voorwaardelijke inhoud

Als u voorwaardelijke inhoud wilt toevoegen die de inhoud aanpast aan de doelprofielen op basis van regels, selecteert u een inhoudscomponent en klikt u op de knop **[!UICONTROL Enable conditional content]** op de werkbalk van de component. Wanneer het gepubliceerde fragment in een e-mailbericht wordt opgenomen, bepalen de voorwaardelijke regels de variant van een voorwaardelijke component die in het e-mailbericht wordt weergegeven.

Voor meer informatie, zie [_Voorwaardelijke inhoud_](./conditional-content.md).

## Fragmentaanpassing inschakelen

Wanneer een auteur een fragment aan een [&#x200B; e-mail &#x200B;](./email-authoring.md#content-authoring---use-visual-fragments) of [&#x200B; e-mailmalplaatje &#x200B;](./email-template-authoring.md#content-authoring---use-visual-fragments) toevoegt, wordt de fragmentinhoud gesloten door gebrek. Wijzigingen in het gepubliceerde fragment worden automatisch doorgegeven aan alle inhoudselementen waar het fragment wordt gebruikt. Wanneer u een parameter voor een component in het fragment toewijst als bewerkbaar, kan de auteur van de e-mail of sjabloon een aangepaste veldwaarde opgeven die specifiek is voor zijn of haar behoeften. Deze aanpassingsvlag is beperkt tot beeld, tekst, en knoop visuele componenten.

Als u bijvoorbeeld een herbruikbare banner ontwerpt die een klikbare knop bevat, kunt u de URL-parameter voor de knop instellen als bewerkbaar. E-mailauteurs kunnen vervolgens een URL gebruiken die specifieker is voor hun e-mailcampagne. Met deze aanpasbare velden kunnen marketers herbruikbare inhoud beheren en aanpassen zonder dat ze geheel nieuwe inhoudsblokken hoeven te maken of de overgeërfde updates van het oorspronkelijke fragment moeten onderbreken.

1. Selecteer in de visuele inhoudeditor de afbeelding, tekst of knopelement waar u aanpassing wilt inschakelen.

1. Selecteer de tab **[!UICONTROL Editable fields]** in de componentdetails aan de rechterkant.

1. Klik op de optie **[!UICONTROL Enable edition]** om te schakelen en stel de bewerkbare velden in.

   ![&#x200B; laat editable gebieden voor een component van het fragmentbeeld &#x200B;](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"} toe

   U kunt aanpassingen inschakelen voor de weergegeven velden, afhankelijk van het componenttype en de parameters die in het fragment zijn gedefinieerd.

   Verander de knevel in toegelaten staat voor elk gebied waar u aanpassing wilt toestaan.

1. Klik op **[!UICONTROL Overview]** om alle bewerkbare velden en de bijbehorende standaardwaarden te bekijken.

   ![&#x200B; herzie de editable gebieden en hun standaardwaarden &#x200B;](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. Sla uw wijzigingen op.

## Gekoppelde URL-tracking bewerken

{{$include /help/_includes/content-design-links.md}}
