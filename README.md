# MakerBot Typer Project
This Project's goal was to use what was once a Makerbot 3D printer and reprogram it to do something else entirely. Our goal was to connect it with two keyboards and have it read so that whenever something was typed on one keyboard it would type it faster on the other. The problem this solved was helping Zack type faster on an online typing test.

<img src="https://user-images.githubusercontent.com/112979288/217347712-2c251434-4a55-4bea-a959-e4c4425f95dc.jpg?raw=true" alt="wiring2" style="width:318px;"> <img src="https://user-images.githubusercontent.com/112979288/217352139-2f6f64c7-9ace-4b89-bcd1-329e3a5a4a7f.jpg?raw=true" alt="wiring2" style="width:318px;">

### Table of Contents

## Planning
We started off this project with an old makerbot replicator 3D printer. After removing most of the unnecessary parts we began researching how it works.
### Stepper Intergration
Our original plan was to use the motors that were already in the MakerBot. however these motors were not compatible with the H bridges the engineering lab provided. They were technically compatible however with the H bridges in the Makerbot. We spent a good deal of time trying to figure out how they work. Due to another engineering student (Graham) frying them we ended up removing the steppers entirely and replacing them with ones that were compatible with the H bridges in the lab. We also took apart some more of the MakerBot and removed the Steppers it came with, replacing them with the Steppers the lab provided. The stepper size was NEMA-17.


### Typing Arm attachment
We also ran into a problem with changing the arm already on the printer due to it not being designed for typing. We ended up removing a large portion of it and replacing it with a 3D part and a servo that would be used as an arm to punch the keys. This initially did not work as the arm came in at an angle that did not press the keys right. So I designed an arm that came in at a better angle.
Another problem we ran into was that the replacement steppers were a little bit longer than the original. This was not a problem for most of the replacements except the one for the x axis. we needed to design a part that would hold the stepper back just enough so that nothing would obstruct its rotation. putting this part in was incredibly difficult because it was really tight but ended up fitting

<img src="https://user-images.githubusercontent.com/112979288/217354597-351d8de1-489a-4bbc-abcf-782780c5e713.jpg?raw=true" alt="wiring2" style="width:318px;">

## Parts Design
### Typing Arm Attachment
#### Purpose
We also ran into a problem with changing the arm already on the printer due to it not being designed for typing. We ended up removing a large portion of it and replacing it with a 3D part and a servo that would be used as an arm to punch the keys. This initially did not work as the arm came in at an angle that did not press the keys right. So I designed an arm that came in at a better angle.
#### Image
<img src="https://user-images.githubusercontent.com/112979288/217354597-351d8de1-489a-4bbc-abcf-782780c5e713.jpg?raw=true" alt="wiring2" style="width:318px;">
#### Evidence
[Link](https://cvilleschools.onshape.com/documents/9e516a7f78c5ed6bf7303036/w/41e953797044e05bd9e8a00e/e/c8e9a7781c4316b081b41bd0)
#### Reflection
This part is meant to press the keys. It was originally straight but when that version tried to press the keyes it hit them at an angle that was unable to press the keys.
### Stepper Holder
#### Purpose
#### Image
![thing](https://user-images.githubusercontent.com/112979288/217352737-ef97f164-0b01-4b9d-a98f-be0bfb9de4bc.png)
#### Evidence
[Link](https://cvilleschools.onshape.com/documents/9e516a7f78c5ed6bf7303036/w/41e953797044e05bd9e8a00e/e/6943abbfb780bc1d2de1d966)
This part was printed in order to hold the Servo on the Arm. It rests in  between the vertical parts and screws in perfectly.
#### Reflection
### Spacer
#### Purpose
Another problem we ran into was that the replacement steppers were a little bit longer than the original. This was not a problem for most of the replacements except the one for the x axis. we needed to design a part that would hold the stepper back just enough so that nothing would obstruct its rotation. putting this part in was incredibly difficult because it was really tight but ended up fitting.
![unnamed](https://user-images.githubusercontent.com/112979288/217354597-351d8de1-489a-4bbc-abcf-782780c5e713.jpg)
#### Image
#### Evidence
#### Reflection

## Wiring
#### Image
![image](https://user-images.githubusercontent.com/112979288/217928821-43becff0-1c39-4742-8a9c-8a6691fa268b.png)
#### Reflection

## Coding
#### Goal
#### Code
``` C++
#include <Stepper.h>

Servo myServo;
Stepper stepperx(STEPS, 4, 5, 6, 7);
Stepper steppery(STEPS, 8, 9, 10, 11);
int buttonPin = 12;
int servoPin = 3;
int servopush = 90;
int servoretract = 0;
int leftrange = 412;
int rightrange = 611;
void setup()
{
  myServo.attach(servoPin);//Attaches the servo object to a pin
  pinMode(buttonPin, INPUT);
  Serial.begin(9600);
  Serial.println("Stepper test!");
  stepper.setSpeed(60);
  myServo.write(servoretract);
  
  }

void loop()
{ int sensorValuex = analogRead(A0);
  int sensorValuey = analogRead(A1);
  Serial.println(sensorValuex);
  Serial.println(sensorValuey);
  if (rightrange > sensorValue1 > leftrange & rightrange > sensorValue2 > leftrange) {
    digitalRead(buttonPin);
    if(buttonPin=HIGH) {
      Servo.write(servopush);
      Serial.println(click);
      Servo.write(servoretract);
      Serial.println(release);
    } else {
      Serial.println(wrongspot);
    }
    continue;
  }
  if (sensorValuex < leftrange) {
    stepperx.step(1);
    Serial.println(xleft);
    }
    else {
      stepperx.step(-1);
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
#### Evidence
#### Reflection

## Final Reflection
#### Matt
#### Zac
