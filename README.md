# MakerBot Typer Project

## Table of Contents
- [Planning](#planning)
- [Parts Design](#parts-design)
- [Code and Wring](#code-and-wiring)
- [Construction](#construction)
- [Final Reflection](#final-reflection)
## Planning
We started off this project with an old makerbot replicator 3D printer. After removing most of the unnecessary parts we began researching how it works.
Here is a Link to Our Planning Document. [Link](https://docs.google.com/document/d/1T3XDndcVtskV35GWUf_W5hFFygKiFvkT9gGz4ztQe54/edit#heading=h.ukbi0a75zb46)

<img src="https://github.com/matthewbowling123/MakerBot-Project/blob/master/Media/MakerBot_Replicator2_Front_View.jpg?raw=true" alt="wiring2" style="width:318px;">

Original Makerbot before we removed unnecessary parts.

<img src="https://user-images.githubusercontent.com/112979288/217347712-2c251434-4a55-4bea-a959-e4c4425f95dc.jpg?raw=true" alt="wiring2" style="width:318px;"> <img src="https://user-images.githubusercontent.com/112979288/217352139-2f6f64c7-9ace-4b89-bcd1-329e3a5a4a7f.jpg?raw=true" alt="wiring2" style="width:318px;">

Maker bot after all side panels had been taken off but before project completion


#### Goals
Our first goal was to get the steppers to movie the rails along the X and Y axis. The Z axis was not reqiuired for this project beause we would hold the keyboard at a fixed hight and create a module to press each key. Our second Goal was to get the keys pressede through means of a button. A large solenoid was what ultimatly was decided on. Our final goal was to get these to work together and type on a keyboard. If we have extra time before the project deadline we want to develope an easy way to type in some text editor and send the text to our robot and then the text would be typed. Perhaps this is too ambitious but we will see.

#### Objective
This Project's goal was to use what was once a Makerbot 3D printer and reprogram it to do something else entirely. Our goal was to connect it with two keyboards and have it read so that whenever something was typed on one keyboard it would type it faster on the other. The problem this solved was helping Zack type faster on an online typing test.
#### Materials
The total cost of materials is unknown due to us using an already existing Makerbot. The total Materials required though are as followed.
* 2 Stepper Motors
* 2 H Bridges
* 1 Arduino
* 1 Big Solenoid
* A MakerBot 3D printer
* Wires
* BreadBoard
* 2 Potentiometers
* Button
* Nuts and Bolts of various sizes
* Acrylic panel for mounting controls.
* 1 tip120 for solenoid wiring
* 1 diode for solenoid wiring
* 1 resistor

#### Potential Obstacles
* How to intergrate steppers and whether or not we could use the steppers already within the makerbot.
* How to press each key precisely and with enough force.
* How to tell each stepper to move to get the pressing mechanism to each key location.

#### Planning Sketches
<img src="https://github.com/matthewbowling123/MakerBot-Project/assets/112979288/62af7025-5d81-4aac-afd7-ebc57aee9e6b" alt="wiring2" style="width:318px;">
<img src="https://github.com/matthewbowling123/MakerBot-Project/assets/112979288/94b4d4ad-a6b8-41b9-94f0-b16a890b476a" alt="wiring2" style="width:318px;">

#### Milestones
| Stage  | Date | Objectives
| ------------- | ------------- | ------------ |
| Research and Proof of Concept| 11/28-12/17 | Can we control steppers in the 3d printer or do we need to replace them. How are we going to press the keys. |
| Design  | 1/4-1/17 | Cad design for brakets |
| Building | 1/17-1/31 | Mount in the steppers and key pushing mechanism. |
| Coding | 1/31-2/10 | Code and test on individual parts |
| Final touches and documentation | 2/10-2/14 | Make sure everything is working |


## Parts Design
| **Solenoid Holder** | **Stepper Spacer** |
|--------|--------------|
| **Description:** In order to have a solenoid press each button we need a bracket to hold the solenoid upright. To make this part we took the mesurements of the cart that ran along the rails. Then using the dimensions of the solonoid we created a cylindrical holder that we are able to screw the threads of the solenoid into. | **Description:** Another problem we ran into was that the replacement steppers were a little bit longer than the original. This was not a problem for most of the replacements except the one for the x axis. we needed to design a part that would hold the stepper back just enough so that nothing would obstruct its rotation. putting this part in was incredibly difficult because it was really tight but ended up fitting. | 
| <img src="https://user-images.githubusercontent.com/71402927/226723091-04569b69-43ff-4de7-a1c6-aa458dda53b2.png" alt="wiring2" style="width:318px;"> | <img src="https://user-images.githubusercontent.com/112979288/217354597-351d8de1-489a-4bbc-abcf-782780c5e713.jpg?raw=true" alt="wiring2" style="width:318px;"> |
| **Evidence:** [Link](https://cvilleschools.onshape.com/documents/9e516a7f78c5ed6bf7303036/w/41e953797044e05bd9e8a00e/e/6943abbfb780bc1d2de1d966) | **Evidence:** [Link](https://cvilleschools.onshape.com/documents/9e516a7f78c5ed6bf7303036/w/41e953797044e05bd9e8a00e/e/6943abbfb780bc1d2de1d966)
| **Reflection:** This part worked very well, the solenoid screwed in perfectly. However the bracket did not fit perfectly into the cart so we had to do some filing to get it to fit properly. Another thing we realized after putting in the solonoid in was that the tip did not extend down far enough to press the keys. We could raise the keyboard up but then other keys would be pressed down by other parts of the 3D printer. I hindsight it would have been better to measure and plan out where everything would go. This would have prevented the issue with the bracket not properly fitting. | **Reflection:** Our original plan was to use the motors that were already in the MakerBot. however these motors were not compatible with the H bridges the engineering lab provided. They were technically compatible however with the H bridges in the Makerbot. We ended up removing the steppers entirely and replacing them with ones that were compatible with the H bridges in the lab. We also took apart some more of the MakerBot and removed the Steppers it came with, replacing them with the Steppers the lab provided. The lab steppers had a slightly longer shaft than the ones in the maker bot. As a result, the end of the shaft hit part of the plastic bracket on the x-stepper preventing it from turning. A spacer was used to offset the stepper so they would not touch. They solved the problem but it was a pain to put in place. The small space and our clumsy fingers lead to several frustrating hours. We could have done nothing to avoid this because we could not cut the end of a stepper shaft off to make it fit better.  |

| Solenoid in down position  | Solenoid in up position |
| ------------- | ------------- |
| <img src="https://user-images.githubusercontent.com/112979288/226721677-1324fcad-9c80-49d7-b6e7-bd6ef048a0c3.jpg" alt="wiring2" style="width:318px;"> | <img src="https://user-images.githubusercontent.com/112979288/226720964-acab377a-7198-40f2-a331-69bd18af13fd.jpg" alt="wiring2" style="width:318px;"> |
 

## Code and Wiring
#### Goal
The goal of this code was to use two potentiometers and a button to control the steppers and solenoid. The the code has set ranges that execute an action if the potentiometer value is in that range.For example if it is less than value x turn right, greater than x but less than y dont turn, and greater than y turn left. The solenoid can then be activated using a button and only if both the x and y steppers are stationary. The cons of this code are: it relies on you manually moving the solenoid over the key to press it, which could result in inprecise and slow typing.
#### Pseudo code template
* Setup and pin assignment
* start loop
* read potentiometer values
* if in middle range steppers dont move and if button is pressed activate solonoid
* if in left range move steppers left 1 step. This will repeat each run through the code so long as the potentiometer is still turned left.
* Otherwise turn the steppers right.
* Repeat code for both steppers on x and y axis. 
#### Evidence
``` C++
// Matt and Zachary makerbot code
// May 29 2023
// Code for controlling the steppers and solenoid
#include <Stepper.h>

Servo myServo;
Stepper stepperx(STEPS, 4, 5, 6, 7); //stepper pins
Stepper steppery(STEPS, 8, 9, 10, 11);
int buttonPin = 12; //Pin setup
int solenoidPin = 13;
int leftrange = 412; // Variable for potentiometer ranges
int rightrange = 611;
void setup()
{
  myServo.attach(servoPin);//Attaches the servo object to a pin
  pinMode(buttonPin, INPUT);
  Serial.begin(9600);
  Serial.println("Stepper test!");
  stepper.setSpeed(60);
  pinMode(solenoidPin, OUTPUT);
  
  }

void loop()
{ digitalWrite(solenoidPin=LOW);
  int sensorValuex = analogRead(A0); //reads potentiometer values
  int sensorValuey = analogRead(A1);
  Serial.println(sensorValuex); // prints the reading
  Serial.println(sensorValuey);
  if (rightrange > sensorValue1 > leftrange & rightrange > sensorValue2 > leftrange) {
    digitalRead(buttonPin); // Makes sure the potentiometer value for each stepper is in the middle range of variable
    if(buttonPin=HIGH) { // checks if the button is pressed
      digitalWrite(solenoidPin=HIGH); // Presses the key using the solenoid
      Serial.println(click); //
      digitalWrite(solenoidPin=LOW);
      Serial.println(release);
    } else {
      Serial.println(wrongspot);
    }
    continue; //Jumps back to start of void loop
  }
  if (sensorValuex < leftrange) { // if the potentiometer is turned to the left move the stepper 1 step left
    stepperx.step(1);             // this will repeat moving the belt to the left
    Serial.println(xleft);
    }
    else {
      stepperx.step(-1); // otherwise move the stepper right
      Serial.println(xright);
    }  
  if (sensorValuey < leftrange){
    steppery.step(1);
    Serial.println(yleft);
    }
    else {
      steppery.step(-1);
      Serial.println(yright);
    }
    
}
```
[Link to code](https://create.arduino.cc/editor/zsiller38/8c163371-1a76-42bb-82ac-ac71e4fa67b8)
#### Reflection
The code recived several revisions throughout the project. It was initially supposed to allow us to type a message and then the robot would move and type it back. We never figured out how we were going to do this partly because neither of us fully planned out the code and therefor did not know were to start. This idea was also scraped due to time limitations from delays while encorperating the steppers. We then tried a service called octoprint which would allow us to control a 3d printer from an app. We soon realized that this would mean we are essentially using 3d printer software to control our project and we felt we had lost are initl purpose for the project. Finally we reverted to a simple code in c++ because that is what we were most comfortable with. The code took only a couple of days to write but as said earlier we never tested it fully because we ran out of time. In hindsight we would have used python because even though we were less familiar with it, it would have been a good learning experience to prepare us for our PID project.

#### Wiring
| Image | Reflection |
| ----- | ------ |
| <img src="https://github.com/matthewbowling123/MakerBot-Project/blob/master/Media/Screenshot%202023-05-29%201.34.04%20AM.png?raw=true" alt="wiring2" style="width:500px;"> | The Wiring proved to be one of the more difficult parts of this project due to the unique wiring required for the Solenoid to work and for the stepper motors. We initially had the Stepper and Solenoid wired on seperate Arduinos so that we could work on both simultaneously. After getting both wiring diagrams to work with their respective codes we combined the wiring and code to put it on a singular Arduino Board. I would say overall the wiring was not as hard as the code itself but at times became very tedious. Thankfully we figured it out in time for the project. |

## Construction
Construction took a very long time and was filled with challenges. The steppers not fitting due to there long shaft tokk weeks to resolve. This could have been avoided with a more thorough proof of conceptWhen the deadline arrived we had gotten both steppers to move properly and we could control them with code. This also had it problems. When the cart slide along the y rail it kept getting caught on something. After cleaning the rail the problem was less sever. The solonoid was also mounted and fuctioning properly but we never saw both parts working in tandem with the code we had written.

| Working Stepper | Working Solenoid | Wiring | Final |
| ------ | ------- | ------ | ------ |
| <img src="https://github.com/matthewbowling123/MakerBot-Project/assets/112979288/462eccbd-fead-4424-a14d-f15414e4acb7" alt="wiring2" style="width:318px;"> |  <img src="https://github.com/matthewbowling123/MakerBot-Project/blob/master/Media/Solenoid.gif" alt="wiring2" style="width:318px;"> |  <img src="https://github.com/matthewbowling123/MakerBot-Project/assets/112979288/60ca0dba-5c48-45b8-88d8-8c40b5129857" alt="wiring2" style="width:318px;">| <img src="https://github.com/matthewbowling123/MakerBot-Project/assets/112979288/c6827c20-e20b-42ec-874a-e20bb86556ac" alt="wiring2" style="width:318px;">


Final assembly images

## Final Reflection
This project was incredibly difficult and we needed more time on it. However it was a wonderful learning expierience in terms of figuring out how Steppers work. Overall we are glad we did this. In future projects involving Steppers we will definitly be returning to this project.
#### Problems
Our Robot arm encountered many issues throughout its design. First it was the steppers that came with the makerbot 3d printer. These steppers were not compatable with the H bridges we had in the Lab. Kaz and Graham tried to make use of the H bridges included in makerbot but they were unsuccessful. As a result we had to replace the steppers with ones from the lab. Although we had anticipated this it did add extra time to the project and created more issues. Secondly our original plan for pushing the keys did not work as intended. We planned that a servo would flick down to press each key, but after making a few prototypes we found that the range of motion of the servo was to limited and the shape of the keys made pressing each key perfectly very difficult. Both of these issues took weeks to resolve and poor time management meant we ran out of time before we could fully assemble the project.

#### Lessons Learned
This project started out very ambitious. We wanted to be able to type some text and get our robot to type that message back to us. This project might have tried to achive too much but in hindsight we think it was still possible if we were more efficent and did a better job managing our time. The initial plans got reduced to controling the steppers with two potentiometers which although it would work was not as elegant as our original plans. In conclusion the primary reason we did not fully complete this project was our poor time management and a few problem that derailed our workflow.

