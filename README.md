### Hi, I'm Awab

I study Artificial Intelligence at Lusail University in Doha. I mostly work on two things: getting language models to say when their answers shouldn't be trusted, and computer vision that runs in real time on ordinary hardware. I also build the apps around them.

#### Research

**[Truth Calibration Layer](https://github.com/awabmoha/truth-calibration-layer)**: can a model estimate how much each of its answers can be trusted? In Phase 1 I trained probes on the hidden states of three open models (Qwen2.5-0.5B, Phi-3.5-mini, Gemma 2B) across TriviaQA, SQuAD and NQ-Open, 1,500 test questions per pairing. The probe beat calibrated raw confidence in 4 of 6 pairings and roughly matched semantic entropy from a single forward pass, but it didn't transfer across datasets. Phase 2 tests whether training the trust head jointly with the model fixes that.

<img src="https://raw.githubusercontent.com/awabmoha/truth-calibration-layer/main/assets/phase1-probe-vs-raw.svg" alt="Phase 1: frozen probe vs calibrated raw confidence (AUROC)" width="640" />

#### Projects

- **LU SmartCount** *(private)*: counts people entering a room from a camera feed. RT-DETR detection and ByteTrack tracking, exported to ONNX and run on a laptop GPU through DirectML. It stores no video and no identities, only entry events.
- **Qatar For You** *(private)*: an Android app for finding activities, events and places in Qatar. Four quick questions give you a personalised map and list, in English and Arabic. React Native (Expo) and TypeScript.
- **[realtime-face-analytics](https://github.com/awabmoha/realtime-face-analytics)**: webcam face detection, age/gender and emotion estimation, and local face matching with OpenCV, DeepFace and SQLite.
- **[Portfolio](https://awab-ai.vercel.app)**: my CV as an interactive 3D site, built with React and Three.js.

#### Stack

- **ML:** Python, PyTorch, Hugging Face Transformers, scikit-learn
- **Vision:** OpenCV, RT-DETR, ByteTrack, ONNX Runtime
- **Apps:** TypeScript, React, React Native (Expo), Three.js

Reach me at oawab06@gmail.com.
