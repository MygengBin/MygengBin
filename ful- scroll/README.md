# Full Screen scroll

```css
section*10>h1{title $}
html{
	scroll-snap-type: y mandatory;
}
section{
	block-size:100vh;
	scroll-snap-align:center;
	scroll-snap-stop:always;
	display:grid;
	place-items:center;
}
```
