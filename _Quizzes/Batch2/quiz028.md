# Quiz 028

## Paper Solution

## Code

```

import numpy as np
import matplotlib.pyplot as plt
import matplotlib
import requests

plt.style.use("ggplot")
matplotlib.use("MacOSX")

# Server and user details
server_ip = "192.168.4.137"
user = {'username':'UNANDI','password':'nananandi08'}
# register (only one)
#answer = requests.post(f'http://{server_ip}/register',json=user)


login_response = requests.post(f'http://{server_ip}/login', json=user)
cookie = login_response.json().get('access_token')
if not cookie:
    raise ValueError("Failed to retrieve access token. Check login credentials.")

#fetch data from sensor
headers = {'Authorization': f'Bearer {cookie}'}
request = requests.get(f'http://{server_ip}/readings', headers=headers)
data = request.json()

print("Data Response:", data)

#store values
readings = data['readings'][0]
temp = [r["value"] for r in readings if r["sensor_id"] == 11]

#smooth values
window_size = 10
smoothed_values = np.convolve(temp, np.ones(window_size)/window_size, mode='valid')

#range
filtered_indices = np.where((smoothed_values > 0) & (smoothed_values < 40))[0]
filtered_values = smoothed_values[filtered_indices]

#quadratic model
x = np.arange(len(filtered_values))
coefficients = np.polyfit(x, filtered_values, 2)
quadratic_model = np.poly1d(coefficients)

#plot
plt.figure(figsize=(10, 6))
plt.plot(temp, label="Raw Values", alpha=0.5)
plt.plot(np.arange(len(smoothed_values)), smoothed_values, label="Smoothed Values", linewidth=2)
plt.scatter(filtered_indices, filtered_values, color='red', label="Filtered Values")
plt.plot(np.arange(len(filtered_values)), quadratic_model(np.arange(len(filtered_values))),
        label="Quadratic Fit", color='green', linewidth=2)

plt.title("Sensor Data Analysis (Sensor ID = 11)")
plt.xlabel("Time (arbitrary units)")
plt.ylabel("Sensor Value")
plt.legend()
plt.grid()
plt.show()

```
## Proof of Work

<img width="1470" alt="Screenshot 2024-12-03 at 12 49 03" src="https://github.com/user-attachments/assets/749ef49c-9779-4a73-9a05-3d0d0170aece">

