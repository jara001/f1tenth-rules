# RoboRacer Rules
_Note: This is a draft of v3 rules. Commentary will be removed in the final version._

<!-- https://discourse.devontechnologies.com/t/css-for-markdown-numbered-headings/71404/3 -->
<style>
body {
  counter-reset: h1;
}
h1 {
  counter-reset: h2;
}
h1::before {
  counter-increment: h1;
  content: counter(h1)  ". ";
}
h2 {
  counter-reset: h3;
}
h2::before {
  counter-increment: h2;
  content: counter(h1) "." counter(h2) ". ";
}
h3::before {
  counter-increment: h3;
  content: counter(h1) "." counter(h2) "." counter(h3) ". ";
}
h3 {
  counter-reset: h4;
}
h4::before {
  counter-increment: h4;
  content: counter(h4, lower-alpha) ". ";
}
</style>
<!--
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
-->

## Outline
 The main concept is to go though v2 rules, and filter out those that are not required anymore. In general, v3 should be ready for **all** competitions, introducing harmony a transparency to the overall competition environment.

Current idea is to provide a set of rules (also, general rules) and then, optionally, competition modifications (also, additional rules).

Even though the aim is to make the general rules shorter, it should give multiple options to host a competition; then, inside the additional rules, you specify which parts apply.

The final rules should be coherent and leave smaller window for possible mistakes, e.g., officially having an UK competition in Pennsylvania.

Note: Parts of these rules are taken over from rules of past ~16 competitions. Credits go to the people creating those rules. (Even though they are mostly unknown.)

Filling up the registration form -> Sending all required materials -> REGISTERED
On-site registration -> ???

Inspection -> APPROVED + Qualification -> QUALIFIED

## Covered sections

In the rules, we should cover:

- Definitions
- Car
- Track
- Competition Area
- Practice
- Inspection
- Qualification
- Timed Race
- Head-to-Head Race

## General
These rules apply for all official in-person RoboRacer competitions.

With every competition instance, these rules might be altered by specific / additional rules. In parts where both documents contradict, additional rules take preference.

These rules are organized as follows:
...

Violating the rules may result into a team warning. Upon receiving three warnings, the team may be disqualified from the competition. Multiple disqualification and repeated misbehaviour may result into a ban.

## Competition rules

- Specify timeline
- Place
- Track/area parameters
- Which parts are applied
- Contact on organizers
- Prizes

Organizers reserve the right to change the rules applied in the competition.


## Definitions

- Track: Space where we drive, muhehe
- Heat: Single instance of n-teams racing on the track. A race can be composed on multiple heats.
- Session: Block of specific competition part.
- Touching
- Crashing
- Track section: Centerline based...?


## Vehicle specifications
_Note: I omit classes as ICRA 2025 removed them. I think that it currently makes sense._

Each vehicle will be inspected as a part of qualification whether it meets the criteria. In case the criteria are not met, the vehicle is disqualified.

Following rules mostly specify the upper bounds on the components; generally everything that is of a lower spec is allowed.

1. Size
    - Width: 296mm ± 10%
    - Length: 568mm ± 10%
2. Weight
    - No limits.
3. Chassis
    - No additional limits.
    - Recommended: Traxxas 1:10 (e.g., TRA74054, TRA6804R, TRA68086).
4. Tires
    - No limits.
4. Drivetrain
    - No limits. Both 2WD and 4WD are allowed.
4. Motor
    - Electric motors only.
    - ... TODO: Add that Velineon is the upper limit (?)
    - Recommended: Velineon 3500
5. Battery
    - Up to **4S** for powering the motor.
    - Additional batteries for powering other components are not limited.
5. Electronic Speed Controllers
    - No limits.
    - Recommended: VESC
6. CPU
    - No limits, but all computation has to be done onboard the vehicle.
    - Recommended: Xavier, Orin, NUC... dunno what to write here
7. LiDAR
    - Single plane only.
    - Detection range: ≤ 30m
    - Scanning frequency: ≤ 40Hz
    - Angular resolution: ≥ 0.125°s
    - Recommended: Hokuyo UST-30LX
8. Camera
    - No limits. Monocameras and stereocameras are allowed.
9. External localization
    - GPS and similar indoor solutions are not allowed.
    - Exception: Organizers.

... add other parts: bumpers, parachutes.

Other sensors are not restricted.

### Vehicle parameters

- You can't hinder opponents from detecting you.
- It needs to have a box ...

## Competition Area

_Reserved for future._

## Track

Racing track is...

The competition rules should specify:

