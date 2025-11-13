# AM-using-Python

## Aim


To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. The general form of an FM signal is:



## Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program
```
import numpy as np
import matplotlib.pyplot as plt
AM=5.1
fm=353
fs=35300
AC=10.2
fc=3530
t=np.arange(0,2/fm,1/fs)
m=AM*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=AC*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s =(AC + m)*np.cos(2*3.14*fc*t)# Define s as the sum of m and c
plt.subplot(3,1,3)
plt.plot(t,s)
plt.tight_layout()
plt.show()


```

## Output Waveform
![WhatsApp Image 2025-09-11 at 08 58 32_f0be449e](https://github.com/user-attachments/assets/57a6c38e-b41d-4a49-b162-30799819e94d)





## Tabular Column
![WhatsApp Image 2025-11-13 at 09 27 41_d4a8c900](https://github.com/user-attachments/assets/eafbc45b-a9e4-4761-95e1-6506492f7696)




## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
