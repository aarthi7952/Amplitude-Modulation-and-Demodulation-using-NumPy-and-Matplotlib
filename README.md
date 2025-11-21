# Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib
## AIM

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. Apparatus Required
Software: Python with NumPy and Matplotlib libraries

## HARDWARE
Personal Computer

## THEORY

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal. The general form of an AM signal is:<img width="290" height="152" alt="image" src="https://github.com/user-attachments/assets/dbe771a4-4857-47ca-a3e3-c9e0559add09" />


## ALGORITHM

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Generate Carrier Signal: Define the carrier signal as a cosine wave.
5.	Modulate Signal: Apply the AM formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## PROGRAM:
```
Ac = 12.2;     
Am = 6.1;      
fc = 5630;   
fm = 563;     
fs = 56300;  
t = 0:1/fs:2/fm; 
m = Am * cos(2 * 3.14 * fm * t);
c = Ac * cos(2 * 3.14 * fc * t);
s = (Ac + m) .* cos(2 * 3.14 * fc * t);
env = abs(hilbert(s));
m_demod = env - mean(env); 
figure;
subplot(4,1,1);
plot(t, m);
xlabel('Time (s)');
ylabel('Amplitude');
title('Message Signal');
subplot(4,1,2);
plot(t, c);
xlabel('Time (s)');
ylabel('Amplitude');
title('Carrier Signal');
subplot(4,1,3);
plot(t, s);
xlabel('Time (s)');
ylabel('Amplitude');
title('AM Modulated Signal');
subplot(4,1,4);
plot(t, m_demod);
xlabel('Time (s)');
ylabel('Amplitude');
title('Demodulated Signal');
```
## TABULATION
![516136056-171ce611-9058-4f0e-87dd-b56a150a7043](https://github.com/user-attachments/assets/a001d6f7-9b4c-4c41-8ae7-15a9c2485c01)

## OUTPUT
<img width="762" height="716" alt="516131445-9ebf79f2-2602-4d0d-9155-05ad36ff2b39" src="https://github.com/user-attachments/assets/dfc39737-d192-45c8-97be-2eecb34a66b8" />

## RESULT
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus AM is implemented using numPy and Matplotlib.

