# AngularJS snippets for vim #

- [Module](#module)
- [Controller](#controller)
- [Filter](#filter)
- [Service](#service)
- [Back to main page](../README.md)

### Module ###

`ngmodule`

```js
angular

.module('module_name', [

])

;
```

`ngconfig`

```js
.config([

  function() {

  }
])
```

`ngrun`

```js
.run([

  function() {

  }
])
```
### Controller ###

`ngcontroller`

```js
angular

.module('module_name')

.controller('controller_name', [
  '$scope',
  function($scope) {

  }
]);
```

`ngcontrollertest`

```js
describe('controller_name controller', function() {
  beforeEach(module('module_name'));

  var $controller;
  var $rootScope;

  var scope;
  var controller;

  beforeEach(inject(function($injector) {
    $controller = $injector.get('$controller');
    $rootScope = $injector.get('$rootScope');

    scope = $rootScope.$new();
    controller = $controller('controller_name', {
      $scope: scope
    });
  }));

  describe('', function() {
    it('', function() {

    });
  });
});
```

### Filter ###

`ngfilter`

```js
angular

.module('module_name')

.filter('filter_name', [

  function() {
    return function(input) {

    };
  }
]);
```

`ngfiltertest`

```js
describe('filter_name filter', function() {
  beforeEach(module('module_name'));

  var $filter;
  var filter;

  beforeEach(inject(function($injector) {
    $filter = $injector.get('$filter');
    filter = $filter('filter_name');
  }));

  describe('', function() {
    it('', function() {

    });
  });
});
```

### Service ###

`ngservice`

```js
angular

.module('module_name')

.service('service_name', [
  'dependency',
  function(dependency) {
    this.testMethod = function() {

    };
  }
]);
```

`ngfactory`

```js
angular

.module('module_name')

.factory('factory_name', [
  'dependency',
  function(dependency) {
    var api = {};

    api.testMethod = function() {

    };

    return api;
  }
]);
```

`ngservicetest`

```js
describe('service_name service', function() {
  beforeEach(module('module_name'));

  beforeEach(inject(function($injector) {

  }));

  describe('', function() {
    it('', function() {

    });
  });
});
```
