## Part 3: Documentation & Analysis

### 1. Implementation Notes

**Challenges:**
- Variable input sizes for spectrograms
- Risk of overfitting due to small dataset
- Background noise in some audio files

**Solutions:**
- Used `AdaptiveAvgPool2d` for fixed output size
- Normalized spectrograms with decibel scaling

**Assumptions:**
- Real and fake voices show different spectrogram patterns
- `.wav` files are loadable and clean enough for analysis

---

### 2. Model Analysis

**Why CNN?**
- CNNs handle spectrograms well as image-like data
- Simple 3-layer CNN gives good performance and is easy to interpret

**How It Works:**
- Audio → Mel Spectrogram → CNN layers → Adaptive pooling → Dense → Output (Real/Fake)

**Results:**
- 100 % accuracy due to overfitting
- Balanced precision and recall for both classes

**Strengths:**
- Performs well even with some background noise
- Easy to train and deploy

**Weaknesses:**
- Less effective on noisy or low-quality recordings
- Doesn’t capture linguistic or emotional features

**Future Improvements:**
- Add more diverse data & noise augmentation
- Try transfer learning with wav2vec or VGGish
- Explore hybrid CNN + LSTM architectures

---

### 3. Reflection

1. Biggest challenge: handling input size variability.
2. Real-world performance may drop due to uncontrolled noise.
3. For specific tye of spoof noise you have to train according to it.

### 3. Datasets

1. For training and validation : https://www.kaggle.com/datasets/kambingbersayaphitam/speech-dataset-of-human-and-ai-generated-voices
2. For testing :  https://www.kaggle.com/datasets/hejuncheung/songs-data
