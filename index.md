# Epochalypse Project

Y2K38, the Year 2038 Problem, or simply the Epochalypse is approaching fast.

19 January 2038 at 03:14:07 UTC software and hardware implementations relying on 32-bit signed integer standard epoch timestamps will overflow, resulting in a system time of 20:45:52 UTC on 13 December 1901. (So-called "Unix epoch time" is a concept far more ubiquitous than Unix itself within our technology stack, this bug impacts a wide array of platforms.)

For the purposes of not constantly repeating ourselves below, we will stop saying "19 January 2038 at 03:14:07 UTC" and just call it "zero hour."

For most impacted systems, the result will be some chaotic breakdown of running state machine logic in which the flow of time logically reverses itself and/or division by zero occurs in sensitive time-handing code.

If it helps, think about the odometer in a car. When you put enough kilometers/miles on it, the odometer which measures the use of the car will rollover back to all zeros. That is what will happen with many many systems supporting our digital society if we fail to take adequate action.

There are today approximately two orders of magnitude (100x) more systems needing to be checked and fixed than there were in the years leading up to Y2K. In order to address the 32-bit timestamp vulnerability (aka, "the Y2K38 bug") we are going to have to pull a lot of fielded equipment out of the ground, test it in a lab, and put remediations in place, all across the globe, and during the next 52 quarters (slightly over 12 years.) Let that sink in for a bit.

The 32-bit timestamp vulnerability presents a real challenge for any system reliant on 32-bit timestamps. Our research documents how various systems and devices react as they approach and cross the zero hour threshold. We are documenting classes of failure modes triggered by these programming flaws using controlled experiments across multiple environments, including IoT devices, ICS/OT, and embedded systems.

These findings reveal some critical risks that our society cannot afford to ignore, especially given that for a resourceful attacker, 2038 can be any old day they like.

# What can I do? How can I help?

## Safety Reminders for Everyone

*Important: No matter who you are, follow these safety guidelines:*

- Only test systems you own or have permission to test
- Never test on production systems or critical infrastructure
- Back up important data before testing
- Physically isolate systems with changed dates to prevent time confusion
- **WARNING: USE CARE THAT FALSIFIED (TESTING) TIME SIGNALS DO NOT LEAK OUTSIDE YOUR INTENDED TESTING ENVIRONMENT.**
- Return systems to the correct date after testing
- Document everything you find, even if it seems minor
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.


## Literally anyone on the internet reading this

Even if you're just someone who heard about the 32-bit timestamp rollover problem on a podcast, you can help:

