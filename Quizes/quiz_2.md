[Quiz](https://openclassrooms.com/en/courses/5664281-create-responsive-websites-efficiently-with-bootstrap-4/exercises/3605)
# Check Your Understanding of Responsive Page Layouts

## Question 1
**Wrapping your page's contents in a div with the.container-fluid class creates:**
- [ ] A centered container that adapts to the width of its content.
- [ ] A centered container that adapts to the width of the viewport.
- [x] A container that takes up 100% of the width of the viewport.

_Wrapping your content in a div with the  .container-fluid  class creates a container that takes up 100% of the width of the viewport. On the other hand, wrapping it in a div with a  .container  class adapts to the width of the viewport and provides horizontal padding for its contents so they don’t push up against the edges._

## Question 2
**The correct basic hierarchy of the classes used to create a Bootstrap grid is:**
- [ ] Container > column > row
- [ ] Row > column > container
- [x] Container > row > column
- [ ] Column > container > row

_The basic hierarchy of the Bootstrap grid is that of a container that contains rows, which in turn contain columns._

## Question 3
**Which of the following is true?**
- [ ] A  .container  div can include only one  .row  div, and a  .row  div can contain multiple  .col[-*]  divs.
- [x] A  .container  div can include multiple  .row  divs, and a  .row  div can contain multiple  .col[-*]  divs.
- [ ] A  .container  div can include multiple  .row  divs, and a  .row  div can contain only one  .col[-*]  div.
- [ ] A  .container  div can include only one  .row  div, and a  .row  div can contain only one  .col[-*]  div.

_Containers can contain multiple rows, and rows can contain multiple columns._

## Question 4
**How many columns will each of the divs with the  .col  class in this code snippet take up?
<div class="row">
    <div class="col">
        ...
    </div>
    <div class="col">
        ...
    </div>
    <div class="col">
        ...
    </div>
</div>**
- [ ] 2
- [ ] 3
- [x] 4
- [ ] 6

_The default Bootstrap grid is based on a 12-column structure which means that using the .col class without any size modifier will divide the grid equally in all viewports between the divs in a row. In this case, the 12 columns will be divided equally between the three divs, giving each one a width of four columns._

## Question 5
**Which of the following will create a row that contains two <divs>, the first taking up 1/4 of its width and the second taking up 3/4 of its width:**
- [x] <div class="row">
    <div class="col-3">...</div>
    <div class="col-9">...</div>
</div>
- [ ] <div class="row">
    <div class="col-1">...</div>
    <div class="col-3">...</div>
</div>
- [ ] <div class="row">
    <div class="col-4">...</div>
    <div class="col-3">...</div>
</div>
- [ ] <div class="row">
    <div class="col-4">...</div>
    <div class="col-8">...</div>
</div>

_Since Bootstrap is based on a 12 column grid, a <div> that takes up 1/4 of the width would span three columns and therefore have a class of  .col-3 , whereas the second <div> would span nine columns and have a class of  .col-9._

## Question 6
**In the context of front-end design and development, a breakpoint is:**
- [ ] A point at which the page layout may stop working. It is usually expressed as a viewport width in pixels.
- [ ] A point at which the page layout may change. It is usually expressed as a viewport width in columns.
- [x] A point at which the page layout may change. It is usually expressed as a viewport width in pixels.
- [ ] A point at which the page layout may stop working. It is usually expressed as a viewport width in columns.

_In the context of front-end design and development, a breakpoint is a point at which the layout of a page may change. It is usually expressed as a number representing the number of pixels that represent the width of the viewport at which the breakpoint occurs._

## Question 7
**Based on the following code, which viewport sizes will have each of the column <div>’s take up half of the width of the row:
<div class="row">
    <div class="col-6 col-md-4">...</div>
    <div class="col-6 col-md-8">...</div>
</div>**
- [x] Extra-small
- [x] Small
- [ ] Medium
- [ ] Large
- [ ] Extra-large

_The  .col-6  class has no size related class modifier, so it applies to extra-small viewports upwards. However, the  .col-md-*  classes apply to medium viewports upwards, overriding the earlier class for those viewports. So the col-6, which spans half of the 12 column grid, will apply only to extra-small and small viewports._

## Question 8
**Which of the following grid structures will have the following responsive behavior: half the width on small and extra-small viewports; ⅓ the width on medium viewports; and ¼ of the width on large and extra-large viewport.**
- [ ] <div class="row">
    <div class="col-6 col-md-3 col-lg-4">
        ...
    </div>
        ...
</div>
- [ ] <div class="row">
    <div class="col-2 col-md-3 col-lg-4">
        ...
    </div>
        ...
</div>
- [x] <div class="row">
    <div class="col-6 col-md-4 col-lg-3">
        ...
    </div>
        ...
</div>
- [ ] <div class="row">
    <div class="col-sm-6 col-md-4 col-lg-3">
        ...
    </div>
        ...
</div>

_Since the requirement is for extra-small and small viewports to span half the width of the grid, the  .col-6  class would apply to extra-small viewports upwards. Adding the  .col-md-4  would override this for medium viewports upwards, resulting in the <div> spanning four out of the 12 columns (i.e. ⅓). Finally, adding the  .col-lg-3  class would override the previous classes for large viewports upwards, resulting in the <div> spanning three out of the 12 columns (i.e. ¼)._
