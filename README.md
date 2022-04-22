# firebaseImagestorage_App


Firebase is a mobile and web application development platform. It provides services that a web application or mobile application might require. Firebase provides secure file uploads and downloads for Firebase application.

 *This app will help you to build an Android application with the ability to select the image from the mobile gallery and upload images to Firebase Storage.

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

Step 4. Setting up MainActivity.java file

   In MainActivity

* Set listeners on interaction of defined button views. On interaction, you want to call a method that triggers either the selection of an image from the gallery or the uploading of the selected image to Firebase storage. setOnClickListener is used for that action on interaction.

* When SelectImage method is called, a new Intent instance is created. The intent type is set to image, and its action is set to get some content. The intent creates an image chooser dialog that allows the user to search through the device gallery to select the image from the gallery.

* startActivityForResult is used to receive the result, which is the selected image.

* To display this image, make use of a method called onActivityResult(). onActivityResult receives a request code, result code, and the data. Check in this method, if the request code equals PICK_IMAGE_REQUEST, with the result code equal to RESULT_OK and the data available. If all this is true, display the selected image in the ImageView below buttons.

* Override the startActivityForResult method and write its implementation.

* Also in uploadImage() method, Firebase storage reference is taken and putFile() function is used to upload the image to firebase storage with success and failure listeners. If an image is uploaded than success toast is there otherwise failure toast is there.

