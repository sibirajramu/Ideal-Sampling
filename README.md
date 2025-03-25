## **IDEAL SAMPLING**

## **AIM:**

To perform Construction and Re-Construction of impulse or ideal sampling using python

## **APPARATUS REQUIRED:**

Python IDE with Numpy and Scipy

## **CODE:**

import numpy as np 
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()

## **OUTPUT:**

![ideal sampling 1](https://github.com/user-attachments/assets/601cf20a-75f3-4149-873e-90f9ee08e4f2)
![ideal sampling 2](https://github.com/user-attachments/assets/45344ff9-4877-4bfa-8abb-1109a86900c8)
![ideal sampling 3](https://github.com/user-attachments/assets/995c1f15-d04c-411e-8cae-bb98b5e359bd)

## **RESULT:**

The Construction or Re-Construction of impulse or ideal sampling using python are verified
