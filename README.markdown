# LorenzAttractorSimulator

## Description
This Python script simulates the Lorenz system, a set of differential equations known for its chaotic behavior, using the 4th-order Runge-Kutta (RK4) method. It visualizes the system's trajectory in both 2D (y vs. time and z vs. x) and 3D plots using `matplotlib`. The 2D plot of z vs. x uses a gradient colormap to indicate temporal progression, while the 3D plot shows the full trajectory with start and end points. Both plots are saved as high-quality PNG files. An optional animation feature visualizes the trajectory's evolution in 3D. The script leverages `numpy` for efficient numerical computations.

## Features
- Solves the Lorenz system using the RK4 method for accurate integration.
- Generates two 2D plots: y vs. time and z vs. x with a gradient colormap.
- Creates a 3D plot of the Lorenz attractor with start and end points.
- Saves plots as high-quality PNG files (`lorenz_2d_plot.png` and `lorenz_3d_plot.png`).
- Supports optional 3D animation to visualize trajectory evolution.
- Uses vectorized operations for performance and modular code for readability.

## Requirements
- Python 3.x
- Required libraries:
  - `numpy`
  - `matplotlib`
- Optional (for saving animation as GIF):
  - `pillow` (for `Pillow` writer)
  - `imagemagick` (alternative for GIF export)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/lorenz-attractor-simulator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd lorenz-attractor-simulator
   ```
3. Install the required libraries:
   ```bash
   pip install numpy matplotlib
   ```
4. (Optional) For GIF animation support, install `pillow`:
   ```bash
   pip install pillow
   ```

## Usage
1. Save the script as `lorenz_attractor.py`.
2. Run the script:
   ```bash
   python lorenz_attractor.py
   ```
3. The script will:
   - Simulate the Lorenz system with default parameters (σ=10, R=28, β=8/3, initial conditions [0, 1, 0]).
   - Generate two plots:
     - 2D plots: y vs. time and z vs. x with a gradient colormap (`lorenz_2d_plot.png`).
     - 3D plot: Full trajectory with start (green) and end (red) points (`lorenz_3d_plot.png`).
   - Save both plots in the project directory.
   - Display the plots.
4. To enable animation, modify the script to call `plot_lorenz_attractor(animate=True)`. Optionally, uncomment the GIF saving line to export the animation as `lorenz_animation.gif`.

## Example Output
Below are examples of the generated plots for a 1000-point simulation over 50 time units:

**2D Plots**:
![2D Lorenz Plot](lorLsenz_2d_plot.png)

**3D Plot**:
![3D Lorenz Plot](lorenz_3d_plot.png)

*(Note: Add screenshots of the plots by running the script and uploading the generated PNG files to the repository.)*

## Code Explanation
- **Function**: `lorenz_derivatives(state, time)`
  - Computes derivatives of the Lorenz system (dx/dt, dy/dt, dz/dt).
- **Function**: `rk4_integrate(f, initial_cond, t_array)`
  - Solves the system using the 4th-order Runge-Kutta method.
- **Function**: `plot_lorenz_attractor(initial_cond, t_max, num_points, animate, figsize, dpi)`
  - Simulates the system and generates 2D and 3D plots.
  - Supports animation for the 3D plot if `animate=True`.
  - Saves plots as PNG files.
- **Key Parameters**:
  - `initial_cond = [0.0, 1.0, 0.0]`: Initial conditions [x0, y0, z0].
  - `t_max = 50.0`: Maximum simulation time.
  - `num_points = 1000`: Number of time points.
  - `animate = False`: If True, displays an animated 3D plot.
iamas
  - `figsize = (12, 6)`: Size of 2D plots.
  - `dpi = 300`: Resolution for saved plots.

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or feedback, feel free to open an issue on GitHub or contact [your-email@example.com](mailto:your-email@example.com).