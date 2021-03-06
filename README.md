# very.js

very is a micro-library (< 1kb minified) for wiring events to elements.

## API Reference

very takes two arguments - an object and an element - and defines event listeners on elements
by defining functions on the object using the format `onX`.

```js
var element = document.createElement('div');

var object = {
  onClick (event) {
    // do something on click
  },

  onMouseMove (event) {
    // do something on mouse move
  }

  // ...
};

// function returns a callback the remove all event bindings when executed
var callback = very(object, element);

// unbind all events
callback();
```

## Supported Events

The follow is the list of supported events:

```
'Abort', 'Blur', 'CanPlay', 'CanPlayThrough', 'Change', 'Click', 'ContextMenu',
'Copy', 'CueChange', 'Cut', 'DblClick', 'Drag', 'DragEnd', 'DragEnter',
'DragLeave', 'DragOver', 'DragStart', 'Drop', 'DurationChange', 'Emptied',
'Ended', 'Error', 'Focus', 'Input', 'Invalid', 'KeyDown', 'KeyPress', 'KeyUp',
'LoadedData', 'LoadedMetaData', 'LoadStart', 'MouseDown', 'MouseMove', 'MouseOut',
'MouseOver', 'MouseUp', 'Paste', 'Pause', 'Play', 'Playing', 'Progress',
'RateChange', 'Reset', 'Scroll', 'Search', 'Seeked', 'Seeking', 'Select', 'Show',
'Stalled', 'Submit', 'Suspend', 'TimeUpdate', 'Toggle', VolumeChange', 'Waiting',
'Wheel'
```
