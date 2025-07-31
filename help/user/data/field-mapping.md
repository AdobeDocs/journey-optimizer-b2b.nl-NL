---
title: XDM-velden
description: Controleer de standaardkenmerkvelden die zijn gesynchroniseerd tussen de Adobe Experience Platform en Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: b62891e3d87ac4ff5345dac564d63c0b8aaa9669
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 6%

---

# XDM-velden

Accountpublieksgegevens worden opgeslagen als kenmerken in zowel de XDM Business Account- als de XDM Business Person-klassen. De gegevens worden periodiek gesynchroniseerd tussen Adobe Experience Platform en Journey Optimizer B2B edition. In de volgende secties worden de standaardsets met kenmerken weergegeven.

>[!TIP]
>
>U kunt de klassen van de Zakelijke Persoon XDM en van de Zakelijke Rekening XDM in een vele-aan-vele verhouding modelleren door de klasse van de Verhouding van de Person van de Onderneming XDM te gebruiken XDM zoals die in de [ documentatie XDM van Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"} wordt beschreven.

## Kenmerken XDM Zakelijke account persoon relatie

| [ Bezit ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Weergavenaam | Journey Optimizer B2B-weergavenaam | Gegevenstype | Beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Personrollen | Functie | Tekenreeksarray | Een array met rollen die aan de persoon op de account zijn gekoppeld, zoals `owner, accountant, designer` . |

## Kenmerken XDM-bedrijfsnaam

>[!IMPORTANT]
>
>Het e-mailadreskenmerk is vereist en moet worden ingevuld voor de juiste functionaliteit. Standaard gebruikt het systeem `workEmail.Address` . Als u een verschillend attribuut van plan bent te gebruiken, contacteer de Steun van Adobe alvorens om het even welke reizen te publiceren om juiste configuratie te verzekeren.<br/>
>
>Zorg ervoor dat het e-mailkenmerk niet null is, omdat dit van invloed kan zijn op gegevenssynchronisatie en downstreamprocessen.
><ul><li>Als het e-mailkenmerk null is in CDP B2B in realtime en de persoon bestaat in Journey Optimizer B2B edition, wordt het kenmerk in overschreven in Journey Optimizer B2B edition met de waarde null tijdens de synchronisatie. Vervolgens blijft de waarde null in Marketo Engage.<li>Als het e-mailkenmerk null is in CDP B2B in realtime en de persoon niet bestaat in Journey Optimizer B2B edition, wordt het persoonrecord niet gesynchroniseerd.<ul/>

| [ Bezit ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Weergavenaam | Journey Optimizer B2B-weergavenaam | Gegevenstype | Beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | Indicator voor het in de handel brengen | Marketing opgeschort | Boolean | De waarde geeft aan of het op de markt brengen is opgeschort voor de persoon. |
| `b2b.marketingSuspendedCause` | Handelsgewijze oorzaak | Handelsgewijze oorzaak | String | Als het op de markt brengen voor de persoon wordt opgeschort, verstrekt dit bezit de reden waarom. |
| `b2b.personStatus` | Status persoon | Leadstatus | String | Veld waar de huidige marketing-/verkoopstatus van de persoon wordt geregistreerd. |
| `consents.marketing.email.reason` | Opt-out reden | Reden voor niet geabonneerd | String | Reden voor de e-mailopt-out. |
| `consents.marketing.email.val` | Niet geabonneerd | Niet geabonneerd | String | Als unsubscribed waar is (bijvoorbeeld waarde = 1), stelt u `consents.marketing.email.val` in als (n). Als unsubscribed false is (bijvoorbeeld value = 0), stelt u `consents.marketing.email.val` in als null. |
| `extendedWorkDetails.jobTitle` | Beroep | Beroep | String | Functie van de persoon. |
| `faxPhone.number` | Getal | Faxnummer | String | Telefoonnummer fax. |
| `mobilePhone.number` | Getal | Mobiel | String | Het mobiele telefoonnummer dat aan de persoon is gekoppeld. |
| `person.birthDate` | Geboortedatum (JJJ-MM-DD) | Geboortedatum | String | De volledige datum waarop een persoon is geboren. YYYY-MM-DD |
| `person.name.courtesyTitle` | Titel met dank | Aanhef | String | Normaal gesproken een afkorting van de titel, de eer of de aanhef van een persoon. De courtesyTitle wordt gebruikt voor de volledige of achternaam in het openen van teksten. Bijvoorbeeld meneer, mevrouw of dr. |
| `person.name.firstName` | Voornaam | Voornaam | String | Het eerste segment van de naam in de geschreven orde die het meest algemeen in de taal van de naam wordt toegelaten. In veel culturen heeft het de voorkeur voor een persoonlijke of voornaam. De eigenschappen firstName en lastName zijn geïntroduceerd om verenigbaarheid met bestaande systemen te handhaven die modelnamen op een vereenvoudigde, niet-semantische, en niet-internationaliseerbare manier modelleren. Het gebruik van `xdm:fullName` heeft altijd de voorkeur. |
| `person.name.lastName` | Achternaam | Achternaam | String | Het laatste segment van de naam in de geschreven orde die het meest algemeen in de taal van de naam wordt toegelaten. In veel culturen is dit de overgeërfde familienaam, achternaam, patronymische of matronymische naam. De eigenschappen firstName en lastName zijn geïntroduceerd om verenigbaarheid met bestaande systemen te handhaven die modelnamen op een vereenvoudigde, niet-semantische, en niet-internationaliseerbare manier modelleren. Het gebruik van `xdm:fullName` heeft altijd de voorkeur. |
| `person.name.middleName` | Tussenvoegsel | Tussenvoegsel | String | Midden-, alternatieve of aanvullende namen opgegeven tussen de voornaam en achternaam. |
| `workAddress.city ` | Stad | Stad | String | De naam van de stad. |
| `workAddress.country` | Land | Land | String | De naam van het door de overheid bestuurde gebied. Met uitzondering van `xdm:countryCode` is het een veld met vrije vorm dat de naam van het land in elke taal kan hebben. |
| `workAddress.postalCode` | Postcode | Postcode | String | De postcode van de locatie. Postcodes zijn niet voor alle landen beschikbaar. In sommige landen bevat het slechts een deel van de postcode. |
| `workAddress.state` | Staat | Staat | String | De naam van de staat voor het adres. Het is een veld met vrije vorm. |
| `workAddress.street1` | Adres 1 | Adres | String | Primaire straatinformatie, appartementnummer, straatnummer en straatnaam. |
| `workEmail.address` | Adres | E-mailadres | String | **Vereist gebied** <br/> het technische adres, bijvoorbeeld, `<name@domain.com>` zoals algemeen bepaald in RFC2822 en verdere normen. |
| `workEmail.status` | Status | E-mail opgeschort | String | Een indicatie van de mogelijkheid om het e-mailadres te gebruiken. |
| `workPhone.number` | Getal | Telefoonnummer | String | Telefoonnummer zakelijk. |

## Kenmerken van XDM Business Account

>[!IMPORTANT]
>
>Het attribuut `accountName` is vereist. Als de account voor een account in een accountpubliek leeg is, wordt dat account niet opgenomen en weggelaten voor reizen naar en het kopen van groepen die naar het publiek verwijzen.

| [ Bezit ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | Weergavenaam | Journey Optimizer B2B-weergavenaam | Gegevenstype | Beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Stad | Stad | String | De naam van de stad die in het factuuradres wordt gebruikt. |
| `accountBillingAddress.country` | Land | Land | String | De naam van het door de overheid bestuurde gebied dat in het factuuradres wordt gebruikt. Met uitzondering van `xdm:countryCode` is het een veld met vrije vorm dat de naam van het land in elke taal kan hebben. |
| `accountBillingAddress.postalCode` | Postcode | Postcode adres | String | De postcode van de plaats van het factureringsadres. Postcodes zijn niet voor alle landen beschikbaar. In sommige landen bevat het slechts een deel van de postcode. |
| `accountBillingAddress.region` | Regio | Adresregio | String | Het gebied, het graafschap, of het districtsgedeelte van het factureringsadres. |
| `accountBillingAddress.state` | Staat | Staat | String | De naam van de staat voor het factureringsadres. Het is een veld met vrije vorm. |
| `accountBillingAddress.street1` | Adres 1 | Adres 1 | String | Informatie op het primaire straatniveau voor het factuuradres, die typisch het flatnummer, straatnummer en straatnaam zou omvatten. |
| `accountName` | Naam | Naam | String | **Vereiste gebied** <br/> Naam van het bedrijf. Dit veld mag maximaal 255 tekens bevatten. |
| `accountOrganization.annualRevenue.amount` | Jaaromzet | Jaaromzet | Getal | Geraamde jaarlijkse inkomsten van de organisatie. |
| `accountOrganization.industry` | Marktsegment | Marktsegment | String | De bedrijfstak die aan de organisatie is toegeschreven. Het is een vrij-vormgebied, en het is raadzaam om een gestructureerde waarde voor vragen te gebruiken of het `xdm:classifier` bezit te gebruiken. |
| `accountOrganization.logoUrl` | Logo URL | Logo URL | String | Pad dat moet worden gecombineerd met de URL van een Salesforce-instantie (bijvoorbeeld `https://yourInstance.salesforce.com/` ) om een URL te genereren voor het aanvragen van de afbeelding van het profiel van het sociale netwerk die aan de account is gekoppeld. De gegenereerde URL retourneert een HTTP-omleiding (code 302) naar de afbeelding van het sociale netwerkprofiel voor de account. |
| `accountOrganization.numberOfEmployees` | Aantal werknemers | Aantal werknemers | Geheel | Het aantal werknemers in de organisatie. |
| `accountOrganization.SICCode` | SIC-code | SIC-code | String | De code Standard Industrial Classification (SIC) is een code van vier cijfers die de industrieën die bedrijven tot behoren, categoriseert op basis van hun bedrijfsactiviteiten. |
| `accountOrganization.website` | URL website | Domeinnaam | String | De URL van de website van de organisatie. |
| `accountPhone.number` | NVT | Telefoonnummer account | String | Het telefoonnummer dat aan de account is gekoppeld. |
| `accountSourceType` | NVT | Source-type | String | Source-type voor de account. |

<!-- ## XDM Business Opportunity attributes

Additionally, opportunity data is stored as attributes in the XDM Business Opportunity class, which can be associated with the XDM Business Account class through a many-to-one relationship, as described in the [Exerience Platform documentation](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`expectedCloseDate` | Expected Close Date  | Expected opportunity close date   | String | Expected date of closure for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | Total opportunity expected revenue   | String | Calculated revenue based on the Amount and Probability.   |
|`fiscalQuarter` | Fiscal Quarter   | Opportunity fiscal quarter  | String | The targeted fiscal quarter for the opportunity.   |
|`fiscalYear` | Fiscal Year   | Opportunity fiscal year   | String | The targeted fiscal year for the opportunity.   |
|`forecastCategory`|Forecast Category | Opportunity Forecast category | String | Forecast Category determined by the opportunity Stage value. |
|`forecastCategoryName`|Forecast Category Name | Opportunity forecast category name | String | Forecast category name that is displayed in reports for a particular forecast category. |
|`isClosed` | Closed Flag  | Opportunity closed   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | Opportunity won   | String | Flag that indicates if the opportunity is won.  |
|`lastActivityDate` | Last Activity Date  | Last activity date   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | Lead source   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | Opportunity next step   | String | Description of the next task for closing the opportunity.   |
|`opportunityAmount.amount` | Opportunity Amount  | Total Opportunity Amount | String | Estimated total sale amount for the opportunity.   |
|`opportunityDescription` | Opportunity Description   | Opportunity description  |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityName` | Opportunity Name   | Opportunity name |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityQuantity` | Opportunity Quantity  | Opportunity quantity   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`opportunityStage` | Opportunity Stage   | Opportunity stage   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`opportunityType` | Opportunity Type   | Opportunity type   | String | Type assigned to the opportunity, such as _Existing Business_ or _New Business_  |
|`probabilityPercentage` | Probability Percentage  | Opportunity probability percentage  | String | Likelihood of closing the opportunity, stated as a percentage.  |
 -->