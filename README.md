# Tatanka Strength V12.0 - AI Program Generator 🤖

## What's New in V12.0

### 🎯 AI Program Generator
The biggest feature yet! Users can now generate fully customized 20-week workout programs using embedded AI.

**How it works:**
1. User clicks "Generate AI Workout Program" button in the Program tab
2. Enters their fitness goals (e.g., "build core and lower body strength for hockey season")
3. Selects experience level (Beginner/Intermediate/Advanced)
4. Chooses training days per week (2-6 days)
5. AI generates a complete custom program using your 50-exercise library
6. User previews the generated workouts
7. Can accept the program or regenerate with adjustments

### Technical Implementation

**Claude API Integration:**
- Uses the Anthropic Messages API directly from the browser
- No API key needed (handled backend in claude.ai artifacts)
- Model: `claude-sonnet-4-20250514`
- Structured JSON responses for workout programs

**Prompt Engineering:**
- Sends user goals, experience level, and training frequency
- Provides the complete 50-exercise library (exercises ONLY from your library)
- Enforces structured JSON output
- Includes periodization and progressive overload principles
- Balances muscle groups across the week

**Program Validation:**
- Validates JSON structure before accepting
- Ensures all exercises exist in library
- Checks for required fields (name, sets, reps, weight)
- Handles time-based exercises (Plank)

**User Experience:**
- Loading spinner during generation
- Error handling with user-friendly messages
- Preview before accepting
- Option to regenerate
- Saves to localStorage as custom program

### AI Prompt Structure

The prompt includes:
- User's fitness goals (free text)
- Experience level (beginner/intermediate/advanced)
- Training days per week (2-6)
- Complete exercise library (50 exercises)
- Sets/reps/weight guidelines based on experience
- 20-week progressive overload strategy
- Muscle group balance requirements

### Files Updated

**index.html (122 KB)**
- New AI Generator section in Program tab
- AI modal with input form
- Preview system for generated programs
- Loading states and error handling
- Complete Claude API integration

**sw.js (2.2 KB)**
- Updated cache version to v12.0

**manifest.json (428 B)**
- Updated description to include AI-powered feature

## All Features in V12.0

### 4 Main Tabs:

1. **🏋️ Workout Tab**
   - 20-week progressive program
   - Dial controls for sets/reps/weight
   - Workout A/B toggle
   - Uses custom AI-generated or manual programs

2. **📅 Calendar Tab**
   - Visual workout history
   - Log workouts to specific dates
   - Today indicator
   - Workout completion tracking

3. **📈 Progress Tab**
   - Custom goal tracking
   - Max efforts (last 90 days)
   - Personal records

4. **⚙️ Program Tab**
   - **NEW: AI Program Generator** 🤖
   - Manual program builder
   - 50-exercise library
   - CRUD operations (Create, Read, Update, Delete)
   - Reset to defaults

## Exercise Library (50 Exercises)

### Upper Body (20)
Bench Press, Tricep Pushdowns, Cable Chest Flys, Lateral Raises, Bicep Curls, Overhead Press, Pull-ups, Dips, Bent Over Rows, Face Pulls, Incline Bench Press, Decline Bench Press, Cable Curls, Hammer Curls, Skull Crushers, Chest Press Machine, Lat Pulldown, Seated Cable Row, Arnold Press, Shrugs

### Lower Body (20)
Back Squat, Lunges, Leg Extensions, Hamstring Curls, Box Jumps, Step-ups, Bulgarian Split Squat, Leg Press, Romanian Deadlift, Deadlift, Front Squat, Goblet Squat, Calf Raises, Hip Thrusts, Glute Bridges, Walking Lunges, Sumo Deadlift, Hack Squat, Sled Push, Farmer Carries

### Core (10)
Plank, Russian Twists, Ab Roll Outs, Push-ups, Hanging Leg Raises, Side Plank, Mountain Climbers, Cable Crunches, Bicycle Crunches, Dead Bug

## Data Storage

All data stored in localStorage:
- `workoutData` - Daily workout tracking
- `workoutHistory` - Completed workouts by date
- `customGoals` - User-defined goals
- `customProgram` - AI-generated or manually built programs

## How to Deploy

1. Upload all files to your GitHub repo
2. Enable GitHub Pages (Settings → Pages → Deploy from main branch)
3. Your app will be live at: `https://airfoil-agency.github.io/TatankaStrength`

## Files to Upload

- `index.html` (Main app file)
- `sw.js` (Service worker)
- `manifest.json` (PWA configuration)
- `icon-192.png` (App icon 192x192)
- `icon-512.png` (App icon 512x512)

## Technical Notes

- Progressive Web App (PWA)
- Works offline after first load
- Auto-updates when new version deployed
- Mobile-optimized responsive design
- No backend required
- AI calls work directly in browser (no CORS issues)

## User Privacy

- All workout data stored locally in browser
- No data sent to external servers (except AI generation API calls)
- AI prompts include only: goals, experience level, days/week
- No personal information in AI requests

## Future Enhancement Ideas

- Save multiple AI-generated programs
- Weekly program variations
- Deload weeks
- Exercise substitution suggestions
- Form videos/tutorials
- Social sharing
- Export to PDF

## Version History

- **V12.0** - AI Program Generator 🤖
- V11.0 - Program Builder with 50 exercises
- V10.0 - Custom goals tracking
- V9.0 - Max efforts tracking
- V8.0 - Calendar with workout logging
- V7.0 - Initial 20-week program

---

Built with ❤️ by Michael | Powered by Claude AI
