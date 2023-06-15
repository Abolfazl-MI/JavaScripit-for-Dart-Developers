# JavaScript For Dart developers

# JavaScript Variables

for defining variables in JavaScript we have `let` and `const` for variables. the ********let******** could change him values but ********************const********************  variables could not change and you could not assign value after definition 

## JavaScript Strings

you could define Strings in 3 way  "quotation", ‘quotation’,`quotation`

for string interpolation you should use `` with ${} pattern ,=> `Abolfazl ${variables}`  

## JavaScript Condition

the syntax of conditions in JavaScript is like this : `if(condition){}` , the else is like this `if(condition){}else{}` . the else if syntax is like this `if(condition){}else if(condition){}` .

## JavaScript comments

for commenting in JS we use `//` for commenting 

## JavaScript `null` and `undefined`

When we define a variable in JavaScript and do not assign a value, it is considered `undefined`. On the other hand, `null` is used to indicate that a variable has no value.

## JavaScript Logical operators

### JavaScript Logical Operators

JavaScript has three logical operators: `&&`, `||`, and `!`.

- The `&&` operator returns `true` if both operands are `true`, and `false` otherwise.
- The `||` operator returns `true` if at least one of the operands is `true`, and `false` otherwise.
- The `!` operator returns the opposite of the operand's boolean value (`true` becomes `false`, and `false` becomes `true`).

These operators are often used in conjunction with conditional statements to create more complex logic.

## JavaScript Math operators

### JavaScript Math Operators in Conditions

JavaScript has several math operators that can be used in conditions, including:

- `<`: less than
- `>`: greater than
- `<=`: less than or equal to
- `>=`: greater than or equal to
- `===`: equal to (compares value and type)
- `!==`: not equal to (compares value and type)

These operators can be used to compare variables or values in conditional statements. For example:

```
let x = 5;
if (x < 10) {
  console.log("x is less than 10");
}

```

In this example, the condition `x < 10` evaluates to `true`, so the code inside the `if` statement is executed and "x is less than 10" is logged to the console.

Note that the `===` and `!==` operators compare both the value **and** the type of the operands. This means that `"5" === 5` would evaluate to `false`, because the left operand is a string and the right operand is a number.

## JavaScript Functions

for creating functions in JavaScript we create it with `function` key word then the name of function , the functions could have inputs. the parameters could be the input of functions

```jsx
function sayHello(parameter){
	console.log(parameter);
}
```

### JavaScript value checking

for checking that value is exists or not we could use `!` operator in out code lets see example

```jsx
if(!user){
	// condition would excute if there is no user providede to us
}
```

for doing the if checking of available value we could also use this kind of checking 

```jsx
user=user||'empty state is valid';
```

here if user did not provided the value would be other string 

For checking if variables have  null or undefined  in JavaScript as we do in dart we could use ?? operator in our code , note that this just check if value is null or undefined   and it dose not do any more

```jsx
user=user??'the state is only valid when the user is null or undefinded'
```

### Experssion functions in JavaScript

the expersion functions are kind of functions which they could place in variables like this

```jsx
let myVar= function (){
	alert('my functuion')
}

sayHi();
```

if the () are not placed in-front of the function is like that it dos not run so we could run it by placing () in-front of the variable , the returned value from function would stored on the variables , and it could not before initializing usage 

### Arrow Functions in JavaScript

the arrow functions is like that experssion functions in js but the way of implementing is different . like this. 

```jsx
let myFunction=(param,param2)=>{
	console.log()
}
```

## Array in JavaScript

for defining Arrays in Js we could use `let` or `const` like this 

```jsx
let users=[];
const podcasts=[];
```

### if we want to add one value to arrays we use `push` method

```jsx
let users=[];
users.push('abolfazl')
```

### if we want to remove one index before from array we use `pop`

```jsx
let users=['abolfazl','mostafa']
user.pop()
// result => ['abolfazl']
```

### if we want to remove one from first index we use `shift`

```jsx
let users=['abolfazl','mostafa']
users.shift()
// users =>['mostafa']
```

### if we want to add value to first index of arrays we use `unShift` method

```jsx
let users=['abolfazl','mostafa']
users.unshift('asma')
//result=>['asma','abolfazl','mostafa']
```

<aside>
💡 Const arrays could not modify by all , but you could modify the index

</aside>

### Loops and For loops in List

for creating loops inside the the `Arrays` in JavaScript  in normal way we could do this way.

```jsx
let users=['abolfazl','mostafa'];
for(let user of users){
	console.log(user);
}

for(let i=0;i<users.length;i++){
	console.log(users[i]);
}

```

but there is other `for` in JavaScript called `for of` that is common in any programming language.

 

### `for...of` and `for...in` loops in JavaScript

`for...of` and `for...in` are two types of loops used in JavaScript to iterate over collections such as arrays and objects.

### `for...of` loop

The `for...of` loop allows you to iterate over the values in an array or other iterable object. It has the following syntax:

```jsx
for (let value of iterable) {
  // code to execute for each value
}

```

