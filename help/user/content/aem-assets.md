---
title: Werken met Experience Manager Assets
description: Leer hoe u afbeeldingselementen van een verbonden AEM Assets-opslagplaats kunt gebruiken bij het ontwerpen van inhoud in Adobe Journey Optimizer B2B Edition.
feature: Assets, Content
source-git-commit: 0bdf0da4db0cbfc781d16f1c50716b1fc8ea4db9
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Werken met Experience Manager-elementen

Wanneer Adobe Experience Manager Assets as a Cloud Service is geïntegreerd met Adobe Journey Optimizer B2B Edition, kunt u eenvoudig digitale middelen vinden en openen voor gebruik in uw marketinginhoud. Terwijl u de inhoud ontwerpt, zijn de elementen toegankelijk via het _[!UICONTROL Assets]_-item in de linkernavigatie en wanneer u e-mailinhoud ontwerpt voor een accountreis. U kunt ook rechtstreeks vanuit Adobe Journey Optimizer B2B Edition middelen uploaden naar een aangesloten AEM Assets as a Cloud Service-opslagplaats.

>[!NOTE]
>
>Momenteel worden alleen afbeeldingselementen van Adobe Experience Manager Assets ondersteund in Adobe Journey Optimizer B2B Edition. Wijzigingen in de activa moeten worden aangebracht vanuit de centrale gegevensbank van Adobe Experience Manager Assets. [ Leer meer ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets)

Als u deze digitale elementen gebruikt, worden de meest recente wijzigingen in Assets as a Cloud Service automatisch doorgegeven aan live e-mailcampagnes via gekoppelde verwijzingen. Als afbeeldingen worden verwijderd in Adobe Experience Manager Assets as a Cloud Service, worden de afbeeldingen weergegeven met een verbroken verwijzing in de e-mails. Wanneer de activa die momenteel binnen rekeningreizen worden gebruikt worden gewijzigd of geschrapt, worden de reisauteurs op de hoogte gebracht van de beeldveranderingen en de lijst van reizen die het beeld gebruiken. Alle wijzigingen in de activa moeten plaatsvinden in de centrale gegevensbank van Adobe Experience Manager Assets.

## AEM Assets gebruiken als afbeeldingsbron

Als uw milieu één of meerdere [ de bewaarplaatsen van Assets verbindingen ](../admin/configure-aem-repositories.md) heeft, kunt u AEM Assets als bron voor activa aanwijzen wanneer u creeert of details voor een e-mail, e-mailmalplaatje, of visueel fragment bekijkt.

* Wanneer u nieuwe inhoud maakt, kiest u `AEM Assets` als het **[!UICONTROL Image Source]** -item in het dialoogvenster.

  ![ Uitgezochte AEM Assets als beeldbron in creeer dialoog ](./assets/create-dialog-aem-assets.png){width="500"}

* Wanneer u een bestaande inhoudsbron opent, kiest u `AEM Assets` in het _[!UICONTROL Body]_-deelvenster aan de rechterkant.

  ![ Uitgezochte AEM Assets als beeldbron in de eigenschappen ](./assets/content-source-aem-assets.png){width="700" zoomable="yes"}

## Elementen openen voor ontwerpen

>[!IMPORTANT]
>
>Een beheerder moet gebruikers die toegang tot Assets nodig hebben, toevoegen aan de profielen Assets Consumer Users of/and Assets Users Product. [ Leer meer ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console)

In de visuele inhoudsredacteur, klik het _selecteur van Activa_ pictogram in linkerzijbalk. Hiermee wijzigt u het deelvenster Gereedschappen in een lijst met beschikbare middelen in de geselecteerde opslagplaats.

![ klik het de selecteurspictogram van Assets om tot de beeldactiva ](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"} toegang te hebben

Als u meer dan één aangesloten AEM opslagplaatsen hebt, klikt u op de menupijl voor **[!UICONTROL Repository]** om de opslagplaats te kiezen die u wilt gebruiken.

![ kies een bewaarplaats van AEM Assets om tot de beeldactiva ](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"} toegang te hebben

Er zijn meerdere methoden om een afbeeldingselement toe te voegen aan het visuele canvas:

* Sleep een afbeeldingsminiatuur vanuit de linkernavigatie en zet deze neer.

  ![ kies een bewaarplaats van AEM Assets om tot de beeldactiva ](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"} toegang te hebben

* Voeg een afbeeldingscomponent toe aan het canvas en klik op **[!UICONTROL Browse]** om het dialoogvenster _[!UICONTROL Select Assets]_te openen.

  In het dialoogvenster kunt u een afbeelding kiezen in de geselecteerde opslagplaats.

  Er zijn meerdere gereedschappen beschikbaar om u te helpen de middelen te vinden die u nodig hebt.

  ![ gebruikshulpmiddel in de Uitgezochte dialoog van Assets om een beeldactiva ](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"} te vinden en te selecteren

   * Wijzig de **[!UICONTROL Repository]** rechtsboven.

   * Klik op **[!UICONTROL Manage assets]** rechtsboven om de Assets-opslagplaats te openen in een ander browsertabblad en AEM Assets-beheergereedschappen te gebruiken.

   * Klik het _type van Mening_ selecteur bij het hoogste recht om de vertoning in **[!UICONTROL List View]**, **[!UICONTROL Grid View]**, **[!UICONTROL Gallery View]**, of **[!UICONTROL Waterfall View]** te veranderen.

   * Klik het _pictogram van de Sorteervolgorde_ om de sorteervolgorde tussen het stijgen en het dalen te veranderen.

   * Klik op de menupijl **[!UICONTROL Sort by]** om de sorteercriteria te wijzigen in **[!UICONTROL Name]** , **[!UICONTROL Size]** of **[!UICONTROL Modified]** .

   * Klik het _pictogram van de Filter_ op de bovenkant verlaten om de getoonde punten volgens uw criteria te filtreren.

   * Typ tekst in het veld Zoeken om de weergegeven items te filteren op een overeenkomst met de elementnaam.

  ![ Gebruik de filters en het onderzoeksgebied om van de activa ](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"} de plaats te bepalen

<!-- 
## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.

-->