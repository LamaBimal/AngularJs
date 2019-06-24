# ngRoute

If you want to navigate to different pages in your application, but you also want the application to be a SPA (Single Page Application), with no page reloading, you can use the ngRoute module.

The ngRoute module routes your application to different pages without reloading the entire application.

To make your applications ready for routing, you must include the AngularJS Route module:
```
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular-route.js"></script>
```
Then you must add the **ngRoute** as a dependency in the application module:
```
var app = angular.module("myApp", ["ngRoute"]);
```
Now your application has access to the route module, which provides the $routeProvider.

Use the $routeProvider to configure different routes in your application:
```
app.config(function($routeProvider) {
  $routeProvider
  .when("/", {
    templateUrl : "main.htm"
  })
  .when("/red", {
    templateUrl : "red.htm"
  })
  .when("/green", {
    templateUrl : "green.htm"
  })
  .when("/blue", {
    templateUrl : "blue.htm"
  });
});
```
Where Does it Go?
Your application needs a container to put the content provided by the routing.

This container is the ng-view directive.

There are three different ways to include the ng-view directive in your application:

Example:
```HTML
<div ng-view></div>
```
Example:
```HTML
<ng-view></ng-view>
```
Example:
```HTML
<div class="ng-view"></div>
```
Applications can only have one ng-view directive, and this will be the placeholder for all views provided by the route.

#### $routeProvider
With the $routeProvider you can define what page to display when a user clicks a link.
