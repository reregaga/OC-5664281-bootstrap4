# Add Bootstrap to project
## Guides 
https://getbootstrap.com/docs/4.3/getting-started/download/

## Quick way
Easiest and quickest way is to link to the minified CSS file hosted on the [BootstrapCDN](https://www.bootstrapcdn.com/)

1. Add this line to the  `<head>`  section of your HTML file: `<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">` Make sure that **it’s added before any other CSS files** so that your styles override the default Bootstrap styles.
2. Some Bootstrap components use JavaScript, in particular, the jQuery and popper.js libraries, as well as Bootstrap’s JavaScript library. To make sure everything works as expected, you should also add the following to the bottom of your page just before the closing  `</body>`  tag:
```html
<!-- jQuery first, then Popper.js, then Bootstrap JS -->

<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>

<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
```
_Note: attribute `crossorigin="anonymous"` for `<link>` and `<script>` dont need, cuz it s default value for `crossorigin`. [Source](https://developer.mozilla.org/ru/docs/Web/HTML/Attributes/crossorigin)_

# Customization
Many themes providers exist. One of them: https://themes.getbootstrap.com/