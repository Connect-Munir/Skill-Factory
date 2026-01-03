# SVG Infographic Templates

Ready-to-use SVG structures for common infographic patterns.

## Base Template

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 1200" width="800" height="1200">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&amp;display=swap');
      :root {
        --primary: #2563eb;
        --secondary: #f1f5f9;
        --accent: #f59e0b;
        --text: #1e293b;
        --text-light: #64748b;
        --bg: #ffffff;
      }
      .title { font: 700 36px 'Poppins', sans-serif; fill: var(--text); }
      .subtitle { font: 400 16px 'Poppins', sans-serif; fill: var(--text-light); }
      .section-header { font: 600 22px 'Poppins', sans-serif; fill: var(--text); }
      .body { font: 400 14px 'Poppins', sans-serif; fill: var(--text); }
      .stat-number { font: 700 32px 'Poppins', sans-serif; fill: var(--primary); }
      .stat-label { font: 400 12px 'Poppins', sans-serif; fill: var(--text-light); }
      .icon { stroke: var(--primary); stroke-width: 2; fill: none; }
    </style>
  </defs>
  
  <!-- Background -->
  <rect width="800" height="1200" fill="var(--bg)"/>
  
  <!-- Content goes here -->
</svg>
```

## Stat Card Component

```svg
<g class="stat-card" transform="translate(X, Y)">
  <!-- Background card -->
  <rect width="180" height="120" rx="8" fill="var(--secondary)"/>
  
  <!-- Icon (24x24) -->
  <g transform="translate(78, 16)">
    <svg width="24" height="24" viewBox="0 0 24 24" class="icon">
      <!-- Icon path -->
    </svg>
  </g>
  
  <!-- Number -->
  <text x="90" y="72" text-anchor="middle" class="stat-number">42%</text>
  
  <!-- Label -->
  <text x="90" y="100" text-anchor="middle" class="stat-label">Growth Rate</text>
</g>
```

## Timeline Component (Horizontal)

```svg
<g class="timeline" transform="translate(40, Y)">
  <!-- Timeline line -->
  <line x1="0" y1="30" x2="720" y2="30" stroke="var(--secondary)" stroke-width="3"/>
  
  <!-- Step 1 -->
  <g transform="translate(0, 0)">
    <circle cx="0" cy="30" r="12" fill="var(--primary)"/>
    <text x="0" y="10" text-anchor="middle" class="body" font-weight="600">Step 1</text>
    <text x="0" y="60" text-anchor="middle" class="stat-label">Description</text>
  </g>
  
  <!-- Step 2 -->
  <g transform="translate(180, 0)">
    <circle cx="0" cy="30" r="12" fill="var(--primary)"/>
    <text x="0" y="10" text-anchor="middle" class="body" font-weight="600">Step 2</text>
    <text x="0" y="60" text-anchor="middle" class="stat-label">Description</text>
  </g>
  
  <!-- Add more steps... -->
</g>
```

## Comparison Table

```svg
<g class="comparison" transform="translate(40, Y)">
  <!-- Headers -->
  <rect x="0" y="0" width="360" height="48" fill="var(--primary)" rx="8 8 0 0"/>
  <rect x="360" y="0" width="360" height="48" fill="var(--accent)" rx="8 8 0 0"/>
  <text x="180" y="30" text-anchor="middle" fill="white" class="section-header">Option A</text>
  <text x="540" y="30" text-anchor="middle" fill="white" class="section-header">Option B</text>
  
  <!-- Row 1 -->
  <rect x="0" y="48" width="720" height="48" fill="var(--secondary)"/>
  <text x="180" y="78" text-anchor="middle" class="body">Feature 1</text>
  <text x="540" y="78" text-anchor="middle" class="body">Feature 1</text>
  
  <!-- Row 2 -->
  <rect x="0" y="96" width="720" height="48" fill="var(--bg)"/>
  <text x="180" y="126" text-anchor="middle" class="body">Feature 2</text>
  <text x="540" y="126" text-anchor="middle" class="body">Feature 2</text>
