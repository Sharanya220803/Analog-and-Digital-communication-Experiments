SIMULATION OF QUADRATURE PHASE SHIFT KEYING

AIM:
To implement the generation of QPSK using MATLAB

APPARATUS REQUIRED:
MATLAB

PROGRAM:

clc;

clear all;

close all;

Tb=1;

t=0:(Tb/100):Tb;

fc=1;

c1=sqrt(2/Tb)*cos(2*pi*c*t);

c2=sqrt(2/tb)*cos(2*pi*fc*t);

N=8;

m=rand(1,N);

t1=0;

t2=Tb;

for i=1:2:(N-1)

t=[t1:(Tb/100):t2];

if m(i)>0.5

m_s=ones(1,length(t));

else

m(i)=0;

m_s=-1*ones(1,length(t));

end

odd_sig(i,:)=c1.*m_s;

if m(i+1)>0.5 m(i+1)=1;

m_s=ones(1,length(t));

else

m(i+1)=0;

m_s=-1*ones(1,length(t));

end

even_sig(i,:)=c2.*m_s;

qpsk=odd_sig+even_sig;

subplot(3,2,4);

plot(t,qpsk(i,:));

title('qpsk signal');

xlabel('t--->');

ylabel('s(t)');

grid on;

hold on;

t1=t1+(Tb+.01);t2=t2+(Tb+.01);

end

hold off

subplot(3,2,1);

stem(m);

title('binary data bits');

xlabel('n--->');

ylabel('b(n)');

grid on;

subplot(3,2,2);

plot(t,c1);

title('carrier signal-1');

xlabel('t--->');

ylabel('c1');

grid on;

subplot(3,2,3);

plot(t,c2);

title('carrier signal-2');

xlabel('t--->');

ylabel('c2');

grid on;

OUTPUT:

![Image](https://github.com/user-attachments/assets/8105af69-33da-4ff3-910d-2f44cd3fda87)

RESULT:
Thus, generation of QPSK was implemented using MATLAB
