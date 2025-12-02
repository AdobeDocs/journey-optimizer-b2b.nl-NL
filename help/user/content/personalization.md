---
title: Inhoud aanpassen
description: B2B-e-mailberichten personaliseren met account, persoon en systeemtokens in Journey Optimizer B2B edition. Leer om de verpersoonlijkingsredacteur en syntaxis te gebruiken.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: expressie, editor, start, personalisatie
source-git-commit: 5063f9a924aef0a54b05e9bf223fc2d4898bc5a5
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# Inhoud aanpassen {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="Ervaringen met inhoud aanpassen"
>abstract="Het gebruik **Adobe Journey Optimizer B2B edition** om uw berichten aan elke specifieke ontvanger aan te passen door de gegevens en de informatie leveraging u over hen hebt. Het kan hun voornaam, industrie, titel, en meer zijn."

Met de aanpassingsmogelijkheden van [!DNL Adobe Journey Optimizer B2B Edition] kunt u uw e-mailberichten aanpassen aan elke specifieke ontvanger door de gegevens en informatie waarover u beschikt, te benutten. Het kan hun voornaam, industrie, titel, en meer zijn.

Gebruikend de _verpersoonlijkingsredacteur_, kunt u selecteren, schikken, aanpassen en alle gegevens bevestigen om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen. Gebruik verschillende gereedschappen, zoals hulplijnfuncties, om berichten op maat te maken. De redacteur gebruikt een gealigneerde verpersoonlijkingssyntaxis die op _wordt gebaseerd Handlebars_, waar de uitdrukkingen met inhoud worden geconstrueerd die door dubbele krullende steunen `{{}}` wordt ingesloten.

Bij het verwerken van het bericht vervangt Journey Optimizer B2B edition de expressie door de gegevens in de Adobe Experience Platform-gegevensset en lokale systeemwaarden. `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` wordt bijvoorbeeld dynamisch `Hello John Doe` .

Met deze syntaxis kunt u berichten in meerdere velden personaliseren, waaronder onderwerpregel-, berichttekst- en verzender-informatie voor e-mail.

## Personalization-tokens

In [!DNL Journey Optimizer B2B Edition] kunt u dynamische e-mailinhoud maken met behulp van personalisatietokens:

* **tokens van de Rekening** - Deze tokens zijn gebaseerd op de rekeningsattributen, zoals _rekeningsnaam_, _industrie_, en _aantal werknemers_. Gebruik deze tokens om kenmerkgegevens te bevolken die door het **_worden beheerd XDM BedrijfsRekeninggegevens_** schema, dat in Adobe Experience Platform wordt bepaald.

* {de tokens van 0} Persoon **- Deze tokens zijn gebaseerd op de attributen van de bedrijfsnaam, zoals** voornaam _,_ baantitel _, en_ bedrijfsnaam _._ Gebruik deze tokens om kenmerkgegevens te bevolken die door het **_worden beheerd XDM BedrijfsPersoon Details_** schema, dat in Adobe Experience Platform wordt bepaald.

* **tokens van het Systeem** - Deze tokens zijn gebaseerd op de waarden van het systeemgebied, zoals _datum_, _tijd_, en _unsubscribe verbinding_.

