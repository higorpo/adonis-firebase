# adonis-firebase

Firebase client and admin SDK wrapper for Adonis JS 4.0

## Install

```bash
npm install adonis-firebase --save
```

## Usage

Create a file in `app/config/firebase.js` and paste the code below by replacing it's values where necessary. Sample configuration can also be found in src/sample-config/firebase.js:

```javascript
'use strict';

/*
 |--------------------------------------------------------------------------
 | Firebase
 |--------------------------------------------------------------------------
 |
 | Provide details of firebase project
 |
 */

module.exports = {

  /*
   |--------------------------------------------------------------------------
   | Firebase Admin credentials key file
   |--------------------------------------------------------------------------
   */
  credentials: "",
  /*
   |--------------------------------------------------------------------------
   | API key
   |--------------------------------------------------------------------------
   */
  apiKey: "",
  /*
   |--------------------------------------------------------------------------
   | Auth
   |--------------------------------------------------------------------------
   */
  authDomain: "",
  /*
   |--------------------------------------------------------------------------
   | Database
   |--------------------------------------------------------------------------
   */
  databaseURL: "",
  /*
   |--------------------------------------------------------------------------
   | Hosting
   |--------------------------------------------------------------------------
   */
  storageBucket: ""

};
```

Also you need to add the provider to AdonisJS at `app/bootstrap/app.js`:

```javascript
const providers = [
   ...
   'adonis-firebase/providers/Firebase',
   'adonis-firebase/providers/FirebaseAdmin'
];
```

then you can simply call it from within controllers etc:

```javascript
const Firebase = use('Firebase');
const FirebaseAdmin = use('FirebaseAdmin');
`````