# Javascript Snippets

### Arrow functions

```javascript
const hello = () => {
  return "Hello World!";
}
```

### bind() function

The member object borrows the fullname method from person:

```javascript
const person = {
  firstName:"John",
  lastName: "Doe",
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}

const member = {
  firstName:"Hege",
  lastName: "Nilsen",
}

let fullName = person.fullName.bind(member);
```

### splice() method

Adds and/or removes array elements. Also it overwrites the original array.

```javascript
let x = [1,3,5,2,4]

x.splice(2,1) // removes one element from index 2
x.splice(3,0,8) // insert number 8 at third index
x.splice(3,0,[10,20,30]) // insert 10, 20 and 30 at index 3
```