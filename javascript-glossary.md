# Javascript Glossary

* [Arrow functions](javascript.md#arrow-functions): don't have their own bindings to this, arguments, or super, and should not be used as methods.
    * test
* [Bind()](javascript.md#bind-function): an object can borrow a method from another object.
* [Binding]():
* [Destructuring]():
* Global Object: object that always exists in the global scope.
    * web browsers have a Window as its global object.
    * globalThis allows one to access the global object regardless of the current environment.
* Hoist: a variable can be used before it has been declared. It is the default behavior of moving all declarations to the top of the current scope.
* [Rest operator]():
* [splice](javascript.md#splice-method): adds and/or removes array elements. Also it overwrites the original array.
    * array.splice(index, howmany, item1, ....., itemX)
    * index: position to add or remove items; howmany: number of items to be removed. item1, ..., itemX: new elements(s) to be added.
* this: keyword that refers to an object.
    * In an object method, this refers to the object.
    * Alone, this refers to the global object.
    * In a function, this refers to the global object.
    * In a function, in strict mode, this is undefined.
    * In an event, this refers to the element that received the event.
    * Methods like call(), apply(), and bind() can refer this to any object.