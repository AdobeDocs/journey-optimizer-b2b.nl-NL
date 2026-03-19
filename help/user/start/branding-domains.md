---
title: Brandingsdomeinen configureren
description: Configureer uw brandingdomeinen zodat elk van uw merken zijn eigen merkkoppelingen heeft.
feature: Setup, Channels
role: Admin
source-git-commit: 023e44e1ad2baed2a5586d95a26ef8693020667a
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Brandingsdomeinen configureren

Een brandingdomein in Marketo Engage is een aangepast subdomein (zoals `links.yourcompany.com` ) dat wordt gebruikt om koppelingen te herschrijven en kliks op e-mailberichten bij te houden en ervoor te zorgen dat deze uw merk weerspiegelen in plaats van een algemeen domein. Elk brandingdomein fungeert als een klikvolgdomein om de leesbaarheid en het vertrouwen te verbeteren door de koppelingen van uw e-mail- en landingspagina aan uw domein aan te passen.

* Algemene koppelingen worden vervangen door uw eigen merknaam in e-mailhyperlinks.
* Wanneer de leiding van een account op een koppeling klikt, wordt dit aangepaste domein doorgestuurd om de prestaties te kunnen bijhouden, maar lijken de e-mailfilters legitiem.
* Als u meerdere merken hebt, kunt u aanvullende brandingdomeinen configureren om verschillende bedrijfseenheden of merken te ondersteunen.

>[!BEGINSHADEBOX]

**Unieke CNAMEs voor het volgen van verbindingen**

Koppelingen voor het bijhouden van e-mail moeten nieuw en uniek zijn voor het bijgevoegde Marketo Engage-exemplaar. Als u bestaande CNAMEs voor het volgen van verbindingen hebt richten aan een reeds bestaand (productie) geval van Marketo Engage, kunnen zij niet worden opnieuw gebruikt _as-is_.

U kunt domeinbranding via het retourpad delen tussen uw productie-Marketo Engage-instantie en de bijgevoegde instantie, maar dit is een achterwaartse wijziging. Open een ondersteuningsticket en geef het Marketo Engage-voorvoegsel (Munchkin-id) en het nieuwe Journey Optimizer B2B edition-voorvoegsel (Munchkin-id) op als u een verzoek wilt indienen voor gedeelde return-path domain branding.

>[!ENDSHADEBOX]

