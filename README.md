# Aspect ratio CSS

A simple SCSS script for fixed aspect ratios in HTML

## What is this?

If you ever needed boxes with fixed aspect ratios inside your web layout this little Sass snippet could help you. You just have to define a Sass list with all the aspect ratios you need, then build the Sass and you should be ready to go. 

## How to use? 

### 1. Installation and building

1. Download or fork the repository
2. Install [SASS](https://sass-lang.com)
3. Build the aspectratio.scss file inside the src folder
4. Embed the generated CSS file inside the out folder into your HTML

```bash
sass --watch --sourcemap=none  src/aspectratio.scss:out/aspectratio.css
```

### 2. Configuring the aspect ratios

To configure the needed aspect ratios you just have to open the aspectratio.scss file inside the src folder and write them into the $aspectRatios variable.

Format: list(list(integer for aspect x portion, integer for aspect y portion), (x,y), (x,y)) 

```scss
$aspectRatios: ((1,1), (2,1), (16,5), (16,9), (16,10));
```

### 3. Using the aspect ratios inside your HTML

```html
<div class="aspect-16x9">
    <div class="aspect-element"></div>
    <div class="aspect-content">
        <!-- your html content inside the aspect ratio goes into here -->
    </div>
</div>
```

The Sass script generates a aspect-[x]x[y] class for every defined aspect ratio.

