# Tatanka Strength V11.0 - Program Builder

## Current Version: V11.0

A complete 20-week strength training Progressive Web App with customizable workout programs.

**Live App:** https://airfoil-agency.github.io/TatankaStrength

## Features

### 🏋️ Workout Tracking
- 20-week progressive program (Workouts A & B)
- Interactive dial controls for sets, reps, and weight
- Real-time workout data tracking
- Supports custom programs

### 📅 Calendar
- Visual workout history
- Log workouts to specific dates
- See which days you trained
- Today indicator
- Monthly view navigation

### 📈 Progress Tracking
- **Custom Goals** - Track any lift or movement
  - Set target and current weights
  - View progress percentage
  - Multiple goals supported
- **Max Efforts** (Last 90 Days)
  - Automatic tracking from workout history
  - See your personal records
  - Sorted by weight

### ⚙️ Program Builder
Build completely custom workout programs!

**50-Exercise Library:**
- Upper Body (20): Bench Press, Pull-ups, Rows, Curls, etc.
- Lower Body (20): Squats, Deadlifts, Lunges, etc.
- Core (10): Planks, Russian Twists, etc.

**Full CRUD Functionality:**
- ✅ **Create** - Add exercises to Workout A or B
- ✅ **Read** - View your custom program
- ✅ **Update** - Edit sets, reps, and weights
- ✅ **Delete** - Remove exercises
- ✅ **Reset** - Restore default program

**Smart Features:**
- Category filtering (Upper/Lower/Core)
- Time-based exercises (Plank in seconds)
- All workouts saved to localStorage
- Program persists across sessions

## Default Program

**Workout A (Upper Body Focus):**
- Bench Press: 3×10 @ 135 lbs
- Tricep Pushdowns: 3×12 @ 50 lbs
- Cable Chest Flys: 3×12 @ 30 lbs
- Lateral Raises: 3×12 @ 15 lbs

**Workout B (Lower Body Focus):**
- Back Squat: 3×10 @ 185 lbs
- Lunges: 3×10 @ 30 lbs
- Leg Extensions: 3×12 @ 70 lbs
- Plank: 3×60 sec

## Data Storage

Everything stored locally in your browser:
- `workoutData` - Your daily workout tracking
- `workoutHistory` - Completed workouts by date
- `customGoals` - Your fitness goals
- `customProgram` - Your custom workout program

**No account required. No data sent to servers.**

## How to Use

### Track a Workout
1. Select your week (1-20)
2. Choose Workout A or B
3. Adjust sets/reps/weight using dials or +/- buttons
4. Complete your workout

### Build Custom Program
1. Go to Program tab (⚙️)
2. Click "+ Add Exercise" on Workout A or B
3. Filter by category (Upper/Lower/Core)
4. Select exercise from library
5. Edit sets/reps/weight as needed
6. Delete exercises you don't want
7. Your custom program automatically syncs to Workout tab

### Log Workouts
1. Go to Calendar tab (📅)
2. Tap any day
3. Click "Log Today's Workout"
4. Your current workout data is saved

### Track Goals
1. Go to Progress tab (📈)
2. Click "+ Add New Goal"
3. Enter exercise name, target, and current weight
4. Track progress over time

## Technical Details

- **Type:** Progressive Web App (PWA)
- **Works Offline:** Yes (after first load)
- **Auto-Updates:** Yes (via service worker)
- **Mobile-Optimized:** iPhone/Android responsive
- **No Backend Required:** 100% client-side

## Installation

### As PWA (Recommended)
iPhone: Safari → Share → Add to Home Screen
Android: Chrome → Menu → Install App

### GitHub Pages Deployment
1. Fork or clone repo
2. Upload files to your repo
3. Enable GitHub Pages (Settings → Pages)
4. Deploy from main branch

## File Structure

```
├── index.html (113 KB) - Main app
├── sw.js (1.1 KB) - Service worker
├── manifest.json - PWA config
├── icon-192.png - App icon (192x192)
└── icon-512.png - App icon (512x512)
```

## Browser Support

- Chrome/Edge (recommended)
- Safari (iOS 13+)
- Firefox
- Samsung Internet

## Version History

- **V11.0** - Program Builder with 50-exercise library
- V10.0 - Custom goal tracking
- V9.0 - Max efforts tracking (90 days)
- V8.0 - Calendar with workout logging
- V7.0 - Initial 20-week program

## Upcoming Features (Planned)

- Workout C, D, E (5-6 day splits)
- Exercise reordering (drag & drop)
- Pre-made program templates
- Auto-progression rules
- Rest timer between sets
- Exercise demo videos
- Dark mode
- Export workout data

## Development

Built by: Michael (InsightDynamo LLC)
Tech: Vanilla JavaScript, localStorage, Service Workers
PWA Framework: None - pure HTML/CSS/JS

## License

Free to use. Attribution appreciated but not required.

---

**Need Help?**
Check the app's tooltips or create an issue on GitHub.

**Want AI Program Generation?**
That feature is in development and will require API authentication. Stay tuned for V12!
