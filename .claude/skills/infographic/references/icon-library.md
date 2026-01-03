# Minimalistic Icon Library

SVG paths for common infographic icons. All icons use 24x24 viewBox with stroke-based design.

## Base Icon Wrapper

```svg
<svg width="24" height="24" viewBox="0 0 24 24" fill="none" 
     stroke="currentColor" stroke-width="2" 
     stroke-linecap="round" stroke-linejoin="round">
  <!-- Insert path here -->
</svg>
```

## Data & Statistics

### Bar Chart
```svg
<path d="M18 20V10M12 20V4M6 20v-6"/>
```

### Line Chart
```svg
<path d="M3 12l4-4 4 4 4-8 6 6"/>
```

### Pie Chart
```svg
<circle cx="12" cy="12" r="10"/>
<path d="M12 2v10l8.5 5"/>
```

### Trending Up
```svg
<polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/>
<polyline points="17 6 23 6 23 12"/>
```

### Trending Down
```svg
<polyline points="23 18 13.5 8.5 8.5 13.5 1 6"/>
<polyline points="17 18 23 18 23 12"/>
```

### Percentage
```svg
<circle cx="6" cy="6" r="2"/>
<circle cx="18" cy="18" r="2"/>
<line x1="20" y1="4" x2="4" y2="20"/>
```

## Process & Flow

### Arrow Right
```svg
<line x1="5" y1="12" x2="19" y2="12"/>
<polyline points="12 5 19 12 12 19"/>
```

### Arrow Down
```svg
<line x1="12" y1="5" x2="12" y2="19"/>
<polyline points="19 12 12 19 5 12"/>
```

### Chevron Right
```svg
<polyline points="9 18 15 12 9 6"/>
```

### Refresh/Cycle
```svg
<path d="M23 4v6h-6"/>
<path d="M1 20v-6h6"/>
<path d="M3.51 9a9 9 0 0114.85-3.36L23 10M1 14l4.64 4.36A9 9 0 0020.49 15"/>
```

### Check Circle
```svg
<circle cx="12" cy="12" r="10"/>
<polyline points="9 12 11 14 15 10"/>
```

### Steps (Numbered)
```svg
<circle cx="12" cy="12" r="10"/>
<text x="12" y="16" text-anchor="middle" font-size="12" fill="currentColor" stroke="none">1</text>
```

## People & Users

### User
```svg
<circle cx="12" cy="7" r="4"/>
<path d="M5.5 21a7.5 7.5 0 0115 0"/>
```

### Users (Group)
```svg
<circle cx="9" cy="7" r="4"/>
<path d="M3 21v-2a4 4 0 014-4h4a4 4 0 014 4v2"/>
<circle cx="17" cy="7" r="3"/>
<path d="M21 21v-2a3 3 0 00-2.12-2.88"/>
```

### User Plus
```svg
<circle cx="12" cy="7" r="4"/>
<path d="M5.5 21a7.5 7.5 0 0113 0"/>
<line x1="20" y1="8" x2="20" y2="14"/>
<line x1="17" y1="11" x2="23" y2="11"/>
```

## Objects & Concepts

### Document
```svg
<path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/>
<polyline points="14 2 14 8 20 8"/>
```

### Folder
```svg
<path d="M22 19a2 2 0 01-2 2H4a2 2 0 01-2-2V5a2 2 0 012-2h5l2 3h9a2 2 0 012 2z"/>
```

### Lightbulb (Idea)
```svg
<path d="M9 18h6"/>
<path d="M10 22h4"/>
<path d="M12 2a7 7 0 017 7c0 2.38-1.19 4.47-3 5.74V17a1 1 0 01-1 1H9a1 1 0 01-1-1v-2.26C6.19 13.47 5 11.38 5 9a7 7 0 017-7z"/>
```

