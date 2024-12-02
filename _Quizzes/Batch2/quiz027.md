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
