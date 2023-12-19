# KindeAngular

Kinde integration for Angular

## Quick setup

```bash
npm i tbd
```

import module to your app module
```typescript
import { KindeModule } from 'tbd';
```

Add KindeModule to your imports
```typescript
@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    KindeAngularModule.forRoot({
      clientId: 'client_id_here',
      authDomain: 'https://domain.kinde.com',
      redirectURL: 'http://localhost:4200/',
      logoutRedirectURL: 'http://localhost:4200/',
    })
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

Add KindeService to your component via contructor or Inject method
```typescript
  constructor(private authService: KindeAngularService){
  }
```
Or
```typescript
  const authService = inject(KindeAngularService);
```
