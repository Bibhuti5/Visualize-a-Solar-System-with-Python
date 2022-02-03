# Visualize a Solar System with Python
In this article, I will explain to you how we can visualize the solar system with Python. There is a great selection of graphics libraries in Python that allows you to plot all major types of graphics so that you can visualize your data.
## Visualize The Solar System
I first thought to simply use the 3D Scatter plot by creating custom size markers for the Sun and planets. However, this was not ideal as the markers stayed the same size when zoomed in or out.

This led to unwanted effects such as Saturn’s rings inside the planet and the Sun engulfing all rocky inner planets once zoomed out. This meant that I had to find a different solution to display the Sun and the planets.

Fortunately, Plotly also offers a 3D surface plot that I could use for my celestial objects. However, this required drawing several spheres, each different in size and colour.

## Visualize Solar System: The Sun and Planets
To minimize the amount of coding required, I’ll define a function that will do the job of creating spheres for us. It is quite short, although it does require some knowledge of the spherical coordinate system. Alternatively, just accept that I will define the coordinates of a sphere as follows.

To draw a sphere, we will need to pass an array for the x, y and z coordinates containing the points in space. Note that it is up to us to choose how many points we want to specify, however, if we choose too few, our sphere will not be as round as we would like.

In this case, we create two arrays containing 100 equally spaced points. Note that theta varies between 0 and 2pi while phi is between 0 and pi.

Once we have theta and phi, we simply calculate the x, y and z coordinates using the formulas above. Note, I used the size instead of the radius and also specified the distance which tells us the distance from the sun. This is how we can place our spheres in the right places.

Also note that Plotly requires a 2D array for the z coordinates, therefore, we have filled the first dimension with 1’s, with the second dimension conforming to the formula.

## Creating Orbits
If you look up into the sky, you won’t see orbital lines everywhere. However, in solar system models, we like to draw orbits. Now I will define a new function that we can use for both, orbits as well as for drawing rings around the Saturn:.

## Now Let’s Visualize The Solar System
Now that we have all the little functions to help us out, we can put it all together and create the entire graph. Here is the code to visualize the solar system with Python.

We start by creating a few lists that contain the distance from the Sun and the diameter of celestial objects. Note that we had to reduce the size of the Sun by making it much smaller otherwise it would have made it too big for our graph.
While we have maintained the scale to ensure that the sizes of the planets are correct relative to each other, the Sun is not. In addition, the distance of the planets is to scale, for example, Jupyter is 7 times farther from the Sun than Venus.
However, we did not maintain the scale between the planets and the distance to the Sun because we expressed the diameter in kilometres while the distance was expressed in millions of kilometres.
Then we just use the functions defined previously to create traces for each sphere and orbit, including a few rings around Saturn.


# Bibhuti Bhusan sahoo

Portfolio:- https://bibhutiport.blogspot.com/
Github:- https://github.com/Bibhuti5
Linked In:- https://www.linkedin.com/in/bibhutibhusansahoo97/