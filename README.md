# This is a TA training program for the Python and Machine Learning Course 
import numpy as np
import matplotlib.pyplot as plt
a = np.array([
    [30, 40, 50,  2,  6, 14, 14, 6],  
    [60, 70, 80, 18, 12,  2,  6, 8],  
    [46, 61, 70,  2,  6, 14, 14, 6]
])
print (a)

[[30 40 50  2  6 14 14  6]
 [60 70 80 18 12  2  6  8]
 [46 61 70  2  6 14 14  6]

b=a[:,3:]
print (b)

[[ 2  6 14 14  6]
 [18 12  2  6  8]
 [ 2  6 14 14  6]]

c=np.sum(b,axis=1)
print (c)
y=np.transpose(c)

[42 46 42]

print (a)
print (y)
v = np.linalg.lstsq (a, y)
print (v)

[[30 40 50  2  6 14 14  6]
 [60 70 80 18 12  2  6  8]
 [46 61 70  2  6 14 14  6]]
[42 46 42]
(array([-0.12822723, -0.5267449 ,  0.65566393,  0.89355145,  0.81751536,
        0.7541641 ,  0.9316059 ,  0.64007355]), array([], dtype=float64), 3, array([178.09293181,  20.15309694,   4.6647961 ]))
C:\Users\Ata\Anaconda3\lib\site-packages\ipykernel_launcher.py:3: FutureWarning: `rcond` parameter will change to the default of machine precision times ``max(M, N)`` where M and N are the input matrix dimensions.
To use the future default and silence this warning we advise to pass `rcond=None`, to keep using the old, explicitly pass `rcond=-1`.
  This is separate from the ipykernel package so we can avoid doing imports until
