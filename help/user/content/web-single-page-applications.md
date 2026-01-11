---
title: Toepassingen met één pagina
description: Creeer Webervaringen voor enig-paginatoepassingen (SPAs) - vorm mening het volgen, handvat dynamische inhoud, en beheer cliënt-zijnavigatie in Journey Optimizer B2B edition.
feature: Channels, Personalization
role: User
badgeBeta: label="Beta" type="informative" tooltip="Deze functie bevindt zich momenteel in een beperkte bètaversie"
source-git-commit: e50b6830736bf763d3aae6a58595e868bbac36e0
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# Toepassingen met één pagina

Toepassingen van één pagina (SPAs) stellen unieke uitdagingen voor Webverpersoonlijking voor omdat zij dynamisch paginainhoud zonder volledige paginaherladingen bijwerken. Journey Optimizer B2B edition biedt speciale gereedschappen om SPA-personalisatie effectief af te handelen.

## SPA&#39;s begrijpen

In tegenstelling tot traditionele websites van meerdere pagina&#39;s waar elke navigatie een volledige paginading teweegbrengt, gebruiken SPAs JavaScript om inhoud dynamisch bij te werken terwijl het handhaven van één enkele pagina van HTML. Deze benadering leidt tot verscheidene overwegingen voor Webervaringen:

* **Geen paginaherladingen** - de veranderingen van de Inhoud komen voor zonder de traditionele gebeurtenissen van de paginading te veroorzaken.
* **Virtuele meningen** - Verschillende _meningen_ of _schermen_ binnen het KUUROORD die als afzonderlijke pagina&#39;s moeten worden gevolgd.
* **client-kant die** verplettert - de routers van JavaScript (zoals React Router, de Router van de Kleurtoon, en de Router van Angular) behandelen navigatie eerder dan serververzoeken.
* **Dynamisch DOM** - de elementen van de Pagina kunnen worden gecreeerd, worden gewijzigd, of worden verwijderd na aanvankelijke paginalading.

## SPA-ondersteuning configureren

Om SPAs effectief te personaliseren, moet u mening het volgen vormen zodat Journey Optimizer B2B edition kan identificeren wanneer de gebruikers tussen virtuele meningen navigeren.

### Weergavedeclaraties instellen

Werk met uw ontwikkelingsteam om meningsverklaringen uit te voeren gebruikend het Web SDK van Adobe. Het gebruiken van deze meningsverklaringen impliceert het roepen van het `sendEvent` bevel met meningsinformatie wanneer SPA aan een nieuwe mening navigeert.

**de implementatie van het Voorbeeld:**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### Naamgevingsconventies weergeven

Gebruik consistente, beschrijvende weergavenamen die overeenkomen met de logische structuur van uw toepassing:

| Weergave | Voorbeeldnaam |
| ---- | ------------ |
| Homepage | `home` |
| Productaanbieding | `product-list` |
| Productgegevens | `product-detail` |
| Winkelwagentje | `cart` |
| Afhandeling | `checkout` |
| Accountdashboard | `account-dashboard` |

>[!NOTE]
>
>Weergavenamen zijn hoofdlettergevoelig. Gebruik een consistente naamgevingsconventie (kleine letters met afbreekstreepjes wordt aanbevolen) in uw implementatie.

## Webervaringen voor SPA&#39;s maken

Wanneer het creëren van Webervaringen voor SPAs, overweeg de volgende beste praktijken:

### Doelspecifieke weergaven

* In de [ configuratie van het Webkanaal ](../admin/configure-channels-web.md), opstelling URL passende regels die zich met uw SPA richten die structuur verplettert.

* Geef bij het maken van wijzigingen de weergave op waar de wijziging moet worden toegepast.

* Gebruik CSS-kiezers die specifieke elementen voor elke weergave als doel hebben.

### Dynamische inhoud afhandelen

SPAs laadt vaak dynamisch inhoud nadat de aanvankelijke pagina teruggeeft. Gebruik de volgende technieken om ervoor te zorgen dat de wijzigingen correct worden toegepast:

#### Afwachten op elementen

Vorm wijzigingen om op de doelelementen te wachten alvorens toe te passen:

1. Voeg in de niet-visuele editor een wijziging toe met een CSS-kiezer.

1. Schakel **[!UICONTROL Wait for element]** in en geef de maximale wachttijd op.

1. De wijziging wordt toegepast zodra het doelelement in het DOM wordt weergegeven.

#### Waarnemers voor mutaties gebruiken

Voor zeer dynamische inhoud, omvat het Web SDK ingebouwde veranderingswaarnemers die ontdekken wanneer de nieuwe elementen aan de pagina worden toegevoegd. Deze waarnemers zorgen ervoor dat de wijzigingen worden toegepast zelfs wanneer de elementen asynchroon worden geladen.

