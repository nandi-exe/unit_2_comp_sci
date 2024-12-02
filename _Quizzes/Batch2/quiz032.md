# Quiz 032

## Paper Solution

<img width="690" alt="Screenshot 2024-12-02 at 22 06 30" src="https://github.com/user-attachments/assets/4c2d74b5-4ad6-40c8-99e5-2fa0943cd3d5">

## Code

```
def mystery(a :list, b :list):
    x = []
    for i in a:
        for j in b:
            if i == j:
                x.append(i)
    return x

c = [3,6,9,12,15,18]
d = [2,4,6,8,10,12,14,16,18,20]

print(mystery(c,d))
```
## Proof of Work

![image](https://github.com/user-attachments/assets/ef647e1c-0b75-4a86-b77f-ef3b52191e6a)
