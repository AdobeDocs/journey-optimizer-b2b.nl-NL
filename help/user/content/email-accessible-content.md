---
title: Toegankelijke inhoud ontwerpen
description: Leer hoe u toegankelijke inhoud ontwerpt voor uw e-mails en landingspagina's in Journey Optimizer B2B edition
feature: Landing Pages
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: e-mail, ontwerp, toegankelijkheid
source-git-commit: 09391f6d7c3360d0624edd7dae6c25a8616046d9
workflow-type: tm+mt
source-wordcount: '1636'
ht-degree: 0%

---

# Toegankelijke inhoud ontwerpen {#accessible-content}

De [&#x200B; Europese toegankelijkheidswet &#x200B;](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} is een richtlijn die wordt ontworpen om de interne markt voor toegankelijke producten en diensten te verbeteren door barrières weg te nemen die door verschillende nationale regels in de lidstaten worden veroorzaakt.

Deze verordening bepaalt dat alle digitale communicatie, inclusief e-mails, nieuwsbrieven, PDF&#39;s en downloadbare inhoud, toegankelijk moet zijn. Wanneer u inhoud maakt voor uw ontvangers, moet u daarom bepaalde richtlijnen volgen, zoals het gebruik van toegankelijke lettertypen, leesbare indelingen en het aanbieden van alternatieve tekst voor afbeeldingen.

De [!DNL Journey Optimizer B2B Edition] ontwerphulpmiddelen laten marketers toe om inhoud zowel voor **e-mail** als **landende pagina&#39;s** te bouwen. Gebruik deze gereedschappen om te voldoen aan deze richtlijn, gebaseerd op Web Content Accessibility Guidelines (WCAG) 2.1, niveau AA.

In de volgende secties wordt een overzicht gegeven van de aanbevolen procedures voor het ontwerpen van toegankelijke inhoud met [!DNL Journey Optimizer B2B Edition] . Deze informatie richt zich op het ontwerpen van inhoud die toegankelijk is voor al uw ontvangers, zodat mensen met een handicap uw e-mails en landingspagina&#39;s kunnen lezen, begrijpen en ermee kunnen communiceren.
 

## Zorg ervoor dat de tekst leesbaar is {#text-readability}

Gebruik de tab **[!UICONTROL Styles]** van de component **[!UICONTROL Text]** om ervoor te zorgen dat de tekst leesbaar is, bijvoorbeeld door een juist kleurcontrast en eenvoudige lettertypen te gebruiken. Voor meer informatie over de vormgeving van tekstcomponenten, zie [&#x200B; componenten van de Inhoud &#x200B;](content-components.md#text)

{het lusje van de de componentenStijlen van de Tekst van 0} het tonen van doopvont, grootte, en kleurenopties ![](assets/accessible-text-styles.png){width="700" zoomable="yes"}

Volg onderstaande richtlijnen voor lettertypen en tekst:

### Fontselectie

* Gebruik sans-serif-lettertypen, zoals Arial, Verdana, Tahoma, Helvetica of Open Sans.
* Vermijd serif-, cursieve of decoratieve lettertypen in de inhoud van het lichaam.
* Selecteer een beperkte lettertypeset voor consistentie en fallback (bijvoorbeeld: `font-family: Arial, Helvetica, sans-serif;`).

### Fontgrootte

* Zorg voor een minimale tekengrootte van 16 px voor platte tekst.
* Gebruik een juiste hiërarchie voor koppen.

### Kleurcontrast

* Houd een contrastverhouding van minstens 4.5 :1 tussen tekst en achtergrond.
* Voor grote tekst (≥ 24px of gewaagd 18px), zorg minstens een 3 :1 contrast.
* Vermijd lichtgrijze of pasteltekst op witte achtergronden.
* Vertrouw niet op kleur alleen om betekenis over te brengen, maar gebruik in plaats daarvan onderstrepingen, pictogrammen, enzovoort.

### Toegankelijkheid van tekst

* Vermijd tekst in afbeeldingen.
* Gebruik niet alle uiteinden in lichaamstekst.
* Zorg ervoor dat op tekst kan worden ingezoomd tot 200% zonder de layout te verbreken.

## Zorg voor visuele toegankelijkheid {#visual-accessibility}

Volg onderstaande tips om te controleren of uw inhoud visueel toegankelijk is:

* Vermijd het gebruik van alleen-kleuren-indicatoren voor belangrijke informatie.
* Gebruik tekstlabels of pictogrammen voor meer duidelijkheid.
* Optimaliseer uw ontwerp voor mobiele en responsieve lay-outs, zodat de knoppen groot zijn en de juiste afstand hebben.
* Regelmatig testen op verschillende apparaten en schermformaten om de toegankelijkheid te behouden.

In [!DNL Journey Optimizer B2B Edition] kunt u de grootte en tussenruimte van de verschillende elementen in uw inhoud verder verfijnen met de opmaakparameters en -kenmerken uit het deelvenster Designer e-mailen **[!UICONTROL Styles]** .

U kunt bijvoorbeeld de achtergrond bijwerken of de marges, opvulling en uitlijning wijzigen om de visuele toegankelijkheid van de inhoud te verbeteren.

![&#x200B; ruit van Stijlen met achtergrond, marges, het opvullen, en groeperingsmontages &#x200B;](assets/accessible-styles.png){width="700" zoomable="yes"}

Bovendien kunt u met de [!DNL Journey Optimizer B2B Edition] Email Designer een voorvertoning weergeven van het ontwerp van verschillende apparaten en schermgrootten en het ontwerp ervan optimaliseren. U kunt op elk gewenst moment **[!UICONTROL Switch to live view]** controleren hoe uw inhoud op verschillende apparaatgrootten wordt gerenderd.

![&#x200B; Levende meningsknevel het tonen van Desktop, tablet, en mobiele voorproefopties &#x200B;](assets/accessible-live-view.png){width="700" zoomable="yes"}

>[!CAUTION]
>
>De live weergave is een algemene voorvertoning die is ontworpen om te vergelijken hoe de rendering er tussen verschillende apparaatgrootten uitziet. De uiteindelijke rendering kan variëren afhankelijk van de e-mailclient van de ontvanger.

## Alternatieve tekst gebruiken voor afbeeldingen {#alt-text}

Gebruik de component **[!UICONTROL Image]** om alternatieve tekst voor afbeeldingen te bieden. Voor meer informatie over de montages van de beeldcomponent, zie [&#x200B; componenten van de Inhoud &#x200B;](content-components.md#image)

![&#x200B; de componenteninstellingenpaneel van het Beeld met Afwisselend benadrukt tekstgebied &#x200B;](assets/accessible-alt-text.png){width="700" zoomable="yes"}

Volg onderstaande richtlijnen voor effectieve alternatieve tekst in digitale producten:

* Beschrijf het doel van de afbeelding beknopt en contextueel.
* Vermijd overbodige zinnen zoals &quot;Afbeelding van ...&quot; en gebruik lege alt-tekst voor decoratieve afbeeldingen.
* Gebruik voor pictogrammen met betekenis, nuttige labels en voor complexe afbeeldingen een korte alt-tekst plus een langere beschrijving elders.

## Leesbare indeling gebruiken {#readable-format}

Gebruik de e-mail van Designer relevante structuur en [&#x200B; inhoudscomponenten &#x200B;](content-components.md), evenals de opties in de **[!UICONTROL Styles]** ruit, om uw inhoud op een duidelijke, logische en beknopte manier te organiseren die voor allen toegankelijk is.

![&#x200B; E-mail Designer die structuur en inhoudscomponenten voor georganiseerde lay-outs tonen &#x200B;](assets/accessible-components.png){width="800" zoomable="yes"}

* Gebruik gestructureerde, semantische HTML met de juiste koppen, alinea&#39;s, lijsten en tabellen.
* Zorg ervoor dat de inhoud een logische stroom volgt van links naar rechts en van boven naar beneden.
* Gebruik duidelijke, beknopte taal.
* Alternatieve indelingen bieden voor PDF&#39;s en informatie.
* Formaat van tekst wijzigen en opnieuw plaatsen toestaan en ervoor zorgen dat typografie met een passend kleurcontrast in alle indelingen kan worden gelezen.

## Leesbaarheid van inhoud garanderen {#readability}

Om leesbaar te zijn, moet uw inhoud duidelijk zijn, goed gestructureerd, en bruikbaar voor iedereen, met inbegrip van mensen met visuele, cognitieve, of lezingsmoeilijkheden en degenen die hulptechnologieën gebruiken. Enkele punten waarmee u rekening moet houden bij het maken van toegankelijke inhoud zijn:

* Zelden van zinnen tot ongeveer 20 woorden of minder.
* Bewerk de kopie om direct naar het punt te gaan.
* Gebruik actieve stem om de zinsstructuur eenvoudiger te houden.
* Vermijd slang, jargon of regionale woorden die sommige mensen misschien niet kennen.

Om uw e-mailleesbaarheid te evalueren, gebruik de populaire [&#x200B; test van de Versnelling van de Lezing van de Vlesch &#x200B;](https://support.microsoft.com/en-us/office/get-your-document-s-readability-and-level-statistics-85b4969e-e80a-4777-8dd3-f7fc3c8b3fd2){target="_blank"} in Microsoft Word. Het berekent hoe gemakkelijk uw inhoud is om op een schaal van 0-100 te lezen.

## Uw inhoud testen {#test}

Om de toegankelijkheid van uw inhoud te controleren, kunt u de testmogelijkheden gebruiken die door [!DNL Journey Optimizer B2B Edition] worden verstrekt. Ze zijn niet specifiek ontworpen om te controleren of uw inhoud volledig toegankelijk is, maar ze kunnen wel een eerste verificatieniveau bieden.

* Geef een voorvertoning van de inhoud weer met testprofielen.

* Gebruik de [&#x200B; E-mail die &#x200B;](email-test-rendering.md) optie teruggeeft die hefboomwerkingen Litmus om uw ontwerpen over belangrijke e-mailcliënten (de Post van Apple, Gmail, Vooruitzichten) te simuleren en te zien of maken de tekst, de kleuren en de beelden uw inhoud toegankelijk. <!--Litmus includes accessibility testing-->

* Verzend proefdrukken om de rendering van uw inhoud te testen voordat u deze naar uw echte publiek stuurt.

![&#x200B; de simulatieinterface van de inhoud met de opties van de de voorproef van het testprofiel &#x200B;](assets/accessible-simulate.png){width="800" zoomable="yes"}

Als u op een meer consistente manier wilt controleren of uw inhoud betrouwbaar toegankelijk is, gaat u naar specifieke externe gereedschappen, zoals:

* De [&#x200B; contrastcontrole WebAim &#x200B;](https://webaim.org/resources/contrastchecker/){target="_blank"} en het [&#x200B; hulpmiddel van de de evaluatie van de Webtoegankelijkheid van de WAVE &#x200B;](https://wave.webaim.org/){target="_blank"} om contrast en naleving te evalueren;

* De technologieën van de hulp zoals het schermlezers (bijvoorbeeld: [&#x200B; NVDA &#x200B;](https://www.nvaccess.org/download/){target="_blank"}, of [&#x200B; VoiceOver &#x200B;](https://support.apple.com/en-ie/guide/iphone/iph3e2e415f/ios){target="_blank"} op iPhone) om e-mails van het perspectief van visueel gehandicapte gebruikers te ervaren.

## Donkere modus gebruiken {#dark-mode}


De donkere modus verbetert de visuele toegankelijkheid voor gebruikers met lichtgevoeligheid of een visuele handicap voor een betere kijkervaring.

![&#x200B; E-mailvoorproef die lichte wijze en donkere wijzerenteruggeven vergelijkt &#x200B;](assets/accessible-dark-mode.png){width="800" zoomable="yes"}

Gebruik bij het ontwerpen voor de donkere modus transparante PNG- of SVG-afbeeldingen en stel de juiste metatags en CSS in. Maak toegankelijke fallback-stijlen als de donkere modus niet wordt ondersteund. Test ten slotte alle e-mailinhoud en UI-elementen in zowel de lichte als de donkere modus.

## Specifieke kenmerken voor toegankelijkheid gebruiken {#attributes}

### Taalkenmerken {#language}

Wanneer u ontwerpen maakt, neemt u de kenmerken `lang` (taal) en `dir` (tekstrichting) op in de hoofdtekst van de inhoud. Deze kenmerken helpen ondersteunende hulpmiddelen, zoals schermlezers, om uw inhoud op de juiste manier te interpreteren en te presenteren.

* Het attribuut `lang` geeft de taal van de e-mail aan ondersteunende technologieën aan, zodat woorden correct worden uitgesproken.

  +++Voorbeelden

  Voorbeeld voor Engels:

  ```
  <body lang="en">
  ```

  Voorbeeld voor Frans:

  ```
  <body lang="fr">
  ```

  +++

* Het kenmerk `dir` geeft de tekstrichting op. De meeste talen, waaronder Engels en Frans, worden van links naar rechts (ltr) gelezen, terwijl talen zoals Arabisch en Hebreeuws van rechts naar links (rtl) worden gelezen.

  +++Voorbeelden

  Voorbeeld voor Engels (van links naar rechts):

  ```html
  <body lang="en" dir="ltr">
  ```

  Voorbeeld voor Arabisch (van rechts naar links):

  ```html
  <body lang="ar" dir="rtl">
  ```

  +++

Schermlezers vertrouwen op het kenmerk `lang` om de juiste uitroepingsregels toe te passen. Met de tekstrichting zorgt u ervoor dat de inhoud op natuurlijke wijze doorloopt in talen die van links naar rechts of van rechts naar links worden geschreven. Zonder deze kenmerken kunnen gebruikers last krijgen van verwarrende leesvolgorde of verkeerde uitspraak. Plaats daarom altijd de juiste kenmerken voor `lang` en `dir` in de hoofdtekst van de e-mail.

>[!TIP]
>
>Als uw e-mail meerdere talen bevat, wijst u de juiste taalkenmerken toe aan specifieke secties (zoals `<table>` - of `<td>` -blokken) om ervoor te zorgen dat elk onderdeel correct wordt gelezen.

### Tabellen {#tables}

In HTML-inhoud worden tabellen vaak gebruikt voor de lay-out. Standaard behandelen schermlezers elke `<table>` als een gegevenstabel, waarbij rijen, kolommen en structuur worden aangekondigd. Deze structuur kan verwarrend zijn als de tabel alleen wordt gebruikt voor opmaak.

Voeg `role="presentation"` (of `role="none"` ) toe aan indelingstabellen om ervoor te zorgen dat ondersteunende hulpmiddelen hun structuur overslaan en alleen de werkelijke inhoud activeren.

+++Voorbeeld - Lay-outtabel (met `role="presentation"`)

```html
<table role="presentation" border="0" cellpadding="0" cellspacing="0" width="100%"> 
  <tr> 
    <td align="center"> 
      <h1>Hello World</h1> 
      <p>Welcome to our newsletter</p> 
    </td> 
  </tr> 
</table>
```

De schermlezers lezen:
&quot;Hallo wereld. Welkom bij deze nieuwsbrief.&quot; *(Geen vermelding van rijen, kolommen of tabel)*

+++

+++Voorbeeld - Gegevenstabel (zonder `role="presentation"`)

```html
<table border="1" cellpadding="5" cellspacing="0"> 
  <tr> 
    <th scope="col">Name</th> 
    <th scope="col">Score</th> 
  </tr> 
  <tr> 
    <td>Alice</td> 
    <td>95</td> 
  </tr> 
  <tr> 
    <td>Bob</td> 
    <td>88</td> 
  </tr> 
</table> 
```

De schermlezers lezen:
&quot;Tabel met 2 kolommen en 3 rijen.&quot;

&quot;Naam, Alice. Score, 95.&quot;

&quot;Naam, Bob. Score, 88.&quot;

+++

>[!TIP]
>
>Gebruik `role="presentation"` uitsluitend voor lay-outtabellen. Voor gegevenstabellen, behoud de semantische `<table>` structuur zodat de schermlezers correct kopballen en verhoudingen kunnen aankondigen.

### Tekst voor koppelingen {#links}

Schermlezers lezen koppelingen voor met behulp van hun tekst. Als een verbinding wordt geëtiketteerd slechts _hier_ klikt of _meer_ leest, kennen de gebruikers van hulptechnologieën niet de bestemming. Om toegankelijkheid te waarborgen, hebben ze beschrijvende tekst nodig die het doel of de actie duidelijk aangeeft.

Gebruik de Designer-mailtoepassing om een koppeling naar uw inhoud toe te voegen en het label te bewerken, zodat deze herkenbaar (zichtbaar) en beschrijvend (duidelijk over het doel) is. Vermijd vage etiketten zoals _hier_ of _meer_.

![&#x200B; paneel dat van de montages van de Verbinding URL gebied en beschrijvende etiketopties toont &#x200B;](assets/accessible-link.png){width="600" zoomable="yes"}

+++Voorbeeld - Goede koppeling (beschrijvend): 

```
<p>Learn more in the  
<a href="https://adobe.com/release-notes">August release notes</a>. 
</p>
```

De schermlezers lezen:
&quot;Link, August release notes.&quot;

+++

+++Voorbeeld - Ongeldige koppeling (niet beschrijvend)

```
<p>Learn more about our new features.  
  <a href="https://adobe.com/release-notes">Click here</a>. 
</p>
```

De schermlezers lezen:
&quot;Link, klik hier.&quot; *(Verstrekt geen context uit leesorde)*

+++

## Ondersteuning voor toetsenbordnavigatie en focus bieden {#keyboard}

<!--for landing pages-->

Als u ondersteuning biedt voor toetsenbordnavigatie en focus, kunnen mensen die geen muis kunnen gebruiken, toegang krijgen tot en werken met inhoud. Het verbetert ook de algemene bruikbaarheid door alle gebruikers een duidelijke en consistente manier te geven om door informatie te bewegen.

* Focus via toetsenbord
   * Zorg ervoor dat alle interactieve elementen (zoals knoppen, selectievakjes, koppelingen) `tabindex="0"` hebben, zodat ze in de natuurlijke tabvolgorde worden opgenomen.
   * Navigeren met de Tab- en pijltoetsen ( ↑ &lt;ART →) toestaan, waardoor het element dat de focus heeft zichtbaar moet worden gemarkeerd.
* Aangepaste focusstijl
   * Pas duidelijke en te onderscheiden stijlen toe om zich op actioneerbare elementen te concentreren:
     +++Voorbeeld (CSS)

     ```
     [tabindex="0"] : focus { 
     outline: 2px solid #00AEEF;  /* Cyan border */ 
     background-color: #20CEFF;   /* Optional background */ 
     }
     ```

     +++

   * Zorg ervoor dat focusindicatoren voldoen aan de WCAG 2.2-standaarden voor focusweergave, waaronder:
      * Minimaal gebied: 2 CSS-pixels dikke omtrek.
      * Contrastverhouding: ≥ 3 :1 tussen de toestand Gericht en niet-geconcentreerd.

* Ondersteuning voor toetsenbordactivering
   * Zorg ervoor dat selectievakjes en knoppen reageren op de Enter- en Space-toets.
   * Valideer de interactie met alleen het toetsenbord:
      * Voer selectievakjes in of gebruik de spatiebalk.
      * Voer de knoppen in of gebruik de spatiebalk.
