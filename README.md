# Hybrid_AI-ML_noise_cancellation_for_defence
The real-time Active Noise Cancellation (ANC) pipeline deploys a compact Temporal Convolutional Network (TCN) on a Raspberry Pi 5 using dual USB audio devices.

**First Stage**
 - Data Collection
    we collect data over 23480 raw audio file of cear speech and noisy audio file in .wav format each.
    The noisy audio contain-
    Stationary-
    - Vehical noise
    - Motor noise
    - Engine noise
    - Foot steps
    - Environment noise

    Non-SStationary-
    - Siren
    - Explosion

    Impulsive-
    - Gun fire
    - Sudden sound (like - drop, crack, etc)

 - Data mixing
   mixing a data of noisy audio with clean speech and make a two audio file, One of clean speech and another for noisy + clean peech.

**Second Stage**
 - this is model building stage for which we use a TCN (Temporal Convolutional Network) to train our data over approx 50,000 audio file.

<img width="2390" height="1426" alt="Screenshot 2026-10-03 022815" src="https://github.com/user-attachments/assets/76bd5076-b160-4afd-b5fa-177c2b5b3be4" />

 - This is how our model work on different noise type -
<img width="2877" height="1622" alt="Screenshot 2026-09-30 040759" src="https://github.com/user-attachments/assets/14e1deb4-7cad-4566-b349-380595640f32" />


**Third Stage**
 - After training the model we quannitized a model in .onnx format and convert into a INT8. After that we deployed the model in Raspberry pi 5 4gb.
 - We convert audio into chunks and process through the model inn real time with < 40dB  latency.
 - And connect with microphone, speaker and power supply 20W.
 - our prototype is ready to work in realtime Audio Noise Cancellation.

<img width="2756" height="1402" alt="Screenshot 2026-09-30 040836" src="https://github.com/user-attachments/assets/fa927103-00ae-4746-bbf5-170ec0acb057" />





   
