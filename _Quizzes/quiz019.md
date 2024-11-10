# Quiz 019

## Paper Solution

## Code

```

import random
random.seed(1234)
def produce(n, m, s):
    result = ""
    for _ in range(n):
        x = random.randint(0, 100)  # Generate a random integer x between 0 and 100
        y = x * (0.5 * (m / s)) ** 2
        
        result = result + f'\n| {x} | {y} |'
    return result

sample = produce(n=5, m=3, s=2)
print(sample)
```

## Proof of Work

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/2fa96492-6a44-4aa7-b849-439db4cd44e6">


## Part B

![IMG_1024](https://github.com/user-attachments/assets/ba4be63f-3eae-4318-94d4-150af177c500)
