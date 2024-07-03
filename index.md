# Knee Rehab Monitor

<!---
Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
-->

<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->


| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Arjun V | Las Lomas High School | Mechanical Engineering | Incoming Junior

<!---**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**-->

<img src="Arjun_V.png" width="305" height="400">
  
<!---# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE-->



# Second Milestone

<iframe width="745" height="419" src="https://www.youtube.com/embed/CIAtUQvTl04" title="Arjun V.  Second Milestone" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<p>My second milestone was to add bluetooth to my Arduino, so it could display data on the serial monitor without having to be connected, adding a powerbank to power the whole thing, and then soldering it and attaching it to my knee sleeve. 

<p>My first step was to attach bluetooth to my Arduino. I wired it to the breadboard and Arduino, and connected it to my computer. I wired VCC to +5V, Ground to GND, TX to RX and RX to TX on the Arduino. TX means transmitter, and RX means receiver, so when wiring, the receiver of the one device goes to the other device’s transmitter. If you connected TX to TX, then there would be no way to receive the transmitted data. How the module itself works is by connecting to another device by emitting low-energy radio waves. The reason for adding this to the project was so I could see the flex sensor and accelerometer data without having to use a wired connection, making the project overall more useful.

<p>At this point, I also had to add the power bank so the whole project could be powered without being connected to my computer. The power bank I used was the Anker PowerCore. It has more than enough capacity (5000 mAh) so it can power the device for 100 hours. This way I could connect my bluetooth to see if the data would print without a wired connection.

<p>One of my challenges was that I wasn’t able to connect to my computer with the HC05. In the room, many people used the same bluetooth module, so the first obstacle was even connecting to the module that was mine. For half the day, I connected to all the modules, have none of them connect to my computer, then have to forget all of them and re-pair all of them again.

<p>After pairing to one module, mine began to blink which indicated it was paired. After that I named the module “arjun HC05” in the device settings of my Mac. Now, the data would print on the serial monitor.

![HC05](HC-05-Bluetooth-Module-Pinout.png)

<p><i>Figure 5; <a href="https://components101.com/wireless/hc-05-bluetooth-module">Components 101, HC-05 - Bluetooth Module</a> -  This image shows where the wires go on the HC05</i>

<p>After I attached the bluetooth module, all my components were attached and working. This meant I could solder everything so it was permanently connected. I got a new proto board, and began adding the components and soldering it from underneath it. The proto-board helped reduce the overall size of the project, making it more functional. Aside from a few minor mistakes, I got all the wires and components soldered onto the proto board, and now I just needed to test if everything still worked. The type of wire I chose to use for this was solid-core wire, and I made this choice because it would be easier to solder onto the proto board, and the higher degree of flexibility stranded-core wire offered was not required. One thing I learned to do while wiring was labeling my wire. This would save a lot of time in the future over confusion over which wire goes where.

<p>When soldering, I accidentally put a wire connected to the piezo buzzer that was supposed to be connected to digital port 2 to the 5v area. This caused the buzzer to constantly be on at a really high pitch whenever it was connected to power. However, this was a simple fix. I simply had to melt the solder that was on that wire and remove it with the solder sucker, and put it into the right port. Then, everything worked fine.

<p>After this, I attached everything to the knee sleeve. This part was simple, but tedious. I learned how to sew, and then I attached the parts one by one. First, I attached the proto board with all the wires on it, and I sewed the arduino next to it. After those two, I sewed the bluetooth module and accelerometer in place so they would not move around anymore.
  
![SewingHolesArduino](sewing.png)

![SewingHolesProto](image0.png)

<p>Figure 6; The circled holes are where I sewed the arduino down

<p>Then, the problem of how I would attach the flex sensor to the knee sleeve. The problem was that the knee sleeve stretched a lot when it was worn, so if I just put the flex sensor on the sleeve there was a risk of it breaking while the knee sleeve wanted to stretch. To combat this risk, I utilized a strip of neoprene fabric and put it over the sensor, sort of forming a tube for the sensor to fit in. This solved my issue because it let the flex sensor slide around as much as it wanted to, but it also held it down tight enough so I could measure its bend.

