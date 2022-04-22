# firebaseImagestorage_App


Firebase is a mobile and web application development platform. It provides services that a web application or mobile application might require. Firebase provides secure file uploads and downloads for Firebase application.

Step 1. Create a new project on android studio or open an existing project in which you want to add authentication and add the firebase to that android application.

Step 2. Add the firebase storage dependency in build.gradle (Module:app)file. Latest Dependency for firebase storage is:

              implementation 'com.google.firebase:firebase-storage:19.1.0'
              
Step 3. Setting up the activity_main.xml layout file

  The activity_main.xml layout file consists of:
  
1) Two layouts: nesting linear layout inside relative layout
2) Two buttons:
    * one for selecting an image from gallery
    * other button is for uploading an image on firebase storage on the cloud
3) An image view in which image is shown chosen from the gallery
