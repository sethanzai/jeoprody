# Jeopardy Game - OMIYA TAGALOG

An interactive Jeopardy-style game designed for the OMIYA TAGALOG community. Features include team scoring, a timer, and music playback for sing-along questions.

## Features

- **5 Categories** with 5 difficulty levels ($100–$500) each
- **Team Scoring**: Red and Blue teams compete
- **Timer**: 30-second countdown per question
- **Sing-Along Category**: Plays corresponding hymn/song files (AWIT) when questions are selected
- **Responsive Design**: Works on desktop and tablet displays

## Categories

1. **Sino ako?** - "Who am I?" biblical figures
2. **IMITATE THEIR FAITH** - Stories of faith and courage
3. **UMAWIT NG MASAYA** - Sing-along songs (plays audio files)
4. **BIBLE QUOTES** - Famous scripture passages
5. **JW/NUMBER** - Numbers and facts

## Files

- `jeopardy.html` - Main game file (single-file application)
- `songs/` - Audio files for sing-along questions
  - `046.mp3` - AWIT 46
  - `040.mp3` - AWIT 40
  - `038.mp3` - AWIT 38
  - `132.mp3` - AWIT 132
  - `140.mp3` - AWIT 140

## How to Play

1. Open `jeopardy.html` in any modern web browser
2. Click on a dollar amount to see the question
3. Click "Show Answer" to reveal the answer
4. One team member selects which team answered correctly (Red or Blue)
5. For sing-along questions, a "Play Song" button will appear to control audio playback
6. Click "Back to Main Screen" to continue playing

## Setup & Hosting

### Local Play
- Simply open `jeopardy.html` directly in your browser, or
- Serve via a local web server:
  ```bash
  python3 -m http.server 8000
  ```
  Then visit `http://localhost:8000`

### GitHub Pages Hosting

1. Create a new repository on GitHub (e.g., `omiya-jeopardy`)
2. Clone it locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/omiya-jeopardy.git
   cd omiya-jeopardy
   ```
3. Copy the contents of this folder into the repository
4. Commit and push:
   ```bash
   git add .
   git commit -m "Initial commit: Jeopardy game"
   git push -u origin main
   ```
5. Enable GitHub Pages:
   - Go to repository **Settings** → **Pages**
   - Under "Source", select `main` branch and `/root` folder
   - Save and wait ~1 minute for deployment
   - Your game will be live at `https://YOUR_USERNAME.github.io/omiya-jeopardy/`

## Browser Requirements

- Modern browser with HTML5 audio support
- JavaScript enabled
- Recommended: Chrome, Firefox, Safari, Edge (latest versions)

## Notes

- The game is a single HTML file with embedded CSV data—no backend server required
- All audio files must be in the `songs/` folder relative to `jeopardy.html`
- Timer shows "Time's up!" when countdown reaches zero
- Answered questions are marked and cannot be clicked again

## Customization

To add more questions or categories, edit the CSV data inside the `<script>` tag in `jeopardy.html`.

Format:
```
Category,Question,Answer,Value
Your Category,Your question here?,Answer text,100
```

---

Enjoy the game! 🎉
