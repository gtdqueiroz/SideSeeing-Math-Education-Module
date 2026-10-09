# Initial Trajectory Collection Plan

## Objective

Build a small multimodal dataset of planar geometric trajectories to support
the SideSeeing Mathematics Education Module.

## Planned trajectory types

- Line segments
- Circles
- Simple polygons

These trajectories will be used to connect geometric representations with
time-series, spatial, visual, and sensor-based data.

## Planned modalities

Each collection session may contain the following modalities when available:

- Video
- Audio
- Accelerometer data
- GPS data

## Metadata to record

For each trajectory, the initial dataset should identify:

- Trajectory ID
- Geometric shape
- Collection session
- Approximate execution pace
- Device orientation or placement
- Available modalities
- Notes about interruptions or data-quality issues

## Initial analysis goals

The first analysis stage will organize the collected files and explore:

- Spatial trajectory plots
- Position as a function of time
- Comparisons between intended and observed geometric shapes
- Visual and audio features related to the collection context

## Data policy

Raw videos, audio recordings, GPS traces, and participant-identifying data are
kept outside this repository unless explicit authorization for sharing is given.

## Open decisions

The exact collection protocol, number of repetitions, and final file structure
will be refined after an initial pilot collection.
