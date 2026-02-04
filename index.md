# The Epochalypse Project
## Time Integrity & Epoch Rollover Risk (2036–2038)

**→ Read the FAQ: [FAQ — 2036/2038 Epoch Rollover Risk](faq.md)**

**On 2038-01-19 03:14:08 UTC, systems that still rely on the ubiquitous 32-bit signed Unix timestamp (`time_t`) may experience incorrect time calculations, mis-ordered events, crashes, or other failures — unless remediated or architected to tolerate rollover.**

Attackers don't need to wait. Weaknesses in time synchronization mechanisms and time-dependent logic can be exploited today by inducing or amplifying time anomalies.

This is not science fiction. It is a real engineering and security risk affecting systems we rely on daily — from industrial automation and telecom infrastructure to embedded devices and long-lived operational technology.

---

## Why should you care?

Time is a shared dependency — the coordination backplane of our digital world. When timestamps become incorrect, or when systems disagree about time, failures can be hard to predict and even harder to diagnose.

Potential impacts include:

- Incorrect scheduling or logging (mis-ordered events, audit gaps)
- Failures in time-based authentication, token validation, or certificate handling
- Data corruption or replication errors in time-ordered systems
- Malfunctioning monitoring and alerting (false positives / false negatives)
- Disruptions to industrial processes or safety-critical systems

Not every system will fail on the rollover moment. Not every failure will be catastrophic. But the risk is real, widespread, and concentrated where patching and replacement cycles are slow.

---

## What is the 32-bit timestamp problem?

Many systems represent time using a 32-bit signed integer counting seconds since 1970-01-01T00:00:00Z ("Unix time"). When this counter overflows, affected systems may interpret subsequent timestamps as dates in 1901.

| Event | Timestamp |
|-------|-----------|
| Pre-rollover  | 2038-01-19 03:14:07 UTC |
| Post-rollover | 1901-12-13 20:45:52 UTC |

This is the **Year 2038 problem** (Y2038 / Y2K38).

Where it shows up:

- Legacy Linux/Unix environments and older libc/toolchains
- Widely-used network protocols
- Common data formats
- Embedded and industrial devices using 32-bit time representations
- Long-lived appliances and IoT devices with unclear ownership and/or update paths
- Databases storing time values as 32-bit epoch seconds

The core risk pattern: **time representation limits + long-lived deployment + slow remediation.**

---

## Why attackers don't have to wait

Many systems treat time as a trust input. If an attacker can influence a device's clock, they may trigger time-dependent failures early:

- Bypass or break time-based authentication
- Force premature expiration of certificates or tokens
- Induce mis-ordering of events, logs, or database records
- Cause monitoring and alerting failures

This doesn't mean attackers can magically flip every system into 2038 behavior. It means **time integrity is a security boundary**, and insecure time synchronization turns timekeeping bugs into operational security issues.

---

## Related rollover events

Y2038 is not the only time-related rollover in this critical two-year window:

| Event | Date |
|-------|------|
| NTP Era rollover | 07 February 2036 |
| 32-bit `time_t` rollover | 19 January 2038 |
| GPS week number rollover | 20 November 2038 |

These events affect different technologies, but often intersect operationally in real systems. The common thread: **time assumptions that were safe when systems were young become dangerous when systems live for decades.**

---

## Why this is hard

The challenges compound:

1. **Long-lived deployments** — many affected devices are designed to run 10–30 years
2. **Embedded and OT constraints** — patching may be difficult, risky, or impossible
3. **Supply-chain opacity** — organizations often don't know which components contain time limits
4. **Shared dependencies** — time failures cascade across systems assuming consistent timestamps
5. **Incentive mismatch** — remediation costs are local; benefits are global
6. **Lack of ownership** — much of the problem lives in the public commons (e.g., free and open-source software) where it's unclear who should fund or oversee remediation

Even where fixes exist, remediation takes time: sufficient talent pool, inventory, testing, vendor engagement, change windows, operational risk management. This is a coordination problem as much as a technical one.

---

## What we're doing

The Epochalypse Project is a collaborative effort to:

- Improve shared understanding of rollover and time-integrity risk patterns
- Develop and share safer testing methodologies
- Document observed device and system behaviors
- Support responsible vendor engagement and coordinated vulnerability mitigation
- Connect practitioners across sectors and standards bodies

We aim to be practical: focus on what can be tested, measured, documented, and improved today.

---

## Who we are

The project was founded by **Trey Darley** and **Pedro Umbelino**, security researchers with backgrounds spanning vulnerability research, incident response, and long-lived digital infrastructure.

This is a volunteer-driven effort to help the community coordinate earlier, test more safely, and reduce surprise as these rollovers approach.

---

## How you can help

### Safety guidelines for testing

Time testing can cause real disruption if done carelessly.

- Only test systems you own or have explicit permission to test
- Never test production systems or critical infrastructure
- Use isolated test environments (lab networks, VMs, offline devices)
- Avoid broadcasting "test time" onto networks others rely on
- Record firmware/software versions and configurations
- Restore correct time after testing and document what changed
- Test multiple times — in many cases, this will not be "one and done" but "rinse and repeat"

**If you're unsure whether a test could affect others, don't run it — ask first.**

---

### For individuals

You can help without touching sensitive systems:

- Identify devices you rely on that are designed to last 10+ years (routers, NAS, IoT hubs, appliances)
- Check whether vendors state 2038/2036 readiness or long-term support policies
- Report vendor documentation gaps and update constraints
- Share safe observations and participate in discussions

**Join us:** [FIRST Time Security SIG](https://www.first.org/global/sigs/time/)

---

### For operators and industry professionals

If you operate or build systems with long lifetimes:

- Inventory time-dependent components (OS, firmware, middleware, logging, databases)
- Request vendor statements on time representation and rollover behavior
- Include time rollover scenarios in QA and change management
- Plan for remediation where updates are possible, mitigations where they're not
- Treat time synchronization as a security control

---

### For researchers and technical contributors

- Identify common patterns of time representation limits in firmware and software
- Design safer test harnesses and reproducible test cases
- Document findings with enough detail to reproduce
- Support responsible disclosure where appropriate

---

## Join the effort

We're building a shared map of risk patterns, testing methods, and mitigation paths — so fewer organizations discover these problems too late and alone.

If you can help test safely, document behaviors, or improve guidance, you're welcome here.

*Let's reduce catastrophic surprise — together. 🕊️*

---

_Epistemic note: This page reflects current understanding as of the date below. 
Specific behaviors vary by system, implementation, and deployment context._

**Page Last Updated:** 2026-01-29
