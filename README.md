# 1D Magnetotelluric Forward Modeling

This repository contains Python code for 1D magnetotelluric (MT) forward modeling using three different methods: Wait (1954), Constable (1987), and Grandis (1999).

## Introduction

Magnetotellurics (MT) is a passive electromagnetic geophysical method that uses natural time-varying electric and magnetic fields to investigate the electrical resistivity structure of the subsurface. 1D MT forward modeling calculates the theoretical MT response (apparent resistivity and phase) for a layered earth model.

This notebook implements and compares three different approaches for 1D MT forward modeling:

- **Wait (1954):** A classical approach based on the impedance at the surface of a layered earth.
- **Constable (1987):** Uses the C-function method for calculating the MT response.
- **Grandis (1999):** Implements the transfer matrix method.

The code calculates the apparent resistivity and phase for a given layered earth model over a range of frequencies and then plots the results for comparison.

## Getting Started

### Prerequisites

- Python 3.x
- Libraries: `numpy`, `matplotlib`

### Installation

No specific installation is required beyond having Python and the necessary libraries. You can run the code directly in a Jupyter Notebook or a Python environment.

### Running the code

1. Clone this repository or download the `1D_MT_Forward_Modeling.ipynb` notebook.
2. Open the notebook in a Jupyter environment (e.g., JupyterLab, Google Colab).
3. Run the cells sequentially.

## Code Description

The notebook is structured as follows:

- **Import Libraries:** Imports necessary libraries (`numpy`, `matplotlib`, `random`).
- **Define Model Parameters:** Sets up the layered earth model with resistivities and thicknesses.
- **Frequency Setup:** Defines the range of frequencies for the forward modeling.
- **Wait (1954) Method:** Implements the forward modeling using Wait's method.
- **Constable (1987) Method:** Implements the forward modeling using Constable's C-function method. Includes helper functions for hyperbolic cotangent and inverse hyperbolic cotangent.
- **Grandis (1999) Method:** Implements the forward modeling using Grandis' transfer matrix method.
- **Plotting:** Generates plots of apparent resistivity and phase as a function of frequency for all three methods.

## Model Parameters

The layered earth model is defined by:

- `camadas`: Number of layers.
- `resistivities`: A NumPy array of resistivity values for each layer in Ohm.m.
- `h`: A NumPy array of thicknesses for each layer in meters (excluding the last layer, which is semi-infinite).

The frequencies are defined using `np.logspace` to create a logarithmically spaced array.

## Output

The code outputs plots showing:

- Apparent resistivity (Ω·m) vs. Frequency (Hz)
- Phase (degrees) vs. Frequency (Hz)

These plots compare the results obtained from the three different forward modeling methods.

## Contributing

If you would like to contribute to this project, please feel free to fork the repository and submit a pull request.


## References
    - Wait, J. R. (1954). Mutual Coupling of Loops in a Layered Homogeneous Half-Space. *Geophysics*, 19(2), 290-296.
    - Constable, S. C., Parker, R. L., & Constable, C. G. (1987). Occam's inversion: A practical algorithm for generating smooth models from electromagnetic sounding data. *Geophysics*, 52(3), 289-300.
    - Grandis, H. (1999). 1D MT forward modelling program. *Computers & Geosciences*, 25(3), 253-260.