</g>
```

## Progress Bar

```svg
<g class="progress" transform="translate(X, Y)">
  <!-- Label -->
  <text x="0" y="0" class="body">Metric Name</text>
  
  <!-- Background bar -->
  <rect x="0" y="12" width="200" height="12" rx="6" fill="var(--secondary)"/>
  
  <!-- Progress fill (width = percentage * 2) -->
  <rect x="0" y="12" width="150" height="12" rx="6" fill="var(--primary)"/>
  
  <!-- Percentage -->
  <text x="210" y="22" class="body" font-weight="600">75%</text>
</g>
```

## Pie/Donut Chart

```svg
<g class="donut" transform="translate(X, Y)">
  <!-- Segments using stroke-dasharray -->
  <circle cx="80" cy="80" r="60" fill="none" stroke="var(--primary)" 
          stroke-width="24" stroke-dasharray="188.5 377" transform="rotate(-90 80 80)"/>
  <circle cx="80" cy="80" r="60" fill="none" stroke="var(--accent)" 
          stroke-width="24" stroke-dasharray="94.25 377" stroke-dashoffset="-188.5" transform="rotate(-90 80 80)"/>
  <circle cx="80" cy="80" r="60" fill="none" stroke="var(--secondary)" 
          stroke-width="24" stroke-dasharray="94.25 377" stroke-dashoffset="-282.75" transform="rotate(-90 80 80)"/>
  
  <!-- Center text -->
  <text x="80" y="75" text-anchor="middle" class="stat-number">50%</text>
  <text x="80" y="95" text-anchor="middle" class="stat-label">Main Metric</text>
</g>
```

## Bar Chart

```svg
<g class="bar-chart" transform="translate(X, Y)">
  <!-- Bars -->
  <rect x="0" y="80" width="40" height="120" rx="4" fill="var(--primary)"/>
  <rect x="60" y="40" width="40" height="160" rx="4" fill="var(--primary)"/>
  <rect x="120" y="100" width="40" height="100" rx="4" fill="var(--primary)"/>
  <rect x="180" y="20" width="40" height="180" rx="4" fill="var(--accent)"/>
  
  <!-- Labels -->
  <text x="20" y="220" text-anchor="middle" class="stat-label">Q1</text>
  <text x="80" y="220" text-anchor="middle" class="stat-label">Q2</text>
  <text x="140" y="220" text-anchor="middle" class="stat-label">Q3</text>
  <text x="200" y="220" text-anchor="middle" class="stat-label">Q4</text>
  
  <!-- Value labels -->
  <text x="20" y="70" text-anchor="middle" class="body">60</text>
  <text x="80" y="30" text-anchor="middle" class="body">80</text>
  <text x="140" y="90" text-anchor="middle" class="body">50</text>
  <text x="200" y="10" text-anchor="middle" class="body" font-weight="700">90</text>
</g>
```

## Icon + Text Row

```svg
<g class="icon-row" transform="translate(X, Y)">
  <!-- Icon container -->
  <rect width="48" height="48" rx="8" fill="var(--secondary)"/>
  <g transform="translate(12, 12)">
    <svg width="24" height="24" viewBox="0 0 24 24" class="icon">
      <!-- Icon path -->
    </svg>
  </g>
  
  <!-- Text -->
  <text x="64" y="20" class="body" font-weight="600">Title Text</text>
  <text x="64" y="38" class="stat-label">Supporting description text</text>
</g>
```

## Callout Box

```svg
<g class="callout" transform="translate(X, Y)">
  <rect width="720" height="80" rx="8" fill="var(--accent)" opacity="0.1"/>
  <rect width="4" height="80" fill="var(--accent)"/>
  <text x="24" y="32" class="body" font-weight="600" fill="var(--accent)">Key Insight</text>
  <text x="24" y="56" class="body">Important takeaway message goes here.</text>
</g>
```
