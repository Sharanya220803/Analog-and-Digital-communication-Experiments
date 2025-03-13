SIMULATION OF FREQUENCY SHIFT KEYING

AIM:
To implement FSK using MATLAB.

SOFTWARE REQUIRED:
MATLAB

PROGRAM:

clc;

clear all;

close all;

t=0:0.0001:0.15;

m=squarewave(2*%pi*10*t);

c1=sin(2*%pi*60*t);

c2=sin(2*%pi*120*t);

s1=(m+c1);

for i=1:1500

if (m(i)==1)

s1(i)=c1(i);

else

s1(i)=c2(i);

end

end

figure(1)

subplot(4,1,1);

plot(m);

xlabel('time');

ylabel('amplitude');

title('bit clock');

suplot(4,1,2);

plot(c1);

xlabel('time');

ylabel('amplitude');

title('carrier low frequency');

subplot(4,1,3);

plot(c2);

xlabel('time');

ylabel('amplitude');

title('carrier high frequency');

subplot(4,1,4);

plot(s1);

xlabel('time');

ylabel('amplitude');

title('fsk modulated ouptut');


OUTPUT:

![Image](https://github.com/user-attachments/assets/5ba3e6d3-21bf-45f8-b1b5-c78f626e1437)

RESULT:
Thus, generation of FSK was implemented using MATLAB.
