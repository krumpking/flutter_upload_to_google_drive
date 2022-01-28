# upload_to_google_drive

A new Flutter project.

## Getting Started

This project is about uploading a file to Google Drive 

First of all, create a project in Google Cloud Platform.

Click Create Credentials and OAuth client ID

Select Android and input necessary information.

The package name must be the same as the value specified to package in android\app\src\main\AndroidManifest.xml.

Enter the SHA-1 , I will send it to you    , created by running in 
keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android 
for Linux&Mac 
./gradlew signingReport should work in Android 

Download google-services.json and place it to android\app\google-services.json.

Select Scopes

 Go to API Library page

Then, click Google Drive API

Click the ENABLE button here.

Once it’s enabled and the scopes page is reloaded, the new items are shown.

Add test users, (or maybe publish it in our case)

Create Firebase Project

Add 4 dependencies into pubspec.yaml file.

 googleapis: ^7.0.0
  google_sign_in: ^5.2.1
  firebase_auth:
  firebase_core:

Add classpath 'com.google.gms:google-services:4.3.10'  in dependencies android\build.gradle

Add apply plugin: 'com.google.gms.google-services'  in android\app\build.gradle

Ensure minSdk is 20(though 19 would , 20 is safer)

Add implementation 'com.google.firebase:firebase-analytics' in android\app\build.gradle 



