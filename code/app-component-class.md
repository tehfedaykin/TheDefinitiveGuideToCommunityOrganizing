### Example Component Refactored to Class

```typescript
import IQueen from "./Iqueen";
import queensTemplate from './queens.component.html';
import ISeason from "../seasons/Iseason";

class QueensCtrl implements angular.IComponentController {
  public static $inject: string[] = ['QueenService', 'SeasonService'];
  public queens: [];

  constructor(private QueenService: any ) {}

  public $onInit () {
    this.QueenService.getQueens().then((res) => {
      vm.queens = res;
    })
  }
}

class QueensComponent implements ng.IComponentOptions {
  public controller: ng.Injectable<ng.IControllerConstructor>;
  public controllerAs: string;
  public template: string;

  constructor() {
    this.controller = QueensCtrl;
    this.controllerAs = "vm";
    this.template = queensTemplate;
  }
}

export default QueensComponent
```