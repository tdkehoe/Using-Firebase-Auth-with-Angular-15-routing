# Using Firebase Auth with Angular 15 Routing

# AngularFire?

AngularFire 7 has libraries for Auth and AuthGuard:

```js
import { provideAuth, getAuth, } from '@angular/fire/auth';
import { AuthPipe, AuthGuard, AuthGuardModule, } from '@angular/fire/auth-guard';
```

There's no documentation for these libraries. I'll list all the methods at the end of this tutorial/

## Get rid of AngularFire 6 references

Get rid of any references to AngularFire 6. The directory `@angular/fire/compat` is AngularFire 6. For example, 

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

# AngularFire 7 Methods

Here are complete lists of AngularFire 7 methods:

applyActionCode	 
authInstance$	 
authState	 
beforeAuthStateChanged	 
browserLocalPersistence	 
browserPopupRedirectResolver	 
browserSessionPersistence	 
checkActionCode	 
CompleteFn	 
confirmPasswordReset	 
connectAuthEmulator	 
createUserWithEmailAndPassword	 
CustomParameters	 
debugErrorMap	 
deleteUser	 
EmailAuthCredential	 
EmailAuthProvider	 
ErrorFn	 
FacebookAuthProvider	 
FactorId	 
fetchSignInMethodsForEmail	 
getAdditionalUserInfo	 
getAuth	 
getIdToken	 
getIdTokenResult	 
getMultiFactorResolver	 
getRedirectResult	 
GithubAuthProvider	 
GoogleAuthProvider	 
idToken	 
indexedDBLocalPersistence	 
initializeAuth	 
inMemoryPersistence	 
isSignInWithEmailLink	 
linkWithCredential	 
linkWithPhoneNumber	 
linkWithPopup	 
linkWithRedirect	 
NextFn	 
NextOrObserver	 
OAuthCredential	 
OAuthProvider	 
onAuthStateChanged	 
onIdTokenChanged	 
OperationType	 
parseActionCodeURL	 
PhoneAuthCredential	 
PhoneAuthProvider	 
PhoneInfoOptions	 
PhoneMultiFactorGenerator	 
prodErrorMap	
provideAuth
ProviderId	 
reauthenticateWithCredential	 
reauthenticateWithPhoneNumber	 
reauthenticateWithPopup	 
reauthenticateWithRedirect	 
RecaptchaVerifier	 
reload	 
SAMLAuthProvider	 
sendEmailVerification	 
sendPasswordResetEmail	 
sendSignInLinkToEmail	 
setPersistence	 
signInAnonymously	 
SignInMethod	 
signInWithCredential	 
signInWithCustomToken	 
signInWithEmailAndPassword	 
signInWithEmailLink	 
signInWithPhoneNumber	 
signInWithPopup	 
signInWithRedirect	 
signOut	 
unlink	 
Unsubscribe	 
updateCurrentUser	 
updateEmail	 
updatePassword	 
updatePhoneNumber	 
updateProfile	 
useDeviceLanguage	 
user	 
UserProfile	 
verifyBeforeUpdateEmail	 
verifyPasswordResetCode	



