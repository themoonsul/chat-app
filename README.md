# chat-app
Real-time chat with rooms, message likes, social media auth, role-based permissions, file upload, audio messages and real-time notifications.

Stack:

React
Firebase (realtime database, FCM, cloud functions)
Styles with Sass and Rsuite
Developed using Node v10. However, if you have one of the latest Node versions, you can easily have dependecy-related errors (when running npm run start), for example with node-sass. Feel free to update conflict packages to versions with no conflicts.

The reason for developing with Node v10 is to deploy cloud functions without any error. Engine.node is set to 10 inside functions/package.json. When deploying functions with different version other than 10, version conflict will pop-up.

Ideally, you should have Node Version Manager installed to easily switch between different NodeJS versions.

Run frontend locally
Inside src/misc/firebase.js replace config with your firebase project config.
Get FCM vapid key for real-time notificaitons from Firebase dashboard > Cog icon > Project Settings > Cloud Messaging > Web push certificates > Key pair and put it as fcmVapidKey inside src/misc/firebase.js.
Run npm run start and develop :)
If you have problems with node-sass, just update the package to other version.

Run functions locally
Download a service account from Firebase dashboard > Cog icon > Project Settings > Service accounts > Generate new private key.
Put the file as functions/service-account.json
Run npm run start from functions
Deployment
Install firebase-cli by running npm install -g firebase-tools
Run firebase deploy
