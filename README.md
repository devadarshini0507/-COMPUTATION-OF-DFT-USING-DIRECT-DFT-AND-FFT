
# EXP 2 : COMPUTATION OF DFT USING DIRECT DFT AND FFT

# AIM: 

To obtain DFT and FFT of a given sequence in SCILAB. 


# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
# DISCRETE FOURIER TRANSFORM 
```
clc;
clear;
xn=[1 2 3 1 1 2 0 0];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
      for k=0:N-1
          for n=0:N-1
              Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
      end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle=atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('phase');
title('Phase spectrum');
```
# Fast Fourier Transform
```
clc;
clear;
close;
xn=[1 2 3 1 1 2 0 0];
n1=0:1:length(xn)-1;
subplot(2,2,1);
plot2d3(n1,xn);
xlabel('time n');
ylabel('amplitude');
title('input sequence');
xk=fft(xn);
k1=0:1:length(xk)-1;
magnitude=abs(xk)
subplot(2,2,2);
plot2d3(k1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');

angle=atan(imag(xk),real(xk));
subplot(2,2,3);
plot2d3(k1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('phase spectrum');
y=ifft(xk);
n2=0:1:length(y)-1;
subplot(2,2,4);
plot2d3(n2,y);
xlabel('time n');
ylabel('amplitude');
title('inverse FFT of x(k)');
```

# CALCULATIONS: 
# DISCRETE FOURIER TRANSFORM 
<img width="1600" height="1532" alt="image" src="https://github.com/user-attachments/assets/b271b35d-c4a5-40bf-9867-76f07bee7ea1" />
<img width="1538" height="695" alt="image" src="https://github.com/user-attachments/assets/7dc2d282-915a-4055-ac3a-5a9a00a689ec" />

# Fast Fourier Transform
<img width="1531" height="788" alt="image" src="https://github.com/user-attachments/assets/a098f10c-2dd9-4d15-954d-7ce8a5fcd74f" />
<img width="1015" height="1542" alt="image" src="https://github.com/user-attachments/assets/390fc28b-a0cb-4418-8a1e-2e9caed6c40d" />



# SAMPLE OUTPUT: 
# DISCRETE FOURIER TRANSFORM 
<img width="1323" height="1080" alt="image" src="https://github.com/user-attachments/assets/5078cfff-25ba-4d49-afb1-32d5094e7a03" />


# Fast Fourier Transform
<img width="1600" height="1250" alt="image" src="https://github.com/user-attachments/assets/ab4e13ab-8ddd-4498-a1f5-0642b40e1b70" />


# RESULT: 

Thus, the Discrete Fourier Transform (DFT) and Fast Fourier Transform (FFT) of the given input sequence were successfully computed using SCILAB.
