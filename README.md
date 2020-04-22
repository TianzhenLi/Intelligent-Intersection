# Intersection Management via V2I
The SUMO is used to simulate the traditional traffic lights, adaptive traffic lights, and the proposed V2I strategy.

## Simulation 1: Same traffic density on each lane
Vehicles are generated every 6 seconds with probability of 0.3 at the starting point of each lane. 

### Traditional phase-fixed light
![traditional_1](https://user-images.githubusercontent.com/51109877/79990231-611db180-84e3-11ea-9e1d-01dcb54a83aa.gif)

### Adaptive traffic light
![adaptive_1](https://user-images.githubusercontent.com/51109877/79991313-c0c88c80-84e4-11ea-9ba9-50ebcff4f76f.gif)

### The proposed V2I strategy
![v2i_1](https://user-images.githubusercontent.com/51109877/79983136-eac88180-84d9-11ea-977d-1c4306533049.gif)

## Simulation 2: Unbalanced traffic density
We set the number of vehicles coming from the north-south road much greater than that from the east-west road. In the simulation, a vehicle is generated for every 6 seconds with probability of 0.3 in the north-south direction, while with probability of 0.03 in east-west direction.

### Traditional phase-fixed light


### Adaptive traffic light
![adaptive_2](https://user-images.githubusercontent.com/51109877/79993426-56651b80-84e7-11ea-9d15-152bb21ed417.gif)



## Simulation 3: The influence of traffic density
In this part, we examine the influence of traffic density on the three IM strategies. The time intervals for generating a
vehicle are chosen as 3 seconds, 6 seconds, 9 seconds, and 12 seconds, all with probability of 0.3.

### 3 seconds
![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/3s/traditional-light.gif "traditional-light") 

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/3s/intelligent-light.gif "intelligent-light")

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/3s/intelligent-intersection.gif "intelligent-intersection")

### 9 seconds

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/9s/traditional-light.gif "traditional-light") 

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/9s/intelligent-light.gif "intelligent-light")

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/9s/intelligent-intersection.gif "intelligent-intersection")

### 12 seconds

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/12s/traditional-light.gif "traditional-light") 

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/12s/intelligent-light.gif "intelligent-light")

![image](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/gif/simulation3/12s/intelligent-intersection.gif "intelligent-intersection")
