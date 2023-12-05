# v4l2camera
fork from https://github.com/yizhongliu/AnV4L2Camera, fix for jitpack.

# how to use 
1. add to your build.gradle
  `implementation 'com.github.jiamicu:v4l2camera:v1.0.3'`
2. make sure the video node (eg. /video/0) has the access right
3. init and call the function
   ```
   V4L2Camera usbCamera;
   class CameraStateCallback implements IStateCallback {...}
   cameraStateCallback = new CameraStateCallback();
   usbCamera = new V4L2Camera();
   usbCamera.init(cameraStateCallback, this);
   usbCamera.open(0);//the camera number is 0
   ```
