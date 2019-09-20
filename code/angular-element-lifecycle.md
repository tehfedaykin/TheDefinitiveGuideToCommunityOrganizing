### Angular Element Lifecycle Hooks

```typescript
class RandomQueenGenerator extends HTMLElement {
  connectedCallback() {
    //fires when element is added to DOM
  }
  disconnectedCallback()
  {
    //fires when element is destroyed or removed from DOM
  }
}
customElements.define('random-queen-generator', RandomQueenGenerator);
```