* **Mijn tokens** (wanneer bepaald voor de reis) - de [&#x200B; douanetokens die voor de reis &#x200B;](./personalization-my-tokens.md) worden bepaald waar e-mail verblijft.

>[!NOTE]
>
>Leer meer over de schema&#39;s XDM in de [&#x200B; documentatie van het Gegevensmodel van Adobe Experience Platform (XDM) &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}.

## Personalization Editor

De verpersoonlijkingsredacteur is beschikbaar in elke context waar u verpersoonlijking in e-mailinhoud moet bepalen. In de redacteur, kunt u selecteren, rangschikken, aanpassen, en bevestigen alle gegevens om een aangepaste verpersoonlijking voor uw inhoud tot stand te brengen.

Voeg verpersoonlijking op om het even welk gebied of inhoudscomponent toe door _te klikken verpersoonlijking_ ( ![&#x200B; voeg verpersoonlijkingspictogram &#x200B;](../../assets/do-not-localize/icon-personalization-field.svg) toe) pictogram toe.

![&#x200B; redacteur van Personalization &#x200B;](./assets/personalization-editor.png){width="800" zoomable="yes"}

>[!NOTE]
>
>De volgende informatie over de verpersoonlijkingsredacteur wijst op de veranderingen die voor [!DNL Journey Optimizer B2B Edition] milieu&#39;s beschikbaar zijn die op de [&#x200B; vereenvoudigde architectuur &#x200B;](../simplified-architecture.md) worden voorzien.

### Tokens en hulpfuncties

Om een verpersoonlijkingstoken of hulpfunctie te gebruiken, bepaal de plaats van het in de linkernavigatieruit en klik **+** om het aan de uitdrukking toe te voegen.

Klik het _Meer menu_ ( **..**) pictogram (naast _voeg_ toe ( **+**) pictogram) om meer details voor elk attribuut te bekijken en uw vaakst gebruikte attributen aan _favorieten_ toe te voegen. Kenmerken die aan favorieten worden toegevoegd, zijn toegankelijk via het menu **[!UICONTROL Favorites]** in de linkernavigatie van de editor.

![&#x200B; de redacteur van Personalization - teken Meer menu &#x200B;](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
U kunt ook een standaard fallback-tekstreeks definiëren die wordt weergegeven als een tekenreekstype profielkenmerk leeg is. Klik het _Meer menu_ ( **..**) pictogram voor de attributen en selecteer **[!UICONTROL Insert with fallback text]**. Voer de tekst in die moet worden weergegeven wanneer de waarde van het kenmerk leeg is voor een profiel en klik op **[!UICONTROL Add]** .

Het wordt aanbevolen de expressie te valideren voordat u deze in de inhoud invoegt. Klik op **[!UICONTROL Validate]** onder aan de editor om de syntaxis te controleren en te controleren of er geen fouten zijn.

![&#x200B; de redacteur van Personalization bevestigde code &#x200B;](./assets/personalization-editor-validated.png){width="500"}

Klik op **[!UICONTROL Save]** wanneer de expressie voltooid en foutloos is.

### Aangepaste gegevenssets

U kunt relationele schema&#39;s (op model-gebaseerde klassen) voor e-mailverpersoonlijking gebruiken. De douanevoorwerpen worden bepaald binnen _relationele schema&#39;s_, en een productbeheerder kan [&#x200B; relationele schemagebieden &#x200B;](../admin/xdm-field-management.md#relational-schemas) in [!DNL Journey Optimizer B2B Edition] vormen. Deze gebieden zijn toegankelijk in de verpersoonlijkingsredacteur. Alleen aangepaste objecten met een één-op-veel-relatie (1 :M) met Account <!-- (M1.5 Beta) or Person (M1.5 GA) --> zijn beschikbaar.

>[!IMPORTANT]
>
>Alvorens u douanevoorwerpen voor gescripte verpersoonlijking gebruikt, zorg ervoor dat u de [&#x200B; het templating taal van de Greep &#x200B;](https://handlebarsjs.com/guide/), [&#x200B; verpersoonlijkingssyntaxis &#x200B;](./personalization-syntax.md), en de ingebouwde [&#x200B; hulpfuncties &#x200B;](./personalization-helper-functions.md) herzien en begrijpt.

Wanneer u verpersoonlijking gebruikend de douanevoorwerpen bepaalt, kunt u tot alle variabelen in manuscript-toegankelijke voorwerpen over **[!UICONTROL Personalization tokens]** (persoon/lood, rekening, systeem, en Mijn Tokens) en **[!UICONTROL Model-based classes]** (relationele schema&#39;s) toegang hebben. Als op een model gebaseerde klassen zijn geselecteerd, kunt u de velden weergeven door op de map met aangepaste objecten te klikken. Klik **+** voor elk gebied dat u het aan de uitdrukking wilt toevoegen.

![&#x200B; de redacteur van Personalization - Op model-gebaseerde klassen - voeg de gebieden van douaneobjecten &#x200B;](./assets/personalization-editor-custom-object-fields.png){width="800" zoomable="yes"} toe

<!-- ## Personalization experimentation {#playground}

**[!DNL Adobe Journey Optimizer]** includes an interactive tool designed to help you learn and experiment with personalization capabilities.

This playground provides a simulated environment to write and test personalization code using sample data without requiring live datasets. You can leverage predefined code samples, edit dummy profile payloads, and preview the output of your personalization code in real-time. 

![personalization playground](assets/playground.png)

➡️ [Access the personalization playground](https://experienceleague.adobe.com/en/apps/journey-optimizer/ajo-personalization){target="_blank"} 

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Learn how to add profile-based personalization to a message and how to use audience membership as a pre-condition to a personalization block.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Learn how to leverage the personalization editor playground to write and test personalization code using sample data.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12) -->