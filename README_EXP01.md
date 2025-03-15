AMPLITUDE SHIFT KEYING

AIM: 
To implement ASK usihg MATLAB

APPARATUD REQUIRED:
MATLAB

PROGRAM:

clc;

t=0:0.0001:0.15;

m=squarewave(2*%pi*10*t);

c=sin(2*%pi*60*t);

y1=(m.*c);

for  i = 1:1500

if(m(i)==1)

y1(i)=c(i);

else

y1(i)=0;

end

end

figure(1)

subplot(3,1,1);

plot(m);

subplot(3,1,2);

plot(c);

subplot(3,1,3);

plot(y1);

OUPTUT:

![Image](https://github.com/user-attachments/assets/a7df3075-c022-4e07-874a-cd2ba4a64789)


RESULT:
Thus, the generation of ASK was implemented using MATLAB.
