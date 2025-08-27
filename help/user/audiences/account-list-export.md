---
title: Exportaccounts
description: Leer hoe u de accountlijst exporteert op basis van het filter voor inkoopgroepen.
feature: Account Lists
role: User
exl-id: 3ec8e8fd-1bc2-4efa-840f-f06520099060
source-git-commit: 124d917de02a2481bcf2558b381c0f932129a255
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Exportaccounts

Gebruik de _eigenschap van de Rekening van de Uitvoer_ om alle rekeningen of een reeks rekeningen uit te voeren die op het filtreren worden gebaseerd die u bepaalt. Tijdens het exportproces wordt een CSV-bestand gemaakt en wordt de URL voor het opgeslagen bestand binnen een pulsmelding verzonden. U kunt deze functie gebruiken om accounts indien nodig naar externe platforms te verplaatsen.

1. Ga in Journey Optimizer B2B edition naar **[!UICONTROL Accounts]** > **[!UICONTROL Buying groups]** in de linkernavigatie.

1. Selecteer de tab **[!UICONTROL Browse]** .

1. Klik op **[!UICONTROL Export accounts]** rechtsboven.

   ![ geef rekeningsdetails ](./assets/export-accounts.png){width="800" zoomable="yes"} uit

1. Definieer in het dialoogvenster de parameters van het accountpubliek dat u wilt exporteren.

   ![ specificeer het rekeningspubliek filtreren ](./assets/export-accounts-dialog.png){width="400"}

   Voor **[!UICONTROL Engagement score]** is de operator `Between` inclusief, evenals percentagebereiken. Bijvoorbeeld, zijn 5.1 en 5 zowel _tussen_ 5 en 6.

   Lege filterparameters worden als `Is Any` behandeld.

1. Klik op **[!UICONTROL Export accounts]** om het CSV-bestand te genereren met de opgegeven filters.

1. Wanneer u het bericht ontvangt dat het exporteren is voltooid, klikt u op de meldingskoppeling om het CSV-bestand te openen.

   ![ klik het bericht om het uitgevoerde dossier van de rekeningslijst CSV ](./assets/export-accounts-notification.png){width="425"} te downloaden

   >[!NOTE]
   >
   >Als u een berichtabonnement voor e-mailmeldingen hebt dat is ingesteld in de voorkeuren van uw Adobe-gebruikersaccount, is het mogelijk een e-mailmelding.

   De toepassingspagina richt zich aan _het Kopen Groep_ doorbladert lusje en de dialoog van het systeemsparen dossier zet u ertoe aan om het dossier aan uw systeem te bewaren. Als u de gegevens wilt delen, kunt u het systeem voor het delen van bestanden van uw team gebruiken.
