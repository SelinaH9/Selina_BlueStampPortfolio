# Surveilance Robot
Hello, my name is Selina and for BlueStamp, my project is the tabletop robot. This robot can detect obstacles and can follow or avoid the object. This robot car can also line-track, following a specific path drawn on the floor. I seek to modify this robot to have the ability to allow wireless charging and to perform certain useful functions such as picking up certain objects.

| **Engineer** | **School** | **Mechanical Engineering** | **Grade** |
|:--:|:--:|:--:|:--:|
| Selina H | North Gwinnett High School | Mechanical Engineering | Incoming Sophomore

![Headstone Image](IMG_8778.JPG)
  
# Final Milestone
For the final milestone, I reached the end of the finishing project. Instead of adding LED lights to the original Arduino. Instead, I added the lights to another Arduino that will function separately from the other one. The led lights will be activated by the motion sensor, which lights up the LED lights.

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Second Milestone
For the second milestone, I started by downloading the files from the Elegoo website. There were multiple challenges I faced, such as where certain files won't work. I solved this by getting help from other people and it worked out. After downloading the files for the Arduino, I wanted to start on my modifications, trying to add a motion sensor light and LED on the Arduino. However, the Arduino board on my robot was covered by the expansion board, which covered all of the pins that the LED could be inserted. This took a day to solve, so I took a different path to learn the Arduino. Learning about Arduino was interesting as if it was like reaching the brain of the software. After that, I continued working on the modifications but changed the original plan. For my third milestone, I hope to figure out a way to put the led lights on the robot, showing my understanding of circuits and Arduino.

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# First Milestone

For my first milestone, I was supposed to code the Arduino before building the robot. However, the USB was not compatible with my computer as I did not have an adapter. Since coding was not a choice for me, I decided to build the robot before I receive the adapter. I opened my robot kit and looked at each individual part and its functions. After looking up their key functions and how they work, I assembled the robot to see all of the functions working together and the wiring going to their corresponding places. There are different colored wires and the order of how it is plugged in played an important role in the energy flow which for example, determined the direction the motor spun. When the wires are flipped, the motor spins in the opposite direction than before. Overall, the hardest part of the kit was not being confused about the orientation of the black and red wires, but building the kit was successful. For my next milestone, I want to start coding the Arduino and research some modifications I can work with on the robot car.

<iframe width="560" height="315" src="https://www.youtube.com/embed/BDyy4Iachg8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Schematics 
<img width="780" alt="Screenshot 2023-06-22 at 3 24 42 PM" src="https://github.com/SelinaH9/Selina_BlueStampPortfolio/assets/136386424/ff2c752e-44f1-46a4-a728-bfe5fb6157ff">

<img width="791" alt="Screenshot 2023-06-22 at 3 25 21 PM" src="https://github.com/SelinaH9/Selina_BlueStampPortfolio/assets/136386424/ddfcee70-0083-4155-8f5a-b6b6236e21ce">

<img width="791" alt="Screenshot 2023-06-22 at 3 35 21 PM" src="https://github.com/SelinaH9/Selina_BlueStampPortfolio/assets/136386424/e34416fe-bd5c-456a-bad5-353a54a96f86">

<img width="791" alt="Screenshot 2023-06-22 at 3 35 48 PM" src="https://github.com/SelinaH9/Selina_BlueStampPortfolio/assets/136386424/44421956-5d00-444d-a0c6-7f3ef84e120a">


# Code
The link for the Arduino code cane be downloaded <a href="https://www.elegoo.com/pages/arduino-kits-support-files"> here </a>

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!")
    Application_FunctionSet.ApplicationFunctionSet_Init();
  wdt_enable(WDTO_2S);;
}

void loop() {
  //   wdt_reset();
  Application_FunctionSet.ApplicationFunctionSet_SensorDataUpdate();
  Application_FunctionSet.ApplicationFunctionSet_KeyCommand();
  Application_FunctionSet.ApplicationFunctionSet_RGB();
  Application_FunctionSet.ApplicationFunctionSet_Follow();
  Application_FunctionSet.ApplicationFunctionSet_Obstacle();
  Application_FunctionSet.ApplicationFunctionSet_Tracking();
  Application_FunctionSet.ApplicationFunctionSet_Rocker();
  Application_FunctionSet.ApplicationFunctionSet_Standby();
  Application_FunctionSet.ApplicationFunctionSet_IRrecv();
  Application_FunctionSet.ApplicationFunctionSet_SerialPortDataAnalysis();

  Application_FunctionSet.CMD_ServoControl_xxx0();
  Application_FunctionSet.CMD_MotorControl_xxx0();
  Application_FunctionSet.CMD_CarControlTimeLimit_xxx0();
  Application_FunctionSet.CMD_CarControlNoTimeLimit_xxx0();
  Application_FunctionSet.CMD_MotorControlSpeed_xxx0();
  Application_FunctionSet.CMD_LightingControlTimeLimit_xxx0();
  Application_FunctionSet.CMD_LightingControlNoTimeLimit_xxx0();
  Application_FunctionSet.CMD_ClearAllFunctions_xxx0();

}
```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Elegoo Smart Robot Car Kit V4.0 | This is used for to build the robot car | $79.99 | <a href="https://www.amazon.com/ELEGOO-Tracking-Ultrasonic-Intelligent-Educational/dp/B07KPZ8RSZ/ref=sr_1_1_sspa?crid=3464RQUK2O87S&keywords=elegoo+smart+robot+car+kit+v4.0&qid=1687461310&sprefix=elegoo+smart+ro%2Caps%2C158&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Wireless Spy Camera | This camera allows the person to view the robot no matter where they are | $29.99 | <a href="https://www.amazon.com/WAXOXIH-Security-Wireless-Smallest-Detection/dp/B0BVLXNY4V/ref=sr_1_1?crid=3UXJL392E812S&keywords=waxoxih+mini+spy+camera&qid=1687893035&sprefix=WAXO%2Caps%2C108&sr=8-1/"> Link </a> |
|:--:|:--:|:--:|:--:|
| LED Lights | The LED lights blink as the car moves in a specific direction | $4.99 | <a href="https://www.amazon.com/MCIGICM-Circuit-Assorted-Science-Experiment/dp/B07PG84V17/ref=sr_1_3?crid=P23LQ60BH549&keywords=led+lights+for+arduino&qid=1687461479&sprefix=led+lights+for+arduino%2Caps%2C119&sr=8-3/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Motion Sensor Light | The motion sensor lights are attached to sense human movements using infrared light | $6.99 | <a href="https://www.amazon.com/Stemedu-HC-SR501-Infrared-Raspberry-ESP32-Cam/dp/B0897BMKR3/ref=sr_1_4?crid=1X7WLM791MEL9&keywords=motion+sensor+light+for+arduino&qid=1687461749&sprefix=mtion+sensor+light+for+arduino%2Caps%2C103&sr=8-4/"> Link </a> |
|:--:|:--:|:--:|:--:|
| ELEGOO Breadboard Jumper Wire | The jumper wires are for connecting the motion sensor to the Arduino and to the LED light | $6.98 | <a href="https://www.amazon.com/Elegoo-EL-CP-004-Multicolored-Breadboard-arduino/dp/B01EV70C78/ref=sr_1_5?crid=1A4S8NIO2N5W6&keywords=jumper+wires&qid=1687893112&sprefix=jumper+wires%2Caps%2C109&sr=8-5/"> Link </a> |
|:--:|:--:|:--:|:--:|

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
