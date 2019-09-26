<!--docs:
title: "Buttons"
layout: detail
section: components
excerpt: "Material Design-styled buttons."
iconId: button
path: /catalog/buttons/button
-->

# Buttons (mdc-button)

<!--<div class="article__asset">
  <a class="article__asset-link"
     href="https://material-components.github.io/material-components-web-catalog/#/component/button">
    <img src="{{ site.rootpath }}/images/mdc_web_screenshots/buttons.png" width="363" alt="Buttons screenshot">
  </a>
</div>-->

Buttons allow users to take actions, and make choices, with a single tap. This button component has several built-in styles to support different levels of emphasis, as typically any UI will contain a few different buttons to indicate different actions.

## `mdc-button` Variants
* [Text (flat) button](#text-flat-button)
    <img src="" alt="image or demo of a text button">
* [Outlined button](#outlined-button)
    <img src="" alt="image or demo of an outline button">
* [Contained (raised) button](#contained-raised-button)
    <img src="" alt="image or demo of a contained (raised) button">

## Using `mdc-button`
The `mdc-button` component provides an implementation of Material Design’s button component without the toggle capability. Go to [mdc-icon-button](mdc-icon-button) to add [toggle buttons using icons](https://material.io/buttons/#toggle-button).

### Install `mdc-button`
Install the `mdc-button` component before including it in your source.

```bash
npm install @material/buttons
```
### Add a theme (style)
The `mdc-button` component works with themes (styles). Import a style into your stylesheet to apply it to your website, including buttons:

```css
@import "@material/button/mdc-button";
```
### Import JavaScript button effects
You can also add a JavaScript ripple effect (see [MDC Ripple](https://github.com/material-components/material-components-web/blob/master/packages/mdc-ripple)) to your buttons by importing then instantiating `MCDRipple`. See the page on importing the [JavaScript component](https://github.com/material-components/material-components-web/blob/master/docs/importing-js.md) for more information on importing JavaScript.

```js
import {MDCRipple} from '@material/ripple';

const buttonRipple = new MDCRipple(document.querySelector('.mdc-button'));
```

### Add an icon to `mdc-button`

Add an icon to your `mdc-button` instance using the following steps:

1. In your HTML file, reference the font library you would like to use (we recommend the [Material Icons](https://material.io/tools/icons/) from Google Fonts):
    ```HTML
    <head>
      <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    </head>
    ```
1. Include the `mcd-button__icon` class inside your button element. Set the attribute `area-hidden="true"`.
    **Note** The location of the icon element determines if the icon comes before (*leading*) or after (*trailing icon*) the text.

    **Example using [Material Icons](https://material.io/tools/icons/)**
    ```HTML
    <button class="mdc-button">
      <i class="material-icons mdc-button__icon" aria-hidden="true">favorite</i>
      <span class="mdc-button__label">Button</span>
    </button>
    ```
    **Example using SVG Icons**
    ```html
    <button class="mdc-button">
      <svg class="mdc-button__icon" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" viewBox="...">
        /*...*/
      </svg>
      <span class="mdc-button__label">Button</span>
    </button>
    ```
### Related APIs

<ul class="icon-list">
  <li class="icon-list-item icon-list-item--spec">
    <a href="https://material.io/go/design-buttons">Material Design guidelines: Buttons</a>
  </li>
  <li class="icon-list-item icon-list-item--link">
    <a href="https://material-components.github.io/material-components-web-catalog/#/component/button">Demo</a>
  </li>
</ul>

### Text (flat) button

Text buttons are typically used for less-pronounced actions, including those located:
* In dialogs
* In cards
In cards, text buttons help maintain an emphasis on card content.



element | class | class description
---|---|---
button | `mdc-button` | text button
span | `mdc-button__label` | applies the text to the button

#### Text button example
<img src=""<img src="" alt="image or demo of a text (flat) button based on the sample code output">

```html
 <button class="mdc-button">
  <span class="mdc-button__label">Button</span>
</button>
```

### Outlined button

Outlined buttons are medium-emphasis buttons. They contain actions that are important, but aren’t the primary action in an app.


#### Outlined button example

<img src=""<img src="" alt="image or demo of an outlined button based on the sample code output">

```html
 <button class="mdc-button--outlined">
  <span class="mdc-button__label">Button</span>
</button>
```

### Contained (raised) button

Contained buttons are high-emphasis, distinguished by their use of elevation and fill. They contain actions that are primary to your app.


#### Contained button example


<img src=""<img src="" alt="image or demo of a contained (raised) button based on the sample code output">

```html
 <button class="mdc-button--elevated">
  <span class="mdc-button__label">Button</span>
</button>
```