### Gear (Settings)
```svg
<circle cx="12" cy="12" r="3"/>
<path d="M19.4 15a1.65 1.65 0 00.33 1.82l.06.06a2 2 0 010 2.83 2 2 0 01-2.83 0l-.06-.06a1.65 1.65 0 00-1.82-.33 1.65 1.65 0 00-1 1.51V21a2 2 0 01-2 2 2 2 0 01-2-2v-.09A1.65 1.65 0 009 19.4a1.65 1.65 0 00-1.82.33l-.06.06a2 2 0 01-2.83 0 2 2 0 010-2.83l.06-.06a1.65 1.65 0 00.33-1.82 1.65 1.65 0 00-1.51-1H3a2 2 0 01-2-2 2 2 0 012-2h.09A1.65 1.65 0 004.6 9a1.65 1.65 0 00-.33-1.82l-.06-.06a2 2 0 010-2.83 2 2 0 012.83 0l.06.06a1.65 1.65 0 001.82.33H9a1.65 1.65 0 001-1.51V3a2 2 0 012-2 2 2 0 012 2v.09a1.65 1.65 0 001 1.51 1.65 1.65 0 001.82-.33l.06-.06a2 2 0 012.83 0 2 2 0 010 2.83l-.06.06a1.65 1.65 0 00-.33 1.82V9a1.65 1.65 0 001.51 1H21a2 2 0 012 2 2 2 0 01-2 2h-.09a1.65 1.65 0 00-1.51 1z"/>
```

### Calendar
```svg
<rect x="3" y="4" width="18" height="18" rx="2" ry="2"/>
<line x1="16" y1="2" x2="16" y2="6"/>
<line x1="8" y1="2" x2="8" y2="6"/>
<line x1="3" y1="10" x2="21" y2="10"/>
```

### Clock
```svg
<circle cx="12" cy="12" r="10"/>
<polyline points="12 6 12 12 16 14"/>
```

### Target
```svg
<circle cx="12" cy="12" r="10"/>
<circle cx="12" cy="12" r="6"/>
<circle cx="12" cy="12" r="2"/>
```

### Star
```svg
<polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/>
```

### Heart
```svg
<path d="M20.84 4.61a5.5 5.5 0 00-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 00-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 000-7.78z"/>
```

## Money & Business

### Dollar
```svg
<line x1="12" y1="1" x2="12" y2="23"/>
<path d="M17 5H9.5a3.5 3.5 0 000 7h5a3.5 3.5 0 010 7H6"/>
```

### Briefcase
```svg
<rect x="2" y="7" width="20" height="14" rx="2" ry="2"/>
<path d="M16 21V5a2 2 0 00-2-2h-4a2 2 0 00-2 2v16"/>
```

### Building
```svg
<rect x="4" y="2" width="16" height="20" rx="2" ry="2"/>
<line x1="9" y1="22" x2="9" y2="2"/>
<line x1="15" y1="22" x2="15" y2="2"/>
<line x1="4" y1="12" x2="20" y2="12"/>
```

## Communication

### Mail
```svg
<rect x="2" y="4" width="20" height="16" rx="2"/>
<polyline points="22 6 12 13 2 6"/>
```

### Message
```svg
<path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/>
```

### Globe
```svg
<circle cx="12" cy="12" r="10"/>
<line x1="2" y1="12" x2="22" y2="12"/>
<path d="M12 2a15.3 15.3 0 014 10 15.3 15.3 0 01-4 10 15.3 15.3 0 01-4-10 15.3 15.3 0 014-10z"/>
```

## Technology

### Smartphone
```svg
<rect x="5" y="2" width="14" height="20" rx="2" ry="2"/>
<line x1="12" y1="18" x2="12.01" y2="18"/>
```

### Monitor
```svg
<rect x="2" y="3" width="20" height="14" rx="2" ry="2"/>
<line x1="8" y1="21" x2="16" y2="21"/>
<line x1="12" y1="17" x2="12" y2="21"/>
```

### Cloud
```svg
<path d="M18 10h-1.26A8 8 0 109 20h9a5 5 0 000-10z"/>
```

### Lock
```svg
<rect x="3" y="11" width="18" height="11" rx="2" ry="2"/>
<path d="M7 11V7a5 5 0 0110 0v4"/>
```

## Simple Shapes (For Custom Icons)

### Circle
```svg
<circle cx="12" cy="12" r="10"/>
```

### Square
```svg
<rect x="3" y="3" width="18" height="18" rx="2"/>
```

### Triangle
```svg
<polygon points="12 2 22 22 2 22"/>
```

### Plus
```svg
<line x1="12" y1="5" x2="12" y2="19"/>
<line x1="5" y1="12" x2="19" y2="12"/>
```

### Minus
```svg
<line x1="5" y1="12" x2="19" y2="12"/>
```

### X (Close)
```svg
<line x1="18" y1="6" x2="6" y2="18"/>
<line x1="6" y1="6" x2="18" y2="18"/>
```
