---
title: Gebruikersbeheer
description: Leer hoe u teamleden toewijst aan Journey Optimizer B2B Edition-productprofielen.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: f8ae6e51e76ded14316273c8e746ed814e7eb68b
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 0%

---

# Gebruikersbeheer

Nadat de provisioning is voltooid en de sandboxen zijn gebonden, voert u de volgende stappen uit om Adobe Journey Optimizer B2B Edition-toegang te bieden aan uw team en gebruikers.

1. [ creeer een het productprofiel van het Marketo Engage ](#marketo-engage-profile) in de Admin Console (nieuwe instantie van het Marketo Engage slechts).
1. [ creeer een gebruikersgroep ](#create-user-group) in de Admin Console.
1. [ creeer een rol ](#create-role) in Toestemmingen AEP.
1. [ voegt gebruikers ](#add-users) in de Admin Console toe.

Als beheerder kunt u deze taken uitvoeren in de Adobe Admin Console, een centrale plaats voor het beheer en beheer van de productlicenties en gebruikers van uw Adobe. In de Admin Console, kunt u gebruikers in één enkele plaats in plaats van binnen uw diverse individuele oplossingen tot stand brengen en leiden. Verwijs naar de [ pagina van het overzicht van de Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html) om meer over zijn functies en mogelijkheden te leren.

## Toegang tot de Admin Console

Alvorens u de Admin Console kunt gebruiken om gebruikers binnen uw team te beheren, moet u ervoor zorgen dat u tot de Admin Console kunt toegang hebben en de aangewezen toestemmingen hebben.

1. Als systeembeheerder ontvangt u meerdere e-mails van de Adobe als onderdeel van het instapproces.

   Zoek de welkomstmail die de informatie over de organisatienaam verstrekt waaraan u toegang hebt verleend.

1. Klik op de koppeling **[!UICONTROL Get started]** in uw welkomstbericht om naar de Admin Console te navigeren.

   Als u niet e-mail kunt vinden, open browser rechtstreeks aan de Admin Console in [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Meld u aan met uw Adobe ID.

   Op succesvolle login, ziet u de _pagina van het Overzicht_ van Adobe Admin Console.

1. Als u toegang tot veelvoudige organisaties hebt, zorg ervoor dat u aan de correcte organisatie hebt het programma geopend.

   Als u uw organisatie wilt wijzigen, klikt u in de rechterbovenhoek op de naam van de organisatie en kiest u de organisatie waartoe u toegang nodig hebt.

1. Selecteer **[!UICONTROL Administrators]** op de _[!UICONTROL Users]_-kaart om te controleren of u systeembeheerder bent.

   ![ overzicht van de Admin Console - klik Beheerders ](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Zoek door je Adobe ID-e-mail, gebruikersnaam, voornaam of achternaam in te voeren.

   * Als uw toegang correct wordt gevormd, keert het onderzoek uw verslag terug.

   * Als de waarde in de kolom **[!UICONTROL ADMIN ROLE]** `System` toont, weet u dat u (of de getoonde gebruiker) een systeembeheerder bent.

## Het productprofiel van het Marketo Engage maken {#marketo-engage-profile}

Wanneer het verlenen van toegang tot een oplossing van de Adobe, wilt u hen niet noodzakelijk volledige toegang verlenen. Met productprofielen kan elke oplossing beschikken over een eigen set gebruikersrechten. Gebruik de Admin Console om productprofielen toe te wijzen.

Voor meer informatie over het gebruiken van productprofielen voor gebruikersrechten, zie [ productprofielen voor ondernemingsgebruikers ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) in de documentatie van de Admin Console beheren.

>[!NOTE]
>
>Een systeembeheerder van het het systeem van de Admin Console of van het Marketo Engage productbeheerder kan deze stappen uitvoeren.

1. Login aan [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Selecteer de tab **[!UICONTROL Products]** .

1. Open de instantie Markt inschakelen waar u het profiel wilt toevoegen en klik op Nieuw profiel.

   ![ Admin Console - de instantie van het Marketo Engage - Nieuw profiel ](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Ga een naam van het productprofiel, zoals _StandaardGebruiker_ in.

1. Klik **daarna** en dan **sparen**.

## Een gebruikersgroep maken {#create-user-group}

Een gebruikersgroep is een inzameling van gebruikers wordt verleend een gedeelde reeks toestemmingen. U kunt gebruikers toevoegen aan of verwijderen uit uw gebruikersgroep. De machtigingen voor de groep blijven ongewijzigd wanneer de gebruikers in de groep worden gewijzigd.

Voor meer informatie over hoe de gebruikersgroepen worden gebruikt om toestemmingen te beheren, zie [ gebruikersgroepen ](https://helpx.adobe.com/enterprise/using/user-groups.html) beheren in de documentatie van de Admin Console.

>[!NOTE]
>
>Een systeembeheerder van het systeem van de Admin Console kan deze stappen uitvoeren.

1. Login aan [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Selecteer de tab **[!UICONTROL Users]** .

1. Kies **[!UICONTROL User Groups]** in de linkernavigatie.

1. Klik op **[!UICONTROL New user group]** rechtsboven.

1. Ga een naam voor de gebruikersgroep, zoals _StandaardGebruikers_ in en klik **[!UICONTROL Save]**.

1. Klik op de gebruikersgroep die u zojuist hebt gemaakt.

1. Selecteer de tab **[!UICONTROL Assigned product profiles]** en klik op **[!UICONTROL Assign profile]** .

1. Klik **+** en voeg elke instantie van de volgende producten toe:

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Adobe Experience Platform Data Collection]
   * [!UICONTROL Data Collection All Access]

   ![ Admin Console - gebruiker-groep - voeg producten ](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save]**.

## Een rol maken in AEP-machtigingen {#create-role}

Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die aan een productprofiel zijn toegewezen. Elke toestemming wordt verzameld onder een mogelijkheid, zoals reizen of inkoopgroepen, die de verschillende functies of objecten in Journey Optimizer B2B Edition vertegenwoordigt.

Het _gebied van Toestemmingen_ van Adobe Experience Platform is waar de beheerders gebruikersrollen en toegangsbeleid kunnen bepalen om toegangstoestemmingen voor eigenschappen en voorwerpen binnen een producttoepassing te beheren. In deze app kunt u rollen maken en beheren en kunt u de gewenste resourcemachtigingen voor deze rollen toewijzen. Met machtigingen kunt u ook de labels, sandboxen en gebruikers beheren die aan een specifieke rol zijn gekoppeld.

Voor meer informatie, zie [ toestemmingen voor een rol ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) in de documentatie van het Experience Platform beheren.

>[!NOTE]
>
>Als u de volgende stappen wilt uitvoeren, moet u een productbeheerder voor Adobe Experience Platform zijn.

1. Ga naar [ experience.adobe.com ](https://experience.adobe.com/).

1. Selecteer **[!UICONTROL Permissions]** in het deelvenster _[!UICONTROL Quick access]_.

   >[!NOTE]
   >
   >Als u _[!UICONTROL Permissions]_niet ziet, moet u mogelijk op **[!UICONTROL View all]**klikken en deze selecteren in de beschikbare toepassingen.

   ![ Experience Platform - toegangstoestemmingen ](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Selecteer **[!UICONTROL Roles]** in de linkernavigatie en selecteer **[!UICONTROL Create role]**.

1. In de _[!UICONTROL Create new role]_dialoog, ga een naam voor de rol, zoals_ AJO B2B _in, en een beschrijving (facultatief).

1. Klik op **[!UICONTROL Confirm]**.

1. Selecteer uw sandboxen.

   ![ Experience Platform - voeg zandbakken voor de nieuwe rol toe ](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Voeg de profielmachtigingen toe:

   * Zoek in de lijst _[!UICONTROL Resources]_aan de linkerkant het **[!UICONTROL Profile Management]**-item en klik op de plusknop (**+**) om het kenmerk toe te voegen.

   * Voeg voor het kenmerk de volgende machtigingen toe:
      * [!UICONTROL View segments]
      * [!UICONTROL Manage segments]
      * [!UICONTROL View profiles]
      * [!UICONTROL Manage profiles]
      * [!UICONTROL View B2B profile]
      * [!UICONTROL Manage B2B profile]

   ![ Experience Platform - voeg profielen voor de nieuwe rol ](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save]** rechtsboven.

1. Ga naar de details van de rol en selecteer de tab **[!UICONTROL User groups]** .

1. Klik op **[!UICONTROL Add Groups]**.

   ![ Experience Platform - voeg profielen voor de nieuwe rol ](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"} toe

1. Schakel het selectievakje naast de gebruikersgroep in die u eerder in de Admin Console hebt gemaakt.

1. Klik op **[!UICONTROL Save]**.

## Gebruikers toevoegen aan de groep in de Admin Console

>[!NOTE]
>
>Een systeembeheerder van het systeem van de Admin Console of een productbeheerder kan deze stappen uitvoeren.

Voor informatie over gebruikersbeheer, zie [ gebruikers van de Admin Console ](https://helpx.adobe.com/enterprise/using/user-groups.html) in de documentatie van de Admin Console.

1. Ga naar [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Klik onder _[!UICONTROL Quick links]_op **[!UICONTROL Add users]**.

1. Voeg elke gebruiker toe:

   * Voer het e-mailadres, de voornaam en de achternaam van de gebruiker in.

     ![ Experience Platform - voeg profielen voor de nieuwe rol ](./assets/admin-console-add-users.png){width="600" zoomable="yes"} toe

   * Voor **[!UICONTROL User groups]**, klik **+**.

   * Selecteer de gebruikersgroep die u eerder hebt gemaakt.

   * Klik op **[!UICONTROL Apply]**.

1. Klik op **[!UICONTROL Save]**.
