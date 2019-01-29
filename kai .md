# KAI
- **Kai** is a wearable device to track the movement of hand and control device with gestures.
- It can pair with device using bluetooth , which includes AR/VR , Gaming ,Designing 3D modelling , control Presentations , Home Automation , Hardware Control.
- **kai** works with keyboard and mouse. 
- From the provided set of gestures user can select their gesture  to communicate. 
# ARCHITECTURE
 User request is received by dongle and then it goes to SDK , where the decoding takes place and decoded imformation is send to modules and sents the response.
- Hardware
- SDK 
- Control center
- kai Control center
 ## Hardware :
 - Hardware act as an interface for SDK.
 ## SDK:
 - SDK has 2 ways of communication
   * process
   * Web SocketServer
 ## Control Center:
 - **KAI** comes with a control center customising the kai  as simple as it can be.
 - It suggest options based on the software you choose.
 ## Kai Controll Center:
 - It contains datatypes
   * GestureDatatype-swipeup,swipedown 
   * pyrdatatype-pinch,pitch,roll,yaw
 - Using kai control center, you can configure the gesture control for Photoshop.
 # JSON format:
 ### 1.Authentication:
 Here module must send moduleId and modulesecret.
 ```
 type:authentication,
 moduleId:123,
 modulesecret:qwerty |default |true/ false
 ```
 ### 2.Setting Capabilities:
 sets the datatypes values either true /false.
 ```
 type:setcapabilities,
 pyrData:true/false,
 ```  
 ### 3.Calibration 
 #### Finger calibration:
 - It requries hand segmentation and fingertip detection.
#### IMU Calibration:
- Using data from accelerometer,gyroscope,therometer and barometer including angle,pitch angle,roll angle.
### 4.List Connected kai:
- It gives about type and kaiId
```
type:connectedKai,
KaiId:0
```
### 5.SwitchHand:
- User can shift the hands to left or right and sets the defaultlefthand and defaultrighthand to true /false.
### 6.unknown Data:
- If request is unknown type an error response is sent.   