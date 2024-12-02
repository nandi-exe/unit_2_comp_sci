# Quiz 031

## Paper Solution

![IMG_BCCE06AD9D8D-1](https://github.com/user-attachments/assets/fac25b51-6646-49ad-b808-9458d9047006)

## Code

```
from matplotlib import pyplot as plt
import matplotlib

plt.style.use("ggplot")
matplotlib.use("MacOSX")

# Initialize parameters
para1, flip1, para2, flip2 = [], [], [], []
step = 4 / 100  # Step size for x values
x = []
rotated_x = []
rotated_y = []
flipped_x = []
st = -2  # Starting value for x

# Generate x values and corresponding y values
for count in range(100):
    x_value = st + (step * count)
    x.append(x_value)
    y_value = x_value ** 2
    para1.append(y_value)  # Parabola opening upwards
    flip1.append(-y_value)  # Parabola opening downwards
    rotated_x.append(-y_value)  # Rotated x-values for parabolas
    rotated_y.append(x_value) # Rotated y-values
    flipped_x.append(y_value)

# Reflect the rotated parabola (third graph) to create the fourth graph
for ry in rotated_y:
    flip2.append(-ry)  # Reflect rotated_y about the x-axis

# Plot the parabolas
plt.plot(x, para1, linewidth=2, color='red', label="Parabola 1")
plt.plot(x, flip1, linewidth=2, color='blue', label="Parabola 2")
plt.plot(rotated_x, rotated_y, linewidth=2, color='green', label="Parabola 3")
plt.plot(flipped_x, flip2, linewidth=2, color='purple', label="Parabola 4")

# Add labels, title, and legend
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.title("Parabolic Transformations")
plt.legend()
plt.show()
```

## Proof of Work

![image](https://github.com/user-attachments/assets/9604ecfb-572a-4586-b238-072a0b0bdf2c)

