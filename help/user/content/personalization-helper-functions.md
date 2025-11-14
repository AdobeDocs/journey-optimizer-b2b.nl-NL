---
title: Helpfuncties
description: Referentiegids voor hulpfuncties voor personalisatie in Journey Optimizer B2B edition. Hieronder vindt u syntaxis en voorbeelden voor tekenreeksen, datums, wiskunde en meer.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expressie, editor, syntaxis, personalisatie
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4853'
ht-degree: 0%

---

# Helpfuncties

Met de Helper-functies in de verpersoonlijkingseditor kunt u nauwkeurig en efficiënt gepersonaliseerde inhoud definiëren door gegevens te manipuleren, berekeningen uit te voeren en inhoud op te maken. Experimenteer en experimenteer met deze functies, operatoren en helpers om te ontdekken hoe ze samenwerken om u te helpen op maat gemaakte, gegevensgestuurde reizen te maken.

>[!AVAILABILITY]
>
>De functies van de hulp zijn beschikbaar voor de milieu&#39;s van B2B edition van de Optimizer van de Journaal die op de [ vereenvoudigde architectuur ](../simplified-architecture.md) worden voorzien.

## Samenvoegingsfuncties

Gebruik aggregatiefuncties om meerdere waarden te groeperen en één samenvattingswaarde te maken. U kunt ook array- en lijstfuncties gebruiken om gemakkelijker interacties met arrays, lijsten en tekenreeksen te definiëren.

### gemiddelde {#average}

Gebruik de functie `average` om het rekenkundig gemiddelde van alle geselecteerde waarden binnen de array te retourneren.

+++Syntaxis

