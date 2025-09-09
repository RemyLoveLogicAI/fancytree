# ![logo](doc/logo.png?raw=true) Fancytree

[![GitHub version](https://badge.fury.io/gh/mar10%2Ffancytree.svg)](https://github.com/mar10/fancytree/releases/latest)
[![npm](https://img.shields.io/npm/dm/jquery.fancytree.svg)](https://www.npmjs.com/package/jquery.fancytree)
[![jsDelivr](https://data.jsdelivr.com/v1/package/npm/jquery.fancytree/badge)](https://www.jsdelivr.com/package/npm/jquery.fancytree)
[![StackOverflow: fancytree](https://img.shields.io/badge/StackOverflow-fancytree-blue.svg)](https://stackoverflow.com/questions/tagged/fancytree)

Fancytree is a JavaScript tree view / tree grid plugin with support for keyboard, inline editing,
filtering, checkboxes, drag'n'drop, and lazy loading.

### NOTE

Fancytree is considered feature-complete. <br>
The code is still maintained and bugfixes will be commited.
However do not expect new major features.

For a modernized and more capable alternative, **consider upgrading** to
[Wunderbaum](https://github.com/mar10/wunderbaum).

### Demo

[ ![sample](doc/teaser2.png?raw=true) ](https://wwWendt.de/tech/fancytree/demo "Live demo")

### Purpose

Fancytree is a powerful and versatile JavaScript tree view and tree grid plugin for jQuery. It is designed to be highly configurable and extensible, making it suitable for a wide range of applications, from simple hierarchical displays to complex, interactive tree grids.

### Features

*   **Keyboard Navigation**: Full support for keyboard navigation, including intuitive shortcuts for expanding, collapsing, and traversing nodes.
*   **Inline Editing**: Seamlessly edit node titles directly in the tree view.
*   **Filtering**: Easily filter nodes based on custom criteria, with options to dim or hide non-matching nodes.
*   **Checkboxes**: Implement checkboxes with support for hierarchical selection.
*   **Drag'n'Drop**: Move nodes within or between trees with built-in drag-and-drop functionality.
*   **Lazy Loading**: Efficiently load large trees by fetching node data on demand.
*   **Persistence**: Save and restore the tree state (expanded, selected, focused nodes) using cookies or local storage.
*   **Theming**: Easily customize the look and feel of the tree with support for jQuery UI Themeroller.

### Get Started

-   [Try the live demo](https://wwWendt.de/tech/fancytree/demo).
-   [Read the documentation](https://github.com/mar10/fancytree/wiki).
-   [Check the Q&A forum](https://github.com/mar10/fancytree/discussions) or
    [Stackoverflow](https://stackoverflow.com/questions/tagged/fancytree) if you have questions.
-   Play with [jsFiddle](http://jsfiddle.net/mar10/KcxRd/),
    [CodePen](https://codepen.io/mar10/pen/WMWrbq),
    or [Plunker](http://plnkr.co/edit/8sdy3r?p=preview).
-   [Contribute](https://github.com/mar10/fancytree/wiki/HowtoContribute)

### Setup

To get started with Fancytree, you can include the necessary files from a CDN or install them via npm.

**CDN**

```html
<link href="https://cdn.jsdelivr.net/npm/jquery.fancytree@2.38.0/dist/skin-lion/ui.fancytree.min.css" rel="stylesheet">
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/jquery.fancytree@2.38.0/dist/jquery.fancytree-all-deps.min.js"></script>
```

**npm**

```bash
npm install jquery.fancytree
```

Then, you can import the necessary modules in your JavaScript file:

```javascript
import $ from "jquery";
import 'jquery.fancytree/dist/skin-lion/ui.fancytree.less';
import {createTree} from 'jquery.fancytree';
```

### Usage

Here's a basic example of how to create a Fancytree instance:

**HTML**

```html
<div id="tree"></div>
```

**JavaScript**

```javascript
import {createTree} from 'jquery.fancytree';

const tree = createTree('#tree', {
  source: [
    {title: "Node 1", key: "1"},
    {title: "Node 2", key: "2", folder: true, children: [
      {title: "Node 2.1", key: "3"},
      {title: "Node 2.2", key: "4"}
    ]}
  ]
});
```

For more advanced usage and a full list of options, please refer to the official [documentation](https://github.com/mar10/fancytree/wiki).

### ES6 Quickstart

```js
import $ from "jquery";

import 'jquery.fancytree/dist/skin-lion/ui.fancytree.less';  // CSS or LESS

import {createTree} from 'jquery.fancytree';

import 'jquery.fancytree/dist/modules/jquery.fancytree.edit';
import 'jquery.fancytree/dist/modules/jquery.fancytree.filter';

const tree = createTree('#tree', {
  extensions: ['edit', 'filter'],
  source: {...},
  ...
});
// Note: Loading and initialization may be asynchronous, so the nodes may not be accessible yet.
```

See [module loader support](https://github.com/mar10/fancytree/wiki#use-a-module-loader) and
[API docs](https://wwWendt.de/tech/fancytree/doc/jsdoc/Fancytree_Static.html#createTree).

### Credits

Thanks to all [contributors](https://github.com/mar10/fancytree/contributors).
