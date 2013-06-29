
# angular-dnd-directives

  Drag and drop attribute directives for Angular.js

## Installation

  Install with [component(1)](http://component.io):

    $ component install enome-component/angular-dnd-directives

## API

```html
<script src='https://ajax.googleapis.com/ajax/libs/angularjs/1.0.1/angular.js'></script>
<script>
  require('angular-dnd-directives');
  var module = angular.module('my-app', ['dnd-directives']);
  
  module.controller('Ctrl', function ($scope) {
    $scope.execute = function ($event, name) {
      $event.preventDefault();
      console.log(name, $event);
    };
  });
</script>

<div ng-controller='Ctrl'
      dragstart='execute($event, "dragstart")'
      dragend='execute($event, "dragend")'
      dragenter='execute($event, "dragenter")'
      dragover='execute($event, "dragover")'
      dragleave='execute($event, "dragleave")'
      drop='execute($event, "drop")'>

  Drag &amp; drop stuff here.

</div>
```

## License

  MIT
