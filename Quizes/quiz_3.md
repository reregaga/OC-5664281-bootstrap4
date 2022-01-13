[Quiz](https://openclassrooms.com/en/courses/5664281-create-responsive-websites-efficiently-with-bootstrap-4/exercises/3606)
# Check Your Understanding of Bootstrap UI Components

## Question 1
**If you want the Bootstrap navbar to collapse for small and extra-small screens, and expand for all other screens, which of these classes would you have to add to the  &lt;nav&gt;  element?**
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
- [x] &lt;nav class="navbar navbar-expand-lg"&gt;
    &lt;a class="navbar-brand" href="#"&gt;Site Name&lt;/a&gt;
    &lt;button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContent"&gt;
        &lt;span class="navbar-toggler-icon"&gt;&lt;/span&gt;
    &lt;/button&gt;
    &lt;div id="navbarContent" class="collapse navbar-collapse"&gt;
        ... nav items ...
    &lt;/div&gt;
&lt;/nav&gt;
- [ ] &lt;nav class="navbar navbar-expand"&gt;
    &lt;a class="navbar-brand" href="#"&gt;Site Name&lt;/a&gt;
    &lt;button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarContent"&gt;
        &lt;span class="navbar-toggler-icon"&gt;&lt;/span&gt;
    &lt;/button&gt;
    &lt;div id="navbarContent" class="collapse navbar-collapse"&gt;
        ... nav items ...
    &lt;/div&gt;
&lt;/nav&gt;
- [ ] &lt;nav class="navbar navbar-expand-lg"&gt;
    &lt;a class="navbar-brand" href="#"&gt;Site Name&lt;/a&gt;
    &lt;button class="navbar-toggler" type="button" data-toggle="collapse"&gt;
        &lt;span class="navbar-toggler-icon"&gt;&lt;/span&gt;
    &lt;/button&gt;
    &lt;div class="collapse navbar-collapse"&gt;
        ... nav items ...
    &lt;/div&gt;
&lt;/nav&gt;
- [ ] &lt;nav class="navbar navbar-expand-lg"&gt;
    &lt;a class="navbar-brand" href="#"&gt;Site Name&lt;/a&gt;
    &lt;button class="navbar-toggler" type="button" data-target="#navbarContent"&gt;
        &lt;span class="navbar-toggler-icon"&gt;&lt;/span&gt;
    &lt;/button&gt;
    &lt;div id="navbarContent"&gt;
        ... nav items ...
    &lt;/div&gt;
&lt;/nav&gt;

_To create a responsive navbar in Bootstrap, all of the following must be included:_

## Question 4
**Which of the following would cause the alignment of a paragraph to be responsive so that it is center-aligned on medium viewports and right-aligned on all other viewport sizes?**
- [ ] &lt;p class="text-xs-right text-md-center text-lg-right"&gt; ...text... &lt;/p&gt;
- [x] &lt;p class="text-right text-md-center text-lg-right"&gt; ...text... &lt;/p&gt;
- [ ] &lt;p class="text-right text-md-center"&gt; ...text... &lt;/p&gt;

_Bootstrap’s mobile-first approach means that class size modifiers work upwards,  so there’s no need to use the extra-small (xs) class modifier since using them without a class modifier (i.e., .text-center) applies the alignment on extra-small viewports or larger. This also means that the class  .text-md-center  would apply to all viewports of medium size upwards, unless there is another class with a modifier for viewports form the large breakpoint upwards—in this case  .text-lg-right._

## Question 5
**Which of the following is the correct structure for a card with an image, followed by a title and then text?**
- [ ] &lt;div class="card"&gt;
    &lt;div class="card-body"&gt;
        &lt;img class="card-img-top" src="..." alt="..."&gt;
        &lt;h5 class="card-title"&gt;Card Title&lt;/h5&gt;
        &lt;p class="card-text"&gt; ...text... &lt;/p&gt;
    &lt;/div&gt;
&lt;/div&gt;
- [ ] &lt;div class="card"&gt;
    &lt;img class="card-img-top" src="..." alt="..."&gt;
    &lt;h5 class="card-title"&gt;Card Title&lt;/h5&gt;
    &lt;p class="card-text"&gt; ...text... &lt;/p&gt;
&lt;/div&gt;
- [x] &lt;div class="card"&gt;
    &lt;img class=”card-img-top” src=”...” alt=”...”&gt;
    &lt;div class="card-body"&gt;
        &lt;h5 class="card-title"&gt;Card title&lt;/h5&gt;
        &lt;p class="card-text"&gt;Some text...&lt;/p&gt;
    &lt;/div&gt;
&lt;/div&gt;

_The card image should be a sibling of the  .card-body  div, which in turn contains the other card elements._

## Question 6
**To get a nicely styled bullet list in Bootstrap, which of the following would you use?**
- [ ] &lt;ul class="list-styled"&gt;
    &lt;li class="list-item"&gt;Item&lt;/li&gt;
    ...
&lt;/ul&gt;
- [ ] &lt;ul class="list-inline"&gt;
    &lt;li class="list-inline-item"&gt;Item&lt;/li&gt;
    ...
&lt;/ul&gt;
- [x] &lt;ul&gt;
    &lt;li&gt;Item&lt;/li&gt;
    ...
&lt;/ul&gt;

_Bootstrap applies styles to the &lt;ul&gt; and &lt;li&gt; elements without the need of classes to render a nicely styled bullet list by default._

## Question 7
**Bootstrap’s embed classes can be used with which of these HTML elements?**
- [ ] &lt;img&gt;
- [x] &lt;video&gt;
- [x] &lt;iframe&gt;
- [ ] &lt;map&gt;

_Bootstrap’s embed classes can be used with &lt;iframe&gt; and &lt;video&gt;, as well as &lt;object&gt; and &lt;embed&gt; elements. They are not designed to apply rules to other elements._

## Question 8
**Which of the following code snippets shows the correct way to include a logo in a Bootstrap navbar?**
- [x] &lt;nav class="navbar"&gt;
    &lt;a class="navbar-brand" href="#"&gt;
        &lt;img src="/path/to/logo.png" width="40" height="30" alt="Site logo"&gt;
        Site Name
    &lt;/a&gt;
    [...navigation items...]
&lt;/nav&gt;
- [ ] &lt;nav class="navbar"&gt;
    &lt;img src="/path/to/logo.png" width="40" height="30" alt="Site logo"&gt;
    &lt;a class="navbar-brand" href="#"&gt;
        Site Name
    &lt;/a&gt;
    [...navigation items...]
&lt;/nav&gt;
- [ ] &lt;nav class="navbar"&gt;
    &lt;a class="navbar-brand" href="#"&gt;
        Site Name
    &lt;/a&gt;
    &lt;img src="/path/to/logo.png" width="40" height="30" alt="Site logo"&gt;
    [...navigation items…]
&lt;/nav&gt;

_The correct way to include a logo in the Bootstrap navbar is by nesting the &lt;img&gt; element in a link with the  .navbar-brand  class._