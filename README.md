# 🎮 AGAMEZ.XYZ

Your personal gaming website! A dark, edgy game portal to showcase all the games you create.

## 🚀 Quick Start

### Deploying to GitHub Pages

1. **Create a GitHub account** (if you don't have one): https://github.com

2. **Create a new repository**:
   - Click the "+" button → "New repository"
   - Name it: `agamez.xyz` (or anything you want)
   - Make it **Public**
   - Click "Create repository"

3. **Upload your files**:
   - Click "uploading an existing file"
   - Drag and drop ALL the files from this folder (including the `games` folder)
   - Click "Commit changes"

4. **Enable GitHub Pages**:
   - Go to repository "Settings"
   - Click "Pages" in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Select "main" branch and "/ (root)" folder
   - Click "Save"

5. **Wait a minute**, then visit: `https://YOUR-USERNAME.github.io/agamez.xyz`

### Connecting Your Custom Domain (agamez.xyz)

1. In your GitHub repository, go to **Settings → Pages**

2. Under "Custom domain", type: `agamez.xyz` and click Save

3. In GoDaddy, go to your domain's DNS settings and add these records:
   - **A Record** → `@` → `185.199.108.153`
   - **A Record** → `@` → `185.199.109.153`
   - **A Record** → `@` → `185.199.110.153`
   - **A Record** → `@` → `185.199.111.153`
   - **CNAME Record** → `www` → `YOUR-USERNAME.github.io`

4. Wait 10-30 minutes for DNS to update

5. Check "Enforce HTTPS" in GitHub Pages settings

---

## 🎯 Adding New Games

### Step 1: Create Your Game

Create a new folder in the `games` directory:
```
games/
  └── my-new-game/
      ├── index.html    ← Your game file
      └── thumbnail.png ← Game thumbnail (300x200px recommended)
```

### Step 2: Add to the Games List

Open `index.html` and find the `games` array. Add your game:

```javascript
const games = [
    // ... existing games ...
    {
        id: 'my-new-game',           // Unique ID (no spaces)
        title: 'My New Game',         // Display name
        category: 'action',           // action, puzzle, arcade, or adventure
        thumbnail: 'games/my-new-game/thumbnail.png',
        plays: 0,
        isNew: true,                  // Shows "NEW" badge
        path: 'games/my-new-game/index.html'
    },
];
```

### Step 3: Commit and Push

Upload your new files to GitHub and your game will be live!

---

## 📁 File Structure

```
agamez.xyz/
├── index.html          ← Main website
├── README.md           ← This file
└── games/              ← All your games go here
    ├── space-dodge/    ← Sample game
    │   ├── index.html
    │   └── thumbnail.svg
    └── your-game/      ← Your games!
        ├── index.html
        └── thumbnail.png
```

---

## 🎨 Game Categories

- ⚔️ **action** - Fast-paced, combat, shooting games
- 🧩 **puzzle** - Brain teasers, matching, logic games
- 👾 **arcade** - Classic style, high score games
- 🗺️ **adventure** - Story-driven, exploration games

---

## 💡 Tips for Making Games

1. **Keep games simple** - Start with one mechanic and make it fun
2. **Use HTML5 Canvas** - Great for 2D games
3. **Test on mobile** - Many players use phones
4. **Add sound effects** - Makes games more engaging
5. **Save high scores** - Use localStorage

### Simple Game Template

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Game</title>
    <style>
        body {
            margin: 0;
            background: #0a0a0f;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        canvas {
            border: 2px solid #00f0ff;
            border-radius: 8px;
        }
    </style>
</head>
<body>
    <canvas id="game" width="600" height="400"></canvas>
    <script>
        const canvas = document.getElementById('game');
        const ctx = canvas.getContext('2d');
        
        // Your game code here!
        
        function gameLoop() {
            // Clear screen
            ctx.fillStyle = '#0a0a0f';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // Draw your game
            
            requestAnimationFrame(gameLoop);
        }
        
        gameLoop();
    </script>
</body>
</html>
```

---

## 🔧 Customization

### Change Colors
Edit the CSS variables in `index.html`:
```css
:root {
    --accent-cyan: #00f0ff;    /* Main accent color */
    --accent-purple: #b347ff;  /* Secondary accent */
    --accent-pink: #ff2d7a;    /* Highlight color */
    --accent-green: #39ff14;   /* Success color */
}
```

### Change Site Name
Search for "AGAMEZ" in `index.html` and replace with your name!

---

## ❓ Need Help?

- **GitHub Pages Docs**: https://docs.github.com/pages
- **HTML5 Game Tutorials**: https://developer.mozilla.org/en-US/docs/Games
- **Free Game Assets**: https://itch.io/game-assets/free

---

Made with 💜 for young game developers!
