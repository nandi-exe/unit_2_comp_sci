# Quiz 025

## Paper Solution

## Code

```
def flip(d):
    inverted = {}

    for key, value in d.items():
        inverted[value] = key

    return inverted

original_dict = {'a': 1, 'b': 2, 'c': 3}
inverted_dict = flip(original_dict)
print(inverted_dict)
```
## Proof of Work

<img width="1392" alt="image" src="https://github.com/user-attachments/assets/a0ded82a-5b1a-42f0-bad8-ccc5f6f61949">
