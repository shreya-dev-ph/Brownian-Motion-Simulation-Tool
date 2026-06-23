# Brownian-Motion-Simulation-Tool


A Python package for simulating and plotting Brownian motion in 2D and 3D. It is based on random walk using Gaussian noise, and visualizes particle trajectories over time.
The package can simulate multiple trials of random Brownian motion for a user-given number of steps and step length. It also provides plotting functions for visualizing the simulated paths.

## Features

* Simulate 2D Brownian motion
* Simulate 3D Brownian motion
* Run multiple trials
* Plot 2D and 3D trajectories
* Use from Python code or from the command line

## Installation

From the project folder, install the package in editable mode:

```bash
pip install -e .
```

## Command-line usage

Run a 2D simulation:

```bash
brownian_motion_simulation 2D 5 1000 1.0
```

Run a 3D simulation:

```bash
brownian_motion_simulation 3D 5 1000 1.0
```

The arguments are:

```text
dimension trial_number number_of_steps step_length
```

Example:

```bash
brownian_motion_simulation 2D 5 1000 1.0
```

This means:

* `2D`: simulate in two dimensions
* `5`: run 5 trials
* `1000`: use 1000 steps per trial
* `1.0`: use step length 1.0

## Python usage

```python
from brownian_motion_simulation import (
    motion_2d,
    collecting_data_2d,
    plot_2d,
)

x_data, y_data = collecting_data_2d(
    trial_number=5,
    motion_function=motion_2d,
    number_of_steps=1000,
    step_length=1.0,
)

plot_2d(x_data, y_data)
```

## License

This project is licensed under the MIT License.

