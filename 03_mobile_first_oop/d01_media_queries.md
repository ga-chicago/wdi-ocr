## Introduction to Media Queries

#### Sass (SCSS)
```scss
// variables
// device widths (these are generalised)
$device-phone: 480px; // portrait 320px
$device-phablet: 540px; // landscape: 610px
$device-tablet: 700px; // 768px;
$device-laptop: 960px; // 900+
$device-large: 1200px; // 1200px+

body {
	font-size: 16px;
}

.device-phone {
	font-size: 1rem;
	border: 1px solid purple;
	display: none;
	visibility: hidden;
}
.device-phablet {
	font-size: 1rem;
	border: 1px dashed blue;
	display: none;
	visibility: hidden;
}
.device-tablet {
	font-size: 1rem;
	border: 1px solid orange;
	display: none;
	visibility: hidden;
}
.device-laptop {
	font-size: 1rem;
	border: 1px dashed red;
	display: none;
	visibility: hidden;
}
.device-large {
	font-size: 1rem;
	border: 1px solid magenta;
	display: none;
	visibility: hidden;
}

.container {

}

// media queries :)
// let's get responsive
// let's get dangerous
@media (max-width: $device-phone) {
	// do stuff to our styles
	.device-phone {
		display: block;
		visibility: visible;
	}
}
@media (min-width: $device-phone) {
	.device-phone {
		display: none;
		visibility: hidden;
	}
	.device-phablet {
		display: block;
		visibility: visible;
	}
}
// all media queries above target phones
@media (min-width: $device-tablet) {
	.device-phablet {
		display: none;
		visibility: hidden;
	}
	.device-tablet {
		display: block;
		visibility: visible;
	}
}
// all media queries above target phablets
@media (min-width: $device-laptop) {
	.device-tablet {
		display: none;
		visibility: hidden;
	}
	.device-laptop {
		display: block;
		visibility: visible;
	}
}
@media (min-width: $device-large) {
	.device-laptop {
		display: none;
		visibility: hidden;
	}
	.device-large {
		display: block;
		visibility: visible;
	}
}
```

#### HTML

```html
<!DOCTYPE html>
<html>
<head>
	<title>Mobile-First</title>
	<meta name="viewport" content="width=device-width,initial-scale=1">
	<link rel="stylesheet" href="styles/main.css">
	<script type="text/javascript" src="scripts/app.js"></script>
</head>
<body>
	<header>
		<h1>Mobile-First</h1>
		<hr> <!-- a silly line -->
	</header>

	<section class='container'>
		<article class='device-phone'>
			<p>I am on a mobile phone!</p>
		</article>
		<article class='device-phablet'>
			<p>I am on a phablet.</p>
		</article>
		<article class='device-tablet'>
			<p>I am on a tablet.</p>
		</article>
		<article class='device-laptop'>
			<p>I am on a laptop.</p>
		</article>
		<article class='device-large'>
			<p>I am on a large screen.</p>
		</article>
	</section>
</body>
</html>
```
