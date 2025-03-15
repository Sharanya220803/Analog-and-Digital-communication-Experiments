COMMUNICATION LINK SIMULATION:

AIM:
To implement communication link simulation algorithm using MATLAB

APPARATUS REQUIRED:
MATLAB

PROGRAM:

clc;

clear all; 

close all; 

t-0:0.01:1; 

fc=2;

m=input(enter the message bit');

messagelength=length(m);

time=[];

digitalsignal=[];

psksignal=[];

carriersignal=|];

for i=1:1:messagelength 

carrier=sin(2*pi*fc*t);

carriersignal=[carriersignal carrier];

if m(i)=1

bit=ones(1,length(t));

else 

bit=zeros(1,length(t));

end 

digitalsignal=[digitalsignal bit];

if m(i)=1

psk=sin(2*pi*fc*t+0);

else 

psk=sin(2*pi*fc*t+pi);

end 

psksignal=[psksignal psk];

time=[time t]; 

t=t+1;

end 

ray=sqrt(randn(1,length(t)*messagelength).^2+randn(1,length(t)*messagelength).^2);

psksignalray=psksignal*mod(rand(1,1),1)+ray;

demodmsgsignal=ll;

for i=1:1:messagelength

rx(i)=sum(psksignalray(length(t)*(i-1)+1:length(t)*i).*carrier):

if rx(i)<0

demodmsgsignal=[demodmsgsignal zeros(1,length(t))];

else

demodmsgsignal=[demodmsgsignal ones(1,length(t))];

end 

end

subplot(3,1,1);

plot(time,digitalsignal, 'm');

grid on;

axis ([0 messagelength -0.5 1.5]);

title(DIGITAL SIGNAL');

subplot(3,1,2);

plot(time,carriersignal);

grid on;

title(CARRIER SIGNAL');

subplot(3,1,3);

plot(time,psksignal);

grid on;

title(PSK MODULATED SIGNAL');

figure,

subplot(2,1,1);

plot(time,psksignalray,t');

grid on;

axis([0 messagelength -0.15 1.5]);

title('error removed and demodulated');

OUTPUT:

![Image](https://github.com/user-attachments/assets/03c1becb-e8dc-44c8-9de9-9ab795292e9c)

RESULT:
Thus communication link simulationwas implemented using MATLAB.