<p>Next, I will finish Milestone 3, in which I will make it so that the Arduino will be able to make the buzzer buzz when the accelerometer detects bad squat form. For example, if your knees bend inward, the accelerometer could read that position and tell the Arduino to make the buzzer buzz. I am looking forward to this because when I had a leg injury, something that told me when my knee was bent inward would have been very helpful.


# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/Q6NsCcsk8Xg?si=JDRZV4ocUAxqacnu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<p></p>My first milestone was to detect position using a flex sensor and accelerometer. My first step was to create a circuit with a flex sensor and two resistors. First, I looked at a 
<a href="https://learn.sparkfun.com/tutorials/flex-sensor-hookup-guide/all">schematic</a>
that called for a 47k resistor, and a 50k resistor was the closest round number to 47k. As there were no 50k resistors, I learned about resistors wired in parallel to fix this issue. Since the current has more ways to flow through the circuit, there is less resistance overall. Due to this, I ended up putting two 100k resistors in parallel to each other to fix this, because when you put the two resistors in the parallel resistor formula (1/Rt = 1/R1 + 1/R2), the total resistance of the two ends up being 50k. 
<p></p>After resolving my resistor issue, I had to learn how flex sensors work. I learned that the flex sensor has ink that has conductive particles in it, and the more the sensor bends the more resistance is measured across it.
 
![HowItWorksStraight](how-it-works-straight.png)
![HowItWorksBent](how-it-works-bent.png)
<p></p><i>Figure 1; <a href="https://learn.sparkfun.com/tutorials/flex-sensor-hookup-guide/all">Spark Fun, Flex Sensor Hookup Guide</a> - This graphic describes how a flex sensor has more resistance when it is bent.</i>

<p></p>The flex sensor is essentially a variable resistor. The problem is that an Arduino reads voltage. We can fix that by putting the flex sensor in a voltage divider circuit,then use the resistance that the flex sensor gives, use Ohm's law and find the voltage of it, which is something the Arduino can actually read. For example, if we take the formula V<sub>out</sub> = V<sub>in</sub> &times; ( R<sub>2</sub> / ( R<sub>1</sub> + R<sub>2</sub> ) ), and say the flex sensor is R<sub>2</sub>, if the resistance of it increases so does the V<sub>out</sub>. Therefore, if the flex sensor bends more and the resistance increases, so does the voltage out which the arduino reads.

<img src="itemeditorimage_6368822ab7fb6.png" width="300" height="300">

<i><p>Figure 3; <a href="https://resources.pcb.cadence.com/blog/voltage-dividers-operations-and-functions">Voltage Dividers: Operations and Functions</a> - This is a voltage divider circuit. For my project, Z2 would be the Flex sensor and Z1 would be the parallel resistors I talked about earlier.</i>

<p></p>This can be interpreted into the degrees the sensor is bending with some code. In the code, the flex sensor gives a value of 0 - 1023, then it is normalized. I calibrated the resistance for 0 degrees and 90 degrees, with STRAIGHT_RESISTANCE (0 degrees) being 13304.4 ohms and BEND_RESISTANCE (90 degrees) being 31319.56 using the map() function in the Arduino IDE. The function extrapolates the degree value to a different bend. Also, the flex sensor also can only be plugged into analog instead of digital because it has multiple values. When the sensor bends past 110 degrees, the buzzer goes off, which is the most your knees should bend when squatting.

<p></p>Next, I added the accelerometer. I found a way to display the position of the accelerometer on the serial monitor of the Arduino IDE using the Serial.print()function. After some research, I found the code and put that into the Arduino sketch with the flex sensor code. Next, I wired the accelerometer to the Arduino.

![HowItWorksAccelerometer](Accelerometers-04-fullsize.png)

<p></p>Figure 2; <a href="https://insights.globalspec.com/article/1263/specifying-an-accelerometer-function-and-applications">GlobalSpec, Specifying an Accelerometer: Function and Applications</a> -  This is how a accelerometer works.

