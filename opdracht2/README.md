## FAQ

[Pages](https://robinfrugte97.github.io/browser-technologies/opdracht2/FAQ/)

### HTML only

The user is still able to read the content. The anchor links still work in every browser.

![ChromeHTML](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/faqhtmlonlygc.png)

### CSS added

CSS adds general styling to group questions and answers by topic. It also makes the navigation menu fixed to the side.
smooth scroll is added to enhance the experience when clicking in the navigation menu.

![ChomeCSS](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/faqcssgc.png)

IE problem encounters:

- The smooth scroll does not work in Internet Explorer.

- The styling of the Q&A section messes up in Internet Explorer

![IEMessup](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/iemessup.png)

Fixes:

- Added `display: block;` to the element containing all the Q&A elements. This fixes the IE styling mess-up;

![IEMessupCode](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/iemessupfixcode.png)

## Carousel

[Pages](https://robinfrugte97.github.io/browser-technologies/opdracht2/Carousel/)

### HTML only

In HTML the carousel falls back to a simple column of images with an `<img>` tag.

![](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/carouselhtmlgc.png)

### CSS added

CSS makes it a carousel. The radio buttons control which image is shown. The images ease in and out. The `<img>` are hidden and the images are displayed as a background-image in CSS.

![](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/carouselcssgc.png)

Problems encountered:

- Internet explorer.

### JS added

JavaScript adds a preview of all images along the bottom of the carousel. The images replace the radio buttons in controlling which image is shown when clicked.

I check whether the browser uses `querySelectorAll`:

![CarouselCode](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/carouseljscode.png)

If the browser does not support it, the JavaScript does not continue.
In the future I would like to add an `else` to that `if` to check whether the browser uses, for example `getElementsByClassName`.

![](https://github.com/RobinFrugte97/browser-technologies/blob/master/opdracht2/screenshots/carouseljsgc.png)

Problems encountered:

- Internet explorer. It does not support `querySelectorAll`.

Fixes:

- The script does not continue if the browser does not support `querySelectorAll`.
