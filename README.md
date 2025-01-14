<p align="center"><br><img src="https://user-images.githubusercontent.com/236501/85893648-1c92e880-b7a8-11ea-926d-95355b8175c7.png" width="128" height="128" /></p>
<h3 align="center">Firebase Authentication</h3>
<p align="center"><strong><code>@robingenz/capacitor-firebase-authentication</code></strong></p>
<p align="center">
  Capacitor plugin for Firebase Authentication.
</p>

<p align="center">
  <img src="https://img.shields.io/maintenance/yes/2021?style=flat-square" />
  <a href="https://github.com/robingenz/capacitor-firebase-authentication/actions?query=workflow%3A%22CI%22"><img src="https://img.shields.io/github/workflow/status/robingenz/capacitor-firebase-authentication/CI/main?style=flat-square" /></a>
  <a href="https://www.npmjs.com/package/@robingenz/capacitor-firebase-authentication"><img src="https://img.shields.io/npm/l/@robingenz/capacitor-firebase-authentication?style=flat-square" /></a>
<br>
  <a href="https://www.npmjs.com/package/@robingenz/capacitor-firebase-authentication"><img src="https://img.shields.io/npm/dw/@robingenz/capacitor-firebase-authentication?style=flat-square" /></a>
  <a href="https://www.npmjs.com/package/@robingenz/capacitor-firebase-authentication"><img src="https://img.shields.io/npm/v/@robingenz/capacitor-firebase-authentication?style=flat-square" /></a>
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<a href="#contributors-"><img src="https://img.shields.io/badge/all%20contributors-1-orange?style=flat-square" /></a>
<!-- ALL-CONTRIBUTORS-BADGE:END -->
</p>

## Maintainers

