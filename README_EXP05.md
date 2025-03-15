ERROR CONTROL CODING SCHEMES

AIM:
To implement error control coding schemes with linear block codes using MATLAB

APPARATUS REQUIRED:
MATLAB

PROGRAM:

ENCODING:

clc;

close all;

n=7;

k=4;

msg=[1 0 0 1;1 0 1 0;1 0 1 1];

code=encode(msg,n,k,'cyclic');

msg

code

OUTPUT:

![Image](https://github.com/user-attachments/assets/0161178c-bc97-4be4-9bbf-bbdb32f71bd1)

DECODING PROGRAM:

clc;

clear all;

close all;

q=3;

n=2^q-1;

k=n-q;

parmat=hammgen(q);

trt=syndtable(parmat);

recd=[1 0 1 1 1 1 0];

syndrome=rem(recd*parmat',2);

syndrome_de=bi2de(syndrome,'left-msb');

disp(['syndrome=',num2str(syndrome_de),'(decimal)','num2str(syndrome)','(binary)']);

corrvect=trt(1+syndrome_de);

correctedcode=rem(correct+recd,2);

parmat

corrvect

correctedcode

OUTPUT:

![Image](https://github.com/user-attachments/assets/3a290009-b123-48dd-9666-ab532182b476)

RESLUT:
Thus encoding and decoding of block codes are performed using MATLAB.
