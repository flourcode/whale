# 🐋 Whale Tracker - Discover Ocean Giants

A simple, mobile-first web app that tracks whale sightings around the world using real data from GBIF (Global Biodiversity Information Facility). Built with just HTML, CSS, and JavaScript—no frameworks, no build tools, just good vibes.

**[🌊 Live Demo](https://flourcode.github.io/whale/)**

## What It Does

- **Real-time whale tracking** using live data from scientific databases
- **Interactive map** showing recent whale sightings worldwide
- **Species filtering** to focus on specific types of whales
- **Mobile-optimized** with full-screen modals and touch-friendly controls
- **Responsive design** that works on phones, tablets, and desktops

## The Stack (Spoiler: It's Simple)

- **Frontend**: Pure HTML5, CSS3, and vanilla JavaScript
- **Mapping**: Leaflet.js for interactive maps
- **Data**: GBIF API for real whale sighting data
- **Styling**: Custom CSS with ocean-themed design
- **Hosting**: GitHub Pages (free!)

Total monthly cost: **$0** 🎉

## Quick Start

### Option 1: Fork & Deploy (Easiest)
1. Fork this repository
2. Go to Settings → Pages
3. Set source to "Deploy from a branch" → main
4. Your app will be live at `https://yourusername.github.io/whale/`

### Option 2: Download & Run Locally
```bash
git clone https://github.com/flourcode/whale.git
cd whale
# Open index.html in your browser - that's it!
```

### Option 3: One-File Wonder
Just download `index.html` and open it in any browser. Everything is self-contained.

## Features

### 🗺️ Interactive Map
- Ocean-themed map tiles for that underwater feel
- Animated whale markers that bounce when you hover
- Real-time data from multiple whale species

### 📱 Mobile-First Design
- Touch-friendly controls at the bottom
- Full-screen whale details on mobile
- Desktop gets fancy popups instead

### 🔍 Species Filtering
- Filter by specific whale types
- Real-time updates as you select/deselect
- Pretty emoji indicators because why not

### 🎨 Ocean Vibes
- Custom CSS animations (floating whales, wave effects)
- Ocean color palette throughout
- Responsive design that doesn't suck on mobile

## Whale Species Tracked

- 🐋 Blue Whale (*Balaenoptera musculus*)
- 🐋 Humpback Whale (*Megaptera novaeangliae*)
- 🐋 Fin Whale (*Balaenoptera physalus*)
- 🐋 Minke Whale (*Balaenoptera acutorostrata*)
- 🐋 North Atlantic Right Whale (*Eubalaena glacialis*)
- 🐋 Sperm Whale (*Physeter macrocephalus*)
- 🐋 Killer Whale (*Orcinus orca*)
- 🐋 Pilot Whale (*Globicephala melas*)
- 🐬 Common Dolphin (*Delphinus delphis*)

## How I Built This (The Real Story)

This started as a 4-hour weekend project because I like whales. Here's my actual process:

### The Prompts That Worked

**Initial build:**
```
Make me a whale tracking app with a map. Use HTML and JavaScript. 
No placeholder code. I want it to pull real data from a public dataset. 
Optimize it for mobile. Make it work in a single HTML file if possible.
```

**When the API broke:**
```
This code isn't working. Here's the error from the browser console: 
[error message]. Here's my code: [paste code]. 
Fix it and explain what was wrong in simple terms.
```

**Making it pretty:**
```
This app works but looks like it was designed in 1995. Make it modern and 
mobile-friendly without changing the core functionality. Use clean, 
professional styling with an ocean theme.
```

### Tools I Used
- **Claude/ChatGPT** for writing the initial code
- **Gemini** for debugging when things broke
- **Firefox DevTools** for testing and fixing mobile issues
- **Notepad** for editing (seriously)
- **GitHub Pages** for hosting

### What Broke and How I Fixed It
1. **GBIF API returned weird data structures** → Used console.log to understand the actual response format
2. **Mobile popups were terrible** → Switched to full-screen modals on small screens
3. **Map tiles looked boring** → Found ocean-themed tiles and added custom CSS filters
4. **Touch controls interfered with map panning** → Added `touch-action: manipulation` to control elements

## Customization Ideas

Want to build something similar? Here are some ideas:

### Easy Modifications
- **Bird Migration Tracker** - Replace whale species with bird migration data
- **Cherry Blossom Tracker** - Use plant phenology data for bloom tracking
- **Earthquake Monitor** - Switch to USGS earthquake data
- **ISS Tracker** - Use NASA APIs to track the International Space Station

### The Magic Prompt for Variations
```
Take this whale tracking app and modify it to track [YOUR_THING_HERE]. 
Keep the same mobile-friendly design and interactive map, but change 
the data source to [YOUR_API_HERE] and update the styling to match 
the new theme.
```

### Quick Theme Changes
Want a different vibe? Change these CSS variables in the `:root` section:

```css
:root {
    --ocean-deep: #your-dark-color;
    --ocean-light: #your-light-color;
    --ocean-accent: #your-accent-color;
}
```

## Technical Notes

### Data Source
- Uses GBIF (Global Biodiversity Information Facility) API
- Filters for records with coordinates from 2025
- Handles API failures gracefully
- No API key required (it's free!)

### Performance
- Lazy loads whale images
- Limits to 50 records per species to keep it snappy
- Uses efficient marker clustering on the map
- Mobile-optimized animations

### Browser Support
- Works in all modern browsers
- Mobile Safari, Chrome, Firefox tested
- IE? Probably not, but who cares

## Contributing

Found a bug? Want to add a feature? Here's how:

1. Fork the repo
2. Make your changes
3. Test on mobile (seriously, test on mobile)
4. Submit a pull request
5. Include a description of what you changed and why

### Ideas for Contributions
- Add more whale species
- Improve the mobile modal design
- Add sound effects (whale songs?)
- Better error handling for offline use
- Accessibility improvements

## License

MIT License - do whatever you want with this code. Build something cool and let me know!

## Why I Built This

I'm a 56-year-old retired sales guy who likes whales and wanted to prove that you don't need to be a "real developer" to build useful stuff. The tools are getting so good that the gap between an idea and a working app gets smaller every day.

If this helps you build your own thing, even better.

**Good vibes only.**

---

## More Projects

Check out my other "I have no idea what I'm doing" projects:
- **AskArti** - Federal sales AI coach
- **Subhoo** - Federal contractor network mapper

All built the same way: HTML, JavaScript, AI tools, and stubbornness.

👉 **[mflournoy on GitHub](https://github.com/mflournoy)**

---

*Built with ❤️ and way too much coffee by a Marine who still doesn't know what Node.js is.*