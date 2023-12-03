# Visual-Microphone


## Theory
When a sound impacts an object, it induces slight vibrations on its surface. Using high-speed video of the object, we demonstrate the removal of these minute vibrations to recover the original sound, essentially transforming everyday objects into visible microphones. By analyzing high-speed images of various objects with different properties, we assess factors influencing sound retrieval quality, evaluating results using Signal-to-Noise Ratio (SNR) metrics.

### Methodology
The input sound, comprising air pressure fluctuations on an object's surface, causes the object to move, creating a temporal pattern captured by a camera. We process the recorded video through an algorithm to detect and extract the output audio. The video input (V(x, y, t), object) involves high-speed video (1kHz-20kHz), assuming object and camera movement is driven by sound-induced vibrations (s(t)).

(b) Our goal is to recover s(t) from V. We follow three steps: dividing the video into small area bands corresponding to different shapes (θ) and scales (r), computing area motion signals, and synthesizing a single ground motion signal for the object. Audio denoising and filtering techniques are applied to motion signals for audio detection.

## Current Working
The project takes video input from Google Drive, processed via the 'v2s' function in Colab. The resulting 'output.wav' is typically played through advanced software like MATLAB due to its high-frequency nature. Spectrograms of the output are generated within Colab.

- Spectrograms:
![image](https://github.com/Haardik-Ravat/Visual-Microphone/assets/77044000/36b6f581-2e48-46a0-a136-699ad76925a4)


### Technologies Used
- Google Colab
- OpenCV
- PyrTools
- NumPy
- Pandas
- SciPy
- Google Drive/mount
- Matplotlib
- MATLAB

### Issues Faced
- **Taking Input:** Initially resolved using PyCharm as an intermediate IDE, later adopting a Google Drive link for input in Google Colab.
- **Steerable Pyramids:** Formation via the OpenCV library accelerated the process.
- **Extracting Sound from Frames:** Employed the Pandas library after the original SciPy approach failed.
- **Global Motion Signal Conversion:** Reordered signal processing after pyramid formation to correct errors.
- **Interference with Denoising:** Distortion in output signal resolved by separate denoising using OpenCV in pyramid execution.

## Concluding Remarks
We've showcased the retrieval of sound-induced vibrations from everyday objects via high-speed videos, converting them into 'visual microphones'. By amalgamating local motion signals, we compute a single motion signal capturing the object's vibrations over time, resulting in recovered audio signals. Objects with light and rigid characteristics excel as visual microphones. Utilizing video cameras for sound-associated vibration restoration opens new research and application possibilities.

### References
[MIT - Visual Microphone](http://people.csail.mit.edu/mrub/VisualMic/)

### Citations
- Davis, Abe, Michael Rubinstein, Neal Wadhwa, Gautham J. Mysore, Frédo Durand, and William T. Freeman. "The visual microphone: passive recovery of sound from video." ACM Transactions on Graphics (TOG) 33, no. 4 (2014): 1-10.
