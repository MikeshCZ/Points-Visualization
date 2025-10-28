# Points-Visualization

Interactive 3D visualization tool for displaying points and their rotations in 3D space.

**[LIVE DEMO](https://mikesh.tech/points-visualization.html)**

## Features

- **Interactive 3D Scene**: Rotate, pan, and zoom to explore your data
- **Flexible CSV Import**: Load point data with positions (required) and rotations (optional)
- **Rotation Visualization**: Display axes for each point showing their orientation
- **Bilingual Interface**: Switch between Czech and English 🇬🇧/🇨🇿
- **Customizable Display**: Point size, axes size/opacity, individual axis visibility and flip
- **Multiple Rotation Orders**: XYZ, XZY, YXZ, YZX, ZXY, ZYX
- **Angle Units**: Degrees or radians
- **Dark/Light Mode**: Choose your preferred color scheme
- **Pivot Point Selection**: Click on any point to center rotation
- **Smooth Animations**: Camera transitions and visual feedback

## Quick Start

1. Open `src/points-visualization.html` in a web browser
2. Click Load Data panel
3. Select your CSV file
4. Interact with the 3D scene

No installation or build process required!

## CSV Format

**Required columns:**
```csv
name,p_x,p_y,p_z
```

**Optional columns (rotation):**
```csv
r_x,r_y,r_z
```

**Example:**
```csv
name,p_x,p_y,p_z,r_x,r_y,r_z
Point 1,10.0,0.0,0.0,0.0,0.0,0.0
Point 2,0.0,10.0,0.0,90.0,0.0,0.0
Point 3,0.0,0.0,10.0,0.0,0.0,45.0
```

See `example/example.csv` for reference.

### File Validation

The application validates:
- File type (must be .csv)
- File size (max 10MB)
- Required columns presence
- Numeric value formats
- Displays clear error messages for invalid data

## Controls

- **Left mouse**: Rotate view
- **Right mouse**: Pan view
- **Middle mouse**: Select pivot point (click point or empty space for world center)
- **Mouse wheel**: Zoom

## Technology

- **Three.js** (r128): 3D rendering library
- **OrbitControls**: Camera control system
- Pure HTML/CSS/JavaScript - no build process required
- Self-contained single file with CDN dependencies

## Performance Optimizations

The application includes several performance optimizations:

- **Throttled Mouse Tracking**: Raycasting limited to ~60fps for smooth performance
- **Efficient Material Updates**: Axes opacity updates without recreating geometry
- **Smart Rendering**: Only updates what's necessary when settings change
- **Optimized Code**: Reduced code duplication and improved maintainability

## License

See [LICENSE](LICENSE) file for details.