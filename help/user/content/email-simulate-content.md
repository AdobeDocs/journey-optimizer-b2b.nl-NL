---
title: Uw e-mailinhoud voorvertonen en testen
description: Leer hoe u uw e-mailinhoud kunt voorvertonen en testen om te controleren of deze geen fouten bevat in de instellingen voor inhoud en personalisatie.
feature: Email Authoring
level: Beginner
role: User
exl-id: cf9d7716-b54d-430a-8102-72f9d35cc694
source-git-commit: fb243fbbbf897fd40d816995d6bef96480e355c1
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Uw e-mailinhoud voorvertonen en testen

Gebruik _simuleren inhoud_ eigenschap om de e-mailinhoud voor te vertonen en testleveringen naar specifieke ontvangers te verzenden. De vereiste e-mailvelden moeten zijn gedefinieerd, inclusief _[!UICONTROL From name]_,_[!UICONTROL From address]_ , _[!UICONTROL Reply-to address]_en_[!UICONTROL Subject line]_ , voor toegang tot de voorvertoning- en testfuncties.

>[!IMPORTANT]
>
>U kunt geen voorbeeld van het e-mailbericht weergeven als er fouten optreden. Controleer het _Alarm_ om ervoor te zorgen dat geen fouten de voorproeffuncties blokkeren. De waarschuwingen blokkeren geen voorproef, maar u zou hen moeten richten alvorens u de reis publiceert die de e-maillevering teweegbrengt.

## De e-mailvoorvertoning weergeven

U kunt tot de teruggevende voorproef van de [ e-mailontwerpruimte ](./email-authoring.md) toegang hebben, of van _[!UICONTROL Summary]_wanneer u [ een e-mail van de lijst E-mail ](./emails-list.md#edit-emails) opent.

1. Klik op **[!UICONTROL Simulate Content]** boven.

   ![ klik Simuleren inhoud ](assets/email-simulate-content.png){width="800" zoomable="yes"}

   >[!NOTE]
   >
   >Deze knop is niet beschikbaar als er fouten zijn of als de vereiste velden niet zijn gedefinieerd voor de e-mail.

1. Selecteer op de pagina _[!UICONTROL Simulate]_een personenprofiel in de lijst **[!UICONTROL People]**dat u wilt gebruiken voor het weergeven van de e-mail.

   In de voorvertoning van de inhoud worden gepersonaliseerde elementen gevuld volgens het geselecteerde persoonlijke profiel.

   ![ selecteer een personenprofiel om de simulatie ](./assets/email-simulate-content-preview.png){width="800" zoomable="yes"} terug te geven

   Als de _[!UICONTROL People]_lijst op de linkerzijde leeg is, [ voegt mensen ](#add-people-to-the-profiles-list) toe gebruikend contacten van de verbonden instantie van Marketo Engage.

   >[!TIP]
   >
   >U kunt [ Litmus gebruiken test het teruggeven integratie ](./email-test-rendering.md) om e-mailbericht het teruggeven in populaire Desktop, mobiele, en web-based cliënten te controleren.

## De weergaveopties aanpassen

Met de weergavegereedschappen kunt u de voorvertoning wijzigen op basis van het apparaattype of het zoomniveau:

* Selecteer het _Desktop_ ( ![ de vertoningspictogram van de Desktop ](../../assets/do-not-localize/icon-device-desktop.svg)) pictogram om de voorproef te tonen gebruikend de Desktop het stileren en aspectverhouding.
* Selecteer het _Mobiele_ ( ![ Mobiele vertoningspictogram ](../../assets/do-not-localize/icon-device-mobile.svg)) pictogram om de voorproef te tonen gebruikend het mobiele apparaat het stileren en aspectverhouding.
* Klik het _niveau van het Gezoem_ pijl en selecteer een gezoempercentage om te herzien hoe de inhoud volgens het gezoemniveau verandert.

![ pas de voorproefvertoning ](assets/email-simulate-content-preview-display-options.png){width="600" zoomable="yes"} aan

## Proefdrukken verzenden

Een bewijs is een geleverd testbericht dat u en uw teamleden toestaat om een e-mailbericht te herzien alvorens het naar leden van een publiek te verzenden. Ontvangers van de proefdruk kunnen de rendering van berichten, de inhoud, de instellingen voor personalisatie en de configuratie controleren. U kunt proefdrukken verzenden met een geselecteerd testprofiel.

1. Klik op **[!UICONTROL Send proof]** rechtsboven.

   ![ klik verzendt proef ](assets/email-simulate-content-preview-send-proof.png){width="500"}

1. In _verzend proef_ pagina, ga het eerste e-mailadres van de ontvanger in.

1. Voor elke andere ontvanger die u in de revisie wilt opnemen, klikt u op **[!UICONTROL Add recipient]** en voert u het bijbehorende e-mailadres in het veld **[!UICONTROL Send to]** in.

   U kunt maximaal tien ontvangers toevoegen voor de proefaflevering.

1. Stel voor elke ontvanger het veld **[!UICONTROL Simulate as]** in door een testprofiel te selecteren voor het aanpassen van de inhoud van het bericht.

   ![ voeg ontvangers toe en plaats testprofielen ](assets/email-simulate-content-preview-send-proof-recipients.png){width="700" zoomable="yes"}

1. Klik op **[!UICONTROL Send proof]**.

## Personen toevoegen aan de lijst met profielen

1. Klik boven aan de lijst _[!UICONTROL People]_op **[!UICONTROL Add People]**.

   ![ pas de voorproefvertoning ](assets/email-simulate-content-add-people.png){width="500"} aan

1. Voer in het dialoogvenster _[!UICONTROL Add people for testing]_het volledige e-mailadres voor de contactpersoon in.

   Om veelvoudige contacten toe te voegen, ga veelvoudige adressen in die door een komma worden gescheiden.

1. Schakel het selectievakje in voor elke overeenkomende contactpersoon die u wilt toevoegen aan de lijst met testprofielen.

   ![ pas de voorproefvertoning ](assets/email-simulate-content-add-people-addresses.png){width="700" zoomable="yes"} aan

1. Klik op **[!UICONTROL Add]** rechtsboven.
