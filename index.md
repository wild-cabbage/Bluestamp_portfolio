# Three Joint Arm
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

<!--- You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions: -->

<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->


| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Irene L | Stratford Preparatory Blackford | electrical engineering, mechanical engineering, and/or computer science | Rising 7th

<!---**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**-->

# Cabbage
![Headstone Image](cabbage.jpeg) 
<!---copy image uploaded to gh part, not main; just put the name :) -->
Cabbage is pretty edible.
  
<!--- # Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone -->

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/tGmL5t1myjA?si=I-FYEx09ZaVeYxXU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<!--- For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project -->

The first milestone enacted upon emptiness was...to have the joystick's movement control the servo's movement, and yes. 

<!--- # Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser, couldn't go into schematic diagrams, will do this later -->

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
#include "Servo.h"
Servo servo_one;
int pos = 0;


  

void setup() {

   //pinMode (3, INPUT); //joystick position

  servo_one.attach(7); //in case I need another servo
  //pinMode (7, OUTPUT); //pos of servo

  Serial.begin(9600);
  servo_one.write(0);

}

void loop() {
  // put your main code here, to run repeatedly:  
  int xvalue = analogRead(A0); //joystick
  Serial.println(xvalue);

  /*int yvalue = analogRead (A1);
  int zvalue = analogRead (A3); */
  //servo.write(0);

  /*if (pos == 180) {
    pos = 0;
    servo.write(pos);
    delay(50);
  }
  */

  //testing code:
  /*
  for (int i = 0; i < 180; i++) {
    servo_one.write(i);

  }

  for (int i = 180; i>0; i--) {
    servo_one.write(i);

  }
  */

  //servo.write(0);
 //delay(500);
  //servo.write(180);

  
  
  if (xvalue > 600) {
    pos = 180;
    servo_one.write(pos);
   
    delay(50);
  }

  if (xvalue < 300) {
    pos = 0;
    servo_one.write(pos);

  
    delay(50);
  }
  
}

```
<!--- # Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 
| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

-->

# Starter Project: RGB LED Slider kit
<iframe width="560" height="315" src="https://www.youtube.com/embed/qZ0iKe8ecOE?si=rf3ahFnXm_ps0_Ei" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>



The RGB LED kit uses three sliders, or linear potentiometers, to control the intensity and color of the LED. Linear potentiometers control resistance through linear motion, and there are essentially three smaller LEDs in a dome. Each slider/potentiometer sends voltage to the LED/LEDs, and this causes different brightness and colors. This RGB LED kit is essentially soldering practice, and the person soldering can be burnt because metal conducts heat quite well (and the sliders are metal), however this can be resolved by using something to prop it up. 

<!---elaborate-->



# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here. 
