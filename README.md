# QuantunBot

## Setup

1. **Clone the repository:**
2. **Install the dependencies:**
   ```sh
   cd functions
   npm install
3. **Set Firebase Project:**
   ```sh
   firebase use --add

4. **Initialize Firebase Admin SDK:**
   ```sh
    const admin = require("firebase-admin");

    if (!admin.apps.length) {
    admin.initializeApp({
        credential: admin.credential.applicationDefault(),
        databaseURL: "https://<YOUR_PROJECT_ID>.firebaseio.com"  // Replace with your own database URL
    });
    }

    module.exports = admin;

## Deployment
1. **Deploy functions to Firebase:**
   ```sh
   firebase deploy --only functions