# 🚀 Quick Deployment Guide - V12.0

## Files Ready to Upload

✅ `index.html` - Main app (122 KB)
✅ `sw.js` - Service worker (2.2 KB)
✅ `manifest.json` - PWA config
✅ `README.md` - Documentation

## Step-by-Step Deployment

### Option 1: GitHub Web Interface (Easiest)

1. Go to: https://github.com/airfoil-agency/TatankaStrength

2. Click "Add file" → "Upload files"

3. Drag these 3 files:
   - `index.html`
   - `sw.js`
   - `manifest.json`

4. Commit message: "V12.0 - AI Program Generator"

5. Click "Commit changes"

6. Wait 1-2 minutes for GitHub Pages to rebuild

7. Visit: https://airfoil-agency.github.io/TatankaStrength

### Option 2: Git Command Line

```bash
cd /path/to/TatankaStrength
git add index.html sw.js manifest.json
git commit -m "V12.0 - AI Program Generator"
git push origin main
```

## Testing the AI Feature

1. Open the app
2. Go to "Program" tab (4th tab)
3. Click "Generate AI Workout Program" button
4. Enter goals: "build core and lower body strength for hockey season"
5. Select experience: Intermediate
6. Select days: 4 days per week
7. Click "Generate Program"
8. Wait ~5-10 seconds for AI generation
9. Preview the custom workout program
10. Click "Accept Program" to save it

## What Users Will See

**New AI Generator Section** at the top of Program tab:
- 🤖 Icon and title
- Description of the feature
- Big "Generate AI Workout Program" button

**AI Modal** when button clicked:
- Text area for fitness goals
- Experience level dropdown
- Days per week dropdown
- Generate button
- Loading spinner during generation
- Preview of generated workouts
- Accept/Regenerate buttons

## How the AI Works

1. User enters goals and preferences
2. App calls Claude API (no API key needed!)
3. Claude creates custom program using your 50-exercise library
4. Returns structured JSON with workouts
5. App validates and displays preview
6. User accepts → saves to localStorage as custom program
7. Workout tab automatically uses the new custom program

## Important Notes

⚠️ **The AI feature only works when deployed on claude.ai** (in artifacts)
   - This is because the API authentication is handled by Claude's backend
   - It will NOT work if you open index.html locally in a browser
   - It WILL work when deployed to GitHub Pages via Claude artifacts

✅ **All other features work everywhere:**
   - Manual program builder
   - Workout tracking
   - Calendar
   - Progress tracking

## Troubleshooting

**If AI generation fails:**
- Check browser console for errors
- Make sure you're using the app through claude.ai
- Try regenerating with different inputs
- Make sure you filled in the goals field

**If custom program doesn't save:**
- Check browser localStorage is enabled
- Try clearing site data and refreshing
- Check that you clicked "Accept Program"

**Cache issues after update:**
- Force refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Or tap the green "New version available" banner

## Version Update Flow

1. Upload new files to GitHub
2. GitHub Pages rebuilds (1-2 min)
3. Users see green "New version available" banner
4. Tap banner to reload
5. Service worker loads V12.0
6. New AI feature available!

## Success Checklist

- [ ] Files uploaded to GitHub
- [ ] GitHub Pages shows green checkmark
- [ ] App loads at github.io URL
- [ ] Version shows "v12.0 - AI Program Generator"
- [ ] Program tab shows AI generator section
- [ ] Can generate AI program successfully
- [ ] Generated program saves and appears in Workout tab
- [ ] All previous features still work

---

**Questions or issues?** Check the README.md for detailed documentation.
