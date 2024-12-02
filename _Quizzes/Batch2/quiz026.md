# Quiz 026

## Paper Solution

![IMG_F0AA97E45948-1](https://github.com/user-attachments/assets/ad3e5460-2e32-4b39-8b2c-108bd8fbe9c2)

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
