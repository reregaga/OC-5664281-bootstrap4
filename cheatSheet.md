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
**If you create more than 12 col elements**, row will be breaks, it will look like cols after 12 will be moved to next line.
# Responsive
One of the reasons Bootstrap is so popular with front-end developers. It takes a **mobile-first approach**, meaning that its grid and components are designed to render correctly on small screens by default. 

Good news is that you don't have to create a different layout for every screen size. You can make your work easier, while still creating great user experiences, by grouping all the screen sizes into different buckets, or size ranges, and generating layouts for each range. A typical example is to have one layout that's shown on devices with large screens (desktop computers); another for devices with medium-sized screens (tablets and small laptops); and a third for smaller devices (smartphones).

| Size | Breakpoint | Class modifier |
|-|-|-|
| Extra small | <576px | none |
| Small | ≥576px | `-sm` |
| Medium | ≥768px | `-md` |
| Large | ≥992px | `-lg` |
| Extra large | ≥1200px | `-xl`|

In the context of front-end design and development, a **breakpoint** is the point at which the layout changes. It is usually expressed as a number representing the number of pixels that represent the width of the viewport at which the breakpoint occurs.

To apply the appropriate Bootstrap class modifiers for these layout options, it’s important to understand that they work **upwards**. For example, a class with the modifier `-md` will apply to all medium-size screens and bigger (in other words, viewports with a width ≥768px), unless there are class modifiers applied to an element for large (`-lg`) or extra-large (`-xl`). You can see that the **extra-small** size doesn’t need a class modifier. Since Bootstrap is **mobile-first, if you don't add a size-related class modifier**, they will automatically render the relevant grid elements and components to the smallest screens and will maintain the same layout as they grow.

```html
<div class="container">
    ...
    <div class="row">
        <div class="col-6 col-md-4 col-lg-3">
            One of two columns
        </div>
        <div class="col-6 col-md-8 col-lg-9">
            One of two columns
        </div>
    </div>
</div>
```
Here is a row with two child divs which take up different widths depending on the viewport size. Remembering that the class modifiers work upwards, the way to interpret the classes for the first of the row's child divs is:
- `.col-6`  class means: for all screens with extra-small size (basically all screen sizes) upwards, allocate six columns to this div.
- `.col-md-4`  class means: for all screens with a medium width (768px) upwards, allocate four columns to this div.