<p></p>Some challenges I had were that I had to learn about parallel resistors to solve my resistor issue. This concept took me two days to grasp, but once I learned it it made my understanding of the circuit much better. I also had to learn how to get data from an accelerometer. I had no idea how to code this, but I was able to find some code online which made adding to my code much easier.
Up next is my second milestone. I plan on attaching the bluetooth module, so I can track the data from the accelerometer and flex sensor much easier.

# Schematics 
<i>Figure 4</i>; Milestone 1 Schematic - 
![Milestone1Schematic](MainProjM1.png)

<i>Figure 7</i>; Milestone 2 Schematic (Breadboard is supposed to be proto board, simply solder components onto proto board how breadboard is wired) -
![Milestone2Schematic](milestone2.png)

# Code
```c++
#include <MPU6050.h>
#include <Wire.h>
#include <I2Cdev.h>

MPU6050 mpu;
int16_t ax, ay, az;
int16_t gx, gy, gz;

struct MyData {
  byte X;
  byte Y;
  byte Z;
};

MyData data;


const int FLEX_PIN = A0; // Pin connected to voltage divider output
const int buzzerPin = 2;
// Measure the voltage at 5V and the actual resistance of your
// 47k resistor, and enter them below:
const float VCC = 4.98; // Measured voltage of Ardunio 5V line
const float R_DIV = 50000.0; // Measured resistance of 3.3k resistor

// Upload the code, then try to adjust these values to more
// accurately calculate bend degree.
const float STRAIGHT_RESISTANCE = 13304.4; // resistance when straight
const float BEND_RESISTANCE = 31319.56; // resistance at 90 deg

void setup() 
{
  Serial.begin(9600);
  pinMode(FLEX_PIN, INPUT);
  pinMode(buzzerPin, OUTPUT);

  Serial.begin(9600);
  Wire.begin();
  mpu.initialize();
  //pinMode(LED_BUILTIN, OUTPUT);
}

void loop() 
{
  // Read the ADC, and calculate voltage and resistance from it
  int flexADC = analogRead(FLEX_PIN);
  float flexV = flexADC * VCC / 1023.0;
  float flexR = R_DIV * (VCC / flexV - 1.0);
  Serial.println("Resistance: " + String(flexR) + " ohms");

  // Use the calculated resistance to estimate the sensor's
  // bend angle:
  float angle = map(flexR, STRAIGHT_RESISTANCE, BEND_RESISTANCE,
                   0, 90.0);
  Serial.println("Bend: " + String(angle) + " degrees");
  Serial.println();

  delay(500);

  if (angle >= 110) {
  tone(buzzerPin,50);
  } else {
    noTone(buzzerPin);
  }
  mpu.getMotion6(&ax, &ay, &az, &gx, &gy, &gz);
  data.X = map(ax, -17000, 17000, 0, 255 ); // X axis data
  data.Y = map(ay, -17000, 17000, 0, 255); 
  data.Z = map(az, -17000, 17000, 0, 255);  // Y axis data
  delay(500);
  Serial.print("Axis X = ");
  Serial.print(data.X);
  Serial.print("  ");
  Serial.print("Axis Y = ");
  Serial.print(data.Y);
  Serial.print("  ");
  Serial.print("Axis Z  = ");
  Serial.println(data.Z);
}

```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino Uno R3 | Microcontoller | $13 | <a href="https://www.amazon.com/ELEGOO-Controller-ATmega328P-CompatibleArduino/dp/B0B6VV7MS7/ref=asc_df_B0B6VV7MS7/?tag=hyprod20&linkCode=df0&hvadid=692875362841&hvpos=&hvnetw=g&hvrand=2388022148290709767&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9032183&hvtargid=pla-2281435180738&psc=1&mcid=e0097333ec013ec0a6c874e637b79075&hvocijid=2388022148290709767-B0B6VV7MS7-&hvexpln=73&gad_source=1"> Link </a> |
| BodyProx Knee Sleeve | Keeps All Components on Knee | $15 | <a href="https://www.amazon.com/gp/aw/d/B0987XN6QH/?_encoding=UTF8&pd_rd_plhdr=t&aaxitk=5aed513eac49a60526c6d9777d9d93db&hsa_cr_id=7875900910501&qid=1719864251&sr=1-1-9e67e56a-6f64-441f-a281 df67fc737124&ref_=sbx_be_s_sparkle_mcd_asin_0_mariomsg&pd_rd_w=qsSVr&content-id=amzn1.sym.8591358d-1345-4efd-9d50-5bd4e69cd942%3Aamzn1.sym.8591358d-1345-4efd-9d50-5bd4e69cd942&pf_rd_p=8591358d-1345-4efd-9d50-5bd4e69cd942&pf_rd_r=PA56EJATP874WHNCNE6H&pd_rd_wg=ihoKq&pd_rd_r=388c0a8d-3fca-4ec1-a970-cdcf8c7489c9&th=1"> Link </a> |
| Adafruit Long Flex sensor | Measures Bend of Knee | $18 | <a href="https://www.amazon.com/Adafruit-Long-Flex-sensor-ADA182/dp/B01BNNNS5Q/ref=sr_1_3?crid=1GEOF65S7SCLW&dib=eyJ2IjoiMSJ9.lhZF8xWpz39rDzMy73v TT23Ss_RjBfj1RB7kEAbJ9D0yBHgcKw1YMgsMIaCD6oj4egLyFTXzJPJROjBXBNuLyvP3hfVG8V9B_gtFq3L7mxpoS6d2cm8cA453b16MvFuDDX9kD9oJbk3173icFBHyeg2y1Vvlqp7qWjWgna1VVPTA_OUwnV1JetfY2OnlDWNX90LumgmwPODB1DZMXj6Kx2Tzoz5_4Zp1N0XQmSndWHGVCr9QXxmgB0P2268U5jbYeGzZgUcZSGgiQ8JObtVoiz5yTr6MRas9v0iQbuOp6U.q-rFWTMu_qQemed_1UjkLOc3NMOPC5JBJq03fSe7z5M&dib_tag=se&keywords=flex+sensor&qid=1719864423&s=industrial&sprefix=flex+sensor%2Cindustrial%2C138&sr=1-3"> Link </a> |
| Shillehtek MPU6050 | Accelerometer/Gyroscope | $10| <a href="https://www.amazon.com/Pre-Soldered-Accelerometer-Raspberry-Compatible-Arduino/dp/B0BMY15TC4/ref=sr_1_2_sspa?crid=CM7TEBWH5LIO&dib=eyJ2IjoiMSJ9.nQ-HfKOFyZoszrV3cxLK6tLh71T4Dx8jkRlVGhGj_VwMCeIYm-9LTdm85DpoJu1zh0nywPtx4TH5RhL8Z-Dze2fKh6NQv4hdiCWU70ldzvGRL0cRXElTh8IXOK45Kve48uzqOfYj4xRcReIj9blNK7ouqQJZkUzzGQP-Z4T4d34sV47Q78cE0ftOXOwW59uY_WEA2LdPn6S9FBtO29E9Kr-oWRQQg2XawN6RWeAWLrwyeMVOSFCFbOH8elVhz2Y6ewiAfOcbz70dHT_pC_78tWQrrrW7UdHvmuhcLSkrWhk.zaJyxNlLDGbpF6KYhgewIzE7xs7HMFwbHXO3tCVeyrA&dib_tag=se&keywords=mpu6050&qid=1719864499&s=industrial&sprefix=mpu6050%2Cindustrial%2C169&sr=1-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1"> Link </a> |
| Piezo Buzzer | Alerts User of Incorrect Form | $6 | <a href="https://www.amazon.com/Cylewet-Terminals-Electronic-Electromagnetic-Impedance/dp/B01NCOXB2Q/ref=sr_1_6?crid=2LHY512NYTX03&dib=eyJ2IjoiMSJ9.v9xp9jV7C-sQT7j4p0UIV_xVKzU8DDa55Zy7nzfVmYaimJdByrZMfNvEm2fHDR0za4DaPd8brwiVZEi-IHCgo2sBg8k3EJMcmg-sVR90kJcP9oOf8zSFh1iWZlw1PJrUObynF7hsFTlUl4Mjw1yLhEb5aveIgXUMHiN2P2TdYaKK_yFtrf95J7L5mXjX1oEvZH1Cnvc-xk1Nel5twsTKJkHHc66-oivwv6bs2SLxMd-EUIVOKxL7DltKGCHB1GZoH1BXVwGU2Y8otebOLO8e3y7KD-K5CpOcO4zjO47owcg.r5O90tcYn3TNrCpGtKRJVSosnV60zYqj_ue96Klj1DU&dib_tag=se&keywords=piezo+buzzer&qid=1719864686&s=industrial&sprefix=piezo+buzzer%2Cindustrial%2C134&sr=1-6"> Link </a> |
| 100k Resistors | Increases Resistance in Circut | $7 | <a href="https://www.amazon.com/Cylewet-Terminals-Electronic-Electromagnetic-Impedance/dp/B01NCOXB2Q/ref=sr_1_6?crid=2LHY512NYTX03&dib=eyJ2IjoiMSJ9.v9xp9jV7C-sQT7j4p0UIV_xVKzU8DDa55Zy7nzfVmYaimJdByrZMfNvEm2fHDR0za4DaPd8brwiVZEi-IHCgo2sBg8k3EJMcmg-sVR90kJcP9oOf8zSFh1iWZlw1PJrUObynF7hsFTlUl4Mjw1yLhEb5aveIgXUMHiN2P2TdYaKK_yFtrf95J7L5mXjX1oEvZH1Cnvc-xk1Nel5twsTKJkHHc66-oivwv6bs2SLxMd-EUIVOKxL7DltKGCHB1GZoH1BXVwGU2Y8otebOLO8e3y7KD-K5CpOcO4zjO47owcg.r5O90tcYn3TNrCpGtKRJVSosnV60zYqj_ue96Klj1DU&dib_tag=se&keywords=piezo+buzzer&qid=1719864686&s=industrial&sprefix=piezo+buzzer%2Cindustrial%2C134&sr=1-6"> Link </a> |
| DSD Tech HC-05 Bluetooth Module | Makes Monitor Able to Connect via Bluetooth | $10 | <a href="https://www.amazon.com/DSD-TECH-HC-05-Pass-through-Communication/dp/B01G9KSAF6/ref=sxin_16_pa_sp_search_thematic_sspa?content-id=amzn1.sym.bb5bd4b6-13f8-40e4-93bc-54b5ec1d9a4f%3Aamzn1.sym.bb5bd4b6-13f8-40e4-93bc-54b5ec1d9a4f&crid=ZH7SPS2M4YOW&cv_ct_cx=hc05+bluetooth+module&dib=eyJ2IjoiMSJ9.bSlJf7yGmFdK_yurhnUR1waUYkTrXwtjXCfVVPxX04FMnTul5bQ1fyu1GIC9Q9Cg.dGG2pIBfz8I8cKweIvvcoCi1Dp8AoEVnWBTMpqeJN3g&dib_tag=se&keywords=hc05+bluetooth+module&pd_rd_i=B01G9KSAF6&pd_rd_r=374f2b72-d008-4ebc-8223-472f142a8f69&pd_rd_w=apboR&pd_rd_wg=rlLyo&pf_rd_p=bb5bd4b6-13f8-40e4-93bc-54b5ec1d9a4f&pf_rd_r=3K27SVZJ2ZB65JDVHNJB&qid=1719864907&s=industrial&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=hc05+%2Cindustrial%2C120&sr=1-1-47f26250-4ef4-4791-82ee-5e64b96b83fb-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9zZWFyY2hfdGhlbWF0aWM&psc=1"> Link </a> |