- Nature of the surface (flatness, reflectiveness, material).
- Nature of the room.
- Type of delimiters (air ducts, cardboard boxes).
- Height of delimiters.
- Maximum size (e.g., area) of the track.
- List of used track features.

### Track Features

A list of possible track features follow. Competition rules will specify, which of them (might) apply.

#### Dead-ends

Track contains parts that do not lead to the finish line. (I mean like a "trap dead-end".)


#### Open walls

Track borders are not closed, i.e., there are vertical gaps in them.

Gaps might be in the inner walls as well as in the outside walls.

Driving inside the gaps is not allowed.

Inside the gaps the track border is delimited by a tape on the ground (or any other marking technique).

Note that when the car crosses the track border by at least 3 wheels it is considered as a crash.


#### Intersections

The track contains intersections, i.e., a track section where multiple driving directions are allowed.

In the intersection area, following rules apply...

- Speed limit
- Right of way
- ...

Note that the lap is marked as completed only when all track sections were driven through during it.


#### Surface changes

The track surface is deliberately altered in certain track sections.

This change can both reduce or increase surface friction.

When surface is changed, the track does not have to be entirely flat; a small height change may occur. This change is below a certain threshold.

Competition rules should specify how the surface is altered.

The surface cannot be altered by methods that could damage the cars, e.g., spilling water on the track.


## Competition organization

The competition is composed of:

- Registration
- On-site registration
- Practice
- Inspection
- Qualification
- Time Trial
- Head-to-Head Race
- Awards ceremony

## Registration

- Team interested in participating in the competition has to register using a official registration method. This method may have its deadline.
- Registrations received after the deadline may not be accepted.
- Registration is confirmed by the competition organizers after completing all required steps. These are, but not limited to:
    - Filling up the registration form.
    - Submitting a video of the car autonomously driving.
    - Submitting a hardware list.
    - Paying the registration fee.
- Not submitting in time may void the registration.
- Registration not confirmed by the organizers is not ...


## Eligibility

The team is eligible attend the competition as long as:

- Registration fee is paid.
- Registration is confirmed by the organizers.
- If applicable, the car does not differ from the submitted hardware list.


## On-site registration

Something like: The teams have to register on-site in the given time frame. Exceptions are allowed as long as they are discussed with the organization team.

Upon completing the on-site registration the team is allowed to:

- Make use of the team designated area.
- Sign in to the practice sessions.
- ...


## Practice

Practice is a session for the teams to train and test their car directly on the track.

The practice track should contain all track features used during the competition, but its layout may differ.

_Note: When this happens, there should be another practice session so they can map._

Opt-in practices are designated on a first-come-first-serve basis.

During the practice sessions:

- Teams attending the practice session should be ...
- Teams that are not taking part in the practice session should avoid the track at all times.

Upon decision, a special practice session for mapping the track may be issued.


### Practice variants

A list of possible practice variants follows. Competition rules specify which of them apply.


#### Shared Practice (Group)

Practice session where the track is opened for a subset of teams specified by organizers.


#### Open Practice

Practice session where the track is opened for all teams.


#### Closed Practice (Single)

Practice session where the track is reserved for one team only.


### Violations

Obstructing other teams
Endangering other teams/cars


## Inspection

- The purpose of the Inspection is to check that the hardware of the autonomous cars meets the competition requirements and the cars are not dangerous for the environment, opponents, and people.
- The inspection of the vehicles is done in a dedicated time-frame.
- The inspection is done by the race referees.
- The inspection has to be completed before the Qualification and after any significant changes to the cars hardware or algorithms during any of the days of the event.
- When a hardware list is submitted as a part of the registration, the car is checked to match these parameters.
- Car that is not inspected and approved is not allowed to be used in the competition.


## Qualification

Qualification is a session testing the autonomous capabilities of the racing car.

- Complete a single lap without crashing into anything. Anything can be:

  - Track borders
  - Obstacles
  - Other cars

- Qualification is done with a single racing car on the track.
- Only inspected and approved car can be in a qualification.
- The Qualification may be merged with Time Trial.
    - In this case the obstacle avoidance capability has to be checked separately.


## Time Trial

_Note: Competition rules should specify: #heats, time per heat; e.g. 2x5 minutes._

Time Trial is used as a seeding technique for the Head-to-Head Race.
Time Trial is a race with a goal to drive through the designated track as fast as possible and as consistently as possible. The idea is to push the algorithms to their limits.

Each team must pass the inspection to be able to participate in the Time Trial.


The race consists of multiple heats, two by default. Each heat lasts for a given time (e.g., 5 minutes), and the goal is to drive a single lap in as short time as possible and to drive as many complete laps as possible. Crashing and stopping the car does not pause the heat timer.


