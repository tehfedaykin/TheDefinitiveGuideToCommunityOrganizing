### Example Component Refactored

```typescript
import queensTemplate from './queens.component.html';

QueenCtrl.$inject = ['QueenService'];

function QueensCtrl(QueenService: any) {
  var vm = this;
  QueenService.getQueens().then((res) => {
    vm.queens = res;
  })
}

var QueensComponent = {
  controller: QueensCtrl,
  controllerAs: "vm",
  template: queensTemplate
}

export default QueensComponent
```