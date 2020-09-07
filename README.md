# Initial page

teste

```javascript
// Simples

var inc = (x: number) => x + 1;

// Class

class Person {
	constructor(public age: number) {}
	growOld = () => {
		this.age++;
	};
}

var person = new Person(1);
setTimeout(person.growOld, 1000);

setTimeout(function () {
	console.log(person.age);
}, 2000);

```

