# Responsive Typography, 2018/2019

Als je doof bent, of als je om een andere reden geen geluid kunt horen, dan mis je veel informatie als je een film kijkt. Knisperende voetstappen, langzaam aanzwellende muziek, nerveus getik op een deur, je hoort het natuurlijk allemaal niet. Nu bestaat er zoiets als *closed caption*, wat een type ondertiteling is waarbij ook dingen als omgevingsgeluiden en de muziek beschreven worden. Hierdoor krijgt een kijker die informatie wel binnen.

Alleen wordt die auditieve informatie nogal neutraal beschreven. Het geluid van huilend persoon zou bijvoorbeeld beschreven kunnen worden als *snikgeluid op de achtergrond*. En iemand die lacht zou geschreven kunnen worden als *iemand lacht.* Heel neutraal, bijna zakelijk, en bovendien allebei in precies hetzelfde neutrale lettertype. Terwijl het toch echt over twee heel verschillende emoties gaat. 

Dat kan visueel sterker. 

En dat gaan jullie doen.

## Leerdoelen

- Je kan de kennis over vormgeving die je hebt geleerd tijdens de minor technisch toepassen met behulp van CSS
- Je kan verborgen nuance uit een audiotrack overtuigend vertalen naar visuele typografische beelden
- Je kan je typografische keuzes onderbouwen.
- Je hebt de exclusive design principles gebruikt.

## Oplevering

Je levert een werkende versie op, gemaakt met HTML, CSS en JavaScript. Deze staat op Github. In een duidelijke readme documenteer en onderbouw je je ontwerpkeuzes. Je developmentgeschiedenis is terug te vinden op GitHub.

Je levert ook een *screen recording* met audio op van je fragment. Dit is een video van de definitieve versie, gemaakt van jouw browserscherm.

## Typografische restricties

Je *moet* kiezen, en je keuze moet je onderbouwen:

### Optie 1: Systeemfont

De eerste optie is dat je gebruik maakt van het zogenaamde *systeemfont* van degene die naar jouw werk kijkt. Dit font verschilt per operating system, en het verschilt soms zelfs per versie van het operating system. Het is ook aan te passen door de gebruiker zelf. In dit geval heb je beschikking over normal, **bold** en _italic_.

### Optie 2: Brenner

Je kan er ook voor kiezen om gebruik te maken van de complete Brenner familie. Dit is een zeer uitgebreid en uiterst flexibel font. [Hier kan je je verdiepen in dit font](https://www.typotheque.com/blog/brenner_an_unusual_typeface_family_with_distinct_voices). Als je kiest voor dit font dan heb je de beschikking over een *sans serif*, een *condensed*, een *serif*, een *monotype*, een *slab*, een *display* en een *script* versie. En veel van deze versies hebben varianten van *light* tot *bold*, en allemaal zowel *bold* als *italic*.

Met Brenner zijn er natuurlijk veel en veel meer mogelijkheden dan met systeemfonts. Dat kan zowel een voordeel als een nadeel zijn.

Voor een overzicht, zie [de brenner.pdf](brenner.pdf).

## Het fragment

Ik heb een fragment voorbereid. Het gaat om twee scenes uit *Blade Runner 2049*. De captions staan in de HTML, en ze verschijnen in sync met de video. [Kijk maar](closed-captions/index.html).

### De captions

De captions staan in de html, in het bestand index.html. Je kan aan elke paragraaf eventueel een of meer classes toevoegen. Bijvoorbeeld `voice1` of `voice2 soft`. Classes voeg je handmatig toe in de html.

Met JavaScript worden er een paar dingen extra gedaan: 

- er wordt aan elke paragraaf een unieke class toegevoegd (`p0`, `p1`, etc)
- Elk woord wordt in een aparte `span` gezet. Hierdoor kan je elk woord apart stylen, en eventueel ook [na elkaar laten verschijnen](https://github.com/cmda-minor-vid/web-typography-18-19/blob/master/closed-captions/css.css#L41).

### Tijdens het afspelen

Tijdens het afspeelen wordt er een class `on` op de caption gezet als hij moet verschijnen, en een class `off` als hij klaar is. *Zowel class `on` als class `off` blijft op de caption staan!*

De timimg van de captions kan je aanpassen in [closed-captions/captions.js](closed-captions/captions.js).

Er verschijnen ook classes op de body op momenten dat er geluiden worden afgespeeld, zoals `sound1` en `sound2`. Je kan geluiden toevoegen in [closed-captions/sounds.js](closed-captions/sounds.js).

*let op,* de geluiden zijn niet compleet, dit zal je zelf moeten aanvullen.

## Een eigen fragment

Je kan er ook voor kiezen om een eigen, *beter* fragment te gebruiken. Je moet dan wel heel goed onderbouwen waarom het fragment beter is voor deze specifieke opdracht. Vragen die je hierbij kunnen helpen:

- Welke informatie zit er in de audio die echt niet zichtbaar is?
- Welke rol speelt de audio in het fragment?
- Werkt de scene nog zonder geluid?

Je kan dan de nodige HTML en JavaScript genereren door gebruik te maken van [caption generator](https://cmda-minor-vid.github.io/web-typography-18-19/generator/) (in Google Chrome). 

Als je de closed captions wil bewerken dan kan je een tool zoals [Amber Script](https://www.amberscript.com/en) gebruiken. Daar kan je exporteren als `.srt`, en die kan je weer door de generator halen.