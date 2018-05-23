# car_filtering
Use filtering to achieve a more accurate representation of where the car is using GPS and IMU data. 

Use a kalman filter to estimate location of RC using data from the GPS and IMU. 

## The Model
States: 
- X Position  
- Y Position(t)  
- Velocity  
- Reference Angle  
- Angular Velocity  
       
### Continuous Model
d/dt(x) = v(t) * cos(theta(t))  
d/dt(y) = v(t) * sin(theta(t))  
d/dt(v) = 0  
d/dt(theta) = ...  
d/dt(theta_dot) = 0  

### Discrete Model
x(t+h) = x(t) + h * v(t) * cos(theta(t))  
y(t+h) = y(t) + h * v(t) * sin(theta(t))  
v(t+h) = v(t)  
theta(t+h) = theta(t) + h * theta_dot  
theta_dot(t+h) = theta_dot(t)  

