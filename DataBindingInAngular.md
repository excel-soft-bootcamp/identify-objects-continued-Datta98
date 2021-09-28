# Data Binding in Angular
- Data binding in angular deals with how to bind your data from component to HTML DOM elements (Templates).
### Types of Data Binding in Angular
- One-way Data Binding
  - String Interpolation
  - Property Binding
  - Event Binding
  - Class Binding
- Two-way Data Binding

### One-way Data Binding
- One-way data binding is a one-way interaction between component and its template. If you perform any changes in your component, then it will reflect the HTML elements.
- It supports the following types −<br>
#### 1. String Interpolation
-  String interpolation is the process of formatting or manipulating strings. In Angular, Interpolation is used to display data from component to view (DOM). It is denoted by the expression of {{ }}.
```C# 
// Syntax
// databinding.component.ts
 export class DataBindingComponent {
    appName = "My name is Shridatta ";   
}
// databinding.component.html
 <h1>{{appName}}</h1>
```
#### 2. Property Binding
- Property binding is used to bind the data from property of a component to DOM elements. It is denoted by [ ].
```C# 
// Syntax
// databinding.component.ts
 export class DataBindingComponent {
    userName:string = "ShriDatta";  
}
// databinding.component.html
<input type="text" [value]="userName">
```
#### 3. Event Binding
- Events are actions like mouse click, double click, hover or any keyboard and mouse actions. If a user interacts with an application and performs some actions, then event will be raised. It is denoted by  parenthesis ( ).
```C# 
// Syntax
// databinding.component.ts
 export class DataBindingComponent {
   myname:string="";
    onShow()
        {
           this.myname = "Excelsof"; //Event Binding
    }  
}
// databinding.component.html
<div>
    <button (click)="onShow()">Company</button>
    <h3>{{myname}}</h3>
</div>
```
#### 4. Class Binding
- Class binding is used to bind the data from component to HTML class property.
```C# 
// Syntax
// databinding.component.ts
 export class DataBindingComponent {
   myCSSClass = "red"; 
}
// databinding.component.html
<p [class]="myCSSClass">This paragraph class comes from *myCSSClass* property </p>
// databinding.component.css
.red { 
    color: red; 
 }
```
### Two-way Data Binding
- Two-way data binding is a two-way interaction, data flows in both ways (from component to views and views to component).
- If you do any changes in your property (or model) then, it reflects in your view and vice versa.
- To impliment Two-way Data Binding we use ngModel directive.
- NgModel is a standalone directive. ngModel directive binds form control to property and property to form control.
- So Configure FormsModule in AppModule
```C# 
// app.module.ts
import { FormsModule } from '@angular/forms'; 
@NgModule({
    declarations:[DataBindingComponent],
    imports:[BrowserModule,FormsModule],
    bootstrap:[DataBindingComponent],
    exports:[]
})
export class AppModule{

}
```
```C# 
// Syntax
// databinding.component.ts
 export class DataBindingComponent {
    userName:string = "ShriDatta";  
}
// databinding.component.html
  <input type="text" [(ngModel)]="userName" >
<p>Two way binding! Hello {{ userName }}!</p>
```
