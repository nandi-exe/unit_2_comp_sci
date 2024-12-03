# Quiz 028

## Paper Solution

![IMG_229E4EE02B4C-1](https://github.com/user-attachments/assets/89880f06-bfa1-4733-bf3c-b0144c82ae25)
![IMG_D2CEE6EBE4AF-1](https://github.com/user-attachments/assets/01e81890-58e9-4150-8598-968c86d45474)
![IMG_BCA1AFB5B61B-1](https://github.com/user-attachments/assets/7600ba23-8d19-405b-8ae4-76199f678ed9)

## Code

```
import numpy as np
from matplotlib import pyplot as plt
import matplotlib
import requests

def moving_average(windowSize: int, x:list)-> list:
    x_smoothed = []
    for i in range(0,len(x)-windowSize):
        x_section = x[i:i+windowSize]
        x_average = sum(x_section)/windowSize

    return x_smoothed

plt.style.use("ggplot")
matplotlib.use("MacOSX")

server_ip= '192.168.4.137'

request = requests.get(f"http://{server_ip}/readings")
data = request.json()

readings = data['readings'][0]

temp = []
for r in readings:
    if r['sensor_id'] == 11:
        temp.append(r["value"])

temp_segment = temp[600:1600]
temp_smoothed = moving_average(windowSize = 50, x=temp_segment)

x = [*range(0,len(temp_smoothed))] # converting into LIST
#1 liner
m, b = np.polyfit(x, temp_smoothed, deg= 1)
plt.subplot(2,1,1)
plt.title("Temperature")
plt.plot([0,x[-1]], [m*0+b,m*x[-1]+b], color = 'blue')

a,b,c = np.polyfit(x,temp_smoothed,deg = 2)

y_quad = []
for i in x:
    y_quad += [a*i**2 + b*i +c]
plt.plot(y_quad, color = 'purple')

a,b,c,d = np.polyfit(x,temp_smoothed,deg=3)

y_cubic = []
for i in x:
    y_cubic += [a*i**3 + b*i**2 + c*i + d]
plt.plot(y_cubic, color = 'orange')


pressure = []
for r in readings:
    if r['sensor_id'] == 12:
        pressure.append(r["value"])

pressure_segment = pressure[600:1600]
pressure_smoothed = moving_average(windowSize = 50, x=pressure_segment)
x = [*range(0,len(pressure_smoothed))] # converting into LIST

plt.subplot(2,1,2)
plt.plot(pressure_smoothed)
plt.title("Pressure")


plt.subplot(2,1,1)
plt.plot(temp_segment, alpha = 0.5) # until 1599   # alpha is Transparency
plt.plot(temp_smoothed, color='black')
plt.show()
```
## Proof of Work

<img width="1470" alt="Screenshot 2024-12-03 at 12 49 03" src="https://github.com/user-attachments/assets/749ef49c-9779-4a73-9a05-3d0d0170aece">

