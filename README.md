**An object is used to represent a specific entity, through an aggregation of data and functionalities.**

# **Objects**

## **Object Literal notation**
```javascript
var emptyObject = {};
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
person.greet = function(){
    return 'Hello there!'
}

var name = person.name
var surname = person["middle-name"]
```

## **Object properties**

```javascript
var obj = {}
Object.defineproperty(obj, 'attrib', 
{
    value: 42,
    writable: true,
    configurable: false //attrib cannot be deleted})
})

delete obj.attrib; //doesn't work
```

## **Methods** ##

```javascript
var person = {
    name: "John",
    "surname": "Smith"
}

function showFullName(){
    return 'John Smith';
}

person.fullName = showFullName;
```