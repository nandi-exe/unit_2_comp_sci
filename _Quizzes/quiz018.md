# Quiz 018

## Paper Solution


## Code

```
def flip(num:int):
    if num == 1:
        num = 0
    elif num == 0:
        num = 1
    return num

def or_func(x:int,y:int):
    if x == 0 and y == 0:
        return 0
    else:
        return 1


print("| A | B | C |")
a, b, c = True, True, True
for i in range(8):
    if i%1 == 0:
        c = not c
    if i%2 == 0:
        b = not b
    if i%4 == 0:
        a = not a
    in1, in2, in3, = 1*a, 1*b, 1*c
    enter1 = or_func(flip(in2),flip(in2*in3))
    enter2 = (in1*in2)
    value = or_func(enter1,enter2)
    print(f'| {1*a} | {1*b} | {1*c} | {value} |')
```

## Proof of Work

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/c63d4954-2305-452b-93d9-ce2cec42ee34">

## Part B

![IMG_1023](https://github.com/user-attachments/assets/0fb90f96-e8a8-439d-902a-fcc20cce885d)

