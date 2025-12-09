---
title: E-maildeduplicatie
description: Leer hoe u e-maildeduplicatie kunt gebruiken tijdens reizen naar uw account om te voorkomen dat dezelfde e-mail meerdere keren naar hetzelfde e-mailadres wordt verzonden.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: e-mail, deduplicatie, transport, dupliceren
source-git-commit: 89dcfae6293fc2bd1eefb58943bee354c57bc73a
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# E-maildeduplicatie

Gebruik deduplicatie via e-mail bij reizen om ervoor te zorgen dat hetzelfde e-mailadres niet meerdere keren naar hetzelfde e-mailadres wordt verzonden tijdens een rit. Wanneer u deze functie inschakelt, worden dubbele e-mailadressen geblokkeerd totdat de eerste record met dat e-mailadres de reis voltooit. Nadat een account een reis heeft voltooid, kan een persoon in aanmerking komen om opnieuw e-mails te ontvangen als onderdeel van een nieuwe account die de reis betreedt.

## Wanneer gebruikt u deduplicatie van e-mail

Er zijn een paar belangrijke scenario&#39;s waar u zou moeten nadenken toelatend e-maildeduplicatie:

* **E-mail wordt niet gebruikt als identiteit in Real-Time CDP** - het zelfde e-mailadres kan over veelvoudige personenprofielen verschijnen. Schakel deze functie in als deze dubbele profielen in aanmerking komen voor dezelfde rit en u wilt voorkomen dat de e-mail meerdere keren wordt verzonden.

* **Enige persoon verbonden aan veelvoudige rekeningen** - als uw het gegevensmodel van Real-Time CDP één enkele persoon toestaat om met veelvoudige rekeningen worden geassocieerd, en u wilt vermijden verzendend zelfde e-mail tweemaal naar die persoon wanneer de veelvoudige rekeningen (met inbegrip van profielen met het zelfde e-mailadres) voor de zelfde reis kwalificeren, laat deze eigenschap toe.

>[!NOTE]
>
>E-maildeduplicatie is van toepassing op het niveau van de reis. Als een persoon met hetzelfde e-mailadres in aanmerking komt voor verschillende reizen, kunnen hij of zij nog steeds e-mails ontvangen van elke reis.

## E-maildeduplicatie voor een reis inschakelen

E-maildeduplicatie voor een accountreis mogelijk maken:

1. Open een accountreis.

1. Klik **[!UICONTROL More]** (**..**) in de hoger-juiste hoek van de reiswerkruimte.

   ![&#x200B; de werkruimte van de Reis met Meer uitgevouwen menu die optie van de Deduplicatie E-mail tonen &#x200B;](./assets/email-deduplication-more-menu.png){width="450"}

1. Kies **[!UICONTROL Email Deduplication]** .

1. Selecteer in het dialoogvenster het selectievakje **[!UICONTROL Email Deduplication]** .

   ![&#x200B; de dialoog van de Deduplicatie E-mail met toegelaten knevel &#x200B;](./assets/email-deduplication-dialog.png){width="400"}

1. Klik op **[!UICONTROL Save]**.

Wanneer e-maildeduplicatie is ingeschakeld, controleert de rit elk e-mailadres voordat het e-mailadres wordt verzonden. Als een record met hetzelfde e-mailadres al dat knooppunt is ingevoerd, wordt de nieuwe invoer geblokkeerd totdat de eerste record de reis heeft voltooid.
