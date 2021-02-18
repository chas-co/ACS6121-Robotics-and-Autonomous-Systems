# ACS6121-Robotics-and-Autonomous-Systems
Control strategy for foraging and collision avoidance for EPuck robot in V-Rep.

# Overview
Your task is to design a control strategy for e-puck robots that do the following:
● explore the given environment to collect resources ( foraging );
● while foraging, avoid collisions between robots and with the environment boundary.
For an object to be collected, a robot's centre must be within 5 cm of the object's centre. There won't be
any collisions between the robot and the object.
For the evaluation of this task, two foraging scenarios will be considered:
1. with a single robot ;
2. with a group of 5 robots (all with an identical controller).
The controller used for both scenarios MUST be the same.
To assess the foraging performance of your strategy, you are expected to conduct 10 trials per scenario.
Each trial should last 60 seconds of simulation time (note that the actual time that elapses on your
watch/computer may be different.). Your report should include plots showing the number of objects
collected in total over time (average and standard deviation over 10 trials). Include one plot for each
scenario .
The simulation environment is shown in Figure 1. The simulations will be made using V-REP. An
introduction to V-REP is provided in the Week 1 Tutorial. You must use the simulation project provided on
MOLE ( scenes.zip ) as your starting point. Your are expected to design and implement a solution using
the routines available in the software. Important:
● Do not use wheel speeds the e-puck cannot achieve. That is, when using function
sim.setJointTargetVelocity(.,.), make sure the velocity argument is bounded by [-6.24, 6.24] .
● You should use the sensors available on the e-puck platform (e.g. camera, proximity). You may
implement additional sensors, however, these must not provide any global information (e.g.
absolute position or orientation) and you need to describe these in your report.
Each e-puck explores the environment in a circular motion looking for resources to gather. When the e-puck identifies a resource, it navigates towards the resource and collects it. If the e-puck identifies more than one resource, it moves towards the closest resource and collects it. The circular motion of the e-puck enables it to scan all areas of the environment with its camera for resources. 
Additionally, each e-puck avoids collision with the walls and other e-pucks. When an e-puck detects a wall or another object in front of it, it turns around. Figure 1 is the graphical representation of the control strategy for the e-puck. 

<img src="Flow_Chart.png" width="400" height="650" />
