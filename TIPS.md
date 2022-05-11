# Installing Bootstrap for Angular with npm
After install it, the **angular.json** file must be modified:
1. In the file, find the "architect" section --> build --> styles and scripts
2. In the styles object, include the path to the bootstrap.min.css:
    "./node_modules/bootstrap/dist/css/bootstrap.min.css"
3. In the scripts object, include the paths for bootstrap, popper and jquery JS files:
    "./node_modules/bootstrap/dist/js/bootstrap.min.js",
    "./node_modules/popper/index.css",
    "./node_modules/jquery/dist/jquery.min.js"

# Installing Ramda for Angular with npm
https://material.angular.io/

```
npm i @types/ramda ramda --save
```

# Installing Material in Angular
- Using ng command:
```
ng add @angular/material
```

## Creating a custom material module
```
ng generate module app-material
```

Import Material component modules in this new AppMaterialModule. Note that we also need to put the same list of modules in NgModule.exports too.
```
...
@NgModule({
  imports: [
    CommonModule,
    MatInputModule,
    MatButtonModule
  ],
  exports: [
    MatInputModule,
    MatButtonModule
  ]
})
export class AppMaterialModule { }
```

Then in our **AppModule**, we can import on **AppMaterialModule**.