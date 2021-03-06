# NBody
Animating simulation of celestial movement using standDraw library.

<img width="385" alt="planets" src="https://user-images.githubusercontent.com/83999326/135667454-e09f0b48-cb90-457c-8649-f3ca11e788a4.png">

## Description
- NBody is an animating simulator of celestial movement which allows users to input multiple planetary parameters via a text file to generate an animation of planetary movements based on Newton’s law of universal gravitation.
- Implemented with Model-View-Controller designing pattern in *Java*.


### How to run NBody?
To animating the simulation of celestial movement, run NBody class with command line arguments
- eg. `20000000.0 20000.0 data/planets.txt`.
  - the first arguement is the total running time, the second is the time difference will be incremented from 0. The animation will stop when it reach to the total running time.
  - The third arugment is a file stores 
    1. *the number of bodies*
    2. *the radius of the universe*
    3. *the position, velocity, mass and image path* 



*Through this simulator, we can also generate some very intersting animations like the images below.*

<img width="385" alt="dance10" src="https://user-images.githubusercontent.com/83999326/135667451-e715ecbb-69d9-4a7b-a660-b5520409c1b9.png">
<img width="385" alt="antimatter" src="https://user-images.githubusercontent.com/83999326/135667455-56afe730-322b-4d4e-9aab-d8b48455f30f.png">

## Classes and Algorithms
### Body
The Body class represents a celestial planet object, which is the core of the project. Its instances variables consists of all key information for simulating celestial movement.
* Instance Variables
  -  `xxPos` `yyPos` - the two-dimensional coordinate of the body.
  -  `xxVel` `yyVel` - the two-dimensional velocity of the body, together the form a velocity vector.
  -  `mass` - the mass of the body.
  -  `imgFileName` - the path of the corresponding image.

### Why it works?
The animation is formed by keep updating the status of all bodies in the universe, using StdDraw library. The key part is to make our update works correctly according to Newton's law.
- The `update` method is fulfilled by the methods below, which calculated the distance and force of this body and others.
  - `calcDistance`
  - `calcForceExertedBy`
  - `calcForceExertedByX`
  - `calcForceExertedByY`
  - `calcNetForceExertedByX`
  - `calcNetForceExertedByY`
- After the calculation, `update` will get the result of force as argument to update the instance variables of body object.



### Acknowlegement
Adapted from Project0: NBody of UCB CS61B-Data Structures course, taught by Josh Hug.
My solutions for other projects, labs and homeworks of this course can be found at [CS61B_20Fall_Assignments](https://github.com/qcwssss/CS61B_20Fall). 

