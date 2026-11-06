### Hi, I'm Awab

I study Artificial Intelligence at Lusail University in Doha. Most of my time right now goes into one question: can a language model tell you when its own answer shouldn't be trusted?

**[Truth Calibration Layer](https://github.com/awabmoha/truth-calibration-layer)** is where that work lives. In Phase 1 I trained probes on the hidden states of three open models (Qwen2.5-0.5B, Phi-3.5-mini, Gemma 2B) across TriviaQA, SQuAD and NQ-Open, 1,500 test questions per pairing. The probe beat calibrated raw confidence in 4 of 6 pairings and roughly matched semantic entropy from a single forward pass, but it didn't transfer across datasets. Phase 2 tests whether training the trust head jointly with the model fixes that.

<img src="https://raw.githubusercontent.com/awabmoha/truth-calibration-layer/main/assets/phase1-probe-vs-raw.svg" alt="Phase 1: frozen probe vs calibrated raw confidence (AUROC)" width="640" />

Other things I've built:

- **[realtime-face-analytics](https://github.com/awabmoha/realtime-face-analytics)**: webcam face detection, age/gender and emotion estimation, and local face matching with OpenCV, DeepFace and SQLite.
- **[Portfolio](https://awab-ai.vercel.app)**: my CV as an interactive site, built with React and Three.js.

Python, PyTorch, Hugging Face Transformers, scikit-learn, OpenCV, React.

Reach me at oawab06@gmail.com.
