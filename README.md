# closest_material_design_color

A Python tool for identifying the closest Material Design color to a given HEX input using color matching in the HLS color space.

## Description

This tool takes a HEX color code as input and finds the closest matching color from the Material Design color palette. It uses the HLS (Hue, Lightness, Saturation) color space for comparison, which provides a reasonable approximation of perceptual color differences.

## Usage

Run the script from the command line, providing a HEX color code as an argument:

```
python closest_material_design_color.py <HEX_COLOR>
```

Example:

```
python closest_material_design_color.py #E3E0CA
```

Output:
```
The closest Material Design color to #E3E0CA is Brown 100.
```

## Features

- Supports all standard Material Design colors, including their variants (50-900 and A100-A700)
- Uses HLS color space for color comparison
- Simple command-line interface

## Requirements

- Python 3.x
- NumPy
- Pillow (PIL)

## Installation

1. Clone this repository or download the `closest_material_design_color.py` file.
2. Install the required dependencies:

```
pip install numpy pillow
```

## Note

While this tool provides a good approximation, it may not always match human perception perfectly. For more accurate results, consider using more advanced color difference algorithms like CIEDE2000 in the CIE Lab* color space.
