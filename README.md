# DroneComponents
DroneComponents

##Index

1. [YU - The Hexacopter](https://github.com/yuthehexacopter/DroneComponents#yu---the-hexacopter-)
2. [The Blog](https://github.com/yuthehexacopter/DroneComponents#the-blog)
3. [Repository](https://github.com/yuthehexacopter/DroneComponents#repository)
4. [Important References](https://github.com/yuthehexacopter/DroneComponents#references)

Hi, I am Ankit. I am an Engineer. Recently I started an Insta handle @yuthehexacopter and posted some of the
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

[Back to top](https://github.com/yuthehexacopter/DroneComponents#dronecomponents)


### The Blog

A lot of people who have come accross have been asking me question regarding the making of a drone. So, In my blog today, I will take you for a rollar-coster ride about how you make your own copter with all the Components available in the market today and play with it. All your questions have been summed-up here and you can always connect with me on my [instagram](https://www.instagram.com/yuthehexacopter/).

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

7. [Companion Computers](https://github.com/yuthehexacopter/DroneComponents#companion-computers)
8. [IoT board - Arduino & ESP8266](https://github.com/yuthehexacopter/DroneComponents#iot-boards)
9. [LiDAR Sensor](https://github.com/yuthehexacopter/DroneComponents#lidar)

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
* Recommended: Propeller: "1045" OR "8045" Orange Propeller (CW & CCW)
* Recommended: Battery: 3S Orange LiPo (1800 - 3600mAh)
* Recommended: ESC: 15A - 40A.
* Recommended: Motor: 800-1100 KV (brushless dc motor)


[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Flight Controller

#### Pixhawk

![pixhawk!](/img/pixhawk.png "Pixhawk")

* Pixhawk is an independent open-hardware project that aims to provide the standard for readily-available, hiqh-quality and low-cost autopilot hardware designs for the academic, hobby and developer communities.
* Pixhawk supports many additional sensors and other devices via PX4 drivers

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

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)


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

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

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

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

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

### GPS Module

![GPS!](/img/gps.png "GPS")

#### Ublox Neo 7M GPS Module or Ublox Neo 8M GPS Module

Ublox Neo 7M GPS module that includes an HMC5883L digital compass. The new Ublox NEO 7 series is a high sensitivity, low power GPS module that has 56 channels and outputs precise position updates at 10Hz. This GPS module also comes with a molded plastic case which keeps the module protected against the elements making it ideal for use on your aircraft or quadcopter.

#### Features:

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

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

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

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Remote Controller

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Companion Computers

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### IoT Boards

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### LiDAR

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Repository

[Back to top](https://github.com/yuthehexacopter/DroneComponents#dronecomponents)

### References


[Back to top](https://github.com/yuthehexacopter/DroneComponents#dronecomponents)
