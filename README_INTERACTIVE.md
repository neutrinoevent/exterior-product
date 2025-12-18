# Interactive Exterior Product Visualization

**Live, real-time geometric algebra visualization in your browser!**

## 🚀 Try It Now

Simply open `index.html` in any modern browser - no installation needed!

## ✨ Features

### 🎯 Interactive Vector Manipulation
- **Drag endpoints** of vectors u and v with mouse or touch
- **Real-time updates** - bivector recalculates instantly
- **Smooth animations** - spinning orientation arrow at 60fps

### 🔄 Multiple Wedge Product Modes
Toggle between four modes:
- **u ∧ v** - Standard exterior product
- **v ∧ u** - Reversed order (shows anticommutativity)
- **-u ∧ v** - Negated first vector
- **-v ∧ u** - Negated second vector, reversed

### 📱 Mobile-Optimized
- Touch-enabled dragging
- Responsive design
- Fast performance on phones/tablets
- No dependencies - works offline!

### 🌀 Animated Orientation Arrow
- **Spins continuously** in the direction it indicates
- Clockwise (red) for negative orientation
- Counter-clockwise (blue) for positive orientation
- Visual representation of the bivector's "handedness"

## 🌐 Deploy to GitHub Pages

### Option 1: Quick Deploy
1. Create a new repository on GitHub
2. Upload `index.html` 
3. Go to Settings → Pages
4. Select branch: `main`, folder: `/` (root)
5. Save and wait ~1 minute
6. Visit: `https://yourusername.github.io/reponame/`

### Option 2: Using Git
```bash
# Create a new repo or clone existing one
git clone https://github.com/yourusername/geometric-algebra.git
cd geometric-algebra

# Copy index.html to the repo
cp index.html geometric-algebra/

# Commit and push
git add index.html
git commit -m "Add interactive exterior product visualization"
git push origin main

# Enable GitHub Pages in repo settings
```

### Option 3: Use Existing Repo
Just add `index.html` to any existing repo and GitHub Pages will serve it!

## 🎮 How to Use

### Basic Interaction
1. **Drag the endpoints** (small circles) of vectors u (orange) or v (blue)
2. Watch the **parallelogram update** in real-time
3. The **spinning arrow** shows the orientation
4. **Area and orientation** display in the info panel

### Mode Buttons
- Click any button to switch wedge product calculation
- Notice how **u ∧ v = -(v ∧ u)** (anticommutativity)
- Experiment with negated vectors to see sign changes

### Color Coding
- **Blue** = Positive orientation (CCW, right-handed)
- **Red** = Negative orientation (CW, left-handed)
- Orange = Vector u
- Dark blue = Vector v

## 🎓 Educational Use

Perfect for teaching:
- **Exterior algebra** fundamentals
- **Anticommutativity** of wedge product
- **Orientation** and handedness
- **Geometric interpretation** of bivectors

### Key Concepts Demonstrated

**1. The Exterior Product**
```
u ∧ v = oriented area element
```
The parallelogram represents the magnitude and orientation of the bivector.

**2. Anticommutativity**
```
v ∧ u = -(u ∧ v)
```
Switch modes to see the orientation flip!

**3. Linearity**
```
(-u) ∧ v = -(u ∧ v)
u ∧ (-v) = -(u ∧ v)
```
Negating either vector flips the orientation.

**4. Sign Interpretation**
- **Positive**: Counter-clockwise from u to v (shortest path)
- **Negative**: Clockwise from u to v

## 🛠️ Technical Details

### Technology Stack
- **Vanilla JavaScript** - No frameworks for maximum speed
- **HTML5 Canvas** - Hardware-accelerated 2D rendering
- **CSS3** - Modern, responsive styling
- **Touch Events** - Mobile compatibility

### Performance
- Runs at **60fps** on modern devices
- Single file (~15KB) - loads instantly
- No external dependencies
- Works offline after first load

### Browser Support
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari (Desktop & iOS)
- ✅ Mobile browsers (iOS Safari, Chrome Android)

## 🎨 Customization

### Adjust Vector Colors
Edit lines ~350-351:
```javascript
drawArrow(center.x, center.y, uCanvas.x, uCanvas.y, '#FF6B35', 4); // u color
drawArrow(center.x, center.y, vCanvas.x, vCanvas.y, '#004E89', 4); // v color
```

### Change Orientation Arrow Speed
Edit line ~337:
```javascript
const rotationSpeed = isPositive ? 0.02 : -0.02; // Increase for faster
```

### Modify Arrow Size
Edit line ~325:
```javascript
const arrowRadius = ... * 0.35; // Change 0.35 to adjust size
```

### Change Color Scheme
Edit lines ~292-295:
```javascript
const faceColor = isPositive ? 'rgba(123, 159, 212, 0.4)' : 'rgba(212, 123, 123, 0.4)';
const edgeColor = isPositive ? '#0066CC' : '#CC0000';
```

## 📊 Comparison with Python Animations

| Feature | Python (GIF) | HTML (Live) |
|---------|--------------|-------------|
| Interactivity | ❌ None | ✅ Full |
| Real-time | ❌ Pre-rendered | ✅ 60fps |
| Mobile | ⚠️ View only | ✅ Touch control |
| File size | 📦 Large GIFs | 🪶 15KB HTML |
| Deployment | ⚠️ Upload GIFs | ✅ GitHub Pages |
| Vector adjustment | ❌ Re-run script | ✅ Drag instantly |
| Learning curve | 📈 High | 📉 Click & drag |

## 🎯 Use Cases

### 1. Teaching & Presentations
- Project on screen during lectures
- Students can manipulate on their devices
- Instant visual feedback for exploration

### 2. Online Courses
- Embed in course websites
- Interactive homework problems
- Self-paced learning tool

### 3. Research Documentation
- Include in research papers (link to live demo)
- Supplement static figures
- Interactive supplements for publications

### 4. Personal Study
- Explore geometric algebra concepts
- Build intuition for wedge products
- Experiment with different vector configurations

## 🚧 Roadmap / Future Enhancements

Possible additions:
- [ ] 3D trivector visualization with WebGL
- [ ] Multiple bivector overlays
- [ ] Vector magnitude sliders
- [ ] Angle measurement display
- [ ] Export vector configurations
- [ ] Keyboard shortcuts
- [ ] Dark mode toggle
- [ ] Animation recording

## 📝 License

Free to use for educational purposes. Attribution appreciated!

## 🐛 Known Issues

**On very old mobile devices:**
- May run <60fps (still usable)
- Solution: Reduce arrow animation speed

**Safari iOS < 14:**
- Touch events may need polyfill
- Solution: Update iOS or use Chrome

## 🤝 Contributing

Feel free to:
- Report bugs via GitHub Issues
- Suggest features
- Submit pull requests
- Share your deployment!

## 📚 Learn More

- [Geometric Algebra Wikipedia](https://en.wikipedia.org/wiki/Geometric_algebra)
- [Exterior Algebra](https://en.wikipedia.org/wiki/Exterior_algebra)
- Hestenes, D. "New Foundations for Classical Mechanics"

---

**Made with ❤️ for geometric algebra enthusiasts everywhere!**

*Deploy once, interact forever - no server required!* 🚀
