# ESP32 cam image based motion detector and email sender. No SD card or SPIFFS required 
## This repository shows a method of detecting motion based on image frame difference only. No additional hardware needed. Also shows how to send the captured image using email without the need of SD card or SPIFFS. 

### board installation link : https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/
### library required : [EloquentArduino](https://github.com/eloquentarduino/EloquentArduino), [ESP mail client](https://github.com/mobizt/ESP-Mail-Client)



Board selection in arduino IDE:<br>(for port selction,  select your FTDI programmer's com port)

![alt text](https://github.com/AsifKhan991/ESP32_cam_image_based_motion_detector_and_email_sender/blob/main/board%20settings.PNG?raw=true)

How the mail looks like:

![alt text](https://github.com/AsifKhan991/ESP32_cam_image_based_motion_detector_and_email_sender/blob/main/sample1.PNG?raw=true)

How the motion triggering image looks like:

![alt text](https://github.com/AsifKhan991/ESP32_cam_image_based_motion_detector_and_email_sender/blob/main/capture.jpg?raw=true)
<br>tested in ESP-32 Ai-Thinker module<br>
Note: 
  1) It's better to power up the esp32-cam module with seperate power source or it might cause brownout while processing frames
  2) Make sure your ISP isn't blocking connection to smtp server!
  3) Don't exceed frame quality of SVGA
  4) Jpeg conversion quality in line 133 effects the heap memory required to store the image
  5) Becareful of heap memory usage as smptp ssl connection depends on it. Less memory might cause problem when handling ssl connection. 

