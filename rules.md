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

These rules are prepared for the _10th International F1TENTH Autonomous
Racing Competition_. Rules can be modified overtime. The latest version
can be found [here](https://iros2022-race.f1tenth.org/rules.html).

Date: 2021-12-17

**Table of content**
- ToC
{:toc}


# 1. General

International F1TENTH Autonomous Racing Competition is a racing competition open to teams of all levels. Competing teams may consist of any number of members; however, each participant should be a member of only one team.

The competition is organized in two variants:

- In-Person competition, and
- Virtual competition.

Teams can register for the competition using a [registration form](https://icra2022-race.f1tenth.org/registration.html), where they select a single variant of the competition. Registration is open until April 11, 2022.

_Note: If the in-person competition gets canceled due to the ongoing pandemic situation, registered teams may compete in the virtual competition instead._

The preferred communication method with the organizers is the _#ICRA2022_ channel on [F1TENTH-teams Slack](https://join.slack.com/t/f1tenth-teams/shared_invite/enQtMzc3ODU2ODM1NzE3LTBjMmVkMzZjZTJiNWUzZDFhZTJiODgzMjg0MTA1MDAxZTUxMzkwMDRhNTM2NzdjNDc5MTk5YTc5YmNhNTdhMTU).


# 2. In-person (physical) competition

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

The competition will take place in the [Pennsylvania Convetion Center](https://www.paconvention.com/). The characteristics of the environment where the track will be built are:

1. The surface is flat and reflective. Therefore, LiDAR beams may reflect from the ground and measure the surrounding area rather than the ground. Similarly, depth cameras have problems with proper ground detection.
2. The room is surrounded by windows and “glass walls”. The windows will be covered by non-transparent material up to 50 cm from the ground to improve the perception. The room is bright, and the Sun can shine into it.
3. The track border is constructed from one air pipes of 33 cm diameters. They are made from aluminium and metal, secured with plastic/wodden holders. Keep in mind that there can be a gap between the pipes through which the LiDAR beams can pass.
4. The track will fit into the area of around the size of 28.5×11 m.
5. The track can be mapped in either the training sessions on each day or in the qualification session of each team. We are not providing a dedicated time slot for teams to map the track. Since many teams using SLAM algorithm or vision-based localization techniques, a dedicated **Map Creation** or **Mapping** session is not provided for the teams.


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

3. Each team is provided two dedicated time slot for their vehicle to qualify. No time extensions are given and after the 5 minutes we move on to the next time slot and the next team. If a team is not able to run the car in this dedicated time slot, the qualification phase is not passed for this team.

4. The teams are allowed to change the configuration of their algorithms in between the heats, and even during the heat. When the configuration is changed during the heat, the car must stand still. In other words, the teams cannot update the configuration on-line while the car moves.

5. The map (track layout) is **known** a priori and the track layout does not change over the whole competition. Keep in mind that cars crash into the walls and the layout of the track might slightly shift a little bit. Please consider this in your algorithms.

6. The final score for the qualification is two parts: Firstly, based on the ranking of the fastest laptimes you receive points. E.g. with 10 teams the fastest team receives 10 points, second fastest 9 points, thrid fastest 8 points …. and so on. Secondly, based on the number of consecutive uninterrupted laps, a ranking of the teams is created and therefore the teams receive points. E.g. with 10 teams the team with the most laps receives 10 points, second team 9 points, thrid team 8 points …. and so on. The final score is the sum of both scores.

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

2. The racetrack has the same layout as in the training and qualification sessions.

3. The algorithms must not intentionally hinder the opponent or perform any damage to it. Specifically, manoeuvres such as deliberate crowding of a car beyond the edge of the track or any other abnormal change of direction are strictly prohibited. The referees will have the final say in whether a driver is in violation of the rule.

4. The head-to-head race will be organized as a knockout tournament with brackets seeded by results of the qualification. For example, with 8 teams, the bracket of the first round will be (#1 vs. #8, #2 vs. #7, #3 vs. #6, and #4 vs. #5).

5. One head-to-head race consists of two teams racing against each other. One race has a dedicated timeslot of around 10 minutes. If one team is not showing up in these 10 minutes and let their car race, the other team won. If at some point along the race a car is not able to drive anymore (e.g. hardware issue, software not running etc.) and the teams are not able to restart the car withing the 10 minutes, the other team one the race. No time extensions are given and after the 10 minutes we move on to the next time slot and the next team.

6. Each of the competing cars starts at its own starting line. Starting lines will be located at the opposite parts of the track.

7. Overtaking may be carried out on either the right or the left.

8. As opposed to time trials, no reconfiguration is allowed during the race, except after the crash, as described below.

9. Ultimately, organizers reserve the right to assign blame in the case of vehicle collision in the head-to-head tournament.


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

3. Upon crashing the border of the track, the team has to fix the track and place the car on the side of the track at the place where the car first crashed the border. Then, the car can continue the race. During all of this, the opponent’s car must not be restricted by the team’s actions and the opponent is allowed to further race without stopping its car. The penalty is the time spent on fixing the track and placing the car.

4. Upon crashing the opponent, these steps are applied:

    1. Referees judge which car is at fault.
    2. Both cars are placed next to each other at the place decided by the referees
    3. The referees restart the race.

### 2.5.4 Evaluation

1. The first car that completes 10 laps wins.
2. There will be two referees, one for each car.
3. Each referee counts the lap for one car and is responsible for identifying the crashes.

# 3. Virtual (simulation) competition

## 3.1 General
  1. The virtual competition will be completely done in an simulation environment only and no hardware is involved.

  2. This simulation environment is based on the 2D Simulator F1TENTH GYM and is operated by the Riders.Ai competition platform. The F1TENTH virtual competition will be complete done in this environment only and teams need to submit their code in time to this platform.

  3. The virtual competition will comprise two parts – *Time Trials* and *2 Vehicle Head-to-Head* race. Every participant must pass the Time Trials and will be automatically registered to both races.

  4. F1TENTH reserves the right to reject any submission that we deem illegal due to circumstances such as exploiting the simulation environment. Therefore their source code submission will be examined by the race stuarts after the race.

  5. The map used for all the races (Time Trials, Head-to-Head) will be the same. In the Time Trials this map will have added obstacles for the obstacle avoidance task.

## 3.2 Registration, Training, Code Submission.

1. All simulations are done on the Riders.ai competition platform

2. Teams must register themselves for the 9th F1TENTH Autonomous Grand Prix on the Riders.Ai platform on their own with their team name.

3. We will provide test environments (maps) for the teams to use this platform as a training and evaluation environment while they develop their code.

4. Teams need to prepare their code with their local machine

5. Teams need to submit their code with their local machine.

6. All simulation event evaluations are done on the Riders.Ai cloud. Based on this evaluation the leaderboard will be created.

7. We define deadlines for the submissions of the Time-Trial code and the Head-to-Head for the teams. No extensions are given.

## 3.3 Time Trials

1. The Time Trials in the F1TENTH simulation environment are here to define both the capabilities of the vehicles to race in a static environment with and without obstacles as well as for creation of the seeding in the Head-to-Head race.

2. The Time Trials are single vehicle races only.

3. The Time Trials consist of 2 races:

  1. **Qualification** race: Race 2 laps of track as quickly as possible without collision into the walls (determines Grand Prix seeding). If an agent can finish without collision with the environment, it’ll receive a lap time and update its ranking on the leaderboard.

  2. **Obstacle avoidance** race: Race 2 laps around the track with added obstacles unknown to participants. The car needs to go round 2 laps without collision. The location and the size of the obstacles will not be revealed prior to submission. Some example maps with obstacles will be provided.

4. The submission of the Time Trial Code is done via the Riders.ai platform

5. The code for both Qualification and Obstacle avoidance race needs to be the same.

## 3.4 Head To Head Race

1. The Head-to-Head race is a race with two cars on the track at the same time.

2. The car that crosses the finish line first after 2 laps wins the race.

3. The Head-to-Head race is a best of 3 trials. The car that wins two races moves on to the next round.

  1. The third race is a tie-braker if the first two races are 1:1. In the third race, the cars starting again on their predifined P1 and P2 position. The car that is seeded in the qualification higher is located on P1.

4. The cars start in alternating position (inside, outside) in each of the races.

5. Seeding: The elimination bracket of the tournament will be filled by submissions that passed the obstacle avoidance test and seeded by the result of the timed trials. For example, with 8 teams, the bracket of the first round will be (#1 vs. #8, #2 vs. #7, #3 vs. #6, and #4 vs. #5).

6. Overtaking: According to the circumstances, may be carried out on either the right or the left. Maneuvers liable to hinder other drivers, such as deliberate crowding of a car beyond the edge of the track or any other abnormal change of direction, are strictly prohibited. The stewards will have the final say in whether a driver is in violation of the rule.

7. Causing a collision (decided by the stewards) for more than 3 times will result in automatic disqualification of one car.

8. Collisions at the fault of both vehicles will result in a redo trial. After 3 redos of the same case, both vehicles are disqualified.

9. The stewards reserve the right to have the final say.
