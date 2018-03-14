## Opdracht 1.2

### De opdracht
Ik ga progressive enhancement toepassen op mijn wafs site. Hierbij ga ik stap voor stap door 8 belangrijke features heen om te checken of mijn site "progressive enhanced" genoeg is.

### WAFS site
Mijn Web App From Scratch site gaat over Marvel superheroes. Er is een overzicht van characters met elk een detail pagina. Op een detail pagina heb je een grotere afbeelding en kun je zien in welke comic het desbetreffende character in voor komt.

### De 8 features

1. Afbeeldingen
2. Custom fonts
3. Javascript (volledig)
4. Kleur
5. Breedband internet
6. Cookies
7. Local Storage
8. Muis/Trackpad

### Afbeeldingen
De site maakt veel gebruik van afbeeldingen, zowel op de hoofdpagina als op de detailpaginas. Ik krijg alle afbeeldingen in een zelf gekozen grootte terug van de Marvel API. Elke afbeelding die een superhero afbeeldt is een JPG. Het logo is een PNG afbeelding.

Problemen:
1. De images hebben geen `alt`.


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
