# Tatanka Strength V11.3 - Program Wizard

## ✨ What's New in V11.3

### 🧙‍♂️ Program Wizard Feature

A complete guided wizard that helps users find the perfect workout program based on their goals, schedule, and experience!

**How it works:**
1. Answer 5 simple questions
2. Get 2-3 personalized program recommendations
3. Preview full program details
4. Select and load instantly into your tracker

**No AI needed** - All programs are pre-built, high-quality, curated templates that load instantly and work offline!

## The 4 Core Programs

### 1. Full Body Strength (3 days/week)
- **Focus:** Compound movements, balanced development
- **Best for:** Beginners to advanced, general strength
- **Workouts:** A, B, C
- **Duration:** ~60 minutes
- **Sample Day A:**
  - Back Squat 4×8
  - Bench Press 4×8
  - Barbell Rows 3×10
  - Overhead Press 3×8
  - Romanian Deadlift 3×8
  - Plank 3×60s

### 2. Push/Pull/Legs Split (6 days/week)
- **Focus:** Bodybuilding-style split, muscle mass
- **Best for:** Intermediate to advanced, hypertrophy goals
- **Workouts:** A (Push), B (Pull), C (Legs), D (Push), E (Pull), F (Legs)
- **Duration:** ~60 minutes
- **Sample Day A (Push):**
  - Bench Press 4×8
  - Incline DB Press 3×10
  - Overhead Press 3×8
  - Tricep Pushdowns 3×12
  - Lateral Raises 3×15
  - Pec Flys 3×12

### 3. Upper Body Focus (3 days/week)
- **Focus:** Chest, back, shoulders, arms emphasis
- **Best for:** Upper body strength/mass goals
- **Workouts:** A (Chest/Triceps), B (Back/Biceps), C (Shoulders/Arms)
- **Duration:** ~60 minutes
- **Sample Day A:**
  - Bench Press 4×8
  - Incline DB Press 3×10
  - Pec Flys 3×12
  - Close-Grip Bench 3×8
  - Tricep Pushdowns 3×12
  - Dips 3×10

### 4. Lower Body Focus (3 days/week)
- **Focus:** Legs, glutes, posterior chain
- **Best for:** Lower body strength, athletic performance
- **Workouts:** A (Squat), B (Deadlift), C (Power/Conditioning)
- **Duration:** ~60 minutes
- **Sample Day A:**
  - Back Squat 5×5
  - Front Squat 3×8
  - Bulgarian Split Squat 3×10
  - Leg Extensions 3×12
  - Calf Raises 4×15
  - Plank 3×60s

## The Wizard Flow

### Step 1: Goals (select all that apply)
- Build upper body strength
- Build lower body strength
- Build core strength
- Improve athletic performance
- Gain muscle mass (hypertrophy)
- Lose body fat
- General fitness / maintenance

### Step 2: Training Frequency
- 2 days per week
- 3 days per week
- 4 days per week
- 5 days per week
- 6 days per week

### Step 3: Session Length
- 30-45 minutes (short, efficient)
- 45-60 minutes (standard)
- 60-90 minutes (comprehensive)
- 90+ minutes (extensive)

### Step 4: Experience Level
- Beginner (< 1 year)
- Intermediate (1-3 years)
- Advanced (3+ years)

### Step 5: Equipment Access
- Full commercial gym
- Home gym (barbell, dumbbells, rack)
- Minimal equipment (dumbbells only)
- Bodyweight only

## Matching Algorithm

Programs are scored based on:
- **Frequency match** (+30 points exact, +15 for ±1 day)
- **Duration match** (+20 points within 15 min, +10 within 30 min)
- **Goals alignment** (+10 points per matched goal)
- **Equipment compatibility** (+20 points)
- **Experience fit** (+10 points)

Top 3 matches shown, best match highlighted with ⭐ badge.

## Weight Selection Guidance (RPE)

### "Reps in Reserve" Method

**For every exercise: Choose weights where you have 2-3 reps left in reserve on your last set**

**Example: Bench Press (3 sets × 10 reps)**

✅ **Just Right:**
- Sets 1-2: Moderate effort, complete easily
- Set 3: Reps 8-10 are challenging, could do 2-3 more

❌ **Too Light:**
- All sets feel easy
- Could do 15+ reps

❌ **Too Heavy:**
- Struggling to complete 10 reps
- Form breaks down

**Why it works:**
Leaving 2-3 reps in reserve ensures you're working hard enough to build strength while avoiding failure that could compromise form or lead to injury.

### Where RPE Guidance Appears

1. **Education Modal** (shown after program selection)
   - Full explanation with examples
   - Visual good/bad examples
   - "Got it! 💪" button

2. **Exercise Cards** (during workouts)
   - Yellow banner under each exercise
   - "💡 Choose weight for 2-3 reps in reserve"
   - Constant reminder

3. **Preview Modal**
   - RPE guidance shown before accepting
   - "Learn more" link to education modal

## Medical Disclaimer

### When It Shows
- **After program selection** (before loading)
- User clicks "I Understand" to proceed
- Then sees RPE education modal
- Then program loads into tracker

