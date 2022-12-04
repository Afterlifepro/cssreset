# Afterlifepro's CSS reset!
## Files
#### There are 3 files in this repo
1. `README.md`  
    This is the readme - Ignore this
2. `cssresettest.html`   
    This is the test file - check it out HERE
3. `cssreset.css`  
    This is the css - copy-paste it into your code, but please keep atribution  

## Code
```css
/* CSS RESET - CREDIT TO https://github.com/afterlifepro/ */
/* reset the html and body to full height and enable dark mode */
html, body { width: 100%; height: 100%; color-scheme: light dark; }
/* remove all margin and padding */
* { margin: 0; padding: 0; }
/* reapply margin and padding to ul and ol in an article */
article :where(ul, ol) { margin-block: 1em; padding-inline-start: 40px; }
/* remove list decoration from uls and ols not in an article */
:where(ul, ol):not(article :where(ol, ul)) { list-style: none; }
/* make images 100% width so they are responsive */
img { width: 100%; }
/* ensure a tags are underlined */
a { text-decoration: underline; }
```
We start by ensuring the html and body tags are full size and making sure dark mode works.
```css
html, body { 
    width: 100%; 
    height: 100%; 
    color-scheme: light dark; 
}
```
Next, margins and padding is removed over **ALL** elements.
```css
* { 
    margin: 0; 
    padding: 0; 
}
```
Now we need to reapply default margin/padding this to all `ul` and `ol` in an `article` - no matter how nested they are.
```css
article :where(ul, ol) { 
    margin-block: 1em; 
    padding-inline-start: 40px; 
}
```
We should remove the list decoration from `ul` and `ol` that aren't in an article.
```css
:where(ul, ol):not(article :where(ol, ul)) { 
    list-style: none; 
}
```
Having images width determined by the image file and not the parents size makes them unresponsive, so let's fix that!
```css
img {
    width: 100%
}
```
Now theres one more fix I want to make - `a` tags only have an underline when they have an href.
```css
a {
    text-decoration: underline;
}
```
### Is this the end of the reset?? For now, yes. But I'll keep adding to this as I do more css, so why not star and watch the repo?