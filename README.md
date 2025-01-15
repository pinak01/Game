# 3D Maze Game

A 3D maze game built with JavaScript using raycasting techniques, designed to run in Scribble (a JavaScript notebook environment).

## 🎮 Demo Controls

- **↑**: Move forward
- **↓**: Move backward
- **←**: Strafe left
- **→**: Strafe right
- **A**: Rotate view left
- **D**: Rotate view right

## 🚀 Getting Started

### Prerequisites
```
- Scribble (JavaScript notebook)
- Modern web browser with HTML5 Canvas support
```

### Installation
```javascript
// 1. Create a new notebook in Scribble
// 2. Copy the game code into a cell
// 3. Run the cell
```

## 🏗️ Code Structure

### Player Class
```javascript
class Player {
    constructor(x, y, dir, options) {
        this.x = x;
        this.y = y;
        this.dir = dir;
        this.color = options ? (options.color ? options.color : defaultColor) : defaultColor;
    }
    // ... movement methods
}
```

### Game Class
```javascript
class Game {
    constructor(width, height, rows, cols) {
        this.width = width;
        this.height = height;
        this.cols = cols;
        this.rows = rows;
        // ... initialization
    }
    // ... game methods
}
```

## 🗺️ Maze Configuration

### Wall Definition Format
```javascript
[y1, x1, y2, x2] // Coordinates for start and end points
```

### Example Map Structure
```javascript
const outerWalls = [
    [5, 5, 5, 95],    // Left wall
    [5, 95, 95, 95],  // Bottom wall
    [95, 95, 95, 5],  // Right wall
    [95, 5, 5, 5]     // Top wall
];
```

## 🛠️ Customization

### Modifying the Maze
```javascript
function setMap() {
    // Add your wall configurations here
    const lines = [
        [y1, x1, y2, x2],
        // ... more walls
    ];
}
```

### Changing Colors
```javascript
const defaultColor = { r: 255, g: 12, b: 100 };
```

## ⚡ Performance

### Game Loop
```javascript
function gameLoop() {
    draw();
    if (looping) {
        requestAnimationFrame(gameLoop);
    }
}
```

### Optimization
- Movement stops after 2s of inactivity
- Uses requestAnimationFrame for smooth rendering
- Efficient raycasting calculations

## 🐛 Common Issues

### Blank Screen
```javascript
// Check canvas initialization
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
```

### Movement Problems
```javascript
// Verify event listeners
document.addEventListener('keydown', (event) => {
    // ... movement code
});
```

## 📚 Resources

### Documentation
- Canvas API: https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
- Raycasting: https://lodev.org/cgtutor/raycasting.html

### Support
Create an issue in the repository for:
- Bug reports
- Feature requests
- General questions

## 📝 License

This project is open source and available under the MIT License.