### Always Accessible
- Footer link on every page
- Click "⚠️ Disclaimer" to view anytime

### Disclaimer Content
- Consult physician before starting
- Especially important if: age 40+, medical conditions, etc.
- Not medical advice
- Assumption of risk
- Stop if experiencing: chest pain, dizziness, etc.

## User Experience Flow

### Complete Journey

1. **User clicks** "Start Program Wizard ✨"
2. **Answers 5 questions** (step-by-step with back/next navigation)
3. **Sees results** (2-3 matched programs with scores)
4. **Previews program** (full workout breakdown)
5. **Selects program** (clicks "Accept Program")
6. **Reads disclaimer** (clicks "I Understand")
7. **Learns RPE method** (weight selection education)
8. **Program loads** into tracker
9. **Starts workout** (with RPE guidance on each exercise)

**Total time: 2-3 minutes from start to first workout!**

## Technical Features

### Pre-Built Programs Structure
```javascript
{
  name: "Program Name",
  description: "Short description",
  frequency: 3,              // Days per week
  duration: 60,              // Minutes per session
  goals: ['upper', 'lower'], // Matched goals
  equipment: ['full', 'home'], // Compatible equipment
  experience: ['beginner', 'intermediate', 'advanced'],
  workouts: ['A', 'B', 'C'], // Workout days
  rpeGuidance: "2-3 reps in reserve",
  program: {
    A: [
      { name: "Exercise", sets: "4x8", reps: 8 }
    ]
  }
}
```

### Integration with Existing App
- Loads seamlessly into 20-week program structure
- Updates week/day selectors dynamically
- Preserves all existing features
- User profile still used for calories
- Progress tracking continues normally

### Wizard State Management
```javascript
wizardAnswers = {
  goals: ['upper', 'hypertrophy'],
  frequency: 6,
  duration: 60,
  experience: 'intermediate',
  equipment: 'full'
}
```

## All V11.3 Features

### 🧙‍♂️ Program Wizard (NEW)
- 5-step questionnaire
- 4 curated programs
- Matching algorithm
- Preview system
- RPE education
- Medical disclaimer

### 👤 User Profile (V11.2)
- Weight, height, age, sex
- BMI calculator
- Personalized calories

### 🔥 Calorie Tracking (V11.1)
- MET-based calculation
- Modal after completion
- History tracking

### 🏋️ Workout Tracking
- 20-week progressive program
- 6 workout variations
- Exercise toggles
- Workout notes

### 📅 Calendar
- Visual history
- Date selection for logging
- Calories displayed

### 📈 Progress
- Profile section
- Custom goals
- Max efforts (90 days)
- Workout statistics

### ⚙️ Program Builder
- 50-exercise library
- Custom workouts
- Full CRUD operations
- **NEW: Wizard button**

## Files Changed

**index.html** - Main app
- Program Wizard button and UI
- 4 additional modals (Results, Preview, RPE, Disclaimer)
- Wizard JavaScript functions (~400 lines)
- 4 pre-built program templates
- RPE guidance on exercise cards
- Footer with disclaimer link
- Version updated to v11.3

**sw.js** - Service worker
- Cache version: v11-3

**manifest.json** - Unchanged

## Deployment

Upload these 3 files to GitHub:
1. `index.html` (V11.3 with Program Wizard)
2. `sw.js` (cache v11-3)
3. `manifest.json` (unchanged)

Users will see update banner automatically.

## What's NOT in This Version

**Coming in future versions:**
- 4 additional programs (8 total):
  - Powerlifting (4 days)
  - Athletic Performance (4 days)
  - Hypertrophy (5 days)
  - General Fitness (2-3 days)
- Auto-calculated weights from current maxes
- Weekly progression built into programs
- More granular equipment filters

**This is the simplified V11.3** - 4 core programs to test the concept!

## Testing Checklist

1. ✅ Click "Start Program Wizard ✨"
2. ✅ Answer all 5 questions (try different combinations)
3. ✅ See results with 2-3 programs
4. ✅ Preview a program (full details shown)
5. ✅ Select a program
6. ✅ Read disclaimer modal
7. ✅ See RPE education modal
8. ✅ Program loads into tracker
9. ✅ Week/Day selectors updated correctly
10. ✅ Exercises show RPE guidance banners
11. ✅ Complete a workout (calories still work)
12. ✅ Check calendar (workout logged)
13. ✅ Click footer "Disclaimer" link
14. ✅ Test on mobile (responsive)

## Browser Compatibility

- Chrome/Edge ✅
- Safari (iOS/Mac) ✅
- Firefox ✅
- Samsung Internet ✅

## Future Enhancements

**V11.4 ideas:**
- Add 4 more programs
- Program comparison view
- Save favorite programs
- Program history
- Share programs
- Custom program creation wizard

---

**The wizard is ready!** Test it thoroughly and let me know what needs adjusting! 🧙‍♂️💪

Built by: Michael (InsightDynamo LLC)
Version: 11.3
Updated: November 2024
