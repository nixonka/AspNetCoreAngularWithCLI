
# Asp Net Core Angular Template With Angular CLI

Created SPA app using Visual Studio 2017 and Asp Net Core Angular template. 


Updated all Angular packages
```
npm install @angular/common@latest @angular/compiler@latest @angular/compiler-cli@latest @angular/core@latest @angular/forms@latest @angular/http@latest @angular/platform-browser@latest @angular/platform-browser-dynamic@latest @angular/platform-server@latest @angular/router@latest @angular/animations@latest typescript@latest 
```


Add Angular CLI  package
```
npm install --save-dev @angular/cli@latest
```
in ```.angular-cli.json``` configuration file added
```
 {
   "$schema": "./node_modules/@angular/cli/lib/config/schema.json",
   "project": {
     "name": "AspNetCoreAngularWithCLI",
     "ejected": true
   },
   "apps": [
     {
       "root": "ClientApp"
     }
   ]
 }
```
IMPORTANT: ```"ejected": true```

Recompile 
```
webpack --config webpack.config.vendor.js 
```
(must have webpack installed globally: ```npm install -g webpack@latest```)



Replaced files manually in app.module:
```
import { HttpModule } from '@angular/http';
```
to 
```
import { HttpClientModule } from '@angular/common/http';
```
in services files instead of Http I've used HttpClient:
```
import { HttpClient } from '@angular/common/http'; 
```


Start application
```
dotnet restore
dotnet run
```


Add new component 
```
ng g component test-component --module=app.shared.module
```



