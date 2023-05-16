# MakerBot Typer Project

### Table of Contents
- [Planning](planning)
- [Part Design](part_design)
- [Code](code)
- [Construction](construction)
- [Final Reflection](final_reflection)
## Planning
We started off this project with an old makerbot replicator 3D printer. After removing most of the unnecessary parts we began researching how it works.

<img src="https://user-images.githubusercontent.com/112979288/217347712-2c251434-4a55-4bea-a959-e4c4425f95dc.jpg?raw=true" alt="wiring2" style="width:318px;"> <img src="https://user-images.githubusercontent.com/112979288/217352139-2f6f64c7-9ace-4b89-bcd1-329e3a5a4a7f.jpg?raw=true" alt="wiring2" style="width:318px;">
### Objective
This Project's goal was to use what was once a Makerbot 3D printer and reprogram it to do something else entirely. Our goal was to connect it with two keyboards and have it read so that whenever something was typed on one keyboard it would type it faster on the other. The problem this solved was helping Zack type faster on an online typing test.

### Milestones
| Stage  | Date | Objectives
| ------------- | ------------- | ------------ |
| Research and Proof of Concept| 11/28-12/17 | Can we control steppers in the 3d printer or do we need to replace them. How are we going to press the keys. |
| Design  | 1/4-1/17 | Cad design for brakets |
| Building | 1/17-1/31 | Mount in the steppers and key pushing mechanism. |
| Coding | 1/31-2/10 | Code and test on individual parts |
| Final touches and documentation | 2/10-2/14 | Make sure everything is working |
### Stepper Intergration
Our original plan was to use the motors that were already in the MakerBot. however these motors were not compatible with the H bridges the engineering lab provided. They were technically compatible however with the H bridges in the Makerbot. We spent a good deal of time trying to figure out how they work. Due to another engineering student (Graham) frying them we ended up removing the steppers entirely and replacing them with ones that were compatible with the H bridges in the lab. We also took apart some more of the MakerBot and removed the Steppers it came with, replacing them with the Steppers the lab provided. The stepper size was NEMA-17.
### Solenoid
| Solonoid in down position  | Solonoid in up position |
| ------------- | ------------- |
| <img src="https://user-images.githubusercontent.com/112979288/226721677-1324fcad-9c80-49d7-b6e7-bd6ef048a0c3.jpg" alt="wiring2" style="width:318px;"> | <img src="https://user-images.githubusercontent.com/112979288/226720964-acab377a-7198-40f2-a331-69bd18af13fd.jpg" alt="wiring2" style="width:318px;"> |
 


### Typing Arm attachment
We also ran into a problem with changing the arm already on the printer due to it not being designed for typing. We ended up removing a large portion of it and replacing it with a 3D part and a servo that would be used as an arm to punch the keys. This initially did not work as the arm came in at an angle that did not press the keys right. So I designed an arm that came in at a better angle.


<img src="https://user-images.githubusercontent.com/112979288/217354597-351d8de1-489a-4bbc-abcf-782780c5e713.jpg?raw=true" alt="wiring2" style="width:318px;">

## Parts Design
| **Solonoid Holder** | **Stepper Spacer** |
|--------|--------------|
| **Description:** In order to have a solonoid press each button we need a bracket to hold the solonoid upright. To make this part we took the mesurements of the cart that ran along the rails. Then using the dimensions of the solonoid we created a cylindrical holder that we are able to screw the threads of the solonoid into. | **Description:** Another problem we ran into was that the replacement steppers were a little bit longer than the original. This was not a problem for most of the replacements except the one for the x axis. we needed to design a part that would hold the stepper back just enough so that nothing would obstruct its rotation. putting this part in was incredibly difficult because it was really tight but ended up fitting. | 
| <img src="https://user-images.githubusercontent.com/71402927/226723091-04569b69-43ff-4de7-a1c6-aa458dda53b2.png" alt="wiring2" style="width:318px;"> | <img src="https://user-images.githubusercontent.com/112979288/217354597-351d8de1-489a-4bbc-abcf-782780c5e713.jpg?raw=true" alt="wiring2" style="width:318px;"> |
| **Evidence:** [Link](https://cvilleschools.onshape.com/documents/9e516a7f78c5ed6bf7303036/w/41e953797044e05bd9e8a00e/e/6943abbfb780bc1d2de1d966) | **Evidence:** [Link](https://cvilleschools.onshape.com/documents/9e516a7f78c5ed6bf7303036/w/41e953797044e05bd9e8a00e/e/6943abbfb780bc1d2de1d966)
| **Reflection:** This part worked very well, the solonoid screwed in perfectly. However the bracket did not fit perfectly into the cart so we had to do some filing to get it to fit properly. Another thing we realized after putting in the solonoid in was that the tip did not extend down far enough to press the keys. We could raise the keyboard up but then other keys would be pressed down by other parts of the 3D printer. I hindsight it would have been better to measure and plan out where everything would go. This would have prevented the issue with the bracket not properly fitting. | **Reflection:** This part worked very well, the solonoid screwed in perfectly. However the bracket did not fit perfectly into the cart so we had to do some filing to get it to fit properly. Another thing we realized after putting in the solonoid in was that the tip did not extend down far enough to press the keys. We could raise the keyboard up but then other keys would be pressed down by other parts of the 3D printer. I hindsight it would have been better to measure and plan out where everything would go. This would have prevented the issue with the bracket not properly fitting. |


## Code
#### Goal
#### Evidence
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
#### Reflection

## Construction

## Final Reflection
This project was incredibly difficult and we needed more time on it. However it was a wonderful learning expierience in terms of figuring out how Steppers work. Overall we are glad we did this. In future projects involving Steppers we will definitly be returning to this project.

