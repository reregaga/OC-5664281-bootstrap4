[Quiz](https://openclassrooms.com/en/courses/5664281-create-responsive-websites-efficiently-with-bootstrap-4/exercises/3606)
# Check Your Understanding of Bootstrap UI Components

## Question 1
**If you want the Bootstrap navbar to collapse for small and extra-small screens, and expand for all other screens, which of these classes would you have to add to the  <nav>  element?**
- [ ] navbar-expand
- [ ] navbar-expand-sm
- [x] navbar-expand-md
- [ ] navbar-expand-lg

_Bootstrap modifier classes work upwards. So adding the  .navbar-expand-md  class will cause the navbar to expand on medium screens upwards to large and extra-large screens (i.e., all screens that are larger than the medium breakpoint), and not to screens that are smaller than the medium breakpoint._

## Question 2
**The  .navbar-light  and  .navbar-dark  classes:**
- [ ] Adjusts the color of the background of the navbar component.
- [x] Adjusts the color of elements in the navbar component.
- [ ] Adjusts the color of the background and the element of the navbar component.

_The  .navbar-light  and  .navbar-dark  classes will adjust the color of any elements in the navbar, such as the brand and navigation links, to contrast well with the chosen background. The classes that can adjust the background of the component are the  bg-*  classes._

## Question 3
**Which of the following will create a responsive navbar that is expanded on viewports with the size of the large breakpoint or wider and collapsed in all other viewport widths?**
- [x] <nav class="navbar navbar-expand-lg">
    <a class="navbar-brand" href="#">Site Name</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContent">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div id="navbarContent" class="collapse navbar-collapse">
        ... nav items ...
    </div>
</nav>
- [ ] <nav class="navbar navbar-expand">
    <a class="navbar-brand" href="#">Site Name</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContent">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div id="navbarContent" class="collapse navbar-collapse">
        ... nav items ...
    </div>
</nav>
- [ ] <nav class="navbar navbar-expand-lg">
    <a class="navbar-brand" href="#">Site Name</a>
    <button class="navbar-toggler" type="button" data-toggle="collapse">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse">
        ... nav items ...
    </div>
</nav>
- [ ] <nav class="navbar navbar-expand-lg">
    <a class="navbar-brand" href="#">Site Name</a>
    <button class="navbar-toggler" type="button" data-target="#navbarContent">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div id="navbarContent">
        ... nav items ...
    </div>
</nav>

_To create a responsive navbar in Bootstrap, all of the following must be included:_

## Question 4
**Which of the following would cause the alignment of a paragraph to be responsive so that it is center-aligned on medium viewports and right-aligned on all other viewport sizes?**
- [ ] <p class="text-xs-right text-md-center text-lg-right"> ...text... </p>
- [x] <p class="text-right text-md-center text-lg-right"> ...text... </p>
- [ ] <p class="text-right text-md-center"> ...text... </p>

_Bootstrap’s mobile-first approach means that class size modifiers work upwards,  so there’s no need to use the extra-small (xs) class modifier since using them without a class modifier (i.e., .text-center) applies the alignment on extra-small viewports or larger. This also means that the class  .text-md-center  would apply to all viewports of medium size upwards, unless there is another class with a modifier for viewports form the large breakpoint upwards—in this case  .text-lg-right._

## Question 5
**Which of the following is the correct structure for a card with an image, followed by a title and then text?**
- [ ] <div class="card">
    <div class="card-body">
        <img class="card-img-top" src="..." alt="...">
        <h5 class="card-title">Card Title</h5>
        <p class="card-text"> ...text... </p>
    </div>
</div>
- [ ] <div class="card">
    <img class="card-img-top" src="..." alt="...">
    <h5 class="card-title">Card Title</h5>
    <p class="card-text"> ...text... </p>
</div>
- [x] <div class="card">
    <img class=”card-img-top” src=”...” alt=”...”>
    <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">Some text...</p>
    </div>
</div>

_The card image should be a sibling of the  .card-body  div, which in turn contains the other card elements._

## Question 6
**To get a nicely styled bullet list in Bootstrap, which of the following would you use?**
- [ ] <ul class="list-styled">
    <li class="list-item">Item</li>
    ...
</ul>
- [ ] <ul class="list-inline">
    <li class="list-inline-item">Item</li>
    ...
</ul>
- [x] <ul>
    <li>Item</li>
    ...
</ul>

_Bootstrap applies styles to the <ul> and <li> elements without the need of classes to render a nicely styled bullet list by default._

## Question 7
**Bootstrap’s embed classes can be used with which of these HTML elements?**
- [ ] <img>
- [x] <video>
- [x] <iframe>
- [ ] <map>

_Bootstrap’s embed classes can be used with <iframe> and <video>, as well as <object> and <embed> elements. They are not designed to apply rules to other elements._

## Question 8
**Which of the following code snippets shows the correct way to include a logo in a Bootstrap navbar?**
- [x] <nav class="navbar">
    <a class="navbar-brand" href="#">
        <img src="/path/to/logo.png" width="40" height="30" alt="Site logo">
        Site Name
    </a>
    [...navigation items...]
</nav>
- [ ] <nav class="navbar">
    <img src="/path/to/logo.png" width="40" height="30" alt="Site logo">
    <a class="navbar-brand" href="#">
        Site Name
    </a>
    [...navigation items...]
</nav>
- [ ] <nav class="navbar">
    <a class="navbar-brand" href="#">
        Site Name
    </a>
    <img src="/path/to/logo.png" width="40" height="30" alt="Site logo">
    [...navigation items…]
</nav>

_The correct way to include a logo in the Bootstrap navbar is by nesting the <img> element in a link with the  .navbar-brand  class._