## Quiz 017

# Paper Solution

![IMG_1030](https://github.com/user-attachments/assets/17e5d3d2-8bff-4b73-b2c0-26bff2b837d4)

# Code

```
a, b, c  = 0,0,0
input = [0,1]
print("| A | B | C |")
print(f'| {a} | {b} | {c} |')
for i in range(8):
    if i//1 == 0:
        c = 0
    else:
        c = 1
    if i//2 == 0:
        b = 0
    else:
        b = 1
    if i//4 == 0:
        a = 0
    else:
        a = 1
    print(f'| {a} | {b} | {c} |')
```
# Proof of Work

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/9f095a75-4cae-43e8-af6f-1bc602d8f9d2">

# Part B

![IMG_1022](https://github.com/user-attachments/assets/dae79c8a-0f1d-45dd-82d9-e4bcf834bde4)
