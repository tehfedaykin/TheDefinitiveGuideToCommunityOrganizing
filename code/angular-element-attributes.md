### Angular Element Attributes

```typescript
class RandomQueenGenerator extends HTMLElement {
  static myAttributes = ['name', 'quote'];
  attributeChangedCallback(key, oldVal, newVal){
    //fires when attributes change
  }
  ...
}
customElements.define('random-queen-generator', RandomQueenGenerator);
```