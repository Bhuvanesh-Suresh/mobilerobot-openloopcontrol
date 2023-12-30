# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step 1:

Use from robomaster import robot

### Step 2:

Choose the x,y,z - axis movement distance(meters).

### Step 3:

Give ep_chassis.move to move straight.

### Step 4:

Give time.sleep() for a break.

### Step 5:

Give ep_chassis.drive_speed to have a circular movement.

## Program
```
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.5, y=0, z=80, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=-1.6, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

   
    ep_chassis.move(x=0, y=0, z=55, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=1.4, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
    
    ep_chassis.move(x=0, y=0, z=45, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    
    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")
    
    ep_chassis.move(x=0, y=0, z=95, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=192,effect="on")

    ep_chassis.move(x=2.1, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=204,effect="on")

    ep_chassis.move(x=0, y=0, z=83, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=204,effect="on")


    ep_chassis.move(x=0.8, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)
![Screenshot 2023-12-30 195600](https://github.com/Bhuvanesh-Suresh/mobilerobot-openloopcontrol/assets/145742661/b7095844-d50b-42d2-aaa6-40b3b395d0d3)

## MobileRobot Movement Video:

https://youtu.be/8opPA__Ks38?si=Zxx4-HmyMrhUHc8V

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
