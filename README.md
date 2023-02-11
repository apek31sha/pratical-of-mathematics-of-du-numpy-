# pratical-of-mathematics-of-du using numpy,sympy
import numpy as np

# question 1
#transpose of matrix and conjugate's transpose

p = np.matrix([[1,2,9,3],[1,3,4,4],[3,45,56,9]])
t=p.transpose()
print(t)
p = np.matrix([[1,2,9j,-1j],[1,3,4,4],[3,45j,56,-9]])
z=np.conjugate(p)
x=z.transpose()
print(x)


#question2
#rank of matrix using sympy
import sympy 
m=sympy.Matrix([[1,2,33,4],[1,2,34,5],[5,6,78,8],[1,2,34,45]])
print(m.rref())
print('Rank of matrx:',m.rank())

#question3

#finding determinant ,adjoint,cofactor,inverse using numpy
import numpy as np
n_array =np.array([[50,19],[30,44]])
print("matrix be:\n",n_array)
det =np.linalg.det(n_array)
inverse=np.linalg.inv(n_array)
print("determinant of matrix:",int(det))
print("inverse of matrix:\n",inverse)

# adjoint =transpose of  cofactor
# inverse=transpose of cofactor/determinant of matrix
# determinant of matrix*inverse's transpose = cofactor


k=np.matrix([[1,9,3],[2,5,4],[3,7,8]])
if np.linalg.det==0:
    print('it is a singular matrix')
else:
    cofactor= np.linalg.det(k)*np.linalg.inv(k).T
    print("cofactor of matrix:\n",cofactor)
    print("adjoint of matrix:\n",cofactor.T)
    
