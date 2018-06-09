# Install CLI
- ```npm install -g @angular/cli```

# New Application 
- ```ng new <my-app>```

# Run (Serve) Application
- ``` cd <my-app> ```
- ``` ng serve --open ```


```
*app.component.ts* — the component class code, written in TypeScript.
*app.component.html* — the component template, written in HTML.
*app.component.css* — the component's private CSS styles.
```

# Angular CLI Commands

- ```ng generate component <component-name>```
- ```ng generate service <service-name>```

# Routing

```ng generate module app-routing --flat --module=app```

--flat puts the file in src/app instead of its own folder.<br>
--module=app tells the CLI to register it in the imports array of the AppModule.

```
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';

import { HeroesComponent } from './heroes/heroes.component';

const routes: Routes = [
  {path: 'heroes', component: HeroesComponent}
];

@NgModule({
  imports: [ RouterModule.forRoot(routes) ],
  exports : [RouterModule],
})
export class AppRoutingModule { }
```
