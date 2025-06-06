# 📐 Polygon Area Calculator

This is a beginner-friendly Python project that uses **Object-Oriented Programming (OOP)** concepts to build a simple geometry utility for rectangles and squares. It includes two classes: `Rectangle` and `Square` (which is a subclass of `Rectangle`).

## 🚀 Features

- Create `Rectangle` and `Square` objects
- Compute:
  - Area
  - Perimeter
  - Diagonal
- Print ASCII pictures of the shapes (up to a size limit)
- Check how many times one shape fits inside another
- Easily modify dimensions

## 📦 Classes

### `Rectangle`

| Method           | Description |
|------------------|-------------|
| `__init__(width, height)` | Initializes the rectangle with width and height |
| `set_width(width)` | Sets a new width |
| `set_height(height)` | Sets a new height |
| `get_area()` | Returns the area: `width * height` |
| `get_perimeter()` | Returns the perimeter: `2 * width + 2 * height` |
| `get_diagonal()` | Returns the diagonal length |
| `get_picture()` | Returns a string picture of the shape (max size: 50) |
| `get_amount_inside(other_shape)` | Returns how many times `other_shape` fits inside |
| `__str__()` | Returns `Rectangle(width=..., height=...)` |

---

### `Square` (inherits from `Rectangle`)

| Method           | Description |
|------------------|-------------|
| `__init__(side)` | Initializes a square with equal side length |
| `set_side(side)` | Sets both width and height to `side` |
| `set_width(width)` | Also sets height to maintain square shape |
| `set_height(height)` | Also sets width to maintain square shape |
| `__str__()` | Returns `Square(side=...)` |

## 💡 Example Usage

```python
from polygon_calculator import Rectangle, Square

rect = Rectangle(10, 5)
print(rect.get_area())          # 50
rect.set_height(3)
print(rect.get_perimeter())     # 26
print(rect.get_picture())

sq = Square(9)
print(sq.get_area())            # 81
sq.set_side(4)
print(sq.get_diagonal())        # 5.656...
print(sq.get_picture())

rect.set_height(8)
rect.set_width(16)
print(rect.get_amount_inside(sq))  # 8
