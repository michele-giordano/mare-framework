# MARE: Modular Asynchronous Role-based Ecosystem
![Open Source](https://img.shields.io/badge/Open%20Source-green)
![License](https://img.shields.io/badge/License-MIT-green)
![Modular Asynchronous](https://img.shields.io/badge/Modular-Asynchronous-blue)
![Role-based Ecosystem](https://img.shields.io/badge/Role%20Based-Ecosystem-blue)
![Generative AI](https://img.shields.io/badge/Generative-AI-red)
![LLM TTS](https://img.shields.io/badge/LLM-TTS-orange)

A framework to orchestrate complex multimodal and generative pipelines through clearly defined, modular, asynchronous, specialized roles.

---

## About

MARE is an architectural framework designed to manage distributed AI pipelines that integrate multiple modalities (such as text, speech, and 3D visualization) and generative AI components. 
It provides a modular and asynchronous ecosystem where each role focuses on a specific responsibility, enabling scalable, maintainable, and adaptable systems.

MARE is the formal evolution of **RAEF** (Role-Based Asynchronous Extensible Framework), an architecture originally conceived and implemented for the author's software engineering thesis project.

---

## Architecture Overview

MARE structures the system into four logical departments:

1. **PRODUCTION**
   - Generates and refines the core textual content.
   - Typical roles:
     - Writer: primary language model (e.g. Gemma3n).
     - Reviewer: consistency or style enforcement.

2. **DUBBING**
   - Converts text into audio and synchrony metadata.
   - Typical roles:
     - Dubbler: TTS engine (e.g. VerbaManent).
     - Dubbing Reviewer: post-processes voice or intonation.
     - Phoneme & Viseme Generator: prepares data for lipsync.

3. **ENACTMENT**
   - Executes the enactment of the final multimodal output through two specialized roles:
     - **Choreographer**: aggregates and synchronizes all data streams — textual content, audio files, and animation directives, including lip-sync data, facial expressions, gestures, and overall body choreography within the spatial context — ensuring they are properly sequenced and harmonized before passing them on.
     - **Protagonist**: receives the synchronized directives from the Choreographer and performs the enactment, aligning lip movements and gestures with the audio, displaying the text, and ultimately becoming the visible and audible embodiment of the system's response.

4. **TRANSPORT**
   - Handles communication, encryption, handshakes, and asynchronous data flow.
   - Typical roles:
     - Bureaucrat: authentication and secure setup.
     - Couriers: manage the Client-Server and Server-Server message transfers.

Each department is composed of specialized roles that interact asynchronously, ensuring modularity and fault tolerance.


---

## Key features

MARE is an innovative architecture designed to facilitate rich multimodal representation, particularly when combined with generative AI models. Its main application [**MGVT**](https://github.com/michele-giordano/mgvt) (Multimodal Generative Virtual Teacher), demonstrates this by integrating text, speech, and 3D visualization into a coherent, interactive system.

Here are the key features:

- **Modular, asynchronous and role-based:** every step of the pipeline is represented by virtual roles, organized into the four main departments (Production, Dubbing, Enactment, Transport). Each department and role can be implemented modularly client-side, server-side, or in any combination, ensuring maximum flexibility and adaptability.

- **Multimodal and generative:** integrates generative AI, Text-to-Speech (TTS), phoneme and viseme synchronization, and 3D avatar staging into an organized pipeline, supporting natural spoken interaction and rich non-verbal communication.

- **Local and privacy-first:** all information, including user questions, answers, and any related content, from language generation to speech synthesis and animation, runs privately and encrypted on local hardware, with no data leaving the user's machine.

- **Cloud-free and subscription-free:** the system is fully customizable, expandable and open-source, requiring no external services or ongoing payments. This setup ensures full ownership, long-term sustainability, and deployability even in resource-constrained environments.

- **Accessibility-focused:** designed with voice input as the primary mode of interaction, while remaining fully compatible with any assistive input device needed by the user, it presents the content through multiple modalities, such as text, audio, and synchronized facial and body movements. This facilitates the learning process for users with or without sensory or motor impairments.

- **Open-source and ethical:** released under the MIT license to encourage adoption by educators and non-profits, rejecting surveillance-based or locked-in business models. 

This positions MARE as a flexible foundation for building local, human-centered AI systems that leverage generative, multimodal, and privacy-respecting technologies.


---

## Basic Example

A minimal example is provided in [`examples/MARE_basic_pipeline_demo.py`](examples/MARE_basic_pipeline_demo.py).  
This illustrates how to instantiate a simple pipeline where a Writer produces text and a Dubbler processes it, demonstrating MARE's asynchronous orchestration.


---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


---

## Citation & Contact

If you use or adapt this framework in your research or applications, please cite:

Michele Giordano, "MARE Framework (Modular Asynchronous Role-based Ecosystem)", 2025.

For collaborations, advanced implementations or consulting inquiries:
giordano.michele@gmail.com
