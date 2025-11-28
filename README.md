Mean-and-Variance
Aim

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

Equipments Needed

1.Computer with i3 Processor

2.SCI LAB

Algorithm

Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function. Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range. Evaluate the Function: Compute the function values at each of these sample points. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values. Display Results: Output the computed mean variance and Cross Correlation. Procedure

Refer Algorithms and write code for the experiment. Open SCILAB in System Type your code in New Editor Save the file Execute the code If any Error, correct it in code and execute again Verify the generated results
output:
Mean

function y = f(x)
    z = 3.7 * (1 - x)^2;
    y = x * z;
endfunction
function y = c(y_input)
    z = 3.7 * (1 - y_input)^2;
    y = y_input * z;
endfunction
a = 0;
b = 1;
EX = intg(a, b, f);
EY = intg(a, b, c);
disp(EX, "i) Mean of X = ");
disp(EY, "Mean of Y = ");
Varaince

function y=g(x)
    z= 3.7*(1-x).^2;
    y=x.^2 .*z;
endfunction
a=0;
b=1;
[EX2, errX2]= intg(a,b,g);
function y=h(yv)
    z= 3.7*(1-yv).^2;
    y=yv.^2 .*z;
endfunction
[EY2, errY2]=intg(a,b,h)
vX2=EX2-EX^2;
vY2=EY2-EY^2;
disp(vX2, "ii)Variance of X=");
disp(vY2, " Variance of Y=");
Cross Correlation

x=input("type in the referance sequence=");
y=input("type in the second sequence=");
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
Calculatiom:
![WhatsApp Image 2025-11-28 at 19 51 03_bc1d12bf](https://github.com/user-attachments/assets/da2e0960-176e-4a71-8198-b34d8e37ff4d)
![WhatsApp Image 2025-11-28 at 19 51 14_a2b7bd78](https://github.com/user-attachments/assets/5edf63c7-0958-4f2a-8881-5779852f6b19)
![WhatsApp Image 2025-11-28 at 19 51 26_c629120c](https://github.com/user-attachments/assets/ea96e059-3218-4f07-9269-96775715373a)

Result:
Result

Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
