# Quiz 023

## Paper Solution

![image](https://github.com/user-attachments/assets/335c8669-b241-4908-91d7-cbe226fdff79)

## Code

```
from matplotlib import pyplot as plt
import matplotlib
import numpy as np
plt.style.use('ggplot')
matplotlib.use('MacOSX')
x = []
h = [57.0,56.0,57.0,56.0,55.0,55.0,54.0,54.0,54.0,53.0,53.0,54.0,53.0,53.0,52.0,52.0,51.0,51.0,51.0,50.0,50.0,49.0,49.0,48.0,49.0,49.0,48.0,48.0,48.0,49.0]
for i in range(len(h)):
    x.append(i*3.2)
m, b = np.polyfit(x, h, 1)
plt.scatter(x,h , color = 'blue')
plt.xlabel("Time in seconds")
plt.ylabel("Relative Humidity")
plt.show()
```

## Proof of Work

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/fdf22c7b-6894-4540-9ba3-89d619f9a8d4">

## Part B

![IMG_1028](https://github.com/user-attachments/assets/4336235f-5774-437c-8bc7-da46ff6bfa93)
