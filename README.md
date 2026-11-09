### Hi, I'm Awab 👋

I study AI at Lusail University in Doha, and I spend most of my time asking language models a slightly rude question: *do you actually know when you're wrong?*

Short answer so far: a little. Their hidden states carry a real signal, but it's small, it depends on the model, and it falls apart on a new dataset. Gemma turned out to be very good at knowing when it's about to refuse, which isn't quite the same thing. Phase 2 is me trying to train that humility in properly.

```python
awab = {
    "based_in":   "Doha, Qatar",
    "studying":   "AI @ Lusail University",
    "currently":  "asking LLMs if they're sure",
    "llm_answer": "yes",  # they were not
    "side_quest": "counting people walking through a door, very seriously",
}
```

#### 🧠 Research

**[Truth Calibration Layer](https://github.com/awabmoha/truth-calibration-layer)**: probes on the hidden states of Qwen2.5-0.5B, Phi-3.5-mini and Gemma 2B, tested on TriviaQA, SQuAD and NQ-Open with 1,500 questions per pairing. The probe beat calibrated confidence in 4 of 6 pairings and roughly matched semantic entropy from a single forward pass. It did not transfer across datasets, which is what Phase 2 is about.

<img src="https://raw.githubusercontent.com/awabmoha/truth-calibration-layer/main/assets/phase1-probe-vs-raw.svg" alt="Phase 1: frozen probe vs calibrated raw confidence (AUROC)" width="640" />

#### 🛠️ Things I've built

- 🚪 **LU SmartCount** *(private)*: counts people walking into a room from a camera feed. RT-DETR + ByteTrack, exported to ONNX and run on a laptop GPU. It never stores video or faces, only "someone came in at 10:42".
- 📍 **Qatar For You** *(private)*: answer four quick questions, get a map of things to do in Qatar. English and Arabic, React Native (Expo).
- 🙂 **[realtime-face-analytics](https://github.com/awabmoha/realtime-face-analytics)**: webcam age, gender and emotion estimation with OpenCV and DeepFace. An old student project, cleaned up.
- 🌐 **[Portfolio](https://awab-ai.vercel.app)**: my CV, but in 3D, because a PDF felt too calm. React + Three.js.

#### 🧰 Stack

**ML:** Python, PyTorch, Hugging Face Transformers, scikit-learn<br>
**Vision:** OpenCV, RT-DETR, ByteTrack, ONNX Runtime<br>
**Apps:** TypeScript, React, React Native (Expo), Three.js

📫 oawab06@gmail.com. Happy to talk calibration, computer vision, or what to do in Qatar.
