# Presentations

### [The architecture of digital audio workstations (and other time-based media software)](https://sched.co/1PudM)
####ADC 2023 - [PDF Slides](https://github.com/IliasBergstrom/presentations/blob/main/Ilias%20Bergstro%CC%88m%20-%20The%20Architecture%20of%20Digital%20Audio%20Workstations.pdf) - Video (will link when available)

The ADC community has produced a wonderful wealth of material on audio software development!
But there is a relative dearth on “the big picture”: of how all these coding techniques, practices, strategies, and design patterns, can interrelate, giving rise to the complex beast that is a modern Digital Audio Workstation (DAW).

While there are some open-source DAWs to study, there is little material on their architecture, apart from the source code itself - with the main exception being the (GUI-less) Tracktion engine of course.

Although implicit / emergent architecture may be sufficient for small to medium size codebases, a large codebase such as a DAW demands deliberate attention to design.

We present the low-level design patterns for the DAW engine and presentation layers, the UI/UX design patterns these interrelate to, and the architectural design patterns for the complete system. Crucially, the main emphasis of our talk is not the details of the above, but how they all together define a modern DAW.

We then present the challenges faced in defining such an architecture to satisfy the specific Attributes of a DAW - e.g. a non-destructively alterable model, and the real-time constraints that necessitate lock-free communication between threads. We discuss the compromises needed to satisfy such conflicting needs, and some future challenges presented, as the software category evolves into the future, e.g. with MIDI 2.0 around the corner.

While we concentrate on DAWs, much of this discussion also generalises to the broader category of Time-Based Media software.

The presentation is grounded in two DAW-like applications we have developed: one is a desktop application with a GUI, and the other is a “headless”, embedded DAW, with a separately executed GUI application. They are both very different, each lacking central features that the other has. But together, and even more so through their differences, they serve as great illustrations of the concepts we present.

This subject area is vast, and a review of every topic and technique is impossible in the scope of a single talk. We give a good introductory overview, hopefully laying a foundation for further learning and knowledge dissemination in the community.
