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
while(length(p)>2)
tempsum=p(length(p)) +p(length(p)-1);
sumarray=[sumarray,tempsum];
P=[P(1:length(p)-2),tempsum];
p=sort(p,'descend');
=i+1:
49
b(i,:)=[p,zeros(1,w-length(p))];
wl=0;
lengthp=[lengthp,length(p)];
for temp=1:length(p) if p(temp) —tempsum; wl-temp;
end end
tempfinal=[wl,tempfinal]; % Find the place where tempsum has been inserted
display(p);
end
sizeb(1:2)=size(b);
tempdisplay=0; temp2=0;
* i= I:sizeb(
np2=[temp2,b(1,
end sumarray=[0,sumarray];
var-11; e=1;
foodi sinie (2)
