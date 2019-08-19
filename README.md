# common-dom-utils
Common DOM util functions.

Supporting types and tree shaking with webpack.

## Contents
1. [load js script in to container](load-js-script-into-DOM-container)
1. [load css file into DOM container](load-css-file-into-DOM-container)
1. [load css string into DOM container](load-css-string-into-DOM-container)
1. [load js scripts series into DOM container](load-js-scripts-series-into-DOM-container)

### load js script into DOM container
Load js script file into DOM.
```
import { loadScript } from 'common-dom-utils';

loadScript('https://script-url.com/script.js').then(
  () => { console.log('Script loaded') },
  (e) => { conole.log(e) }
);
```

parameters:
- src: javascript file url
- container: DOM element that \<script\> tag is inserted into, default: document.head

### load js scripts series into DOM container
Load js script file into DOM.
```
import { loadScriptsSeries } from 'common-dom-utils';

loadScriptsSeries([
  'https://script-url.com/script1.js',
  'https://script-url.com/script1.js'
]).then(
  () => { console.log('Scripts loaded') },
  (e) => { conole.log(e) }
);
```

parameters:
- src: javascript file url
- container: DOM element that \<script\> tag is inserted into, default: document.head


### load css file into DOM container
Load css file into DOM.
```
import { loadCssFile } from 'common-dom-utils';

loadCssFile('https://css-file-url/file.css');
```

parameters:
- cssFileUrl: css file url
- container: DOM element that \<link\> tag is inserted into, default: document.head

### load css string into DOM container
Load css string into DOM.
```
import { addCssString } from 'common-dom-utils';

addCssString('*, *:before, *:after { box-sizing: border-box;}');
```

parameters:
- cssString: css string
- container: DOM element that \<style\> tag is inserted into, default: document.head
- before: insert \<style\> tag before all other children, default: false

