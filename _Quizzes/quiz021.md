# Quiz 021

## Paper Solution

![IMG_1035](https://github.com/user-attachments/assets/afe33aba-7d59-44e8-99f5-278f8eab9376)

## Code
```
from matplotlib import pyplot as plt
import random
import matplotlib
plt.style.use('ggplot')
matplotlib.use('MacOSX')
start = -10
step = 0.2
x, y = [], []
for i in range (int(20/step)):
   x.append(start + i*step)
   y.append(2*(x[-1]+5)**2)

plt.plot(x,y)
plt.show()
```

## Proof of Work

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/f6041348-679c-4ae3-931f-f7b07d346cb4">

## Part B

![IMG_1026](https://github.com/user-attachments/assets/f7992528-a765-4591-abca-ff2eb90dab68)
