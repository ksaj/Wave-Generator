# WHAT IS IT?
This is a 3D version of the 2D model Wave Machine. This model simulates wave motion in a membrane. The four edges of the membrane are fixed to a frame. A green rectangular area represents a driver plate that moves up and down, exhibiting sinusoidal motion.

# HOW TO USE IT

## Controls of membrane properties:

The FRICTION slider controls the amount of friction or attenuation in the membrane. The STIFFNESS slider controls the force exerted on a turtle by a unit deflection difference between the turtle and its four neighbors.

## Controls of the driving force:

The DRIVER-FREQUENCY slider controls the frequency at which the green area of the membrane (the driving force) moves up and down. The DRIVER-AMPLITUDE slider controls the maximum height of the green area of the membrane.

The DRIVER-X and DRIVER-Y sliders control the position of the driver. The DRIVER-SIZE slider controls the size of the driver.

# THINGS TO NOTICE

The membrane is made up of lines of turtles. Each turtle acts as it were connected to its four neighboring turtles by springs. In this model, turtles move only up and down – the force’s direction IS only up and down. The greater the distance between a turtle and its neighbors, the stronger the force.

When the green turtles move up, they “pull up” the turtles which are their neighbors, which in turn pull up the turtles which are their neighbors, and so on. In that way, a wave moves along the membrane. When the wave reaches the edges of the membrane (the blue turtles), the wave is reflected back to the center of the membrane.

The amplitude of the green turtles is fixed regardless of the stiffness of the membrane. However, moving a stiff membrane requires a lot more force to move it the same amount as an unstiff membrane. So even as the stiffness of the membrane is increased, the wave height will remain the same because the amplitude is kept the same.

# THINGS TO TRY

Try different membranes. Soft membranes have smaller stiffness values and hard membranes have larger stiffness values.

Try different driving forces, or try changing the frequency or amplitude. It is very interesting to change the size and the position of the driving force to see symmetrical and asymmetrical wave motions.

Try to create a “standing wave,” in which some points in the membrane do not move at all.

# EXTENDING THE MODEL

In this model, the movement of the turtles is only in the vertical direction, perpendicular to the membrane. Modify the model such that the movement is within the membrane plane, i.e. the x-y plane.

You can also try to add additional driving forces to make a multi-input membrane model. Another thing you can try is to apply different waveforms to the driving-force to see how the membrane reacts to different inputs. Try changing the overall shape of the driving force.

Try to build a solid model, that is, a model of waveforms within all three dimensions.

Instead of using amplitude to create the wave, change it to apply a fixed amount of force continuously.

# NETLOGO FEATURES

Note the use of the turtles-on reporter to find turtles on neighboring patches.

A key step in developing this model was to create an internal coordinate system. X, Y, and Z are just three turtles-own variables. You can imagine that turtles are situated in and move around in 3-space. But to display the turtles on the screen, which is two-dimensional, the turtle’s three coordinates must be mapped into two.

# CREDITS AND REFERENCES

Thanks to Weiguo Yang for his work on this model.

# HOW TO CITE

If you mention this model or the NetLogo software in a publication, we ask that you include the citations below.

For the model itself:

* Wilensky, U. (1996). NetLogo Wave Machine 3D model. http://ccl.northwestern.edu/netlogo/models/WaveMachine3D. Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.

Please cite the NetLogo software as:

* Wilensky, U. (1999). NetLogo. http://ccl.northwestern.edu/netlogo/. Center for Connected Learning and Computer-Based Modeling, Northwestern University, Evanston, IL.

# COPYRIGHT AND LICENSE

Copyright 1996 Uri Wilensky.

![](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png "")
 
This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 3.0 License. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-sa/3.0/ or send a letter to Creative Commons, 559 Nathan Abbott Way, Stanford, California 94305, USA.

Commercial licenses are also available. To inquire about commercial licenses, please contact Uri Wilensky at uri@northwestern.edu.

This is a 3D version of the 2D model Wave Machine. [EDIT: Also the 2D version for direct comparison]

This model was created as part of the projects: PARTICIPATORY SIMULATIONS: NETWORK-BASED DESIGN FOR SYSTEMS LEARNING IN CLASSROOMS and/or INTEGRATED SIMULATION AND MODELING ENVIRONMENT. The project gratefully acknowledges the support of the National Science Foundation (REPP & ROLE programs) – grant numbers REC #9814682 and REC-0126227.
 