| Assorted Single-Core Wires | Connections between Components | $15 | <a href="https://www.amazon.com/Electrical-7colors-spools-UL1007-breadboard/dp/B083DN5R61/ref=asc_df_B083DN5R61/?tag=hyprod-20&linkCode=df0&hvadid=692875362841&hvpos=&hvnetw=g&hvrand=8530834579962313816&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9032183&hvtargid=pla-2281435179978&psc=1&mcid=8b897963727d312e9a95e09793193a56&hvocijid=8530834579962313816-B083DN5R61-&hvexpln=73&gad_source=1"> Link </a> |


# Other Resources/Examples
<!---One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components. -->
- [Flex Sensor Hookup Guide](https://learn.sparkfun.com/tutorials/flex-sensor-hookup-guide/all)
- [MPU6050 Sensor Arduino Tutorial](https://www.youtube.com/watch?v=a37xWuNJsQI)
- [Specifying an Accelerometer: Function and Applications](https://insights.globalspec.com/article/1263/specifying-an-accelerometer-function-and-applications)
- [HC-05 - Bluetooth Module](https://components101.com/wireless/hc-05-bluetooth-module)
- [Serial Communication](https://learn.sparkfun.com/tutorials/serial-communication/wiring-and-hardware#:~:text=As%20such%2C%20serial%20devices%20should,other%2C%20and%20vice%2Dversa.)
- [Elegoo Uno R3](https://epow0.org/~amki/car_kit/Datasheet/ELEGOO%20UNO%20R3%20Board.pdf)



# Starter Project

<iframe width="560" height="315" src="https://www.youtube.com/embed/Xf_h2ZlMCag?si=Pgq-o5lSrfOtKBD6" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<p></p>My starter project is a microcontroller-based Arduino project. It buzzes when I press a button and an LED goes off when it detects motion.    
<p></p>There are 5 main components in this project. The parts consist of the Arduino itself, a button, a piezo buzzer, a green LED and a PIR motion sensor. The first input and output is the button and the piezo buzzer. The piezo buzzer works by applying voltage to a piezoelectric ceramic material. The voltage causes the material to deform and vibrate, making sound waves.

![PiezoBuzzerDiagram](1606313155-gsk-04-buzzer-understand.png)
<i>Figure 1</i> ; Photo from Arduino Sensor Kit - The image shows how the buzzer vibrates to produce a tone

<p></p>The button makes the piezo buzzer buzz at a tone of about 50 hz by closing the circuit and allowing the current to flow to the buzzer. 
<p></p>The second input and output are the PIR, or Passive Infrared motion sensor and the LED, or Light Emitting Diodes. A PIR sensor detects infrared radiation. It does this by sensing a heat source’s movements, which cause a pulse which the PIR sensor sends as a signal. When the sensor detects the heat source moving, the Arduino reads it and tells the LED to turn off. The Arduino can have code uploaded to it, and that tells the microcontroller what to do.

![PIRSensorDiagram](0118-pir_motion_sensor.jpg.png)
<i><p>Figure 2</i> ; Photo from Adafruit, Lady Ada - The image shows how the signal is generated. The heat sources passes through the detecting area and the PIR sensor registers that.

<p></p>I had a few major challenges, with the biggest one being the difficulty of uploading my code to the Arduino. The port for the Arduino would not show up on the Arduino software. Therefore I could not upload my fixed code. I tried many things to troubleshoot this issue. For example, I tried pressing the reset button on Arduino, removing and reinstalling the software, and even testing the cable and the USB-C adapter, but the issue ended up being more simple. After rewiring the board, I got it working again.
<p></p>Next, I will be working on my main project, the Knee Rehabilitation Monitor. The starter project gave me a good understanding of wiring, coding, and breadboards, so I am looking forward to my main project with this knowledge. The reason I chose my main project is because it looked like a helpful device for people with frequent knee injuries, like athletes or the elderly, and I think making something like the knee rehab monitor will help me find and make other ways to help in the future.

# Starter Project Schematics 

![SchematicForStarter](StarterSchematics2.png)
