# AI Tools

## Tools
The following are generic tools without standalone utility, but meant to provide APIs usable in more tailored use-cases.

In aggregate, they can be thought of as a sort of operating system, with brain being the kernel and the rest being peripheral components.

While the peripherals are meant to be used by an AI assistant, they have no explicit connection to one and can be used in any other programmatic system.

### brain [[>>]](https://github.com/mgbrian/brain/)

A suite of cognitive features: sensory (audio and visual) and higher cognition (language processing, reasoning, memory, etc.).

This is designed to mimic a human brain's functions, focusing on how it interacts with the environment i.e. input -> processing -> output

### files [[>>]](https://github.com/mgbrian/files/)

Interact with the (Unix+) filesystem.

### phone [[>>]](https://github.com/mgbrian/phone/)

Send SMS and make/receive live phone calls.

### browser [[>>]](https://github.com/mgbrian/browser/)

Programmatically browse the web like a human (visually, with a real browser).

### transport [[>>]](https://github.com/mgbrian/transport/)

Move data between system components (if `brain` is analogous to a human brain, this is the nervous system). Provides both the infrastructure for communication (sockets, client/server code, etc.) between different components as well as a system for message encoding.

## Apps
Below are applications built (or that could have been built) on top of the above APIs. These apps were built at different stages of the above tools' development, with the express purpose of helping fine-tune and test a component thereof (in addition to their other purpose):

- Munchking helped develop the LLM interfaces, VAD and transcription (`brain`);
- eagle-eye -- object detection and camera capture (`brain`);
- catsitter -- live audio/video input/processing alongside simultaneous user interaction (`brain`), and `phone`;
- tutor - the hard lesson not to try and do this all in one project.
- dev will help develop generic "function-calling" (that works across LLM APIs) and test `files`.
- vector will help develop memory (`brain`).

### vector [[>>]](https://github.com/mgbrian/vector/)
### dev [[>>]](https://github.com/mgbrian/dev/)
### transcriber [[>>]](https://github.com/mgbrian/transcriber/)
### catsitter [[>>]](https://github.com/mgbrian/catsitter/)
### eagle-eye [[>>]](https://github.com/mgbrian/eagle-eye/)
### munchking [[>>]](https://github.com/mgbrian/munchking/)

### tutor [[>>]](https://github.com/mgbrian/tutor/)

This was a stab at building a full-fledged AI assistant, which very quickly became unmanageable.
