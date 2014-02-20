*This repository is a mirror of the [component](http://component.io) module [component/selectable](http://github.com/component/selectable). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-selectable`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# selectable

  Selectable DOM elements.

  ![dom element selection js component](http://i.cloudup.com/iZqb9fzgccE.png)

## Installation

    $ component install component/selectable

## Example

```html
<ul id="pets">
  <li data-name="tobi">Tobi</li>
  <li data-name="loki">Loki</li>
  <li data-name="jane">Jane</li>
  <li data-name="abby">Abby</li>
</ul>

<script>
  var selectable = require('selectable');
  var selection = selectable('#pets > li');

  selection.on('change', function(e){
    for (var i = 0; i < e.selected.length; i++) {
      console.log(e.selected[i].getAttribute('data-name'));
    }
  });
</script>
```

## API

### Selectable(selector, el)

  Make elements with the given `selector` selectable, with optional context `el`.

### Selectable#select(els)

  Add the given `els` to the selection.

### Selectable#deselect(els)

  Remove the given `els` from the selection.

## License

  MIT
