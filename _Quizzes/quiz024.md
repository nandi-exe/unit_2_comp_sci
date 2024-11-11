# Quiz 024

[NB: was unable to complete part B due to the 24th quiz not being in the slides]
## Paper Solution

![image](https://github.com/user-attachments/assets/636340f3-1f8e-4e44-8a13-ce95e4445eef)

## Code

```
from matplotlib import pyplot as plt
import matplotlib
plt.style.use('ggplot')
matplotlib.use('MacOSX')

data =  {
'x': [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19],
'y': [24, 1, 2, 25, 26, 21, 23, 34, 49, 2, 19, 32, 7, 17, 36, 7, 45, 28, 40, 46]
}

x_values = data['x']
y_values = data['y']

plt.scatter(x_values, y_values, color='blue', label='Data Points')
plt.title('Scatter Plot of Data')
plt.xlabel('X Values')
plt.ylabel('Y Values')
plt.legend()
plt.show()
```

## Proof of Work
![image](https://github.com/user-attachments/assets/18172013-2f27-4f3f-99b4-6f0e44d392c3)
