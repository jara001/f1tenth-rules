# RoboRacer Rules
## Version: 3.0.0-draft
_Note: This is a draft of v3 rules. Commentary will be removed in the final version._

<!-- https://discourse.devontechnologies.com/t/css-for-markdown-numbered-headings/71404/3 -->
<style>
body {
  counter-reset: h1;
  counter-reset: p;
}
h1 {
  counter-reset: h2;
}
h1::before {
  counter-increment: h1;
  /*content: counter(h1)  ". ";*/
}
h2 {
  counter-reset: h3;
}
h2::before {
  counter-increment: h2;
  /*content: counter(h1) "." counter(h2) ". ";*/
  content: counter(h2) ". ";
}
h3::before {
  counter-increment: h3;
  /*content: counter(h1) "." counter(h2) "." counter(h3) ". ";*/
  content: counter(h2) "." counter(h3) ". ";
}
h3 {
  counter-reset: h4;
}
h4::before {
  counter-increment: h4;
  content: counter(h4, lower-alpha) ". ";
}
p::before {
  counter-increment: p;
  content: "§ " counter(p);
  margin-right: 1rem;
  font-weight: bold;
}
hr {
  counter-reset: p;
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
The main concept is to go though v2 rules, and filter out those that are not required anymore. In general, v3 should be ready for **all** competitions, introducing harmony a<!--and?--> transparency to the overall competition environment.

Current idea is to provide a set of rules (also, general rules) and then, optionally, competition modifications (also, additional rules).

Even though the aim is to make the general rules shorter, it should give multiple options to host a competition; then, inside the additional rules, you specify which parts apply.

The final rules should be coherent and leave smaller window for possible mistakes, e.g., officially having an UK competition in Pennsylvania.

Note: Parts of these rules are taken over from rules of past ~16 competitions. Credits go to the people creating those rules. (Even though they are mostly unknown.)

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

On the other hand I want to avoid:

- Duplicit rules (e.g., parts about the box on the car). <!--replace with references-->
- Rules that are not used anymore (or not used at all).
- Change will/must into may in parts where the rules might not be applied because of the competition setting (e.g., small competitions have different need than big competitions).

---

## General

<!--Add reference to RFC for MUST, MAY, SHOULD, ... This makes defining rules a lot easier: https://datatracker.ietf.org/doc/html/rfc2119-->

These rules apply for all official in-person RoboRacer competitions.

With every competition instance, these rules might be altered by specific / additional rules. In parts where both documents contradict, additional rules take preference. <!--who officially communicates rules and how are they communicated?-->
_The rules used in a competition are posted on the competition website, including the version and commit hash. This document uses [semantic versioning 2](https://semver.org) for defining version._

<!--Add versioning for rules and specify who defines which rules are used-->

These rules are organized as follows:
...

<!--Replace warning with a different word-->
Violating the rules may result into a team warning. Upon receiving three warnings, the team may be disqualified from the competition. Multiple disqualification and repeated misbehaviour may result into a ban, i.e., unability to attend future competitions.
    - Note that warnings are induced on whole teams not individuals.

!! WE HAVE TO DIFFERENTIATE BETWEEN THIS WARNING AND THE WARNING FROM HEAD-TO-HEAD!!_ <!--YES, we should have a section about possible penalties and the scope of those penalties. E.g.: do strikes remain after a race or are they reset?-->

_I would call them strikes. But maaaaybe we don't need to differentiate between them._


## Competition rules

- Specify timeline
- Place
- Track/area parameters
- Which parts are applied
- Contact on organizers
- Prizes

Organizers reserve the right to change the rules applied in the competition.


## Definitions

**ADD MORE CLEAR DEFINITIONS**

- Car
- Hardware list: List of components that the car is composed of. All parts of the Vehicle specification must be addressed along with additional sensors.
- Track: Space where we drive, muhehe
- Heat: Single instance of n-teams racing on the track. A race can be composed on multiple heats.
- Session: Block of specific competition part.
- Touching
- Crashing
- Track section: Centerline based...?
- Whistle<!--: LOUD!?-->
- Overtakes?
- Track section
- Penalties:
- Violations: Rules that result into warnings?
- Warning: Issued for violating the rules. Three warnings may lead to disqualification from the competition.
- Disqualification.
- Flags: When flags are used during the competition, their meaning is as follows:
    - Checkered flag: A flag is raised if the team is on the last lap. The flag is dropped and then waved when the team finishes and wins the current round.
    - Red flag: A flag is raised if a race-stopping car crash occurs. The flag is dropped after all cars are stopped, and the team representatives are allowed to approach the track. ~~After the crash is resolved by the stewards, the flag is dropped and the race resumes.~~ <!--NAMING_CONSISTENCY: steward-->
    - Yellow flag: A flag is raised if the team is warned for a rule violation.
    - Black flag: A flag is raised if the team is disqualified. The flag is dropped after the disqualified team stops the car and leaves the track. The opponent is allowed to continue the race till completion of the set number of laps.
    - Green flag: Optional - raised to signal that the race is safe to continue. The flag is dropped after the race resumes.
    - Blue flag: Optional - used during open testing to indicate that a team needs to let another team pass.
    - The steward holds the black flag in each hand, one for each team. <!--Point flags to the side of the team-->
- Team
- Team Member

## Vehicle specifications
_Note: I omit classes as ICRA 2025 removed them. I think that it currently makes sense._

Each vehicle will be inspected during the competition whether it meets the specified criteria. In case the criteria are not met, the vehicle is not allowed to be used in the competition.

Following rules mostly specify the upper bounds on the components; generally everything that is of a lower spec is allowed.

1. Size
    - Width: 296mm ± 10%
    - Length: 568mm ± 10%
    - Height: TODO
2. Weight
    - No limits.
    - _Felix: Should we add a maximum weight limit? Maybe 5kg? That should be enough for a car (even though it could be tight with BE)_
3. Chassis
    - No additional limits.
    - Recommended: Traxxas 1:10 (e.g., TRA74054, TRA6804R, TRA68086).
3. Bumpers
    - Front bumper (at least 5 cm thickness) from a soft material is required.
    - The bumper must be attached to the car in a way that it does not fall off at any time during the head-to-head race.
    - Example: TRA7436 + TRA7437 + TRA7415X
4. Tires
    - No limits.
4. Drivetrain
    - No limits. Both 2WD and 4WD are allowed.
4. Motor
    - Electric motors only.
    - Only a single motor can be used for operating the drivetrain.
    - ... TODO: Add that Velineon is the upper limit (?)
    - _Felix: If so, what is the limit? The non-existant torque parameters of the motor? The kV, can be, at best, interpreted as inverse proportional to the torque?; So: higher kV -> higher max RPM & lower torque; So limit: max. 4S with Velineon +/- 10% for torque (we should check what the hobbywing has for this)_
    - _J: You are completely right, but we should (kinda have to) address that. Sooner or later someone *wink wink* tries to drive with something more powerful._
    - _Felix: https://things-in-motion.blogspot.com/2018/12/how-to-estimate-torque-of-bldc-pmsm.html describes the relationship between torque, KV and current (might also be interesting for the control team...). Should we, if this is correct, use this for the limits?_
    - Recommended: Velineon 3500
5. Battery
    - Up to **4S** for powering the motor.
    - Additional batteries for powering other components are not limited.
    - _Felix: What are the other components? Should we clarify that they most not provide any power to the drive train? "Other components" is maybe not clear enough. In this setting it would, theoretically, be possible to power the steering servo with a separate battery (which would be fine IMHO) but we should specify here_
5. Electronic Speed Controllers
    - No limits.
    - Recommended: VESC
6. CPU
    - No limits, but all computation during the race has to be done onboard the vehicle.
    - Recommended: NVIDIA Jetson Xavier, NVIDIA Jetson Orin, Intel NUC, etc.
7. LiDAR
    - _Note: Multi-plane lidar might add more features (outside of the track walls) for localization_
    - Number of planes: Not limited
    - Detection range: Not limited
    - Scanning frequency: ≤ 40Hz
    - Angular resolution: ≥ 0.125°s
    - Recommended: Hokuyo UST-30LX, Hokuyo UST-10LX, etc.
8. Camera
    - No limits. Monocameras and stereocameras are allowed.
    - _Felix: Should we include/exclude optical flow sensors (for odometry?)_
    - _J: I would keep them allowed. But they should be listed in the HW list?_
    - _Felix: Yes, I think they should be a requirement, if used._
9. External localization
    - GPS and similar indoor solutions are not allowed.
    - Exception: Organizers.

Other sensors are not restricted.<!--but MUST be mentioned in the hardware list.-->

### Vehicle parameters

- You can't hinder the opponents from detecting your car, e.g., using materials/colors to adjust the car reflectivity.
- While on the track, the car MUST occupy a square-shaped space of size at least 12×12 cm at every horizontal plane between 10 to 30 cm above the ground. Usually, this is achieved by placing a 12x12x20cm box on top of the car at its back.<!--Replace `While` with `At all times`-->
    - The box should be made of LiDAR perceivable material (e.g., cardboard).
    - As long as the object results in the desired LiDAR signature, the object can have any additional aeorodynamic shapes added like fins, wings, etc.
    - The box maybe of any color as long as it is easily perceivable by the LiDARs of the other cars.


## Competition Area

_Reserved for future._

_Felix: Is this intended for tables and stuff?_

_J: Not sure now..._

## Track

Racing track is a delimited area used for racing.

The competition rules must specify:

- Nature of the surface (flatness, reflectiveness, material).
- Nature of the room (e.g., walls/windows, ceiling type).
- Type of delimiters (e.g., air ducts, cardboard boxes).
- Height of delimiters.
- Maximum size (e.g., area) of the track.
- List of used track features.

### General track notes

- The surface friction may naturally slightly differ across the track.
- When the room is surrounded by windows or semi-transparent surfaces, it might result into incorrect sensor measurements.
- When the track is delimited by a set of pipes (on top of each other) there might be gaps between them.
- Due to the car tilting, the sensors might see over the track borders.
- When multiple tracks are present, their parameters, features and overall nature may differ.
    - Current session may differ as well. In that case the organizers must clearly state the current session on each track.

### Track behaviour

_Note: I want to make it as a collection of rules "how to behave on the track"._

_Note: Eventually, "racer stance" should be here as well._


### Violations

- Driving outside of the track is generally not allowed.
    - Exception is testing the car in very slow speeds.

- Not adhering to track behaviour...


### Track Features

A list of possible track features follow. Competition rules will specify, which of them (might) apply.


#### Dead-ends

Track contains parts that do not lead to the finish line.

- Driving into these track sections is not penalized.


#### Speed-restricted sections

Track contains sections with defined speed limits.

- Driving with forbidden speed is considered as a ...
- The speed limit is defined as ... _e.g., traffic signs? lights?_


#### Pit lane

Track contains sections that are marked as a pit lane.

- When this track feature is used, stopping outside the pit lane is not allowed.
    - Stopping outside of pit lane is considered as a...
- Teams are allowed to add cars to the track only at a pit lane area.
    - Teams are highly encouraged to do the car removal here as well, unless required by the current situation.


#### Open walls

Track borders are not closed, i.e., there are horizontal gaps in them.

- Gaps might be in the inner walls as well as in the outside walls.

- Inside the gaps the track border is delimited by a tape on the ground (or any other marking technique).

- Driving inside the gaps is not allowed.
    - Crossing the track border is considered as a touch.
    - Crossing the track border by at least 3 wheels is considered as a crash.


#### Intersections

The track contains intersections, i.e., a track section where multiple driving directions are allowed.

- In the intersection area, following rules apply...

    - Speed limit
    - Right of way
    - ...

- The lap is marked as completed only when all track sections were driven through during it.


#### Surface changes

The track surface is deliberately altered in certain track sections.

- This change can both reduce or increase surface friction.
- When surface is changed, the track does not have to be entirely flat; a small height change may occur.
    - This change is below a certain threshold to not pose a threat to the cars.
- Competition rules must specify:
    - How the surface is altered.
        - The surface cannot be altered by methods that could damage the cars, e.g., spilling water on the track.
    - Maximum height change between two surfaces (mm).


#### Track splits

The track contains track splits, i.e., the track section is split into multiple paths.

- Driving through the track may be performed by any of the paths. They are considered equal.
    - However, they might not be equal performance-wise, e.g., taking one of the paths might be more beneficial than the other.
- Driving though only one of the paths is required for lap completion.


#### Bridge (Elevation/Slopes?)

The track contains a bridge.

- In this section the track is generally not flat.
- Competition rules must specify:
    - Maximum elevation (%).

_Note: When using this track feature it can't prevent teams using single plane lidar from completing a lap._


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

_Felix:
Who is responsible for what and who can decide what? (organizer roles)

Types of Referess:
- Race Director(s) (determined by foundation, probably Ahmad)
- Race Organizer(s) (local-ish organizers, resposible for the whole race)
- Track marshall(s) (local-ish volunteers, responsible for one track)
- Track referee(s) (local-ish volunteer, subordinate of track marshall)

What things can be determined by who and where is the next highest instance required. What about conflict of interest?

Any higher role can also perform the tasks of a subordinate rule.
_

_J: I think this is not something that has to be in rules... more like in the rules for organizers. But yes, it should be clear who is "the contact person"._

_Felix: I would day that for transparency it should be included herer as well. Then teams know who to bother with what and who might have a conflict-of-interest._


## Registration

_Note: Competition rules should specify: registration method, requirements, deadlines._

- Team interested in participating in the competition has to register using a official registration method. This method may have its deadline.
- Registrations received after the deadline may not be accepted.
- Registration is confirmed by the competition organizers after completing all required steps. These are, but not limited to:
    - Filling up the registration form.
    - Submitting a video of the car autonomously driving.
    - Submitting a hardware list.
- Not submitting in time may void the registration.
- Registration not confirmed by the organizers is not ...


## Eligibility

_Note: I wanted to add something in between -- you are registered, but can you actually attend the competition?_

The team is eligible to attend the competition as long as:

- Registration fee is paid.
- Registration is confirmed by the organizers.
- All required forms and materials are sent to the organizers by the given deadline.
- If applicable, the car does not differ from the submitted hardware list.
- _Felix: This is part of the on-site registration/inspection, I'm not sure if we actually need this section... We could add it as a "Checklist" in general_


## On-site registration

Upon their arrival to the competition site, the teams must promply register on-site in order to race.

- The teams have to register on-site in the given time frame.
    - Exceptions are allowed as long as they are discussed with the organization team.
    - If a team is late for the registration, it must inform the organizers (e.g., for flights with a tight deadline, they can send the flight number to the organizers and this is considered enough notice).

- The on-site registration is composed of:

    - Confirmation of team details.
    - Pre-registration of the cars used within the competition. This also includes associating the car with its hardware list if a part of the registration.
        - Organizers may allow cars without the hardware list if they can approve all required components on the spot.

- Upon completing the on-site registration the team is allowed to:

    - Attend the competition.
    - Make use of the team designated area.
    - Sign in to the practice sessions.

- Not completing the on-site registration in time may result into a team disqualification from the competition.


## Practice

Practice is a session for the teams to train and test their car directly on the track.

- When possible, the practice track should contain all track features used during the competition, but its layout may differ.

_Note: When this happens, there should be another practice session so they can map._

_Second note: Basically before every racing part there should be a practice session on the same track layout. It might be a full practice or just a mapping session._

- Opt-in practices are designated on a first-come-first-serve basis.

- During the practice sessions: (Probably removed for violations.)

    - Teams attending the practice session should be ...
    - Teams that are not taking part in the practice session should avoid the track at all times.

- Upon decision, a special practice session for mapping the track may be issued.

_Felix: This is never specified what it means. Should we specify that it is open practice with a speed limit? Speed limits are enforced by average measurements. If teams exceed the speed limit..._

_J: Yes, we need to define that properly. It might be closed practice, shared practice (with limited speed)... whatever we think is suitable._


### Practice variants

_Note: I will do variants in this way. They might show differently based on your CSS, but they should be quite minimal; "list-like"._

A list of possible practice variants follows. Competition rules specify which of them apply.


#### Shared Practice (Group)

Practice session where the track is opened for a subset of teams specified by organizers.


#### Open Practice

Practice session where the track is opened for all teams.


#### Closed Practice (Single)

Practice session where the track is reserved for one team only.


#### Mapping Practice

Practice session used for mapping the track.

- Teams are not allowed to test their racing algorithms during this practice.
- A speed limit may be employed for this practice, especially when it is Shared.


### Violations

- Teams are not allowed to obstructing other teams by any means (e.g., leaving a stationary car on the track outside of the designated area).
- Teams are not allowed to endanger other teams and cars by an inappropriate behaviour.

_Note: Racing violations are not applied here._

_Note: Penalties are not the same as violations._


## Inspection

The purpose of the Inspection is to check that the hardware of the autonomous cars meets the competition requirements and the cars are not dangerous for the environment, opponents, and people.

- The inspection of the vehicles is done in a dedicated time-frame.
- The inspection is done by the race referees.
- The inspection has to be completed before the Qualification and after any significant changes to the cars hardware or algorithms during any of the days of the event.
- When a hardware list is submitted as a part of the registration, the car is checked to match these parameters.
    - Organizers may also approve using cars that do not match their parameters.
- Car that is not inspected and approved is not allowed to be used in the competition.


## Qualification

Qualification is a session testing the autonomous capabilities of the racing car.

_Felix: Is crash defined somewhere? Touching would be okay, right? Or is all kind of contact forbidden? Then we need to make it possible to do it_

_J: Food for thoughts._

- Complete a single lap without touching and crashing anything. Anything can be:

    - Track borders
    - Obstacles
    - Other cars

- Qualification is done with a single racing car on the track.
- Only inspected and approved car can be used in the Qualification.
    - In case the team intends to use multiple cars during the competition, they have to qualify with all of them.

- The Qualification may be merged with Time Trial.
    - In this case the obstacle avoidance capability has to be checked separately during a dedicated session. _Felix: or during open training?_

- Teams register for the Qualification slot in a FCFS way.

- There are no penalties. Touching and/or crashing results into another try. (Up to the time limit.)
    - Teams may manually place the car to the starting line.

- Organizers might add more slots based on the success rate of the teams.


## Race ...

_Note: Just a placeholder to put stuff here in case I can actually make a general race section._

- Following methods may be used during a race...
    - The race stewards will utilize a system of colored flags to communicate with the teams.

- Starting the race
- Process of stopping (pausing) the race


## Time Trial

_Note: Competition rules should specify: #heats, time per heat; e.g. 2x5 minutes._

Time Trial is a race with a goal to drive through the designated track as fast as possible and as consistently as possible. The idea is to push the algorithms to their limits.

- Each team must pass the Qualification to be able to participate in the Time Trial.

- Time Trial is used as a seeding technique for the Head-to-Head Race.

- The race consists of multiple heats, two by default. Each heat lasts for a given time (e.g., 5 minutes), and the goal is to drive a single lap in as short time as possible and to drive as many complete laps as possible. Crashing and stopping the car does not pause the heat timer.

- Teams have to book (FCFS) a time slot in each heat. The heat timer is fixed to the time slot and no extensions are given. Missing out a time slot does not give the team an additional slot.

    - Upon their mutual agreement, the teams are allowed to exchange the slots by informing the responsible organizers.

- The teams are allowed to change the configuration of their algorithms in between the heats, and even during the heat. When the configuration is changed during the heat, the car must stand still. In other words, the teams cannot update the configuration on-line while the car moves.

- The map (track layout) is known a priori (from a practice before) and the track layout does not change during the race. Keep in mind that cars crash into the walls and the layout of the track might slightly shift a little bit. Please consider this in your algorithms.


### Penalties

- Touching the border of the track is not penalized. Excessive, repeated touching (up to the organizers) is considered a crash.

- Upon crashing the track border, the team has to stop the car and move it (by hand or using the remote control) on the side of the track next to the latest position before crash. After repairing the track, the car may continue. The time spent on moving the car and repairing the track is considered the penalty.

_Note: Violations should be here as well, but I want to have them somewhere in one place._

_Felix: Yes, maybe move them to a separate section and clearly specify what the consequences are_

### Evaluation

- Each team will be evaluated based on the following criteria:

    - Lap time. It will be measured with a time-keeping system provided by the race director.
    - Consecutive uninterrupted laps.

- Evaluation is performed in multiple categories, each one resulting in its result table.

    - Fastest laptimes: Teams are ranked based on their fastest lap times.
    - Consecutive uninterrupted laps: Teams are ranked based on the highest number of consecutive uninterrupted laps they complete.

- Points are awarded in each category separately according to the ranking of the teams.

    - A (1) Point is given for completing at least one heat.
    - A (1) Point is given for every team that has worse scoring.

- The final score for the Time Trial is the sum of the points from all categories.

    - Note that the best achieved results may be from different time slots.
    - This allows teams to push their algorithms to the limits in each of the categories.

- Should a tie occur in the final ranking, the team with more laps is ranked higher. Additional tie is, with respect to the seeding, resolved by a random method (e.g., coin flip).


## Head-to-Head Race

_Competition rules have to specify: Timeslot, competition type, ..._

_Outline: What?, General overview, starting position, race start, race rules, penalities, etc._

Head-to-Head race is a race with multiple cars on the track at the same time.

- One head-to-head race consists of two teams racing against each other. One race has a dedicated timeslot, e.g., 10 minutes.

_Note: Add something about starting on time, regardless of the teams._

- The initial placement of the competing cars in one of the following ways. Competition rules specify which are used.
    - **Side-by-Side**: Both competing cars start on the same starting line.
        - The teams will start side-by-side seperated by one car width (30cm) from each other.
    - **Grid**

- In the first round, the team that ranked higher in Time Trial chooses the starting position. In the second round, the teams switch sides.
- Should a third round be necessary, a coin flip will determine the starting position. The team that ranked higher in Time Trial will call the coin flip (i.e., heads or tails). The team that wins the coin flip chooses the starting position.

- The race starts in one of the following ways. Competition rules specify which are used.
    - _TODO: How the race starts._
    - **Manual**
    - **Automatic**
    - _Felix: You can copy that part from the corresponding section in the T2V module blog post (and read it again...)_

- Overtaking the opponent may be carried out on either the right or the left.

- As opposed to Time Trial, no reconfiguration is allowed during the race, except after a crash, as described below.

- Ultimately, organizers reserve the right to assign blame in the case of vehicle collision in the head-to-head tournament.


### Tournament types

Below a list of possible tournament types follows. Competition rules specify, which are used. <!--add the who starts where and who wins here-->

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


#### Single Cup + Final Four

All teams are racing in the same cup using double elimination bracket, but the finals (with the top four teams) are performed using single elimination bracket.

- The double-elimination tournament with two brackets is seeded by results of the Time Trial.
- The two winners of each bracket will qualify to compete in the Final Four race. This final tournament will feature a single elimination bracket.


#### Double Cup (??? Cup, Master Cup)

During the seeding, the participants are split into two groups, cups. Note that the rules may differ between the cups.

Admission to Master Cup (with respect to the seeding) is done as follows:

- Master Cup may contain up to the half of the team roster.
- First 4 teams automatically proceed.
- Up to the first half, all teams have an opportunity to either join or not.
- The rest of the master cup teams may be filled by teams that placed top 3 in the last 3 years (1100 days).

If the racing track is changed for the Master Cup, the teams are given an extra practice session to test their car and algorithms on the new track.


### Penalties

- Touching the border of the track or a static obstacle is not penalized. Excessive, repeated touching (up to the organizers) is considered a crash.
    - Track abuse: If a team abuses the track (e.g., deliberately cutting corners, damaging the track, or violating race boundaries excessively), they will be penalized. Penalties will be decided by a group of referees, and their decisions are final.

- Upon crashing the track border, the team has to stop the car and move it (by hand or using the remote control) on the side of the track next to the latest position before crash. After repairing the track, the car may continue. The time spent on moving the car and repairing the track is considered the penalty.
    - During all of this, the opponent’s car must not be restricted by the team’s actions and the opponent is allowed to further race without stopping its car.

- The algorithms must not intentionally hinder the opponent or perform any damage to it. Specifically, maneuvers such as deliberate crowding of a car beyond the edge of the track or any other abnormal change of direction are strictly prohibited. The referees will have the final say in whether a driver is in violation of this rule.

- Touching the opponent (e.g., light side-bumps and slow-speed nudges) is not penalized.

- Upon crashing the opponent (e.g., one of the cars significantly diverges from its expected trajectory), these steps are applied:

    - Referees call the crash and pause the race. _and signal for it by raising the red flag._ <!--NAME_CONSISTENCY: stewards?-->
        - Not adhering to the race pause may result into a warning.
    - Referees judge which car is at fault.
    - Both cars are placed at the location of the crash, with the at-fault car placed behind the other car by 2 meters.
        - If the team that was crashed into is able to autonomously detect and recover from the crash by stopping on the side of the track, that team is granted an extra head-start of 1 meter before resuming the race (i.e., the at-fault car is placed 3 meters behind the other car).
    - The referees resumes the race. _with a green flag._

_Felix: add whistles as signals?
Also:
define flag and whistle signals_


### Violations

- A crash is not considered a warning unless judged by the referees.
    - Crashes that result in a warning include but are not limited to "malicious" crashes where the autonomous car did not attempt to slow down or steer away from the opponent.
- Under special circumstances, the referees may decide to give a warning to a team with the option of stopping the race to address the issue. The team has a maximum of 5 minutes to fix the issue and resume the race.
    - This does not apply for double-elimination.

- After 3 warnings, the team is disqualified and the opponent automatically wins.


### Evaluation

- The first car that completes given amount of laps wins.
    - In case that this objective is not achieved by any car, the amount of completed laps along with the achieved progress on the track is the decisive factor.

_TODO: List other tiebreaker factors, e.g., overtakes, crashes._

There will be at least three referees.
One referee will be assigned to each car and is solely responsible to call flag raises and rule violations per-team. The third referee is tasked with enforcing penalties, crash resolution, and time-keeping.



---

Registration form -> ??? + Sending all materials -> REGISTERED/ELIGIBLE

- ELIGIBLE + On-site Registration -> ATTENDING
- ATTENDING + Inspection -> INSPECTED
- INSPECTED + Qualification -> QUALIFIED
- QUALIFIED + Time Trial -> CUP
- CUP + Head-to-Head -> PLACED


----

Notes by Felix

- classic & pro series, pro series has little time
    - new features only in pro series, after evaluation
    - then they can move to classic series
    - only relevant for features that hinder beginner teams
- multiple tracks, should be the same
- mapping session (speed limited sections)
- check: avoid static & dynamic obstacles
- strict timing
- hardware specs before race (at registration) online & published after competition
- different friction surfaces (carpet, floor)
- T2V
- starting positions: pole position? until second corner, start is repeated on crash
- check: double elimination
- gaps in track borders
- time per races
- track behavior (no jumping, injuries are own fault)
- "racer stance"
- workshop incentive? blocked from all races for the next year
- pit lane/parking spots
- check: track width
- check: track boundaries, lidar perceivable material
- bridges: details TBD, maximal height of car, up to 10%, 40cm height

how to keep stray cars from going into other track

live stream and stuff, with GDPR

discussion of future of roboracer at Workshop
