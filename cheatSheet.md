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

# Site parts
- **Header section**: The top of the page is the header section that contains the branding and navigation. The content remains more or less the same whichever page you're on. The navigation section usually contains links to the main parts of the website most frequently accessed by users and visitors.
- **Footer section**: Traditionally, most web pages have a footer section that contains details about the site and links to the less commonly visited parts of a site, such as the details of the company or organization, as well as the legalese such as terms of use and copyright notices. As with the header section, the content stays the same across the site.
- **Content Section**: We'll define the content section as everything after the header and before the footer. This is where the content that varies from page to page will go.
# Containers
Most basic layout element in Bootstrap, the **container**. Wrapping your content in a div with the  `.container`  class creates a centered container that adapts to the width of the viewport and provides horizontal padding for its contents, so they don’t push up against the edges. _It also have margins._
```html
<div class="container">
    <!-- Content here -->
</div>
```
If you want the content to always take up 100% of the width of the viewport, then you can use the  `.container-fluid`  class instead.
# Grid
In addition to **containers**, the Bootstrap grid uses a series of **rows** and **columns** to layout content on the page. A row div is declared by giving it a `.row` class. For each column in the row, a div that is a direct child of the row div must be given one of the Bootstrap 4 column classes. The first of these column classes is the `.col` class. 
```html
<div class="container">
    <div class="row">
        <div class="col">
            First column
        </div>
        <div class="col">
            Second column
        </div>
    </div>
</div>
```
**Bootstrap has a 12-column grid**, so in this case Bootstrap will automatically assign half of the columns to each of the  `.col`  divs, making each of them 6-columns wide—in other words, half the width of the row. So the general rule is that Bootstrap will divide up the 12 columns equally among the divs that are given the  `.col`  class.

For specify the number of columns explicitly rather than leave it up to Bootstrap, need appending each of those numbers to the respective `.col` class.
```html
<div class="container">
    <div class="row">
        <div class="col-8">
            First column
        </div>
        <div class="col-4">
            Second column
        </div>
    </div>
</div>
```