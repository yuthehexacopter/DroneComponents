# DroneComponents
DroneComponents

##Index

1. [YU - The Hexacopter](https://github.com/yuthehexacopter/DroneComponents#yu---the-hexacopter-)
2. [The Blog](https://github.com/yuthehexacopter/DroneComponents#the-blog)
3. [Repository](https://github.com/yuthehexacopter/DroneComponents#repository)
4. [Important References](https://github.com/yuthehexacopter/DroneComponents#references)

Hi, I am Ankit. I am an Engineer. Recently, I started an Insta handle @yuthehexacopter and posted some of the
drone footages and snaps which I recetnly built.

### YU - The Hexacopter <a name="introduction"></a>

![YU Official Logo!](/img/yu_logo.png "YU Official Logo")

Introducing Vayu / YU / वायु is an educational purpose Artificial Intelligence (AI) based hexacopter created for research of drone for Indian Scenerios. YU is self made hexacopter for learners - skilled from beginners to advance level drone makers and enthusiasts, interested in both Hardware & Software side of development. The hardware side includes Electronics Components and Software side includes including Data Science (DS) / Machine Learning (ML) / Internet of Things(IoT) and Computer Vision(CV).

<img src="/img/snap01.png" alt="YU snap!" width="400"/>

Unmanned Arial Vehicle(UAV) is simplest structure which is designed to fly by a precalculated angular velocity and upward thrust. The fun part begins with automation. This particular drone is a flying linux computer. Infact a complete implemention of Artificial Intelligence (AI) that includes Machine Learning(ML), Computer Vision(openCV), and Internet of Things(IOT). The brain of UAV is usually a flight controller controlled by a Ground Control Station (GCS) - The remote control in your hand basically plus a laptop connected with telemetry in this case. BUT, when I put a bigger processing power above it, A Raspberry Pi, A Single Board Computer(SBC) in this case, the GCS fly with it, giving them instructions and collecting all the information without any manual intervention. NOW thats a perfect automation. 🤩🤩🤩

PYTHON + DRONEKIT + RASPBERRY PI + PIXHAWK + OPENCV + TENSORFLOW.

Drone built by @dwalkincamera
@contemplativeradicals.ai
follow the channel for Artificial Intelligence, Computer Vision & Internet of Things!

Connect with me on.
YU Instagram: https://www.instagram.com/yuthehexacopter/

#### Buy A Basic Drone Kit

I would recommend, there are tons of ways to build a quadcopter under a budget, so feel free to do your research before buying anything. Suggested (But not recommended), a basic kit below if you want to build a basic manually driven quodcopter.  

- <a href="https://amzn.to/3hZKu4a" target="_blank">Amazon</a>

[Back to top](https://github.com/yuthehexacopter/DroneComponents#dronecomponents)

### The Blog

A lot of people who have come across my instagram handle, have been asking me question regarding the making of a drone. So, In my blog today, I will take you for a rollar-coster ride about how you make your own copter with all the Components available in the market today and play with it. All your questions have been summed-up here and you can always connect with me on my [instagram](https://www.instagram.com/yuthehexacopter/).

Well let start with the List of the Components. You need the following items in our inventory to make your own Copter.
These components are common for Quadcopter / Hexacopter as a carrier or racing drones.

#### Basics

01. [Drone Theory](https://github.com/yuthehexacopter/DroneComponents#drone-theory)
02. [Local drone rules by concerned authority](https://github.com/yuthehexacopter/DroneComponents#drone-rules)
03. [Drone Frame](https://github.com/yuthehexacopter/DroneComponents#drone-frame)
04. [Flight Controller](https://github.com/yuthehexacopter/DroneComponents#flight-controller)
05. [Electronic Speed Controller](https://github.com/yuthehexacopter/DroneComponents#esc)
06. [Brushless Motors & Propellers](https://github.com/yuthehexacopter/DroneComponents#motors-and-propellers)
07. [Battery](https://github.com/yuthehexacopter/DroneComponents#battery)
08. [GPS Module](https://github.com/yuthehexacopter/DroneComponents#gps-module)
09. [Telemetry Module (Sender & Receiver)](https://github.com/yuthehexacopter/DroneComponents#telemetry)
10. [2.4 GHz 6 Channel Remote Control & Receiver](https://github.com/yuthehexacopter/DroneComponents#remote-controller)

#### Advanced

01. [Companion Computers](https://github.com/yuthehexacopter/DroneComponents#companion-computers--iot-boards)
02. [LiDAR Sensor](https://github.com/yuthehexacopter/DroneComponents#lidar)
03. [Power Module](https://github.com/yuthehexacopter/DroneComponents#power-module)

#### Accessories

01. [Landing Gear](https://github.com/yuthehexacopter/DroneComponents#landing-gear)
02. [Propeller Guard](https://github.com/yuthehexacopter/DroneComponents#propeller-guard)
03. [Raspberry PI Cover](https://github.com/yuthehexacopter/DroneComponents#raspberrypi-cover)

#### Software Requirements

01. [Mission Planner](https://github.com/yuthehexacopter/DroneComponents#mission-planner)
02. [QGroundControl](https://github.com/yuthehexacopter/DroneComponents#qgroundcontrol)
03. [DroneKit](https://github.com/yuthehexacopter/DroneComponents#dronekit)
04. [Ardupilot](https://github.com/yuthehexacopter/DroneComponents#ardupilot)

[Back to top](https://github.com/yuthehexacopter/DroneComponents#dronecomponents)

### Drone Theory

![Drone Motion!](/img/drone-motion.png "Drone Motion")

#### Vertical Motion

Drones use rotors for propulsion and control. The rotor can be considered as a fan which spins the  blades to push air down. All forces come in pairs, which means that as the rotor pushes down on the air, the air pushes up on the rotor. This is the basic idea behind lift, which comes down to controlling the upward and downward force. The faster the rotors spin, the greater the lift, and vice-versa.
A drone or UAV can do three things in the vertical plane: hover, climb, or descend. To hover, the net thrust of the four rotors pushing the drone up must be equal to the gravitational force pulling it down. Just increase the thrust (speed) of the four rotors so that there is a non-zero upward force that is greater than the weight. After that, the thrust can be decreased a little bit but there are now three forces on the drone: weight, thrust, and air drag. So, thrusters still have to be greater than just a hover. Descending requires doing the exact opposite. Simply decrease the rotor thrust (speed) so the net force is downward.

#### Turning (Rotating)

![Drone Rotation!](/img/drone-rotation.png "Drone Rotation")

##### Turning left

In this configuration, the red rotors are rotating counterclockwise and the green ones are rotating clockwise. With the two sets of rotors rotating in opposite directions, the total angular momentum is zero. Angular momentum is a lot like linear momentum, and you calculate it by multiplying the angular velocity by the moment of inertia. The angular momentum depends on how fast the rotors spin.

If there is no torque on the drone, then the total angular momentum must remain constant - zero in this case. The red counterclockwise rotors have a positive angular momentum and the green clockwise rotors have a negative angular momentum. I'll assign each rotor a value of +2, +2, -2, -2, which adds up to zero.

##### Turning Right:

If the angular velocity of rotor 1 decreased such that now it has an angular momentum of -1 instead of -2. The total angular momentum of the drone would now be +1. So the drone rotates clockwise so that the body of the drone has an angular momentum of -1. Decreasing the spin of rotor 1 did indeed cause the drone to rotate, but it also decreased the thrust from rotor 1. Now the net upward force does not equal the gravitational force, and the drone descends because the thrust forces aren't balanced, so the drone tips downward in the direction of rotor 1. To rotate the drone without creating all those other problems, decrease the spin of rotor 1 and 3 and increase the spin for rotors 2 and 4. The angular momentum of the rotors still doesn't add up to zero, so the drone body must rotate. But the total force remains equal to the gravitational force and the drone continues to hover. Since the lower thrust rotors are diagonally opposite from each other, the drone can still stay balanced.

##### Forwards and Sideways

Since the drones are symmetrical there is not much of a difference between forward, backward and sideways motion. Basically a quadcopter drone is like a car where every side is the front. In order to fly forward, a forward component of thrust is needed from the rotors. Here is a side view with forces of a drone moving at a constant speed.
Increase the rotation rate of rotors 3 and 4 (the rear ones) and decrease the rate of rotors 1 and 2. The total thrust force will remain equal to the weight, so the drone will stay at the same vertical level. Also, since one of the rear rotors is spinning counterclockwise and the other clockwise, the increased rotation of those rotors will still produce zero angular momentum. The same holds true for the front rotors, and so the drone does not rotate. However, the greater force in the back of the drone means it will tilt forward. Now a slight increase in thrust for all rotors will produce a net thrust force that has a component to balance the weight along with a forward motion component.

#### Flying Style

The flying style is very important before purchasing a drone flight controller. Since each flight controller is designed for the specific flying purpose, you must choose a one which suits your needs. There are 3 flying styles for a drone.

**Cinema flying:** This type of quad flight controllers serves the purpose of obtaining smooth videos. This type of flight controller has reduced flight characteristics and slow control stick rates.

**Autonomous flying:** A lot of flyers, especially beginners, look to fly the quadcopter without using too many controls. The autonomous drone controllers can do most of the work for you with its auto programmed feature. Eg, auto take-off, auto landing, one-click return home, etc.

**Sports flying:** Sports flying is the most advanced flying style and liked by most of the experienced users. In this mode, you have to make quick changes during flight and you would have to vary between very aggressive and very passive maneuvers. This type of flying helps you to do fast roll rates, 360 degree flips, hold a particular angle, etc. This is why a sports quadcopter flight controller is lovable by pro users.

##### Using a Computer

A type of computer control system which can simply push a joystick can be handled by a computer. Just as we are using a flight controller like Pixhawk and Arducopter in between. An accelerometer and gyroscope in the drone can further increase the ease and stability of flight by making minute adjustments in the power to each rotor. A GPS system can be added to get rid of the human entirely.

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Drone Rules

Before taking a fly, make sure you are aware and following all the local rules and norms related to drones from your country and you local authority. It is the most important respect the provacy of other and the security guideline of the country.

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Drone Frame

![Drone Quadcopter Frame!](/img/drone-frame-quad.png "Drone Quadcopter Frame")

Built from quality glass fiber and poly amide nylon.Integrated PCB connections for direct soldering of your ESCs and Pre-threaded brass sleeves for all the frame bolts.

* Width: 450mm
* Height: 55mm
* Weight: 282 grams (w/out electronics)

#### Features

* Made by advanced engineering material, super strong & smooth
* Easy to assemble and disassemble.
* The frame is tough and durable.
* The main glass fiber frame has good strength.
* The arm equips support ridges for better and faster forward flight.
* Features pre-threaded brass sleeves.
* Large mounting tabs for camera mounting.
* In-built power distribution board.
* Arm mounting holes: 3 mm.
* **Recommended:** Propeller: "1045" OR "8045" Orange Propeller (CW & CCW)
* **Recommended:** Battery: 3S Orange LiPo (1800 - 3600mAh)
* **Recommended:** ESC: 15A - 40A.
* **Recommended:** Motor: 800-1100 KV (brushless dc motor)

#### Buy Item

- Qudcopter Frame with landing gear
  - <a href="https://amzn.to/3567RVV" target="_blank">Amazon</a>
- Hexacopter Frame
  - <a href="https://amzn.to/2R4Jwb3" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Flight Controller

#### Pixhawk

![pixhawk!](/img/pixhawk.png "Pixhawk")

* Pixhawk is an independent open-hardware project that aims to provide the standard for readily-available, hiqh-quality and low-cost autopilot hardware designs for the academic, hobby and developer communities.
* Pixhawk supports many additional sensors and other devices via PX4 drivers

#### Buy item

- <a href="https://amzn.to/3hVSXVV" target="_blank">Amazon</a>

#### Arducopter (Discontinued)

![pixhawk!](/img/arducopter.png "Pixhawk")

* APM 2.6 is a revision of the APM that makes use of an external compass.
* The APM 2.6 has no on board compass, and is optimized for vehicles where the compass should be placed as far from power and motor sources as possible to avoid magnetic interference.
* APM 2.6 is designed to be used with the 3DR GPS uBlox LEA-6 with Compass module.
*	The GPS/Compass module may be mounted further from noise sources than the APM itself.
*	APM 2.6 requires a GPS unit with an on board compass for full autonomy.
*	For information on installing a 3DR GPS uBlox LEA-6 with Compass, visit 3DR Power Module.
*	The APM2.6 board is no longer supported for Copter. From Copter 3.3 firmware (and later) no longer fits on APM boards. The last firmware builds that can be installed (AC v3.2.1) can be downloaded from here: APM2.x and AMP1.x
*	The APM2.6 board is no longer supported for Plane. The last firmware build that fits on the APM is Plane 3.3.0.

#### List of other available flight controllers

1. The Naza-M V2 Flight Controller
2. DJI A3 Flight Controller
3. DJI N3 Quadcopter Flight Controller
4. Naza-M Lite Flight Controller
5. RJX Raceflight F4 Flight Controller
6. Crazepony F3 Flight Controller
7. Naze32 Rev 6 Flight Controller
8. KISS FC – 32bit Flight Controller V1.03

#### Buy item

- <a href="https://amzn.to/35193Kc" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### ESC

![ESC!](/img/esc.png "ESC")

An electronic speed control or ESC is an electronic circuit that controls and regulates the speed of an electric motor. It may also provide reversing of the motor and dynamic braking.

* Cut Off Voltage: 4V
* Current: 30A

#### Features

* High-quality MOSFETs for BLDC motor drive.
* Backward-polarity protection and protection on the 5V receiver line.
* High-performance microcontroller for best compatibility with all types of motors at greater efficiency.
* Fully programmable with any standard RC remote control.
* Heat sink with a high-performance heat transmission membrane for better thermal management.
* 3 start modes: Normal / Soft / Super-Soft, compatible with fixed-wing aircraft and helicopters.
* Throttle range can be configured to be compatible with any remote control available
in the market.

#### Buy Item

- <a href="https://amzn.to/358ZsAW" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Motors and Propellers

#### Brushless Motor

![Motor!](/img/motors.png "Motor")

Built with high-end magnets, a high pole count and custom motor mount.

* Length: 40 mm
* Width: 27.7 mm
* Shaft Diameter: 3.17 mm
* Item Weight: 53 grams

#### Features

*	The steel design is capable of withstanding competitive conditions.
*	Lightweight design makes them suitable for a wide range of quadcopters and Hexacopter Frames.
*	Compact size.
*	Offers great performance and value for money.
*	Smooth throttle response for best RC experience.

#### 1045/1045R propellers

This is 1045(10x4.5) SF Propellers Black. They are for lower RPM motor and slow flying drone models.
They have wide and thin blades in their size category which makes them much flexible in crash conditions where they do not break easily. 1045(10x4.5) SF Propellers Black especially draws larger currents and in results will give you a considerable amount of thrust.
1045(10x4.5) SF Props have high-quality propellers specially designed for multi-copters. 1045(10x4.5) SF Props has 15° angle design in the end of the propeller to avoid whirlpool multi-copter flying.

*	Material: Carbon Nylon
*	Thickness of center: 9.7mm
*	Length: 10 inch (25.4cm)
*	Slope: 4.5 inch (11.43cm)
*	Weight: 30 gms

#### Features:

*	Comes with thin and wide blades
*	1045(10x4.5) SF Propellers Black features epoxy resin cover.
*	It comes with a set of plastic reducers (2.75, 3, 3.17, 4, 4.70, 5, 6, 6.25 mm).
*	Quick to release, quick to attach
*	New design propellers, with greater aerodynamic efficiency, good lifting capacity.

#### Buy Item

- <a href="https://amzn.to/32WGfQf" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Battery

#### Lipo battery

Lithium Polymer batteries are a type of battery now used in many consumer electronics devices. They have been gaining in popularity in the radio control industry over the last few years, and are now the most popular choice for anyone looking for long run times and high power. LiPo batteries offer a wide array of benefits, but each user must decide if the benefits outweigh the drawbacks.

#### Pros

*	Light weight, and can be made in almost any size or shape.
*	High capacities, allowing them to hold much more power.
*	Much higher discharge rates, meaning they pack more punch.

#### Cons

*	Short lifespan; LiPos average only 150–250 cycles.
*	The sensitive chemistry can lead to fire if the battery gets punctured.
*	Need special care for charging, discharging, and storage.

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### GPS Module

![GPS!](/img/gps.png "GPS")

#### Ublox Neo 7M GPS Module or Ublox Neo 8M GPS Module

Ublox Neo 7M GPS module that includes an HMC5883L digital compass. The new Ublox NEO 7 series is a high sensitivity, low power GPS module that has 56 channels and outputs precise position updates at 10Hz. This GPS module also comes with a molded plastic case which keeps the module protected against the elements making it ideal for use on your aircraft or quadcopter.

#### Features

* Locate performance
* These are Pre-configured, Flashed with the correct settings, and tested. To make them Plug and Play.
*	Super Bright LED
*	Backplane with Standard Mk style mounting holes 45mm X 45mm
*	38400 bps (Default) Changed to 115200bps!
*	Output GGA, GSA and RMC frames
*	1Hz (Default) Changed to 5Hz!
*	Permanent Configuration Retention
*	compass on board
*	6 pin connectors for EZ connect to MEGA BLACK
*	4 pin connectors for only GPS use
*	4 pin connectors for compass only use
*	Can use both 4 pin at once.
*	56-channel
*	GPS L1 C/A, GLONASS L1 FDMA
*	QZSS L1 C/A
*	Galileo E1B/C
*	SBAS: WAAS, EGNOS, MSAS
*	10Hz update rate
*	25x25x2 Ceramic patch antenna
*	Rechargeable 3V Backup battery
*	Low noise 3.3V regulator
*	I2C EEPROM storage
*	Power and fix LED’s
*	Pedestal Mount/Case
*	Pixhawk/PX4 compatible
*	LNA MAX2659ELT+
*	Pre-configured 38,400 Baud and prams

#### Buy Item

- <a href="https://amzn.to/3lM2Nfl" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Telemetry

![Telemetry!](/img/telementary.png "Telemetry")

#### Single TTL 3DR radio telemetry

This Telemetry radio set allows you to link to a flight controller via a USB equipped device such as a computer, laptop or tablet supporting a USB connection (OTG). The Radio set not only lets you see live data such as live GPS position overlaid on a map (if the flight controller has the GPS option) to system voltage, heading, waypoint navigation even artificial horizon and so much more, using open source MAV link based ground station software.

#### Features

*	Very small size
*	Light weight (under 4 grams without antenna)
*	433Mhz frequency band
*	Receiver sensitivity to -117 dBm
*	Transmit power up to 20dBm (100mW)
*	Transparent serial link
*	Air data rates up to 250kbps
*	Range of approx 1 mile with supplied antennas
*	Demonstrated range of several kilometers with a small omni antenna
*	Can be used with a bi-directional amplifier for even more range
*	MAVLink protocol framing and status reporting
*	Frequency hopping spread spectrum (FHSS)
*	Adaptive time division multiplexing (TDM)
*	Support for LBT and AFA
*	Configurable duty cycle
*	Built in error correcting code (can correct up to 25% data bit errors)
*	Open source firmware
*	AT commands for radio configuration
*	RT commands for remote radio configuration
*	Adaptive flow control when used with APM
*	Based on the HopeRF HM-TRP radio module, featuring an SiLabs Si1000 RF microcontroller.
*	Upgraded to more convince Molex 1.25mm

#### Buy Item

- <a href="https://amzn.to/2Z4kpJx" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Remote Controller

![Remote Control!](/img/remote_control.png "Remote Control")

##### Flysky FS-i6 2.4GHz 6 Channel RX+ TX

This is the FlySky FS-i6 2.4G 6CH PPM RC Transmitter With FS-iA6B Receiver. This is a great entry-level radio for those just starting in the field of drones flying due to the ease of use of this product and an impressive list of features for a first-time radio. FlySky FS-i6 2.4G 6CH PPM RC Transmitter is a 6-channel telemetry 2.4GHz transmitter that uses the reliable Automatic Hopping Digital System (AFHDS) and includes such features as digital trims, backlit LCD screen, and simple programming.

#### Features

*	Entry-level 6 channel 2.4GHz radio with telemetry capability.
*	Dual Rate/Trims/Gear/Flap/Gyro Gain Adjust/Flight Mode/Throttle Hold/Hover Pitch Switches.
*	Easy to use Programming & Navigation Buttons.
*	Supports Heli/Standard Wing/Elevon/V-Tail.
*	20 Model Memory.
*	8 Character Model Name.
*	Trainer and charging ports.
*	The backlit LCD screen displays real-time transmitter and receiver voltage.
*	4 Stick Mode Selectable.
*	2 Modes.
*	It comes with a receiver.

#### Features of Transmitter

*	Model Type: Glider/Heli/Airplane
*	Band: 142
*	2.4ghz System: AFHDS 2A and AFHDS
*	Code Type: GFSK
*	DSC Port: PS2;
*	Output:PPM
*	Charger Port: No
*	ANT length: 26mm*2(dual antenna)
*	On-line update: Yes
*	Certificate: CE0678,FCC
*	Model Memories: 20
*	Channel Order: Aileron-CH1, Elevator-CH2, Throttle-CH3, Rudder-CH4, Ch 5 & 6 open to assignment to other functions.

#### Features of Receiver

*	Channel: 6.
*	Frequency Range: 2.4055–2.475 GHz.
*	Band Width Number: 140
*	Transmitting Power: ≤ 20 dBm.
*	RF Receiver Sensitivity: 105 dBm.
*	2.4G Mode: The second generation of an enhanced version of the automatic FM digital system.
*	Encoding: GFSK.
*	Antenna Length : 2 x 26 mm (dual antenna).
*	Input Power : 4.0 – 8.4 VDC (2A).
*	Dimension : 47 x 26.2 x 15 mm
*	Weight : 14.9 gm.
*	Data Acquisition Interface: Yes.
*	Model Type : Airplane / Glider / Helicopter.
*	Compatible Transmitter: Compatible with FS-i4, FS-i6, FS-i10, FS-GT2E, FS-GT2G.

#### Buy Item

- <a href="https://amzn.to/3gYbNKJ" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Companion Computers / IoT Boards

#### Raspberry Pi

The Raspberry Pi is a series of small single-board computers developed in the UK by the Raspberry Pi Foundation to put the power of computing and digital making into the hands of people all over the world. If at the beginning the aims of the Raspberry Pi project were leaned towards the promotion of teaching of basic computer science in schools and in developing countries, it rapidly expanded into a wider range of uses, as the original model became far more popular than anticipated, selling outside its target market for uses such as robotics. It is now widely used even in research projects, such as for weather monitoring because of its low cost and portability. It does not include peripherals (such as keyboards and mice) or cases. However, some accessories have been included in several official and unofficial bundles.

#### Buy Item

- <a href="https://amzn.to/2GsvwFS" target="_blank">Amazon</a>

#### List of Single board computers and IoT Boards

* ESP8266
* Raspberry Pi Zero
* Onion Omega2Plus	5
* BBC micro:bit
* Rock64 Media Board
* PocketBeagle
* Arduino Mega
* Le Potato
* Rock Pi 4 Model B
* Odroid-C4
* Pine A64-LTS
* Banana Pi
* Orange Pi 4B
* NanoPC-T3 Plus
* Odroid-XU4
* Asus Tinker Board S
* LattePanda
* Minnowboard Turbot Dual Ethernet
* BeagleBoard-X15

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### LiDAR

Lidar is a method for measuring distances by illuminating the target with laser light and measuring the reflection with a sensor. Differences in laser return times and wavelengths can then be used to make digital 3-D representations of the target. It has terrestrial, airborne, and mobile applications.

#### TFMini

<img src="/img/lidar.jpg" alt="Lidar" width="400"/>

The TFMini is a ToF (Time of Flight) LiDAR sensor capable of measuring the distance to an object as close as 30 centimeters and as far as 12 meters! As with all LiDAR sensors, your effective detection distance will vary depending on lighting conditions and the reflectivity of your target object, but what makes this sensor special is its size. Measuring only 42x15x16mm, the TFMini allows you to integrate LiDAR into applications traditionally reserved for smaller sensors such as the SHARP GP-series infrared rangefinders. The TFMini is easy to power at only 5V and easy to talk to using a 3.3V UART at 115200 baud.

#### Features

* Input Voltage: 5V
* Average Power: ≤120mW
* LED Peak Current: 800mA
* UART TTL Voltage: 3.3V
* Baud Rate: 115200 8N1
* Resolution: 5mm
* Minimum Detected Object Size at 2m: 20mm
* Operating Wavelength: 850nm
* Signal Acceptance Angle: 2.3°

#### Buy Item

- <a href="https://amzn.to/3lPTrPw" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Power Module

![Power Module!](/img/power-module.png "Power Module")

#### Plug Current Sensor

Voltage and current measurement configured for 5V ADC. 6-pos DF13 cable plugs directly to APM 2.5's 'PM' connector. Switching regulator outputs 5.3V and 3A max. The Power Module comes completely assembled with Deans connectors, and wrapped in shrink tubing for protection.

#### Buy Item

- <a href="https://amzn.to/3hUObYQ" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Landing Gear

![Landing Gear!](/img/landing-gear.png "Landing Gear")

This Plastic Landing Gear for Quadcopter is specially designed for the F450. It protects the frame during landing especially if you are using cameras for FPV. High-quality material which is very durable and heavy duty.

*	Material: ABS Plastic
*	Height: 150 mm
*	Width: 275 mm
*	Weight: 220 grams (with all included parts)

#### Features

*	Good-Quality Landing Gears
*	Provides 200 mm ground clearance
*	Skid proof landing gears
*	Compatible with Q450 and S500 and another large size frames

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Propeller Guard

![Propeller Guards!](/img/guards.png "Propeller Guards")

Propeller guard will protect the propellers from crashes like accidentally bumping into trees, walls, or any other obstacles.

*	Material: Plastic
*	Weight: 145 grams

#### Buy Item

- <a href="https://amzn.to/3gX8cMM" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Raspberrypi Cover

<img src="/img/rpiCover.jpg" alt="RaspberryPi Cover" width="400"/>

This is the cover I have used.

#### Buy Item

- <a href="https://amzn.to/2QQYNMf" target="_blank">Amazon</a>

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Mission Planner

![Mission Planner!](/img/mission-planner.png "Mission Planner")

**Software license:** Open Source
**Compatible OS:** Windows
**Description:** The Mission Planner is a ground control software  for ArduPilot created by Michael Oborne. Here are some

#### Features

*	Point-and-click waypoint entry, using Google Maps/Bing/Open street maps/Custom WMS.
*	Select mission commands from drop-down menus
*	Download mission log files and analyze them
*	Configure APM settings for your airframe
*	Interface with a PC flight simulator to create a full hardware-in-the-loop UAV simulator.
*	See the output from APM’s serial terminal

[Download](https://ardupilot.org/planner/docs/mission-planner-installation.html)

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### QGroundControl

![QGroundControl!](/img/qgroundcontrol.png "QGroundControl")

**Software license:** Open Source
**Compatible OS:** Windows,Mac, Linux/Unix, IOS & Android
**Description:** QGroundControl provides full flight control and mission planning for any MAVLink enabled drone. Its primary goal is ease of use for professional users and developers.

#### Features

*	Full setup/configuration of ArduPilot and PX4 Pro powered vehicles.
*	Flight support for vehicles running PX4 and ArduPilot (or any other autopilot that communicates using the MAVLink protocol).
*	Mission planning for autonomous flight.
*	Flight map display showing vehicle position, flight track, waypoints and vehicle instruments.
*	Video streaming with instrument display overlays.
*	Support for managing multiple vehicles.

[Download](http://qgroundcontrol.com/downloads/)

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### DroneKit

![DroneKit!](/img/drone-kit.png "DroneKit")

**Software license:** Open Source
**Compatible OS:** Windows,Mac, Unix & Android
**Language:** Python
**Description:** DroneKit offers an SDK and web API to easily develop apps for your drones. It is used for intelligent planning, Flight Automation and Live telementary. DroneKit also helps create powerful apps that communicate directly with MAVLink vehicles and python API. DroneKit makes it easy to create customized Android experiences for in-flight interaction using Android API.

[Download](https://github.com/dronekit/dronekit-python)

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Ardupilot

![Ardupilot!](/img/ardupilot.png "Ardupilot")

This is the full-featured, open-source multicopter UAV controller that won the Sparkfun 2013 and 2014 Autonomous Vehicle Competition (dominating with the top five spots). Copter is capable of the full range of flight requirements from fast paced FPV racing to smooth aerial photography, and fully autonomous complex missions which can be programmed through a number of compatible software ground stations. The entire package is designed to be safe, feature rich, open-ended for custom applications, and is increasingly easy to use even for the novice.

*	A Pixhawk or other autopilot loaded with the latest version of the Copter firmware.
*	Mission Planner software – gives you an easy point-and-click setup/configuration, and a full-featured ground control interface.
*	This Copter Wiki provides all the information you need to set up and operate a multicopter or traditional helicopter.
*	A suitable MultiCopter or Helicopter for your mission.
*	Plus many other useful options: e.g. data radios, which allow two-way wireless telemetry and control between the vehicle and your computer.

#### Multicopters:

*	Utilize differential thrust management of independent motor-prop units to provide lift and directional control
*	Benefit from mechanical simplicity and design flexibility
*	A capable payload lifter that’s functional in strong wind conditions
*	Redundant lift sources can give increased margin of safety
*	Varied form factor allows convenient options for payload mounting.

#### Helicopters:

*	Typically use a single lifting rotor with two or more blades
*	Maintain directional control by varying blade pitch via servo-actuated mechanical linkage (many versions of these craft exist and it is beyond the scope of this manual to cover them all – the mechanical systems used in helicopters warrant special study and consideration)
*	Strong, fast and efficient – a proven-worker suitable to many missions.

[Download](https://firmware.ardupilot.org/)

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

---

### Repository

Comming Soon!

[Back to top](https://github.com/yuthehexacopter/DroneComponents#dronecomponents)

---

### References

Check the following websites for updates and configuration documentations.

* [Pixhawk](https://pixhawk.org/)
* [Ardupilot](https://ardupilot.org/copter/index.html)
* [Drone Kit](https://dronekit-python.readthedocs.io/en/latest/)
* [QGroundControl](http://qgroundcontrol.com/)
* [Raspberry Pi](https://www.raspberrypi.org/)
* [Arduino](https://www.arduino.cc/)
* [Open CV](https://opencv.org/)
* [Python](https://www.python.org/)
* [Tensor Flow](https://www.tensorflow.org/)

[Back to top](https://github.com/yuthehexacopter/DroneComponents#dronecomponents)
