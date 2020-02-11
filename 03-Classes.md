# **Classes**
```javascript
class Person{

    constructor(name, surname){
        this.name = name;
        this.surname = surname;
    }

    displayFullName(){
        return this.name + " " + this.surname;
    }
}
var Person = class{
    //descriptions
}
var johnSmith = new Person("John","Smith")
johnSmith.displayFullName()
```

The capability to model a problem through objects and relationships among objects

Association

relationship between two or more objects is independent of the others

```javascript
function Person(name, surname){
    this.name = name;
    this.surname = surname;
    this.parent = null;
}
var johnSmith = new Person("John", "Smith");
var fredSmith = new Person("Fred", "Smith");
fredSmith.parent = johnSmith
```

Aggregation
special form of association relationship where an object has a more important role than the others:
```javascript
function Person(name, surname){
    this.name = name;
    this.surname = surname;
    this.parent = null;
}
var company = {
    name: "ACME Inc.",
    employees: []
};
var johnSmith = new Person("John", "Smith");
var fredSmith = new Person("Fred", "Smith");
company.employees.push(johnSmith);
company.employees.push(fredSmith);
```
Compositions
strong type of aggreation, where each component object has no independent life without its owner

```javascript
var person = {
    name: "John",
    "surname": "Smith"
    "middle-name": "Ian"
    address: {
        street: "13 Duncannon Street",
        city: "london"
        country: "United Kingdom"
    }
}
```

address cannot exist without person

The encapsulation principle allows an object to expose just what is needed to use it, hiding the complexity of its implementation

```javascript
function Company(name) {
    var employees = [];
    this.name = name;
    this.getEmployee = function(){
        return employees;
    }
    this.addEmployee = function(employee){
        employees.push(employee)
    };
    this.sortEmployeesByName = function(){
        //...
    }
}

var company = new Company("Acme Inc.")
```

# ** Inheritance **
```javascript
function Person(name, surname) {
    this.name = name;
    this.surname = surname;
}
function Programmer(knownLanguage){
    this.knownLanguage = knownLanguage;
}
Programmer.prototype = new Person();
var programmer = new Programmer("Java Script");
```

# **Polymorhism**
overloading

```javascript
//ES5
function Sum(x,y,z){
    x = x ? x : 0;
    y = y ? y : 0;
    z = z ? z : 0;
    return x + y + z;
}
//ES6
function Sum(x = 0, y = 0, z = 0){
    retun x + y + z;
}
```

no classical inheritace , but Prototypal inheritance is an operation on object

Prototypal Object Oriented 

