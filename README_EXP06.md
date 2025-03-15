SHANNON FANO CODING

AIM:
To implement Shannon fano coding schemes using MATLAB

APPARATUS REQUIRED:
MATLAB

PROGRAM:

clc;

clear all; 

close all;

m= input(Enter the no. of message ensembles: ");

z=[];

h=0;

l=0;

display('Enter the probabilities in descending order');

for i=l:m

  fprintf('Ensemble %d\n',i);
  
  p(i)-input(");
  
end

%Finding each alpha values 

a(1)=0;

for j=2:m;

  a(j)=a(j-l)+p(j-l);

end

fprintf('\n Alpha Matrix');

display(a);

%Finding each code length 

for i=1:m

  n(i)= ceil(-1*(log2(p(i))));
  
end

fprintf('\n Code length matrix');

display(n);

%Computing each code 

for i=l:m 

  int=a(i);

for j=1:n(i)

  frac=int*2; 
  
  c=floor(frac);

  frac=frac-c:
  
  z=[z c];
  
  int=frac;
  
end

fprintf('Codeword %d',i);

display(z);

z=[];

end

%Computing Avg. Code Length & Entropy

fprintf('Avg. Code Length');

for i=l:m

  x=p(i)*n(i);

  l=l+x;
  
  x=p(i)*log2(1/p(i));
  
  h=h+x;
  
end

display(l);

fprintf('Entropy');

display(h);

%Computing Efficiency

fprintf('Efficiency');

display(100*h/l);

fprintf(Redundancy');

display(100-(100*h/l));

OUTPUT:

![Image](https://github.com/user-attachments/assets/3d753c4b-3633-4a89-813f-ef68751f725a)

RESULT:
Thus, Shannon fano coding are performed using MATLAB.
