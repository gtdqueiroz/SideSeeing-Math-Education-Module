# SideSeeing project update — October 12, 2026

We collected 13 SideSeeing recordings for the math education module. The recordings cover circular and triangular paths, spins in place, and phone tilt tests. These setups give us known movements and orientations to compare with the phone's sensor readings.

## Recordings

| Setup | Recordings |
| --- | --- |
| Circular paths | Three circles with different radii |
| Spins in place | Three spins at slow, moderate, and fast speeds |
| Triangular path | The same path traversed at two speeds |
| Phone tilt | Two trials, labeled `inclinacao_mao` and `inclinacao_braco` |
| Fixed phone orientations | Three trials, labeled `angulo_fixo_qualquer`, `angulo_fixo_reto`, and `angulo_fixo_celular_horizontal` |

The recordings are stored in Google Drive under `ROTAS-E-TESTES/ROTAS-12-10-2026`. Each recording folder uses the dataset reference timestamp followed by a descriptive label, such as `2026-10-12-13-56-50-859_pirueta_lenta`.

## Exploration notebook

We added [`rotas_iamai_teste.ipynb`](../rotas_iamai_teste.ipynb) to load and explore one recording at a time. In Google Colab, set `PASTA_COLETAS_DRIVE` to your copy of the data folder, run the first code cell, and select a recording with `INDICE_ROTA`. The notebook discovers recordings by looking for `sensors.three.csv` and reads the other supported CSVs and `metadata.json` when available.

The notebook reports the sample count and typical sampling rate for each sensor. It plots the three axes of the accelerometer, linear acceleration, gravity, and gyroscope signals when available. It also plots the angle between a selected phone axis and the recorded gravity vector. When the metadata includes the video start time, the notebook computes approximate video-relative timestamps for the sensor readings.

## Planned analyses

- **Spins in place.** Compare the measured radial acceleration with the squared angular speed during steady portions of the three spins. For a roughly constant radius, the expected relationship is $a_r = r\omega^2$.
- **Circular paths.** Use the measured radius and lap time to estimate walking speed and compare the expected turning rate with the gyroscope signal when the phone follows the direction of travel.
- **Triangular path.** Use the video to mark the turns. Compare the peak angular velocity and the total angle turned at each corner across the two walking speeds.
- **Tilt and fixed orientations.** Use the fixed-orientation recordings to check the angle reference and sign. Explore whether the pole recording can support a height estimate by identifying when the camera points at the top and estimating the horizontal distance and camera height relative to the base.
