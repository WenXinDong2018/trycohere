# trycohere

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