>[!PREREQUISITES]
>
>Alvorens u uitgeeft of een domein in UI toevoegt, moet u a [&#x200B; in kaart gebrachte NAAM aan een Adobe-Geleverd domein van Marketo Engage &#x200B;](https://experienceleague.adobe.com/nl/docs/marketo/using/getting-started/initial-setup/setup-steps#customize-your-landing-page-urls-with-a-cname){target="_blank"} hebben.
>
>Bij het toevoegen van een domein, controleert het systeem op reeds bestaande SSLs, die manueel kan zijn gecreeerd vroeger. Als u deze validatie tegenkomt, maakt u uw domein zonder SSL te selecteren en sluit u deze aan als een aparte procedure.

## Domeinen met branding openen in Marketo Engage

1. Ga naar het **[!UICONTROL Admin]** -gebied in uw Marketo Engage-instantie en selecteer **[!UICONTROL Email]** .

1. Schuif omlaag naar het deelvenster **[!UICONTROL Branding Domains]** .

   ![&#x200B; brandend paneel van Domeinen in Admin onder E-mail, die het standaarddomein &#x200B;](./assets/me-admin-email-branding-domains.png){width="700" zoomable="yes"} tonen

   In de lijst wordt het standaarddomein voor de Marketo Engage-instantie weergegeven.

## Uw standaardbrandingdomein bewerken

De eerste stap bij het werken met brandingdomeinen is het bewerken van het standaardbrandingdomein dat in uw Marketo Engage-instantie is gedefinieerd.

>[!NOTE]
>
>U kunt geen extra brandend domein bepalen tot u het generische standaarddomein hebt uitgegeven.

1. Selecteer in het deelvenster _[!UICONTROL Branding Domains]_&#x200B;het algemene domein en klik op **[!UICONTROL Edit]**&#x200B;boven.

   ![&#x200B; Brandend paneel van Domeinen met het generische geselecteerde domein &#x200B;](./assets/me-admin-email-branding-domains-edit-default.png){width="500"}

1. Voer in het dialoogvenster _[!UICONTROL Edit Branding Domain]_&#x200B;de naam van uw standaarddomein in het veld **[!UICONTROL Domain]**&#x200B;in.

   ![&#x200B; geef het Brandmerken de dialoog van het Domein uit &#x200B;](./assets/me-admin-email-branding-domains-edit-default-name.png){width="400"}

1. Als er meerdere werkruimten zijn gedefinieerd voor uw Marketo Engage-instantie, klikt u op **[!UICONTROL Next]** .

   Selecteer elk van de werkruimten waar u het bijgewerkte primaire domein wilt toepassen.

   ![&#x200B; geef de Brandende dialoog van het Domein met werkruimteselectie voor primair domein uit &#x200B;](./assets/me-admin-email-branding-domains-edit-default-workspaces.png){width="400"}

1. Klik op **[!UICONTROL Save]** .

## Een extra domein definiëren

Nadat u het standaarddomein hebt bewerkt, kunt u een ander brandingdomein toevoegen wanneer u meerdere merken uit uw Journey Optimizer B2B edition-omgeving wilt uitvoeren, waarin elk merk zijn eigen traceringskoppelingen heeft. Wanneer u een domein toevoegt, hebt u de volgende opties:

>* _maak Primair Domein_: Maak dit het primaire domein voor de werkruimte. Wanneer u deze optie selecteert, worden alle bestaande niet-verzonden e-mails ingesteld op het primaire standaarddomein en worden alle nieuwe e-mails automatisch standaard ingesteld op dit primaire domein. Marketers kunnen waar nodig een alternatief brandingdomein kiezen.
>
>* _produceer SSL Certificaat_: Creeer een Veilige Laag van Contactdozen (SSL) met de verwezenlijking van het domein. Het eerste volgende domein stelt een éénmalige opstelling van infrastructuur in werking die een paar uren kan vergen. Het systeem verzendt een kennisgeving na voltooiing.

_Het domein toevoegen :_

1. Klik in het deelvenster _[!UICONTROL Branding Domains]_&#x200B;op **[!UICONTROL Add]**&#x200B;boven.

   ![&#x200B; Brandend paneel van Domeinen met Add knoop bij de bovenkant &#x200B;](assets/me-admin-email-branding-domains-add.png){width="500"}

1. Typ in het dialoogvenster _[!UICONTROL New Branding Domain]_&#x200B;de naam van het brandingdomein in het veld **[!UICONTROL Domain]**.

1. (Optioneel) Schakel het selectievakje **[!UICONTROL Generate SSL Certificate]** in om automatisch een SSL voor het domein te genereren.

   ![&#x200B; Nieuwe brandende dialoog van het Domein &#x200B;](assets/me-admin-email-branding-domains-add-name.png){width="400"}

   Indien nodig en beschikbaar, kunt u ook selecteren _Primair Domein_ controlevakje maken.

   >[!NOTE]
   >
   >**_Aangepaste SSLs_**: Als u douane SSL nodig hebt, kunt u a [&#x200B; steunkaartje &#x200B;](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"} voorleggen. Gebruik het selectievakje niet voor het maken van SSL.

1. Als er meerdere werkruimten zijn gedefinieerd voor uw Marketo Engage-instantie, klikt u op **[!UICONTROL Next]** .

   Selecteer zo nodig elke werkruimte waarin u het nieuwe domein als primair domein wilt toepassen.

   ![&#x200B; Nieuwe brandende dialoog van het Domein met werkruimteselectie voor het toepassen van het primaire domein &#x200B;](assets/me-admin-email-branding-domains-add-workspaces.png){width="400"}

1. Klik op **[!UICONTROL Save]** .

## SSL&#39;s voor bestaande brandingdomeinen bewerken

Ga als volgt te werk om SSL in te schakelen voor uw bestaande domeinen.

1. Selecteer in het gebied _[!UICONTROL Admin]_&#x200B;de optie **[!UICONTROL Email]**.

1. Selecteer in het deelvenster _[!UICONTROL Branding Domains]_&#x200B;de domeinrij en klik op **[!UICONTROL Add SSL]**.

   ![&#x200B; Brandend paneel van Domeinen met Add SSL bij de bovenkant &#x200B;](./assets/me-admin-email-branding-domain-add-ssl.png){width="500"}

1. Klik in het dialoogvenster op **[!UICONTROL Confirm]** .

   ![&#x200B; produceer SSL de bevestigingsdialoog van het Certificaat &#x200B;](./assets/me-admin-email-branding-domain-generate-ssl-cert-confirm.png){width="400"}

## Foutberichten

| Fout | Details |
| ----- | ------- |
| `Domain already exists.` | Er bestaat al een domein met dezelfde naam. |
| `Domain is not mapped to the default domain.` | Het aangepaste domein wordt niet correct toegewezen aan het standaarddomein. Verifieer de montages van de domeinafbeelding en zorg ervoor dat de DNS configuratie aan het correcte standaarddomein richt. |
| `SSL certificates could not be issued due to unsupported CAA records. Request your IT to update your CAA records.` | De CAA-records zijn niet bijgewerkt. Voor gebruikers die gebruikmaken van door Adobe beheerde SSL-certificaten, moeten CAA-records worden bijgewerkt naar certificaten die worden aanbevolen door de leverancier. |
| `SSL certificate has already been issued.` | Er bestaat al een SSL-certificaat voor dit aangepaste domein. Er is geen verdere actie nodig tenzij het certificaat is verlopen of opnieuw moet worden uitgegeven. |
| `The default domain was not found. Please contact Support for assistance.` | Er is een probleem opgetreden bij het zoeken naar het standaarddomein. Neem contact op met de Adobe-ondersteuning om het onderzoek te starten. |
| `Unexpected error encountered while creating a domain. Please contact Support for assistance.` | Er is een onverwachte fout opgetreden. Verzamel logboeken en foutgegevens en escaleer het probleem naar Adobe-ondersteuning. |

## Een brandingdomein verwijderen

>[!NOTE]
>
>Als u het primaire brandingsdomein (in één of meerdere werkruimten) wilt schrappen, moet u een verschillend brandend domein eerst selecteren om het primaire voor elke werkruimte te zijn.
>
>Het schrappen van een domein **_schrapt niet_** het SSL certificaat. Deze handleiding voorkomt gebruikersfouten die ertoe leiden dat een website geen SSL-certificaten heeft. Neem contact op met de ondersteuning van Adobe als u de SSL-certificaten wilt verwijderen.

Selecteer in het deelvenster _[!UICONTROL Branding Domains]_&#x200B;het domein en klik op **[!UICONTROL Delete]**&#x200B;bovenaan.
