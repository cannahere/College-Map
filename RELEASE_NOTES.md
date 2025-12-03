# Release Notes

## Release 4 (v4) - Performance Optimizations, SEO Updates, and UX Improvements

**Release Date**: December 2024  
**Previous Release**: v3.0.0 (Route search, guidance bubbles, mobile refinements)

### Summary Statistics
- **Files changed**: 3 files
- **Total changes**: +6,853 insertions, -3,663 deletions
- **Commits**: 28 commits between v3.0.0 and v4

---

### Major Features & Improvements

#### 1. **Saved Colleges Feature**
- ✅ Saved Colleges overlay with search, save/unsave functionality
- ✅ Saved Only mode filtering
- ✅ Notice for Saved Only mode with zero saved colleges
- ✅ Empty state messages and overlay improvements
- ✅ **NEW: Enhanced "Map Saved Only" Toggle Rules (4 Rules)**
  - Rule 1: Prevents toggle ON when user has 0 saved colleges (with helpful hint)
  - Rule 2: Prevents toggle ON when no saved colleges match current filters/context (nearby/route/explore)
  - Rule 3: Auto-turns OFF toggle when SavedStore becomes empty after unsave
  - Rule 4: Auto-turns OFF toggle when last visible saved college is removed
- ✅ **NEW: Teaching Moment** - One-time hint when user reaches 2 saved colleges
- ✅ **NEW: Filter Change Detection** - Auto-turns OFF toggle when filters exclude all saved colleges
- ✅ **NEW: Enhanced Hint System** - All hints auto-dismiss after 5-8 seconds, previous hints close when new ones appear

#### 2. **Performance Optimizations**
- ✅ Saved only toggle performance (deferred rendering with `requestAnimationFrame`)
- ✅ Mobile marker click performance (DOM caching, deferred UI updates)
- ✅ Dynamic marker sizing for mobile/iPad (blue dots and saved icons scale with zoom)
- ✅ **NEW: Route Filter Optimization** - Skip distance recalculation when only saved-only filter changes

#### 3. **Visual & UX Enhancements**
- ✅ Route styling: royal blue route line with navy outline
- ✅ Refined start/end route pins (white circle start, red teardrop end)
- ✅ Dynamic route line styling by zoom level (weight and opacity adjust)
- ✅ Mobile/iPad tap highlight changed from orange to white
- ✅ Tooltip/popup mutual exclusivity (tooltips hide when popups open)
- ✅ **NEW: Route Planner Modal Overlay**
  - Centered modal (replaced sliding panel)
  - Dynamic college count in header ("N college stops on this route")
  - Colleges sorted by distance from starting address
  - Google Maps integration with waypoints
  - Improved UI with reduced padding

#### 4. **SEO & Content Updates**
- ✅ Updated SEO meta tags (title, description, keywords)
- ✅ Open Graph and Twitter Card tags
- ✅ Schema.org structured data (WebApplication, WebSite, BreadcrumbList)
- ✅ Updated H1 tag
- ✅ Updated "About This Map" section content

#### 5. **Analytics & Tracking**
- ✅ GA4 event tracking for high-level features:
  - `feature_saved_used` - fired whenever a user saves or unsaves a college
  - `feature_saved_list_opened` - fired when the Saved List overlay is opened
  - `feature_saved_only_toggled` - fired whenever the Saved Only toggle changes
  - `feature_nearby_used` - fired when a Nearby search successfully completes
  - `feature_route_used` - fired when a Route search successfully completes
  - `feature_filter_type_used` - fired whenever the Type dropdown value changes
  - `feature_filter_region_used` - fired whenever the Region dropdown value changes
  - `feature_filter_state_used` - fired whenever the State dropdown value changes

#### 6. **Form & Autofill Improvements**
- ✅ Strengthened autofill prevention for address fields (all devices)
- ✅ Enhanced state dropdown protection against autofill
- ✅ Continuous monitoring and faster checks

#### 7. **Other Updates**
- ✅ Bing Webmaster Tools verification
- ✅ Favicon links
- ✅ College data updates (CSV file changes)

---

### Key Technical Improvements

- **Performance**: Deferred rendering, DOM caching, optimized marker creation
- **Mobile/Tablet**: Dynamic sizing, improved tap targets, better visual feedback
- **Code Quality**: Better separation of concerns, improved event handling

---

### Comparison with Release 3

**Release 3 (v3.0.0)** focused on:
- Route search functionality
- Guidance bubbles
- Mobile refinements

**Release 4 (v4)** builds on Release 3 with:
- Major performance optimizations
- Comprehensive SEO improvements
- Enhanced user experience features
- Saved colleges functionality
- Better mobile/tablet support

---

## Release 3 (v3.0.0) - Route Search, Guidance Bubbles, Mobile Refinements

**Release Date**: Previous release  
**Tag**: v3.0.0

### Features
- Route search functionality
- Guidance bubbles
- Mobile refinements

---

## Release 2 (v2.0-phase2-complete)

**Tag**: v2.0-phase2-complete

---