- Test your own smart devices at home by changing their dates to zero hour
- Take photos of any error screens or weird behavior
- Check your smart TV, fitness tracker, home security system, or connected appliances
- Try entering dates beyond zero hour in websites you use (like booking sites or calculators)
- Join our online community discussing the 32-bit timestamp rollover problem to share what you find
- Ask companies about their 32-bit timestamp rollover readiness when buying new tech
- Spread awareness by telling friends and family about the issue
- Test non-critical smartphone apps by changing your device date
- Submit your findings to us, we are tracking the 32-bit timestamp rollover problem!
- Raise awareness of this issue with your government officials and any geeky/techie friends who might be able to help us!
- Consider joining our [mailing list](https://groups.io/g/epochalypse-discuss) and/or our [discussion forums](https://github.com/orgs/Epochalypse-Project/discussions).
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Manufacturers

As a product manufacturer, you can help by:

- Testing your products by changing system times to zero hour and beyond
- Documenting all error messages, crashes, or unusual behaviors in your products
- Creating test certificates with expiration dates beyond zero hour to check proper certificate handling
- Updating your product security requirements to include 32-bit timestamp rollover mitigation
- Testing database systems that store timestamps to ensure they handle dates beyond zero hour
- Including 32-bit timestamp rollover testing in your vulnerability management procedures
- Sharing non-confidential test results with the wider community to help others
  - TODO: add link to reporting form when it's published
- Developing firmware/software updates for affected products
- Including 32-bit timestamp rollover compliance in your product documentation and conformity assessments
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Importers

As a product importer, you can help by:

- Verify that manufacturers have tested their products for 32-bit timestamp rollover compliance
- Request documentation of 32-bit timestamp rollover testing from your suppliers
- Conduct your own sample testing on imported products by changing dates to zero hour
- Check smart devices in your inventory by changing their dates forward to zero hour
- Test how imported products handle certificates with expiration dates beyond zero hour
- Maintain records of which products have been tested for 32-bit timestamp vulnerabilities
- Inform manufacturers of any 32-bit timestamp vulnerabilities you discover
- Ensure proper labeling of products that have been verified as 32-bit timestamp rollover safe
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Distributors

As a distributor of digital products, you can help by:

- Ask manufacturers and importers for information about 32-bit timestamp rollover compliance
- Test demo units in your inventory by changing their dates to zero hour
- Document and report any errors or strange behaviors to manufacturers
- Check if product documentation mentions 32-bit timestamp rollover readiness
- Help raise awareness among customers about the 32-bit timestamp rollover problem
- Create a simple checklist for customers to test their own devices
- Share testing results with suppliers to help improve products
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Authorized Representatives

As an authorized representative, you can help by:

- Coordinate 32-bit timestamp rollover readiness testing efforts between manufacturers and competent authorities
- Maintain documentation of 32-bit timestamp rollover testing
- Help manufacturers understand their obligations regarding long-term support
- Ensure technical documentation addresses the 32-bit timestamp rollover problem
- Facilitate information sharing about discovered vulnerabilities
- Connect manufacturers with competent testing resources
- Help prepare conformity declarations that include 32-bit timestamp rollover considerations
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Government Official

As a government official, you can help by:

- Develop official guidance documents on the 32-bit timestamp rollover problem for critical infrastructure operators
- Create regulatory frameworks that require 32-bit timestamp rollover compliance in public procurement
- Establish reporting mechanisms for organizations to disclose 32-bit timestamp rollover vulnerabilities
- Coordinate cross-border exercises simulating 32-bit timestamp rollover scenarios in critical sectors
- Assess national-level risks from the 32-bit timestamp rollover problem for essential services
- Develop sector-specific guidelines for industries like healthcare, transportation, and energy
- Allocate research funding for 32-bit timestamp rollover mitigation solutions
- Host workshops bringing together public and private stakeholders to address the challenge
- Update existing technical standards to include 32-bit timestamp rollover compliance requirements
- Create certification schemes that verify products are protected against the 32-bit timestamp rollover problem
- Develop public awareness campaigns about the potential impact on citizen services
- Establish emergency response protocols for potential 32-bit timestamp rollover-related disruptions
- Incorporate 32-bit timestamp rollover readiness into existing cybersecurity capability assessment frameworks
- Provide technical assistance to smaller member states with limited resources
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Cybersecurity Researcher

As an experienced cybersecurity researcher, you can help by:

- Disassemble and analyze firmware of embedded systems to identify 32-bit timestamp rollover vulnerability patterns
- Reverse engineer proprietary time-handling protocols to check for 32-bit integer usage
- Create fuzzing tools specifically designed to test time-related functions and APIs
- Develop proof-of-concept exploits that safely demonstrate 32-bit timestamp rollover vulnerabilities
- Map the attack surface of critical systems related to time handling
- Audit low-level code in open source projects for time_t dependencies
- Analyze binary blobs in IoT devices for time overflow vulnerabilities
- Share your findings through responsible disclosure channels
- Create detection signatures for common 32-bit timestamp rollover vulnerability patterns
- Mentor junior researchers on time-related vulnerability hunting techniques
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Incident Responder

As a seasoned incident responder, you can help by:

- Develop incident response playbooks specifically for time-related failures
- Create forensic tools that can analyze systems after simulated 32-bit timestamp rollovers
- Build containment strategies for potential cascading failures from time errors
- Test backup and recovery procedures against 32-bit timestamp rollover scenarios
- Design tabletop exercises that simulate 32-bit timestamp rollover-related incidents
- Analyze logs for timestamp handling anomalies when testing with future dates past zero hour
- Document patterns of system behavior before and after simulated time rollovers
- Create a 32-bit timestamp rollover incident classification framework to standardize reporting
- Train response teams on recognizing time-related system failures
- Review existing CERT advisories for time-handling vulnerabilities
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## Software Developer

As an experienced software developer, you can help by:

- Audit codebases for 32-bit time_t usage and upgrade to 64-bit implementations
- Review legacy code for hardcoded time assumptions or magic numbers related to timestamps
- Create unit tests specifically targeting time handling past zero hour
- Refactor time-dependent algorithms to handle the 32-bit timestamp rollover transition gracefully
- Develop time simulation libraries to facilitate easier testing of future dates
- Check serialization/deserialization routines for proper handling of future timestamps
- Review database schemas and ORM implementations for time field limitations
- Audit third-party libraries and dependencies for time-handling issues
- Implement time-related error detection and graceful recovery mechanisms
- Document patterns and anti-patterns in time handling for your organization
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

## QA Tester

As a veteran QA professional, you can help by:

- Develop comprehensive test suites specifically for time-related functions
- Create automated testing frameworks that can simulate system time manipulation
- Design edge cases specifically targeting date and time handling
- Build regression test suites that verify fixes for 32-bit timestamp rollover-related bugs
- Create testing environments with virtualized time that can simulate zero hour and beyond
- Develop performance tests that measure system behavior before and after the zero hour threshold
- Document testing methodologies specifically for time-dependent systems
- Create time-related test data generators that produce dates spanning beyond the zero hour
- Design test matrices that cover various time zones and daylight saving time scenarios
- Train QA teams on specialized techniques for temporal testing
- Consider submitting useful findings, testing methodology, tips and tricks, etc. with us, we are coordinating a global response to the 32-bit timestamp rollover problem.

By working together across all these roles, we can identify and fix 32-bit timestamp rollover problems before they cause real issues!
