---
title: Personalization-syntaxis
description: Leer op Handlebars-gebaseerde verpersoonlijkingssyntaxis in Journey Optimizer B2B edition, met inbegrip van uitdrukkingen, helpers, letterlijke types, en het formatteren regels.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: expressie, editor, syntaxis, personalisatie
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Personalization-syntaxis {#personalization-syntax}

De uitdrukkingen in de [!DNL Journey Optimizer B2B Edition] [&#x200B; verpersoonlijkingsredacteur &#x200B;](./personalization.md#personalization-editor) zijn gebaseerd op de _4&rbrace; het malplaatjesyntaxis van Handelaren &lbrace;._ Er worden een sjabloon en een invoerobject gebruikt om HTML of andere tekstopmaak te genereren. Handlebars de malplaatjes kijken als regelmatige teksten met ingebedde uitdrukkingen Handlebars.

Voor meer details over Handlebars en hoe het werkt, verwijs naar de [&#x200B; documentatie HandlebarsJS &#x200B;](https://handlebarsjs.com/){target="_blank"}.

## Algemene bepalingen

Voorbeeld van eenvoudige expressie:

```
{{account.accountName}}
```

Waarbij:

* `account` is een naamruimte.
* `accountName` is een token dat wordt samengesteld door kenmerken.

  >[!NOTE]
  >
  >De attributenstructuur wordt bepaald in een [&#x200B; Adobe Experience Platform XDM Schema &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/home){target="_blank"}.

* Id&#39;s kunnen elk Unicode-teken zijn, behalve de volgende:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* De syntaxis is hoofdlettergevoelig.

* De woorden **waar**, **vals**, **ongeldig** en **niet gedefiniëerd** worden slechts toegestaan in het eerste deel van een weguitdrukking.

* In Handlebars, zijn de waarden die door {\ {expression} \} zijn teruggekeerd _HTML-ontsnapte_. Als de expressie `&` bevat, wordt de geretourneerde uitvoer met escape-teken van HTML gegenereerd als `&amp;` . Als u geen waarde wilt laten ontsnappen aan Handgrepen, gebruikt u de +-driestash_.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

* Voor argumenten voor letterlijke functies ondersteunt de sjabloontaalparser geen enkel unescaped backslash-symbool (`\`). Aan dit teken moet een extra backslash (`\`) worden toegevoegd. Bijvoorbeeld:

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## Helpers {#helpers-all}

Een hulpfunctie Handlebars is een eenvoudig herkenningsteken dat met parameters kan worden toegevoegd. Elke parameter is een expressie Handlebars. Deze helpers kunnen van om het even welke context in een e-mailmalplaatje worden betreden.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

Voor meer gedetailleerde informatie over deze functies, zie [&#x200B; de functies van de Helper &#x200B;](./personalization-helper-functions.md).

## Letterlijke typen {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition] ondersteunt de volgende letterlijke typen:

| Letterlijk | Definitie |
| ------- | ---------- |
| String | Een gegevenstype dat bestaat uit tekens die worden omringd door dubbele aanhalingstekens. <br> Voorbeelden: `"prospect"` , `"jobs"` , `"articles"` |
| Boolean | Een gegevenstype dat waar of onwaar is. |
| Geheel | Een gegevenstype dat een geheel getal vertegenwoordigt. Het kan positief, negatief, of nul zijn. <br> Voorbeelden: `-201` , `0` , `412` |
| Array | Een gegevenstype dat is samengesteld als een groep andere letterlijke waarden. Er worden vierkante haakjes gebruikt om te groeperen en komma&#39;s om te scheiden tussen verschillende waarden. <br> **Nota:** u kunt niet tot de eigenschappen van punten binnen een serie direct toegang hebben. <br> Voorbeelden: `[1, 4, 7]` , `["US", "FR"]` |

>[!CAUTION]
>
>Het gebruik van **xEvent** variabele is niet beschikbaar in verpersoonlijkingsuitdrukkingen. Een verwijzing naar xEvent resulteert in validatiefouten.
