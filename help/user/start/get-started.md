---
title: Begeleiding aan boord voor beheerders en markeertekens
description: 'Onboardinggids voor beheerders en marketeers: stel sandboxes in, configureer kanalen, maak inkoopgroepen en ontwerp accounttrajecten in Journey Optimizer B2B Edition.'
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 32b36690e76a4920a87bdd6c2fff85158c22d0e7
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 7%

---

# Richtlijnen voor onboarding

De functies en gereedschappen die u in Adobe Journey Optimizer B2B edition wilt gebruiken, zijn afhankelijk van uw rol binnen uw team. Op basis van uw organisatie kunnen beheerders verschillende typen gebruikers definiëren en hun toegang verlenen tot bepaalde mogelijkheden, afhankelijk van hun machtigingen.

>[!TIP]
>
>Controleer ook uw vergunningsrechten en de overeenkomstige [ productbeschrijving ](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} over prestatiesgaranties en statische beperkingen.

>[!BEGINTABS]

>[!TAB  Beheerder ]

Voordat uw team de Adobe Journey Optimizer B2B edition-functies kan gaan gebruiken, moet u verschillende stappen uitvoeren om uw omgeving voor te bereiden. Voer deze stappen uit zodat de gegevenstechnicus en de markeerfunctie kunnen gaan werken met Adobe Journey Optimizer B2B edition.

Als systeembeheerder, moet u productprofielen begrijpen en toestemmingen voor zandbakbeleid en kanaalconfiguratie toewijzen. U moet ook sandboxen instellen en deze beheren voor de beschikbare productprofielen. U kunt vervolgens teamleden toewijzen aan de productprofielen. Productbeheerders die toegang hebben tot de Adobe Admin Console kunnen deze mogelijkheden beheren. [ leer meer over Adobe Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html).

Meer informatie over toegangsbeheer vindt u op de volgende pagina&#39;s:

1. **creeer zandbakken** om uw instanties in afzonderlijke, geïsoleerde virtuele milieu&#39;s te verdelen. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **Werk met uw gegevensingenieur** om uw B2B publiek en profielactivering te plannen en uit te voeren. Bekijk de gepubliceerde blauwdrukken en volg de richtlijnen op basis van uw vereisten. [Meer informatie](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **Plan en voer de integratie van Marketo Engage** uit om douaneschema, opname van profielen en rekeningen, en de orchestratie van gepersonaliseerde reizen voor het kopen van groepen op te nemen. [Meer informatie](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/b2b-activation/b2b-journeys-with-marketo){target="_blank"}

1. **opstelling het productprofiel**. Een productprofiel is een reeks eenheidrechten in Adobe Experience Platform die gebruikers toegang tot bepaalde functies of objecten in de interface biedt. [Meer informatie](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **de toestemmingen van de Opstelling van de gebruikerstoestand** voor productprofielen, met inbegrip van zandbakken, en geven toegang tot uw teamleden door hen aan verschillende productprofielen toe te wijzen. Deze taak wordt uitgevoerd in de Admin Console. [Meer informatie](../admin/user-management.md#create-a-user-group)

1. **vorm klassen XDM en gebieden** om de gegevens te controleren die voor reis orchestration en inhoudsverpersoonlijking Journey Optimizer B2B edition beschikbaar zijn. [Meer informatie](../admin/xdm-field-management.md)

1. **vorm e-maillevering** in Marketo Engage, die uw team toelaat om e-mailinhoud van rekeningsreizen te verzenden. [Meer informatie](../admin/configure-channels-emails.md){target="_blank"}

1. **vorm de diensten van SMS**. Stel een van de ondersteunde SMS-providers van derden in die de services voor tekstberichten onafhankelijk aanbieden en de accountgegevens in Adobe Journey Optimizer B2B edition configureren. [Meer informatie](../admin/configure-channels-sms.md)

1. **vorm en laat gebruik van Adobe Experience Manager Assets** voor teams toe die Assets as a Cloud Service voor gecentraliseerd digitaal activabeheer gebruiken. [Meer informatie](../admin/configure-aem-repositories.md)

1. **de definities van de Gebeurtenis van de Ervaring van de Opstelling Adobe Experience Platform (AEP)** voor teams verantwoordelijk voor het creëren van rekeningsreizen die aan de Gebeurtenissen van de Ervaring van AEP luisteren. [Meer informatie](../admin/configure-aep-events.md)

>[!TAB  Marketer ]

Als marktleider, of een _Praktijk van de Reis van de Rekening_, bent u verantwoordelijk voor het ontwerpen van reizen en het creëren van inhoud. U kunt met Adobe Journey Optimizer B2B edition beginnen te werken nadat de systeembeheerder en de gegevensengineer uw omgeving hebben voorbereid en u toegang hebben verleend.

Raadpleeg de volgende secties voor het instellen van de eerste rit, het toevoegen van elementen en het verzenden van inhoud:

1. **voeg rekeningspubliek** toe. Met Journey Optimizer B2B edition kunt u accountpubliek maken via segmentdefinities direct vanuit de toepassing en deze gebruiken voor reizen naar uw account. [Meer informatie](../audiences/account-audience-overview.md)

1. **creeer het kopen groepen**. Definieer de belangrijkste componenten voor het bereiken van uw bedrijfsdoelstellingen en -doelstellingen en maak inkoopgroepen die de leden voor uw doelaccountlijsten identificeren. [Meer informatie](../buying-groups/buying-groups-overview.md)

1. **creeer en beheer activa**. Adobe Experience Manager Assets biedt één gecentraliseerde opslagplaats voor middelen die u kunt gebruiken om uw berichten te vullen. [Meer informatie](../content/assets-overview.md)

1. **voeg gepersonaliseerde en dynamische e-mailmalplaatjes** toe. Gebruik Journey Optimizer B2B edition-mogelijkheden voor personalisatie en dynamische inhoud om uw boodschap aan te passen aan uw publiek. [Meer informatie](../content/email-templates.md)

1. **de rekeningsritten van het Ontwerp om gepersonaliseerde, contextuele ervaringen** te leveren. Met Journey Optimizer B2B edition kunt u gebruiksscenario&#39;s voor realtime orchestratie maken met contextuele gegevens die zijn opgeslagen in gebeurtenissen of gegevensbronnen. Het ontwerp multi-step, geavanceerde scenario&#39;s aangedreven door de volgende mogelijkheden:

   * Eenmalige levering in real time wordt geactiveerd wanneer een gebeurtenis wordt ontvangen, of in batch met Adobe Experience Platform-publiek.

   * Gebruik contextuele gegevens van gebeurtenissen, informatie van Adobe Experience Platform of gegevens van externe API-services.

   * Gebruik de ingebouwde kanaalacties (e-mail en SMS) om berichten te verzenden die in Journey Optimizer B2B edition zijn ontworpen.

   * In het reisoverzicht, bouw uw multi-step gebruiksgevallen, voeg voorwaarden toe en verzend gepersonaliseerde berichten.

[Meer informatie](../journeys/journey-overview.md)

>[!ENDTABS]
