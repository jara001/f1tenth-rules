---
title: F1TENTH Rules
layout: page
section: race
---

<style>
.post ol {
  list-style-type: lower-alpha;
}

.post ol ol,
.post ul ol {
  list-style-type: lower-roman;
}
.post ol, .post ul, .post p {
  margin-bottom: 0rem;
}
h2, h3, h4, h5, h6 {
  margin-top: 1rem;
  margin-bottom: 1rem;
}
</style>

These rules are prepared for the German Grand Prix of the F1Tenth. Rules can be modified overtime.

**Table of content**
- ToC
{:toc}


# 1. General

International F1TENTH Autonomous Racing Competition is a racing competition open to teams of all levels. Competing teams may consist of any number of members; however, each participant should be a member of only one team. The competition is organized as an in-person event.

Teams can register for the competition using a [registration form](https://forms.gle/rTjyEu4NA9aojWBX8), where they select a single variant of the competition. Registration is open until July 31, 2021.


# 2. Competition

1. The competition will comprise three parts – *Inspection*, *Time
Trials* and *2 Vehicle Head-to-Head* race. Every participant must pass
qualification and will be automatically registered to both races.

2. Teams registered to the in-person competition need to provide and build a F1TENTH car by themselves according to the constraints listed below. In addition, each team must have a unique vehicle (i.e., a research lab may not field six teams with one car).

3. To increase the quality of the future F1TENTH competitions, the winner of each race is encourage to publish the code of their algorithm under an open-source license in the [F1TENTH repository](https://github.com/f1tenth) on Github.


## 2.1 Vehicle classes

1. The in-person competition distinguishes two vehicle classes: Restricted Class and Open Class.

2. **Restricted Class** allows only cars that meet the following constraints:

    1. The vehicle is constructed according to the official [bill of materials](https://f1tenth.readthedocs.io/en/stable/getting_started/build_car/bom.html). The teams are allowed to use components of similar or lower specifications.
    2. Each vehicle will be inspected as a part of qualification whether it meets the criteria. In case the criteria are not met, the vehicle is moved to the Open Class.
    3. **F1TENTH Competition is a battle of algorithms. Any hardware that should turn the odds in your favor is not allowed**.
    4. _Chassis_:
        Any chassis listed as *1:10 scale* car is allowed. Preferably **1:10 Traxxas** (e.g., [TRA74054](https://traxxas.com/products/models/electric/ford-fiesta-st-rally), [TRA6804R](https://traxxas.com/products/models/electric/6804Rslash4x4platinum), [TRA68086](https://traxxas.com/products/models/electric/slash-4x4-tsm)), but generally, any chassis with similar dimensions is allowed. Both 4WD and 2WD are permitted.
    5. _Main Computation Unit_:
        **Nvidia Jetson Xavier NX**, Equivalents to the Nvidia Jetson NX (e.g. Nvidia Jetson TX2, Nvidia Jetson Nano), or anything of equal or lower GPU and CPU specification is allowed. Examples of possible computation units could be: Raspberry Pi, Arduino, Beaglebone.
    6. _LiDAR_:
        [**Hokuyo UST-10LX**](https://www.hokuyo-aut.jp/search/single.php?serial=167), its equivalent, or anything of lower specifications is allowed. The main observed characteristics are: detection range (10 m), scanning frequency (40 Hz), and angular resolution (0.25°).
    7. _Camera_:
        Both *monocamera* (e.g. Logitech C270, Logitech C920, Raspberry Pi Camera Module V2, Arducam) and *stereokameras* (e.g. Intel Realsense, ZED) are allowed.
    8. _Engine_:
        Only brushless DC motors are allowed. The [**Velineon 3500 kV**](https://traxxas.com/products/parts/motors/velineon3500motor), its equivalent, or anything of lower specifications regarding power and torque are allowed.
    9. _Other sensors_:
        Other sensors (IMUs, encoders, custom electronic speed controllers) are not restricted. Indoor GPS sensors (e.g. Marvelmind) are not allowed. In addition, in the spirit of the competition, components with significant internal computation power are prohibited.

3. **Open Class** allows cars that do not fit into Restricted Class. These cars may compete, but they are not eligible for prizes and their ranking is kept separate. In addition, the following constraints are applied:

    1. Car dimensions should be within 10% difference to the dimensions of the car required in the Restricted Class. This is to make sure that the car can fit comfortably in the racing track and that it can compete with other cars in the Head-to-Head race.
    2. Only electric drive motors are allowed.


## 2.2 Track & racing environment

The competition will take place at the Lausitzring Germany. The characteristics of the environment where the track will be built are:

1. TBD


## 2.3 Inspection

1. The purpose of the Inspection is to check that the hardware of the autonomous cars meets the competition requirements and the cars are not dangerous for the environment, opponents, and people.

2. The inspection of the vehicles is done on the first competition day in the morning.

3. The inspection is done by the race referees.

4. The inspection has to be completed before the Time Trials and after significant changes to the cars hardware or algorithms.

## 2.4 Time Trial

### 2.4.1 Definitions

1. *Touching* means moving the object by less than 5 cm. Moving by greater distance is called *Crashing*.

2. Moving the track border by any distance is called *Crashing*.

2. The track will contain several *checkpoints*, marked with a line across the track. Starting line is not a checkpoint.

### 2.4.2 General

1. Time Trial is a race with a goal to drive through the designated track as fast as possible. The idea is to push the algorithms to their limits.

2. The race consists of two heats. Each heat lasts for 5 minutes, and the goal is to drive a single lap in as short time as possible and/or to drive as many complete laps as possible. Crashing and stopping the car does not pause the heat timer.

3. The teams are allowed to change the configuration of their algorithms in between the heats, and even during the heat. When the configuration is changed during the heat, the car must stand still. In other words, the teams cannot update the configuration on-line while the car moves.

4. The map (track layout) is **known** a priori. The teams are encouraged to map the track prior to the race (a time slot for the mapping will be provided).

5. The track will contain several static obstacles of size from 12×12×30 cm up to 35×32×30 cm, made from LiDAR perceivable material (e.g., cardboard). The intention is to make time trial race closer to head-to-head race, but still simpler.

6. Crashing into the obstacle is penalized as discussed later.

### 2.4.3 Requirements for Time Trial qualification

1. Each vehicle must demonstrate that it can drive autonomously through a track without crashing.

2. The team must demonstrate that it is possible to trigger car emergency stop remotely.

### 2.4.4 Penalties

1. Touching the border of the track or a static obstacle is not penalized. Excessive, repeated touching (up to the organizers) is considered a crash.

2. Upon crashing the track border or the static obstacle the team has to stop the car and move it (by hands) to the latest crossed checkpoint. After repairing the track and returning the obstacles to their appropriate locations, the race may continue. The time spent on moving the car to the checkpoint and repairing the track is considered the penalty.

### 2.4.5 Evaluation

Each team will be evaluated based on the following criteria:

1. *Fastest lap time*. The laptime will be measured with specific equipment by the race director.
2. *Number of completed laps per heat*

There will be two results tables based on these criteria.

## 2.5 Head-to-Head Race

### 2.5.1 General

1. The Head-to-Head race is a race with two cars on the track at the same time.

2. The track will be simpler and wider compared to timed trials. The teams are encouraged to map the track prior to the race (a time slot for the mapping will be provided).

3. The algorithms must not intentionally hinder the opponent or perform any damage to it. Specifically, manoeuvres such as deliberate crowding of a car beyond the edge of the track or any other abnormal change of direction are strictly prohibited. The referees will have the final say in whether a driver is in violation of the rule.

4. Depending on the number of participants, the race will be organized either as
    1. an all-play-all tournament with ties broken by an additional match, or
    2. a knockout tournament with brackets seeded by results of the time trial.

5. Each of the competing cars starts at its own starting line. Starting lines will be located at the opposite parts of the track.

6. Overtaking may be carried out on either the right or the left.

7. As opposed to time trials, no reconfiguration is allowed during the race, except after the crash, as described below.

8. Ultimately, organizers reserve the right to assign blame in the case of vehicle collision in the head-to-head tournament.


### 2.5.2 Requirements for qualification

1. The team has successfully completed the Time Trial.
2. The car must be equipped with front foam bumper, e.g., [TRA7436](https://traxxas.com/products/parts/7436) + [TRA7437](https://traxxas.com/products/parts/7437) +  [TRA7415X](https://traxxas.com/products/parts/7415X). This solution is compatible with _Slash_. Model of _Ford Fiesta_ already has this bumper.
3. The car has to be easily perceivable by the opponent’s LiDAR. Therefore, the car must occupy a space of size at least 12×12 cm at every horizontal plane between 10 to 30 cm above the ground.
4. The car needs to provide beforehand that is is able to avoid static and dynamic obstacles. This is evaluated by the race referess with a test:
   1. The cars need to run 1 lap around the racetrack that includes static and dynamic obstacles
   2. These obstacles contain of size up to 35×32×30 cm, made from LiDAR perceivable material (e.g., cardboard).
   3. The racecars must show their ability to avoid those obstacles
   4. Based on this results the access to the race is granted.

### 2.5.3 Penalties

1. Touching the border of the track or a static obstacle is not penalized. Excessive, repeated touching (up to the organizers) is considered a crash. (Same rules as for Time Trial.)

2. Touching the opponent is not penalized unless one of the cars significantly diverges from its expected trajectory.

3. Upon crashing the border of the track, the team has to fix the track and place the car on the side of the track at the place where the car first crashed the border. Then, the car can continue the race. During all of this, the opponent’s car must not be restricted by the team’s actions. The penalty is the time spent on fixing the track and placing the car.

4. Upon crashing the opponent, these steps are applied:

    1. Referees judge which car is at fault.
    2. Upon the first crash of the faulty car and when both cars can continue the race, a penalty of two laps is applied to the faulty car. Otherwise, the faulty car is disqualified, and the opponent wins by default.
    3. Both cars are placed next to each other at the place decided by the referees, and teams have two minutes to re-configure their algorithms. After that time, the race is resumed by the referees.

### 2.5.4 Evaluation

1. The first car that completes 10 laps wins. There will be two referees, one for each car.
