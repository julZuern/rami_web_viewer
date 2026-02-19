# RAMI 4.0 Cube Visualization

An interactive 3D web application for visualizing and exploring the Reference Architecture Model for Industry 4.0 (RAMI 4.0) cube.

## Overview

RAMI 4.0 is a three-dimensional reference architecture model that provides a comprehensive framework for Industry 4.0 implementations. This visualization tool allows users to interactively explore the model's three dimensions:

- **Layers** (Y-axis): Six architectural layers from physical assets to business processes
- **Hierarchy Levels** (Z-axis): Seven levels from individual products to connected world systems
- **Life Cycle & Value Stream** (X-axis): Four phases divided into Type and Instance categories

## Features

### Interactive 3D Visualization
- **Rotate**: Left mouse button to rotate the cube
- **Zoom**: Mouse wheel to zoom in/out
- **Pan**: Right mouse button to pan the view
- **Click Selection**: Click any field or annotation to view detailed information

### Field Management
- **Select Fields**: Click on individual cube fields to highlight and view details
- **Occupied Fields List**: Track and manage fields relevant to your project
- **Add to Occupied**: Press Enter or click the "+ Add to Occupied" button
- **Remove Fields**: Click the × button next to any occupied field
- **Visual Indicators**: 
  - Green fields = Occupied
  - Blue fields = Currently selected
  - White/transparent = Empty fields
  - Vertical green lines = Show occupied field columns

### Keyboard Navigation
- **Arrow Keys**: Navigate between fields in the cube
- **Enter**: Add currently selected field to occupied list
- **Navigation adapts to camera angle** for intuitive control

### Import/Export
- **Export**: Copy occupied fields to clipboard as JSON
- **Import**: Load occupied fields from clipboard JSON
- Share configurations or save states for later use

### Transparency Controls
- **Layer-specific opacity**: Adjust individual layer transparency
- **Overall transparency**: Quickly adjust all layers together using ▲/▼ buttons
- Helps visualize internal structure and relationships

## RAMI 4.0 Model Details

### Layers (Architectural Dimensions)

1. **Asset**: Physical assets, hardware, and equipment
2. **Integration**: Integration technologies and interfaces
3. **Communication**: Communication protocols and networks
4. **Information**: Data models, information exchange, and semantics
5. **Functional**: Functions, processes, and business logic
6. **Business**: Business processes, workflows, and enterprise functions

### Hierarchy Levels (IEC 62264 / IEC 61512)

1. **Product**: Individual manufactured item or product type specification
2. **Field Device**: Sensors, actuators, and field-level devices
3. **Control Device**: PLCs, controllers, and control-level systems
4. **Station**: Work cells, production lines, or station-level systems
5. **Work Centers**: Shop floor areas or work center management systems
6. **Enterprise**: Plant-level or company-wide systems
7. **Connected World**: External systems, supply chain, and inter-enterprise connections

### Life Cycle & Value Stream (IEC 62890)

#### Type (Product Design & Procedures)
- **Development**: Research, design, and engineering of product types
- **Maintenance & Usage (Type)**: Operational procedures and usage guidelines for product designs

#### Instance (Physical Products)
- **Production**: Manufacturing and assembly of product instances
- **Maintenance & Usage (Instance)**: Operational maintenance and usage of manufactured products

## Technical Details

### Technologies Used
- **Three.js** (v0.153.0): 3D graphics library
- **OrbitControls**: Camera navigation
- **Vanilla JavaScript**: No additional frameworks required
- **HTML5 Canvas**: Text rendering for annotations

### Browser Requirements
- Modern web browser with WebGL support
- JavaScript enabled
- Clipboard API support for import/export (optional)

### File Structure
- `RAMI_webapp.html`: Complete standalone application
- `rami_webapp_config.json`: Configuration file (optional)
- `README.md`: This documentation

## Usage Guide

### Getting Started

1. **Open the Application**: Open `RAMI_webapp.html` in a web browser
2. **Explore the Cube**: Use mouse controls to rotate and examine the model
3. **Read Annotations**: Click on axis labels and layer names to see detailed descriptions
4. **Select Fields**: Click on cube fields to select them

### Working with Occupied Fields

1. **Select a field** by clicking on it in the 3D view
2. **Review field details** in the sidebar information panel
3. **Add to occupied list** by clicking "+ Add to Occupied" or pressing Enter
4. **Manage the list** by clicking items to select them or using × to remove
5. **Export your configuration** to save or share with collaborators
6. **Import configurations** to load previously saved states

### Best Practices

- **Start with transparency adjustments** to see internal structure
- **Use keyboard navigation** for precise field selection
- **Export regularly** to save your work
- **Click annotations** to understand each dimension before selecting fields
- **Adjust camera angle** before using arrow key navigation

## Export/Import Format

Occupied fields are exported as JSON in the following format:

```json
[
  {
    "layer": "Information",
    "hierarchy": "Control Device",
    "lifecycle": "Development"
  },
  {
    "layer": "Functional",
    "hierarchy": "Station",
    "lifecycle": "Production"
  }
]
```

This format is human-readable and can be easily edited in any text editor.

## Use Cases

- **Architecture Planning**: Model your Industry 4.0 architecture decisions
- **Documentation**: Visual representation of system components and their relationships
- **Communication**: Share architectural concepts with stakeholders
- **Analysis**: Identify gaps or overlaps in system coverage
- **Education**: Learn and teach RAMI 4.0 concepts interactively
- **Project Management**: Track implementation scope and progress

## Standards Compliance

This visualization is based on the following IEC standards:

- **IEC 62264**: Enterprise-control system integration (Hierarchy Levels)
- **IEC 61512**: Batch control (Hierarchy Levels)
- **IEC 62890**: Life-cycle management for systems and products (Life Cycle dimension)

## Limitations

- Client-side only (no server required, but no persistent storage)
- Export/import requires manual clipboard operations
- No multi-user collaboration features
- No undo/redo functionality (use export before major changes)

## Future Enhancements

Potential improvements for future versions:
- Local storage persistence
- Undo/redo functionality
- Field annotations and notes
- Color coding by project/category
- Connection lines between related fields
- Export to various formats (PDF, PNG, etc.)
- Comparison mode for different configurations

## License

This application is provided as-is for research and educational purposes.

## Support

For questions, issues, or contributions, please contact the project maintainer.

## Version History

- **Version 1.0**: Initial release with core visualization and field management features

---

**Note**: This is a research/educational tool. For production Industry 4.0 implementations, please consult with qualified systems architects and refer to the official IEC standards documentation.
