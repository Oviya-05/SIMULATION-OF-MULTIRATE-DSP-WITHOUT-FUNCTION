# EXP 6 : SPEECH RECOGNITION USING SCILAB
## Oviya K P (212223060191)
### AIM: 
To perform and verify multirate DSP without function using SCILAB. 

### APPARATUS REQUIRED: 
PC installed with SCILAB. 

### PROGRAM : 
```
clear; 
clc; 
close; 
n = 0:%pi/50:2*%pi; 
x = sin(%pi*n); //original signal 
M=input('Enter the downsampling factor'); 
L=input('Enter the upsampling factor'); 
//Down Sampling 
downsampling_x = x(1:M:length(x)); 
disp(x,'Input signal x(n)='); 
disp(downsampling_x,'Downsampled Signal'); 
figure(1); 
subplot(2,1,1) 
plot2d3(1:length(x),x); 
xtitle('original singal') 
subplot(2,1,2) 
plot2d3(1:length(downsampling_x),downsampling_x); 
xtitle('Downsampled Signal by a factor of M'); 
//Upsampling 
upsampling_x=[]; 
for i=1:length(x) 
upsampling_x(1,L*i)=x(i); 
end 
disp(x,'Input signal x(n)='); 
disp(upsampling_x,'Upsampled Signal');
figure(2); 
subplot(2,1,1); 
plot2d3(x); 
title('original signal'); 
subplot(2,1,2); 
plot2d3(upsampling_x); 
title('Upsampled Signal by a factor of L');
```
### OUTPUT: 

<img width="978" height="288" alt="image" src="https://github.com/user-attachments/assets/fbf08bbb-81a5-47d8-9cf1-12e8e8425049" />


<img width="1618" height="859" alt="image" src="https://github.com/user-attachments/assets/7bbe1afb-eaaa-478f-a653-b3e17338729c" />


<img width="1623" height="853" alt="image" src="https://github.com/user-attachments/assets/9843de8c-6df5-4cb6-9124-d6cb682550b4" />



### RESULT: 
Thus the decimation process by a factor M and interpolation process by a factor L using 
SCILAB was implemented. 
