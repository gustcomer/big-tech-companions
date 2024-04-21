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

### Currying

multiply() function written in the traditional way
```javascript
function multiply(x, y, z) {
    return x * y * z;
}
```

multiply() function written with Currying.
```javascript
function multiply(x) {
    return function(y) {
        return function(z) {
            return x * y * z;
        }
    }
}
```

Currying helps in scenarios where you might want to reuse the function with some specific parameter.
```javascript
// All at once
console.log(multiply(2)(3)(4)); // Output: 24

// Step by step
const multiplyByTwo = multiply(2);
const multiplyBySix = multiplyByTwo(3);
console.log(multiplyBySix(4)); // Output: 24
```