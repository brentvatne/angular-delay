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
