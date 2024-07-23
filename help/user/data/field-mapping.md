---
title: XDM-veldtoewijzing
description: Bekijk de veldafbeelding tussen het AEP XDM-schema, het Marketo Engage en de Journey Optimizer B2B Edition.
source-git-commit: af287825508b2372f51aa8ea629cc6eda0a50b35
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 10%

---

# XDM-veldtoewijzing

De Data Transfer Service (DTS) in is verantwoordelijk voor het synchroniseren van gegevens van Adobe Experience Platform naar Journey Optimizer B2B Edition. DTS baseert zich op afbeeldingen tussen Experience Platform XDM schemagebieden en hun equivalenten in Marketo Engage.

## XDM Business Person standaardveldtoewijzingen

| XDM Business Person | Weergavenaam persoon Marketo Engage | AJO B2B-weergavenaam persoon | XDM-type | Marketo-type | XDM-beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Adres | ? | string | text | Primaire straatinformatie, appartementnummer, straatnummer en straatnaam. |
| `workAddress.city ` | Stad | Stad | string | string | De naam van de stad. |
| `b2b.companyName` | Bedrijfsnaam | ? | string | string | De naam van het bedrijf waaraan een ondernemer is gekoppeld. |
| `workAddress.country` | Land | Land | string | string | De naam van het door de overheid bestuurde gebied. Met uitzondering van `xdm:countryCode` is dit een veld met vrije vorm dat de landnaam in elke taal kan hebben. |
| `person.birthDate` | Geboortedatum | Geboortedatum | string | date | De volledige datum waarop een persoon is geboren.  YYYY-MM-DD |
| `workEmail.address` | E-mailadres | E-mailadres | string | email | Het technische adres, bijvoorbeeld, &quot;<name@domain.com>&quot;zoals algemeen bepaald in RFC2822 en verdere normen. |
| `workEmail.status` | E-mail opgeschort | E-mail opgeschort | string | boolean | Een indicatie van de mogelijkheid om het e-mailadres te gebruiken. |
| `faxPhone.number` | Faxnummer | ? | string | telefoon | Telefoonnummer fax. |
| `person.name.firstName` | Voornaam | Voornaam | string | string | Het eerste segment van de naam in de schrijfvolgorde wordt meestal geaccepteerd in de taal van de naam. In veel culturen is dit de persoonlijke of voornaam die de voorkeur heeft. De eigenschappen firstName en lastName zijn geïntroduceerd om verenigbaarheid met bestaande systemen te handhaven die modelnamen op een vereenvoudigde, niet-semantische, en niet-internationaliseerbare manier modelleren. Het gebruik van xdm:fullName heeft altijd de voorkeur. |
| `extendedWorkDetails.jobTitle` | Beroep | Beroep | string | string | Functie van de persoon. |
| `person.name.lastName` | Achternaam | Achternaam | string | string | Het laatste segment van de naam in de schrijfvolgorde dat het meest wordt geaccepteerd in de taal van de naam. In veel culturen is dit de overgenomen familienaam, achternaam, patronymische of matronymische naam. De eigenschappen firstName en lastName zijn geïntroduceerd om verenigbaarheid met bestaande systemen te handhaven die modelnamen op een vereenvoudigde, niet-semantische, en niet-internationaliseerbare manier modelleren. Het gebruik van xdm:fullName heeft altijd de voorkeur. |
| `b2b.personStatus` | Leadstatus | ? | string | string | Veld waar de huidige marketing-/verkoopstatus van de persoon wordt geregistreerd. |
| `b2b.isMarketingSuspended` | Marketing opgeschort | ? | boolean | boolean | Geeft aan of het op de markt brengen is opgeschort voor de persoon. |
| `b2b.marketingSuspendedCause` | Handelsgewijze oorzaak | ? | string | string | Als het op de markt brengen voor de persoon wordt opgeschort, verstrekt dit bezit de reden waarom. |
| `person.name.middleName` | Tussenvoegsel | ? | string | telefoon | Midden-, alternatieve of aanvullende namen opgegeven tussen de voornaam en achternaam. |
| `mobilePhone.number` | Mobiel | Mobiel | string | telefoon | Mobiel telefoonnummer. |
| `workPhone.number` | Telefoonnummer | Telefoonnummer | string | telefoon | Telefoonnummer zakelijk. |
| `workAddress.postalCode` | Postcode | Postcode | string | string | De postcode van de locatie. Postcodes zijn niet voor alle landen beschikbaar. In sommige landen zal dit slechts een deel van de postcode bevatten. |
| `person.name.courtesyTitle` | Aanhef | ? | string | string | Normaal gesproken een afkorting van de titel, de eer of de aanhef van een persoon. De courtesyTitle wordt gebruikt voor volledige of achternaam in het openen van teksten. Bijvoorbeeld meneer, juffrouw of Dr. |
| `workAddress.state` | Staat | Staat | string | string | De naam van de staat. Dit is een veld met vrije vorm. |
| `consents.marketing.email.val` | Niet geabonneerd | Niet geabonneerd | string | boolean | Als unsubscribed waar is (bijvoorbeeld waarde = 1), stelt u `consents.marketing.email.val` in als (n). Als unsubscribed vals is (bijvoorbeeld, waarde = 0), dan plaats toestemmingen.marketing.email.val als ongeldig. |
| `consents.marketing.email.reason` | Reden voor niet geabonneerd | Reden voor niet geabonneerd | string | string |  |
| `b2b.companyWebsite` | Website | ? | string | url | Website van het bedrijf waaraan een ondernemer wordt geassocieerd. |

