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

# UI Components
## Navigation bar
Bootstrap has a powerful, responsive navigation bar component. It’s implemented using a  `nav`  element with a `.navbar` class. Navbars also require a  `.navbar-expand{-sm|-md|-lg|-xl}`  class for responsive collapsing. The  .navbar-expand  class affects the viewport width at which the navbar expands/collapses. For most websites, branding is displayed alongside the main navigation, so Bootstrap has a  `.navbar-brand`  class for it inside the navbar component. Add the site name in the branding element like below: 
```html
<nav class="navbar navbar-expand">
    <a class="navbar-brand" href="...">Space School</a>
</nav>
```
The navigation elements should be placed in an unordered list with the  `<ul>`,  `<li>`, and  `<a>`  elements given the classes shown in this snippet:
```html
<nav class="navbar navbar-expand">
    <a class="navbar-brand" href="index.html">Space School</a>
    <ul class="navbar-nav">
        <li class="nav-item active">
            <a class="nav-link" href="index.html">Home</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="#">Lessons</a>
        </li>
    </ul>
</nav>
```
`.active` class is used to highlight one of the navigation items as the “active” or currently selected item.

To **change the colors of the background and text** in the navbar, you can add some CSS styles. [Presets.](https://getbootstrap.com/docs/4.3/utilities/colors/#background-color) We’ll use the `.bg-dark`  utility class to change its color: `<nav class="navbar navbar-expand bg-dark">...</nav>`.
Another handy set of Bootstrap color utilities are the  `.navbar-light`  and  `.navbar-dark`  classes. These classes adjust the color of any elements in the navbar, such as the brand and navigation links, to contrast with the chosen background. So you would add the  `.navbar-light`  class to a light-colored navbar. Alternatively, as in the case of our site, you would add the  `.navbar-dark`  class to a dark-colored navbar. `<nav class="navbar navbar-expand bg-dark navbar-dark">...</nav>`. Also you want the `<nav>` element of the header section to maintain the same width and padding as the rest of the page’s content and the background to expand to the full width. For this using two separate `.container` divs: one to wrap the `<nav>` element, and another to wrap the rest of the page's content outside of the header section.
```html
<!-- Header Section -->
<div class="bg-dark"> <!-- 100% width -->
    <div class="container"> <!-- width with margins -->
        <div class="row">
            <nav class="col navbar navbar-expand navbar-dark">
                ...navbar content...
            </nav>
        </div>
    </div>
</div>
<!-- Rest of page -->
<div class="container"> <!-- width with margins -->
    ...page content...
</div>
```
**Note how the `.col` class was added to the `<nav>` element** to make sure it takes up the whole width of its enclosing `.row` div.

**Implementing the responsive navigation** is to use the size-related class modifier on the  `.navbar-expand`  class of the  `<nav>`  element. 
```html
<nav class="col navbar navbar-expand-lg navbar-dark">
    ...navbar content...
</nav>
```
Next, **you need to add the toggle navigation button**. For a Bootstrap responsive navigation, add a button just after the branding, with the following attributes and content:
```html
<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContent">
    <span class="navbar-toggler-icon"></span>
</button>
```
The final step is to add the  `.collapse`  and  `.navbar-collapse`  classes to the  `<div>`  that wraps the unordered list containing the navigation links, as well as an `id` attribute with a value that matches that of the `data-target` attribute of the navbar toggle button—in this case  `navbarContent`.
```html
<div id="navbarContent" class="collapse navbar-collapse">
    <ul class="navbar-nav">
        ...nav items...
    </ul>
</div>
```
The  `.*collapse`  classes and `id` of the  `<div>`, the corresponding  `data-*`  attributes of the toggle button. Final version:
```html
<nav class="col navbar navbar-expand navbar-dark">
    <a class="navbar-brand" href="index.html">Space School</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContent">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div id="navbarContent" class="collapse navbar-collapse">
        <ul class="navbar-nav">
            <li class="nav-item active">
                <a class="nav-link" href="index.html">Home</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" href="#">Courses</a>
            </li>
        </ul>
    </div>
</nav>
```

## Jumbotron
To create a jumbotron, you simply add the `.jumbotron` class to a div: `<div class="jumbotron"><h1>Welcome!</h1></div>`.
## Cards
The card component is a flexible container that has options for a header, footer, and content. The basic setup for a card component is to assign a `.card` class to a  `<div>`  and add a child  `<div>`  with a `.card-body` class:
```html
<div class="card">
    <div class="card-body">
        This is the content of the card body
    </div>
</div>
```
The  `.card-body`  div can contain many types of card elements, but for now use these:
- `.card-title` is added to a `<h*>` tag to style the title of the card.
- `.card-text` is added to a  `<p>`  tag to style text such as lead-ins or descriptions.
```html
<div class="card">
    <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">Some text to build on the card title and make up the card's content.</p>
    </div>
</div>
```
## Text
### Headings
Bootstrap 4 has styling for all HTML headings from  `<h1>`  through to  `<h6>`. To apply the heading style, all you need to do is use the relevant  `<h*>`  tag. You also have the option of adding a  `.h1`  to  `.h6`  class to other tags like a  `<p>`  tag, if you can’t use the `<h*>` elements.

### Lists
Bootstrap 4 also applies styles to the HTML  `<ul>`  and  `<ol>`  list tags, so you get nicely-styled lists out of the box.  You can also remove the styling from a list by adding the  `.list-unstyled`  class. Another option is to create an inline list by adding a `.list-inline` class to the  `<ul>`  tag and  `.list-inline-item`  class to its  `<li>`  children.
### Formatting
Change the alignment of text within an element by adding one of the text alignment classes:
|Class|Description|
|-|-| 
|`.text-left`| Left align text in an element|
|`.text-center`| Center align text in an element|
|`.text-right`|Right align text in an element|

Text alignment in Bootstrap also has responsive classes:
|Class|Description|
|-|-|
|`.text-sm-left`|Left align text on all small (sm) viewports or larger|
|`.text-md-center`|Center align text on all medium (md) viewports or larger|
|`.text-lg-right`|Right align text on all large (lg) viewports or larger|
|`.text-xl-center`|Center align text on all extra-large (`xl`) viewports|

There’s no need to use the extra-small (`xs`) class modifier. To achieve responsive alignment that changes with the viewport size, you can combine alignment classes in an element. `<p class=”text-center text-lg-left”>[The alignment of this text would change depending on the viewport size]</p>`

### Font Weight
With Bootstrap, you can change the formatting of any text element by adding the relevant  `.font-weight-*`  class. 
|Class|Effect|
|-|-|
|`font-weight-bold`|Bold text|
|`font-weight-bolder`|Bolder weight text (relative to the parent element|
|`font-weight-normal`|Normal weight text|
|`font-weight-light`|Light weight text|
|`font-weight-lighter`|Lighter weight text (relative to the parent element)|

You can also change an element's text format to italic by adding the `.font-italic` class.

### Images
You can add an  `<img>`  element with a  `.card-img-top`  class.
### Videos
```html
<div class="embed-responsive">
    <iframe class="embed-responsive-item" src="..." allowfullscreen></iframe>
</div>
```
|Modifier Class|Aspect Ratio|
|-|-|
|`.embed-responsive-21by9`|21:9|
|`.embed-responsive-16by9`|16:9|
|`.embed-responsive-4by3`|4:3|
|`.embed-responsive-1by1`|1:1 (square)|
```html
<div class="embed-responsive embed-responsive-16by9">
    <iframe class="embed-responsive-item" src="..."></iframe>
</div>
```

### Buttons
To render a button in Bootstrap, use either a  `<button>`  or an  `<a>`  element with a `.btn`  class as well as a second class to control the background color: `.btn-primary`, `.btn-danger`, etc.
```html
<button type="button" class="btn btn-primary">Primary</button>
```

### Carousel
The basic Bootstrap 4 carousel can be set up with the following HTML structure:
```html
<div class="carousel slide" data-ride="carousel">
    <div class="carousel-inner">
        <div class="carousel-item active">
            <img src="..." class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
            <img src="..." class="d-block w-100" alt="...">
        </div>
    </div>
</div>
```
Let’s take a look at some of the details of the carousel’s structure:
- **One of the carousel items has to have the `.active` class; otherwise, the carousel will not be visible**. This is usually the first item.
- The class  `.d-block`  gives the element a display value of block. There are other `d-*` classes in Bootstrap for other display values. You can find all the available options in [Bootstrap’s Display property](https://getbootstrap.com/docs/4.3/utilities/display/) documentation.
- The  `.w-100`  class is a sizing class that controls the width of an element. The available classes are  `w-100`,  `w-75`,  `w-50`,  `w-25`, and  `w-auto`,  which respectively give an element width values of 100%, 75%, 50%, 25%, and auto relative to its parent.
- To make sure that you prevent default browser image alignment in the carousel, add the classes  `.d-block`  and  `.w-100`  to its  `<img>`  elements.

Let’s give our users a bit more control by adding **previous and next controls**.
```html
<div id="carouselControls" class="carousel slide" data-ride="carousel">
    <div class="carousel-inner">
        [... carrousel items ...]
    </div>
    <a class="carousel-control-prev" href="#carouselControls" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carouselControls" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a>
</div>
```

### Alerts
A simple alert can be implemented in Bootstrap by adding the  `.alert`  class to a  `<div>`  and adding a  `role=”alert”`  attribute to it. To control the background color of the alert, you need to also add a class of  `.alert-{value}`  to the  `<div>`, where  `{value}`  is any one of `primary, secondary, success,  danger, warning, info, light, dark`. The default colors of each of these values are the same as those for the  `.bg-*`  and  `.button-*`  classes you’ve seen earlier in this course. So to create a simple  “success”  alert (default color is green), you add this  `<div>`  to your page:
```html
<div class="alert alert-success" role="alert">
    You’ve successfully done the thing you did!
</div>
```
Option to dismiss an alert after they’ve seen it. To to this, you need to add the classes  `.alert-dismissible`,  `.fade`, and  `.show`  to the alert  `<div>`  and add a  “close”  button to allow for the dismissal.
```html
<div class="alert alert-success alert-dismissible fade show" role="alert">
    You’ve successfully done the thing you did!
    <button type="button" class="close" data-dismiss="alert" aria-label="Close">
        <span aria-hidden="true">×</span>
    </button>
</div>
```
