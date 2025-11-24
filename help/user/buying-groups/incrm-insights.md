---
title: In-CRM-inzichten
description: Open Journey Optimizer B2B edition-inkoopgroepen rechtstreeks in CRM's. De leden van het verkoopteam kunnen betrokkenheidsgegevens bekijken en verkoopmogelijkheden identificeren met In-CRM Inzichten.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: b5173345f5dfb879b36726ca27e164d9a267dac4
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---


# In-CRM-inzichten

[!DNL In-CRM Insights] is een webtoepassing die is geïntegreerd in Salesforce en Microsoft Dynamics 365 en die u rechtstreeks toegang biedt tot [!DNL Journey Optimizer B2B Edition] -inkoopgroepen binnen uw CRM. Het verenigt verkoopgegevensbronnen, die het gemakkelijker maken om kansen voor verhoogde betrokkenheid en verkooppotentieel te identificeren.

De [!DNL In-CRM Insights] toepassing is beschikbaar in het [&#x200B; pakket van de Inzichten van de Verkoop van Marketo &#x200B;](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange).

## Installatie

Het installatieproces omvat:

* Gebruikersmachtigingen en groepen instellen
* Het softwarepakket installeren
* Aanmelden via uw CRM

### Machtigingen instellen

Gebruikers die de software installeren, moeten machtigingen hebben om Salesforce-pakketten te installeren.

Om tot de toepassing toegang te hebben, moeten de gebruikers lidmaatschap in een rol met de **2&rbrace; toestemming van de Inzichten van de Verkoop van de Verkoop :View hebben.**

Als u gebruikers wilt beperken tot alleen [!DNL In-CRM Insights] :

1. Creeer a [&#x200B; douanerol &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role) en wijs het de **Inzichten van de Verkoop toe: De toestemming van de Inzichten van de Verkoop van de Mening**.
1. Creeer een nieuwe [&#x200B; gebruikersgroep &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group).
1. Voeg een Experience Platform-productprofiel toe aan de groep.

### Het pakket installeren

Volg de stappen voor Salesforce of Microsoft Dynamics om het In-CRM Insights-pakket te installeren.

#### Salesforce

1. Download het [&#x200B; In-CRM het installerpakket van Inzichten &#x200B;](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce).
1. Nadat u zich hebt aangemeld, wordt u omgeleid naar de installatiepagina van het pakket.
1. Selecteer de optie **[!UICONTROL Install for All Users]** en klik op **[!UICONTROL Install]** .

   ![&#x200B; installeer het pakket van Inzichten In-CRM &#x200B;](assets/incrm-install-sf.png){width=500}

1. Goedkeuren van toegang van derden in het dialoogvenster en klik vervolgens op **[!UICONTROL Continue]** .
1. Klik op **[!UICONTROL Done]** wanneer de installatie is voltooid.

   Het is nu vermeld op de **Geïnstalleerde pagina van Pakketten** en **Journey Optimizer B2B edition** is vermeld in de Lanceerinrichting van de App.

   ![&#x200B; Inzicht in-CRM opstelling binnen Salesforce &#x200B;](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. Download het [&#x200B; In-CRM het installerpakket van Inzichten &#x200B;](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics).
1. Ga naar de [&#x200B; haven van de Apps van de Macht &#x200B;](https://make.powerapps.com/){target=_blank}.
1. Nadat u zich hebt aangemeld, selecteert u de omgeving voor het pakket en navigeert u vanuit het linkermenu naar **[!UICONTROL Solutions]** .
1. Klik op **[!UICONTROL Import solution]**.
1. Blader naar en upload het installerpakket en klik vervolgens op **[!UICONTROL Next]** .
1. Controleer de pakketgegevens en klik op **[!UICONTROL Next]** .
1. Onder _variabelen van het Milieu_, verifieer dat de waarde aan `prod` wordt geplaatst (verander niet de waarde) en klik **[!UICONTROL Import]**.
1. Wanneer de installatie is voltooid, wordt **[!UICONTROL Journey Optimizer B2B Edition]** > **[!UICONTROL Buying groups]** weergegeven op de linkernavigatiebalk.

   ![&#x200B; In-CRM Inzichten beschikbaar in Microsoft Dynamics &#x200B;](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## Je koopgroepen bekijken

Volg de aanwijzingen om u aan te melden bij uw Adobe-account. Je koopgroepen worden geladen en kunnen worden weergegeven.

Na het selecteren van een het kopen groep, kunt u de [&#x200B; groepsdetails &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#) doorbladeren. Dit is hetzelfde als de gegevens en inzichten die worden weergegeven in Journey Optimizer B2B edition, maar gegevens zijn alleen-lezen via [!DNL In-CRM Insights] .
