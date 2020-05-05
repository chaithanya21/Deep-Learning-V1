<h1>Localization Using Kalman Filters</h1>

All self-driving cars go through the same series of steps to safely navigate through the world.
The First Step to safely navigate around the world  is <b>localization</b>. Before cars can safely navigate, they first use sensors and other collected data to best estimate where they are in the world.

<h2>1. Initial Prediction</h2>

First, we start with an initial prediction of car’s location and a probability distribution that describes our uncertainty about that prediction.

Below is a 1D example, we know that the car is on this one lane road, but don't know its exact location.

<img src='https://github.com/chaithanya21/Deep-Learning-V1/blob/master/Computer%20Vision/Object%20Tracking%20and%20Localization/Kalman%20Filters/Kalman_Images/1.png' width='300' height='300' >

<h2>2. Measurement Update</h2>

We then sense the world around the car. This is called the measurement update step, in which we gather more information about the car’s surroundings and refine our location prediction.

Say, we measure that we are about two grid cells in front of the stop sign; our measurement isn't perfect, but we have a much better idea of our car's location.

<img src='https://github.com/chaithanya21/Deep-Learning-V1/blob/master/Computer%20Vision/Object%20Tracking%20and%20Localization/Kalman%20Filters/Kalman_Images/2.png' width='300' height='300' >

<h2>3.Prediction (or Time Update)</h2>

The next step is moving. Also called the time update or prediction step; we predict where the car will move, based on the knowledge we have about its velocity and current position. And we shift our probability distribution to reflect this movement.

In the next example, we shift our probability distribution to reflect a one cell movement to the right.

<img src='https://github.com/chaithanya21/Deep-Learning-V1/blob/master/Computer%20Vision/Object%20Tracking%20and%20Localization/Kalman%20Filters/Kalman_Images/3.png' width='300' height='300' >

<h2>4. Repeat</h2>

Then, finally, we’ve formed a new estimate for the position of the car! The Kalman Filter simply repeats the sense and move (measurement and prediction) steps to localize the car as it’s moving!

<img src='https://github.com/chaithanya21/Deep-Learning-V1/blob/master/Computer%20Vision/Object%20Tracking%20and%20Localization/Kalman%20Filters/Kalman_Images/4.png ' width='300' height='300'>
