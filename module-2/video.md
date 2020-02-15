destruction syntax: ...args => to get all arguments into array
parseFloat(value) or parseInt(value) is better than +value

localeCompare - compare two letters according to locale alphabet

the only value in JS that isn't equal to itself in NaN

Function types in JS
- function declaration
- function expression

// declaration
const foo = function () {
	return 'foo';
}

// declaration
function foo () {
	return 1;
}

// arrow function
const foo = () => {} - doesn't have this?, doesn't have arguments
const sum = a => b => a + b
sum(1)(2)

// closure
function makeCounter() {
	let count = 0;

	return function () {
		return count++;
	}
}

const counter = makeCounter();

counter() => 0
counter() => 1
etc.

Code quality - do not write functions with >3 params, better use the object

Arrays
array.length = last index + 1

array.pop() / array.shift() / array.unshift() / array.push()

Iterations:
- array.forEach()
- for (let item of array) {} - iterates only over own properties
- for (let index in array) {} - iterates over inherited properties, need to check for own properties
- array.map()
- array.reduce()
- array.sort() - mutates array
- array.slice().sort() - doesn't mutate array

function foo() {
	console.log(Array.isArray(arguments)) // false - pseudo-array
}

elements = document.getElementsByTagName() -> returns HTMLCollection
Array.from(elements)
[...elements]

array,slice() / Array.from() - shallow copy
array.map(item => ({...item})) - one level deep copy
array.map(item => Object.assign({}, item))
