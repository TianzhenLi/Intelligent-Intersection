# Intersection Management via V2I
The SUMO is used to simulate the traditional traffic lights, adaptive traffic lights, and the proposed V2I strategy. You can reproduce these results on your computer .

## Install
### Dependencies
You need dependencies below.
* Python3
* Plexe: Plexe added elements related to platooning to facilitate the construction of the Platooning scene. Plexe-sumo also provides a [Python API](https://github.com/michele-segata/plexe-pyapi) that can be called in Python as a module, making programming easier. Further details on Plexe can be found on the [Plexe website](http://plexe.car2x.org/).

### Install SUMO
The system we use is Ubuntu. If you use Ubuntu, you can install it directly as follows. If not, check out the [SUMO](https://sumo.dlr.de/docs/Downloads.php). 
SUMO is already in Ubuntu's official repo and can be installed directly using the following command:

<table><tr><td bgcolor=gray>1. sudo apt-get install sumo sumo-tools sumo-doc</td></tr></table>

If you need a up-to-date ubuntu version, you can add:

<table><tr><td bgcolor=gray>1. sudo add-apt-repository ppa:sumo/stable</td></tr></table> 

<table><tr><td bgcolor=gray>2. sudo apt-get update</td></tr></table> 

<table><tr><td bgcolor=gray>3. sudo apt-get install sumo sumo-tools sumo-doc</td></tr></table>

We can use SUMO to simulate many actual traffic scenarios. SUMO is not a single program, but contains multiple packages/applications. It mainly includes the following applications:

![SUMO application](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/picture/SUMO%20Application.png)

You can go to [SUMO-Application](https://sumo.dlr.de/docs/index.html) to learn the details.

Within each policy folder, there are the corresponding network information file.

![cfg-file](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/picture/cfg-file.png)

If you want to learn the meaning of each file, or if you're interested in editing the network yourself, you can check out the [SUMO tutorial](https://sumo.dlr.de/docs/Tutorials/quick_start.html).

## Run the program
Once SUMO and python3 are installed, you can run the program.
For examples, enter the folder 'traditional_traffic' and use python3 to run the main program.
<table><tr><td bgcolor=gray>1. cd traditional_traffic</td></tr></table>
<table><tr><td bgcolor=gray>2. python3 runner.py</td></tr></table>

This program will run the results in Simulation1; If you want to get the results in Simulation2, then you need to run the corresponding program in the folder ‘uneven’; If you want to get the result in Simulation3, then you need to modify the parameter ‘ADD_PLATOON_STEP’ in the main program to 300, 900 or 1200.

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

## Data analysis
When you start to run SUMO, right-click on the SUMO interface and select ‘show parameter’ to view the current vehicle related information parameters.
![Parameter](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/picture/parameter.png)

We have added statements in the main program so that the result can generate an XML file named'xx_output_file.xml' that contains all vehicle information. Analyzing this XML file, you can get the average delay time and its variance.

You can perform data analysis according to the [reference program](https://github.com/TianzhenLi/Intelligent-Intersection/blob/master/xml.etree.ElementTree.ipynb) given in this article. Different files only need to replace the file name in the program.

About the specific content of ‘xml.etree.ElementTree’, if you are interested, you can go to the [relevant website](https://docs.python.org/zh-cn/3/library/xml.etree.elementtree.html) to learn.