Here, `iterable` is the collection of values you want to iterate over, and `value` is a variable that will be assigned to each value in turn. The loop will execute once for each value in the iterable.

For example, the following code uses a `for...of` loop to log each value in an array to the console:

```jsx
let numbers = [1, 2, 3];
for (let number of numbers) {
  console.log(number);
}
// Output:
// 1
// 2
// 3

```

### `for...in` loop

The `for...in` loop allows you to iterate over the properties of an object. It has the following syntax:

```
for (let property in object) {
  // code to execute for each property
}

```

Here, `object` is the object whose properties you want to iterate over, and `property` is a variable that will be assigned to each property in turn. The loop will execute once for each property in the object.

For example, the following code uses a `for...in` loop to log each property of an object to the console:

```
let person = { name: "Alice", age: 30 };
for (let property in person) {
  console.log(property + ": " + person[property]);
}
// Output:
// name: Alice
// age: 30

```

Note that the order in which properties are iterated over is not guaranteed to be the same as the order in which they were defined in the object. If you need to iterate over properties in a specific order, you should use an array instead.

### `Splice` in `Array`

The `splice()` method in JavaScript is used to add or remove items from an array at a specific index. It takes in two required arguments: the starting index and the number of items to remove. It can also take in additional arguments to specify items to add to the array at the specified index. If no items are specified to add, `splice()` will simply remove the items specified by the starting index and number of items to remove.

Example of using the `splice()` method:

```
let numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 1); // remove the third item (index 2)
// numbers is now [1, 2, 4, 5]

numbers.splice(1, 0, 6, 7); // add two items (6, 7) at index 1
// numbers is now [1, 6, 7, 2, 4, 5]

```

for adding value with `splice`  method  first we say which index we want to insert inside `(1)`

then we say how many to remove `(1,0)` then we  specify the items which we want to add `(1,0,6,7)` . For removing that we just specify the `index` where to start then we specify `how many we want to remove` 

### `forEach` method in `Arrays`

The `forEach()` method in JavaScript is used to iterate over an array and execute a function for each element. It takes in a single argument, which is a function to execute for each element of the array. The function takes in three arguments: the current element, the index of the current element, and the array being iterated over.

Here is an example of using the `forEach()` method to log each element of an array to the console:

```
let numbers = [1, 2, 3];
numbers.forEach(function(number) {
  console.log(number);
});
// Output:
// 1
// 2
// 3

```

In this example, the `forEach()` method is called on the `numbers` array and passed a function that logs each element to the console. The function takes a single parameter, `number`, which represents the current element of the array being iterated over.

Note that the `forEach()` method does not modify the original array. If you need to modify the array, you should use a different method, such as `map()` or `filter()`.

### `Find` method of `Array` in js

For finding specific item in list in js we could use `find` method like this , if not find would return `undefinded` , if there is multiply items in list it would return the first item

```jsx
let users=['abolfazl','mostafa','reza']
let user=users.find((item)=>{
	if(item =='abolfazl'){
	return item
	}
})
let user=users.find(item=>item=='abolfazl');
```

### `Filter` method of `Array` in JS

The filter method used for getting items with the some shared things in Array. this method is like the `where` method of dart `Arrays` which you could create a list of items with specified item.

Here is an example of using the `filter()` method to create a new array of numbers greater than 3:

```
let numbers = [1, 2, 3, 4, 5];
let filteredNumbers = numbers.filter(function(number) {
  return number > 3;
});
// filteredNumbers is now [4, 5]

```

In this example, the `filter()` method is called on the `numbers` array and passed a function that returns `true` if the current element is greater than 3. The method returns a new array containing only the elements that meet the condition.

Note that the `filter()` method does not modify the original array. If you need to modify the array, you should use a different method, such as `map()` or `splice()`.

### `Include` method in Js

To search for and determine if a specific item is available in a list, you can use the `includes` method. it like the `contains` method of Dart. 

```jsx
const skills=['nodeJs','Mongo','Dart']
const hasNodeJs=skills.includes('nodeJs')
// result => true
```

### `Some` method of `Array` in Js

This method returns true if there are any available matched items, else it returns false.  this  method is flexible  for making condition for items

```jsx
const skills=['nodeJs','dart','flutter']
const available=skills.some(item=>item=='nodeJs')
```

### `Every` method of `Array` in Js

This method returns true if every item of Array match the condition we determine for it 

```jsx
const skill=['js','dart','htm','web'];
const everyItem=skill.every(item=>item=='js')// fales
const isNotEmptyArray=skill.every(item=>item.lenght>2)//true
```

### `FindIndex` method of `Array` in Js

This method returns the index of element in array , this method is similar to `indexOf` method in dart. and we could make condition for it  

```jsx
const skills=['js','dart','pythond','flutter']
const indexOfJs=skills.findIndex(item=>item=='js')//0
```

### `Map` method of `Array` in Js

This method is both important and useful. If you want to create a new `Array` from an existing `Array` without changing the default values, you can use `map()`. This is similar to Dart's `map` function.

```jsx
const numbers=[1,2,3,4,5]
const doubledNumber=numbers.map((item)=>item*2)// [2,4,6,8,10]
```