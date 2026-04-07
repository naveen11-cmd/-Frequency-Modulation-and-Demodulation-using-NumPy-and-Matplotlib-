# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__
// Parameters
Am = 9.7;        
Fm = 380;         
B  =  4.6;         
Ac = 19.4;          
Fc = 3800;       
Fs = 38000;       
T  = 0:1/Fs:2/Fm; 

// Message signal
em = Am * cos(2*%pi*Fm*T);
subplot(3,1,1);
plot(T, em);
xtitle("Message Signal");
xgrid();

// Carrier signal
ec = Ac * cos(2*%pi*Fc*T);
subplot(3,1,2);
plot(T, ec);
xtitle("Carrier Signal");
xgrid();
// FM signal
efm = Ac * cos( (2*%pi*Fc*T) + (B * sin(2*%pi*Fm*T)) );
subplot(3,1,3);
plot(T, efm);
xtitle("FM Signal");
xgrid();

__Output:__
<img width="630" height="469" alt="image" src="https://github.com/user-attachments/assets/def1fa3b-3e48-4957-9db1-32146123c0f4" />

__Result:__
![WhatsApp Image 2026-04-07 at 12 04 45 PM](https://github.com/user-attachments/assets/63c08569-7135-4f7a-8100-eeae834e56f8)

