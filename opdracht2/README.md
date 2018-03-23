## FAQ

### HTML only

The user is still able to read the content. The anchor links still work in every browser.

![ChromeHTML]()

### CSS added

CSS adds general styling to group questions and answers by topic. It also makes the navigation menu fixed to the side.
smooth scroll is added to enhance the experience when clicking in the navigation menu.

![ChomeCSS]()

IE problem encounters:

- The smooth scroll does not work in Internet Explorer.

- The styling of the Q&A section messes up in Internet Explorer

![IEMessup]()

Fixes:

- Added `display: block;` to the element containing all the Q&A elements. This fixes the IE styling mess-up;

![IEMessupCode]()

## Carousel

### HTML only

In HTML the carousel falls back to a simple column of images with an `<img>` tag.

![]()

### CSS added

CSS makes it a carousel. The radio buttons control which image is shown. The images ease in and out. The `<img>` are hidden and the images are displayed as a background-image in CSS.

![]()

Problems encountered:

- Internet explorer.

### JS added

JavaScript adds a preview of all images along the bottom of the carousel. The images replace the radio buttons in controlling which image is shown when clicked.

I check whether the browser uses `querySelectorAll`:

![CarouselCode]()

If the browser does not support it, the JavaScript does not continue.
In the future I would like to add an `else` to that `if` to check whether the browser uses, for example `getElementsByClassName`.

![]()

Problems encountered:

- Internet explorer. It does not support `querySelectorAll`.

Fixes:

- The script does not continue if the browser does not support `querySelectorAll`.
