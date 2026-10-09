# Exploring Circular Trajectories with Smartphone Data

## Learning goal

Connect circular motion recorded with a smartphone to geometric and functional
representations of a circle.

## Core question

How do the spatial trajectory and the graphs of position change when a circular
path is performed at different speeds?

## Mathematical model

For an ideal circle with radius r and center (x_0, y_0):

    x(t) = x_0 + r cos(theta(t))
    y(t) = y_0 + r sin(theta(t))

When angular speed is approximately constant:

    theta(t) = omega t + theta_0

Changing the pace changes omega, and therefore the frequency of the position
signals. The radius should remain approximately constant for the same path.

## Proposed activity

1. Record the same circular trajectory at two or more different paces.
2. Plot the observed path in the x-y plane.
3. Plot x(t) and y(t) separately.
4. Compare the amplitude, period, phase difference, and deviations from the
   ideal circular model.
5. Discuss how noise, uneven speed, GPS precision, and device movement affect
   the observed data.

## Multimodal connection

In addition to the spatial trajectory, accelerometer and audio signals may help
describe movement pace and collection context. These signals will be explored
after the initial trajectory data is organized.

## Future implementation

Future Python tools should load a trajectory, generate spatial and time-series
plots, and support comparison with an ideal geometric representation.
