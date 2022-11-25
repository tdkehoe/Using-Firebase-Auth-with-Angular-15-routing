# Using Firebase Auth with Angular 15 Routing

## Get rid of AngularFire 6 references

Before anything else, get rid of all references to AngularFire 6. The directory `@angular/fire/compat` is AngularFire 6. For example, 

```js
import { AngularFireAuthGuard } from '@angular/fire/compat/auth-guard';
```

There is a file in that directory that is compatible with TypeScript only up to 4.7.3. Angular 15 uses TypeScript 4.8.4. 

# Import Firebase Auth into `app.module.ts`

Import AngularFire 7 Auth into your `app.module.ts`:

```js
import { provideAuth, getAuth } from '@angular/fire/auth';

@NgModule({
  imports: [
  provideAuth(() => getAuth()),
```

# Import Auth into `app-routing.module.ts`

