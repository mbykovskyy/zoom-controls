# zoom-controls
[Polymer][polymer] web component providing generic zooming in and out controls.

## Install

```bash
bower install --save mbykovskyy/zoom-controls
```

## Usage

```html
<link rel="import" href="zoom-controls.html">

<zoom-controls id="zoom_controls"></zoom-controls>
<div id="box"></div>

<script>
  document.addEventListener('polymer-ready', function() {
    var zoomControls = document.getElementById('zoom_controls');
    var box = document.getElementById('box');

    box.style.transformOrigin = '0 0';
    box.style.transform = 'scale(' + zoomControls.zoom +')';

    zoomControls.addEventListener('zoom', function() {
      box.style.transform = 'scale(' + zoomControls.zoom +')';
    });
  });
</script>
```

See [component page][zoom-controls] for details and demo.

[polymer]: http://polymer-project.org "Polymer"
[zoom-controls]: http://mbykovskyy.github.io/zoom-controls "Component Page"
