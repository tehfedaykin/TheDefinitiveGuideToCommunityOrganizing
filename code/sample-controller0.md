### Example Setup

```typescript
angular.
  module('ngQueenApp').
  component('queensComponent', {
    template:  '<ul>' +
          '<li ng-repeat="queen in $ctrl.queens">' +
            '<span>{{queen.name}}</span>' +
            '<p>{{queen.quote}}</p>' +
          '</li>' +
        '</ul>',
    controller: function QueensController() {
      this.queens = [
        {name: 'Bianca Del Rio', quote: `I will show you versatility 
        when Santino wins a sewing competition and Visage 
        wears a fucking turtle neck!`},
        {name: 'BenDeLaCreme', quote:'Excuse me, we originated the language'},
        {name: 'Courtney Act', quote: `Sewing is not my forte but... 
        everything else is.` }
      ];
    }
  })
```