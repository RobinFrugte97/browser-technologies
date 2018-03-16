## Opdracht 1.2

### De opdracht
Ik ga progressive enhancement toepassen op mijn wafs site. Hierbij ga ik stap voor stap door 9 belangrijke features heen om te checken of mijn site "progressive enhanced" genoeg is.

### WAFS site
Mijn Web App From Scratch site gaat over Marvel superheroes. Er is een overzicht van characters met elk een detail pagina. Op een detail pagina heb je een grotere afbeelding en kun je zien in welke comic het desbetreffende character in voor komt.

### 9 features

1. Afbeeldingen
2. Custom fonts
3. Javascript (volledig)
4. Kleur
5. Screenreader
6. Breedband internet
7. Cookies
8. Local Storage
9. Muis/Trackpad


### Afbeeldingen
De site maakt veel gebruik van afbeeldingen, zowel op de hoofdpagina als op de detailpaginas. Ik krijg alle afbeeldingen in een zelf gekozen grootte terug van de Marvel API. Elke afbeelding die een superhero afbeeldt is een JPG. Het logo is een PNG afbeelding.

Problemen:
1. De images hebben geen `alt`. Als de afbeeldingen om wat voor reden dan ook niet laden, dan weet je niet waar het om gaat.
2. De site bestaat grotendeels uit afbeeldingen. Voor blinden of slechtzienden is de site dus praktisch onbruikbaar.

Oplossingen:
1. Per image wordt nu naast een `<img>` src ook een `<img>` alt gerendert.
  Code voor:
  ```
  thumbnail: {
    src: function(){
      return this.thumbnail;
    }
  }
  ```
  Code na:
  ```
  thumbnail: {
    src: function(){
      return this.thumbnail;
    },
    alt: function(){
      return "Thumbnail afbeelding van ${this.character}
    }
  }
  ```
2. Per image wordt nu ook een `<img>` title gerendert, met daarin de naam van de desbetreffende superhero.  


### Custom fonts
Ik maak gebruik van een custom font op de website. De kans bestaat dat om wat voor reden dan ook de font niet geladen kan worden.

Problemen:
1. Er is geen fallback font.

Oplossingen:
1. Helvetica toegevoegd als fallback font. Als fallback daarop een sans-serif font.
`font-family: americanCaptain, helvetica, sans-serif;`


### JavaScript
De website werkt niet zonder JavaScript. Zonder JavaScript zul je niet verder komen dan de loading spinner.

Problemen:
1. De website werkt niet zonder JavaScript. De data wordt niet opgehaald en er wordt geen pagina gerendert.

Oplossingen:
1. De site zou aan de server kant gerendert kunnen worden.


### Kleur
De site heeft een aantal verschillende kleuren, dankzij de vele verschillende afbeeldingen en kleurrijke characters.

De site is goed te gebruiken in zwart-wit.

![Zwart-wit](/screenshots/blackandwhite2.png)

In de toekomst wil ik testen of de site te gebruiken is voor kleurenblinden. Om dit te checken met bijvoorbeeld een browser extentie, moet ik de site online zetten. De Marvel API werkt dat op het moment een beetje tegen.


### Screenreader
Ik heb de site getest met een screenreader. De gebruikte screenreader heet [NVDA](https://www.nvaccess.org/). De reader leest per character de afbeeldingen en de naam van het character.

![reader](/screenshots/screenreader.png)

### Breedband internet
De site is bijna geheel gebaseerd rond de Marvel API.
De API call die naar alle characters wordt gemaakt duurt op langzaam 3G netwerk minimaal 10 seconden. Vervolgens moeten alle afbeeldingen geladen worden. Per afbeelding duurt het 2 tot 5 seconden voor het geladen is.

Problemen:
1. Op een langzaam 3G netwerk duurt het erg lang om de site te laden. Dit komt mede door de vele afbeeldingen die geladen moeten worden.
2. Er wordt een groot aantal afbeeldingen binnen gehaald. Dit kan problemen veroorzaken bij iemand met een trage internet snelheid, zoals een langzame 3G verbinding op hun telefoon.

Oplossingen:
1. De Marvel API biedt verschillende afbeelding formaten. Je zou binnen JavaScript kunnen checken of de afbeeldingen er te lang over doen en vervolgens doorgaan met een kleiner formaat afbeeldingen.
2. De API call naar Marvel is eenvoudig te limiten. Zo is het aantal characters dat opgehaald wordt beperkt.

### Cookies
Ik maak op het moment geen gebruik van cookies in de website.


### Local Storage
Ik maak geen gebruik van local storage in de website.

Problemen:
1. Omdat er geen gebruik wordt gemaakt van local storage, moet de gebruiker elke keer de afbeeldingen en andere content opnieuw downloaden. Dit kan met een trage verbinding problemen opleveren.

Oplossingen:
1. De images zouden in de local storage opgeslagen kunnen worden voor mensen die vaker op de site terug komen, in het geval dat de gebruiker langzaam internet heeft.


### Muis / Trackpad
Ik had geen aandacht besteed aan hoe de site te bedienen is zonder muis.

Problemen:
1. Geen focus-states om door de website te navigeren met een toetsenbord.

Oplossingen:
1. Duidelijke focus-states toegevoegd aan alle elementen in de site die een functionaliteit hebben.
