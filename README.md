### Hi, I'm Awab 👋

I study AI at Lusail University in Doha, and I spend most of my time asking language models a slightly rude question: *do you actually know when you're wrong?*

Short answer so far: a little. Their hidden states carry a real signal, but it's small, it depends on the model, and it falls apart on a new dataset. Gemma turned out to be very good at knowing when it's about to refuse, which isn't quite the same thing. Then I tried to train that humility in properly, jointly with the model. It didn't help: on a new dataset, every trained head still lost to the model's own token confidence. I wrote that up as a paper anyway, because negative results deserve daylight too.

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

**[Truth Calibration Layer](https://github.com/awabmoha/truth-calibration-layer)**: a preregistered research program on whether language models can learn to estimate how much to trust their own answers. Every test has its rules locked before any result.

- **Phase 1:** probes on the hidden states of Qwen2.5-0.5B, Phi-3.5-mini and Gemma 2B, on TriviaQA, SQuAD and NQ-Open. The probe beat calibrated confidence in 4 of 6 pairings and roughly matched semantic entropy from a single forward pass, but it did not transfer across datasets.
- **Phase 2:** does training the trust head *jointly* with the model fix transfer? Four controlled arms, three seeds, one bug found, one allowed rerun. No: joint training never transferred better than a frozen head, and plain language-model fine-tuning matched its only gain.
  📄 *Joint Training Does Not Make Trust Heads Transfer: A Preregistered Negative Result* (preprint, 2026). DOI: [10.5281/zenodo.24403374](https://doi.org/10.5281/zenodo.24403374)
- **Next:** can a head trained on many datasets beat raw confidence on one it has never seen?

<img src="https://raw.githubusercontent.com/awabmoha/truth-calibration-layer/main/assets/phase2-transfer.svg" alt="Phase 2 and 2b: no trained trust head transfers; raw confidence and semantic entropy beat every arm" width="720" />

#### 🛠️ Things I've built

- 🚪 **LU SmartCount** *(private)*: counts people walking into a room from a camera feed. RT-DETR + ByteTrack, exported to ONNX and run on a laptop GPU. It never stores video or faces, only "someone came in at 10:42".
- 📍 **Qatar For You** *(private)*: answer four quick questions, get a map of things to do in Qatar. English and Arabic, React Native (Expo).
- 🙂 **[realtime-face-analytics](https://github.com/awabmoha/realtime-face-analytics)**: webcam age, gender and emotion estimation with OpenCV and DeepFace. An old student project, cleaned up.
- 🌐 **[Portfolio](https://awab-ai.vercel.app)**: my CV, but in 3D, because a PDF felt too calm. React + Three.js.

#### 🧰 Stack

**ML:** Python, PyTorch, Hugging Face Transformers, scikit-learn, LoRA (PEFT)<br>
**Vision:** OpenCV, RT-DETR, ByteTrack, ONNX Runtime<br>
**Apps:** TypeScript, React, React Native (Expo), Three.js

📫 oawab06@gmail.com · ORCID [0009-0003-3611-9839](https://orcid.org/0009-0003-3611-9839). Happy to talk calibration, computer vision, or what to do in Qatar.
