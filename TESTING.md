# How to Test the College Map Application

## Step-by-Step Testing Guide

### Step 1: Start a Local Web Server

**Option A: Using Python (Recommended)**
1. Open **Terminal** (Applications → Utilities → Terminal, or press `Cmd+Space` and type "Terminal")
2. Copy and paste these commands:

```bash
cd /Users/yanliu/Downloads/College-Map-main
python3 -m http.server 8000
```

3. You should see: `Serving HTTP on :: port 8000`

**Option B: Using VS Code Live Server**
1. Open VS Code
2. Install "Live Server" extension (if not installed)
3. Right-click on `index.html`
4. Select "Open with Live Server"

### Step 2: Open in Browser

Open your web browser and go to:
```
http://localhost:8000
```

Or if using Live Server, it will open automatically.

### Step 3: What You Should See

✅ **Immediately visible:**
- Map showing the United States
- Header with "U.S. College Map" logo
- Control panel with filters
- **Region dropdown** should show: All, Northeast, Midwest, South, West, Territories
- Loading indicator may appear briefly

✅ **After 1-2 seconds (when CSV loads):**
- College markers appear on the map
- **State dropdown** populates with all states
- **Type dropdown** populates with college types
- Legend shows count: "Showing X schools"
- Loading indicator disappears

### Step 4: Test Features

#### Test 1: Search
- Type in the search box (e.g., "Harvard")
- Wait ~300ms for results
- Map should filter to matching colleges

#### Test 2: Filters
- Select a **State** → colleges filter to that state
- Select a **Region** → colleges filter to that region  
- Select a **Type** → colleges filter to that type

#### Test 3: Radius Filter (NEW!)
1. Enter an address (e.g., "New York, NY")
2. Click "Set" or press Enter
3. **Should see:**
   - Red pin marker at that location
   - Blue dashed circle showing search radius
   - Only colleges within radius are visible
   - College popups show distance

#### Test 4: Marker Clustering
- Zoom out → markers cluster together
- Click cluster → expands to show individual colleges
- Zoom in → clusters break apart

#### Test 5: Error Handling
- Enter invalid address → red error message appears
- Error auto-dismisses after 5 seconds

### Troubleshooting

**Problem: Dropdowns are empty**
- Check browser console (F12 → Console tab)
- Make sure you're using `http://localhost:8000` not `file://`
- Check if CSV file exists: `ls colleges_usa_2024.csv`

**Problem: Map doesn't load**
- Check internet connection (needs it for map tiles)
- Check console for errors

**Problem: No markers appear**
- Open browser console (F12)
- Look for red error messages
- Check Network tab → is `colleges_usa_2024.csv` loading?

### Stop the Server

When done testing, go back to Terminal and press:
```
Ctrl + C
```

This stops the server.

