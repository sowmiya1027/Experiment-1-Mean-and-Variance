# Experiment-1-Mean-and-Variance
# Aim: 
To find mean and variance of arrival objects from the feeder using probability distribution.

# Software Required: Python and Visual Components tool

# Theory: 

# 1. Mean (Expectation)

The mean or expected value of a discrete random variable represents its average value, weighted by the probabilities of each possible outcome. It indicates the central tendency or typical value of the variable.
It is calculated as:

<img width="306" height="73" alt="image" src="https://github.com/user-attachments/assets/5f2e0454-bf83-40d8-94f5-7f35b0cda25a" />
										
# 2. Variance
The variance of a random variable measures how much the values of the variable vary from the mean. It shows the spread or dispersion of the data.
It is calculated as:
<img width="998" height="184" alt="image" src="https://github.com/user-attachments/assets/4807d369-afba-4736-b3a4-391effa3dcaf" />
# Algorithm: Mean, Variance, and Standard Deviation of Feeder Arrivals
1. Start the program.
   
2. Input the arrival data (list of integers separated by spaces). Example: 0 1 1 2 2 3 3 3.
   
3. Find: N = total number of data values, M = maximum value in the data list.
   
4. Initialize two empty lists: x (for distinct arrival values) and f (for frequency of each arrival value).
 
5. For each value i from 0 to M: count how many times i occurs in the data list, append i to x and its count to f.
   
6.Find total frequency: sf = sum(f).

7. Find probability for each arrival value: p[i] = f[i] / sf.
   
8. Calculate mean (expected value): mean = Σ(x[i] * p[i]).
   
9. Calculate E(X²) (the second moment): EX2 = Σ(x[i]² * p[i]).
    
10. Calculate variance: var = EX2 - (mean)².

11. Calculate standard deviation: SD = √var.

12. Display the Mean, Variance, and Standard Deviation of arrivals.

13. Stop.


# Program: 
Name:Sowmiya R
Reg No: 25013295
Slot Name: 3P1-1

import numpy as np
L=[int(i)for i in input("Enter arrival seperated by space").split()]
N=len(L)
M=max(L)
x=[]
f=[]
for i in range(M+1):
  c=0
  for j in range(N):
    if L[j]==i:
      c+=1
  f.append(c)
  x.append(i)
sf=np.sum(f)
p=[f[i] / sf for i in range(M+1)]
mean=np.inner(x,p)
EX2=np.inner(np.square(x),p)
var=EX2-mean**2
SD=np.sqrt(var)
print(f"The Mean arrival rate is {mean:.3f}")
print(f"The Variance of arrival from feeder is {var:.3f}")
print(f"The Standard deviation of arrival from feeder is {SD:.3f}")


https://colab.research.google.com/drive/1Tyf5bgjFIoBndw1uAR_qThPcYqpacr_F?usp=sharing


# Output:
Enter arrival seperated by space5 5 5 5 6 6 7 8
The Mean arrival rate is 5.875
The Variance of arrival from feeder is 1.109
The Standard deviation of arrival from feeder is 1.053


# Result: 
	The mean and variance of arrivals of objects from feeder using probability distribution are calculated. 



