### Generics

```typescript
function getQueens() {
  return from($http.get('http://www.nokeynoshade.party/api/queens/all')
      .then(getQueensComplete)
      .catch(getQueensFailed));

  function getQueensComplete(res: angular.IHttpResponse<IQueen[]> ): IQueen[] {
    return res.data;
  }

  function getQueensFailed(res: angular.IHttpResponse<error>) {
    console.log('error', res.data.error.message);
  }
}
```