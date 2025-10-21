# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```
import numpy as np
a=np.array(eval(input()))
m,n=a.shape
q=np.zeros((m,n))
r=np.zeros((n,n))
for k in range(n):
    q[:,k]=a[:,k]
    for i in range(k):
        r[i,k]=np.dot(q[:,i],a[:,k])
        q[:,k]-=r[i,k]*q[:,i]
    r[k,k]=np.linalg.norm(q[:,k])
    q[:,k]/=r[k,k]
print("The Q Matrix is \n",q)
print("The R Matrix is \n",r)







```

## Output
```
<img width="1190" height="573" alt="image" src="https://github.com/user-attachments/assets/eb13cf3c-27e5-46df-bce9-10e247806846" />


```

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
