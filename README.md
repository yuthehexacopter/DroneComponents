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

####Vertical Motion

Drones use rotors for propulsion and control. The rotor can be considered as a fan which spins the  blades to push air down. All forces come in pairs, which means that as the rotor pushes down on the air, the air pushes up on the rotor. This is the basic idea behind lift, which comes down to controlling the upward and downward force. The faster the rotors spin, the greater the lift, and vice-versa.
A drone or UAV can do three things in the vertical plane: hover, climb, or descend. To hover, the net thrust of the four rotors pushing the drone up must be equal to the gravitational force pulling it down. Just increase the thrust (speed) of the four rotors so that there is a non-zero upward force that is greater than the weight. After that, the thrust can be decreased a little bit but there are now three forces on the drone: weight, thrust, and air drag. So, thrusters still have to be greater than just a hover. Descending requires doing the exact opposite. Simply decrease the rotor thrust (speed) so the net force is downward.

#### Turning (Rotating)

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


[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Drone Frame

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Flight Controller

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)


### ESC

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Motors and Propellers

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Battery

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### GPS Module

[Back to list](https://github.com/yuthehexacopter/DroneComponents#the-blog)

### Telemetry

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
