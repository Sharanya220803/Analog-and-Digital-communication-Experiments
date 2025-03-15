HUFFMAN CODING

AIM:
To implement Huffman coding schemes using MATLAB

APPARATUS REQUIRED:
MATLAB

PROGRAM:

clc;

clear all;

s=input('Enter symbols-') %format ['a', b','c', d','e', f];

p=input('Enter value of probabilty-') %format [0.22,0.20,0.18,0.15,0.13,0.12];

if length(s) ~=length(p)

error('Wrong entry.. enter again-)
  
end

i=1;

for m=1:length(p)

for n=1: length(p)
  
if(p(m)>p(n))
    
a=p(n); al=s(n);

p(n)=p(m);s(n)=s(m);|

p(m)=a; s(m)=al;

end
    
end
  
end

display(p) %arranged prob. in descending order. 

tempfinal=[0]; 

sumarray=[];

w=length(p);

lengthp=[w];

b(i,:)=p;

while(length(p)>2)

tempsum=p(length(p))+p(length(p)-1);

sumarray=[sumarray,tempsum];

p=[p(1:length(p)-2),tempsum];

p=sort(p,'descend');

i=i+1:

b(i,:)=[p,zeros(1,w-length(p))];

wl=0;

lengthp=[lengthp,length(p)];

for temp=1:length(p) 

if p(temp) —tempsum; wl-temp;
  
w1=temp;
   
end 

end

tempfinal=[wl,tempfinal]; % Find the place where tempsum has been inserted

display(p);

end

sizeb(1:2)=size(b);

tempdisplay=0; 

temp2=[];

for i=1:sizeb(2);

temp2=[temp2,b(1,i)];

end

sumarray=[0,sumarray];

var=[];

e=1;

for ifinal= 1:sizeb(2);

code=[s(ifinal),'   ']
 
for j=1:sizeb(1)

tempdisplay=0;

for i1=1:sizeb(2)

if( b(j,il)==temp2(e))

tempdisplay=b(j.il);

end

if(tempdisplay==0 & b(j,il)==sumarray(j))

tempdisplay=b(j,il);

end
 
end

var=[var,tempdisplay];

if tempdisplay==b(j,length(j))   %assign 0 & 1

code=[code,'1'];

elseif tempdisplaly==b(j,lengthp(j)-1)

code=[code,'0']

else

code=[code,"];

end

temp2(e)=tempdisplay;

end

display(code) %display final codeword

e=e+1;

end

OUTPUT:

![Image](https://github.com/user-attachments/assets/e83f3be9-1f7b-40a8-9f8b-62f9382f49a9)

RESULT:
Thus Huffman coding are performed using MATLAB.
