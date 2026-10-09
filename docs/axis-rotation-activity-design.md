# Exploring Rotation Around the Body Axis

## Learning goal

Connect a full-body rotation while holding a smartphone to angle, angular
velocity, periodicity, and orientation data.

## Sensor requirement

This activity requires gyroscope, heading, or device-orientation data.
Accelerometer and GPS data alone may not describe a smooth rotation around the
vertical body axis reliably.

## Proposed activity

The participant holds the smartphone in a fixed position relative to the body,
for example in front of the chest, and performs one complete turn around their
own vertical axis.

The activity can be repeated at different paces.

## Mathematical model

Let theta(t) describe the orientation angle of the smartphone over time.

For one complete turn:

    change in theta is approximately 2 pi radians

If the rotation is approximately uniform:

    theta(t) = omega t + theta_0

where omega is the angular velocity.

## Questions for exploration

- Does the recorded orientation change by approximately one full turn?
- How does theta(t) change for slow and fast rotations?
- How does the slope of theta(t) relate to angular velocity?
- Does the integral of the gyroscope signal approximate the total rotation?
- What happens when orientation data wraps from 360 degrees back to 0 degrees?

## Multimodal connection

Video may show the change in visual scene during the turn. GPS is expected to
remain approximately constant, which helps illustrate that different modalities
capture different aspects of the same action.

## Future implementation

Future Python tools should load orientation or gyroscope data, unwrap angular
measurements when necessary, plot theta(t), and compare rotations performed at
different speeds.
