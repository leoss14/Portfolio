PORTFOLIO WEBSITE - LIGHT THEME UPDATE
========================================

This folder contains your updated portfolio website with the light blue theme.

FOLDER STRUCTURE:
=================
Website-/
├── index.html              (Redirect file - upload to root)
├── Pages/
│   ├── style.css          (Shared stylesheet - all colors/styles here)
│   ├── index.html         (Homepage)
│   ├── about.html
│   ├── contact.html
│   ├── projects.html
│   ├── uber_project.html
│   └── project-moodys-capstone.html
└── outputs/                (Create this folder and add your HTML visualizations)
    ├── 1_uber_2018_clusters.html
    ├── 2_uber_2025_clusters.html
    ├── 3_top_zones_comparison.html
    ├── 4_hourly_patterns.html
    ├── 5_daily_patterns.html
    ├── 6_demand_heatmaps.html
    ├── 7_borough_analysis.html
    └── 8_cluster_shifts_PROPER.html

WHAT CHANGED:
=============
✓ All pages now use a shared light blue/white theme (style.css)
✓ Colors are consistent across all pages
✓ iframe paths fixed to work with Pages/ folder structure (../outputs/)
✓ Clean, professional light theme throughout
✓ Easy to customize - just edit style.css to change colors/styling

TO UPDATE YOUR WEBSITE:
=======================
1. Upload the root index.html (redirect file) to /Website-/
2. Upload all Pages/ contents to /Website-/Pages/
3. Create /Website-/outputs/ folder and upload your visualization HTML files
4. Push to GitHub and enable GitHub Pages

TO CHANGE COLORS/STYLING:
==========================
Just edit Pages/style.css and change the CSS variables at the top:
- --blue-main: Main blue color
- --blue-dark: Darker blue for headers
- --text-medium: Text color
etc.

All pages will automatically update!

GITHUB PAGES SETUP:
===================
1. Repository name: username.github.io
2. Enable Pages in Settings → Pages
3. Your site: https://username.github.io
   (redirects to https://username.github.io/Pages/index.html)

NOTES:
======
- All visualization iframes in uber_project.html use ../outputs/ paths
- Navigation works between all pages
- GitHub links updated to: github.com/leoss14
- LinkedIn and email preserved from original files