| Maintainer | GitHub                                    | Social                                        |
| ---------- | ----------------------------------------- | --------------------------------------------- |
| Robin Genz | [robingenz](https://github.com/robingenz) | [@robin_genz](https://twitter.com/robin_genz) |

## Installation

```
npm install @robingenz/capacitor-firebase-authentication
npx cap sync
```

Add Firebase to your project if you haven't already ([Android](https://firebase.google.com/docs/android/setup) / [iOS](https://firebase.google.com/docs/ios/setup)).

On **iOS**, verify that this function is included in your app's `AppDelegate.swift`:

```swift
func application(_ app: UIApplication, open url: URL, options: [UIApplication.OpenURLOptionsKey : Any] = [:]) -> Bool {
  return ApplicationDelegateProxy.shared.application(app, open: url, options: options)
}
```

The further installation steps depend on the selected authentication method:

- [Apple Sign-In](docs/setup-apple.md)
- [GitHub Sign-In](docs/setup-github.md)
- [Google Sign-In](docs/setup-google.md)
- [Microsoft Sign-In](docs/setup-microsoft.md)
- [Twitter Sign-In](docs/setup-twitter.md)
- [Yahoo Sign-In](docs/setup-yahoo.md)

## Configuration

No configuration required for this plugin.

## Usage

```typescript
import { FirebaseAuthentication } from '@robingenz/capacitor-firebase-authentication';

const getCurrentUser = async () => {
  const result = await FirebaseAuthentication.getCurrentUser();
  return result.user;
};

const getIdToken = async () => {
  const result = await FirebaseAuthentication.getIdToken();
  return result.token;
};

const setLanguageCode = async () => {
  await FirebaseAuthentication.setLanguageCode({ languageCode: 'en-US' });
};

const signInWithApple = async () => {
  await FirebaseAuthentication.signInWithApple();
};

const signInWithGithub = async () => {
  await FirebaseAuthentication.signInWithGithub();
};

const signInWithGoogle = async () => {
  await FirebaseAuthentication.signInWithGoogle();
};

const signInWithMicrosoft = async () => {
  await FirebaseAuthentication.signInWithMicrosoft();
};

const signInWithTwitter = async () => {
  await FirebaseAuthentication.signInWithTwitter();
};

const signInWithYahoo = async () => {
  await FirebaseAuthentication.signInWithYahoo();
};

const signOut = async () => {
  await FirebaseAuthentication.signOut();
};

const useAppLanguage = async () => {
  await FirebaseAuthentication.useAppLanguage();
};
```

## API

<docgen-index>

* [`getCurrentUser()`](#getcurrentuser)
* [`getIdToken(...)`](#getidtoken)
* [`setLanguageCode(...)`](#setlanguagecode)
* [`signInWithApple()`](#signinwithapple)
* [`signInWithGithub()`](#signinwithgithub)
* [`signInWithGoogle()`](#signinwithgoogle)
* [`signInWithMicrosoft()`](#signinwithmicrosoft)
* [`signInWithTwitter()`](#signinwithtwitter)
* [`signInWithYahoo()`](#signinwithyahoo)
* [`signOut()`](#signout)
* [`useAppLanguage()`](#useapplanguage)
* [Interfaces](#interfaces)

</docgen-index>

<docgen-api>
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

### getCurrentUser()

```typescript
getCurrentUser() => Promise<GetCurrentUserResult>
```

Fetches the currently signed-in user.

Only available for Android and iOS.

**Returns:** <code>Promise&lt;<a href="#getcurrentuserresult">GetCurrentUserResult</a>&gt;</code>

--------------------


### getIdToken(...)

```typescript
getIdToken(options?: GetIdTokenOptions | undefined) => Promise<GetIdTokenResult>
```

Fetches the Firebase Auth ID Token for the currently signed-in user.

Only available for Android and iOS.

| Param         | Type                                                            |
| ------------- | --------------------------------------------------------------- |
| **`options`** | <code><a href="#getidtokenoptions">GetIdTokenOptions</a></code> |

**Returns:** <code>Promise&lt;<a href="#getidtokenresult">GetIdTokenResult</a>&gt;</code>

--------------------


### setLanguageCode(...)

```typescript
setLanguageCode(options: SetLanguageCodeOptions) => Promise<void>
```

Sets the user-facing language code for auth operations.

| Param         | Type                                                                      |
| ------------- | ------------------------------------------------------------------------- |
| **`options`** | <code><a href="#setlanguagecodeoptions">SetLanguageCodeOptions</a></code> |

--------------------


### signInWithApple()

```typescript
signInWithApple() => Promise<SignInResult>
```

Starts the Apple sign-in flow.

Only available for Android and iOS.

**Returns:** <code>Promise&lt;<a href="#signinresult">SignInResult</a>&gt;</code>

--------------------


### signInWithGithub()

```typescript
signInWithGithub() => Promise<SignInResult>
```

Starts the GitHub sign-in flow.

Only available for Android and iOS.

**Returns:** <code>Promise&lt;<a href="#signinresult">SignInResult</a>&gt;</code>

--------------------


### signInWithGoogle()

```typescript
signInWithGoogle() => Promise<SignInResult>
```

Starts the Google sign-in flow.

Only available for Android and iOS.

**Returns:** <code>Promise&lt;<a href="#signinresult">SignInResult</a>&gt;</code>

--------------------


### signInWithMicrosoft()

```typescript
signInWithMicrosoft() => Promise<SignInResult>
```

Starts the Microsoft sign-in flow.

Only available for Android and iOS.

**Returns:** <code>Promise&lt;<a href="#signinresult">SignInResult</a>&gt;</code>

--------------------


### signInWithTwitter()

```typescript
signInWithTwitter() => Promise<SignInResult>
```

Starts the Twitter sign-in flow.

Only available for Android and iOS.

**Returns:** <code>Promise&lt;<a href="#signinresult">SignInResult</a>&gt;</code>

--------------------


### signInWithYahoo()

```typescript
signInWithYahoo() => Promise<SignInResult>
```

Starts the Yahoo sign-in flow.

Only available for Android and iOS.

**Returns:** <code>Promise&lt;<a href="#signinresult">SignInResult</a>&gt;</code>

--------------------


### signOut()

```typescript
signOut() => Promise<void>
```

Starts the sign-out flow.

Only available for Android and iOS.

--------------------


### useAppLanguage()

```typescript
useAppLanguage() => Promise<void>
```

Sets the user-facing language code to be the default app language.

--------------------


### Interfaces


#### GetCurrentUserResult

| Prop       | Type                                          | Description                                               |
| ---------- | --------------------------------------------- | --------------------------------------------------------- |
| **`user`** | <code><a href="#user">User</a> \| null</code> | The currently signed-in user, or null if there isn't any. |


#### User

| Prop                | Type                        |
| ------------------- | --------------------------- |
| **`displayName`**   | <code>string \| null</code> |
| **`email`**         | <code>string \| null</code> |
| **`emailVerified`** | <code>boolean</code>        |
| **`isAnonymous`**   | <code>boolean</code>        |
| **`phoneNumber`**   | <code>string \| null</code> |
| **`photoUrl`**      | <code>string \| null</code> |
| **`providerId`**    | <code>string</code>         |
| **`tenantId`**      | <code>string \| null</code> |
| **`uid`**           | <code>string</code>         |


#### GetIdTokenResult

| Prop        | Type                | Description                            |
| ----------- | ------------------- | -------------------------------------- |
| **`token`** | <code>string</code> | The Firebase Auth ID token JWT string. |


#### GetIdTokenOptions

| Prop               | Type                 | Description                                   |
| ------------------ | -------------------- | --------------------------------------------- |
| **`forceRefresh`** | <code>boolean</code> | Force refresh regardless of token expiration. |


#### SetLanguageCodeOptions

| Prop               | Type                | Description                             |
| ------------------ | ------------------- | --------------------------------------- |
| **`languageCode`** | <code>string</code> | BCP 47 language code. Example: `en-US`. |


#### SignInResult

| Prop       | Type                                          | Description                                               |
| ---------- | --------------------------------------------- | --------------------------------------------------------- |
| **`user`** | <code><a href="#user">User</a> \| null</code> | The currently signed-in user, or null if there isn't any. |

</docgen-api>

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

See [LICENSE](LICENSE).