### SPA-frameworks

Journey Optimizer B2B edition webervaringen werken met populaire SPA-frameworks:

| Kader | Overwegingen |
| --------- | -------------- |
| **Reageren** | Wijzigingen zijn van toepassing nadat React componenten op DOM teruggeeft. Gebruik klassenamen of gegevenskenmerken voor doelversie. |
| **Angular** | Doelelementen na wijzigingsdetectie door Angular. Vermijd het aanwijzen van elementen met `*ngIf` voordat ze worden gerenderd. |
| **Vue.js** | Wacht op Vue `nextTick` om ervoor te zorgen dat de elementen zich in het DOM bevinden. Gebruik verwijzingen of aangepaste kenmerken voor een stabiele doelbinding. |
| **Next.js / Nuxt.js** | Voor SSR/SSG- pagina&#39;s, zorg ervoor dat de hydratie van SDK van het Web wordt voltooid alvorens wijzigingen te verwachten. |

## Beste praktijken voor de verpersoonlijking van het KUUROORD

### Stabiele kiezers gebruiken

SPAs produceert vaak dynamische klassennamen of IDs (vooral met CSS-in-JS oplossingen). U kunt ook het volgende gebruiken:

* **attributen van Gegevens** - voeg de attributen van douanegegevens (`data-testid`, `data-section`, enz.) aan elementen toe u wilt richten.
* **Semantische HTML** - Doel die op de structuur en semantische elementen van HTML wordt gebaseerd.
* **attributen van identiteitskaart** - Gebruik stabiele attributen van identiteitskaart waar mogelijk.

**Voorbeeld:**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**CSS selecteur:** `[data-action="signup"]`

### Weergaven testen

Bij het testen van SPA-webervaringen:

1. Navigeer door alle weergaven waarop wijzigingen van toepassing zijn.

1. Test de volledige gebruikersstroom, inclusief:
   * Directe navigatie aan een mening (deep linking)
   * Navigatie van andere meningen binnen het KUUROORD
   * Browsernavigatie voor- en achteruit

1. Controleer of de wijzigingen opnieuw worden toegepast wanneer u terugkeert naar een eerder bezochte weergave.

### Weergaveovergangen voor handgrepen

Sommige SPAs gebruiken animaties of overgangen tussen meningen. Overweeg:

* **Timing** - verzeker wijzigingen van toepassing zijn nadat de overgangsanimaties volledig zijn.
* **zicht van het Element** - de Elementen kunnen bestaan maar tijdens overgangen worden verborgen.
* **Flickering** - pas vroegtijdig wijzigingen toe genoeg om zichtbare inhoudsveranderingen te vermijden.

## Problemen oplossen

Aangezien u de het ontwerpveranderingen van het SPA herzien, gebruik de volgende aanbevelingen om sommige gemeenschappelijke kwesties op te lossen:

* **Wijzigingen verschijnen niet** - als de wijzigingen niet op uw KUUROORD verschijnen:

   1. **mening het volgen van de Controle** - verifieer dat `sendEvent` de vraag de correcte meningsnaam omvat.

   1. **verifieer elementbestaan** - zorg ervoor dat de doelelementen in DOM zijn wanneer de wijzigingen van toepassing zijn.

   1. **de selecteurs van het Overzicht** - bevestig CSS selecteurs aanpassen de daadwerkelijke structuur DOM.

   1. **de console van de Controle** - zoek de fouten van JavaScript die wijzigingen zouden kunnen verhinderen.

* **Wijzigingen die kort verschijnen dan verdwijnend** - Deze kwestie komt typisch voor wanneer het KUUROORD herstelt en gewijzigde elementen vervangt:

   1. Gebruik specifiekere CSS-kiezers die stabiel blijven op alle renderweergaven.

   1. Schakel waarnemers van mutaties in om wijzigingen opnieuw toe te passen wanneer elementen opnieuw worden gemaakt.

   1. Werk met uw ontwikkelingsteam om stabiele attributen aan doelelementen toe te voegen.

* **dubbele aanpassingen** - als de wijzigingen veelvoudige tijden verschijnen:

   1. Controleer of gebeurtenissen voor het bijhouden van de weergave slechts eenmaal worden geactiveerd per weergaveovergang.

   1. Controleer of wijzigingen binnen het bereik van specifieke weergaven vallen in plaats van globaal toe te passen.

## Verwante onderwerpen

* [Overzicht van webervaringen](./web-experiences.md)
* [Webervaringsontwerp](./web-experience-design.md)
* [Webkanaalconfiguraties](../admin/configure-channels-web.md)