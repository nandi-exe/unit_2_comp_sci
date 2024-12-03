# Quiz 027

## Paper Solution

![IMG_1187](https://github.com/user-attachments/assets/2a8ef987-b3d3-4a65-bd6f-de3529b5ce3c)

## Code

```
def sort_dict(input_dict):
    
    sorted_dict = dict(sorted(input_dict.items(), key=lambda item: item[1]))
    return sorted_dict

example_dict = {'apples': 3, 'bananas': 1, 'cranberries': 2}
sorted_dict = sort_dict(example_dict)
print(sorted_dict)
```
## Proof of Work

<img width="1470" alt="Screenshot 2024-12-03 at 8 47 37" src="https://github.com/user-attachments/assets/c59ad94b-5bb6-4925-85a4-077a28135a28">

# Part B

## Paper Solution

![Screenshot 2024-12-03 at 9 57 41 AM](https://github.com/user-attachments/assets/0a96ad36-8a37-410d-b875-fd5ff984bfb5)

## Code

```
from  matplotlib import pyplot as plt
import matplotlib

plt.style.use('ggplot')
matplotlib.use('MacOSX')

x = []
y = []

start = 0
st = 1/100
for i in range(100):
    x_val = start + i*st
    x.append(x_val)
    y.append(math.sin(2* x_val * 3.14159265))

plt.plot(x,y, color='blue', label='Polynomial')
plt.title("y=sin(2*pi*x)")
plt.show()

```
## Proof of Work

![image](https://github.com/user-attachments/assets/b55bad18-dc14-4e4f-a80c-f3480518cf82)


