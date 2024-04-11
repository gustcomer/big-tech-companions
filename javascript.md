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