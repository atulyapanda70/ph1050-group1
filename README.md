# ph1050-group1

planets_300.csv: Generated a dataset of 300 planets using numpy and pandas. I sampled semi-major axis uniformly between 0.05 and 30 AU, while the host-star mass (\(M\)) was sampled between 0.5 and 1.5 solar masses. The orbital period (\(T\)) was calculated using Kepler's Third Law:
Semi major axis "a" sampled between 0.5 to 30 AU, while stellar mass between 0.5 to 1.5 AU. Then calculated orbital period using kepler's 3rd law. 
To account for measurement uncertainties also added 3% gaussian noise to calculated orbital periods. (used Claude to generate the code for this)

planets (1).csv: I generated a dataset of 300 planets using claude. I used the libraries pandas, numpy and sklearn to train the model on values of the timeperiod based on the semi major axis of the orbit and mass of the planets. The time period was calculated using kepler's thrid law. Upload the planets(1).csv file while running the file end sem - this covers the first subpart of part 3

part1_3.ipynb: This script simulates the orbits of our solar system's eight planets to calculate their exact orbital periods and compares them against real NASA data. Using NumPy for array calculation and handling, the code initializes each planet at its aphelion, the point furthest from the Sun with a starting velocity calculated from vis-viva equation. The core part of the simulation is the 4th-Order Runge-Kutta (RK4) function, which calculates the Sun's gravitational pull at each tiny time step and returns the planet's newly updated state specifically, its new position (x, y) and velocity (vx, vy) for the next state Because RK4 moves the planet in discrete jumps, the planet will inevitably step slightly past the exact finish line of a full orbit (y=0). To fix this, the script tracks the y-coordinate and uses linear interpolation to calculate the precise fraction of that final step where the planet actually crossed the line. Once that exact finish time is found, the code outputs a table showing how closely our simulated time period matches the actual observed one with absolute error. (LLM was used to get the table like structure and also it suggested the linear interpolation to get accurate time period) 

 



