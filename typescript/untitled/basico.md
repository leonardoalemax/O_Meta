# Basico

Tipos podem ser implícitos ou explícitos

```typescript
// implicito:
var foo = 123;
foo = "123"; # will get error

// explicito:
var foo: string = "123";
```

Types são estruturais 

```typescript
interface Dot {
	x: number;
	y: number;
}

interface Voxel {
	x: number;
	y: number;
	z: number;
}

var dot: Dot = { x: 0, y: 10 };
var voxel: Voxel = { x: 0, y: 10, z: 20 };

function iTakeDot(dot: Dot) {
	console.log(dot);
}

iTakeDot(dot); // exact match okay
iTakeDot(voxel); // extra information okay
iTakeDot({ x: 0 }); // Error: missing information `y`
```

