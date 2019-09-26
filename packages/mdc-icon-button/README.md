<!--docs:
title: "Icon Buttons"
layout: detail
section: components
iconId: button
path: /catalog/buttons/icon-buttons/
-->

# Icon Buttons

<!--<div class="article__asset">
  <a class="article__asset-link"
     href="https://material-components.github.io/material-components-web-catalog/#/component/icon-button">
    <img src="{{ site.rootpath }}/images/mdc_web_screenshots/icon-toggles.png" width="20" alt="Icon buttons screenshot">
  </a>
</div>-->

Icon buttons allow users to take actions, and make choices, with a single tap. The icon button can be used to toggle between an on and off icon.

## Using `mdc-icon-button`

The `mdc-icon-button` component provides an implementation of Material Design’s [toggle button](https://material.io/components/buttons/#toggle-button) with icons.

### Install `mdc-icon-button`
Install the `icon-button` before including it in your source.
    ```bash
    npm install @material/icon-button
    ```
### Add a theme (style)
The `mdc-icon-button` component works with themes (styles). Import a style into your stylesheet to apply it to your website, including icon buttons:
    ```js
    @import "@material/icon-button/mdc-icon-button";
    ```

### Import JavaScript button effects
You can also add a JavaScript ripple effect (see [MDC Ripple](https://github.com/material-components/material-components-web/blob/master/packages/mdc-ripple)) to your icon buttons by importing then instantiating `MCDRipple`. See the page on importing the [JavaScript component](https://github.com/material-components/material-components-web/blob/master/docs/importing-js.md) for more information on importing JavaScript.

```js
import {MDCRipple} from '@material/ripple';

const iconButtonRipple = new MDCRipple(document.querySelector('.mdc-icon-button'));
iconButtonRipple.unbounded = true;
```
### Add an icon to an `mdc-icon-button` instance

Add an icon to your `mdc-icon-button` instance using the following steps:

1. In your HTML file, reference the font library you would like to use (we recommend the [Material Icons](https://material.io/tools/icons/) from Google Fonts):
    ```HTML
    <head>
      <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    </head>
    ```
1. Include the `mcd-icon-button__icon` class inside your icon button element.
  You can set the default `pressed` state with the attribute `aria-pressed`. If a toggle button default is `pressed` (`aria-pressed="true"`), you will need to add `mdc-icon-button__icon--on` to the to the class `mdc-icon-button__icon`.

    **Example using [Material Icons](https://material.io/tools/icons/)**
    <img src="" alt="Image or demo of an icon button using Material Icons">
    ```HTML
    <button id="add-to-favorites"
      class="mdc-icon-button"
      aria-label="Add to favorites"
      aria-hidden="true"
      aria-pressed="false">
     <i class="material-icons mdc-icon-button__icon mdc-icon-button__icon--on">favorite</i>
     <i class="material-icons mdc-icon-button__icon">favorite_border</i>
    </button>
    ```
    **Example using SVG Icons**
    <img src="" alt="Image or demo of an icon button using SVG icons">
    ```html
    <button id="star-this-item"
       class="mdc-icon-button mdc-icon-button--on"
       aria-label="Unstar this item"
       aria-hidden="true"
       aria-pressed="true">
       <svg class="mdc-icon-button__icon">
         /*...*/
       </svg>
       <svg class="mdc-icon-button__icon mdc-icon-button__icon--on">
         /*...*/
      </svg>
    </button>
    ```
    **Example using toggle button with an image**
    <img src="" alt="Image or demo of an icon button using on and off button icons">
    ```HTML
    <button id="star-this-item"
      class="mdc-icon-button mdc-icon-button--on"
      aria-label="Unstar this item"
      aria-hidden="true"
      aria-pressed="true">
      <img src="" class="mdc-icon-button__icon"/>
      <img src="" class="mdc-icon-button__icon mdc-icon-button__icon--on"/>
    </button>
    ```

## Related APIs

[Source code](https://github.com/material-components/material-components-web/tree/master/packages/mdc-icon-button): GitHub source repository</br>
[Demo site](https://material-components.github.io/material-components-web-catalog/#/component/icon-button): You can use this site to see examples of toggled icon buttons.

**CSS classes** apply themes (styles) to your button

CSS Class |	Description
---|---
`mdc-icon-button` | Required
`mdc-icon-button--on`	| Apply this class to the root element to indicate if the icon button toggle is in the “on” state.
`mdc-icon-button__icon`	| Apply this class to each icon element for the icon button toggle.
`mdc-icon-button__icon--on`	| Apply this class to an icon element to indicate the toggle button icon that represents the “on” icon.

**Sass Mixins** customize an icon button's color and properties

<<<<<<< HEAD
Mixin | Description
--- | ---
`mdc-icon-button-size($width, $height, $padding)` | Sets the width, height, font-size and padding for the icon and ripple. `$height` is optional and defaults to `$width`. `$padding` is optional and defaults to `max($width, $height)/2`. `font-size` is set to `max($width, $height)`.
`mdc-icon-button-ink-color($color)` | Sets the font color and the ripple color to the provided color value.

**`MDCIconButtonToggle`** sets the icon toggle state

Property | Value Type | Description
--- | --- | ---
`on` | Boolean | Sets the toggle state to the provided `isOn` value.

**Events** triggers when the toggle button changes state

Event Name | Event Data Structure | Description
--- | --- | ---
`MDCIconButtonToggle:change` | `{"detail": {"isOn": boolean}}` | Emits when the icon is toggled.

### Usage within Web Frameworks

If you are using a JavaScript framework, such as React or Angular, you can create an Icon Button Toggle for your framework. Depending on your needs, you can use the _Simple Approach: Wrapping MDC Web Vanilla Components_, or the _Advanced Approach: Using Foundations and Adapters_. Please follow the instructions [here](../../docs/integrating-into-frameworks.md).

**`MDCIconButtonToggleAdapter`**

Method Signature | Description
--- | ---
`addClass(className: string) => void` | Adds a class to the root element.
`removeClass(className: string) => void` | Removes a class from the root element.
`hasClass(className: string) => boolean` | Determines whether the root element has the given CSS class name.
`setAttr(name: string, value: string) => void` | Sets the attribute `name` to `value` on the root element.
`notifyChange(evtData: {isOn: boolean}) => void` | Broadcasts a change notification, passing along the `evtData` to the environment's event handling system. In our vanilla implementation, Custom Events are used for this.

**Foundation: `MDCIconButtonToggleFoundation`**

Method Signature | Description
--- | ---
`handleClick()` | Event handler triggered on the click event. It will toggle the icon from on/off and update aria attributes.

=======
### Add an icon to an `mdc-icon-button` instance

Add an icon to your `mdc-icon-button` instance using the following steps:

1. In your HTML file, reference the font library you would like to use (we recommend the [Material Icons](https://material.io/tools/icons/) from Google Fonts):

    ```HTML
    <head>
      <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    </head>
    ```
    
1. Include the `mcd-icon-button__icon` class inside your icon button element.
  You can set the default `pressed` state with the attribute `aria-pressed`. If a toggle button default is `pressed` (`aria-pressed="true"`), you will need to add `mdc-icon-button__icon--on` to the to the class `mdc-icon-button__icon`.

    **Example using [Material Icons](https://material.io/tools/icons/)**
    
    <img src="" alt="Image or demo of an icon button using Material Icons">
    
    ```HTML
    <button id="add-to-favorites"
      class="mdc-icon-button"
      aria-label="Add to favorites"
      aria-hidden="true"
      aria-pressed="false">
     <i class="material-icons mdc-icon-button__icon mdc-icon-button__icon--on">favorite</i>
     <i class="material-icons mdc-icon-button__icon">favorite_border</i>
    </button>
    ```
    **Example using SVG Icons**
    
    <img src="" alt="Image or demo of an icon button using SVG icons">
    
    ```html
    <button id="star-this-item"
       class="mdc-icon-button mdc-icon-button--on"
       aria-label="Unstar this item"
       aria-hidden="true"
       aria-pressed="true">
       <svg class="mdc-icon-button__icon">
         /*...*/
       </svg>
       <svg class="mdc-icon-button__icon mdc-icon-button__icon--on">
         /*...*/
      </svg>
    </button>
    ```
    **Example using toggle button with an image**
    
    <img src="" alt="Image or demo of an icon button using on and off button icons">
    
    ```HTML
    <button id="star-this-item"
      class="mdc-icon-button mdc-icon-button--on"
      aria-label="Unstar this item"
      aria-hidden="true"
      aria-pressed="true">
      <img src="" class="mdc-icon-button__icon"/>
      <img src="" class="mdc-icon-button__icon mdc-icon-button__icon--on"/>
    </button>
    ```

## Related APIs

[Source code](https://github.com/material-components/material-components-web/tree/master/packages/mdc-icon-button): GitHub source repository</br>
[Demo site](https://material-components.github.io/material-components-web-catalog/#/component/icon-button): You can use this site to see examples of toggled icon buttons.

**CSS classes** apply themes (styles) to your button

CSS Class |	Description
---|---
`mdc-icon-button` | Required
`mdc-icon-button--on`	| Apply this class to the root element to indicate if the icon button toggle is in the “on” state.
`mdc-icon-button__icon`	| Apply this class to each icon element for the icon button toggle.
`mdc-icon-button__icon--on`	| Apply this class to an icon element to indicate the toggle button icon that represents the “on” icon.

**Sass Mixins** customize an icon button's color and properties

Mixin | Description
--- | ---
`mdc-icon-button-size($width, $height, $padding)` | Sets the width, height, font-size and padding for the icon and ripple. `$height` is optional and defaults to `$width`. `$padding` is optional and defaults to `max($width, $height)/2`. `font-size` is set to `max($width, $height)`.
`mdc-icon-button-ink-color($color)` | Sets the font color and the ripple color to the provided color value.

**`MDCIconButtonToggle`** sets the icon toggle state

Property | Value Type | Description
--- | --- | ---
`on` | Boolean | Sets the toggle state to the provided `isOn` value.

**Events** triggers when the toggle button changes state

Event Name | Event Data Structure | Description
--- | --- | ---
`MDCIconButtonToggle:change` | `{"detail": {"isOn": boolean}}` | Emits when the icon is toggled.

### Usage within Web Frameworks

If you are using a JavaScript framework, such as React or Angular, you can create an Icon Button Toggle for your framework. Depending on your needs, you can use the _Simple Approach: Wrapping MDC Web Vanilla Components_, or the _Advanced Approach: Using Foundations and Adapters_. Please follow the instructions [here](../../docs/integrating-into-frameworks.md).

**`MDCIconButtonToggleAdapter`**

Method Signature | Description
--- | ---
`addClass(className: string) => void` | Adds a class to the root element.
`removeClass(className: string) => void` | Removes a class from the root element.
`hasClass(className: string) => boolean` | Determines whether the root element has the given CSS class name.
`setAttr(name: string, value: string) => void` | Sets the attribute `name` to `value` on the root element.
`notifyChange(evtData: {isOn: boolean}) => void` | Broadcasts a change notification, passing along the `evtData` to the environment's event handling system. In our vanilla implementation, Custom Events are used for this.

**Foundation: `MDCIconButtonToggleFoundation`**

Method Signature | Description
--- | ---
`handleClick()` | Event handler triggered on the click event. It will toggle the icon from on/off and update aria attributes.

>>>>>>> 2474fe11dfc3942067bbcad533b3f57f513b831a

## Icon Button Toggle

To style an icon button as an icon button toggle, add
both icons as child elements and place the `mdc-icon-button__icon--on` class on the icon that represents the on element.
If the button should be initialized in the "on" state, then add the `mdc-icon-button--on` class to the parent `button`.
Then instantiate an `MDCIconButtonToggle` on the root element.

```html
<button id="add-to-favorites"
   class="mdc-icon-button"
   aria-label="Add to favorites"
   aria-hidden="true"
   aria-pressed="false">
   <i class="material-icons mdc-icon-button__icon mdc-icon-button__icon--on">favorite</i>
   <i class="material-icons mdc-icon-button__icon">favorite_border</i>
</button>
```

```js
var toggleButton = new mdc.iconButton.MDCIconButtonToggle(document.getElementById('add-to-favorites'));
```


### Disabled

To disable an icon, add the `disabled` attribute directly to the `<button>` element. Icon buttons that use the `<a>` tag
cannot be disabled. Disabled icon buttons cannot be interacted with and have no visual interaction effect.

```html
<button class="mdc-icon-button material-icons" disabled>favorite</button>
```

## Examples

### Example 1

Description of the sample and what it does.
<<<<<<< HEAD
=======

>>>>>>> 2474fe11dfc3942067bbcad533b3f57f513b831a
<img src="" alt="This is the output of the example code">
