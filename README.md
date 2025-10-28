# Points-Visualization
Displaying points and their rotation in 3D space.

## Usage

Open `src/points-visualization.html` in a web browser and load a CSV file with point data.

## CSV Format

The input CSV file must contain the following columns:

```
name,p_x,p_y,p_z,r_x,r_y,r_z
```

- `name` - Point name/label
- `p_x`, `p_y`, `p_z` - Position coordinates (X, Y, Z)
- `r_x`, `r_y`, `r_z` - Rotation angles (degrees by default, or radians if enabled in UI)

Example:
```
name,p_x,p_y,p_z,r_x,r_y,r_z
Bod 1,10.0,0.0,0.0,0.0,0.0,0.0
Bod 2,0.0,10.0,0.0,90.0,0.0,0.0
```

See `example/example.csv` for a complete example.

## Controls

- **Left mouse button**: Rotate view
- **Right mouse button**: Pan view
- **Middle mouse button**: Select rotation pivot point (click on a point)
- **Mouse wheel**: Zoom
- **Checkbox options**: Toggle axes display, switch angle units, change rotation order
