openseadragon-iip-connector
===========================

This connector allows seamless integration with OpenSeaDragon and images served via IIPImage using DeepZoom.

To add an OpenSeaDragon viewer, simply include JQuery, OpenSeaDragon and this connector, and add **img** elements with the class *osd-iip*, for example:

```html
<script src="http://code.jquery.com/jquery-1.11.0.min.js"></script>
<script src="/path/to/openseadragon/openseadragon.min.js"></script>
<script src="/path/to/js/osd-iip-connector.js"></script>

<img src="/iip/iipsrv.fcgi?FIF=jp2/PR311_01_14.jp2&CVT=JPG" height="200" width="300"  id="image_one" class="osd-iip another_class">
```

Things to note:

 - All **img** elements with the *osd-iip* class will be converted to OpenSeaDragon viewers.
 - The OpenSeaDragon viewers will have the same ID and classes as the original **img** elements they replaced.
 - OpenSeaDragon *requires* a height attribute. This can be provided via CSS, although if any *height* or *width* attributes exist on the **img** element, these will be applied to the OpenSeaDragon viewer.
 - Set the **img** *src* attribure to an IIPImage URL with no height or width parameters. As a rule of thumb - when pasted into the address bar, the image URL should show the full size image.
 -OpenSeaDragon is finiky about where its own image resources are located. This script assumes that the OpenSeaDragon provided "images" folder is in the same folder on your web server as either *openseadragon.js* or *openseadragon.min.js* - whichever you choose to use.
