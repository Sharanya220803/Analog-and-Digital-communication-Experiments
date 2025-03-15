SIMULATION OF BINARY PHASE SHIFT KEYING


AIM:
To implement BPSK using MATLAB

APPARATUS REQUIRED:
MATLAB

PROGRAM:

clc;

clear all;

close all;

t=0:0.0001:0.15;

m=square(2*pi*10*t)

c1=sin(2*pi*60*t)

c2=sin((2*pi*60*t)+pi);

s2=(m+c1);

for i=1:1500;

if(m(i)==1);

s2(i)=c1(i);

else

s2(i)=c2(i);

end

end
figure(1);

subplot(4,1,1);

plot(m);

xlabel(‘time’);

ylabel(‘amplitude’);

title(‘data signal’);

subplot(4,1,2);

plot(c1);

xlabel(‘time’);

ylabel(‘amplitude’);

title(‘carrier low signal’);

subplot(4,1,3);

plot(c2);

xlabel(‘time’);

ylabel(‘amplitude’);

title(‘carrier high signal’);

subplot(4,1,4);

plot(s2);

xlabel(‘time’);

ylabel(‘amplitude’);

title(‘psk modulated output’);

OUTPUT:

![Image](https://github.com/user-attachments/assets/99b3ac9e-9beb-49dc-8a8c-cb94fb8f6f80)

RESULT:
Thus,generation of BPSK was implemented using MATLAB
