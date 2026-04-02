# Digital-Signal-Processing--FIR-BAND-PASS-FILTER-DESIGN
## AIM:
To generate design of Band Pass FIR digital filter using Hanning Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
~~~
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1=');
Wc2=input('enter the value of Wc2=');
N=input('enter the value of M=');
alpha=(N-1)/2;
eps=0.001;
%Band Pass Filter Coefficient
n=0:1:N-1;
hd=(sin(Wc1*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)
%Hanning Window Sequence
n=0:1:N-1;
wh=0.5-0.5*cos((2*pi*n)/(N-1))
hn=hd.*wh
% Plot the Band Pass Filter with Hanning window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue')
title('Band Pass FIR Filter using Hanning Window')
~~~~

## OUTPUT:
BAND PASS FIR FILTER USING HANNING WINDOW 

![WhatsApp Image 2026-03-30 at 14 58 24](https://github.com/user-attachments/assets/8e84182f-0095-43fb-bd36-6bfac47f7367)


## RESULT:

![WhatsApp Image 2026-04-02 at 15 52 58](https://github.com/user-attachments/assets/6f753ed9-f3a4-465e-b4bf-2424e69df44d)

