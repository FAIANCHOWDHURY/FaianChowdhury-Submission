
# Project Submission: Max and Linear Search Algorithms

## Submitted by: Faian Chowdhury

## Overview
This project implements two fundamental algorithms in Python:
1. **Max Search**: Finds the largest number in a list.
2. **Linear Search**: Searches for a target value in a list and returns its index.

The project also demonstrates the use of Git and GitHub for version control and collaboration, adhering to best practices in software development.

---

## How to Run the Code
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/Daniel-Packer/MAT2440-Projects-F24
   ```
2. Navigate to the `src` folder.
3. Run the `max_search.py` and `linear_search.py` scripts with Python:
   ```bash
   python max_search.py
   python linear_search.py
   ```

## Folder Structure
```
faian-chowdhury-submission/
├── README.md            # Project documentation
├── src/                 # Code folder
│   ├── max_search.py    # Max Search implementation
│   └── linear_search.py # Linear Search implementation
└── tests/               # Test scripts
    ├── test_max_search.py
    └── test_linear_search.py
```

---

## Algorithms
### Max Search
The Max Search algorithm identifies the largest value in a list of integers.

#### Algorithm Description:
1. Assume the first element in the array is the maximum.
2. Loop through the rest of the array:
   - If a value greater than the current maximum is found, update the maximum value.
3. Return the maximum value.

#### Python Implementation:
```python
# File: src/max_search.py

def max_search(arr):
    # Assume the first element is the maximum
    max_val = arr[0]

    # Loop through the rest of the elements
    for num in arr[1:]:
        if num > max_val:
            max_val = num  # Update max_val if a larger element is found

    return max_val

# Example usage
if __name__ == "__main__":
    example_list = [3, 1, 4, 1, 5, 9, 2, 6]
    print("The largest value is:", max_search(example_list))
```
---

### Linear Search
The Linear Search algorithm iterates through a list to find a target value and returns its index.

#### Algorithm Description:
1. Iterate through the list, starting from the first element.
2. If the current element matches the target value, return its index.
3. If the end of the list is reached without finding the target, return -1.

#### Python Implementation:
```python
# File: src/linear_search.py

def linear_search(arr, target):
    for index, value in enumerate(arr):
        if value == target:
            return index  # Return index of the found element
    return -1  # Return -1 if not found

# Example usage
if __name__ == "__main__":
    example_list = [3, 1, 4, 1, 5, 9, 2, 6]
    target_value = 5
    result = linear_search(example_list, target_value)
    if result != -1:
        print(f"Target value {target_value} found at index {result}.")
    else:
        print(f"Target value {target_value} not found.")
```
---

## Testing
The `tests` folder includes scripts to verify the correctness of the algorithms. The test cases cover a wide range of inputs, including edge cases, typical scenarios, and special conditions.

#### Max Search Test:
```python
# File: tests/test_max_search.py
from src.max_search import max_search

def test_max_search():
    assert max_search([3, 1, 4, 1, 5, 9, 2, 6]) == 9
    assert max_search([10, 20, 30, 40]) == 40
    assert max_search([5, -1, 0, 2]) == 5
    print("All Max Search tests passed!")

if __name__ == "__main__":
    test_max_search()
```

#### Linear Search Test:
```python
# File: tests/test_linear_search.py
from src.linear_search import linear_search

def test_linear_search():
    assert linear_search([3, 1, 4, 1, 5, 9, 2, 6], 5) == 4
    assert linear_search([10, 20, 30, 40], 25) == -1
    assert linear_search([5, -1, 0, 2], -1) == 1
    print("All Linear Search tests passed!")

if __name__ == "__main__":
    test_linear_search()
```

---

## Git and GitHub Workflow
- **Branching**: A separate branch was created for the submission: `faian-chowdhury-submission`.
- **Committing**: Changes were incrementally saved using meaningful commit messages.
- **Pull Request**: The final work was submitted as a pull request for review.

---

## Summary
- **Max Search**: Finds the largest element in a list.
- **Linear Search**: Searches for a target value and returns its index.
- **Testing**: Both implementations include test scripts to validate their correctness and robustness.

### Future Improvements
- Extend the algorithms to handle more complex data structures (e.g., nested lists).
- Optimize the algorithms for specific use cases (e.g., parallel processing).
- Incorporate additional search algorithms (e.g., binary search) for comparison.

Run the tests and code as described above to ensure the project works as intended.
