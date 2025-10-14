---
title: Rolsjablonen voor inkoopgroep
description: Rolsjablonen maken met voorwaardelijke automatische toewijzing om besluitvormers en belanghebbenden te identificeren voor het kopen van groepen in Journey Optimizer B2B edition.
feature: Buying Groups
role: User
exl-id: 9206356e-e9cf-486c-8982-c7d893222413
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Rolinesjablonen voor groepen kopen

Op een B2B-markt worden aankoopbeslissingen meestal door meerdere personen genomen. Deze personen nemen deel aan het besluitvormingsproces overeenkomstig hun rol binnen de organisatie. Creëer de rolmalplaatjes van de Groep van de Kopiëer die een groep roldefinities volgens elk product bevatten die type of rekeningsgebruik aanbieden geval.

![&#x200B; Video &#x200B;](../../assets/do-not-localize/icon-video.svg){width="30"} [&#x200B; bekijk de overzichtsvideo &#x200B;](#overview-video)

## Rolsjablonen openen en doorbladeren

1. Klik in de linkernavigatie op **[!UICONTROL Buying groups]** .

1. Selecteer op de pagina _[!UICONTROL Buying groups]_&#x200B;de tab **[!UICONTROL Roles Templates]**.

   ![&#x200B; het lusje van Malplaatjes van Rollen &#x200B;](assets/roles-templates-tab.png){width="800" zoomable="yes"}

   Het tabblad bevat een overzicht van alle bestaande rolsjablonen en geeft de volgende informatie weer in kolomindeling:

   * [!UICONTROL Name]
   * [!UICONTROL Status]
   * [!UICONTROL Creation date]
   * [!UICONTROL Created by]
   * [!UICONTROL Last update]
   * [!UICONTROL Last updated by]
   * [!UICONTROL Published on]
   * [!UICONTROL Published by]

   De lijst wordt standaard gesorteerd op _[!UICONTROL Last update]_. Alle rolmalplaatjes hebben een status van `Draft` of `Live`.

1. Als u de lijst op naam wilt filteren, gebruikt u het zoekveld boven aan de lijst.

   Voer de eerste paar tekens van de naam in om de weergegeven lijst te beperken tot de overeenkomende items.

   ![&#x200B; het filtreren van Malplaatjes van Rollen door onderzoekskoord &#x200B;](assets/roles-templates-search.png){width="700" zoomable="yes"}

## Een rolsjabloon maken

1. Klik in het tabblad _[!UICONTROL Roles Templates]_&#x200B;op **[!UICONTROL Create template]**&#x200B;in de rechterbovenhoek.

1. Voer in het dialoogvenster een unieke **[!UICONTROL Name]** (vereist) en **[!UICONTROL Description]** (optioneel) voor de sjabloon in.

   ![&#x200B; creeer de dialoog van het Malplaatje van Rollen &#x200B;](assets/roles-template-create-dialog.png){width="400"}

1. Klik op **[!UICONTROL Create]**.

### Sjabloonrollen toevoegen

Nadat u het malplaatje creeert, opent het in de werkruimte en u wordt ertoe aangezet om de rollen toe te voegen. De eerste rolkaart wordt standaard weergegeven.

Elke rol die u voor het malplaatje bepaalt gebruikt een reeks filters, of _voorwaarden_, om de leden te bepalen die aan de rol worden toegewezen. Gebruik de volgende filtertypen om de voorwaarden voor een rol te definiëren:

| Type | Voorwaarde |
| ---- | --------- |
| Persoonskenmerken | <li>E-mailadres <li>E-mail is ongeldig <li>E-mail is geschorst <li>Fax <li>Voornaam <li>Overgenomen deelstaatgebied <li>Functie <li>Achternaam <li>Tweede voornaam <li>Mobiel telefoonnummer <li>Persoonlijke betrokkenheidsscore <li>Telefoonnummer <li>Postcode <li>Staat <li>Niet geabonneerd <li>Reden waarop geen abonnement is genomen |
| Speciale filters | <li>Lid van de lijst <li>Lid van het programma |
| Intentgegevens | Categorie-intentie <li>Productintentie <li>De intentie van het sleutelwoord <br/>[&#x200B; leert over intentgegevens &#x200B;](../admin/intent-data.md). |

1. Voor de eerste rolkaart, bepaal de roleigenschappen.

   * Kies de **[!UICONTROL Buying group role]** in de lijst.

     Er zijn zes standaardrollen: `Decision Maker`, `Influencer`, `Practitioner`, `Executive Steering Committee`, `Champion` en `Other` . De lijst omvat ook om het even welke [&#x200B; douanerollen die in de _2&rbrace; lijst van Rollen_ worden bepaald.](./default-custom-roles.md#custom-roles)

     ![&#x200B; het Kopen lijst van groepsrollen &#x200B;](./assets/roles-template-create-roles-list.png){width="700" zoomable="yes"}

   * Stel de **[!UICONTROL Weighting]** in voor de rol, die wordt gebruikt om de betrokkenheidsscore te berekenen.

     De waarde voor elke optie wordt omgezet in een percentage voor de berekening van de score: [!UICONTROL Trivial] = 20, [!UICONTROL Minor] = 40, [!UICONTROL Normal] = 60, [!UICONTROL Important] = 80 en [!UICONTROL Vital] = 100.

     Bijvoorbeeld, wordt een rolmalplaatje met rollen gebruikend Vital, Belangrijk, en Normaal, dan omgezet als 100/240, 80/240, 60/240.

   * **[!UICONTROL Add conditions for auto-assignment]** - Schakel dit selectievakje in om voorwaarden toe te voegen waaraan automatisch leden worden toegewezen aan de kopende groep die aan de voorwaarde voldoet. Als het selectievakje niet is ingeschakeld, is het NIET nodig voorwaarden toe te voegen.

   * **[!UICONTROL Required for completeness score]** - Selecteer dit selectievakje voor de rol als u wilt dat dit een vereiste is voor het berekenen van een volledigheidsscore.

1. Klik op **[!UICONTROL Add Condition]** en definieer de voorwaardelijke regel voor de rol.

   * Vouw in het dialoogvenster _[!UICONTROL Condition]_&#x200B;de lijst met **[!UICONTROL Person attributes]**&#x200B;uit en zoek een kenmerk dat u wilt gebruiken om de rol aan te passen. Sleep het naar rechts en zet het neer in de filterruimte.

     ![&#x200B; het malplaatje van Rollen voegt voorwaarde belemmeringsattributen toe &#x200B;](assets/roles-template-role-attribute.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >Als u aangepaste persoonvelden hebt gedefinieerd in het accountpublieksschema in Experience Platform, zijn deze velden ook beschikbaar voor gebruik als persoonkenmerken in voorwaarden.

   * Gebruik het kenmerk om een overeenkomend filter te maken met een of meer waarden.

     In het volgende voorbeeld, wordt het attribuut van de Titel van de Baan gebruikt om een gelijke voor de Maker van het Besluit te identificeren. Elke waarde voor een titel die begint met `Director` of `Sr Director` wordt als true beschouwd voor de voorwaarde.

     ![&#x200B; het voorbeeld van de het malplaatjevoorwaarde van Rollen gebruikend baantitel &#x200B;](assets/roles-template-condition-example-job-title.png){width="700" zoomable="yes"}

   * Voeg zo nodig een ander kenmerk en een andere voorwaarde toe die de criteria voor een overeenkomst met de rol verder verfijnen.

   * Klik op **[!UICONTROL Done]**.

1. Voor elke aanvullende rol die u voor de sjabloon wilt opnemen, klikt u op **[!UICONTROL Add another role]** en herhaalt u stap 1 en 2 om de rol te definiëren.

   ![&#x200B; het malplaatje van Rollen met veelvoudige bepaalde rollen &#x200B;](assets/roles-template-multiple-roles.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX  &quot;Marketo Engage list membership&quot;]

In Marketo Engage, _Slimme Campagnes_ controlelidmaatschap van programma&#39;s om ervoor te zorgen dat de leads geen dubbele e-mail ontvangen en niet leden van veelvoudige stromen van e-mails tezelfdertijd zijn. In Journey Optimizer B2B kunt u controleren op lidmaatschap van een Marketo Engage-lijst als voorwaarde voor uw rolsjabloon om te voorkomen dat er dubbel werk wordt gedaan bij het kopen van groepslidmaatschap en reisactiviteiten.

Vouw **[!UICONTROL Special Filters]** uit en sleep de voorwaarde **[!UICONTROL Member of List]** naar de filterruimte als u een lijstlidmaatschap als rolvoorwaarde wilt gebruiken. Voer vervolgens de filterdefinitie in om het lidmaatschap in een of meer Marketo Engage-lijsten te evalueren.

![&#x200B; het malplaatjevoorwaarde van Rollen voor het lijstlidmaatschap van Marketo Engage &#x200B;](assets/roles-template-conditions-member-of-list.png){width="700" zoomable="yes"}

>[!ENDSHADEBOX]

Uw veranderingen worden auto-bewaard in de _status van het Ontwerp_. Als u niet bereid bent om het rolmalplaatje te publiceren, klik de linker (rug) pijl bij de bovenkant van de pagina en terugkeer aan de _[!UICONTROL Roles templates]_&#x200B;lijst.

### Rollensjabloon publiceren

Als de sjabloon gereed is voor gebruik, klikt u op **[!UICONTROL Publish]** rechtsboven.

Het publiceren van het malplaatje plaatst de status aan _Levende_ status en maakt het beschikbaar voor vereniging met een oplossingsrente. Er moet minstens één bepaalde rol zijn om het rolmalplaatje te publiceren.

## Een sjabloon voor conceptrollen bewerken

Wanneer een rolmalplaatje in de staat van het Ontwerp van het a __ is, kunt u de bepaalde rollen blijven uitgeven. Wijzigingen die u aanbrengt, worden automatisch opgeslagen.

Wijzig een van de instellingen in de koptekst van de rolkaart, inclusief de rol van de inkoopgroep, weging, automatische toewijzing en de vereiste voor het bijhouden van volledigheid.

![&#x200B; Verandering die de eigenschappen van de groepsrol koopt &#x200B;](./assets/roles-template-role-properties.png){width="600"}

### De voorwaarden voor een rol wijzigen

Om de voorwaarde/het filtreren logica voor om het even welk van de rollen te veranderen, klik _uitgeven_ ( ![&#x200B; geef pictogram &#x200B;](../assets/do-not-localize/icon-edit.svg)) op hoogste recht van de rolkaart uit. Met deze actie opent u de werkruimte van _[!UICONTROL Conditions]_&#x200B;waar u een bestaand filter kunt wijzigen, een filter kunt toevoegen of verwijderen of de filterlogica kunt wijzigen.

### Een rolkaart verwijderen

Als u een rol uit het malplaatje wilt verwijderen, klik _Schrapping_ ( ![&#x200B; pictogram van de Schrapping &#x200B;](../assets/do-not-localize/icon-delete.svg)) pictogram in de rolkaart.

### De prioriteit voor rollen instellen

U kunt de rollen binnen het malplaatje opnieuw in orde brengen, dat de prioriteit voor het toewijzen bepaalt leidt tot een rol. Rechts van elke rolkaart wordt een **[!UICONTROL Priority]** -controller weergegeven. Klik _Omhoog_ of _Omlaag_ pijl bij het recht om de rolkaart omhoog of neer in prioriteit te bewegen.

![&#x200B; de rolprioriteit van de Verandering &#x200B;](./assets/roles-template-role-priority.png){width="700"}

## Een rolsjabloon verwijderen

U kunt een rolmalplaatje schrappen als het in de _status van het Ontwerp_ is.

1. Selecteer de rolmalplaatje van de lijst om het te openen.

1. Klik op **[!UICONTROL Delete]** rechtsboven.

   ![&#x200B; de rolprioriteit van de Verandering &#x200B;](./assets/roles-template-delete.png){width="700"}

1. Klik in het dialoogvenster op **[!UICONTROL Delete]** om te bevestigen.

## Video over overzicht

>[!VIDEO](https://video.tv.adobe.com/v/3453307/?learn=on&captions=dut)
