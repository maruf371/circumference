# Circumference Calculator

An advanced Python application for calculating circle measurements including circumference, area, diameter, and more.

## Features

- **Multiple Calculations**: Calculate circumference, area, and diameter
- **Object-Oriented Design**: Built with a clean `CircleCalculator` class
- **Input Validation**: Ensures only positive radius values are accepted
- **Interactive Menu**: User-friendly menu system for choosing calculations
- **Unit Tests**: Comprehensive test suite included
- **Error Handling**: Robust error handling with meaningful messages

## Installation

No external dependencies required! This project uses only Python's built-in `math` module.

```bash
git clone https://github.com/maruf371/circumference.git
cd circumference
```

## Usage

### Run the Interactive Application

```bash
python circumference.py
```

### Use as a Module

```python
from circumference import CircleCalculator

# Create a calculator for a circle with radius 5
calc = CircleCalculator(5)

# Get individual measurements
print(calc.circumference())  # Output: 31.4159...
print(calc.area())          # Output: 78.5398...
print(calc.diameter())      # Output: 10

# Get all measurements at once
measurements = calc.get_all_measurements()
print(measurements)
# Output: {'radius': 5, 'diameter': 10, 'circumference': 31.415926..., 'area': 78.539816...}

# Pretty print
print(calc)
```

## API Reference

### CircleCalculator Class

#### Methods

- `circumference()` → float: Returns the circumference of the circle
- `area()` → float: Returns the area of the circle
- `diameter()` → float: Returns the diameter of the circle
- `get_all_measurements()` → dict: Returns a dictionary with all measurements

## Testing

Run the unit tests to verify functionality:

```bash
python -m unittest test_circumference.py -v
```

## Examples

```
Enter the radius of the circle: 10
========================================
Circle with radius 10
  Diameter: 20.0000
  Circumference: 62.8319
  Area: 314.1593
========================================
```

## Error Handling

The calculator includes validation for invalid inputs:

```python
try:
    calc = CircleCalculator(-5)
except ValueError as e:
    print(e)  # Output: Radius must be a positive number
```

## License

This project is open source and available under the MIT License.
