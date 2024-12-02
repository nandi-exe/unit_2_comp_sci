# Quiz 025

## Paper Solution

![IMG_A4AE58BF8A1D-1](https://github.com/user-attachments/assets/514701a6-61fd-4f7d-aa25-1931896c45ea)

## Code

```
def count_letters(input_dict, input_string):

    input_string = input_string.lower()

    for char in input_string:
        if char in input_dict:
            input_dict[char] += 1

    return input_dict
sample_dict = {
    'a':0,
    'e':0,
    'i':0,
    'o':0,
    'u':0,
}

example_string = "Hello World!"

result = count_letters(sample_dict, example_string)
print(result)
```
## Proof of Work

<img width="1435" alt="Screenshot 2024-12-03 at 8 32 41" src="https://github.com/user-attachments/assets/90884c48-1bf6-49f4-a73e-d38e3c99b56f">

