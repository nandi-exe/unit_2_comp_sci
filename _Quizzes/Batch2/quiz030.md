# Quiz 030

## Paper Solution

## Code

```
import numpy as np
from  matplotlib import pyplot as plt
import matplotlib
import requests

plt.style.use("ggplot")
matplotlib.use("MacOSX")

server_ip = "192.168.4.137"
request = requests.get(f"http://{server_ip}/readings")
data = request.json()

readings = data['readings'][0]

temp = []
humidity = []
for r in readings:
    if r['sensor_id'] == 11:
        temp.append(r["value"])
    if r['sensor_id'] == 10:
        humidity.append(r["value"])

x = np.arange(len(temp))

m, b = np.polyfit(x, temp, deg=1)

plt.subplot(3, 1, 1)
plt.plot(temp, color='yellow', label='Temperature')
plt.plot(x, m * x + b, '--', color='blue')
plt.title("Temperature")
plt.legend()

#humidity
plt.subplot(3, 1, 2)
plt.plot(humidity, color='red', label='Pressure')
plt.title("pressure")
plt.legend()

combined = [t - ct for t, ct in zip(temp, humidity)]

plt.subplot(3, 1, 3)
plt.plot(combined, color='red', label='Pressure')
plt.title("pressure")
plt.legend()

plt.tight_layout()
plt.show()
```
## Proof of Work

<img width="1356" alt="image" src="https://github.com/user-attachments/assets/be1c0f83-73ee-4586-9edc-2ae71f8b4982">
