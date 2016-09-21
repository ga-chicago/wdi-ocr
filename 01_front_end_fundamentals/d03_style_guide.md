## Style Guide & Fonts

#### Rule of Thumb for Style Guides

Note that every style guide is unique. This is just a good starting point.

  * Headline Text: 300%
	* B-Head (sub) text: 150%
	* Nav Item: 100%
	* Body copy (text): 100% - starting point could be `body { font-size: 16px }`
  * Byline: 75%

#### Example

* `1rem` = 100%
* `rem` is responsive and related to the `root` of the page.

```css

h1 {
  font-size: 3rem; /* 300% */
}
p {
  font-size: 1rem; /* 100% */

}
nav {
  font-size: 1.25rem; /* 125% */
}
h2 {
  font-size: 1.50rem; /* 150% */
}
h3 {
  font-size: 0.75rem; /* 75% */
}
body {
  font-size: 16px;
}
```
