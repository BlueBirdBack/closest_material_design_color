# closest_material_design_color

A Python tool for identifying the closest Material Design color to a given color input (HEX or RGB) or colors extracted from an image using color matching in the HLS color space.

## Description

This tool takes either a HEX color code, RGB values, or an image file as input and finds the closest matching color(s) from the Material Design color palette. It uses the HLS (Hue, Lightness, Saturation) color space for comparison, which provides a reasonable approximation of perceptual color differences. For image inputs, it extracts the dominant colors and provides Material Design matches for each.

## Usage

Run the script from the command line, providing either a HEX color code, RGB values, or an image file path as an argument:

```
python closest_material_design_color.py [--hex HEX | --rgb R G B | --image IMAGE]
```

Examples:

For a HEX color:
```
python closest_material_design_color.py --hex "#E3E0CA"
```

For RGB values:
```
python closest_material_design_color.py --rgb 227 224 202
```

For an image file:
```
python closest_material_design_color.py --image path/to/your/image.jpg
```

Output for HEX or RGB input:
```
The closest Material Design color to #E3E0CA is Brown 100.
```

Output for image input:
```
Dominant Color: #3F5E8C
Closest Material Design color to dominant: Blue 800
Color Palette:
  #3F5E8C - Closest: Blue 800
  #8CA0B5 - Closest: Blue Grey 200
  #C7D4E2 - Closest: Blue Grey 50
  #E2EBF4 - Closest: Blue Grey 50
  #F0F4F8 - Closest: Blue Grey 50
  #FFFFFF - Closest: White
```

## Features

- Supports all standard Material Design colors, including their variants (50-900 and A100-A700)
- Uses HLS color space for color comparison
- Accepts HEX, RGB, and image file inputs
- Extracts dominant colors from images using colorgram.py
- Simple command-line interface

## Requirements

- Python 3.x
- NumPy
- Pillow (PIL)
- colorgram.py

## Installation

1. Clone this repository or download the `closest_material_design_color.py` file.
2. Install the required dependencies:

```
pip install numpy pillow colorgram.py
```

## Note

While this tool provides a good approximation, it may not always match human perception perfectly. For more accurate results, consider using more advanced color difference algorithms like CIEDE2000 in the CIE Lab* color space.

The image color extraction feature uses colorgram.py, which offers better performance and accuracy compared to older libraries like colorthief.
