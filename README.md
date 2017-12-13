# Renaissance 🎨

The freshest css framework. Simple classnames. No fluff. 

We got the basics down. Flexbox grid, Golden Ratio Typography Flow, Buttons, Forms,Sliders, Progress Bars, Tabs, Navbar, Dropdown menus, Hamburger Menu, Notifications, Animations. Building blocks for the DaVinci in you.

# Getting Started

Either use the css file inside the "dist" directory found on Github

    https://github.com/creatorsneverdie/renaissance

or using NPM:

    npm install renaissancecss

# Grid

Renaissance uses flexbox for it's grid system. Following tradional syntax, there are containers, rows and columns.

Columns must be placed inside a row:
```
<div class="row">
    <div class="column">
    </div>
</div>
```
All columns break into their own block when on mobile, regardless of stated column size:
```
<div class="column column-1"></div>
<div class="column column-2"></div>
<div class="column column-3"></div>
<div class="column column-4"></div>
<div class="column column-5"></div>
<div class="column column-6"></div>
<div class="column column-7"></div>
<div class="column column-8"></div>
<div class="column column-9"></div>
<div class="column column-10"></div>
<div class="column column-11"></div>
<div class="column column-12"></div>
```
# Navbar

The navbar is maintained within the HTML `nav` component. When your site is accessed from mobile, the main items will be hidden and replaced with a hamburger menu. 

```
<nav>
    <div class="navbar">
        <div class="brand">
            <h3>Renaissance</h3>
        </div>

        <div class="nav">
            <div class="item">
              <a href="#">Menu</a>
            </div>

            <div class="item dropdown">
              <a href="#">Dropdown</a>
              <ul class="menu is-active">
                <li><a href="#">Menu-1</a></li>
              </ul>
            </div> 
        </div>
        
        <div class="hamburger">
            <div class="item">
              <span class="line"></span>
              <span class="line"></span>
              <span class="line"></span>
            </div>
        </div>
        
    </div>

    <div class="hamburger-dropdown">
        <div class="item">
            <a href="#">Menu</a>
        </div>
        <div class="item">
          <a href="#">Menu</a>
        </div>
    </div>

</nav>
```

## Dropdown
```
<div class="item dropdown">

<a href="#">Dropdown</a>

<ul class="menu">
    <li><a href="#">Menu-1</a></li>
</ul>

</div>
```
## Hamburger

When your site will be accessed on mobile, the main menu will be hidden and replaced with a hamburger menu. Javascript is not included for handling the click event. If the class `is-active` is placed on `hamburger-dropdown` the menu will expand.
```
<div class="hamburger-dropdown">

    <div class="item">
        <a href="#">Menu</a>
    </div>

    <div class="item">
        <a href="#">Menu</a>
    </div>

</div>
```
# Forms
```
input[type="text"], textarea, select {
    width: 100%;
}
```
All inputs that require text have a 100% width. Create a wrapping div to set the width.

# Slider
```
<div class="sliderContainer">
    <input class="slider" type="range" value="250" min="0" max="500" step="50">
</div>
```
To modify the slider handle, use a chrome or firefox prefix:

## Chrome
```
::-webkit-slider-thumb {
    -webkit-appearance: none;
    width: 30px;
    height: 30px;
    border-radius: 50%;
    background: red;
    cursor: pointer;
    transition: background .15s ease-in-out;

    &:hover {
    background: darkred;
    }
 }

:active::-webkit-slider-thumb {
    background: darkred;
}
```
## Firefox
```
::-moz-range-thumb {
    width: 30px;
    height: 30px;
    border: 0;
    border-radius: 50%;
    background: red;

    &:hover {
    background: darkred;
    }
 }

:active::-moz-range-thumb {
    background: darkred;
}
```
# Notifications

Comes in 3 colors: **success** , **alert** and **reject** 

_**Notice how notifications makes use of the grid. A notification is just a row with 2 columns inside_ 
```
<div class="notification notification--success row">

    <div class="iconContainer column column-1">
        <div class="check icon"></div>
    </div>

    <div class="body column">
        <p>This is a message telling you that everything is a-okay!</p>
    </div>

    <button class="closeContainer"><div class="close icon"></div></button>

</div>
```
# Progress Bar

You can set the percent of the progress bar by setting the width
```
<div class="progress">
    <div class="progress-bar" style="width:50%"></div>
</div>
```
# Buttons

By default, Renaissance buttons are rounded. You can remove this by setting the border-radius
```
button {
    border-radius: 0;
}
```
# Tabs
```
<ul class="tabs">
    <li><a href="#tab1" class="active">Tab 1</a></li>
    <li><a href="#tab2">Tab 2</a></li>
</ul>

<div class="tabgroup">
    <div id="tab1" style="display:block;">
        <h2>Heading 1</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nulla deserunt consectetur ratione id tempore laborum laudantium facilis reprehenderit beatae dolores ipsum nesciunt alias iusto dicta eius itaque blanditiis modi velit.</p>
    </div>

    <div id="tab2">
        <h2>Heading 2</h2>
        <p>Adipisci autem obcaecati velit natus quos beatae explicabo at tempora minima voluptates deserunt eum consectetur reiciendis placeat dolorem repellat in nam asperiores impedit voluptas iure repellendus unde eveniet accusamus ex.</p>
    </div>
</div>
```
You can set any child of **`tabgroup`** to display as a block based on which tab is pressed
