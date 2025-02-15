---
title: Gebruikersbeheer
description: Leer hoe u teamleden toewijst aan Journey Optimizer B2B edition-productprofielen.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: d5197e740a17de507bf72b4d7b64deb5af672346
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# Gebruikersbeheer

Nadat de levering is voltooid en de zandbakken verbindend zijn, voltooi de volgende stappen om Adobe Journey Optimizer B2B edition toegang voor uw team en gebruikers te verlenen.

1. [ creeer een het productprofiel van Marketo Engage ](#marketo-engage-profile) in Admin Console (nieuwe instantie van Marketo Engage slechts).
1. [ creeer een gebruikersgroep ](#create-user-group) in Admin Console.
1. [ geef ingebouwde rollen ](#edit-roles) uit of [ creeer een douanerol ](#create-a-custom-role) met de toestemmingen van Journey Optimizer B2B edition.
1. [ voegt gebruikers ](#add-users) of [ groepen ](#add-user-groups-to-a-role) aan rollen toe.

Als beheerder kunt u deze taken uitvoeren in de Adobe Admin Console, een centrale plaats voor het beheer en beheer van uw Adobe-productlicenties en -gebruikers. In de Admin Console kunt u gebruikers maken en beheren op één locatie in plaats van binnen uw verschillende individuele oplossingen. Verwijs naar de [ overzicht van Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html) pagina om meer over zijn functies en mogelijkheden te leren.

## Toegang tot de Admin Console

Voordat u de Admin Console kunt gebruiken om gebruikers binnen uw team te beheren, moet u ervoor zorgen dat u toegang hebt tot de Admin Console en over de juiste machtigingen beschikt.

1. Als systeembeheerder ontvangt u meerdere e-mails van Adobe als onderdeel van het instapproces.

   Zoek de welkomstmail die de informatie over de organisatienaam verstrekt waaraan u toegang hebt verleend.

1. Klik op de koppeling **[!UICONTROL Get started]** in uw welkomstbericht om naar de Admin Console te navigeren.

   Als u niet e-mail kunt vinden, open direct browser aan Admin Console in [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Meld u aan met uw Adobe ID.

   Op succesvolle login, ziet u de _pagina van het Overzicht_ van Adobe Admin Console.

1. Als u toegang tot veelvoudige organisaties hebt, zorg ervoor dat u aan de correcte organisatie hebt het programma geopend.

   Als u uw organisatie wilt wijzigen, klikt u in de rechterbovenhoek op de naam van de organisatie en kiest u de organisatie waartoe u toegang nodig hebt.

1. Selecteer **[!UICONTROL Administrators]** op de _[!UICONTROL Users]_-kaart om te controleren of u systeembeheerder bent.

   ![ overzicht van Admin Console - klik Beheerders ](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Zoek door je Adobe ID-e-mail, gebruikersnaam, voornaam of achternaam in te voeren.

   * Als uw toegang correct wordt gevormd, keert het onderzoek uw verslag terug.

   * Als de waarde in de kolom **[!UICONTROL ADMIN ROLE]** `System` toont, weet u dat u (of de getoonde gebruiker) een systeembeheerder bent.

## Het Marketo Engage-productprofiel maken {#marketo-engage-profile}

Wanneer u gebruikers toegang geeft tot een Adobe-oplossing, wilt u ze niet altijd volledige toegang geven. Met productprofielen kan elke oplossing beschikken over een eigen set gebruikersrechten. Gebruik de Admin Console om productprofielen toe te wijzen.

Voor meer informatie over het gebruiken van productprofielen voor gebruikersrechten, zie [ productprofielen voor ondernemingsgebruikers beheren ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) {target="_blank"} in de documentatie van Admin Console.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

![ de rolvereisten van de Beheerder ](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Een systeembeheerder of het productbeheerder van Marketo Engage kan de volgende stappen uitvoeren.

1. Login aan [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Selecteer de tab **[!UICONTROL Products]** .

1. Open de Marketo Engage-instantie waar u het profiel wilt toevoegen en klik op **[!UICONTROL New profile]** .

   ![ Admin Console - de instantie van Marketo Engage - Nieuw profiel ](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Ga een naam van het productprofiel, zoals _StandaardGebruiker_ in.

1. Klik **daarna** en dan **sparen**.

## Een gebruikersgroep maken {#create-user-group}

Een gebruikersgroep is een inzameling van gebruikers wordt verleend een gedeelde reeks toestemmingen. U kunt gebruikers toevoegen aan of verwijderen uit uw gebruikersgroep. De machtigingen voor de groep blijven ongewijzigd wanneer de gebruikers in de groep worden gewijzigd.

Voor meer informatie over hoe de gebruikersgroepen worden gebruikt om toestemmingen te beheren, zie [ gebruikersgroepen beheren ](https://helpx.adobe.com/enterprise/using/user-groups.html) {target="_blank"} in de documentatie van Admin Console.

![ de rolvereisten van de Beheerder ](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Een systeembeheerder kan de volgende stappen uitvoeren.

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

## Gebruikers aan een groep toevoegen

Voor informatie over gebruikersbeheer, zie [ de gebruikers van Admin Console ](https://helpx.adobe.com/enterprise/using/user-groups.html) in de documentatie van Admin Console.

![ de rolvereisten van de Beheerder ](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Een systeembeheerder of productbeheerder kunnen de volgende stappen uitvoeren. Een productbeheerder kan alleen gebruikers toevoegen die al in zijn organisatie bestaan.

1. Ga naar [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Klik onder _[!UICONTROL Quick links]_op **[!UICONTROL Add users]**.

1. Voeg elke gebruiker toe:

   * Voer het e-mailadres, de voornaam en de achternaam van de gebruiker in.

     ![ Experience Platform - voeg profielen voor de nieuwe rol ](./assets/admin-console-add-users.png){width="600" zoomable="yes"} toe

   * Voor **[!UICONTROL User groups]**, klik **+**.

   * Selecteer de gebruikersgroep die u eerder hebt gemaakt.

   * Klik op **[!UICONTROL Apply]**.

1. Klik op **[!UICONTROL Save]**.

## Rollen bewerken voor productmachtigingen {#edit-roles}

Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die aan een productprofiel zijn toegewezen. Elke toestemming wordt verzameld onder een mogelijkheid, zoals reizen of inkoopgroepen, die de verschillende functies of objecten in Journey Optimizer B2B edition vertegenwoordigt.

Het _gebied van Toestemmingen_ van Adobe Experience Platform is waar de beheerders gebruikersrollen en toegangsbeleid kunnen bepalen om toegangstoestemmingen voor eigenschappen en voorwerpen binnen een producttoepassing te beheren. In deze app kunt u rollen maken en beheren en kunt u de gewenste resourcemachtigingen voor deze rollen toewijzen. Met machtigingen kunt u ook de sandboxen en gebruikers beheren die aan een specifieke rol zijn gekoppeld.

Voor meer informatie over roltoestemmingen in Experience Platform, zie [ toestemmingen voor een rol ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) beheren {target="_blank"} in de documentatie van Experience Platform.
<!-- 
### B2B product permissions

The following permissions govern access to Journey Optimizer B2B Edition capabilities:

| Category | Description | Permissions |
| -------- | ----------- | ---------- |
| B2B Account Lists | Configure, manage, view, and publish permissions for B2B account lists. These permissions include actions such as add, remove, import, and delete accounts from account lists. | <li>Manage B2B Account Lists |
| B2B Admin Configurations | Configure, manage, and view permissions for B2B administrative configurations. These permissions include digital asset management connections, asset repositories, and events. | <li>Manage B2B Admin Configurations |
| B2B Assets | Configure, manage, and view permissions for B2B assets. These permissions include emails, SMS, landing pages, fragments, templates, and images. | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments|
| B2B Buying Groups | Configure, manage, and view permissions for B2B buying groups. These permissions include solution interests, roles templates, and buying group status. | <li>Manage B2B Buying Groups |
| B2B Channel Configurations | Configure, manage, and view permissions for B2B channel configurations. These permissions include settings for communication limits, API credentials, and security settings. | <li>Manage B2B Channels Configurations |
| B2B Dashboards |Configure and view permissions for B2B dashboards. These permissions include account engagement, buying group stages, surging accounts, and contact coverage. | <li>Manage B2B Dashboards |
| B2B Journeys | Configure manage, view, and publish permissions for B2B journeys. These permissions include account and person actions, event listeners, and split paths | <li>Manage B2B Journeys |

### B2B built-in roles

When your organization has the Journey Optimizer B2B Edition product provisioned, Experience Platform includes a set of built-in (default) roles that you can use to manage access to the product capabilities:

| Role | Permissions |
| ---- | ----------- |
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Intelligent Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View Intelligent Dashboard |

### Edit role permissions

For built-in or custom roles, you can decide at any time to add or delete permissions. If you modify a default or custom role, it impacts every user assigned to the role.

In the following example, you want to add permissions related to the B2B Journeys resource for users assigned to the B2B Channel Manager role. This change enables users for that role to manage account journeys also.

>[!NOTE]
>
>An Admin Console system administrator can perform these steps.

_To change the permissions for a role:_

1. Go to [experience.adobe.com](https://experience.adobe.com/).

1. In the _[!UICONTROL Quick access]_ panel, select **[!UICONTROL Permissions]**.

   >[!NOTE]
   >
   >If you don't see _[!UICONTROL Permissions]_, you may need to click **[!UICONTROL View all]** and select it from the available applications.

   ![Experience Platform - access Permissions](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Select **[!UICONTROL Roles]** in the left navigation.

1. Click the **_B2B Channel Manager_** role name.

1. In the details page, click **[!UICONTROL Edit]** at the top right.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   In the role editor, the _[!UICONTROL Resources]_ menu displays the list of resources that apply to the Experience Cloud - Platform powered applications products.

   You can enter _B2B_ in the search tool to filter the list for the B2B product permissions. 
   
1. Click the _Add_ icon (**+**) for the B2B Journeys resource.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-add.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL B2B Journeys]_ permissions card, select **[!UICONTROL Manage B2B Account Journeys]**.

1. Click **[!UICONTROL Save]**.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Close]** to return to the details page. -->

### Gebruikers aan een rol toevoegen

![ de rolvereisten van de Beheerder ](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Een systeembeheerder of AEP productbeheerder kan de volgende stappen uitvoeren.

1. Open de roldetails en selecteer het **[!UICONTROL Users]** lusje.

   Op dit tabblad wordt een lijst weergegeven met alle gebruikers die aan de rol zijn toegewezen.

1. Klik op **[!UICONTROL Add users]**.

   ![ Experience Platform - voeg gebruikers aan de rol ](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"} toe

1. Zoek in het dialoogvenster _[!UICONTROL Add users]_de gebruikers die u aan de rol wilt toevoegen en selecteer deze.

   * Met het gereedschap Zoeken kunt u de lijst met gebruikers filteren.

   * Schakel het selectievakje voor elke gebruiker in.

   ![ Experience Platform - voeg gebruikersdialoog ](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save]** als u alle gebruikers hebt geselecteerd die u wilt toevoegen.

### Gebruikersgroepen toevoegen aan een rol

Voor informatie over gebruikersbeheer, zie [ de gebruikers van Admin Console ](https://helpx.adobe.com/enterprise/using/user-groups.html) in de documentatie van Admin Console.

![ de rolvereisten van de Beheerder ](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Een systeembeheerder of AEP productbeheerder kan de volgende stappen uitvoeren.

1. Open de roldetails en selecteer het **[!UICONTROL User groups]** lusje.

   Op dit tabblad wordt een lijst weergegeven met alle gebruikersgroepen die aan de rol zijn toegewezen.

1. Klik op **[!UICONTROL Add Groups]**.

   ![ Experience Platform - voeg gebruikers aan de rol ](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"} toe

1. Zoek in het dialoogvenster _[!UICONTROL Add groups]_de groepen die u aan de rol wilt toevoegen en selecteer deze.

   * Met het gereedschap Zoeken kunt u de lijst met gebruikersgroepen filteren.

   * Schakel het selectievakje voor elke gebruikersgroep in.

   ![ Experience Platform - voeg de dialoog van groepen ](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"} toe

1. Klik op **[!UICONTROL Save]** als u alle gebruikers hebt geselecteerd die u wilt toevoegen.

## Een aangepaste rol maken

![ de rolvereisten van de Beheerder ](../../assets/do-not-localize/icon-admin-user.svg){width="30"} Een systeembeheerder of AEP productbeheerder kan de volgende stappen uitvoeren.

1. Selecteer **[!UICONTROL Roles]** in de linkernavigatie en selecteer **[!UICONTROL Create role]**.

1. In de _[!UICONTROL Create new role]_dialoog, ga een naam voor de rol, zoals_ B2B Marketers _, en een beschrijving (facultatief) in.

1. Klik op **[!UICONTROL Confirm]**.

1. Selecteer uw sandboxen.

   ![ Experience Platform - voeg zandbakken voor de nieuwe rol toe ](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Voeg de profielmachtigingen toe:

   * In de _[!UICONTROL Resources]_lijst op de linkerzijde, bepaal de plaats van het **[!UICONTROL Profile Management]**punt en klik_ toevoegen _(**+**) pictogram om de attributen toe te voegen.

   * Voeg voor het kenmerk de volgende machtigingen toe:
      * [!UICONTROL View segments]
      * [!UICONTROL Manage segments]
      * [!UICONTROL View profiles]
      * [!UICONTROL Manage profiles]
      * [!UICONTROL View B2B profile]
      * [!UICONTROL Manage B2B profile]

   ![ Experience Platform - voeg profielen voor de nieuwe rol ](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"} toe

1. B2B-productmachtigingen toevoegen:

   Verwijs naar de lijst van [ B2B producttoestemmingen ](#b2b-product-permissions) om te bepalen welke productmogelijkheden die u voor de rol wilt.

   In de _[!UICONTROL Resources]_lijst op de linkerzijde, bepaal de plaats van de **[!UICONTROL B2B]**punten en klik_ _toevoegen (**+**) pictogram om elk attribuut toe te voegen dat u voor de rol wilt toelaten.

   U kunt _B2B_ in het onderzoekshulpmiddel ingaan om de lijst voor de B2B producttoestemmingen te filtreren.

1. Klik op **[!UICONTROL Save]** rechtsboven.

1. Ga naar de details van de rol en selecteer de tab **[!UICONTROL User groups]** .

1. Klik op **[!UICONTROL Add Groups]**.

   ![ Experience Platform - voeg profielen voor de nieuwe rol ](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"} toe

1. Schakel het selectievakje in naast de gebruikersgroep die u eerder in de Admin Console hebt gemaakt.

1. Klik op **[!UICONTROL Save]**.
