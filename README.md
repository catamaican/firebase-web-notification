# Firebase console
Create your project firebase https://console.firebase.google.com/u/0/ you will need server key, sender id, project id

# Folder "public" -  for client/javascript setup
For service worker we need HTTP*S* so you may use https://firebase.google.com/docs/hosting/quickstart or you can use your own domain with SSL enabled.

Change to your prj folder
npm install -g firebase-tools
$ firebase login
$ firebase init
$ firebase deploy --project yourprojectid

## Firebase get token
Folder "public" follow instruciton https://firebase.google.com/docs/cloud-messaging/js/client

- mainfest.json and firebase-messaging-sw.js are needed both. Just copy them at your < web ROOT!!! >
- put in app.js your own script for working with firebase
- find and replace your own config firebase in both files (app.js , firebase-messaging-sw.js)
    // Initialize Firebase
    var config = { ...}

# Folder "Api.FirebaseNotification" C#
FirebaseController Asp.net restfulApi

- Api to save token from firebase (check app.js). Ajax will call to api "../firebase/savetoken?token=...". You should change your own.

- Api Send message notify to firebase "../firebase/send?msg=..." using HttpClient 

# All in one
You may move the folder "public" inside "Api.FirebaseNotification". With MVC asp.net you can use html and javascript in _Layout.cshtml . 
## mainfest.json and firebase-messaging-sw.js are NEEDED in web root!
If you want to change firebase-messaging-sw.js please check https://firebase.google.com/docs/web/setup
