% FTQC HEM3 — Hackathon & Exchange Meeting

<div class="hero">
  <div class="hero-date">2026/11/25(Wed)–27(Fri)</div>
  <h1>FTQC HEM3</h1>
  <p class="hero-subtitle">FTQC Hackathon &amp; Exchange Meeting for 3 days @ The University of Osaka </p>
  <p class="hero-organizer">Organized by Shin Nishio<br>
  Research Associate, University College London<br>
  Project Assistant Professor, Keio University</p>
</div>

<nav class="site-nav">
  <a href="#background">Background</a>
  <a href="#program">Program</a>
  <a href="#resources">Resources</a>
  <a href="#participants">Participants</a>
  <a href="#venue">Venue</a>
  <a href="#further-plans">Further Plans</a>
  <a href="#contact">Contact</a>
</nav>

## Background &amp; Motivation {#background}

FTQC theorists are working across different physical-system projects in Moonshot, and there is an opportunity to further promote theoretical research and collaboration across different physical systems, within the Moonshot program and more broadly across Japan.  Following the success of the [decoder camp](https://github.com/ysuzuki-qc/qec_camp_1d_rep_code) held at Kyushu University in February 2026, we will host a hackathon and exchange meeting in Osaka to further facilitate such interactions and bring together FTQC theorist / experimentalist from across the Moonshot program and beyond.

The event will also provide opportunities for interaction and collaboration with observer companies. Participants will utilize software developed through Moonshot projects, such as device-aware compilation tools, noisy-circuit simulators, and resource estimators for FTQC.

The goal of HEM3 is not necessarily to produce a completed implementation during the event. We encourage participants to use the hackathon to identify interesting research questions, develop new formulations, test early ideas, and initiate collaborations that may continue beyond HEM3.

**Organizers**: Shin Nishio,  Dr. Fumiyoshi Kobayashi (Mercari)<br>
**Local Organizer**: Mr. Nilton Filho<br>

## Program {#program}

### Day 1 — Introduction to each system &amp; software suite <span class="tag">tentative</span>

<span class="star">★</span> connected to [Stim](https://github.com/quantumlib/Stim)

| Time | Session | Presenter |
|---|---|---|
| 10:00 | Opening & Discussion: What are the **wrong** abstractions in current FTQC? | Nishio |
| 10:30 | **TBA** <span class="star">★</span> (trapped ion): compiler &amp; noisy circuit sim | Mr. Ishikawa |
| 11:00 | **Losssim** <span class="star">★</span>: circuit-level loss / erasure sim | Nishio |
| 11:30 | **TBA** (neutral atom) <span class="star">★</span>: compiler &amp; noisy circuit sim | Dr. Kobayashi |
| 12:00 | Lunch and discussion | — |
| 13:30 | **TBA** (superconductor): compiler &amp; noisy circuit sim | Prof. Matsuzaki |
| 14:00 | **Quration**: resource estimator for FTQC | Dr. Suzuki |
| 14:30 | **VeriQ** | Prof. Soeda |
| 15:00 | Brainstorming &amp; team forming (if necessary) | Nishio |
| 16:00 – | Happy Hacking! | — |

### Day 2 — Hacking
13:00-13:30 Mid discussion

### Day 3 — Hacking and Presentations
We have a presentation for the hackathon results and hold a dicussion.

### What shall we work on?

* Hardware-aware something — decoding, resource estimation, compilation, ...
* Design architecture and criteria
* Try your favorite codes on multiple devices
* Make simulators faster (especially loss sim is very slow...)
* Connect simulators and resource estimator
* Program analysis on intermediate representations

## Resources {#resources}

<span class="star">★</span> connected to [Stim](https://github.com/quantumlib/Stim)

| Tool | Description | GitHub Repository |
|---|---|---|
| **Traqer** <span class="star">★</span> | (QCCD trapped-ion) Compiler &amp; noisy circuit sim | TBA |
| **Losssim** <span class="star">★</span> | Circuit-level loss / erasure sim | TBA |
| **TBA** <span class="star">★</span> | non-Clifford circuit simulator for non-Pauli stabilzer codes | TBA |
| **TBA** <span class="star">★</span> | (neutral atom) Compiler &amp; noisy circuit sim | TBA |
| **TBA** | (superconductor) Compiler &amp; noisy circuit sim | TBA |
| **Quration** | Resource estimator for FTQC | [quration/quration](https://github.com/quration/quration) |
|**VeriQ**| TBA | TBA |

## Participants <span class="tag">tentative</span> {#participants}
TBA

* Expected attendance: about 20 people (may vary depending on the venue)
* We’d like to focus on researchers who can actively participate in hands-on activities
* In general, we’ll invite people who are open to future collaborative research and for whom it is administratively feasible
* We’ll also invite people who are developing error budgets/simulator for each hardware.

Let me know if you have any candidates!

## Venue <span class="tag">tentative</span> {#venue}
Toyonaka Campus, The University of Osaka

<center>
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3276.1233744285023!2d135.45138478553164!3d34.80283780782253!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6000fb00695fa84b%3A0x85cdf459e55340f4!2z5aSn6Ziq5aSn5a2m6YeP5a2Q5oOF5aCx44O76YeP5a2Q55Sf5ZG956CU56m244K744Oz44K_44O8IENlbnRlciBmb3IgUXVhbnR1bSBJbmZvcm1hdGlvbiBhbmQgUXVhbnR1bSBCaW9sb2d5LCBUaGUgVW5pdmVyc2l0eSBvZiBPc2FrYe-8iFFJUULvvIk!5e0!3m2!1sja!2ses!4v1786111054944!5m2!1sja!2ses" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="strict-origin-when-cross-origin"></iframe>
</center>

## Contact {#contact}

All details on this page — venue, and participant list — are still tentative. If you're interested in joining, or have suggestions for participants, tools, or venues, please get in touch.

* Shin Nishio — email: parton (at) sfc.wide.ad.jp
* [parton-quark.github.io](https://parton-quark.github.io/)
