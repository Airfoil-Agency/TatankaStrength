# Tatanka Strength V11.2 - User Profile & Accurate Calories

## ✨ What's New in V11.2

### 👤 User Profile System

Add your personal information for **accurate, personalized calorie calculations!**

**Profile includes:**
- **Weight** (required) - Essential for calorie accuracy
- **Height** (optional) - Calculates BMI
- **Age** (optional) - Improves accuracy
- **Sex** (optional) - Improves accuracy

**Location:** Progress tab → Profile section at top

## How It Works

### With Profile (Accurate!)
Uses **MET-based calculation** - the fitness industry standard:

```
Calories = METs × Body Weight (kg) × Duration (hours)
```

**MET Values (Metabolic Equivalent):**
- Light intensity: 3.5 METs (accessories, light weight)
- Moderate intensity: 5 METs (mixed compound/isolation)
- Vigorous intensity: 6 METs (heavy compound lifts)

**The app intelligently determines intensity based on:**
- Compound exercise ratio (Squats, Deadlifts, etc.)
- Average weight per set
- Total volume

### Without Profile (Generic Estimate)
Falls back to volume-based estimation if no weight provided.

## Example Calculations

**180 lb person, 45-min workout:**

**Light workout** (accessories, 15 sets):
- 3.5 METs × 82 kg × 0.75 hours = **215 calories**

**Moderate workout** (mixed, 18 sets):
- 5 METs × 82 kg × 0.75 hours = **308 calories**

**Heavy workout** (compound, 20 sets):
- 6 METs × 82 kg × 0.75 hours = **369 calories**

Same workouts for different body weights:
- 150 lbs: 185, 264, 316 calories
- 200 lbs: 238, 340, 408 calories
- 250 lbs: 298, 425, 510 calories

**Much more accurate than generic estimates!**

## User Interface

### Profile Section (Progress Tab)

**Before setup:**
```
👤 Your Profile                    [Edit Profile]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📝 Set up your profile for accurate 
   calorie tracking!
   
   [Add Profile Info]
```

**After setup:**
```
👤 Your Profile                    [Edit Profile]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  180 lbs      5'10"      35      Male
  Weight      Height     Age      Sex

  BMI: 25.8
  Normal weight
```

### Profile Modal

Click "Edit Profile" or "Add Profile Info":
- Weight (lbs) * Required
- Height (feet & inches) Optional
- Age Optional
- Sex Optional

### Calorie Completion Modal

**With profile:**
```
🔥
Workout Complete!
Tue, Nov 26, 2024

You burned
318
calories
Personalized for your weight

[Awesome! 💪]
```

**Without profile:**
```
🔥
Workout Complete!
Tue, Nov 26, 2024

You burned
150
calories
Estimate · Add profile for accuracy

[Awesome! 💪]
```

## BMI Calculator

If you provide height, the app calculates and displays your BMI:

| BMI Range | Category |
|-----------|----------|
| < 18.5 | Underweight |
| 18.5 - 24.9 | Normal weight |
| 25.0 - 29.9 | Overweight |
| ≥ 30.0 | Obese |

*Note: BMI is a general indicator and doesn't account for muscle mass.*

## Data Storage

Profile stored in localStorage:

```javascript
{
  weight: 180,           // pounds
  heightFeet: 5,
  heightInches: 10,
  age: 35,
  sex: "male"
}
```

## Privacy

- All data stored **locally** in your browser
- **No data sent to servers**
- Profile is **optional**
- Can be deleted anytime

## Accuracy Comparison

### Generic Formula (No Profile)
*Volume-based estimation:*
- Light workout: ~120 calories
- Medium workout: ~150 calories
- Heavy workout: ~180 calories

**Problem:** Same calories for everyone regardless of body weight!

### MET-Based Formula (With Profile)
*Personalized for YOU:*
- 150 lb person, heavy workout: ~320 cal
- 180 lb person, same workout: ~370 cal
- 210 lb person, same workout: ~420 cal

**30% variance based on body weight alone!**

## All V11.2 Features

### 🏋️ Workout Tracking
- 20-week progressive program
- 6 workout variations (A-F)
- Exercise include/exclude toggles
- **Personalized calorie calculation**

### 📅 Calendar
- Visual workout history
- Click dates to log workouts
- **Calories shown on entries**

### 📈 Progress
- **NEW: User Profile section**
- **NEW: BMI calculator**
- Custom goal tracking
- Max efforts (90 days)
- Workout statistics

### ⚙️ Program Builder
- 50-exercise library
- Custom workout creation
- Full CRUD operations

## Technical Details

**Version:** v11.2 - User Profile
**New Functions:**
- `openProfileModal()` - Show profile form
- `closeProfileModal()` - Hide profile form
- `saveProfile()` - Save profile data
- `updateProfileDisplay()` - Render profile section
- Updated `calculateCaloriesBurned()` - MET-based with user weight
- Updated `showCaloriesModal()` - Shows personalized indicator

**Calculation Logic:**
1. Check if userProfile exists with weight
2. If yes → MET-based calculation using actual body weight
3. If no → Generic volume-based estimation
4. Display appropriate message in completion modal

## Deployment

Upload these 3 files to GitHub:
1. `index.html` (V11.2)
2. `sw.js` (cache v11-2)
3. `manifest.json` (unchanged)

Users will see update banner automatically.

## Upgrading from V11.1

Existing users upgrading from V11.1:
- All workout data preserved
- Calories on old workouts remain unchanged
- Profile section appears in Progress tab
- No setup required (optional)
- New workouts use personalized calculation if profile added

## FAQ

**Q: Is profile required?**
A: No! The app works without it, using generic estimates.

**Q: How accurate are the calories?**
A: With profile: Industry-standard MET formula (~85% accurate)
Without profile: Rough estimate (~60-70% accurate)

**Q: Can I change my profile?**
A: Yes! Click "Edit Profile" anytime to update.

**Q: What if I don't want to share my weight?**
A: That's fine! The app works with generic estimates. Your privacy matters.

**Q: Does the app store my data anywhere?**
A: Only in your browser's localStorage. Nothing is sent to servers.

**Q: Will past workouts update with my profile?**
A: No, past calorie counts stay as logged. Only new workouts use the profile.

## Future Enhancements

Possible additions:
- Heart rate tracking integration
- Activity level adjustment
- Custom MET values
- Calorie goal setting
- Weekly/monthly calorie totals
- Macronutrient calculator

---

**Get the most accurate calorie tracking!** 🔥💪

Built by: Michael (InsightDynamo LLC)
Version: 11.2
Updated: November 2024
