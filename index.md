# Epochalypse Project 

Raising awareness about the 2038 bug in all its manifestations and trying to fix things while there's still time.

In the early days of the computing age, RAM was expensive and programmers represented timestamps using a two digit year.

As the year 2000 approached, retired developers were brought back into the workforce to fix legacy systems so that they would not crash on 01 January 2000. Remediation efforts were aided by the fact that there was a widespread fear of apocalyptic scenarios manifesting to coincide with the change of millenia and this cultural hype, combined with the novelty of dawning public awareness of the existence of the global internet (which we take for granted today), served to amplify the public and governmental attention on the so-called Y2K bug as the trigger date approached.

As we all know, the world did not end on 01 January 2000. So hyped was the Y2K bug, and so high the expectation of disaster, that when “nothing” happened the entire thing came off as a dud in the public sphere.
Those of us working in IT know all too well how our work is invisible when things are working properly, and how our work is usually only noticed when things go wrong. There were incidents related to the Y2K bug, and there is a body of academic literature on this topic, however that is tertiary to this talk.

Consider at a high level the types of systems which would logically fail when confronted with an error of the calendar date in some calculation: shipment, hospitality, travel, billing, logistics, etc. Now consider the types of systems which would logically be impacted if they confronted an error with the system clock representation of ticks: basically this can screw with any naively implemented state machine.

19 January 2038 at 03:14:07 UTC implementations relying on 32-bit signed integer representations of Unix epoch time will overflow, resulting in a system time of 20:45:52 UTC on 13 December 1901. (Unix epoch time is a concept more ubiquitous than Unix itself, this bug impacts a wide array of platforms.)

For most impacted systems, the result will be some chaotic breakdown of running state machine logic in which the flow of time logically reverses itself.

Y2K38, the Year 2038 Problem, or simply the Epochalypse is approaching fast

Recall the 2008 financial crisis? That was 16 years ago, and you can see how well we did at making our financial sector safe in the intervening years. Now consider that 2038 is only 13 years from now. We have been furiously digitizing our whole societies for the past 25 years.

There are today orders of magnitude more systems needing to be checked and fixed than there were in the years leading up to Y2K. In order to address the Y2K38 bug we are going to have to pull a lot of fielded equipment out of the ground, test it in a lab, and put remediations in place, all across the globe, and during the next 13 years. Let that sink in for a bit.

The Y2K38 bug presents a real challenge for any system reliant on 32-bit timestamps. In this session we will move beyond conjecture and demonstrate some of the Y2K38 bug’s real-world consequences in real devices. Our research documents how various systems and devices react as they approach and cross the 2038 threshold. We are documenting classes of failure modes triggered by these programming flaws, with the security researcher mindset.

Using controlled experiments across multiple environments (including IoT devices, ICS/OT, and embedded systems) we document unexpected vulnerabilities and behaviors.

These findings reveal some critical risks that our society cannot afford to ignore, especially given that for a resourceful attacker, 2038 can be any old day they like.

This presentation is intended for developers, security professionals, and incident responders seeking to understand more about this issue. We will present technical realities in plain, hopefully so that any high school kid could understand it, therefore policymakers are encouraged to join, because this issue will impact us all soon!

Outline
# Introduction (5 minutes)
* How it began for both of us.
* Overview of Y2K38 and its relevance.
# Context and Methodology (5 minutes)
* The technical basis of Y2K38 (epoch time and 32-bit limitation).
* How this session addresses the gap between speculation and evidence.
* The idea of exhaustive search and classification.
# Case Studies: Real-World Findings (15 minutes)
* Case study 1 .. N Failure modes observed and mitigation experiments.
* Unexpected software behaviors.
* Challenges for critical infrastructure.
# Mitigation Strategies (5 minutes)
* Steps to identify and address Y2K38 risks.
* Long-term approaches for future-proofing systems.
# Implications & Q&A (remaining time if any)
* Interactive discussion on challenges and solutions.
