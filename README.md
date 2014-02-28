requirejs-link
==============

RequireJS plugin to insert LINK element on DOM, work with CSS and HTMLImport

It will return the reference from the created element, as default it append on the head, but you can remove
from the DOM at anytime or even append it again using the reference from the element.

Easy to use:
------------

You just need to execute the plugin and add the full file path with extension.

```define([link!mystyle.css], function (styleElement) {
  console.log(styleElement.parentElement); // document.head
    
  // Removing example:
  styleElement.parentElement.removeChild(styleElement);
    
  // Addeding again to DOM:
  document.head.appendChild(styleElement);
});```

You also can use with HTMLImports, if the browser support, or if you are using Polymer-project or other shim.

```define([link!my-web-component.html], function (wcElement) {
  console.log(wcElement); // HTMLLinkELement for the imported web-component
});```
