# Maitim_PA-2

### Programming Assignment No. 2 :  Numerical Python  ###
This repository includes the solution to different programming problems involving the Numpy or the Numerical Python Library. The assignment includes the making of "Normalization" and "Divisible by 3".

### Number 1 : Normalization problem ###
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process.

In this code, we will print a 5x5 array with random values and its normalized version

```python
#imports the library of numpy to access
import numpy as np

#Inputs random numbers in a 5x5 array
X = np.random.rand(5,5) 

#uses the mean formula to find the mean of the array
Xmean = np.mean(X) 
#calculates for the std of the array
Xstd = np.std(X) 
#formula for the normalized array
X_normalized = (X-Xmean)/Xstd 

#prints the original values of the 5x5 array
print("Your original values are: \n", X) 

#prints the normalized value
print("The normalized value are: \n", X_normalized) 

#saves the array in the format of X_normalized.npy
np.save("X_normalized.npy", X_normalized) 

```
# Output
![image](https://github.com/user-attachments/assets/5b470fa0-6dea-4b82-95fb-e4ddaf87b3c6)

### Number 2 : Division by 3 ###
In this code, it will generate a 10x10 positive integers that are squared. it will then find the elements that are divisible by 3 and will print the numbers that satisfty the condition also.

```python
#imports the library of numpy to access
import numpy as np

#the .arange() function will create a 1x1 array ranging from 1 to 100 in a single row
array_100 = np.arange(1,101) 
#the .reshape() will reshape the array into a 10x10 array
array= array_100.reshape(10,10) 

#the .square() function will square all the values inside the array
x= np.square(array)
#outputs the square of the numbers
print("The square of the numbers 1-100 are : \n", x)

#checks for the numbers in the array if they are divisible by 3
divby3 = x[x%3 == 0]
#outputs the numbers that are divisible by 3
print("The numbers in the array that are divisble by 3 are :\n",divby3) 

#saves the result as div_by_3.npy
np.save("div_by_3.npy", divby3) 
```

# Output
![image](https://github.com/user-attachments/assets/be35e4c8-0dfb-4ac8-a27d-2b7272e760ed)
