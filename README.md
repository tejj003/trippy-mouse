# Interactive Data Visualization

A beautiful, interactive particle system that responds to mouse movement with real-time parameter adjustments and visual effects.

![Interactive Data Visualization Demo](https://img.shields.io/badge/Status-Active-brightgreen)

## Features

- **Real-time Mouse Interaction**: Control particle behavior by moving your mouse across the canvas
- **Dynamic Parameters**: 6 different parameters that change based on mouse position
- **Shape Morphing**: Click to cycle through 4 different particle shapes (Circle, Square, Triangle, Star)
- **Responsive Design**: Clean, modern UI with tooltips and parameter displays
- **Smooth Animations**: 60fps particle system with glow effects and connecting lines
- **Dark Theme**: Sophisticated textured background with glassmorphism UI elements

## Controls

### Mouse Controls
- **Horizontal Movement (Left-Right)**: 
  - Controls particle count (50-250 particles)
  - Controls speed multiplier (0.2x - 3x speed)
- **Vertical Movement (Up-Down)**:
  - Controls attraction force (magnetic pull strength)
  - Controls color hue (0-360 degrees)
  - Controls size scale (particle sizing)

### Click Controls
- **Canvas Click**: Cycle through particle shapes (Circle → Square → Triangle → Star → Circle)

### Keyboard Controls
- **ESC**: General escape functionality

## Parameters

| Parameter | Range | Description |
|-----------|-------|-------------|
| **Particle Count** | 50-250 | Number of particles rendered on screen |
| **Speed Multiplier** | 0.2x-3x | Movement speed of all particles |
| **Attraction Force** | 0-2 | Strength of magnetic pull toward mouse |
| **Color Hue** | 0-360° | Base color for particle gradient system |
| **Size Scale** | 0.5-1.5 | Size multiplier for all particles |
| **Shape** | 4 types | Current particle shape (Circle/Square/Triangle/Star) |

## Technical Details

### Built With
- **HTML5 Canvas** - For high-performance particle rendering
- **Vanilla JavaScript** - No external dependencies
- **CSS3** - Modern styling with backdrop filters and gradients
- **DM Sans Font** - Clean, modern typography from Google Fonts

### Performance Features
- **Optimized Rendering**: 60fps animation loop with efficient particle management
- **Dynamic Particle Management**: Particles are added/removed based on count parameter
- **Trail Effects**: Subtle trail rendering for enhanced visual appeal
- **Connection Lines**: Dynamic lines between nearby particles
- **Glow Effects**: Real-time shadow blur effects for each particle

### Browser Compatibility
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## File Structure

```
trippy-mouse/
├── index.html          # Main application file
├── README.md           # Project documentation
└── css/                # CSS files (if modularized)
    └── styles.css      # Main stylesheet
└── js/                 # JavaScript files (if modularized)
    └── main.js         # Main application logic
```

## Getting Started

1. **Clone or Download** the project files
2. **Open** `index.html` in a modern web browser
3. **Move your mouse** over the canvas to see the interactive effects
4. **Click** on the canvas to change particle shapes
5. **Hover** over parameter labels to see helpful tooltips

## Customization

### Colors
Modify the HSL color values in the particle drawing function to change the color scheme:
```javascript
ctx.fillStyle = `hsl(${hue}, 70%, 60%)`;
```

### Particle Behavior
Adjust physics parameters in the `Particle.update()` method:
- `force` calculation for attraction strength
- `damping` value (0.99) for movement decay
- `boundary` behavior for edge collisions

### Canvas Size
Change canvas dimensions in the HTML:
```html
<canvas id="canvas" width="1380" height="700"></canvas>
```

## Development

### Local Development
No build process required - simply open `index.html` in your browser.

### Adding New Shapes
Add new cases to the `drawShape()` method in the Particle class:
```javascript
case 4: // New shape
    // Your drawing code here
    break;
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- Particle physics inspiration from various web-based particle systems
- UI design influenced by modern glassmorphism trends
- Font: DM Sans by Google Fonts

---

**Enjoy exploring the interactive particle universe!** 🌟
