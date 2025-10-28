# Points-Visualization

Interactive 3D visualization tool for displaying points and their rotations in 3D space using Three.js.

## Features

- **Interactive 3D Scene**: Rotate, pan, and zoom to explore your data
- **CSV Data Import**: Load point data with positions and rotations from CSV files
- **Rotation Visualization**: Display axes for each point showing their orientation
- **Bilingual Interface**: Switch between Czech (default) and English with a single click 🇬🇧/🇨🇿
- **Customizable Display**:
  - Adjust point size (5-50 pixels)
  - Configure axes size (10-200) and opacity (0-1)
  - Toggle individual axis visibility (X/Y/Z)
  - Flip individual axes by 180°
- **Multiple Rotation Orders**: Support for XYZ, XZY, YXZ, YZX, ZXY, ZYX
- **Angle Units**: Switch between degrees and radians
- **Dark/Light Mode**: Choose your preferred color scheme
- **Pivot Point Selection**: Click on any point to make it the center of rotation
- **Label Display**: Show/hide point names
- **Smooth Animations**: Animated camera transitions and visual feedback

## Usage

1. Open `src/points-visualization.html` in a web browser
2. Click on the "Načíst data" (Load Data) panel
3. Select a CSV file with your point data
4. Interact with the 3D scene using mouse controls

No installation, build process, or server required - just open the HTML file!

- **[LIVE DEMO](https://mikesh.tech/points-visualization.html)**

## CSV Format

The input CSV file must contain the following columns:

```
name,p_x,p_y,p_z,r_x,r_y,r_z
```

- `name` - Point name/label
- `p_x`, `p_y`, `p_z` - Position coordinates (X, Y, Z)
- `r_x`, `r_y`, `r_z` - Rotation angles (degrees by default, or radians if enabled in UI)

Example:

```csv
name,p_x,p_y,p_z,r_x,r_y,r_z
Bod 1,10.0,0.0,0.0,0.0,0.0,0.0
Bod 2,0.0,10.0,0.0,90.0,0.0,0.0
Bod 3,0.0,0.0,10.0,0.0,0.0,45.0
```

See `example/example.csv` for a complete example.

## Controls

### Mouse Controls

- **Left mouse button**: Rotate view around pivot point
- **Right mouse button**: Pan view
- **Middle mouse button**: Select rotation pivot point
  - Click on a point to center rotation on that point
  - Click on empty space to center on world origin [0, 0, 0]
- **Mouse wheel**: Zoom in/out

### Display Options Panel

**Language:**

- Click the flag icon (🇬🇧/🇨🇿) to switch between Czech and English

**Visualization:**

- Toggle axes display for all points
- Toggle label display for all points
- Dark/light mode toggle

**Rotation Settings:**

- Angle units: Degrees (default) or Radians
- Rotation order: XYZ, XZY, YXZ, YZX, ZXY, ZYX

**Appearance:**

- Point size slider (5-50)
- Axes size slider (10-200)
- Axes opacity slider (0-1)

**Axis Control:**

- Individual axis visibility (X/Y/Z)
- Individual axis flip (180° rotation)

## Technology

- **Three.js** (r128): 3D rendering library
- **OrbitControls**: Camera control system
- Pure HTML/CSS/JavaScript - no build process required
- Self-contained single file with CDN dependencies