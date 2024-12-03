# Quiz 030

## Paper Solution

## Code

```
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
hum = []
for r in readings:
    if r['sensor_id'] == 11:
        temp.append(r["value"])
    if r['sensor_id'] == 10:
        hum.append(r["value"])

averages = [(temp[i] + hum[i]) / 2 for i in range(100)]

# Create horizontally arranged subplots
fig, axes = plt.subplots(1, 3, figsize=(15, 5))

# Temperature plot
axes[0].plot(temp, label="Temperature", color="red")
axes[0].set_ylabel("Temperature (°C)")
axes[0].set_title("Temperature Readings")
axes[0].legend()
axes[0].grid(True)

# Humidity plot
axes[1].plot(hum, label="Humidity", color="blue")
axes[1].set_ylabel("Humidity")
axes[1].set_title("Humidity Readings")
axes[1].legend()
axes[1].grid(True)

# Averages plot
axes[2].plot(averages, label="Average", color="green")
axes[2].set_ylabel("Average")
axes[2].set_title("Average of Readings")
axes[2].legend()
axes[2].grid(True)

# Adjust layout
plt.tight_layout()
plt.show()

```
## Proof of Work

<img width="1470" alt="Screenshot 2024-12-03 at 12 53 04" src="https://github.com/user-attachments/assets/13a3d267-9a78-4822-bd3e-982a7ffec7af">

