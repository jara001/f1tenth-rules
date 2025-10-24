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

### Track Features

A list of possible track features follow. Competition rules will specify, which of them (might) apply.

#### Open walls

#### Intersections

#### Surface changes

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



## On-site registration


## Practice

Practice is a session for the teams to train and test their car directly on the track.

Shared Practice (Group)

Open Practice

Closed Practice (Single)


During the practice sessions:

- Teams attending the practice session should be ...
- Teams that are not taking part in the practice should avoid the track at all times.


....

Special practice session for mapping the track may be issued.

## Inspection

- The purpose of the Inspection is to check that the hardware of the autonomous cars meets the competition requirements and the cars are not dangerous for the environment, opponents, and people.
- The inspection of the vehicles is done in a dedicated time-frame.
- The inspection is done by the race referees.
- The inspection has to be completed before the Qualification and after any significant changes to the cars hardware or algorithms during any of the days of the event.

## Qualification

Complete a single lap without crashing into anything. Anything can be:

- Track borders
- Obstacles
- Other cars


## Time Trial

Time Trial is used as a seeding technique for the Head-to-Head Race.

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

The final score is the sum of the points from both categories. Note that the best lap times and the number of laps can be achieved in different time slots. This allows teams to push their algorithms to the limits in each of the two categories.

Should a tie occur in the final ranking, the team with more laps is ranked higher.

The qualification is passed by finishing a single lap without crashing. Otherwise, the team is disqualified from the competition.
## Head-to-Head Race

All-vs-all

Single Elimination Bracket

Double Elimination Bracket



Seeding

Random Seeding

Time Trial seeding



Single Cup

Double Cup (??? Cup, Master Cup)

Participants are split into two groups, cups. Note that following rules may differ between the cups.

First 4 automatically proceed.

Up to the first half, all teams have an opportunity to either join or not.

The rest of the teams may be filled by teams that placed top 3 in the last 3 years, 1100 days.


Upon changing the track, teams are given an extra practice session to test their car and algorithms on the new track.