~~The heat sessions are split in two with a one one-hour practice session in between. The teams have to book a time slot in each session. The schedule of the sessions will be shared with the teams before the race.~~

Teams have to book (FIFO) a time slot in each heat. The heat timer is fixed to the time slot and no extensions are given. Missing out a time slot does not give the team an additional slot.


Each team is provided two dedicated time slot for their vehicle to qualify. No time extensions are given and after the 5 minutes we move on to the next time slot and the next team. There will be 1-5 minutes of dedicated time to switch from one team to the next. If a team is not able to run the car in this dedicated time slot, the qualification phase is not passed for this team.


The teams are allowed to change the configuration of their algorithms in between the heats, and even during the heat. When the configuration is changed during the heat, the car must stand still. In other words, the teams cannot update the configuration on-line while the car moves.


The map (track layout) is known a priori (from practice the day before) and the track layout does not change over the whole competition. Keep in mind that cars crash into the walls and the layout of the track might slightly shift a little bit. Please consider this in your algorithms.


### Penalties

Touching the border of the track is not penalized. Excessive, repeated touching (up to the organizers) is considered a crash.


Upon crashing the track border the team has to stop the car and move it (by hand or using the remote control) to the latest position before crash. After repairing the track, the race may continue. The time spent on moving the car to the checkpoint and repairing the track is considered the penalty.


### Evaluation

Each team will be evaluated based on the following criteria:

- Fastest lap time.
- Number of consecutive uninterrupted laps.

The laptime will be measured with a time-keeping system provided by the race director.

There will be two results tables based on these criteria.

.. team get a point for every team they overpassed (?). When a tie occurs, ...
TODO: Shared 2nd place gives points for the second place?
I think that originally it is points for the third place while placing second.
But dunno.

ICRA25 did not care about places but gave less points.
I already did this in Prague but I can't find the table...

The final score for the qualification consists of two parts:

    Fastest laptimes: Teams are ranked based on their fastest lap times. Points are awarded according to the ranking. For example, with 10 teams, the fastest team receives 10 points, the second fastest receives 9 points, the third fastest receives 8 points, and so on.

    Consecutive uninterrupted laps: Teams are also ranked based on the number of consecutive uninterrupted laps they complete. Points are awarded similarly. For example, with 10 teams, the team with the most laps receives 10 points, the second team receives 9 points, the third team receives 8 points, and so on.

A point is given for completing at least one heat. _Note: To make it 10-1 instead of 9-0._
A point is given for every team that has worse scoring.

The final score is the sum of the points from both categories. Note that the best lap times and the number of laps can be achieved in different time slots. This allows teams to push their algorithms to the limits in each of the two categories.

Should a tie occur in the final ranking, the team with more laps is ranked higher. Additional tie is, with respect to the seeding, resolved by a random method (e.g., coin flip).

The qualification is passed by finishing a single lap without crashing. Otherwise, the team is disqualified from the competition.


## Head-to-Head Race

Head-to-Head race is a race with multiple cars on the track at the same time.


The algorithms must not intentionally hinder the opponent or perform any damage to it. Specifically, maneuvers such as deliberate crowding of a car beyond the edge of the track or any other abnormal change of direction are strictly prohibited. The referees will have the final say in whether a driver is in violation of this rule.


~~Before the start of each head-to-head race, both teams will be tested for obstacle avoidance and are required to use the same code for the race. Any violations to this rule could result in disqualification of the violating team (up to the organizers).~~

~~Teams that fail to pass the obstacle avoidance test will have the option to race on the condition that they do not overtake the opponent.~~

~~If the team fails to pass the obstacle avoidance test and overtakes the opponent, the team will be disqualified.~~
~~The team that failed the obstacle avoidance is permitted to use manual control when the car is 5 meters behind the opponent to slow down the car and avoid overtaking.~~
~~The faulty team is not allowed to use manual control to speed up the car and overtake the opponent.~~
~~The faulty team can only overtake the opponent if the opponent crashes.~~

One head-to-head race consists of two teams racing against each other. One race has a dedicated timeslot of around 10 minutes. If one team is not showing up in these 10 minutes and let their car race, the other team won. If at some point along the race a car is not able to drive anymore (e.g. hardware issue, software not running etc.) and the teams are not able to restart the car withing the 10 minutes, the other team wins the race. No time extensions are given and after the 10 minutes we move on to the next time slot and the next team.

~~Each race consists of three rounds, the team that wins two rounds wins the race.~~

