---
title: In-CRM-inzichten
description: Open Journey Optimizer B2B edition-inkoopgroepen rechtstreeks in Salesforce. De leden van het verkoopteam kunnen betrokkenheidsgegevens bekijken en verkoopmogelijkheden identificeren met In-CRM Inzichten.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# In-CRM-inzichten

In-CRM Insights is een webtoepassing die in Salesforce wordt geïntegreerd, zodat u rechtstreeks toegang hebt tot uw Journey Optimizer B2B edition-inkoopgroepen binnen Salesforce. Hiermee kunt u mogelijkheden voor meer betrokkenheid en verkoopmogelijkheden identificeren.

De toepassing van de Inzichten In-CRM is beschikbaar in het [&#x200B; pakket van de Inzichten van de Verkoop van Marketo &#x200B;](https://experienceleague.adobe.com/nl/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange).

## Machtigingen

Om tot de toepassing toegang te hebben, moeten de gebruikers lidmaatschap in een rol met de **toestemmingen van de Inzichten van de Verkoop :View van de Verkoop** hebben.

Als u een groep gebruikers tot InCRM-Inzichten wilt beperken, gebruik de volgende richtlijnen om een douanerol specifiek voor InCRM-Inzichten tot stand te brengen:

* Creeer een douanerol met slechts de **2&rbrace; geplaatste toestemming van de Inzicht van de Verkoop van de Verkoop :View &lbrace;.**
* Maak een nieuwe gebruikersgroep zonder productprofielen toe te voegen.
* Maak een andere gebruikersgroep en voeg een AEP-productprofiel toe of voeg een bestaand AEP-profiel toe aan de gebruikersgroep die u zojuist hebt gemaakt.
* Wijs de nieuwe gebruikersgroepen aan de nieuwe rol toe en voeg nieuwe gebruikers aan de nieuwe gebruikersgroepen toe.

## In-CRM-inzichten gebruiken

De toepassing In-CRM Insights is beschikbaar in Salesforce via de App Launcher.

1. Klik op App Launcher in Salesforce.
1. Selecteer of zoek naar `Journey Optimizer B2B Edition` .
1. Meld u aan met uw Adobe-gebruikersgegevens op het tabblad dat wordt weergegeven.
1. Kies een sandbox die als host fungeert voor uw accountreizen.

Je koopgroepen worden geladen en beschikbaar. Gegevens zijn alleen-lezen via In-CRM Insights.

>[!NOTE]
>
>Het lidmaatschap in de [&#x200B; productrol van de Gebruiker van de Verkoop 0&rbrace; B2B &lbrace;wordt vereist om tot Inzichten In-CRM toegang te hebben.](../admin/user-management.md#b2b-built-in-roles)

Na het selecteren van een het kopen groep, kunt u de [&#x200B; groepsdetails &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#) doorbladeren, enkel zoals in Journey Optimizer B2B edition.
