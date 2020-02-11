# **Contructor Function**

```javascript

function Person(name, surnamve){
    this.name = name,
    this.surname = surname
    this.displayFullName = function(){
        return this.name + " " + this.surname;
    }
}

var johnSmith = new Person("John", "Smith");

```

# **Generic Object**

```javascript
var person = new Object();
person.name = "John";
perosn.surname = "Smith";

var number = new Object(12);
var string = new Object("test");
var anotherNumber = new Object(3*2);
var person = new Object({name: "John", surname: "Smith"});

//built in object constructor
```

Using Object Prototypes

