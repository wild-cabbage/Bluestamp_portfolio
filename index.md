# Three Joint Arm
<!--- Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails! -->
<!--- The three joint arm is a mechanical arm "connected" by servos and controlled using a joystick. -->

<!--- You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions: -->

<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->


| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Irene L | Stratford Preparatory Blackford | Electrical Engineering, Mechanical Engineering, and/or Computer Science | Rising/Incoming 7th

<!---**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**-->

![Headstone Image](Irene_L.pdf) 
<!---copy image uploaded to gh part, not main; just put the name :) -->
  
<!--- # Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE -->



## Second Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/6ezD6wMuPNM?si=VSegnzb60y6GBvxW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Progress

From the first to the second milestone, I have finished the assembly of the three joint arm. I used the code from last milestone to test the servos. 



### Challenges

A challenge was that the screw that was in the base (continuous) servo was too short, and it had only a few threads inside the servo, so the servo underrotated every time it was supposed to move to 180 degrees (when I was testing). I replaced it with a longer screw, and it stopped underrotating.

<!--- 

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone -->

## First Milestone

**The thumbnail is slightly interesting**

<iframe width="560" height="315" src="https://www.youtube.com/embed/tGmL5t1myjA?si=I-FYEx09ZaVeYxXU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<!--- For your first milestone, describe what your project is and how you plan to build it. You can include:
- An explanation about the different components of your project and how they will all integrate together
- Technical progress you've made so far
- Challenges you're facing and solving in your future milestones
- What your plan is to complete your project -->


### Progress

The first milestone was to have the joystick's movement control the servo's movement. The joystick's x-axis (in this case) can be read from pin A0, and the "signal" is sent to the servo, which is connected, with a data wire, to pin 7. In this code, if the "x value" (position of the joystick) is greater than 600, then the servo will go to 180 degrees, and if it is less than 300 the servo will go to zero degrees (it is set to 0 degrees at the start in void setup). I also printed the x-axis position of the joystick in the Serial monitor to track the movement and for troubleshooting purposes. 

### Challenges

1. The servos that I was using weren't really working initially with a test code that was moving the servo to 90 degrees and it moved about 10 degrees. I restarted the Arduino a few times and then it started working; it could be a software issue that fixed itself, and I need to monitor it in the future.
    
2. The delays in my starting code froze the Serial monitor--it would send approximately three values and then freeze for about thirty seconds, then send three more very slowly. I shortened delays about 50 ms (instead of 100 ms). This problem can carry onto the third milestone, as making the servo turn a certain degree is more difficult with less control. 

Afterwards I should be able to continue with assembling the three joint arm and then coding all four servos. 

<!--- # Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser, couldn't go into schematic diagrams, will do this later -->

### Code
<!--- Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. -->

```c++
#include "Servo.h"
Servo servo_one;
int pos = 0;
  

void setup() {


  servo_one.attach(7); //in case I need another servo


  Serial.begin(9600);
  servo_one.write(0);

}

void loop() {
  // put your main code here, to run repeatedly:  
  int xvalue = analogRead(A0); //joystick
  Serial.println(xvalue);
  
  
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
<!--- ## Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 
| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

-->

## Starter Project: RGB LED Slider kit
<iframe width="560" height="315" src="https://www.youtube.com/embed/qZ0iKe8ecOE?si=rf3ahFnXm_ps0_Ei" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>




The RGB LED kit uses three sliders, or linear potentiometers, to control the intensity and color of the LED. Linear potentiometers control resistance through linear motion, and there are essentially three smaller LEDs in a dome. Each slider/potentiometer sends voltage to the LED/LEDs, and this causes different brightness and colors. This RGB LED kit is essentially soldering practice, and the person soldering can be burnt because metal conducts heat quite well (and the sliders are metal), however this can be resolved by using something to prop it up. 

<!---elaborate-->



# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://circuitdigest.com/microcontroller-projects/controlling-multiple-servo-motors-with-arduino)
<!--- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/) -->

