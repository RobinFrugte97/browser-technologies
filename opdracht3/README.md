## Contactenlijst

Voor deze opdracht heb ik een contactenlijst gemaakt. De gebruiker kan door de contactenlijst navigeren met de rechts aan de rand van de website. Verder kan de gebruiker contacten zoeken in de zoekbalk.

![](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht3/screenshots/browsertech.png)

## Schetsen

Ik had een contactenlijst in gedachten, daarvoor heb ik schetsen gemaakt hoe ik het ongeveer wil hebben qua design en qua html opzet per deel.

![](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht3/screenshots/thumbnail_20180329_133655.jpg)

## Zonder..

- Zonder JavaScript kan de gebruiker nogsteeds door de contactenlijst navigeren door te scrollen of door de navigatie aan de rand van de pagina te gebruiker.
- Zonder CSS kan de gebruiker volgens de links in de navigatie nogsteeds door de lijst navigeren.

## Features

### Kleuren

Ik maak amper gebruik van kleur. Alleen de standaard afbeeldingen bevatten kleur.

### Muis/Trackpad

De site is te gebruiken met keyboard. De details hebben een hover en een focus-state. Je kunt de site navigeren met je toetsenbord door in de navigatie-lijst rechts van de site te tabben.

### JavaScript

Met JavaScript kun je door je contacten zoeken. Ik heb zoveel mogelijk vermeden om met JavaScript een `display:` mee te geven. In plaats daarvan heb ik zoveel mogelijk geprobeerd om `hidden` te togglen. Zo werkt de JavaScript nog als de css weg valt.

Ik heb een feature detect op `indexOf`, omdat dit niet goed werkt in oudere Internet Explorer versies. De fallback is hier de navigatie aan de rand van de pagina.

### Overig

- Smooth scroll `scoll-behaviour: smooth`
- Sticky headers `position: sticky;`
De zoekbalk heeft `position: sticky;`. Als sticky niet ondersteunt wordt is `position: fixed;` de fallback.

## Devicelab

![](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht3/screenshots/thumbnail_20180328_143832.jpg)


Op sommige devices werken de sticky headers niet naar wens.
