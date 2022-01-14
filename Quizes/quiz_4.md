**Attention!** Last two questions contains semi-correct explanation, BUT contains de-facto (for openclassrooms server) correct and de-jure incorrect answers.

[Quiz](https://openclassrooms.com/en/courses/5664281-create-responsive-websites-efficiently-with-bootstrap-4/exercises/3622)
# Check Your Understanding of Interactive Components

## Question 1
**Which of the following will render a link as a red button?**
- [ ] &lt;a href="#" class="btn btn-warning"&gt;Take the Red Pill!&lt;/button&gt;
- [x] &lt;a href="#" class="btn btn-danger"&gt;Take the Red Pill!&lt;/button&gt;
- [ ] &lt;a href="#" class="btn btn-info"&gt;Take the Red Pill!&lt;/button&gt;
- [ ] &lt;a href="#" class="btn btn-primary"&gt;Take the Red Pill!&lt;/button&gt;

_The default effect of the  .btn-danger  class in Bootstrap is to render a button with a red background._

## Question 2
**Which of the following are valid width setting classes in Bootstrap?**
- [x] w-75
- [ ] w-10
- [ ] w-0
- [x] w-auto

_The valid width setting classes are  w-100,  w-75,  w-50,  w-25, andw-auto, which respectively give an element width values of 100%, 75%, 50%, 25%, and auto, relative to its parent._

## Question 3
**Which of the following will render a green border around the element?**
- [ ] &lt;div class="border-secondary"&gt;...&lt;/div&gt;
- [ ] &lt;div class="border-info"&gt;...&lt;/div&gt;
- [ ] &lt;div class="border-warning"&gt;...&lt;/div&gt;
- [x] &lt;div class="border-success"&gt;...&lt;/div&gt;

_The  .border-success  class in Bootstrap has the default effect of rendering a green border._

## Question 4
**When the  .shadow-lg  class is applied to an element...**
- [x] ...it creates a large shadow effect for the element.
- [ ] ...it creates a shadow effect for the element only on large viewports.
- [ ] ...it creates a shadow effect for the element on large viewports upwards.

_The class modifier for the  shadow  class refers to the size of the shadow effect and is not related to the viewport size._

## Question 5
**The easiest way to add structure to your forms with Bootstrap is to create a &lt;div&gt;. Which class should you use to contain the elements related to each form field?**
- [ ] .form-control
- [ ] .form-input
- [ ] .form-field
- [x] .form-group

_The easiest way to add structure to your forms with Bootstrap is to create a &lt;div&gt; with a class of  .form-group  to contain the elements related to each form field._

## Question 6
**Which of the following form field types requires the  .form-control  class to render correctly in Bootstrap?**
- [x] &lt;input type=”text”&gt;
- [ ] &lt;input type="range"&gt;
- [x] &lt;textarea&gt;
- [x] &lt;select&gt;

_The  &lt;input type="range"&gt;  requires a  .form-control-range  class, whereas the others require the  .form-control  class._

## Question 7
**Which of the following combinations of classes will give an element a top margin of 0 on medium viewports and larger and 3 rem on other viewports?**
- [x] &lt;div class="mt-5 mt-md-0"&gt;...&lt;/div&gt;
- [ ] &lt;div class="mt-5 mt-0-md"&gt;...&lt;/div&gt;
- [ ] &lt;div class="mt-3 mt-md-0"&gt;...&lt;/div&gt;
- [ ] &lt;div class="mt-3 mt-0-md"&gt;...&lt;/div&gt;

_The Bootstrap spacing utilities use the format:  {property}{sides}-[{breakpoint}-]{size}.
The  .mt-5  class will give margin top of 5 (which sets it to 3 rem). Since it has no size based class modifier, it applies to all viewports from extra-small upwards. 
The  .mt-md-0  class overrides the earlier class. It will give a margin top of 0. Since it uses the md class modifier, it will apply this margin to medium viewports upwards._

## Question 8
**Which of the following combination of classes will give an element a left and right padding of 3 rem on large viewports and larger and 1 rem on other viewports?**
- [ ] &lt;div class="px-1 px-lg-3"&gt;...&lt;/div&gt;
- [x] &lt;div class="px-3 px-lg-5"&gt;...&lt;/div&gt;
- [ ] &lt;div class="plr-3 plr-lg-5"&gt;...&lt;/div&gt;
- [ ] &lt;div class="plr-1 plr-lg-3"&gt;...&lt;/div&gt;

_The Bootstrap spacing utilities use the format:  {property}{sides}-[{breakpoint}-]{size}.
The  .px-3  class will give padding of 3 (which sets it to 1 rem) to the left and right (ie., both sides in the x-direction). Since it has no size based class modifier, it applies to all viewports from extra-small upwards. 
The  .px-lg-3  class overrides the earlier class. It will give a padding of 5 (which sets it to 3 rem) to the left and right. Since it uses the lg class modifier, it will apply this margin to large viewports upwards._