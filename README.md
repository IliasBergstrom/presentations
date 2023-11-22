# Presentations

### [The architecture of digital audio workstations (and other time-based media software)](https://sched.co/1PudM)
#### ADC 2023 - [PDF Slides](https://github.com/IliasBergstrom/presentations/blob/main/Ilias%20Bergstro%CC%88m%20-%20The%20Architecture%20of%20Digital%20Audio%20Workstations.pdf) - Video (will link when available)

The ADC community has produced a wonderful wealth of material on audio software development!
But there is a relative dearth on “the big picture”: of how all these coding techniques, practices, strategies, and design patterns, can interrelate, giving rise to the complex beast that is a modern Digital Audio Workstation (DAW).

While there are some open-source DAWs to study, there is little material on their architecture, apart from the source code itself - with the main exception being the (GUI-less) Tracktion engine of course.

Although implicit / emergent architecture may be sufficient for small to medium size codebases, a large codebase such as a DAW demands deliberate attention to design.

We present the low-level design patterns for the DAW engine and presentation layers, the UI/UX design patterns these interrelate to, and the architectural design patterns for the complete system. Crucially, the main emphasis of our talk is not the details of the above, but how they all together define a modern DAW.

We then present the challenges faced in defining such an architecture to satisfy the specific Attributes of a DAW - e.g. a non-destructively alterable model, and the real-time constraints that necessitate lock-free communication between threads. We discuss the compromises needed to satisfy such conflicting needs, and some future challenges presented, as the software category evolves into the future, e.g. with MIDI 2.0 around the corner.

While we concentrate on DAWs, much of this discussion also generalises to the broader category of Time-Based Media software.

The presentation is grounded in two DAW-like applications we have developed: one is a desktop application with a GUI, and the other is a “headless”, embedded DAW, with a separately executed GUI application. They are both very different, each lacking central features that the other has. But together, and even more so through their differences, they serve as great illustrations of the concepts we present.

This subject area is vast, and a review of every topic and technique is impossible in the scope of a single talk. We give a good introductory overview, hopefully laying a foundation for further learning and knowledge dissemination in the community.

### [Detaching the UI - Options and challenges for controlling headless and remote audio software](https://sched.co/19wdb)
#### ADC 2022 - [PDF Slides](https://github.com/IliasBergstrom/presentations/blob/main/ADC%2022%20-%20Detaching%20the%20UI%20-%20Ilias%20Bergstro%CC%88m%20%26%20Gustav%20Anderson.pdf) - [Video](https://www.youtube.com/watch?v=HfyUe4NLBdM)

Audio software running in “headless” or remote contexts, i.e. without access to a tightly integrated GUI, is increasingly common, either when running in embedded devices, on a remote cloud server, or distributed over a local network where remote/automated control is desired.

The parameter controls exposed over plugin API’s are insufficient, since the practically usable implementations only support a fraction of the variety necessary. Developers expose many additional controls over the GUI, which doesn’t translate to headless or remote uses.

Plugin GUI’s can be as involved as a fully-fledged DAW, exposing complex interactions. Although MIDI 2.0 will in the medium term replace some of what we discuss, even with full adoption, it doesn’t cover the many interactions possible from a GUI.

In this article we discuss three basic Distributed Systems patterns, for controlling audio software during run-time over a network: simple socket messaging, request/response, and publish/subscribe.

We also demonstrate their implementation using the OSC and gRPC frameworks, discussing challenges and best practices specific to real-time audio.

Grounding the above, we provide a pair of ready to use, fully fledged open-source applications implementing our suggestions, both available to download.

### [Deploying plugins on hardware using open-source Elk Audio OS](https://sched.co/Ww7f)
#### ADC 2019 - [PDF Slides](https://github.com/IliasBergstrom/presentations/blob/main/Elk%20Talk%20Slides%20ADC19.pdf) - [Video](https://www.youtube.com/watch?v=HfyUe4NLBdM)

[Elk Audio OS](https://www.elk.audio/start) significantly streamlines deploying great audio software across digital hardware devices, such as synthesizers, drum-machines and effect pedals.

We take care of the obstacles and specialist knowledge for deploying on extremely high-performance embedded Linux devices, letting developers concentrate on what they do best - creating awesome audio software and products.

In this talk we present the strategies and tools embodied in our platform, using which existing audio plugins can very efficiently be deployed. We will show how plugins can be built for Elk using various tools and frameworks, including JUCE.

An open-source version of Elk will be released shortly after the ADC conference, together with a multi-channel expansion Hat for Raspberry Pi. We will discuss the details of the open-source license, and the implications for releasing products based on Elk.
