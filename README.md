JSON Server Mock Authentication Services
============

## Installation

### Bower Installation
```sh
$ bower install --save angular-cookies
```

## Usage
- Include `json-server-auth` into your app index.html
- Include `json-server-users` if you need to add or edit users

```html

        <script src="/bower_components/angular/angular.min.js"></script>
        <script src="/bower_components/angular-cookies/angular-cookies.min.js"></script>
        <script src="/js/users/index.js"></script>
        <script src="/js/users/users.constants.js"></script>
        <script src="/js/users/users.service.js"></script>
        <script src="/js/auth/index.js"></script>
        <script src="/js/auth/auth.service.js"></script>
        <script type="text/javascript">
            var app = angular.module('app', ['json-server-auth', 'json-server-users']);
        </script>
```

```
AuthenticationService.Login(username, password).then(function(){
    //DO something
})
```
```
AuthenticationService.Logout().then(function(){
    //DO something
})
```
```
if(AuthenticationService.isLoggedIn()){
    //DO something
}
```
```
var loggedInUser = AuthenticationService.getCurrentUser();
```

## Techniques for protecting routes
- [medium.com](https://medium.com/opinionated-angularjs/techniques-for-authentication-in-angularjs-applications-7bbf0346acec#.k2s3uzjad)
- [blog.brunoscopelliti.com](http://blog.brunoscopelliti.com/deal-with-users-authentication-in-an-angularjs-web-app/)
- [youtube.com](https://www.youtube.com/watch?v=Q5iQk0OuDus)