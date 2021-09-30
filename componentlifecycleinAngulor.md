#	Life Cycle Of Angular Components
- In Angular, every component has a life-cycle, a number of different stages it goes through from initializing to destroying.
- There are 8 different stages in the component lifecycle. Every stage is called  life cycle hook events.
- The constructor of the component class executes first before the execution of any other life cycle hook event.
- Angular executes its life cycle hook methods in a specific order.

### 1) ngOnChanges
- This event executes every time when a value of an input control within the component has been changed.
- This event fires first when a value of a bound property has been changed.
### 2) ngOnInit
- This event initializes after angular first displays the data-bound properties or when the component has been initialized.
- This event is mainly used for initializing data in a component.
### 3) ngDoCheck
- This event is triggered every time when the input properties of a component are checked.
- We can use this hook method to implement the check with our own logic check.
- Basically, this method allows us to implement our own custom change detection logic or algorithm for any component.
### 4) ngAfterContentInit
- This lifecycle method is executed when Angular performs any content projection within the component views.
- This event executes just after the ngDoCheck() method. 
- This method is basically linked with the child component initializations.
### 5) ngAfterContentChecked
- This lifecycle hook method executes every time when the content of the component has been checked by the change detection mechanism of the Angular.
- This method called after ngAfterContentInit() method.
- This method is also called on every subsequent execution of ngDoCheck(). 
### 6) ngAfterViewInit
- This lifecycle hook method executes when the component’s view has been fully initialized. 
- It is called only the first time after ngAfterContentChecked(). 
### 7) ngAfterViewChecked
- It is executed every time the when the view of the given component has been checked by the change detection algorithm of Angular. 
- This method also executes when any binding of the children directives has been changed.
- This method is very useful when the component waits for some value which is coming from its child components.
### 8) ngOnDestroy
- This method will be executed just before Angular destroys the components.
- This method is very useful for unsubscribing the observables and detaching the event handlers to avoid memory leaks.
- This method called only once just before the component is removed from the DOM.
