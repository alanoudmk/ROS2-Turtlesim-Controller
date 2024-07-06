# Exploring the Turtlesim Package in ROS 2 Foxy

## What is Turtlesim Package in ROS2 Foxy?

The turtlesim package is a simple 2D robot simulator that comes bundled with ROS2 (and ROS1). It is primarily used for educational and demonstration purposes, allowing users to get familiar with the basic concepts of ROS2 without the need for physical hardware.

## Prerequisites

Before we begin, ensure that you have the following:

1.  ROS Foxy installed on your system.
    - [HERE](https://github.com/alanoudmk/Install-ROS2-Foxy-on-Ubuntu-20.04) is how to download it.
2.  Basic understanding of ROS concepts, such as nodes, topics, and messages.



*****

# Getting Started


### 1. Open a **Terminal**: 
   > Ctrl + Alt + T
  - OR
   > searching for **Terminal** in the application menu.



***


### 2. Set up your environment: 
- In the **Terminal**, run the following command:

  ```
  $ source /opt/ros/foxy/setup.bash
  ```

- After running this command, any ROS 2 commands you execute in the current terminal will use the ROS 2 Foxy environment.
- This is a crucial step before running any ROS 2 related commands, as it ensures that your system is properly configured to work with the ROS 2 Foxy distribution.



***



### 3. Start Turtlesim:

- Run turtlesim:

    ```
    $ ros2 run turtlesim turtlesim_node
    ```

- Here's what this command does:
    - Runs the turtlesim_node: start the turtlesim_node and launch the turtlesim application.
    - Launches the turtlesim GUI: The turtlesim_node will open a graphical window that displays a 2D plane with a turtle icon. This is the turtlesim environment where you can interact with the simulated turtle.
      
  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/403ec57d-af8e-4367-8391-ff4c9378c877" width="520" height="100">


  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/3acf9001-4cfe-49f2-a2b1-9f6153a0665c" width="200" height="100">




***



### 4. Use Turtlesim:
- Open a new **Terminal** window.
  > Ctrl + Alt + T
- Source ROS2 again: 
  
  ```
  $ source /opt/ros/foxy/setup.bash
  ```

- This will start the Turtlesim GUI and allow you to control the turtle using the keyboard.

  
  ```
  $ run turtlesim turtle_teleop_key
  ```
  
  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/89574278-2bf4-42fc-a1fa-bab060af94cc" width="440" height="100">

- Use the arrow keys on your keyboard to control the turtle.

  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/d929d337-16ce-4175-b1b9-4bc0e52a2694" width="150" height="150">



***




### 5. Install ROS2 Qt:

- rqt:
    - stands for "ROS2 Qt" and is built on the Qt framework, providing a modular and customizable GUI.
    - powerful GUI (Graphical User Interface) tool for interacting with and visualizing a ROS2 (Robot Operating System 2) system.
    - It allows users to easily access and interact with various ROS2 functionalities.
    - 
- Open a new **Terminal** window.
  > Ctrl + Alt + T
  
- Source ROS2 again: 
  
  ```
  $ source /opt/ros/foxy/setup.bash
  ```

- Install rqt:
  
  ```
  $ rqt
  ```

- When you run the rqt tool for the first time, the main window may appear <mark>**blank**<mark>.
    - This is normal behavior and not something to be concerned about.
- To access the Service Caller functionality:
    > Plugins  ->  Services  ->  Service Caller
    
<div align="left">
<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/6a67825a-ef99-42f2-b1f7-31f84f140882" width="350" height="100">
    
</div>

<div align="left">
<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/42875025-cac6-445e-bcdb-18d5431eeabc" width="150" height="150">
    
</div>


<div align="left">
<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/cdc7d52a-4928-479d-9141-64381e6d25e1" width="250" height="230">
    
</div>


***


### 6. Spawn Service (a new turtle):

- In the left pane of the Service Caller plugin, you should see the available services. Look for the ```/spawn``` service.
> Service  ->   /spawn
> 
<div align="left">
<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/183f93d4-cbe0-4b04-81de-36809bf951f3" width="500" height="40">
</div>


<div align="left">
<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/d600c43c-5f8b-455d-a0c4-f1a950eed9f7" width="250" height="140">
</div>

- In the right pane, enter the parameters for the new turtle:
<mark>**By Double-Clicking**<mark>
    - To identify the new turtle, assign it a unique name.
        - Ex, you could call it "turtle2".
    - Now, enter valid coordinates at which to spawn the new turtle>
        - x:=1.0
        - y:=1.0


  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/4c76dc97-d41d-4bef-a450-97065b3e59c4" width="250" height="100">



- **Finally**, Click the ``Call`` button to execute the ``/spawn`` service and create the new turtle:


  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/447c3cd5-aa62-48a5-a9ec-9a1a8947eba9" width="250" height="100">


- You should see this:


<div align="left">
  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/88e0ed40-1e86-4318-9301-23527f435bbd" width="260" height="80">  
</div>

<div align="left">
  <img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/925fac8a-6ec1-4e1f-ba6d-a861fbd44415" width="220" height="195">    
</div>



***


### 7. Set_Pen Service:

- In the left pane of the Service Caller plugin, you should see the available services. Look for the ```/spawn``` service.
> Service  ->   /spawn 


- ``Set_pen`` service in the ROS:
    - used to control the appearance and behavior of the "pen" used by a turtle-like robot in the Turtlesim simulation environment.
    -  allows you to modify the following properties of the turtle's pen:
          - 1. Color: You can set the red, green, and blue (RGB) color components of the pen's color, each ranging from 0 to 255.
          - 2. Width: You can set the width of the pen's line, in pixels.
          - 3. Off: You can turn the pen off, which means the turtle will not leave a trail as it moves.



***



### 8. Set the pen for turtle1:

- In the rqt GUI:

  > Plugins  ->  Services  ->   Service Caller  ->  /turtle1/set_pen

<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/b2820475-daf0-440b-b304-809306480723" width="280" height="160">

- In the left pane, look for the ``/turtle1/set_pen`` service.

<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/a091f8a4-3db0-4fdb-a15e-e2e72f9c1353" width="280" height="100">

- In the right pane, enter the desired pen parameters:
    - Ex:
      - r:=255    _# Red color component_
      - g:=0      _# Green color component_
      - b:=0      _# Blue color component_
      - width:=9  _# Pen width of 9 pixels_
      - off:=0    _# Pen is turned ON_
  
<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/4e0195ee-de11-4ab1-bbb8-73d50454c276" width="280" height="130">


-  Click the ``Call`` button to execute the ``/turtle1/set_pen`` service and update the pen settings for turtle1.

<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/fca27c56-89ed-4122-bed8-61a8b508f5e7" width="250" height="90">

- Return to the Terminal where ``turtle_teleop_key``is running.
- Use the arrow keys on your keyboard to control the turtle. you will see turtle1’s pen has changed to Red and has 8 width as shown:

<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/793edf1e-137b-42d7-ab6a-d98794e09bdd" width="250" height="210">


***


### 9. Move turtle2:

- <mark>**By Default**<mark> ,  this node controls the turtle1 instance, but we want to control the turtle2 instance that we just spawned. 

- Open a new **Terminal** window.
  > Ctrl + Alt + T
  
- Source ROS2 again: 
  
  ```
  $ source /opt/ros/foxy/setup.bash
  ```

- Move turtle2:
  
  ```
  ros2 run turtlesim turtle_teleop_key --ros-args --remap turtle1/cmd_vel:=turtle2/cmd_vel
  ```
  
- ``turtle_teleop_key`` node:  allows you to control a turtle in the turtlesim simulation using the keyboard.
- ``--ros-args --remap turtle1/cmd_vel:=turtle2/cmd_vel``  part of the command remaps the  ``turtle1/cmd_vel``  topic to   ``turtle2/cmd_vel``.

<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/2ae5c9fc-ab32-406a-8ca7-a2ee4d2f2136" width="310" height="120">

- This way, the keyboard inputs from the turtle_teleop_key node will be published to the turtle2/cmd_vel topic, allowing you to control turtle2.

<img src="https://github.com/alanoudmk/ROS2-Turtlesim-Controller/assets/127528672/c13a2b70-d1b8-459b-8495-79c1ed786b36" width="250" height="210">

 

