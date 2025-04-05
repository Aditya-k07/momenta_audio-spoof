#  Audio Deepfake Detection: Selected Approaches

The analysis is done from the repo : [Audio-Deepfake-Detection](https://github.com/media-sec-lab/Audio-Deepfake-Detection) .


###  **TASK 1 :- **

 Model is to be selected on the basis of :

- Effectiveness in detecting **AI-generated human speech**
- **Real-time or near real-time** deployment potential
- Applicability to **natural conversations** in uncontrolled environments



##  1. AASIST (Audio Anti-Spoofing with Spectro-Temporal Graph Attention Networks) 

- **Key Technical Innovation**  
  Utilizes graph attention networks over spectro-temporal feature maps from spectrograms, allowing effective modeling of both local and global spoofing cues.

- **Reported Performance Metrics**  
  - Equal Error Rate (EER): **0.83%**
  - t-DCF: **0.028** (Logical Access scenario)

- **Why It’s Promising**  
  - Robust to various spoofing techniques  
  - Good generalization with efficient architecture  
  - Suitable for near real-time inference

- **Limitations**  
  - May need tuning for conversational speech in wild settings  
  - Slightly complex model for lightweight edge deployment



---

##  2. Attention + Joint Optimization (AAM + Meta-Learning)
  
- **Key Technical Innovation**  
  Combines simple attention with joint optimization using Additive Angular Margin loss and meta-learning to improve discriminative embeddings.

- **Reported Performance Metrics**  
  - EER: **0.99%**
  - t-DCF: **0.029**

- **Why It’s Promising**  
  - Lightweight and modular  
  - Easy to integrate with other systems  
  - Meta-learning allows fast adaptation to new spoofing types

- **Limitations**  
  - Less effective on long temporal dependencies  
  - Needs fine-tuning for domain-specific data



---

##  3. RawNet2 (End-to-End Raw Waveform Anti-Spoofing)


- **Key Technical Innovation**  
  Processes raw audio directly using deep residual learning without spectrograms, enabling true end-to-end spoofing detection.

- **Reported Performance Metrics**  
  - EER: **1.12%**
  - t-DCF: **0.033**

- **Why It’s Promising**  
  - Eliminates preprocessing, ideal for pipeline simplification  
  - Suitable for real-world conversational speech  
  - Can be optimized for streaming inputs

- **Limitations**  
  - Slightly higher error rate than AASIST  
  - Higher computational load with raw waveform input



---


