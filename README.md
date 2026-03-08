# 🏍️ MOTO RUSH - Bike Racing Game

A fully functional motorcycle racing game built with HTML5 Canvas, CSS3, and vanilla JavaScript.

## 🎮 Game Features

### Core Gameplay
- **Controls**: Arrow keys for movement, Space for nitro boost
- **Objective**: Survive as long as possible, collect coins, avoid obstacles
- **Progressive Difficulty**: Game gets harder over time
- **Multiple Bikes**: Unlock faster bikes with better stats

### Game Systems
- ✅ Start Menu with multiple options
- ✅ Pause/Resume functionality (Press P)
- ✅ Game Over screen with detailed stats
- ✅ Score tracking system
- ✅ High score saved in localStorage
- ✅ Speed increases over time
- ✅ Mobile touch controls (auto-detected)
- ✅ Settings menu
- ✅ Instructions screen

### Advanced Features
- 🚀 **Nitro Boost System**: Press Space to activate speed boost
- ⛽ **Fuel Management**: Fuel drains when accelerating, collect fuel pickups
- 💰 **Coin Collection**: Collect coins to buy new bikes
- 🏪 **Bike Shop**: 4 different bikes with varying stats
- 📊 **HUD Display**: Real-time score, coins, speed, fuel, and nitro bars
- 🎨 **Particle Effects**: Visual boost effects
- 📱 **Responsive Design**: Works on desktop and mobile

### Obstacles
- 🚗 Cars
- 🪨 Rocks
- 🚧 Barriers

### Power-ups
- 💰 Coins (+10 points each)
- ⛽ Fuel Pickups (restore fuel)

## 🎯 How to Play

### Keyboard Controls
- **⬅️ LEFT ARROW** - Move to left lane
- **➡️ RIGHT ARROW** - Move to right lane
- **⬆️ UP ARROW** - Accelerate
- **⬇️ DOWN ARROW** - Brake
- **SPACE** - Activate nitro boost
- **P** - Pause game

### Mobile Controls
- Touch buttons appear automatically on mobile devices
- Can be toggled in Settings menu

### Gameplay Tips
1. **Manage Your Fuel**: Keep an eye on your fuel bar and collect fuel pickups
2. **Use Nitro Wisely**: Nitro regenerates slowly, use it strategically
3. **Collect Coins**: Save up to buy faster bikes in the shop
4. **Avoid Obstacles**: Any collision ends the game
5. **Stay Focused**: The game gets progressively harder

## 🏪 Bike Shop

### Available Bikes

| Bike | Speed | Acceleration | Price |
|------|-------|--------------|-------|
| Classic | 100% | 100% | Free |
| Sport | 120% | 110% | 500 coins |
| Racing | 150% | 130% | 1500 coins |
| Turbo | 180% | 150% | 3000 coins |

Coins persist between games, so keep playing to unlock better bikes!

## 🚀 Installation & Setup

### Option 1: Direct Play (Easiest)
1. Download all three files:
   - `index.html`
   - `style.css`
   - `game.js`
2. Place them in the same folder
3. Double-click `index.html` to open in your browser
4. Start playing!

### Option 2: Local Server (Recommended for Development)
1. Install [Node.js](https://nodejs.org/)
2. Install a simple HTTP server:
   ```bash
   npm install -g http-server
   ```
3. Navigate to the game folder:
   ```bash
   cd path/to/bike-game
   ```
4. Start the server:
   ```bash
   http-server
   ```
5. Open your browser to `http://localhost:8080`

### Option 3: Python Server
1. Navigate to the game folder in terminal
2. Run:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```
3. Open browser to `http://localhost:8000`

### Option 4: VS Code Live Server
1. Open the folder in VS Code
2. Install "Live Server" extension
3. Right-click `index.html` and select "Open with Live Server"

## 📁 File Structure

```
bike-game/
├── index.html          # Main HTML structure
├── style.css           # All styling and animations
├── game.js            # Complete game logic
└── README.md          # This file
```

## 🎨 Customization

### Modify Game Difficulty
Edit `CONFIG` object in `game.js`:
```javascript
const CONFIG = {
    initialSpeed: 3,        // Starting speed
    maxSpeed: 15,          // Maximum speed
    fuelDrainRate: 0.05,   // How fast fuel drains
    // ... more settings
};
```

### Change Colors
Modify CSS variables in `style.css`:
```css
.game-title {
    background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
}
```

### Add New Bikes
Add to `bikes` array in `game.js`:
```javascript
{
    id: 'super',
    name: 'Super Bike',
    icon: '🏍️',
    speed: 2.0,
    acceleration: 1.8,
    price: 5000,
    owned: false,
    selected: false,
}
```

## 🔧 Technical Details

### Technologies Used
- **HTML5 Canvas API**: For game rendering
- **CSS3**: Modern styling with gradients and animations
- **Vanilla JavaScript**: No frameworks or libraries
- **localStorage**: For saving game progress
- **requestAnimationFrame**: For smooth 60 FPS gameplay

### Performance
- Optimized rendering with requestAnimationFrame
- Efficient collision detection
- Minimal DOM manipulation during gameplay
- Smooth 60 FPS on most devices

### Browser Compatibility
- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers (iOS Safari, Chrome Android)

## 🎮 Game Mechanics

### Scoring System
- Distance traveled: +points per frame
- Coins collected: +10 points each
- Bonus for higher speeds

### Difficulty Scaling
- Obstacles spawn faster over time
- Maximum speed increases with distance
- Formula: `difficulty = 1 + distance / 5000`

### Collision Detection
- AABB (Axis-Aligned Bounding Box) collision
- 10px buffer for better gameplay feel

### Fuel System
- Drains when accelerating or boosting
- Game over when fuel reaches 0
- Restore with fuel pickups (+30%)

### Nitro System
- Drains when Space is held
- Regenerates when not in use
- Provides significant speed boost

## 🐛 Known Issues & Limitations

1. **Sound Effects**: Placeholder audio elements included but not implemented (requires audio files)
2. **Mobile Landscape**: Best played in portrait mode on mobile
3. **Save Data**: Clearing browser cache will reset progress

## 🔮 Future Enhancements

Potential features to add:
- [ ] Sound effects and background music
- [ ] Multiple game modes (time trial, endless, etc.)
- [ ] Leaderboard system
- [ ] More obstacle types
- [ ] Weather effects
- [ ] Different road environments
- [ ] Multiplayer support
- [ ] Achievements system

## 📝 License

This game is provided as-is for educational and entertainment purposes.
Feel free to modify and use for personal projects.

## 🙋 Support

If you encounter any issues:
1. Make sure all three files are in the same folder
2. Check browser console for errors (F12)
3. Try a different browser
4. Clear browser cache and reload

## 🎉 Credits

- **Game Design & Development**: Professional game engine with modern web technologies
- **Graphics**: Canvas-based procedural graphics
- **Inspiration**: Classic arcade racing games

---

**Enjoy the game! Race safely and collect those coins! 🏍️💨**
