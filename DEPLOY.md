# 🚀 Deployment Guide - V11.0

## Files Ready to Upload

✅ **index.html** (56 KB) - Main app with all V11 features
✅ **sw.js** (1.1 KB) - Service worker for PWA
✅ **manifest.json** (455 B) - PWA configuration
✅ **README.md** (4.6 KB) - Documentation

## Quick Deploy to GitHub Pages

### Option 1: GitHub Web Interface (Easiest)

1. Go to: **https://github.com/airfoil-agency/TatankaStrength**

2. Click **"Add file"** → **"Upload files"**

3. Drag and drop these files:
   - `index.html`
   - `sw.js`
   - `manifest.json`

4. Commit message: **"V11.0 - Program Builder"**

5. Click **"Commit changes"**

6. Wait 1-2 minutes for deployment

7. Visit: **https://airfoil-agency.github.io/TatankaStrength**

### Option 2: Git Command Line

```bash
cd /path/to/TatankaStrength
git pull origin main
git add index.html sw.js manifest.json
git commit -m "V11.0 - Program Builder"
git push origin main
```

## What's in V11.0

### ✅ All Working Features:
- 20-week workout program (A & B)
- Dial controls for sets/reps/weight
- Calendar with workout logging
- Custom goal tracking
- Max efforts (90-day window)
- **Program Builder with 50 exercises**
- Full CRUD for custom workouts
- Exercise library (Upper/Lower/Core)
- Reset to defaults

### 🚫 Removed from Previous Version:
- AI Program Generator (authentication issues on GitHub Pages)
  - Will add back in future version with proper API setup

## Testing Checklist

After deployment:

- [ ] App loads at github.io URL
- [ ] Version shows "v11.0 - Program Builder"
- [ ] Workout tab displays exercises
- [ ] Dial controls work (click/drag)
- [ ] Calendar displays current month
- [ ] Can add custom goal
- [ ] Program tab shows Workout A & B
- [ ] Can add exercise from library
- [ ] Can edit exercise (sets/reps/weight)
- [ ] Can delete exercise
- [ ] Custom program saves after refresh

## Force Cache Update

If users still see old version:

**Desktop:**
- Windows: `Ctrl + Shift + R`
- Mac: `Cmd + Shift + R`

**Mobile:**
- Tap green "New version available" banner
- Or clear site data in browser settings

## Troubleshooting

**Problem:** Exercises not showing in Workout tab
**Solution:** Go to Program tab, make any small edit, go back to Workout

**Problem:** Calendar not updating
**Solution:** Change month back and forth

**Problem:** Goals not saving
**Solution:** Check browser localStorage is enabled

**Problem:** Service worker not updating
**Solution:** 
1. Open DevTools (F12)
2. Application tab → Service Workers
3. Click "Unregister"
4. Refresh page

## Next Steps

Once V11 is deployed and working:

1. **Test thoroughly** - Try all features
2. **Get user feedback** - See what people want most
3. **Plan V12** - Add AI generation with proper backend
4. **Consider additions**:
   - Workout C, D, E templates
   - Exercise reordering
   - Auto-progression
   - Rest timers

## Need Help?

- Check the README.md for full documentation
- Review index.html for any customizations
- Browser console (F12) will show any JavaScript errors

---

**Deployment time:** ~2 minutes
**Cache clear time:** Automatic (service worker)
**User action required:** None (or tap update banner)
