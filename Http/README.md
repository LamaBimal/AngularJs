# Methods

The example above uses the .get method of the $http service.

The .get method is a shortcut method of the $http service. There are several shortcut methods:

- .delete()
- .get()
- .head()
- .jsonp()
- .patch()
- .post()
- .put()
The methods above are all shortcuts of calling the $http service:

Basic Example
```HTML
<div ng-app="myApp" ng-controller="myCtrl"> 

<p>Today's welcome message is:</p>
<h1>{{myWelcome}}</h1>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope, $http) {
  $http.get("welcome.htm")
  .then(function(response) {
    $scope.myWelcome = response.data;
  });
});
</script>
```
