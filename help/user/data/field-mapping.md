---
title: XDM-veldtoewijzing
description: Bekijk de veldafbeelding tussen het AEP XDM-schema, het Marketo Engage en de Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 838308621a27bcfc6425b8683f642a66f1fa6a7b
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 7%

---

# XDM-veldtoewijzing

De Data Transfer Service (DTS) is verantwoordelijk voor het synchroniseren van gegevens van Adobe Experience Platform naar Journey Optimizer B2B Edition. DTS baseert zich op afbeeldingen tussen Experience Platform XDM schemagebieden en hun equivalenten in Marketo Engage.

## XDM Business Person standaardveldtoewijzingen

| [ XDM Bedrijfs Persoon ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | XDM-weergavenaam | Weergavenaam Marketo Engage | XDM-type | Marketo-type | XDM-beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `b2b.companyName` | Bedrijfsnaam | Bedrijfsnaam | string | string | De naam van het bedrijf waaraan een ondernemer is gekoppeld. |
| `b2b.companyWebsite` | Website van bedrijf | Website | string | url | Website van het bedrijf waaraan een ondernemer wordt geassocieerd. |
| `b2b.isMarketingSuspended` | Indicator voor het in de handel brengen | Marketing opgeschort | boolean | boolean | De waarde geeft aan of het op de markt brengen is opgeschort voor de persoon. |
| `b2b.marketingSuspendedCause` | Handelsgewijze oorzaak | Handelsgewijze oorzaak | string | string | Als het op de markt brengen voor de persoon wordt opgeschort, verstrekt dit bezit de reden waarom. |
| `b2b.personStatus` | Status persoon | Leadstatus | string | string | Veld waar de huidige marketing-/verkoopstatus van de persoon wordt geregistreerd. |
| `consents.marketing.email.reason` | Opt-out reden | Reden voor niet geabonneerd | string | string | Reden voor de e-mailopt-out. |
| `consents.marketing.email.val` | Niet geabonneerd | Niet geabonneerd | string | boolean | Als unsubscribed waar is (bijvoorbeeld waarde = 1), stelt u `consents.marketing.email.val` in als (n). Als unsubscribed vals is (bijvoorbeeld, waarde = 0), dan plaats toestemmingen.marketing.email.val als ongeldig. |
| `extendedWorkDetails.jobTitle` | Beroep | Beroep | string | string | Functie van de persoon. |
| `faxPhone.number` | Getal | Faxnummer | string | telefoon | Telefoonnummer fax. |
| `mobilePhone.number` | Getal | Mobiel | string | telefoon | Het mobiele telefoonnummer dat aan de persoon is gekoppeld. |
| `person.birthDate` | Geboortedatum (JJJ-MM-DD) | Geboortedatum | string | date | De volledige datum waarop een persoon is geboren. YYYY-MM-DD |
| `person.name.courtesyTitle` | Titel met dank | Aanhef | string | string | Normaal gesproken een afkorting van de titel, de eer of de aanhef van een persoon. De courtesyTitle wordt gebruikt voor de volledige of achternaam in het openen van teksten. Bijvoorbeeld meneer, mevrouw of dr. |
| `person.name.firstName` | Voornaam | Voornaam | string | string | Het eerste segment van de naam in de geschreven orde die het meest algemeen in de taal van de naam wordt toegelaten. In veel culturen heeft het de voorkeur voor een persoonlijke of voornaam. De eigenschappen firstName en lastName zijn geïntroduceerd om verenigbaarheid met bestaande systemen te handhaven die modelnamen op een vereenvoudigde, niet-semantische, en niet-internationaliseerbare manier modelleren. Het gebruik van `xdm:fullName` heeft altijd de voorkeur. |
| `person.name.lastName` | Achternaam | Achternaam | string | string | Het laatste segment van de naam in de geschreven orde die het meest algemeen in de taal van de naam wordt toegelaten. In veel culturen is dit de overgeërfde familienaam, achternaam, patronymische of matronymische naam. De eigenschappen firstName en lastName zijn geïntroduceerd om verenigbaarheid met bestaande systemen te handhaven die modelnamen op een vereenvoudigde, niet-semantische, en niet-internationaliseerbare manier modelleren. Het gebruik van `xdm:fullName` heeft altijd de voorkeur. |
| `person.name.middleName` | Tussenvoegsel | Tussenvoegsel | string | telefoon | Midden-, alternatieve of aanvullende namen opgegeven tussen de voornaam en achternaam. |
| `workAddress.city ` | Stad | Stad | string | string | De naam van de stad. |
| `workAddress.country` | Land | Land | string | string | De naam van het door de overheid bestuurde gebied. Met uitzondering van `xdm:countryCode` is het een veld met vrije vorm dat de naam van het land in elke taal kan hebben. |
| `workAddress.postalCode` | Postcode | Postcode | string | string | De postcode van de locatie. Postcodes zijn niet voor alle landen beschikbaar. In sommige landen bevat het slechts een deel van de postcode. |
| `workAddress.state` | Staat | Staat | string | string | De naam van de staat voor het adres. Het is een veld met vrije vorm. |
| `workAddress.street1` | Adres 1 | Adres | string | text | Primaire straatinformatie, appartementnummer, straatnummer en straatnaam. |
| `workEmail.address` | Adres | E-mailadres | string | email | Het technische adres, bijvoorbeeld, `<name@domain.com>` zoals algemeen bepaald in RFC2822 en verdere normen. |
| `workEmail.status` | Status | E-mail opgeschort | string | boolean | Een indicatie van de mogelijkheid om het e-mailadres te gebruiken. |
| `workPhone.number` | Getal | Telefoonnummer | string | telefoon | Telefoonnummer zakelijk. |

## Standaard XDM Business Account-veldtoewijzingen

| [ XDM BedrijfsRekening ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | XDM-weergavenaam | Weergavenaam Marketo Engage | XDM-type | Type Marketo Engage | XDM-beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `accountBillingAddress.city` | Stad | Stad | string | string | De naam van de stad die in het factuuradres wordt gebruikt. |
| `accountBillingAddress.country` | Land | Land | string | string | De naam van het door de overheid bestuurde gebied dat in het factuuradres wordt gebruikt. Met uitzondering van `xdm:countryCode` is het een veld met vrije vorm dat de naam van het land in elke taal kan hebben. |
| `accountBillingAddress.postalCode` | Postcode | Postcode adres | string | string | De postcode van de plaats van het factureringsadres. Postcodes zijn niet voor alle landen beschikbaar. In sommige landen bevat het slechts een deel van de postcode. |
| `accountBillingAddress.region` | Regio | Adresregio | string | string | Het gebied, het graafschap, of het districtsgedeelte van het factureringsadres. |
| `accountBillingAddress.state` | Staat | Staat | string | string | De naam van de staat voor het factureringsadres. Het is een veld met vrije vorm. |
| `accountBillingAddress.street1` | Adres 1 | Adres 1 | string | string | Informatie op het primaire straatniveau voor het factuuradres, die typisch het flatnummer, straatnummer en straatnaam zou omvatten. |
| `accountName` | Naam | Naam | string | string | Naam van de onderneming. Dit veld mag maximaal 255 tekens bevatten. |
| `accountOrganization.annualRevenue.amount` | Jaaromzet | Jaaromzet | getal | valuta | Geraamde jaarlijkse inkomsten van de organisatie. |
| `accountOrganization.industry` | Marktsegment | Marktsegment | string | string | De bedrijfstak die aan de organisatie is toegeschreven. Het is een vrij-vormgebied, en het is raadzaam om een gestructureerde waarde voor vragen te gebruiken of het `xdm:classifier` bezit te gebruiken. |
| `accountOrganization.logoUrl` | Logo URL | Logo URL | string | string | Pad dat moet worden gecombineerd met de URL van een Salesforce-instantie (bijvoorbeeld `https://yourInstance.salesforce.com/` ) om een URL te genereren voor het aanvragen van de afbeelding van het profiel van het sociale netwerk die aan de account is gekoppeld. De gegenereerde URL retourneert een HTTP-omleiding (code 302) naar de afbeelding van het sociale netwerkprofiel voor de account. |
| `accountOrganization.numberOfEmployees` | Aantal werknemers | Aantal werknemers | integer | integer | Het aantal werknemers in de organisatie. |
| `accountOrganization.SICCode` | SIC-code | SIC-code | string | string | De Standard Industrial Classification (SIC)-code, een code van vier cijfers die de industrieën die bedrijven tot behoren, categoriseert op basis van hun bedrijfsactiviteiten. |
| `accountOrganization.website` | URL website | Domeinnaam | string | string | De URL van de website van de organisatie. |
| `accountPhone.number` | NVT | Telefoonnummer account | string | string | Het telefoonnummer dat aan de account is gekoppeld. |
| `accountSourceType` | NVT | Source-type | string | string | Source-type voor de account. |
