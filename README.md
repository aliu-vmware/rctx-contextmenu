![NPM Badge](https://badge.fury.io/js/rctx-contextmenu.svg)

# rctx-contextmenu 🔥
Context menu plugin for React.
[Live Demo](https://reachtokish.github.io/rctx-contextmenu/) | [Example Code](https://github.com/reachtokish/rctx-contextmenu/tree/master/example)

## The problem :hushed:
There are lot of times when you want to customize the right click menu or Context Menu. May be you want to add more customized options or even sub options with same look and feel how a native context menu gives.

<!-- --------------------------------------------------- -->

## The solution :smile:
`rctx-contextmenu` gives that flexibility to customize Context Menu. You can add options, sub-options with exactly the look and feel how you get when you use the native Context Menu.

<!-- --------------------------------------------------- -->

## Key features :bulb:
<!-- - Append to body or root tag :sparkler: -->
- Customize styling like however you want :bouquet:
- N level of Sub-Menu :scream:
- Extensive list of APIs 💪

<!-- --------------------------------------------------- -->

## Table of contents :pizza:
- [Installation](#installation-heavy_check_mark)
- [Sample Usage](#sample-usage-rocket)
- [Live Demo](#live-demo-saxophone)
- [Example Code](#example-code-book)
- [APIs](#apis-evergreen_tree)
- [Styling](#styling-ear_of_rice)
- [Contributions](#contributions-pray)
- [LICENSE](#license-triangular_flag_on_post)

<!-- --------------------------------------------------- -->

## Installation :heavy_check_mark:
```
npm install --save rctx-contextmenu
```

<!-- --------------------------------------------------- -->

## Sample Usage :rocket:
```jsx
import React from 'react';
import { ContextMenuTrigger, ContextMenu, ContextMenuItem } from 'rctx-contextmenu';

function App() {
  return (
    <div className="app">
      <ContextMenuTrigger
        id="my-context-menu-1"
      >
        <div className="box">
          Right Click On Me
        </div>
      </ContextMenuTrigger>

      <ContextMenu id="my-context-menu-1">
        <ContextMenuItem>Menu Item 1</ContextMenuItem>
        <ContextMenuItem>Menu Item 2</ContextMenuItem>
        <ContextMenuItem>Menu Item 3</ContextMenuItem>
        <ContextMenuItem>Menu Item 4</ContextMenuItem>
      </ContextMenu>
    </div>
  );
}

export default App;
```
<!-- --------------------------------------------------- -->

## Full example usage
```jsx
<ContextMenu
  id="my-contextmenu"
  hideOnLeave={false}
  preventHideOnResize={false}
  preventHideOnScroll={false}
  onMouseLeave={() => console.log('Mouse left')}
  onShow={() => console.log('I am visible!')}
  onHide={() => console.log('I am hidden!')}
/>
```

```jsx
<ContextMenuItem
  disabled={true}
  preventClose={false}
  disableIfShiftIsPressed={true}
  attributes={{
    'aria-label': 'Some text'
    'aria-labelledby': 'Some text'
  }}
  onClick={() => console.log("I'm clicked!")}
/>
```

```jsx
<ContextMenuTrigger
  id="my-contextmenu"
  disable={false}
  attributes={{
    'aria-label': 'Some text'
    'aria-labelledby': 'Some text'
  }}
/>
```

```jsx
<Submenu
  title="My submenu"
/>
```

## Live Demo :saxophone:
Live demo is available [here](https://reachtokish.github.io/rctx-contextmenu/).

<!-- --------------------------------------------------- -->

## Example Code :book:
Example code is available [here](https://github.com/reachtokish/rctx-contextmenu/tree/master/example).

<!-- --------------------------------------------------- -->

## APIs :evergreen_tree:
#### `<ContextMenu />`
<table class="table table-bordered table-striped">
  <thead>
  <tr>
    <th style="width: 60px;">Name</th>
    <th style="width: 50px;">Type</th>
    <th style="width: 10px;">Options</th>
    <th>Description</th>
  </tr>
  </thead>
  <tbody>
    <tr>
      <td>id</td>
      <td>String</td>
      <td>Should be a string.</td>
      <td>`ContextMenu` and `ContextMenuTrigger` id should match</td>
    </tr>
    <!-- <tr>
      <td>appendTo</td>
      <td>Element</td>
      <td>Should be a valid DOM element. <strong>Default: Enclosed element</strong></td>
      <td>Append context menu inside the passed element</td>
    </!-->
    <tr>
      <td>hideOnLeave</td>
      <td>Boolean</td>
      <td>true / false. <strong>Default: false</strong></td>
      <td>Hide contextmenu on blur or mouseOut.</td>
    </tr>
    <tr>
      <td>onMouseLeave</td>
      <td>Function</td>
      <td>() => {}</td>
      <td>Invoke onMouseLeave on blur or mouseOut.</td>
    </tr>
    <tr>
      <td>preventHideOnResize</td>
      <td>Boolean</td>
      <td>true / false. <strong>Default: false</strong></td>
      <td>Prevent hiding contextmenu from hiding on window resize.</td>
    </tr>
    <tr>
      <td>preventHideOnScroll</td>
      <td>Boolean</td>
      <td>true / false. <strong>Default: false</strong></td>
      <td>Prevent hiding contextmenu from hiding on scroll.</td>
    </tr>
    <tr>
      <td>onShow</td>
      <td>Function</td>
      <td>() => {}</td>
      <td>Trigger this event when Context Menu is visible.</td>
    </tr>
    <tr>
      <td>onHide</td>
      <td>Function</td>
      <td>() => {}</td>
      <td>Trigger this event when Context Menu is hidden.</td>
    </tr>
  </tbody>
</table>

#### `<ContextMenuItem />`
<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <th style="width: 60px;">Name</th>
      <th style="width: 50px;">Type</th>
      <th style="width: 10px;">Options</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>onClick</td>
      <td>Function</td>
      <td>() => {}</td>
      <td>Fire onClick event.</td>
    </tr>
    <tr>
      <td>disabled</td>
      <td>Boolean</td>
      <td>true / False . Default False</td>
      <td>Disable menu item.</td>
    </tr>
    <tr>
      <td>preventClose</td>
      <td>Boolean</td>
      <td>true / False . Default False</td>
      <td>Context menu is closed as soon as an item is clicked.</td>
    </tr>
    <tr>
      <td>attributes</td>
      <td>Object</td>
      <td>Rest props</td>
      <td>-</td>
    </tr>
    <tr>
      <td>disableIfShiftIsPressed</td>
      <td>Boolean</td>
      <td>true / false. <strong>Default: false</strong></td>
      <td>Open browser default contextmenu if shift pressed while right click on trigger element.</td>
    </tr>
  </tbody>
</table>

#### `<ContextMenuTrigger />`
<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <td>id</td>
      <td>String</td>
      <td>Should be a string.</td>
      <td>`ContextMenu` and `ContextMenuTrigger` id should match</td>
    </tr>
    <tr>
      <th style="width: 60px;">Name</th>
      <th style="width: 50px;">Type</th>
      <th style="width: 10px;">Options</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>attributes</td>
      <td>Object</td>
      <td>{}</td>
      <td>Add addition props.</td>
    </tr>
    <tr>
      <td>disable</td>
      <td>true / false. <strong>Default: false</strong></td>
      <td>false</td>
      <td>Disable contextmenu and open browser default contextmenu.</td>
    </tr>
  </tbody>
</table>

#### `<Submenu />`
<table class="table table-bordered table-striped">
  <thead>
    <tr>
      <td>title</td>
      <td>String</td>
      <td>Should be a string.</td>
      <td>Title for the Submenu</td>
    </tr>
  </tbody>
</table>

<!-- --------------------------------------------------- -->

## Styling :ear_of_rice:
Styling is totally up to you. You can use CSS or even SCSS to customize the styling part. Below are the classes you can consider for styling

- **menu-trigger** (Right click area wrapper)
- **contextmenu** (The Context Menu)
- **contextmenu__item** (Each Context Menu item)
- **submenu** (Context Submenu)
- **submenu__item** (Context Submenu item)

<!-- --------------------------------------------------- -->

## Contributions :pray:
Any kind of contribution would be much appreciated. It could be small change in the doc or even any kind of advice. You can create issues if you feel any feature which is missing which solves bigger problems.

<!-- --------------------------------------------------- -->

## License :triangular_flag_on_post:
MIT License