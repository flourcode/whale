# 🐋 Whale Tracker - Product Requirements Document

## Project Overview

**Product Name:** Whale Hello - Ocean Giants Tracker  
**Project Type:** Weekend Experiment → Useful Tool  
**Target Users:** Anyone who likes whales, marine biology enthusiasts, developers looking for simple examples  
**Primary Goal:** Make whale tracking accessible and fun without requiring a PhD in marine biology or computer science

## The "Why" Behind This

I wanted to build something that tracks whales because whales are cool. That's it. No market research, no user personas, no business model. Sometimes you just want to see where the whales are.

**Secondary Goals:**
- Prove that useful apps don't need complex tech stacks
- Show that AI tools can help non-developers build real things
- Create something people might actually use and enjoy
- Provide a code example others can fork and customize

## Core Features (MVP)

### 🗺️ Interactive Whale Map
**What:** Real-time map showing whale sightings worldwide  
**Why:** Visual representation is more engaging than data tables  
**Data Source:** GBIF (Global Biodiversity Information Facility) API  

**Requirements:**
- Display whale sightings as animated markers on a world map
- Use ocean-themed map tiles for immersion
- Show most recent sightings (2025 data)
- Handle up to 450+ data points without performance issues
- Mobile-responsive map controls

**Success Criteria:**
- Map loads within 3 seconds on mobile
- Markers are clearly visible and interactive
- No lag when panning/zooming

### 📱 Mobile-First Experience
**What:** Touch-optimized interface that works better on phones than desktop  
**Why:** Most people will discover this on mobile, desktop is secondary  

**Requirements:**
- Bottom navigation that doesn't interfere with map interaction
- Full-screen whale details on mobile (modals)
- Desktop gets hover popups instead
- Safe area handling for newer iPhones
- Touch-friendly button sizes (minimum 44px target area)

**Success Criteria:**
- Usable with one thumb on a phone
- No accidental map panning when using controls
- Readable text without zooming

### 🔍 Species Filtering
**What:** Filter visible whales by species type  
**Why:** Users might want to focus on specific whales they're interested in  

**Requirements:**
- Toggle individual species on/off
- Real-time map updates when filters change
- Visual indicators showing which filters are active
- Preserve filter state during session

**Success Criteria:**
- Filtering feels instant (< 200ms)
- Clear visual feedback for active filters
- Easy to reset to "show all"

### 🐋 Whale Information
**What:** Educational content about each whale species  
**Why:** People are curious and want to learn  

**Requirements:**
- Species identification with common names
- Brief habitat and behavioral facts
- Sighting metadata (date, location, coordinates)
- Emoji representations for visual appeal

**Success Criteria:**
- Information is accurate and interesting
- Readable without scientific background
- Quick to consume (under 30 seconds)

## Technical Requirements

### Technology Constraints
**Must Use:**
- Pure HTML, CSS, JavaScript (no frameworks)
- Single-file deployment option
- Free APIs only
- GitHub Pages compatible

**Cannot Use:**
- Node.js, React, Vue, etc.
- Paid APIs or services
- Build tools or compilation steps
- Server-side processing

**Why These Constraints:**
- Maximum accessibility for non-developers
- Zero deployment complexity
- Easy to understand and modify
- Minimal ongoing costs

### Performance Requirements
- **Initial Load:** < 3 seconds on 3G mobile
- **Data Refresh:** < 2 seconds for new whale data
- **Map Interaction:** 60fps on modern mobile devices
- **Memory Usage:** < 50MB total footprint

