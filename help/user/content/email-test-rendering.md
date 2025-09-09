---
title: E-mailrendering testen
description: Test de rendering van e-mailberichten op verschillende desktopcomputers, mobiele clients en webclients met Litmus-integratie om ervoor te zorgen dat de inbox-compatibiliteit in Journey Optimizer B2B edition wordt gegarandeerd.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# E-mailrendering testen met Litmus

Om uw e-mails te testen, kunt u hefboomwerking a [ de rekening van de Onderneming van de 1} litmus van Journey Optimizer B2B edition. ](https://www.litmus.com/email-testing){target="_blank"} Met deze integratie kunt u een voorvertoning van uw e-mailrendering weergeven in populaire e-mailclients. Met dit gereedschap kunt u ervoor zorgen dat uw e-mailinhoud er goed uitziet en werkt zoals deze in elke Postvak IN is ontworpen.

>[!AVAILABILITY]
>
>Deze integratie is alleen beschikbaar voor Journey Optimizer B2B edition-gebruikers met Litmus Enterprise-accounts. Voor meer informatie, verwijs naar de [ oplossingspagina op de website van het Malplaatje ](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}.

1. Wanneer uw e-mailontwerp gereed is en klaar is om te worden getest, klikt u op **[!UICONTROL Simulate content]** in de ontwerpruimte voor e-mail.

1. Klik op **[!UICONTROL Render email]** rechtsboven.

   ![ teruggeeft e-mailknoop ](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Als u nog geen verbinding hebt gemaakt met uw Litmus-account vanuit Journey Optimizer B2B edition, biedt de weergegeven pagina een optie voor het starten van een proefaccount of het maken van verbinding met uw bestaande account.

1. Klik op **[!UICONTROL Connect your Litmus account]** rechtsboven of gebruik de koppeling in de pagina.

   ![ verbind uw rekening van de Samenhang ](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Voer uw aanmeldingsgegevens voor uw account in en klik op **[!UICONTROL Sign in]** .

1. Klik op **[!UICONTROL Connect]** om de verbinding tussen Litmus en Journey Optimizer B2B edition te bevestigen en de e-mailinhoud voor rendering te verzenden.

   >[!IMPORTANT]
   >
   >Wanneer u uw account Litmus verbindt met Journey Optimizer B2B edition, gaat u ermee akkoord dat testberichten naar Litmus worden verzonden. Deze inhoud wordt dan beheerd binnen Litmus en niet binnen Adobe. Dientengevolge, is het beleid van de Gegevens van de Litmus e-mail van toepassing op deze e-mail, met inbegrip van verpersoonlijkingsgegevens die in de testberichten kunnen worden omvat.

1. Klik op **[!UICONTROL Run test]** rechtsboven om e-mailvoorvertoningen te genereren.

   ![ stel een Lijn in werking teruggevend test ](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. Controleer uw e-mailinhoud in populaire desktops, mobiele en webclients.

   Klik op de weergegeven miniatuur om de details voor een van de gerenderde clienttests weer te geven.

   ![ de e-mailvoorproeven van de Samenhang ](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. Wanneer u klaar bent met het herzien, klik de achterpijl ( ![ toon of verberg filterpictogram ](../../assets/do-not-localize/icon_back-arrow.svg)) bij top-left om op de Simulate inhoudspagina terug te komen.

   U kunt een ander profiel selecteren en een andere renderingstest uitvoeren, of terugkeren naar de ontwerpruimte van de e-mail om de benodigde aanpassingen aan te brengen op basis van uw revisie.
