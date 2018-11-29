## In order to Create an Angular 7 project using Net Core 2.1 as back-end follow theese steps:

* Update SPA Net Templates:
dotnet new --install Microsoft.AspNetCore.SpaTemplates::*

* Create the Project
dotnet new angular -o angular7core2test

* Open the project file (csproj) with Visual Studio and Save the Solution

* Modify package.json:
Remove "--extract-css" because it's now defined in "angular.json" -> "extractCss": true,
"start": "ng serve",
"build": "ng build",

* Update Angular Version to latest (command line on ClientApp folder):
ncu -u
npm install

* Update to "angular.json" -> Migration -.angular-cli.json to angular.json (command line on ClientApp folder):
ng update @angular/cli

* Fix audit: npm audit fix

* Modify "again" package.json to this version of bootstrap:
"bootstrap": "3.3.7"

* If publishing on IIS modify angular.json adding:
"baseHref": "/Angular5Core2/"
