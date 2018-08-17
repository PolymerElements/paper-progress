[![Published on NPM](https://img.shields.io/npm/v/@polymer/paper-progress.svg)](https://www.npmjs.com/package/@polymer/paper-progress)
[![Build status](https://travis-ci.org/PolymerElements/paper-progress.svg?branch=master)](https://travis-ci.org/PolymerElements/paper-progress)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://webcomponents.org/element/@polymer/paper-progress)

## &lt;paper-progress&gt;
<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="../paper-styles/color.html">
    <link rel="import" href="paper-progress.html">
    <style is="custom-style">
      paper-progress {
        display: block;
        width: 100%;
        margin: 20px 0;
      }
      paper-progress.slow {
        --paper-progress-indeterminate-cycle-duration: 5s;
      }
      paper-progress.blue {
        --paper-progress-active-color: var(--paper-light-blue-500);
        --paper-progress-secondary-color: var(--paper-light-blue-100);
      }
      paper-progress.red {
        --paper-progress-active-color: var(--paper-red-500);
        --paper-progress-secondary-color: var(--paper-red-100);
      }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->

The progress bars are for situations where the percentage completed can be
determined. They give users a quick sense of how much longer an operation
will take.

There is also a secondary progress which is useful for displaying intermediate
progress, such as the buffer level during a streaming playback progress bar.

See: [Documentation](https://www.webcomponents.org/element/@polymer/paper-progress),
  [Demo](https://www.webcomponents.org/element/@polymer/paper-progress/demo/demo/index.html).

## Usage

### Installation
```
npm install --save @polymer/paper-progress
```

### In an html file
```html
<html>
  <head>
    <script type="module">
      import '@polymer/paper-progress/paper-progress.js';
    </script>
  </head>
  <body>
    <paper-progress indeterminate class="blue"></paper-progress>
    <paper-progress indeterminate class="slow red"></paper-progress>
    <paper-progress value="40" secondary-progress="80"></paper-progress>
  </body>
</html>
```
### In a Polymer 3 element
```js
import {PolymerElement, html} from '@polymer/polymer';
import '@polymer/paper-progress/paper-progress.js';

class SampleElement extends PolymerElement {
  static get template() {
    return html`
      <paper-progress indeterminate class="blue"></paper-progress>
      <paper-progress indeterminate class="slow red"></paper-progress>
      <paper-progress value="40" secondary-progress="80"></paper-progress>
    `;
  }
}
customElements.define('sample-element', SampleElement);
```

## Contributing
If you want to send a PR to this element, here are
the instructions for running the tests and demo locally:

### Installation
```sh
git clone https://github.com/PolymerElements/paper-progress
cd paper-progress
npm install
npm install -g polymer-cli
```

### Running the demo locally
```sh
polymer serve --npm
open http://127.0.0.1:<port>/demo/
```

### Running the tests
```sh
polymer test --npm
```
