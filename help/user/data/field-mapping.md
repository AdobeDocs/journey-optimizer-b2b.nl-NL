---
title: XDM-velden
description: Controleer de standaardkenmerkvelden die zijn gesynchroniseerd tussen de Adobe Experience Platform en Journey Optimizer B2B edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: e2a802750ee221caf83989c5731e0daee64aa63e
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 5%

---

# XDM-velden

Accountpublieksgegevens worden opgeslagen als kenmerken in zowel de XDM Business Account- als de XDM Business Person-klassen. De gegevens worden periodiek gesynchroniseerd tussen Adobe Experience Platform en Journey Optimizer B2B edition. In de volgende secties worden de standaardsets met kenmerken weergegeven.

>[!TIP]
>
>U kunt de klassen van de Zakelijke Persoon XDM en van de Zakelijke Rekening XDM in een vele-aan-vele verhouding modelleren door de klasse van de Verhouding van de Person van de Onderneming XDM te gebruiken XDM zoals die in de [ documentatie XDM van Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b) wordt beschreven.

## Kenmerken XDM Zakelijke account persoon relatie

| [ Bezit ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Weergavenaam | Journey Optimizer B2B-weergavenaam | Gegevenstype | Beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Personrollen | Functie | Tekenreeksarray | Een array met rollen die aan de persoon op de account zijn gekoppeld, zoals `owner, accountant, designer` . |

## Kenmerken XDM-bedrijfsnaam

>[!IMPORTANT]
>
>Het attribuut `workEmail.Address` is vereist. Als het voor een lid van het rekeningspubliek leeg is, wordt die persoon niet gegeten en weggelaten van rekeningsreizen en het kopen groepen die het publiek van verwijzingen voorzien.

| [ Bezit ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Weergavenaam | Journey Optimizer B2B-weergavenaam | Gegevenstype | Beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | Bedrijfsnaam | Bedrijfsnaam | String | De naam van het bedrijf waaraan een ondernemer is gekoppeld. |
| `b2b.companyWebsite` | Website van bedrijf | Website | String | Website van het bedrijf waaraan een ondernemer wordt geassocieerd. |
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

| [ Bezit ](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Weergavenaam | Journey Optimizer B2B-weergavenaam | Gegevenstype | Beschrijving |
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

## Kenmerken van XDM Business Opportunity

Bovendien, worden de opportuniteitsgegevens opgeslagen als attributen in de XDM klasse Business Opportunity, die met de XDM klasse van de BedrijfsRekening door een veel-aan-één verhouding kan worden geassocieerd, zoals [ hier ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field) wordt beschreven.

| [ Bezit ](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md) | Weergavenaam | Journey Optimizer B2B-weergavenaam | Gegevenstype | Beschrijving |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Sluiten verwacht | Verwachte opportuniteitssluitingsdatum | String | Verwachte sluitingsdatum voor de gelegenheid. |
| `expectedRevenue.amount` | Verwachte inkomsten | Totale verwachte opportuniteitsinkomsten | String | Berekende opbrengsten op basis van het bedrag en de waarschijnlijkheid. |
| `fiscalQuarter` | Begrotingskwartaal | Opportunity fiscaal kwartaal | String | Het beoogde begrotingskwartaal voor de kans. |
| `fiscalYear` | Begrotingsjaar | Opportunity-boekjaar | String | Het beoogde belastingjaar voor de kans. |
| `forecastCategory` | Prognose-categorie | Opportunity Forecast, categorie | String | Prognose-categorie bepaald door de waarde van het opportuniteitswerkgebied. |
| `forecastCategoryName` | Naam van voorspelde categorie | Naam van opportunity-prognoscategorie | String | Naam van de voorspelde categorie die wordt weergegeven in rapporten voor een bepaalde categorie. |
| `isClosed` | Gesloten vlag | Opportunity gesloten | String | Markering die aangeeft of de opportuniteit is gesloten. |
| `isWon` | Won-markering | Opportunity gewonnen | String | Markering die aangeeft of de opportuniteit wordt gewonnen. |
| `lastActivityDate` | Laatste activiteitendatum | Laatste activiteitendatum | String | Datum van laatste activiteit voor de opportuniteit. |
| `leadSource` | Leadbron | Loodbron | String | Source van de mogelijkheid, zoals Advertisement, Partner of Web. |
| `nextStep` | Volgende stap | Volgende stap opportunity | String | Beschrijving van de volgende taak om de kans te sluiten. |
| `opportunityAmount.amount` | Aantal kansen | Totaal opportuniteitsbedrag | String | Geraamd totaal verkoopbedrag voor de opportuniteit. |
| `opportunityDescription` | Beschrijving van opportunity | Opportuniteitsbeschrijving | String | Aanvullende informatie om de mogelijkheid te beschrijven, zoals mogelijke producten om bij de klant te verkopen of aankopen in het verleden te doen. |
| `opportunityName` | Naam opportunity | Naam opportunity | String | Onderwerp of beschrijvende naam, zoals de verwachte orde of bedrijfsnaam, voor de kans. |
| `opportunityQuantity` | Aantal kansen | Aantal kansen | String | Totaal van alle veldwaarden voor de hoeveelheid van alle producten in de lijst van verwante producten voor de gelegenheid. |
| `opportunityStage` | Opportunity Stage | Opportunity-fase | String | De verkoopfase van de mogelijkheid om het verkoopteam te helpen bij hun pogingen om het te winnen. |
| `opportunityType` | Type opportunity | Type opportunity | String | Het type dat aan de kans wordt toegewezen, zoals _Bestaande Zaken _ of _Nieuwe Zaken_ |
| `probabilityPercentage` | Percentage waarschijnlijkheid | Percentage opportunity-waarschijnlijkheid | String | Waarschijnlijkheid van het sluiten van de mogelijkheid, uitgedrukt als een percentage. |
