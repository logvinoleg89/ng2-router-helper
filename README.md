
[![Build Status](https://travis-ci.org/xmaestro/ng2-tagsinput.svg?branch=master)](https://travis-ci.org/xmaestro/ng2-tagsinput)


Installation
--------------------------------------

Install it from npm:

```bash
npm install ng2-router-helper
```

Usage
--------------------------------------


### Подключение

Подключение декоратора

```html
import {RouterHelper} from "ng2-router-helper";

@Component({
  template: `{{ routerHelper.is('routerName') | async }}`
  providers:[RouterHelper]
})
export class TestComponent {
  constructor(
    private routerHelper: RouterHelper
  ) {}
    
  this.isPartOfRoute$ = this.routerHelper.is('routerName2')
  this.isPartOfRoute$.subscribe(res=>{
    console.log(res)
  })
}
```

- `is(routePath):Observable<boolean>` - проверка на то что 'routePath' является последней частью текущего url 
- `includes(routePath):Observable<boolean>` - проверка на то что 'routePath' является частью текущего url

