# Digital_Doorlock_Control_with_Face_Recognition
Deep Learning Image Processing(DLIP) Project 4.

This is a Tutorial and guidbook for real running of our system.

Prof. y.k.kim 
HGU
2021.06

## Configuration
+ OS:Windows 10 and Ubuntu 
(Basically the program code is nearly same with Windows and Ubuntu. face_recog_realtime.py is the only python program code which is used in Ubuntu.)
(Ubuntu for jetson nano board)
+ Hardware: NVIDIA Jetson Nano, Arduino Uno, Logitech C922 Pro Webcam
+ Python: ver 3.8.10 for Windows / ver 3.6.9 for Ubuntu
+ Numpy: ver 1.20.2 / ver 1.19.3 for Ubuntu
+ Python PIL library: ver 8.2.0 / ver 5.1.0 for Ubuntu
+ OpenCV: ver 4.5.2 (for Windows and Ubuntu)

We have succesfully built this system in above environment. You have to install above or appropriate environments in Windows and Jetson Nano

## Usage

### Windows
Before running real-time recognition system, you should train the authorized persons face in Windows. 

### Arduino
Just compile and Upload the doorLock.ino file into Arduino Uno
Be aware of Arduino COM port number when you run the program code in Windows

### Jetson Nano 
After move the face_recog_realtime.py file and face-trainer.yml and haarcascade_frontalface_default.xml file to Jetson nano,
Now everything is ready!

You should connect all the devices(Arduino Nano and Webcam) to Jetson Nano before run this code.

First, Open the Terminal in Jetson. type the following command for Serial Communication



    sudo chmod a+rw /dev/ttyACM0
    
    
    
After that, you just open the face_recog_realtime.py file
Type the followings in the terminal.



    cd DLIP
    
    
    
(type the folder name instead of DLIP that the face_recog_realtime.py and other yml and xml files are located. For our case, the folder name was DLIP)



    python3 face_recog_realtime.py 
    
    
    
This is it! 
Good Luck