Both competing cars start from the same starting line used in the qualifications.

    The teams will start side-by-side seperated by one car width (30cm) from each other.
    For the first round, the team that ranked higher in qualifications chooses the starting position (left or right). The other team starts on the opposite side.
    In the second round, the teams switch sides. The team that started on the left side in the first round starts on the right side in the second round.
    Should a third round be necessary, a coin flip will determine the starting position. The team that ranked higher in qualifications will call the coin flip (i.e heads or tails). The team that wins the coin flip chooses the starting position.

Overtaking may be carried out on either the right or the left.

As opposed to time trials, no reconfiguration is allowed during the race, except after a crash, as described below.

Ultimately, organizers reserve the right to assign blame in the case of vehicle collision in the head-to-head tournament.

Collisions are judged by the referees.

    Collisions with track boundaries do not stop the race. The team that crashed into the track boundary must fix the track and place the car at the location of the crash. The opponent is allowed to continue. The crashed team bears the burden of the time spent on fixing the track and placing the car.
    Light side-bumps and slow-speed nudges are not penalized and do not stop the race.
    High-impact crashes that result in the displacement of one or both cars on crash result in a stoppage of the race.
    If a car crashes into the opponent, the referees will judge which car is at fault.
    Both cars will be restarted at the location of the crash, with the at-fault car placed behind the other car by 2 meters.
    A crash is not considered a warning unless judged by the referees.
    Crashes that result in a warning include but are not limited to "malicious" crashes where the autonomous car did not attempt to slow down or steer away from the opponent.
    Under special circumstances, the referees may decide to give a warning to a team with the option of stopping the race to address the issue. The team has a maximum of 5 minutes to fix the issue and resume the race.
    After 3 warnings, the team is disqualified and the opponent automatically wins.
    If the team that was crashed into is able to autonomously detect and recover from the crash by stopping on the side of the track, that team is granted an extra head-start of 1 meter before the restart (i.e the at-fault car is placed 3 meters behind the other car).

**Tournament type**

The head-to-head race will be organized as a double-elimination tournament with two brackets seeded by results of the qualification.

The two winners of each bracket will qualify to compete in the Final Four race. This final tournament will feature a single elimination bracket.


### Tournament types

Below a list of possible tournament types follows. Competition rules specify, which are used.

#### All-vs-all

#### Single Elimination Bracket

#### Double Elimination Bracket


### Seeding

Below a list of possible seeding methods follows. Competition rules specify which are used.


#### Random Seeding

#### Time Trial seeding


### Competition model

Below a list of possible competition models follows. Competition rules specify which are used.

#### Single Cup

All teams are racing in the same cup.


#### Double Cup (??? Cup, Master Cup)

During the seeding, the participants are split into two groups, cups. Note that the rules may differ between the cups.

Admission to Master Cup (with respect to the seeding) is done as follows:

- Master Cup contains up to the half of the team roster.
- First 4 teams automatically proceed.
- Up to the first half, all teams have an opportunity to either join or not.
- The rest of the master cup teams may be filled by teams that placed top 3 in the last 3 years (1100 days).

Upon changing the track, teams are given an extra practice session to test their car and algorithms on the new track.


### Penalties

Touching the border of the track or a static obstacle is not penalized. Excessive, repeated touching (up to the organizers) is considered a crash. (Same rules as for Time Trial.)

Track abuse: If a team abuses the track (e.g., deliberately cutting corners, damaging the track, or violating race boundaries excessively), they will be penalized. Penalties will be decided by a group of referees, and their decisions are final.

Touching the opponent is not penalized unless one of the cars significantly diverges from its expected trajectory.

Upon crashing the border of the track, the team has to fix the track and place the car on the side of the track at the place where the car first crashed the border. Then, the car can continue the race. During all of this, the opponent’s car must not be restricted by the team’s actions and the opponent is allowed to further race without stopping its car. The penalty is the time spent on fixing the track and placing the car.

Upon crashing the opponent, these steps are applied:

Referees call the crash and signal for it by raising the red flag.

Referees judge which car is at fault.

Both cars are placed at the location of the crash, with the at-fault car placed behind the other car by 2 meters.

The referees restart the race with a green flag.

### Evaluation

The first car that completes given amount of laps wins.

In case that this objective is not achieved by any car, the amount of completed laps is the decisive factor.

_TODO: List other tiebreaker factors, e.g., overtakes, crashes._

There will be at least three referees.
One referee will be assigned to each car and is solely responsible to call flag raises and rule violations per-team. The third referee is tasked with enforcing penalties, crash resolution, and time-keeping.

