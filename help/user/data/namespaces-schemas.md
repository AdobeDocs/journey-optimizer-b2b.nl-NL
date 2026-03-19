---
title: B2B-naamruimten en -schema's
description: Configureer Experience Platform B2B-naamruimten en -schema's voor Journey Optimizer B2B edition met behulp van het Postman-hulpprogramma voor automatisch genereren.
feature: Setup, Data Management
role: Admin
source-git-commit: 023e44e1ad2baed2a5586d95a26ef8693020667a
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# B2B-naamruimten en -schema&#39;s

De installatie van Journey Optimizer B2B edition op de vereenvoudigde architectuur omvat configuratie van Experience Platform namespaces en schema&#39;s die met B2B bronnen worden gebruikt. Het Postman-hulpprogramma voor automatisering is vereist voor het genereren van B2B-naamruimten en -schema&#39;s.

>[!AVAILABILITY]
>
>- U moet toegang tot [&#x200B; Adobe Real-Time Customer Data Platform B2B edition &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdpb2b-intro/b2b-overview){target="_blank"} voor uw B2B- schema&#39;s hebben om in [&#x200B; in real time het Profiel van de Klant &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/profile/home){target="_blank"} te kwalificeren.
>
>- Uw Experience Platform B2B entiteiten moeten de standaardverhoudingen gebruiken die in [&#x200B; worden geschetst B2B namespaces en schemagids &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/schemas/b2b){target="_blank"}.

Controleer de volgende informatie over de onderliggende opstelling voor namespaces en schema&#39;s die met B2B bronnen moeten worden gebruikt. Het biedt ook informatie voor het instellen van het Postman-automatiseringshulpprogramma, dat vereist is voor het genereren van B2B-naamruimten en -schema&#39;s.

## Het hulpprogramma voor automatisch genereren instellen

Raadpleeg de volgende bronnen voor voorwaarden en gedetailleerde informatie over hoe u de [!DNL Postman] -omgeving zo kunt instellen dat deze ondersteuning biedt voor de naamruimte B2B en het automatisch genereren van schema.

- Download de namespace en het schema auto-generatienutsinzameling en het milieu van de [&#x200B; bewaarplaats GitHub &#x200B;](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility){target="_blank"}.
- Voor informatie over het gebruiken van Experience Platform APIs met inbegrip van details over het verzamelen van waarden voor vereiste kopballen en het lezen van steekproefAPI vraag, zie [_Begonnen het worden met Adobe Experience Platform APIs_ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-guide){target="_blank"}.
- Voor informatie over het produceren van uw geloofsbrieven voor Experience Platform APIs, zie [_voor authentiek verklaren en toegang Experience Platform APIs_ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication){target="_blank"}.
- Voor informatie over vestiging [!DNL Postman] voor Experience Platform APIs, zie [_[!DNL Postman] in Adobe Experience Platform _](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman){target="_blank"}.

### Omgevingswaarden

Met een Experience Platform-ontwikkelaarsconsole en [!DNL Postman] -configuratie kunt u de juiste omgevingswaarden toepassen op uw [!DNL Postman] -omgeving. De volgende tabel bevat voorbeeldwaarden en aanvullende informatie over het vullen van de [!DNL Postman] -omgeving:

| Variabele | Beschrijving | Voorbeeld |
| --- | --- | --- |
| `CLIENT_SECRET` | Een unieke id die wordt gebruikt om de `{ACCESS_TOKEN}` te genereren. | `{CLIENT_SECRET}` |
| `API_KEY` | Een unieke id die wordt gebruikt om aanroepen naar Experience Platform API&#39;s te verifiëren. | `c8d9a2f5c1e03789bd22e8efdd1bdc1b` |
| `ACCESS_TOKEN` | Het toestemmingstoken wordt vereist om vraag aan Experience Platform APIs te voltooien. | `Bearer {ACCESS_TOKEN}` |
| `META_SCOPE` | Met betrekking tot [!DNL Journey Optimizer B2B] en [!DNL Marketo Engage] is deze waarde vast en altijd ingesteld op: `ent_dataservices_sdk` . | `ent_dataservices_sdk` |
| `CONTAINER_ID` | De `global` container bevat alle standaard door Adobe en Experience Platform verschafte klassen, groepen met schemavelden, gegevenstypen en schema&#39;s. Met betrekking tot [!DNL Marketo] is deze waarde vast en altijd ingesteld op `global` . | `global` |
| `TECHNICAL_ACCOUNT_ID` | Een referentie die wordt gebruikt om te integreren in Adobe I/O. | `D42AEVJZTTJC6LZADUBVPA15@techacct.adobe.com` |
| `IMS` | Het Identity Management System (IMS) biedt het framework voor verificatie van Adobe-services. Met betrekking tot [!DNL Journey Optimizer B2B] en [!DNL Marketo Engage] is deze waarde vast en altijd ingesteld op: `ims-na1.adobelogin.com` . | `ims-na1.adobelogin.com` |
| `IMS_ORG` | Een onderneming die producten en diensten kan bezitten of in licentie kan geven en toegang kan verlenen tot haar leden. | `ABCEH0D9KX6A7WA7ATQE0TE@adobeOrg` |
| `SANDBOX_NAME` | De naam van de virtuele sandboxpartitie die u gebruikt. | `prod` |
| `TENANT_ID` | Een id die wordt gebruikt om ervoor te zorgen dat de bronnen die u maakt, correct worden genoemd en zich binnen uw organisatie bevinden. | `b2bcdpproductiontest` |
| `PLATFORM_URL` | Het URL-eindpunt waarnaar u API-aanroepen maakt. Deze waarde is vast en wordt altijd ingesteld op: `http://platform.adobe.io/` . | `http://platform.adobe.io/` |

{style="table-layout:auto"}

### Scripts uitvoeren

Nadat de omgevingswaarden zijn ingesteld, gebruikt u de [!DNL Postman] -interface om het script uit te voeren voor het maken van de naamruimten en schema&#39;s. Selecteer de hoofdmap van het hulpprogramma voor automatische generator en selecteer vervolgens **[!DNL Run]** in de bovenste koptekst.

![&#x200B; omslag van de Wortel van Namespaces en de generator van Schema in Postman UI &#x200B;](./assets/namespaces-schemas-postman-root-folder.png){width="500" zoomable="yes"}

De interface [!DNL Runner] wordt weergegeven. Controleer van hieruit of alle selectievakjes zijn ingeschakeld en selecteer vervolgens **[!DNL Run Namespaces and Schemas Autogeneration Utility]** .

![&#x200B; Postman UI met verscheidene verzoeken in de geselecteerde inzameling Namespaces en Schemas.](./assets/namespaces-schemas-postman-run-generator.png){width="800" zoomable="yes"}

Een succesvol verzoek leidt tot vereiste B2B namespaces en schema&#39;s.

## B2B-naamruimten

Identiteitsnaamruimten zijn een component van Experience Platform [[!DNL Identity Service] &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"} die dienen om de context van een identiteit te onderscheiden. Een volledig gekwalificeerde identiteit omvat een identiteitswaarde en een namespace. Zie [&#x200B; namespaces overzicht &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces){target="_blank"} voor meer informatie.

B2B-naamruimten worden gebruikt in de primaire identiteit van de entiteit.

| Weergavenaam | Identiteitssymbool | Identiteitstype |
| --- | --- | --- |
| B2B-persoon | `b2b_person` | `CROSS_DEVICE` |
| B2B-account | `b2b_account` | `B2B_ACCOUNT` |
| B2B-opportuniteit | `b2b_opportunity` | `B2B_OPPORTUNITY` |
| B2B-opportuniteitsrelatie | `b2b_opportunity_person_relation` | `B2B_OPPORTUNITY_PERSON` |
| B2B-campagne | `b2b_campaign` | `B2B_CAMPAIGN` |
| B2B Campagne-lid | `b2b_campaign_member` | `B2B_CAMPAIGN_MEMBER` |
| B2B-marketinglijst | `b2b_marketing_list` | `B2B_MARKETING_LIST` |
| B2B Marketing List Member | `b2b_marketing_list_member` | `B2B_MARKETING_LIST_MEMBER` |
| B2B Betrekking van rekeningpersoon | `b2b_account_person_relation` | `B2B_ACCOUNT_PERSON` |

{style="table-layout:auto"}

## B2B-schema&#39;s

Experience Platform gebruikt schema&#39;s om de gegevensstructuur op een consistente en herbruikbare manier te beschrijven. Door gegevens consistent in verschillende systemen te definiëren, wordt het eenvoudiger om betekenis te behouden en zo waarde te verkrijgen van gegevens.

Voordat Experience Platform gegevens kan invoeren, moet er een schema zijn dat de gegevensstructuur beschrijft en beperkingen biedt aan het type gegevens dat binnen elk veld kan worden opgenomen. De schema&#39;s bestaan uit een basisklasse en nul of meer groepen van het schemagebied.

Voor meer informatie over het model van de schemacompositie, met inbegrip van ontwerpprincipes en beste praktijken, zie [_Grondbeginselen van schemacompositie_ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}.

+++ B2B-account

<table>
    <tr>
        <td style="width: 30%;">Basisklasse</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account" target="_blank">XDM Business Account</a></td>
    </tr>
    <tr>
        <td>Veldgroepen</td>
        <td>XDM-bedrijfsaccountgegevens</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Ingeschakeld</td>
    </tr>
    <tr>
        <td>Primaire identiteit</td>
        <td><code>accountKey.sourceKey</code> in de basisklasse</td>
    </tr>
    <tr>
        <td>Primaire naamruimte</td>
        <td>B2B-account</td>
    </tr>
    <tr>
        <td>Secundaire identiteit</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in de basisklasse</td>
    </tr>
    <tr>
        <td>Secundaire naamruimte voor identiteit</td>
        <td>B2B-account</td>
    </tr>
    <tr>
        <td>Relatie</td>
        <td><ul><li><code>accountParentKey.sourceKey</code> in XDM Business Account Details, veldgroep</li><li>Eigenschap van bestemming: <code>/accountKey/sourceKey</code></li><li>Type: een-op-een</li><li>Referentieschema: B2B-account</li><li>Naamruimte: B2B-account</li></ul> </td>
    </tr>
</table>

+++

+++ B2B-persoon

<table>
    <tr>
        <td style="width: 30%;">Basisklasse</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile"> XDM Individueel Profiel </a> {target= "_blank"}</td>
    </tr>
    <tr>
        <td>Veldgroepen</td>
        <td><ul><li>XDM Business Person - Gegevens</li><li>XDM Business Person-componenten</li><li>IdentityMap</li><li>Details van goedkeuring en voorkeur</li></ul> </td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Ingeschakeld</td>
    </tr>
    <tr>
        <td>Primaire identiteit</td>
        <td><code>b2b.personKey.sourceKey</code> in de XDM Business Person Details Field Group</td>
    </tr>
    <tr>
        <td>Primaire naamruimte</td>
        <td>B2B-persoon</td>
    </tr>
    <tr>
        <td>Secundaire identiteit</td>
        <td><ol><li><code>extSourceSystemAudit.externalKey.sourceKey</code> van XDM Business Person Details, veldgroep</li><li><code>workEmail.address</code> van XDM Business Person Details, veldgroep</li></ol></td>
    </tr>
    <tr>
        <td>Secundaire naamruimte voor identiteit</td>
        <td><ol><li>B2B-persoon</li><li>E-mail</li></ol></td>
    </tr>
    <tr>
        <td>Relatie</td>
        <td><ul><li><code>personComponents.sourceAccountKey.sourceKey</code> van XDM Business Person Components, veldgroep</li><li>Type: veel-op-één</li><li>Referentieschema: B2B-account</li><li>Naamruimte: B2B-account</li><li>Bestemmingseigenschap: accountKey.sourceKey</li><li>Relatienaam uit huidig schema: Account</li><li>Relatie-naam vanuit referentieschema: Personen</li></ul> </td>
    </tr>
</table>

+++

<!--

+++B2B Opportunity

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity">XDM Business Opportunity</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Opportunity Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in the base class</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td><ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: Opportunities</li></ul></td>
    </tr>
</table>

+++

+++B2B Opportunity Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation">XDM Business Opportunity Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td> **First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Opportunities</li></ul>**Second relationship**<ul><li><code>opportunityKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Opportunity </li><li>Namespace: B2B Opportunity </li><li>Destination property: <code>opportunityKey.sourceKey</code></li><li>Relationship name from current schema: Opportunity</li><li>Relationship name from reference schema: People</li></ul> </td>
    </tr>
</table>


+++

+++B2B Campaign

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign">XDM Business Campaign</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

+++

+++B2B Campaign Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign-members">XDM Business Campaign Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Member Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Campaigns</li></ul>**Second relationship**<ul><li><code>campaignKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Campaign</li><li>Namespace: B2B Campaign</li><li>Destination property: <code>campaignKey.sourceKey</code></li><li>Relationship name from current schema: Campaign</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++B2B Marketing List

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list">XDM Business Marketing List</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

>[!NOTE]
>
>Static List in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Marketing List Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members">XDM Business Marketing List Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Marketing Lists</li></ul>**Second relationship**<ul><li><code>marketingListKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Marketing List</li><li>Namespace: B2B Marketing List</li><li>Destination property: <code>marketingListKey.sourceKey</code></li><li>Relationship name from current schema: Marketing List</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

>[!NOTE]
>
>Static List member in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Account Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account-person-relation">XDM Business Account Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>Identity Map</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>accountPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Account Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: People</li><li>Relationship name from reference schema: Account</li></ul>**Second relationship**<ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++

-->
