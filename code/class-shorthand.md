### Shorthand

```typescript
class Greeter {
  constructor(public greeting: string) {
  }
  greet() {
      return "Hello, " + this.greeting;
  }
}

let greeter = new Greeter("world");
```