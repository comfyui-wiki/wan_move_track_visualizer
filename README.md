# WanMove Track Visualizer

A visual track editor and workflow generator for ComfyUI's WanMove model - an interactive HTML tool that allows you to create, edit, and visualize motion trajectories with real-time preview and export capabilities.

## 🌟 Features

### Visual Track Editing
- **Interactive Canvas**: Draw and edit trajectories directly on a visual canvas
- **Multi-Track Support**: Create and manage multiple independent tracks with different parameters
- **Real-time Preview**: See trajectory changes instantly with directional arrows
- **Drag-and-Drop Control Points**: 
  - Red dots: Start points
  - Green dots: End points  
  - Orange dots: Bezier control points (when enabled)
  - Purple dots: Track spread control points (NEW!)

### Advanced Track Parameters
- **Bezier Curves**: Create smooth curved trajectories with customizable control points
- **Interpolation Modes**: Linear, ease-in, ease-out, ease-in-out, constant
- **Track Spread**: Visual spread adjustment with interactive drag controls
- **Frame Count**: Configurable number of frames (1-1024)
- **Track Count**: Multiple parallel tracks per trajectory (1-100)

### Image Background Support
- **Image Upload**: Drag & drop or upload background images
- **Smart Scaling**: Multiple scaling modes (fit, fill, crop) with real-time preview
- **Canvas Resizing**: Dynamic canvas size adjustment to match image dimensions

### Export Capabilities
- **Track Coordinates**: Export in `track_coords` format for `WanMoveTracksFromCoords` node
- **ComfyUI Workflow**: Generate complete workflow JSON with proper node linking
- **Real-time Updates**: Export data automatically updates as you edit
- **File Download**: Save exports as `.json` files

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- ComfyUI with WanMove extension installed

### Installation
1. Clone or download this repository
2. Open `index.html` in your web browser
3. Start creating trajectories!

### Basic Usage
1. **Create Tracks**: Use the track management panel to add/remove tracks
2. **Edit Parameters**: Adjust start/end points, bezier curves, and timing
3. **Visual Editing**: Drag control points directly on the canvas
4. **Adjust Spread**: Drag purple spread control points to modify track width
5. **Export**: Generate track coordinates or complete ComfyUI workflows

## 🎯 ComfyUI Integration

### Supported Nodes
- **GenerateTracks**: Primary trajectory generation node
- **WanMoveConcatTrack**: Multi-track concatenation
- **WanMoveTracksFromCoords**: Import from coordinate data

### Export Formats

#### Track Coordinates Format
```json
[
  [
    {"x": 100, "y": 200},
    {"x": 150, "y": 250},
    ...
  ]
]
```

#### ComfyUI Workflow Format
Complete workflow JSON with:
- GenerateTracks nodes for each visible track
- WanMoveConcatTrack nodes for multi-track combinations
- Proper node linking and parameter mapping

## 🎨 Interface Overview

### Canvas Area
- **Main Canvas**: Interactive drawing area with background image support
- **Control Points**: Visual manipulation handles for trajectory parameters
- **Track Visualization**: Color-coded tracks with directional arrows
- **Track Labels**: Click to select and switch between tracks

### Control Panel
- **Track Management**: Add, remove, and configure individual tracks
- **Parameter Controls**: Sliders and inputs for all trajectory parameters
- **Image Controls**: Upload and scaling options for background images
- **Export Section**: Generate and download various formats

### Track-Specific Parameters
- **Start/End Points**: Normalized coordinates (0-1)
- **Bezier Control**: Optional curved trajectory support
- **Interpolation**: Motion timing and easing options
- **Track Spread**: Width of parallel track distribution
- **Frame/Track Counts**: Temporal and spatial resolution

## 🛠️ Technical Details

### Architecture
- **Pure HTML/CSS/JavaScript**: No external dependencies
- **Canvas 2D API**: High-performance rendering
- **Real-time Processing**: Immediate visual feedback
- **Responsive Design**: Adapts to different screen sizes

### Coordinate System
- **Normalized Coordinates**: All positions stored as 0-1 values
- **Pixel Conversion**: Automatic scaling to canvas dimensions
- **ComfyUI Compatible**: Direct integration with WanMove nodes

### File Structure
```
wantrack_visualizer/
├── track_visualizer.html    # Main application
├── data.json               # Sample workflow (basic)
├── data2.json             # Sample workflow (with links)
└── README.md              # This file
```

## 🎮 Controls & Shortcuts

### Mouse Controls
- **Left Click**: Select tracks, drag control points
- **Drag**: Move start/end/bezier/spread control points
- **Track Labels**: Click to switch active track

### Visual Indicators
- **Red Circles**: Start points (draggable)
- **Green Circles**: End points (draggable)
- **Orange Circles**: Bezier control points (when enabled)
- **Purple Circles**: Track spread controls (NEW!)
- **Dashed Lines**: Bezier control lines and spread indicators
- **Arrows**: Trajectory direction indicators

## 🔧 Advanced Features

### Multi-Track Workflows
- Create complex motion patterns with multiple trajectory groups
- Automatic workflow generation with proper node concatenation
- Independent parameter control for each track group

### Real-Time Export Updates
- Export data automatically refreshes as you edit
- Seamless switching between coordinate and workflow exports
- Instant file download with appropriate naming

### Visual Spread Control
- Interactive purple control points for track spread adjustment
- Visual feedback showing track width distribution
- Synchronized with parameter sliders

## 🐛 Troubleshooting

### Common Issues
- **Purple spread controls not visible**: Increase track spread value or regenerate tracks
- **Export data empty**: Ensure at least one track is visible and generated
- **Image not loading**: Check file format (supports JPG, PNG, GIF)

### Performance Tips
- Keep frame counts reasonable (< 200) for smooth interaction
- Use fewer tracks for complex trajectories
- Clear unused tracks to improve performance

## 🤝 Contributing

This tool is designed to complement ComfyUI's WanMove extension. Feel free to:
- Report issues or bugs
- Suggest new features
- Submit improvements
- Share usage examples

## 📄 License

This project is provided as-is for use with ComfyUI and the WanMove model.

## 🙏 Acknowledgments

- **WanMove**: Original model and ComfyUI integration
- **ComfyUI**: Node-based UI framework
- **Community**: Feedback and feature suggestions

---

**Happy Trajectory Creating!** 🎬✨