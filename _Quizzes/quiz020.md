# Quiz 020

## Paper Solution

## Code

```
from matplotlib import pyplot as plt
import random
import matplotlib
random.seed(1234)
plt.style.use('ggplot')
matplotlib.use('MacOSX')


#when inputs have values, these are the default
def produce(n=5,m=3,s=2):
    x, y = [], []
    for _ in range (n):
        x.append(random.randint(0,100))
        y.append(x[-1] ** (0.5*(m/s)**2))

    return x,y

x,y = produce(200)
plt.plot(x,y)
plt.show()
```
## Proof of Work

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/81169c95-457e-4946-8fb0-85b31de51dd5">

## Part B
