# paret
A function to paste HTML at the current caret for contenteditable elements

## Parameters

### html (String)

html accepts a string containing html, I have encountered no limitations with this, thus far. Create an issue if you notice something.

### selectPastedContent (Boolean)

selectPastedContent accepts true, or false
  - `true` means that the content of the `html` parameter will be selected post-paste.
  - `false` means that it won't do that.
  
  
## How to

#### html
```html
<div id="editor" contenteditable="true" style="width: 60vw;text-align: left;">
  <p>That though the radiance which was once so bright</p>
  <p>be now forever taken from my sight.</p>
  <p>Though nothing can bring back the hour of splendor in the grass, </p>
  <p>glory in the flower. </p>
  <p>We will grieve not, </p>
  <p>rather find strength in what remains behind.</p>
</div>
```

#### javascript
```javascript
const paret = require('paret');
document.querySelector('#editor').onfocus = function(event){
  paret(`<footer style="text-align: right;"> <p> - <i>William Wordsworth</i></p> </footer>`, false);
}
```
