# AI Tools

This should be a blog. In mid 2023 I started building a [digital assistant](https://docs.google.com/document/d/1x52awYN3-fEHk6RjW9Ly-ygbaGhkSxwNGIoS8oXNdS8/). Things got real, real quick. 

Ensuing wisdom broke what was 1 collosal project into a myriad smaller ones, broken into 2 categories:
- Tools - A collection of APIs (an OS in aggregage) that make it possible to build apps requiring digital intelligence.
- Apps - Real-use-case applications that could be built using the said "tools" ("could be" because the apps here were used to develop the underlying "tools" that would've been useful in developing them).

## Tools
The following are generic tools without standalone utility, but meant to provide APIs usable in tailored use-cases (see Apps below for examples).

In aggregate, they can be thought of as a sort of operating system, with `brain` being the kernel and the rest being peripheral components.

The peripherals, while designed to be used by an AI assistant, have no explicit connection to one and can be used in any other programmatic system.

### brain 
[[code]](https://github.com/mgbrian/brain/)

A suite of cognitive features: sensory (audio and visual) and higher cognition (language processing, reasoning, memory, etc.).

This is designed to mimic a human brain's functions, focusing on how it interacts with the environment i.e. input, processing and output.

### files 
[[code]](https://github.com/mgbrian/files/)

Interact with the (Unix+) filesystem.

### phone 
[[code]](https://github.com/mgbrian/phone/)

Send SMS and make/receive live phone calls.

### browser 
[[code]](https://github.com/mgbrian/browser/)

Programmatically browse the web like a human (visually, with a real browser).

### transport 
[[code]](https://github.com/mgbrian/transport/)

Move data between system components (if `brain` is analogous to a human brain, this is the nervous system). Provides both the infrastructure for communication (sockets, client/server code, etc.) between different components as well as a system for message encoding. The communication pipeline and unified declarative encoding make it easy for any part of the system to trigger behaviour in any other part of the system (seamless "function calling" between systems regardless of programming language or machine location).

### Google APIs 
[[code]](https://github.com/mgbrian/google_apis/)

Interact with Google Apps (GMail, Photos, Sheets, Calendar, etc.).

## Apps
Below are applications built (or that could have been built) on top of the above APIs. These apps were built at different stages of the above tools' development, with the express purpose of helping develop a component thereof (in addition to their other use-case):

- Munchking and Minstrel helped develop the LLM interfaces, VAD and live transcription (`brain`).
- eagle-eye -- object detection and camera capture (`brain`).
- catsitter -- live audio/video input/processing alongside simultaneous user interaction (`brain`), all of `phone`, and async server-side processing (in Python).
- tutor - the hard lesson not to try and do this all in one project.
- dev will help develop generic "function-calling" (that works across LLM APIs) and test `files`.
- vector will help develop memory (`brain`).

### vector 
[[code]](https://github.com/mgbrian/vector/)

(Upcoming)

Meant to test memory representation and retrieval techniques.

### dev 
[[code]](https://github.com/mgbrian/dev/)

(Upcoming)

Dev is (meant to be) a hands-free programmer that writes, tests and executes code to/in the filesystem based on external instructions.

### transcriber 
[[code]](https://github.com/mgbrian/transcriber/)

Needs to be renamed to Scribe. Scribe enables voice-typing in jargon-heavy contexts. Scribe provides an editable text input, into which the user can voice-write fully hands-free, while still remaining fully editable in case the user needs to fine-tune certain spellings. Scribe learns spellings and builds a lexicon of jargon that is used going forward. The intended use case for this was a project I was working on requiring hours of live transcription -- I work in a field where half the phrases do not make sense to anybody outside the field and a lot of the key vocabulary is written in PascalCase.

 * Handwriting recognition coming, utilising a lot of the same infrastructure: think (voice -> transcription -> [other infra]) / (handwriting -> digitization -> [same other infra]).

### catsitter 
[[code]](https://github.com/mgbrian/catsitter/)

A digital nanny using a combination of live vision and back and forth audio communication. The sitter should be able to keep an eye on pets/humans with re-assuring back and forth conversation, while communicating with a remote human care-giver if needed.

### eagle-eye 
[[code]](https://github.com/mgbrian/eagle-eye/)

A surveillance system designed to optimize disk & camera usage and reduce footage review time. The system only records when it detects specified objects/types of activity. It also reduces the wear-and-tear and high disk usage involved in situations that need high fidelity capture by enabling usage of a combination of a cheap always-on camera, and more expensive/higher quality only-triggered-when-necessary camera.

### Minstrel 
[[code]](https://github.com/mgbrian/minstrel/)

A work-buddy that'll shower you with compliments as you work.

### Munchking 
[[code]](https://github.com/mgbrian/munchking/)

A talking shredder who's always excited to compliment and converse with people in sight.

### tutor 
[[code]](https://github.com/mgbrian/tutor/)

This was a stab at building a full-fledged AI assistant all at once (an implementation of this [paper](https://docs.google.com/document/d/1x52awYN3-fEHk6RjW9Ly-ygbaGhkSxwNGIoS8oXNdS8/)), which very quickly became unmanageable. The most important take-away was to build and perfect all the components separately and then integrate them.


