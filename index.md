# Epochalypse Project 

19 January 2038 at 03:14:07 UTC implementations relying on 32-bit signed integer representations of Unix epoch time will overflow, resulting in a system time of 20:45:52 UTC on 13 December 1901. (Unix epoch time is a concept more ubiquitous than Unix itself, this bug impacts a wide array of platforms.)

For most impacted systems, the result will be some chaotic breakdown of running state machine logic in which the flow of time logically reverses itself.

Y2K38, the Year 2038 Problem, or simply the Epochalypse is approaching fast

There are today orders of magnitude more systems needing to be checked and fixed than there were in the years leading up to Y2K. In order to address the Y2K38 bug we are going to have to pull a lot of fielded equipment out of the ground, test it in a lab, and put remediations in place, all across the globe, and during the next 13 years. Let that sink in for a bit.

The Y2K38 bug presents a real challenge for any system reliant on 32-bit timestamps. Our research documents how various systems and devices react as they approach and cross the 2038 threshold. We are documenting classes of failure modes triggered by these programming flaws using controlled experiments across multiple environments (including IoT devices, ICS/OT, and embedded systems.

These findings reveal some critical risks that our society cannot afford to ignore, especially given that for a resourceful attacker, 2038 can be any old day they like.
