## 29.06.2026
### Tasks Completed:

- Brainstormed implementation strategies and workflows for a conversational AI-driven onboarding experience.
- Tested the Sarvam.ai conversational AI capabilities locally to assess latency, voice/text quality, and API integration requirements.

### Key Learnings:

- Designing a conversational AI onboarding system requires careful dialogue structuring to accurately extract user profiles without causing conversational friction.
- Local testing of Sarvam.ai provides critical baseline metrics on performance and response latency, which are key for building a responsive user experience.

## 30.06.2026
### Tasks Completed:

- Built and tested a functional prototype utilizing Sarvam.ai's Speech-to-Text (STT) and Text-to-Speech (TTS) API endpoints.
- Evaluated voice transcription accuracy and synthesized voice output quality to ensure human-like responsiveness and low latency.

### Key Learnings:

- Developing functional prototypes of STT and TTS services early helps validate integration limits, network delays, and transcription error handling.
- Balancing response speed with transcription/synthesis clarity is vital for establishing a natural and seamless voice interaction loop.

## 01.07.2026
### Tasks Completed:

- Presented the final build of the conversational AI onboarding system using Sarvam.ai.
- Configured and integrated Sarvam's STT/TTS services within LiveKit Cloud, paired with Gemini LLM to establish a fully streaming End-to-End (E2E) conversational pipeline.
- Implemented a structured 6-step E2E conversational flow:
  - **STEP 1: Speech Input**: Captures voice input after Sarvam AI speaks the greeting chunk and initial question.
  - **STEP 2: Voice Activity Detection (VAD)**: Configured WebRTC VAD to track speech start and handle AI interruptions, and Silero VAD to detect when the user has finished speaking (with a fallback manual stop button).
  - **STEP 3: STT**: Streamed audio transcription via the LiveKit Sarvam plugin.
  - **STEP 4: LLM**: Processed text transcripts and generated context-aware responses using Gemini.
  - **STEP 5: TTS**: Synthesized the textual response into audio via LiveKit Sarvam.
  - **STEP 6: Speech Output**: Delivered synthesized audio back to the user.

### Key Learnings:

- Utilizing LiveKit Cloud to orchestrate custom plugins (Sarvam.ai for STT/TTS and Gemini for LLM processing) provides a robust, low-latency framework for real-time voice streaming.
- Combining WebRTC VAD for fast interruption handling and Silero VAD for speech termination detection results in a natural voice interface, though manual fallback overrides are still essential for noisy environments.

## 02.07.2026
### Tasks Completed:

- Deployed and validated four independent Redis instances configured specifically for microservice integration.
- Secured all instances using strong cryptographic authentication and configured binding settings to permit secure external connections.
- Set up and configured persistent, systemd-managed deployments for each instance to ensure reliable process lifecycle control and automatic restarts.

### Key Learnings:

- Running isolated Redis instances per microservice prevents cross-service data pollution and limits the operational impact in the event of cache failure.
- Implementing robust cryptographic authentication combined with bind restrictions is essential for securing Redis instances exposed within internal virtual private networks.
- Leveraging systemd for Redis service units provides standardized process management, reliable crash recovery, and centralized logging.
