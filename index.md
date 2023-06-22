# BlueStamp Tabletop Robot
Hello, my name is Selina and for BlueStamp, my project is the tabletop robot. This robot can detect obstacles and can follow or avoid the object. This robot car can also line-track, following a specific path drawn on the floor. I seek to modify this robot to have the ability to allow wireless charging and to perform certain useful functions such as picking up certain objects.

| **Engineer** | **School** | **Mechanical Engineering** | **Grade** |
|:--:|:--:|:--:|:--:|
| Selina H | North Gwinnett High School | Mechanical Engineering | Incoming Sophomore


![Headstone Image](IMG_8778.JPG)
  
# Final Milestone
For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What do you hope to learn in the future after everything you've learned at BSE

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Second Milestone
For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# First Milestone
For my first milestone, I was supposed to code the Arduino before building the robot. However, the USB was not compatible with my computer as I did not have an adapter. Since coding was not a choice for me, I decided to build the robot before I receive the adapter. I opened my robot kit and looked at each individual part and its functions. After looking up their key functions and how they work, I assembled the robot to see all of the functions working together and the wiring going to their corresponding places. There are different colored wires and the order of how it is plugged in played an important role in the energy flow which for example, determined the direction the motor spun. When the wires are flipped, the motor spins in the opposite direction than before. Overall, the hardest part of the kit was not being confused about the orientation of the black and red wires, but building the kit was successful. For my next milestone, I want to start coding the Arduino and research some modifications I can work with on the robot car.

<iframe width="560" height="315" src="https://www.youtube.com/embed/BDyy4Iachg8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

# Schematics 
[Headstone Image](Screenshot 2023-06-22 at 2.56.10 PM.png)
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resources to create professional schematic diagrams, though BSE recommends Tinkercad because it can be done easily and for free in the browser. 

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
| Elegoo Smart Robot Car Kit V4.0 | This is used for to build the robot car | $Price | <a href="https://www.amazon.com/ELEGOO-Tracking-Ultrasonic-Intelligent-Educational/dp/B07KPZ8RSZ/ref=sr_1_1_sspa?crid=3464RQUK2O87S&keywords=elegoo+smart+robot+car+kit+v4.0&qid=1687461310&sprefix=elegoo+smart+ro%2Caps%2C158&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Wireless Spy Camera | This camera allows the person to view the robot no matter where they are | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|
| LED Lights | What the item is used for | $4.99 | <a href="https://www.amazon.com/MCIGICM-Circuit-Assorted-Science-Experiment/dp/B07PG84V17/ref=sr_1_3?crid=P23LQ60BH549&keywords=led+lights+for+arduino&qid=1687461479&sprefix=led+lights+for+arduino%2Caps%2C119&sr=8-3/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Motion Sensor Light | What the item is used for | $6.99 | <a href="https://www.amazon.com/Stemedu-HC-SR501-Infrared-Raspberry-ESP32-Cam/dp/B0897BMKR3/ref=sr_1_4?crid=1X7WLM791MEL9&keywords=motion+sensor+light+for+arduino&qid=1687461749&sprefix=mtion+sensor+light+for+arduino%2Caps%2C103&sr=8-4/"> Link </a> |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
|:--:|:--:|:--:|:--:|

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
