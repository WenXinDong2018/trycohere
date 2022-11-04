# Use Cohere API for intent classification

```
from cohere.classify import Example

examples = [Example("2x+3 = 1", "Solve Linear Equations"),
            Example("5x-2 = 3", "Solve Linear Equations"),
            Example("1+2 = ?", "Addition"),
            Example("3+9 = ?", "Addition"),
            Example("5-4 = ?", "Subtraction"),
            Example("12-2 = ?", "Subtraction")]

inputs=["4x + 3 = -1",
        "2+3 = ?",
        "4-2 = ?"]

response = co.classify(
  model='medium',
  inputs=inputs,
  examples=examples)

print(response.classifications)

```

Result: 

```
[Classification<prediction: "Solve Linear Equations", confidence: 0.9948228>, 
Classification<prediction: "Addition", confidence: 0.9844185>, 
Classification<prediction: "Subtraction", confidence: 0.96842146>]
```
