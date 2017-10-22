[Home](/README.md) | [Gestures](/gestures.md) | [Reference](/reference.md) | [Edit Guide](/editguide.md) | <button class="nav" ><a href="https://github.com/whatifif/handgesture/">View on Github</a></button>  |  <button class="nav" ><a href="https://whatifif.github.io/handgesture/">View on Web</a></button>

[draft-d](/draft-d/README.md) | [draft-h](/draft-h/README.md) | [draft-j](/draft-j/README.md)

# Controlling a Computer by Hand Gesture


## Brief Introduction of the project of Team Echo

Almost people use a desktop or laptop these days. One of serious problem is that we are stuck to the keyboard and mouse, which will cause a serious health problem on a long run. Moreover in VR/AR age, we cannot use keyboard/mouse. Our purpose is to replace a keyboard and mouse with hand gestures. We have devised a virtual keyboard and virtual mouse with subtle hand gestures and made ML recognise our gestures so that we can control our computer remotely. Amazon echo has ear now. It will have eye in future. We need to make a standard gestures for people to adopt easily like a standard keyboard and mouse. ML will address this for us, human. We used Deep Learning as ML in this project.


## Introduction

People have used a keyboard and mouse as a standard way of input to computer for a long time. One of the serious problem of using keyboard and mouse is that we are stuck to the keyboard/mouse and sit still while we are using our desktop or laptop computer. This causes a serious health problem on a long run. 

Moreover we are entering the VR ( Virtual reality )/ AR ( Augmented reality ) age and we cannot use keyboard/mouse as we did before. We have to use some kind of mobile controller or GESTURE !!!

ML( Machine Learning ) can recognise our gesture and control the computer as we intented by gesture remotely.
We will feel like a magician. And by moving our body to control the computer, we can avoid sitting still and getting a health problem. Moreover we can play a game with much more immersive experience by moving our hands, heads and body.

To replace a keyboard and mouse, we have to devise many subtle gestures and these gestures have to be easy one for people to learn easily like a standard keyboard and mouse. It may be annoying if we have to learn different gestures to control different devices in future.

We suggest a standard virtual keyboard and standard virtual mouse like followings. The goal of this project is to search a possibility of using these subtle gestures to control a computer up to the level to replace a keyboard and mouse completely.


## Recent works in this field

1. [Carnegie Mellon University OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose): webcam

2. [Microsoft hololens](https://www.microsoft.com/en-au/hololens): 3D sensor

3. [Microsoft hand tracking](https://www.microsoft.com/en-us/research/project/fully-articulated-hand-tracking/): 3D sensor

4. [Leap Motion](https://www.leapmotion.com): 3D sensor

5. [Mano Motion](https://www.manomotion.com/): smartphone camera

6. [PilotBit Mobile Hand Tracking](http://www.pilotbit.com/): 3D sensor


## Challenging points

1. using a webcam without using 3D sensor (depth camera)

2. detecting the subtle gestures at real time

3. deep learning running at mobile devices such as smartphone, smartglasses and VR/AR headset


## Work flow

1. searching github for open sources and youtube for useful information.

2. defining as many hand gestures as possible to cover all the keys on a keyboard and mouse.

3. coding for tools to create as many data sets as possible in short time.

4. coding to use a deep learning model which can recognise these hand gestures at real time.

5. coding for tracking and capturing hand

6. coding for some demos such as basic calculation or a game.



## Tools used for Team work
1. github site for project page: [https://github.com/whatifif/handgesture](https://github.com/whatifif/handgesture)  
2. github site for coding work : [https://github.com/whatifif/handgesturecode](https://github.com/whatifif/handgesturecode)  
3. slack for team communication and instant file sharing: [https://sml109.slack.com](https://sml109.slack.com)   

## Hardwares and software
1. Coding with MacBook Air (i7, 8GB RAM)
2. ML Model training with nvidia GTX 960 (2GB Graphic memory) on i7 CPU, 8GB RAM, ubunutu 14.04 64bit personal computer
3. Microsoft Webcam HD-3000
4. MacBook Air webcam
5. opencv and python 2.7
6. jupyter notebook as python editor


## Hand Gestures as a Standard Way to replace a Keyboard and Mouse

We have two hands normally. We can use one hand for keyboard and the other for a mouse.
The standard gestures should be easy for people to learn easily. Just imagine that there is a virtual keyboard in front of your left side and virtual mouse on your right side. Lets focus on virtual keyboard first.

We divided the left side into three region

1. left region
2. middle region
3. right region

We can make 10 easy distinct gesture on each region:

1. closed hand
2. open hand
3. thumb only
4. additional index finger
5. additional middle finger
6. folding first finger
7. folding second finger
8. folding middle finger
9. folding index finger
10 folding thumb

If we use 6, 7, 8, 9, 10 as inputs, we have 5 * 3 = 15 different gestures in each region and 15 * 3 = 45 gestures in total region.

If we use 3, 4, 5 as control, we have 3 * 3 = 9 controls and 45 * 9 = 135 different gestures which will cover the whole range of keys ( numbers, lower alphabet, upper alphabet, special keys and controls )

For a mouse, we can have 10 same gestures as left hand, which cover whole inputs from mouse. Our center of hand is a mouse cursor. The mouse cursor of computer will track the center of the right hand.

For a left-handed people, of course we can swap the left and right.

  
  [gestures for keyboard and mouse](/gestures.md)

## Making a data set
To train the ML, several thousand data are needed and these data are to be prepared by ourselves.
So we have to make a program for capturing the hand images easily. With the capturing program, about 2000 hand images were captured. 

## Detecting and tracking Hand
Since we have to move our hands freely in front of webcam, our hands should be detected correctly in the frame of webcam image. Haar cascade, background substraction and skin color detection were tried to track a hand. Skin color detection was found to be stable.

#### detection region for hand and mouse
Since our face has a same skin color as our hands, we have to find ways to ignore the face. Haar cascade can be applied for this purpose. But due to the time limitation of this project, we simply defined a detection region and tried not to push our face into that region.

#### tracking hand
Since we use a skin color detection for hand, background color and our shirts color should have contrasting color to skin color. And we have to wear a long sleeve shirt to hide our arm from detection also.

The environment light affects skin color significantly. So bright room was avoided. And a blue screen made from blue table cloth was used as a background to get a good data. It turns out that the whiteboard is a good background also.

## Deep Learning Model to recognise the gesture

#### Why MxNet?


#### How can the trained model be transferred to work at smartphone?




## TODOs

1. ### getting more data of hand gesture.

2. ### connecting a trained model 
   a. making the model recognise a gesture in application program ( stream-lined at real time)

3. ### making a demo program
   a. calculation program
   
   b. running dinosaur ?
  
4. ### preparing a presentation
   a. introduction
   
   b. creating data sets
   
   c. training and testing
   
   d. demo
   
   e. summary and future work
   

5. ### tracking a right hand for mouse ?

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/whatifif/handgesture/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

### [LICENSE](/LICENSE)
GNU GENERAL PUBLIC LICENSE Version 3, 29 June 2007

Copyright (C) 2007 Free Software Foundation, Inc. <http://fsf.org/>
 
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.
