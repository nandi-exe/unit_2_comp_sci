# Quiz 022

## Paper Solution

## Code

```
from matplotlib import pyplot as plt
import random
import matplotlib
plt.style.use('ggplot')
matplotlib.use('MacOSX')

start1 = -10
stop1 = 0
start2 = 0
stop2 = 10
step = 0.2
x1 = []
x2 = []
y1 = []
y2 = []

for _ in range(int(10/step)):
    x1.append(start1 + _*step)
    y1.append(-1*x1[-1])
    x2.append(start2 + _ * step)
    y2.append(x2[-1])

plt.plot(x1,y1, linewidth = 2, color = 'red')
plt.plot(x2,y2, linewidth = 2, color = 'red')
plt.plot()
plt.show()
```

## Proof of Work

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/13a33932-3ba8-4002-a525-7819a477c40c">

## Part B

![IMG_1027](https://github.com/user-attachments/assets/6530d4ac-9b90-44d0-96f4-11b7684d3c66)
