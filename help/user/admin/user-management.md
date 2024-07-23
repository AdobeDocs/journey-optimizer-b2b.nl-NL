---
title: Gebruikersbeheer
description: Leer hoe u teamleden toewijst aan Journey Optimizer B2B Edition-productprofielen.
feature: Setup
roles: Admin
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '811'
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

   Als u zich met succes hebt aangemeld, wordt de overzichtspagina van de Adobe Admin Console weergegeven.

1. Als u toegang tot veelvoudige organisaties hebt, zorg ervoor dat u aan de correcte organisatie hebt het programma geopend.

   Als u uw organisatie wilt wijzigen, klikt u in de rechterbovenhoek op de naam van de organisatie en kiest u de organisatie waartoe u toegang nodig hebt.

1. Selecteer Beheerders op de gebruikerskaart om te controleren of u systeembeheerder bent.

1. Zoek door je Adobe ID-e-mail, gebruikersnaam, voornaam of achternaam in te voeren.

   * Als uw toegang correct wordt gevormd, keert het onderzoek uw verslag terug.

   * Als de waarde in de kolom **[!UICONTROL ADMIN ROLE]** `System` toont, weet u dat u (of de getoonde gebruiker) een systeembeheerder bent.

## Het productprofiel van het Marketo Engage maken {#marketo-engage-profile}

Wanneer het verlenen van toegang tot een oplossing van de Adobe, wilt u hen niet noodzakelijk volledige toegang verlenen. Met productprofielen kan elke oplossing beschikken over een eigen set gebruikersrechten. Gebruik de Admin Console om productprofielen toe te wijzen.

>[!NOTE]
>
>Deze stappen kunnen slechts door een systeembeheerder van het het systeem van de Admin Console of Marketo Engage productbeheerder worden uitgevoerd.

1. Login aan [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Kies Producten > Marketo Engage.

1. Klik Nieuw profiel en ga een naam van het productprofiel, zoals _StandaardGebruiker_ in.

1. Klik op Volgende > Opslaan

## Een gebruikersgroep maken {#create-user-group}

Een gebruikersgroep is een inzameling van gebruikers wordt verleend een gedeelde reeks toestemmingen. U kunt gebruikers toevoegen aan of verwijderen uit uw gebruikersgroep. De machtigingen voor de groep blijven ongewijzigd wanneer de gebruikers in de groep worden gewijzigd.

>[!NOTE]
>
>Deze stappen kunnen slechts door een systeembeheerder van het Admin Console worden uitgevoerd.

1. Login aan [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Kies **[!UICONTROL Users]** > **[!UICONTROL User Groups]** > **[!UICONTROL New user group]** .

1. Ga een naam voor de gebruikersgroep, zoals _StandaardGebruikers_ in en klik **[!UICONTROL Save]**.

1. Klik op de gebruikersgroep die u zojuist hebt gemaakt.

1. Klik op **[!UICONTROL Assigned product profiles]** > **[!UICONTROL Assign profile]** .

1. Selecteer de volgende producten:
   * [!UICONTROL Marketo Engage - Standard User]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Adobe Experience Platform Data Collection - Default]
   * [!UICONTROL Data Collection All Access]

1. Klik op **[!UICONTROL Save]**.

## Een rol maken in AEP-machtigingen {#create-role}

Machtigingen zijn eenheidrechten waarmee u de machtigingen kunt definiëren die aan een productprofiel zijn toegewezen. Elke toestemming wordt verzameld onder een mogelijkheid, zoals reizen of inkoopgroepen, die de verschillende functies of objecten in Journey Optimizer B2B Edition vertegenwoordigt.

_Toestemmingen_ is het gebied van Adobe Experience Platform waar de beheerders gebruikersrollen en toegangsbeleid kunnen bepalen om toegangstoestemmingen voor eigenschappen en voorwerpen binnen een producttoepassing te beheren. In deze app kunt u rollen maken en beheren en kunt u de gewenste resourcemachtigingen voor deze rollen toewijzen. Met machtigingen kunt u ook de labels, sandboxen en gebruikers beheren die aan een specifieke rol zijn gekoppeld.

>[!NOTE]
>
>Als u de volgende stappen wilt uitvoeren, moet u een productbeheerder voor Adobe Experience Platform zijn.

1. Ga naar [ experience.adobe.com ](https://experience.adobe.com/).

1. Selecteer **[!UICONTROL Permissions]** .

   >[!NOTE]
   >
   >Als u Rechten niet ziet, moet u mogelijk op Alles weergeven klikken en deze selecteren in de beschikbare toepassingen.

1. Selecteer **[!UICONTROL Roles]** in de linkernavigatie en selecteer **[!UICONTROL Create role]**.

1. In de _[!UICONTROL Create new role]_dialoog, ga een naam voor de rol, zoals_ StandaardGebruiker _in, en een beschrijving (facultatief).

1. Klik op **[!UICONTROL Confirm]**.

1. Selecteer uw sandboxen.

1. Voeg de profielmachtigingen toe:

   * Zoek in de lijst _[!UICONTROL Resources]_aan de linkerkant het **[!UICONTROL Profile Management]**-item en klik op de plusknop (**+**) om het kenmerk toe te voegen.

   * Voeg voor het kenmerk de volgende machtigingen toe:
      * [!UICONTROL View segments]
      * [!UICONTROL Manage segments]
      * [!UICONTROL View profiles]
      * [!UICONTROL Manage profiles]
      * [!UICONTROL View B2B profile]
      * [!UICONTROL Manage B2B profile]

1. Klik op **[!UICONTROL Save]** rechtsboven.

1. Kies **[!UICONTROL User groups]** > **[!UICONTROL Add Groups]** .

1. Schakel het selectievakje naast de gebruikersgroep in die u eerder in de Admin Console hebt gemaakt.

1. Klik op **[!UICONTROL Save]**.

## Gebruikers toevoegen aan de Admin Console

>[!NOTE]
>
>Deze stappen kunnen slechts door een systeembeheerder van het Admin Console of een productbeheerder worden uitgevoerd.

1. Ga naar [ https://adminconsole.adobe.com ](https://adminconsole.adobe.com).

1. Klik op **[!UICONTROL Add users]**.

1. Voeg elke gebruiker toe:

   * Voer het e-mailadres, de voornaam en de achternaam van de gebruiker in.
   * Klik op [!UICONTROL User groups].
   * Selecteer de gebruikersgroep die u eerder hebt gemaakt.

1. Klik op **[!UICONTROL Apply]**.

1. Klik op **[!UICONTROL Save]**.
