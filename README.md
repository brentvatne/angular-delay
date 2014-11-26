# angular-delay

Delay execution of a ngChange callback. All credit goes to "Doug R" from
[this StackOverflow discussion](http://stackoverflow.com/a/21420441).

### Installing

`bower install angular-delay`

### Using

Include the package in your application:

```javascript
angular.module('app', ['ngDelay']);
```

```html
<input ng-model="search" ng-change="updateResults()" ng-delay="1500" />
```

This waits 1.5 seconds after the search has been changed before
performing the `ng-change` callback.

### Deprecated in Angular 1.3.x

This is useful for Angular 1.2.x, but it is deprecated with Angular 1.3.x with the introduction of `ng-model-options` where you can now just do the following to have the same effect as `ng-delay="1500"`

```html
  <input ng-model="search" ng-model-options="{debounce: 1500}" />
```

Read more about [ng-model-options in the Angular docs](https://docs.angularjs.org/api/ng/directive/ngModelOptions).
