# Safe-home-system
# **Software engineering project**

## Safe Home manual : emulation system

![image](https://user-images.githubusercontent.com/61031416/123673547-31023900-d873-11eb-9bc9-53d267f8d673.png)

### Project participators:

David Bukedi Diela 2018529627050

### Summary


### 1. About safe Home system

### 2. Explanation of Settings functions

### 3. System explanation:local and online

### 4. The simulation

### 5. A real world simulation

￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣￣

**-----------Safe Home system Manual---------**

Note: **this program is still in development,this is an experiment using only two cameras . refer to the simulator file to have a preview of what the final system looks like .**

All the requirements have been given on the Readme.txt file that you can find on the document.

1. About Safe Home system

This program is basically designed as video-alarm system using python and java . After installing and setting everything up(see readme.txt ), it offers the possibility to keep the user aware of his house and protects your home from intruders .

The program is divided into Two main scripts(other will be added in the next version):

1. **SettingGUIF.py** :

This script contains some ofthe GUI methods and the GUI itself displaying the user parameters and the alarm parameters. It allows the administrator to:

-add a user(up to two users)

-delete a user

-modify the alarm

-change the voice type(male/female)

-change alarm speech(default is &quot;face intruder detected&quot;)

-number of repetition of the alarm system

-set everything back to default(no user)

![image](https://user-images.githubusercontent.com/61031416/123673668-50996180-d873-11eb-98a4-60e3b94accb6.png)

1. **camsystem.py** :

This script contains the engine of the system meaning the face recognition system (face recognition) and the motion detection system:

requirements:

-python \&gt;=3.7

-webcam

-Python modules-opencv,numpy,Pyqt5,beepy

features:

-register user face

-detect unregistered faces and suspicious motion

-set alarm voice type(male/female)

-set alarm speech(change what voice says)

-set alarm sound

1. Explanation of the Settings functions:

How to add a user:

1.Write your name then click on add user

![image](https://user-images.githubusercontent.com/61031416/123673694-5a22c980-d873-11eb-82b6-a8a4cae59391.png)

2.Stay at 60 cm from the cam1 , it will take a picture

From your face to register the user

![image](https://user-images.githubusercontent.com/61031416/123673704-5d1dba00-d873-11eb-85f4-43dd33e2315c.png)

How to delete a user:

1. Write the user&#39;s name then click on Delete user
2. The user&#39;s name must be in the system

![image](https://user-images.githubusercontent.com/61031416/123673720-61e26e00-d873-11eb-8b2b-5d1754237706.png)

How to modify the alarm sound:

1. Click on modify alarm then choose
2. Click on play icon to test the alarm

![image](https://user-images.githubusercontent.com/61031416/123673737-67d84f00-d873-11eb-9cd2-08443ad67191.png)

How to modify voice type

1. Click on change voice
2. Click on play icon to test the voice

![image](https://user-images.githubusercontent.com/61031416/123673757-6d359980-d873-11eb-9c6a-4c713fe51a2b.png)

-How to change the alarm speech

![image](https://user-images.githubusercontent.com/61031416/123673774-7161b700-d873-11eb-8648-4d968d57b2c1.png)

-How change the number of repetition
![image](https://user-images.githubusercontent.com/61031416/123673785-745ca780-d873-11eb-845f-324eaf99e834.png)

installation:

after downloading the project file and installing the dependencies, read those instructions:

-the administrator must log into the system using the username and the password given by the manufacturer

-after loginto the system, the user can add people face so that the alarm will not be activated during the face recognition

-then the user can activate the system by clicking the button on and deactivate by clicking the button off

Case intruder detected:

To find an intruder the system , the cam1 and cam2 motion detection and face recognition

-the system will activate the alarm so that the intruder will understand that he is in a restricted area

-the system will send the intruders face in picture format and the time of motion in cvs format to the owner by email and the owner will be able to use a website or the server(if not away) to see the camera records

1. System explanation
  1. Local system:

The local system is directly managed by the server which is in our case the computer. The cam1 and cam2 work together to perform the face and motion detection . the cam2(ip webcam) generates an ip address that is directly implemented in our source code. The administrator has the possibility to modify it at will since it&#39;s an open-source software.the cam 1 is managed only by the local server meaning within the same network while the cam 2 can be managed anywhere.

Here is the interface of cam 2 local system:

![image](https://user-images.githubusercontent.com/61031416/123673806-79b9f200-d873-11eb-850b-5763be580853.png)

Here is the interface of cam 2 online system:

![image](https://user-images.githubusercontent.com/61031416/123673824-7de60f80-d873-11eb-82ea-1a4883a5139f.png)

As you can see, we can easily record, play and replay the videl that is being streamed.

1. The simulation

**Real world simulation**

To simulate the use of our system in a real world situation, we used our computer&#39;s camera (CAM1) and an ip camera (CAM2
 ).

-the computer&#39;s camera(CAM1) is used as a motion detector, it records all the motions detected , register on a cvs file the duration of all the motions detected and send an email to the owner containing the cvs and the website in which the owner is able to see the cameras records.

![image](https://user-images.githubusercontent.com/61031416/123673853-82aac380-d873-11eb-8a4a-dd668eaa3bd0.png)

![image](https://user-images.githubusercontent.com/61031416/123673869-863e4a80-d873-11eb-85d1-8bf990554422.png)

-the ip camera(CAM2) is used as a face recognizer, it detects all the faces in front of the camera and compare them to those in his database, if a face is not recognized , after a certain amount of time the alarm turns on and the system notifies the owner about the presence of an intruder. The picture is saved in the file &quot;voleur&quot;then sent to the owner.

![image](https://user-images.githubusercontent.com/61031416/123673892-8d655880-d873-11eb-86a4-ebed72cb77ef.png)

In both case the owner receives the picture of the intruder (if the face was on the camera) and the cvs file containing the duration of the movement, the date and the time.

Here is an example of the email I received from the system:

1. ![](RackMultipart20210628-4-1642ify_html_86eda9420013b8f4.gif)the website used by the owner to play,replay and see the live camera

![](RackMultipart20210628-4-1642ify_html_c5e8f20da1078f6a.gif)2. The picture of the intruder

![](RackMultipart20210628-4-1642ify_html_39d703e46dad2886.gif)3.the cvs file containing the date,time and duration

![](RackMultipart20210628-4-1642ify_html_abe77f405f16f1e5.jpg)

SEE THE VIDEO FOR FURTHER EXPLANATIONS

1. Roles of participators

-Software developer:

David Bukedi Diela 