### Browser Support
- **Primary:** Mobile Safari, Chrome Android (latest 2 versions)
- **Secondary:** Desktop Chrome, Firefox, Edge (latest 2 versions)
- **Not Supported:** Internet Explorer (it's 2025, come on)

### Data Requirements
- **Species Coverage:** Minimum 8 whale species
- **Geographic Scope:** Worldwide coverage
- **Data Freshness:** 2025 sightings only
- **Record Limit:** 50 records per species (performance balance)

## User Experience Requirements

### Core User Flows

**Discovery Flow:**
1. User arrives at app (probably on mobile)
2. Loading screen with friendly whale animation
3. Map appears with whale markers visible
4. User taps a whale to learn more

**Exploration Flow:**
1. User wants to see specific whale types
2. Taps "Filter" button
3. Selects/deselects species
4. Map updates in real-time
5. User explores filtered results

**Learning Flow:**
1. User is curious about a specific whale
2. Taps whale marker
3. Gets full-screen information modal (mobile) or popup (desktop)
4. Reads facts and sighting details
5. Closes modal and explores more

### Usability Requirements
- **Zero Learning Curve:** Should be obvious how to use
- **Forgiving Interface:** No destructive actions, easy to undo
- **Progressive Disclosure:** Basic info first, details on demand
- **Consistent Behavior:** Same interactions work the same everywhere

## Design Requirements

### Visual Design Principles
- **Ocean Theme:** Blues, teals, ocean-inspired colors
- **Playful but Professional:** Fun enough for kids, useful for adults
- **High Contrast:** Readable in bright sunlight (mobile usage)
- **Minimal Text:** Icons and visuals over lengthy descriptions

### Animation & Interaction
- **Subtle Animations:** Enhance without distracting
- **Loading States:** Always show progress for async operations
- **Hover Effects:** Desktop gets hover states, mobile gets tap feedback
- **Performance First:** No animation that drops frames

### Mobile-Specific Design
- **Bottom Navigation:** Thumb-friendly placement
- **Large Touch Targets:** Minimum 44px for interactive elements
- **Full-Screen Modals:** Better than tiny popups on small screens
- **Safe Areas:** Handle iPhone notches and home indicators

## Success Metrics

### Usage Metrics
- **Engagement:** Average session duration > 2 minutes
- **Exploration:** Users view details for multiple whales per session
- **Retention:** Users return within a week
- **Technical:** < 5% error rate for data loading

### Feedback Metrics
- **GitHub Stars:** Measure developer interest
- **Forks:** Measure reuse and customization
- **Issues/Questions:** Indicate engagement level
- **Social Sharing:** Natural virality

### Learning Metrics (Personal)
- **Code Quality:** Other developers can understand and modify
- **Documentation:** Clear enough for non-developers to use
- **Maintainability:** Can add features without rewriting

## Risk Assessment

### Technical Risks
- **API Reliability:** GBIF might be slow or unavailable
  - *Mitigation:* Graceful error handling, offline fallbacks
- **Data Quality:** Whale sighting data might be inconsistent
  - *Mitigation:* Data validation and filtering
- **Mobile Performance:** Maps can be resource-intensive
  - *Mitigation:* Marker limits, efficient rendering

### User Experience Risks
- **Complexity Creep:** Adding too many features
  - *Mitigation:* Stick to core use cases, resist feature requests
- **Mobile Usability:** Map interactions on small screens
  - *Mitigation:* Extensive mobile testing, separate mobile UI
- **Information Overload:** Too much data overwhelming users
  - *Mitigation:* Progressive disclosure, clear hierarchy

### Business/Project Risks
- **Scope Creep:** Weekend project becoming months of work
  - *Mitigation:* Fixed time budget, "good enough" mentality
- **Maintenance Burden:** Ongoing support expectations
  - *Mitigation:* Clear documentation, community contributions

## Future Considerations (Not MVP)

### Nice-to-Have Features
- **Sound:** Whale song audio clips
- **Offline Mode:** Cached data for poor connectivity
- **User Contributions:** Allow users to report sightings
- **Historical Data:** Show sightings over time
- **Migration Patterns:** Animate whale movement routes

### Technical Improvements
- **Service Worker:** Better performance and offline capability
- **Data Caching:** Reduce API calls
- **Image Optimization:** Faster whale photos
- **Accessibility:** Screen reader support, keyboard navigation

### Community Features
- **Species Contributions:** Users submit new whale species
- **Photo Uploads:** User-generated whale photos
- **Conservation Info:** Links to whale protection organizations
- **Sharing:** Easy social media sharing of sightings

## Development Approach

### Iteration Strategy
1. **Week 1:** Core map + basic whale markers
2. **Week 2:** Mobile optimization + species filtering
3. **Week 3:** Polish, testing, documentation
4. **Ongoing:** Community feedback and small improvements

### Testing Strategy
- **Manual Testing:** Real devices, not just browser dev tools
- **Mobile-First:** Test on phones before desktop
- **Slow Connections:** Test on 3G, not just WiFi
- **Real Users:** Get feedback from non-developers

### Success Definition
"A non-developer can fork this repo, customize it for tracking something else (birds, earthquakes, etc.), and deploy it successfully within an hour."

---

## Appendix: Technical Specifications

### API Integration
- **Primary:** GBIF Occurrence API
- **Endpoint:** `https://api.gbif.org/v1/occurrence/search`
- **Rate Limits:** 100 requests/hour (sufficient for use case)
- **Data Format:** JSON with coordinates, species, dates

### Map Integration
- **Library:** Leaflet.js (lightweight, mobile-friendly)
- **Tiles:** Ocean basemap from ArcGIS
- **Features:** Markers, popups, zoom controls
- **Mobile:** Touch gestures, responsive controls

### Deployment
- **Primary:** GitHub Pages (free, automatic)
- **Backup:** Any static hosting (Netlify, Vercel, etc.)
- **Requirements:** Just HTML file, no build process
- **Custom Domain:** Optional, not required

---

*This PRD represents the thinking behind a 4-hour weekend project that turned into something people might actually use. The key insight: you don't need a perfect product requirements document to build something useful.*