```sql
{%= average(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de gemiddelde prijs van alle orders.

```sql
{%=average(orders.order.price)%}
```

+++

### aantal {#count}

Gebruik de functie `count` om het aantal elementen binnen de opgegeven array te retourneren.

+++Syntaxis

```sql
{%= count(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert het aantal orders in de array.

```sql
{%= count(orders) %}
```

+++

### max {#max}

Gebruik de functie `max` om de grootste van alle geselecteerde waarden binnen de array te retourneren.

+++Syntaxis

```sql
{%= max(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de hoogste prijs van alle orders.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

Gebruik de functie `min` om de kleinste van alle geselecteerde waarden in de array te retourneren.

+++Syntaxis

```sql
{%= min(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de laagste prijs van alle orders.

```sql
{%=min(orders.order.price) %}
```

+++

### som {#sum}

Gebruik de functie `sum` om de som van alle geselecteerde waarden in de array te retourneren.

+++Syntaxis

```sql
{%= sum(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de som van de prijzen van alle orders.

```sql
 {%=sum(orders.order.price)%}
```

+++

## Rekenkundige functies {#maths}

Gebruik rekenkundige functies om basisberekeningen van waarden uit te voeren.

### toevoegen {#add}

Gebruik de functie `+` (optellen) om de som van twee argumentexpressies te vinden.

+++Syntaxis

```sql
{%= double + double %}
```

**Voorbeeld**

De volgende transactie geeft de prijs van twee verschillende producten weer.

```sql
{%= product1.price + product2.price %}
```

+++

### vermenigvuldigen {#multiply}

Gebruik de functie `*` (vermenigvuldigen) om het product van twee argumentexpressies te zoeken.

+++Syntaxis

```sql
{%= double * double %}
```

**Voorbeeld**

Bij de volgende bewerking worden het product van de inventaris en de prijs van een product gevonden om de brutowaarde van het product te bepalen.

```sql
{%= product.inventory * product.price %}
```

+++

### aftrekken {#substract}

Gebruik de functie `-` (aftrekken) om het verschil tussen twee argumentexpressies te vinden.

+++Syntaxis

```sql
{%= double - double %}
```

**Voorbeeld**

De volgende transactie vindt het prijsverschil tussen twee verschillende producten.

```sql
{%= product1.price - product2.price %}
```

+++

### delen {#divide}

Gebruik de functie `/` (delen) om het quotiënt van twee argumentexpressies te vinden.

+++Syntaxis

```sql
{%= double / double %}
```

**Voorbeeld**

Met de volgende bewerking wordt het quotiënt gevonden tussen de totale verkochte producten en het totale verdiende geld om de gemiddelde kosten per object te zien.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### restant {#remainder}

Gebruik de functie `%` (rest) om de rest te zoeken na het delen van de twee argumentexpressies.

+++Syntaxis

```sql
{%= double % double %}
```

**Voorbeeld**

De volgende bewerking controleert of de leeftijd van de persoon met vijf personen kan worden gedeeld.

```sql
{%= person.age % 5 = 0 %}
```

+++

## Arrays en lijstfuncties {#arrays}

Gebruik deze functies om interactie met arrays, lijsten en tekenreeksen eenvoudiger te maken.

### countOnlyNull {#count-only-null}

Gebruik de functie `countOnlyNull` om het aantal null-waarden in een lijst te tellen.

+++Syntaxis

```sql
{%= countOnlyNull(array) %}
```

**Voorbeeld**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retourneert 3.

+++

### countWithNull {#count-with-null}

Gebruik de functie `countWithNull` om alle elementen van een lijst te tellen, inclusief null-waarden.

+++Syntaxis

```sql
{%= countWithNull(array) %}
```

**Voorbeeld**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Retourneert 6.

+++

### onderscheiden {#distinct}

Gebruik de functie `distinct` om waarden op te halen uit een array of lijst met verwijderde dubbele waarden.

+++Syntaxis

```sql
{%= distinct(array) %}
```

**Voorbeeld**

Met de volgende bewerking worden personen opgegeven die orders in meer dan één winkel hebben geplaatst.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### differentCountWithNull {#distinct-count-with-null}

Gebruik de functie `distinctCountWithNull` om het aantal verschillende waarden in een lijst te tellen met inbegrip van de ongeldige waarden.

+++Syntaxis

```sql
{%= distinctCountWithNull(array) %}
```

**Voorbeeld**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Retourneert 3.

+++

### kop {#head}

Gebruik de functie `head` om het eerste item in een array of lijst te retourneren.

+++Syntaxis

```sql
{%= head(array) %}
```

**Voorbeeld**

De volgende bewerking retourneert de eerste van de bovenste vijf bestellingen met de hoogste prijs. Meer informatie over de `topN` functie kan in [ eerst `n` in serie ](#first-n) sectie worden gevonden.

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

De functie `topN` sorteert een array in aflopende volgorde op basis van de opgegeven numerieke expressie en retourneert de eerste `N` -items. Wanneer de arraygrootte kleiner is dan `N` , wordt de volledige gesorteerde array geretourneerd.

+++Syntaxis

```sql
{%= topN(array, value, amount) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{ARRAY}` | De array of lijst die moet worden gesorteerd. |
| `{VALUE}` | De eigenschap die wordt gebruikt om de array of lijst te sorteren. |
| `{AMOUNT}` | Het aantal objecten dat moet worden geretourneerd. |

**Voorbeeld**

De volgende bewerking retourneert de eerste vijf bestellingen met de laagste prijs.

```sql
{%= topN(orders,price, 5) %}
```

+++

### in {#in}

Gebruik de functie `in` om te bepalen of een item lid is van een array of lijst.

+++Syntaxis

```sql
{%= in(value, array) %}
```

**Voorbeeld**

De volgende bewerking definieert personen met verjaardagen in maart, juni of september.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### include {#includes}

Gebruik de functie `includes` om te bepalen of een array of lijst een bepaald item bevat.

+++Syntaxis

```sql
{%= includes(array,item) %}
```

**Voorbeeld**

De volgende bewerking definieert personen van wie de favoriete kleur rood bevat.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### doorsnede {#intersects}

De functie `intersects` wordt gebruikt om te bepalen of twee arrays of lijsten ten minste één gemeenschappelijk lid hebben.

+++Syntaxis

```sql
{%= intersects(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert personen van wie de favoriete kleuren ten minste een van de kleuren rood, blauw of groen zijn.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

De functie `bottomN` sorteert een array in oplopende volgorde op basis van de opgegeven numerieke expressie en retourneert de eerste `N` -items. Wanneer de arraygrootte kleiner is dan `N` , wordt de volledige gesorteerde array geretourneerd.

+++Syntaxis

```sql
{%= bottomN(array, value, amount) %}
```

| Argument | Beschrijving |
| --------- | ----------- | 
| `{ARRAY}` | De array of lijst die moet worden gesorteerd. |
| `{VALUE}` | De eigenschap die wordt gebruikt om de array of lijst te sorteren. |
| `{AMOUNT}` | Het aantal objecten dat moet worden geretourneerd. |

**Voorbeeld**

De volgende bewerking retourneert de laatste vijf bestellingen met de hoogste prijs.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

Gebruik de functie `notIn` om te bepalen of een item geen lid is van een array of lijst.

>[!NOTE]
>
>De `notIn` functie ** zorgt ook ervoor dat geen van beide waarde aan ongeldig is. Daarom zijn de resultaten geen exacte negatie van de functie `in` .

+++Syntaxis

```sql
{%= notIn(value, array) %}
```

**Voorbeeld**

De volgende bewerking definieert personen met verjaardagen die zich niet in maart, juni of september bevinden.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### subsetOf {#subset}

Gebruik de functie `subsetOf` om te bepalen of een specifieke array (array A) een subset is van een andere array (array B). Met andere woorden, alle elementen in array A zijn elementen van array B.

+++Syntaxis

```sql
{%= subsetOf(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert mensen die al hun favoriete steden hebben bezocht.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### supersetOf {#superset}

Gebruik de functie `supersetOf` om te bepalen of een specifieke array (array A) een superset is van een andere array (array B). Met andere woorden, die array A bevat alle elementen in array B.

+++Syntaxis

```sql
{%= supersetOf(array1, array2) %}
```

**Voorbeeld**

De volgende bewerking definieert mensen die sushi en pizza hebben gegeten ten minste één keer.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## Datum- en tijdfuncties {#date-time}

Gebruik de datum- en tijdfuncties om datum- en tijdbewerkingen op waarden uit te voeren.

### addDays {#add-days}

De functie `addDays` past een bepaalde datum met een bepaald aantal dagen aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.

+++Syntaxis

```sql
{%= addDays(date, number) %}
```

**Voorbeeld**

* Invoer: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Uitvoer: `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

De functie `addHours` past een bepaalde datum met een bepaald aantal uren aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.

+++Syntaxis

```sql
{%= addHours(date, number) %}
```

**Voorbeeld**

* Invoer: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Uitvoer: `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

De functie `addMinutes` past een bepaalde datum met een opgegeven aantal minuten aan, waarbij positieve waarden worden gebruikt voor verhogen en negatieve waarden voor verlagen.

+++Syntaxis

```sql
{%= addMinutes(date, number) %}
```

**Voorbeeld**

* Invoer: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Uitvoer: `2024-11-01T18:09:51Z`

+++

### addMonths {#add-months}

De functie `addMonths` past een bepaalde datum met een bepaald aantal maanden aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.

+++Syntaxis

```sql
{%= addMonths(date, number) %}
```

**Voorbeeld**

* Invoer: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Uitvoer: `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

De functie `addSeconds` past een bepaalde datum met een bepaald aantal seconden aan, waarbij positieve waarden worden gebruikt om te verhogen en negatieve waarden om te verlagen.

+++Syntaxis

```sql
{%= addSeconds(date, number) %}
```

**Voorbeeld**

* Invoer: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Uitvoer: `2024-11-01T17:20:01Z`

+++

### addYear {#add-years}

De functie `addYears` past een bepaalde datum met een bepaald aantal jaren aan, gebruikend positieve waarden aan toename en negatieve waarden aan decrement.

+++Syntaxis

```sql
{%= addYears(date, number) %}
```

**Voorbeeld**

* Invoer: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Uitvoer: `2026-11-01T17:19:51Z`

+++

### ouderdom {#age}

Gebruik de functie `age` om de leeftijd vanaf een bepaalde datum op te halen.

+++Syntaxis

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

De functie `ageInDays` berekent het aantal dagen dat is verstreken tussen de opgegeven datum en de huidige datum. Het gebruikt negatief voor toekomstige data en positief voor vroegere data.

+++Syntaxis

```sql
{%= ageInDays(date) %}
```

**Voorbeeld**

currentDate = 2025-01-07T12 :17: 10.720122+05 :30 (Azië/Kolkata)

* Invoer: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Uitvoer: `5`

+++

### ageInMonths {#age-months}

De functie `ageInMonths` berekent het aantal maanden dat is verstreken tussen de opgegeven datum en de huidige datum. Het gebruikt negatief voor toekomstige data en positief voor vroegere data.

+++Syntaxis

```sql
{%= ageInMonths(date) %}
```

**Voorbeeld**

currentDate = 2025-01-07T12 :22: 46.993748+05 :30 (Azië/Kolkata)

* Invoer: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Uitvoer: `12`

+++

### compareDates {#compare-dates}

De functie `compareDates` vergelijkt de eerste invoerdatum met de andere. Het keert 0 terug als date1 aan date2 gelijk is, -1 als date1 vóór date2 komt, en 1 als date1 na date2 komt.

+++Syntaxis

```sql
{%= compareDates(date1, date2) %}
```

**Voorbeeld**

* Invoer: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Uitvoer: `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

De functie `convertZonedDateTime` zet een datum-tijd om in een bepaalde tijdzone.

+++Syntaxis

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**Voorbeeld**

* Invoer: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Uitvoer: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

Gebruik de functie `currentTimeInMillis` om de huidige tijd in epoch milliseconds op te halen.

+++Syntaxis

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

Gebruik de functie `dateDiff` om het verschil tussen twee datums in aantal dagen op te halen.

+++Syntaxis

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

De `dayOfMonth` retourneert het getal dat de dag van de maand vertegenwoordigt.

+++Syntaxis

```sql
{%= dayOfMonth(datetime) %}
```

**Voorbeeld**

* Invoer: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Uitvoer: `5`

+++

### DayOfWeek {#day-week}

Gebruik de functie `dayOfWeek` om de dag van de week op te halen.

+++Syntaxis

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

Gebruik de functie `dayOfYear` om de dag van het jaar op te halen.

+++Syntaxis

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

De functie `diffInSeconds` retourneert het verschil tussen twee datums in seconden.

+++Syntaxis

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**Voorbeeld**

* Invoer: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Uitvoer: `50`

+++

### extractHours {#extract-hours}

De functie `extractHours` extraheert de uurcomponent uit een bepaald tijdstempel.

+++Syntaxis

```sql
{%= extractHours(date) %}
```

**Voorbeeld**

* Invoer: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `17`

+++

### extractMinutes {#extract-minutes}

De functie `extractMinutes` extraheert de component minute uit een bepaald tijdstempel.

+++Syntaxis

```sql
{%= extractMinutes(date) %}
```

**Voorbeeld**

* Invoer: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `19`

+++

### extractMonths {#extract-months}

De functie `extractMonth` extraheert de component month uit een opgegeven tijdstempel.

+++Syntaxis

```sql
{%= extractMonths(date) %}
```

**Voorbeeld**

* Invoer: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `11`

+++

### extractSeconds {#extract-seconds}

De functie `extractSeconds` extraheert de tweede component uit een bepaald tijdstempel.

+++Syntaxis

```sql
{%= extractSeconds(date) %}
```

**Voorbeeld**

* Invoer: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `51`

+++

### formatDate {#format-date}

Gebruik de functie `formatDate` om een datumtijdwaarde op te maken. De indeling moet een geldig Java `DateTimeFormat` -patroon zijn.

+++Syntaxis

```sql
{%= formatDate(datetime, format) %}
```

Waar de eerste tekenreeks het datumkenmerk is en de tweede waarde hoe u de datum wilt omzetten en weergeven.

>[!NOTE]
>
> Als een datumpatroon ongeldig is, wordt de datum teruggezet naar de ISO-standaardindeling.
>
> U kunt de datum die functies gebruiken Java zoals samengevat in [ documentatie van Oracle ](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Voorbeeld**

De volgende bewerking retourneert de datum in de volgende notatie: MM/DD/YY.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### Patroontekens {#pattern-characters}

Sommige patroonletters kunnen er hetzelfde uitzien, maar vertegenwoordigen verschillende concepten.

| Patroon | Betekenis | Voorbeeld (voor `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Kalenderjaar (standaardjaar) | `2023` |
| `Y` | Weekjaar (ISO 8601). Het kan per jaar verschillen. | `2024` (31 december 2023 valt in de eerste week van 2024) |
| `M` | Maand van jaar (1-12 of tekst zoals `Jan`, `January`) | `12` of `Dec` |
| `m` | Minuut-van-uur (0-59) | `15` |
| `d` | Dag van de maand (1-31) | `31` |
| `D` | Jaar (1-366) | `365` |

#### Datumnotatie met ondersteuning voor landinstellingen {#format-date-locale}

Met de functie `formatDate` kunt u een datumtijdwaarde opmaken in de corresponderende taalgevoelige representatie, bijvoorbeeld voor een gewenste landinstelling. De indeling moet een geldig Java `DateTimeFormat` -patroon zijn.

+++Syntaxis

```sql
{%= formatDate(datetime, format, locale) %}
```

Waar de eerste tekenreeks het datumkenmerk is, is de tweede waarde hoe u de datum wilt converteren en weergeven, en de derde waarde vertegenwoordigt de landinstelling in tekenreeksindeling.

>[!NOTE]
>
> Als een datumpatroon ongeldig is, wordt de datum teruggezet naar de ISO-standaardindeling.
>
> U kunt de datum het formatteren functies van Java zoals samengevat in de [ documentatie van Oracle ](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) gebruiken.
>
> U kunt het formatteren en geldige scènes gebruiken zoals samengevat in de [ documentatie van Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) en [ Gesteunde scènes ](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Voorbeeld**

De volgende bewerking retourneert de datum in de volgende notatie: MM/dd/YY en landinstelling FRANKRIJK.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

De functie `getCurrentZonedDateTime` retourneert de huidige datum en tijd met informatie over de tijdzone.

+++Syntaxis

```sql
{%= getCurrentZonedDateTime() %}
```

**Voorbeeld**

* Invoer: `{%= getCurrentZonedDateTime() %}`
* Uitvoer: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

De functie `diffInHours` retourneert het verschil tussen twee datums in termen van uren.

+++Syntaxis

```sql
{%= diffInHours(endDate, startDate) %}
```

**Voorbeeld**

* Invoer: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Uitvoer: `10`

+++

### diffInMinutes {#diff-minutes}

De functie `diffInMinutes` retourneert het verschil tussen twee datums in minuten.

+++Syntaxis

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**Voorbeeld**

* Invoer: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Uitvoer: `60`

+++

### diffInMonths {#months-difference}

De functie `diffInMonths` retourneert het verschil tussen twee datums in termen van maanden.

+++Syntaxis

```sql
{%= diffInMonths(endDate, startDate) %}
```

**Voorbeeld**

* Invoer: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Uitvoer: `3`

+++

### setDays {#set-days}

Gebruik de functie `setDays` om de dag van de maand voor de opgegeven datum-tijd in te stellen.

+++Syntaxis

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

Gebruik de functie `setHours` om het uur van de datum-tijd in te stellen.

+++Syntaxis

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

De functie `toDateTime` zet een tekenreeks om in datum. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.

+++Syntaxis

```sql
{%= toDateTime(string, string) %}
```

**Voorbeeld**

* Invoer: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Uitvoer: `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

Gebruik de functie `toUTC` om een datetime om te zetten in UTC.

+++Syntaxis

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

Gebruik de `truncateToStartOfDay` functie om een bepaalde datum-tijd te wijzigen door het aan het begin van de dag met tijd bij 00 :00 te plaatsen.

+++Syntaxis

```sql
{%= truncateToStartOfDay(date) %}
```

**Voorbeeld**

* Invoer: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Uitvoer: `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

Gebruik de functie `truncateToStartOfQuarter` wordt gebruikt om een datum-tijd aan de eerste dag van zijn kwartaal (zoals 1 Januari, 1 April, 1 Juli, 1 Oktober 1) om 00 te beknotten :00.

+++Syntaxis

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**Voorbeeld**

* Invoer: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

De functie `truncateToStartOfWeek` wijzigt een bepaalde datum-tijd door het aan het begin van de week (Maandag bij 00 :00 te plaatsen).

+++Syntaxis

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**Voorbeeld**

* Invoer: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Uitvoer: `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

Gebruik de functie `truncateToStartOfYear` om een bepaalde datum-tijd te wijzigen door het te beknotten aan de eerste dag van het jaar (1 Januari) bij 00 :00.

+++Syntaxis

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**Voorbeeld**

* Invoer: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Uitvoer: `2024-01-01T00:00Z`

+++

### weekOfYear {#week-of-year}

Gebruik de functie `weekOfYear` om de week van het jaar op te halen.

+++Syntaxis

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYear {#diff-years}

Gebruik de functie `diffInYears` om het verschil tussen twee datums in termen van jaren te retourneren.

+++Syntaxis

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**Voorbeeld**

* Invoer: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Uitvoer: `5`

+++

## Operator-functies {#operators}

Gebruik de functies Boolean en Compare om logische evaluaties uit te voeren.

### en {#and}

De functie `and` wordt gebruikt om een logische combinatie te maken.

+++Syntaxis

```sql
{%= query1 and query2 %}
```

**Voorbeeld**

De volgende operatie retourneert alle mensen in het thuisland (Frankrijk) en het geboortejaar (1985).

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### of {#or}

De functie `or` wordt gebruikt om een logische scheiding te maken.

+++Syntaxis

```sql
{%= query1 or query2 %}
```

**Voorbeeld**

De volgende operatie retourneert alle mensen in het thuisland (Frankrijk) of het geboortejaar (1985).

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### equals {#operator-equals}

De functie `=` (equals) controleert of een waarde of expressie gelijk is aan een andere waarde of expressie.

+++Syntaxis

```sql
{%= expression = value %}
```

**Voorbeeld**

De volgende operatie controleert of het thuisadresland Frankrijk is.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### niet gelijk aan {#notequal}

De `!=` (niet gelijk aan) functie controleert of één waarde of uitdrukking **** niet gelijk aan een andere waarde of een uitdrukking is.

+++Syntaxis

```sql
{%= expression != value %}
```

**Voorbeeld**

De volgende operatie controleert of het thuisadresland niet Frankrijk is.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### groter dan {#greaterthan}

Controleer met de functie `>` (groter dan) of de eerste waarde groter is dan de tweede waarde.

+++Syntaxis

```sql
{%= expression1 > expression2 %}
```

**Voorbeeld**

De volgende bewerking definieert personen die strikt na 1970 geboren zijn.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### groter dan of gelijk aan {#greaterthanorequal}

Gebruik de functie `>=` (groter dan of gelijk aan) om te controleren of de eerste waarde groter dan of gelijk is aan de tweede waarde.

+++Syntaxis

```sql
{%= expression1 >= expression2 %}
```

**Voorbeeld**

In de volgende bewerking worden personen gedefinieerd die in of na 1970 zijn geboren.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### minder dan {#lessthan}

Gebruik de vergelijkingsfunctie `<` (kleiner dan) om te controleren of de eerste waarde kleiner is dan de tweede waarde.

+++Syntaxis

```sql
{%= expression1 < expression2 %}
```

**Voorbeeld**

In de volgende bewerking worden personen gedefinieerd die vóór 2000 zijn geboren.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### kleiner dan of gelijk aan{#lessthanorequal}

Gebruik de vergelijkingsfunctie `<=` (kleiner dan of gelijk aan) om te controleren of de eerste waarde kleiner dan of gelijk is aan de tweede waarde.

+++Syntaxis

```sql
{%= expression1 <= expression2 %}
```

**Voorbeeld**

De volgende bewerking definieert personen die in 2000 of eerder zijn geboren.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## Dynamische functies {#dynamic-helpers}

Gebruik de dynamische hulpfuncties om voorwaardelijke evaluaties, herhaling en veranderlijke toewijzingen voor dynamische verpersoonlijking te gebruiken.

### Standaardwaarde voor alternatieven {#default-value}

De `Default Fallback Value` helper wordt gebruikt om een standaardreservewaarde terug te keren als een attribuut leeg of ongeldig is. Dit mechanisme werkt voor Profielkenmerken en Reisgebeurtenissen.

+++Syntaxis

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In dit voorbeeld wordt de waarde `there` weergegeven als het `firstName` -kenmerk van dit profiel leeg of null is.

+++

### if (voorwaarden) {#if-function}

De hulpfunctie `if` wordt gebruikt om een voorwaardelijk blok te definiëren.
Als de uitdrukkingsevaluatie waar terugkeert, wordt het blok teruggegeven anders wordt het overgeslagen.

+++Syntaxis

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Na de hulpfunctie `if` kunt u een instructie `else` invoeren om een codeblok op te geven dat moet worden uitgevoerd als dezelfde voorwaarde false is.
De instructie `elseif` geeft een nieuwe voorwaarde op die moet worden getest als de eerste instructie false retourneert.


**Formaat**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### tenzij {#unless}

Met de `unless` -hulplijn kunt u een voorwaardelijk blok definiëren. Als de evaluatie van de expressie false retourneert, wordt het blok gerenderd als dit tegengesteld is aan de `if` helper.

+++Syntaxis

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Voorbeeld**

Geef wat inhoud weer op basis van de extensie van het e-mailadres:

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### elk {#each}

Gebruik de hulpfunctie `each` om een array te doorlopen.

De hulpstructuur is ```{{#each ArrayName}}``` YourContent `{{/each}}`

U kunt het trefwoord `this` in het blok gebruiken om naar de afzonderlijke arrayitems te verwijzen. Gebruik `{{@index}}` om de index van het element van de array te renderen.

+++Syntaxis

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Voorbeeld**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Voorbeeld**

Een lijst met producten weergeven die deze gebruiker in zijn winkelwagentje heeft:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### with {#with}

Gebruik de `with` helper om het evaluatietoken van malplaatje-deel te veranderen.

+++Syntaxis

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

De hulpfunctie `with` is nuttig om ook een sneltoetsvariabele te definiëren.

**Voorbeeld**

Gebruik `with` voor het aliasing van lange variabelenamen naar kortere:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### laten {#let}

Met de functie `let` kan een expressie worden opgeslagen als een variabele die later in een query moet worden gebruikt.

+++Syntaxis

```sql
{% let variable = expression %} {{variable}}
```

**Voorbeeld**

In het volgende voorbeeld kunt u de totale som van prijzen voor producten in de winkelwagen berekenen met prijzen tussen 100 en 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## Metagegevens voor uitvoering {#execution-metadata}

>[!AVAILABILITY]
>
>Deze mogelijkheid is in Beperkte Beschikbaarheid. Neem contact op met uw Adobe-vertegenwoordiger voor toegang.

Gebruik `executionMetadata` om aangepaste sleutel-waardeparen dynamisch vast te leggen en op te slaan in de context van de berichtuitvoering.

Met deze functie kunt u contextafhankelijke informatie toevoegen aan elke native actie van uw campagnes of reizen. Gebruik dit programma om contextuele gegevens voor levering in real time naar externe systemen te exporteren voor verschillende doeleinden, zoals reeksspatiëring, analyse, personalisatie en downstreamverwerking.

>[!NOTE]
>
>Aangepaste acties ondersteunen de functie `executionMetadata` niet.

U kunt bijvoorbeeld de hulpfunctie `executionMetadata` gebruiken om een specifieke id toe te voegen aan elke levering die naar elk profiel wordt verzonden. Deze informatie wordt tijdens runtime gegenereerd en de verrijkte metagegevens voor uitvoering kunnen vervolgens worden geëxporteerd voor afstemming op een extern rapportageplatform.

+++Syntaxis

```
{{executionMetadata key="your_key" value="your_value"}}
```

In deze syntaxis verwijst `key` naar de naam van de metagegevens en is `value` de metagegevens die moeten worden voortgezet.

**hoe het** werkt

Selecteer een element uit de inhoud van uw kanaal in een campagne of een rit en voeg, met de personalisatie-editor, de `executionMetadata` -hulplijn toe aan dit element.

>[!NOTE]
>
>De functie `executionMetadata` is niet zichtbaar wanneer de inhoud zelf wordt weergegeven.

Tijdens runtime wordt de metagegevenswaarde toegevoegd aan de bestaande **[!UICONTROL Message Feedback Event Dataset]** met het volgende schema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>Er is een bovengrens van 2kb op de belangrijkste waardeparen per actie. Als de limiet van 2 kB wordt overschreden, wordt het bericht nog steeds geleverd, maar een van de sleutelwaardeparen kan worden afgekapt.

**Voorbeeld**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

In dit voorbeeld, uitgaande van `profile.person.name.firstName` = &quot;Alex&quot;, is de resulterende entiteit:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## Toewijzingsfuncties {#maps}

Gebruik kaartfuncties in personalisatie om interactie met kaarten eenvoudiger te maken.

### get {#get}

Gebruik de functie `get` om de waarde van een kaart voor een bepaalde sleutel op te halen.

+++Syntaxis

```sql
{%= get(map, string) %}
```

**Voorbeeld**

Met de volgende bewerking wordt de waarde van de identiteitskaart voor de sleutel `example@example.com` opgehaald.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### toetsen {#keys}

Gebruik de functie `keys` om alle sleutels voor een bepaalde kaart terug te winnen.

+++Syntaxis

```sql
{%= keys(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle toetsen voor de kaart `identityMap` opgehaald.

```sql
{%= keys(identityMap) %}
```

+++

### waarden {#values}

De functie `values` wordt gebruikt om alle waarden van een bepaalde kaart op te halen.

+++Syntaxis

```sql
{%= values(map) %}
```

**Voorbeeld**

Met de volgende bewerking worden alle waarden voor de kaart `identityMap` opgehaald.

```sql
{%= values(identityMap) %}
```

+++

## Math-functies {#math}

Leer hoe te om functies Math in de verpersoonlijkingsredacteur te gebruiken.

### absoluut {#absolute}

Gebruik de functie `absolute` om een getal om te zetten in de absolute waarde ervan.

+++Syntaxis

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

Gebruik de functie `formatNumber` om een willekeurig nummer op te maken in de taalgevoelige representatie.

Het accepteert een getal en een tekenreeks die de landinstelling vertegenwoordigen en retourneert een opgemaakte tekenreeks van het getal in de gewenste landinstelling.

+++Syntaxis

```sql
{%= formatNumber(number/double,string) %}: string
```

U kunt het formatteren en geldige scènes gebruiken zoals samengevat in de [ documentatie van Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) en [ Gesteunde scènes ](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Voorbeeld**

Deze query retourneert een opgemaakte tekenreeks in het Arabisch die overeenkomt met 123456,789 als het invoernummer.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### willekeurig {#random}

Gebruik de functie `random` om een willekeurige waarde tussen 0 en 1 te retourneren.

+++Syntaxis

```sql
{%= random() %}: double
```

+++

### roundDown {#round-down}

Gebruik de functie `roundDown` om een getal omlaag te afronden.

+++Syntaxis

```sql
{%= roundDown(double) %}: double
```

+++

### roundUp {#round-up}

Gebruik de functie `roundUp` om een getal naar boven te afronden.

+++Syntaxis

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

De functie `toHexString` zet om het even welk aantal in zijn hexadecimale koord om.

+++Syntaxis

```sql
{%= toHexString(number) %}: string
```

**Voorbeeld**

Deze query retourneert de hexadecimale waarde 158 als 9e.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

Gebruik de functie `toInt` om typen (getal, dubbel, geheel, lang, zwevend, kort, byte, boolean, tekenreeks) om te zetten in een geheel getal.

+++Syntaxis

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Voorbeeld**

Deze vraag keert de geheelwaarde van 42.6 als 42 terug.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercentage {#to-percentage}

Gebruik de functie `toPercentage` om een getal om te zetten in een percentage.

+++Syntaxis

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

Gebruik de functie `toPrecision` om een getal om te zetten in de vereiste precisie.

+++Syntaxis

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

De functie `toString` zet een willekeurig getal om in de tekenreeksrepresentatie.

+++Syntaxis

```sql
{%= toString(string) %}: string
```

**Voorbeeld**

Deze query retourneert `"12"` .

```sql
{%= toString(12) %} 
```

+++

## Objectfuncties {#objects}

Objectfuncties om objecteigenschappen of -kenmerken te controleren.

### isNull {#isNull}

De functie `isNull` bepaalt of een objectverwijzing niet bestaat.

+++Syntaxis

```sql
{%= isNull(object) %}
```

**Voorbeeld**

De volgende verrichting controleert als het huisadres van de persoon niet bestaat.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

De functie `isNotNull` bepaalt of een objectverwijzing bestaat.

+++Syntaxis

```sql
{%= isNotNull(object) %}
```

**Voorbeeld**

De volgende verrichting controleert als het huisadres van de persoon bestaat.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## Reeksfuncties {#string-functions}

Leer hoe te om de functies van het Koord in de verpersoonlijkingsredacteur te gebruiken.

### camelCase {#camelCase}

De functie `camelCase` maakt een hoofdletter van de eerste letter van elk woord van een tekenreeks.

+++Syntaxis

```sql
{%= camelCase(string)%}
```

**Voorbeeld**

Met de volgende functie krijgt de eerste letter van een woord een hoofdletter in het hoofdletteradres van het profiel.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

De functie `charCodeAt` retourneert de ASCII-waarde van een teken, net als de functie `charCodeAt` in JavaScript. Er wordt een tekenreeks en een geheel getal gebruikt (de positie van een teken wordt gedefinieerd) als invoerargumenten en de bijbehorende ASCII-waarde wordt geretourneerd.

+++Syntaxis

```sql
{%= charCodeAt(string,int) %}: int
```

**Voorbeeld**

De volgende functie retourneert de ASCII-waarde `o` (111).

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concat {#concate}

De functie `concat` combineert twee tekenreeksen in één.

+++Syntaxis

```sql
{%= concat(string,string) %}
```

**Voorbeeld**

De volgende functie combineert profielstad en land in één enkele koord.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### contains {#contains}

Gebruik de functie `contains` om te bepalen of een tekenreeks een opgegeven subtekenreeks bevat.

+++Syntaxis

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `STRING_1` | De tekenreeks die de controle moet uitvoeren. |
| `STRING_2` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `CASE_SENSITIVE` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeelden**

* De volgende functie controleert of de voornaam van het profiel de letter A bevat (in hoofdletters of kleine letters). Als het profiel dat wel doet, wordt `true` geretourneerd. Zo niet, dan wordt `false` geretourneerd.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon de tekenreeks `2010@gm` bevat.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContain {#doesNotContain}

Gebruik de functie `doesNotContain` om te bepalen of een tekenreeks geen opgegeven subtekenreeks bevat.

+++Syntaxis

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `STRING_1` | De tekenreeks die de controle moet uitvoeren. |
| `STRING_2` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `CASE_SENSITIVE` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon de tekenreeks `2010@gm` niet bevat.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

Gebruik de functie `doesNotEndWith` om te bepalen of een tekenreeks niet eindigt met een opgegeven subtekenreeks.

+++Syntaxis

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon niet eindigt met `.com`.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

Gebruik de functie `doesNotStartWith` om te bepalen of een tekenreeks niet begint met een opgegeven subtekenreeks.

+++Syntaxis

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of de naam van de persoon niet begint met `Joe`.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

Gebruik de functie `encode64` om een tekenreeks te coderen zodat Personal Information (PI) behouden blijft, bijvoorbeeld om in een URL te worden opgenomen.

+++Syntaxis

```sql
{%= encode64(string) %}
```

+++

### endWith {#endsWith}

Gebruik de functie `endsWith` om te bepalen of een tekenreeks eindigt met een opgegeven subtekenreeks.

+++Syntaxis

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. Mogelijke waarden: true (standaard) / false. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of het e-mailadres van de persoon eindigt met `.com`.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### equals {#equals}

Gebruik de functie `equals` om te bepalen of een tekenreeks gelijk is aan de opgegeven tekenreeks, met hoofdlettergevoeligheid.

+++Syntaxis

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of de naam van de persoon `John` is.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

Gebruik de functie `equalsIgnoreCase` om te bepalen of een tekenreeks gelijk is aan de opgegeven tekenreeks, zonder hoofdlettergevoeligheid.

+++Syntaxis

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende query bepaalt, zonder hoofdlettergevoeligheid, of de naam van de persoon `John` is.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

Gebruik de functie `extractEmailDomain` om het domein van een e-mailadres te extraheren.

+++Syntaxis

```sql
{%= extractEmailDomain(string) %}
```

**Voorbeeld**

De volgende query extraheert het e-maildomein van het persoonlijke e-mailadres.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

Gebruik de functie `formatCurrency` om een willekeurig getal om te zetten in de corresponderende taalgevoelige valutarepresentatie, afhankelijk van de landinstelling die als een tekenreeks in het tweede argument is doorgegeven.

+++Syntaxis

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Voorbeeld**

Deze query retourneert £ 56,00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

Gebruik de functie `getUrlHost` om de hostnaam van een URL op te halen.

+++Syntaxis

```sql
{%= getUrlHost(string) %}: string
```

**Voorbeeld**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Retourneert &quot;www.myurl.com&quot;

+++

### getUrlPath {#get-url-path}

Gebruik de functie `getUrlPath` om het pad na de domeinnaam van een URL op te halen.

+++Syntaxis

```sql
{%= getUrlPath(string) %}: string
```

**Voorbeeld**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Retourneert &quot;/contact.html&quot;

+++

### getUrlProtocol {#get-url-protocol}

Gebruik de functie `getUrlProtocol` om het protocol van een URL op te halen.

+++Syntaxis

```sql
{%= getUrlProtocol(string) %}: string
```

**Voorbeeld**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Retourneert &quot;http&quot;

+++

### indexOf {#index-of}

Gebruik de functie `indexOf` om de positie (in het eerste argument) van de eerste instantie van de tweede parameter te retourneren. Retourneert -1 als er geen overeenkomend actiepunt is.

+++Syntaxis

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die moet worden gezocht in de eerste parameter |

**Voorbeeld**

```sql
{%= indexOf("hello world","world" ) %}
```

Retourneert 6.

+++

### isEmpty {#isEmpty}

Gebruik de functie `isEmpty` om te bepalen of een tekenreeks leeg is.

+++Syntaxis

```sql
{%= isEmpty(string) %}
```

**Voorbeeld**

De volgende functie retourneert &#39;true&#39; als het mobiele telefoonnummer van het profiel leeg is. Anders wordt `false` geretourneerd.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

Gebruik de functie `isNotEmpty` om te bepalen of een tekenreeks niet leeg is.

+++Syntaxis

```sql
{= isNotEmpty(string) %}: boolean
```

**Voorbeeld**

De volgende functie retourneert &#39;true&#39; als het mobiele telefoonnummer van het profiel niet leeg is. Anders wordt `false` geretourneerd.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

Gebruik de functie `lastIndexOf` om de positie (in het eerste argument) van de laatste instantie van de tweede parameter te retourneren. Retourneert -1 als er geen overeenkomend actiepunt is.

+++Syntaxis

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die moet worden gezocht in de eerste parameter |

**Voorbeeld**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Retourneert 7.

+++

### leftTrim {#leftTrim}

Gebruik de functie `leftTrim` om witruimten te verwijderen uit het begin van een tekenreeks.

+++Syntaxis

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

Gebruik de functie `length` om het aantal tekens in een tekenreeks of expressie op te halen.

+++Syntaxis

```sql
{%= length(string) %}
```

**Voorbeeld**

De volgende functie retourneert de lengte van de stadsnaam van het profiel.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### leuk {#like}

Gebruik de functie `like` om te bepalen of een tekenreeks overeenkomt met een opgegeven patroon.

+++Syntaxis

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De expressie die moet overeenkomen met de eerste tekenreeks. Er zijn twee ondersteunde speciale tekens voor het maken van een expressie: `%` en `_` . <ul><li>`%` wordt gebruikt om nul of meer tekens te vertegenwoordigen.</li><li>`_` wordt gebruikt om precies één teken te vertegenwoordigen.</li></ul> |

**Voorbeeld**

Met de volgende query worden alle steden opgehaald waar profielen met het patroon `es` in de live map staan.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### lowerCase {#lower}

Gebruik de functie `lowerCase` om een tekenreeks om te zetten in kleine letters.

+++Syntaxis

```sql
{%= lowerCase(string) %}
```

**Voorbeeld**

Deze functie converteert de voornaam van het profiel naar kleine letters.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### overeenkomsten {#matches}

Gebruik de functie `matches` om te bepalen of een tekenreeks overeenkomt met een specifieke reguliere expressie. Voor meer informatie over passende patronen in regelmatige uitdrukkingen, verwijs naar [ de documentatie van Oracle ](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

+++Syntaxis

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Voorbeeld**

De volgende query bepaalt, zonder hoofdlettergevoeligheid, of de naam van de persoon begint met `John`.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### masker {#mask}

Gebruik de functie `mask` om een deel van een tekenreeks te vervangen door &#39;X&#39;-tekens.

+++Syntaxis

```sql
{%= mask(string,integer,integer) %}
```

**Voorbeeld**

De volgende query vervangt de tekenreeks &quot;123456789&quot; door &quot;X&quot;, behalve voor het eerste en laatste 2 tekens.

```sql
{%= mask("123456789",1,2) %}
```

De query retourneert `1XXXXXX89` .

+++

### md5 {#md5}

Gebruik de functie `md5` om de md5-hash van een tekenreeks te berekenen en te retourneren.

+++Syntaxis

```sql
{%= md5(string) %}: string
```

**Voorbeeld**

```sql
{%= md5("hello world") %}
```

Retourneert &quot;5eb63be01eeed093cb22bb8f5acdc3&quot;

+++

### notEqualTo {#notEqualTo}

Gebruik de functie `notEqualTo` om te bepalen of een tekenreeks niet gelijk is aan de opgegeven tekenreeks.

+++Syntaxis

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of de naam van de persoon niet `John` is.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

Gebruik de functie `notEqualWithIgnoreCase` om twee tekenreeksen te vergelijken waarbij hoofdletters en kleine letters worden genegeerd.

+++Syntaxis

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks die met de eerste tekenreeks moet worden vergeleken. |

**Voorbeeld**

De volgende query bepaalt of de naam van de persoon niet `john` is, zonder hoofdlettergevoeligheid.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### regexGroup {#regexGroup}

Gebruik de functie `regexGroup` om specifieke informatie te extraheren op basis van de reguliere expressie die wordt opgegeven.

+++Syntaxis

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING}` | De tekenreeks die de controle moet uitvoeren. |
| `{EXPRESSION}` | De reguliere expressie die moet overeenkomen met de eerste tekenreeks. |
| `{GROUP}` | Expressiegroep die moet worden gebruikt. |

**Voorbeeld**

De volgende query extraheert de domeinnaam uit een e-mailadres.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### vervangen {#replace}

Gebruik de functie `replace` om een bepaalde subtekenreeks in een tekenreeks te vervangen door een andere subtekenreeks.

+++Syntaxis

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks waar de subtekenreeks moet worden vervangen. |
| `{STRING_2}` | The substring to replace. |
| `{STRING_3}` | De vervangende subtekenreeks. |

**Voorbeeld**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Retourneert `Hello Mark, here is your monthly newsletter!`

+++

### replaceAll {#replaceAll}

Gebruik de functie `replaceAll` om alle subtekenreeksen van een tekst te vervangen die overeenkomt met de expressie regex met de opgegeven letterlijke vervangende tekenreeks. Regex hanteert speciale functies voor `\` en `+` en alle regex-expressies volgen de PQL escapstrategie. De vervanging vindt plaats vanaf het begin van de tekenreeks tot het einde, bijvoorbeeld wanneer `aa` wordt vervangen door `b` in de tekenreeks `aaa` , resulteert in `ba` in plaats van `ab` .

+++Syntaxis

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Wanneer de uitdrukking die als tweede argument wordt genomen een speciaal regex karakter is, gebruik dubbele backslash (`//`).  Speciale regex-tekens zijn: [., +, *, ?, ^, $, (, ), [, ], {, }, |, \.]
> 
> Leer meer in [ documentatie van Oracle ](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

+++

### rightTrim {#rightTrim}

De functie `rightTrim` verwijdert witruimten van het einde van een tekenreeks.

+++Syntaxis

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

De functie `sha256` berekent en retourneert de sha256-hash van een tekenreeks.

+++Syntaxis

```sql
{%= sha256(string) %} : string
```

**Voorbeeld**

```sql
{%= sha256("Eliechxh")%}
```

Retourneert `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

+++

### splitsen {#split}

Gebruik de functie `split` om een tekenreeks te splitsen op een bepaald teken.

+++Syntaxis

```sql
{%= split(string,string) %}
```

+++

### startWith {#startsWith}

Gebruik de functie `startsWith` om te bepalen of een tekenreeks begint met een opgegeven subtekenreeks.

+++Syntaxis

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschrijving |
| --------- | ----------- |
| `{STRING_1}` | De tekenreeks die de controle moet uitvoeren. |
| `{STRING_2}` | De tekenreeks waarnaar moet worden gezocht binnen de eerste tekenreeks. |
| `{CASE_SENSITIVE}` | Een optionele parameter om te bepalen of de controle hoofdlettergevoelig is. De standaardwaarde is true. |

**Voorbeeld**

De volgende query bepaalt, met hoofdlettergevoeligheid, of de naam van de persoon begint met `Joe`.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

De functie `stringToDate` zet een tekenreekswaarde om in een datum-tijdwaarde. Er zijn twee argumenten voor: tekenreeksrepresentatie van een datum-tijd en tekenreeksrepresentatie van de formatter.

+++Syntaxis

```sql
{= stringToDate("date-time value","formatter" %}
```

**Voorbeeld**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_integer {#string-to-integer}

Gebruik de functie `string_to_integer` om een tekenreekswaarde om te zetten in een geheel-getalwaarde.

+++Syntaxis

```sql
{= string_to_integer(string) %}: int
```

+++

### stringToNumber {#string-to-number}

Gebruik de functie `stringToNumber` om een tekenreeks om te zetten in een getal. Deze geeft dezelfde tekenreeks als uitvoer voor ongeldige invoer.

+++Syntaxis

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

Gebruik de functie `substr` om de subtekenreeks van de tekenreeksexpressie tussen de beginindex en de eindindex te retourneren.

+++Syntaxis

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

Gebruik de functie `titleCase` om eerste letters van elk woord van een tekenreeks met hoofdletters te maken.

+++Syntaxis

```sql
{%= titleCase(string) %}
```

**Voorbeeld**

Als de persoon in Washington high street woont, retourneert deze functie `Washington High Street` .

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

Gebruik de functie `toBool` om een argumentwaarde in een booleaanse waarde om te zetten, afhankelijk van het type.

+++Syntaxis

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

Gebruik de functie `toDateTime` om een tekenreeks om te zetten in een datum. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer.

+++Syntaxis

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

Gebruik de functie `toDateTimeOnly` om een argumentwaarde om te zetten in een waarde met alleen de datumtijd. De epochdatum wordt geretourneerd als uitvoer voor ongeldige invoer. Deze functie accepteert veldtypen tekenreeks, datum, lang en geheel getal.

+++Syntaxis

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### bijsnijden {#trim}

De functie `trim` verwijdert alle witruimten vanaf het begin en aan het einde van een tekenreeks.

+++Syntaxis

```sql
{%= trim(string) %}
```

+++

### upperCase {#upper}

De functie `upperCase` zet een tekenreeks om in hoofdletters.

+++Syntaxis

```sql
{%= upperCase(string) %}
```

**Voorbeeld**

Deze functie converteert de achternaam van het profiel naar hoofdletters.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

Gebruik de functie `urlDecode` om een URL-gecodeerde tekenreeks te decoderen.

+++Syntaxis

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

Gebruik de functie `urlEncode` om een tekenreeks als een URL te coderen.

+++Syntaxis

```sql
{%= urlEncode(string) %}: string
```

+++
