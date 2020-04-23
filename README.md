# Intersection Management via V2I
The SUMO is used to simulate the traditional traffic lights, adaptive traffic lights, and the proposed V2I strategy.

## Simulation 1: Same traffic density on each lane
Vehicles are generated every 6 seconds with probability of 0.3 at the starting point of each lane. 

### Traditional phase-fixed light
![traditional_1](https://user-images.githubusercontent.com/51109877/80047354-cb643f80-853f-11ea-9437-4f00d159d119.gif)


### Adaptive traffic light
![adaptive_1](https://user-images.githubusercontent.com/51109877/80047366-d028f380-853f-11ea-8905-523031f1cf26.gif)


### The proposed V2I strategy
![v2i_1](https://user-images.githubusercontent.com/51109877/80047372-d4551100-853f-11ea-9a78-f535a3bc03ee.gif)


## Simulation 2: Unbalanced traffic density
We set the number of vehicles coming from the north-south road much greater than that from the east-west road. In the simulation, a vehicle is generated for every 6 seconds with probability of 0.3 in the north-south direction, while with probability of 0.03 in east-west direction.

### Traditional phase-fixed light
![traditional_2](https://user-images.githubusercontent.com/51109877/80047380-d919c500-853f-11ea-8614-eafc861514e3.gif)


### Adaptive traffic light
![adaptive_2](https://user-images.githubusercontent.com/51109877/80047385-db7c1f00-853f-11ea-8f48-72cafcf204db.gif)

### The proposed V2I strategy
![v2i_2](https://user-images.githubusercontent.com/51109877/80047387-de770f80-853f-11ea-8cb5-7aefc1b16781.gif)


## Simulation 3: The influence of traffic density
In this part, we examine the influence of traffic density on the three IM strategies. The time intervals for generating a
vehicle are chosen as 3 seconds, 6 seconds, 9 seconds, and 12 seconds, all with probability of 0.3.

### 3 seconds
#### Traditional phase-fixed light
![traditional_3s](https://user-images.githubusercontent.com/51109877/80047400-e636b400-853f-11ea-9dbd-3e9fa702d2da.gif)


![adaptive_3s](https://user-images.githubusercontent.com/51109877/80047406-e9ca3b00-853f-11ea-879d-9422fb42938d.gif)

#### The proposed V2I strategy
![v2i_3s](https://user-images.githubusercontent.com/51109877/80047408-ec2c9500-853f-11ea-8e94-6fc82b9a258a.gif)


### 9 seconds
#### Traditional phase-fixed light
![traditional_9s](https://user-images.githubusercontent.com/51109877/80047416-efc01c00-853f-11ea-8f9e-94f3cae352bd.gif)

#### Adaptive traffic light
![adaptive_9s](https://user-images.githubusercontent.com/51109877/80047421-f2bb0c80-853f-11ea-9704-6f51d07e0814.gif)

#### The proposed V2I strategy
![v2i_9s](https://user-images.githubusercontent.com/51109877/80047424-f64e9380-853f-11ea-9a3f-3318d0a4c223.gif)


### 12 seconds
#### Traditional phase-fixed light
![traditional_12s](https://user-images.githubusercontent.com/51109877/80047426-f9e21a80-853f-11ea-9cae-77dcdd115375.gif)


#### Adaptive traffic light
![adaptive_12s](https://user-images.githubusercontent.com/51109877/80047427-fcdd0b00-853f-11ea-8987-e48b1995f317.gif)

#### The proposed V2I strategy
![v2i_12s](https://user-images.githubusercontent.com/51109877/80047431-ffd7fb80-853f-11ea-85b1-e375e41efa4d.gif)
