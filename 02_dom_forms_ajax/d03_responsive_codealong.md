## Responsive Design Codealong

#### HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <!-- this tag is needed for responsive design!!@!212 -->
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <!-- end super important tag!@!@2121 -->
    <title>Intro to Responsive Design</title>
    <link rel='stylesheet' href='styles/main.css'>
  </head>
  <body>

    <h1>Device Check</h1>
    <div class="phone">
      We're on a phone!
    </div>
    <div class="tablet">
      We're on a tablet!
    </div>
    <div class="laptop">
      We're on a laptop!
    </div>

  </body>
</html>
```

#### Style (Sass)

```scss
// generic device widths:

$device-phone: 320px;
$device-phone-landscape: 400px;
$device-phablet: 550px;
$device-tablet: 700px;
$device-netbook: 768px;
$device-notebook: 900px;
$device-laptop: 1200px;

$body-text: black;
$body-background: aliceblue;
$radius: 15px;

.phone {
  display: none;
  background: magenta;
}
.tablet {
  display: none;
  background: orange;
}
.laptop {
  display: none;
  background: yellow;
}

// @media (min-width: 320px) {}
@media (min-width: $device-phone) {
  .phone {
    display: block;
  }
}

// @media (min-width: 700px)
// max-width also works
@media (min-width: $device-tablet) {
  .phone {
    display: none;
  }
  .tablet {
    display: block;
  }
}

@media (min-width: $device-laptop) {
  .phone {
    display: none;
  }
  .tablet {
    display: none;
  }
  .laptop {
    display: block;
  }
}
```
