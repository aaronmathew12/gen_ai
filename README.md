#  AI Music Generation System (RNN + MusicGen)

This project is a hybrid AI-based music generation system that combines a custom Recurrent Neural Network (RNN) with music theory rules and a pretrained Hugging Face model (MusicGen) to generate realistic, mood-based music.

---

##  Features

- RNN-based music generation from MIDI data
- Mood-based control: Happy, Sad, Energetic
- Music theory improvements:
  - Scale snapping (major/minor)
  - Smooth melody transitions
  - Rhythm consistency
  - Chord generation (harmony)
- Pattern memory to reduce randomness
- MIDI to audio conversion using FluidSynth
- Integration with Hugging Face MusicGen
- Comparison between RNN output and MusicGen output

---

##  How It Works

1. MIDI files are converted into note features:
   - Pitch
   - Step (time gap)
   - Duration

2. The RNN is trained on sequences of notes:
   - Input: previous notes
   - Output: next note

3. Music is generated step-by-step:
   - Predict → append → repeat

4. Mood engine modifies the generated notes:
   - Happy → higher pitch, faster
   - Sad → lower pitch, slower
   - Energetic → dynamic rhythm

5. Music theory rules improve quality:
   - Keeps notes in scale
   - Avoids large jumps
   - Adds chords

6. Output is converted:
   - Notes → MIDI → WAV (audio)

7. MusicGen generates high-quality audio for comparison.

---

##  Architecture

MIDI Dataset  
↓  
Feature Extraction (Pitch, Step, Duration)  
↓  
Sequence Creation  
↓  
RNN Model  
↓  
Generated Notes  
↓  
Mood Engine + Music Theory  
↓  
MIDI → Audio (FluidSynth)  
↓  
MusicGen (Hugging Face)  
↓  
Final Audio Output  

---

## 🛠️ Tech Stack

- Python
- TensorFlow (RNN)
- PrettyMIDI
- NumPy, SciPy
- FluidSynth
- Hugging Face Transformers (MusicGen)
- PyTorch

---

##  Installation

1. Clone the repository:

   git clone https://github.com/aaronmathew12/gen_ai  
   cd music-generator  

2. Create virtual environment:

   python -m venv venv  
   venv\Scripts\activate   (Windows)  
   source venv/bin/activate (Mac/Linux)  

3. Install dependencies:

   pip install tensorflow pretty_midi numpy scipy transformers torch  

4. Install FluidSynth:
   Download from https://www.fluidsynth.org/ and add it to system PATH.

---

##  Usage

Run the project:

   python main.py  

Then enter:

   happy / sad / energetic  

---

##  Output

- RNN-generated music (structured)
- MusicGen-generated music (realistic)
- Both outputs can be compared

---

##  Key Concepts

- Recurrent Neural Networks (RNN)
- Sequence modeling
- Autoregressive generation
- Music theory integration
- Hybrid AI systems

---

##  Limitations

- RNN output may still be less complex than real music
- Single instrument (piano only)
- Requires tuning for better results

---

##  Future Improvements

- Add drum beats
- Multi-instrument support
- Use Transformer models (LSTM/Attention)
- Build web UI (Streamlit)
- Real-time music generation

---

##  Demo Explanation

“We built a hybrid AI system that combines RNN-based sequence learning with music theory constraints and pretrained transformer models to generate realistic and mood-based music.”

---

