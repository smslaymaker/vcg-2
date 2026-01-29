# Virginia Consulting Group Website - Codebase Documentation

## Project Overview
This is a GitHub Pages website for the **Virginia Consulting Group (VCG)**, a student-run consulting organization at the University of Virginia. The website is built using Mobirise (a website builder) and serves as a professional presence for the organization.

**Technology Stack:**
- HTML5 static pages
- Bootstrap 5 CSS framework
- jQuery + JavaScript for interactivity
- Mobirise v5.9.18 (website builder/framework)
- GitHub Pages hosting (CNAME: vcg-2/)

---

## Project Structure

```
vcg-2/
├── index.html              # Home page
├── clients.html            # Client services/what we do
├── contact.html            # Contact form
├── ourteam.html            # Meet the team section
├── exec.html               # Executive board
├── join.html               # Get involved/recruitment
├── disclaimer.html         # Disclaimer page
├── project.mobirise        # Mobirise project file (binary)
├── CNAME                   # GitHub Pages domain config
├── hashes.json             # Asset hash tracking
├── assets/                 # All static assets
│   ├── bootstrap/          # Bootstrap 5 CSS & JS
│   ├── mobirise/           # Mobirise theme CSS
│   ├── theme/              # Custom theme
│   │   ├── css/style.css   # Main theme stylesheet (1142 lines)
│   │   └── js/script.js    # Main script with jQuery plugins
│   ├── dropdown/           # Custom dropdown menus
│   ├── images/             # Organization images & logos
│   │   ├── companies/      # Client company logos
│   │   └── headshots/      # Team member photos
│   ├── web/                # Web assets
│   │   └── assets/jquery/  # jQuery library
│   └── [various libs]/     # Utility libraries
├── README.md
└── .git/                   # Git repository
```

---

## Key Pages & Content

### 1. **index.html** - Home Page
- **Purpose:** Main landing page with hero image
- **Key Elements:**
  - Navigation bar with logo and menu
  - Hero section: "UNIQUE ANALYSTS. PROVEN SUCCESS."
  - Tagline about VCG's mission
  - CTA buttons: "WHAT WE DO", "WHY JOIN US", "APPLY NOW" (Google Form link)
  - Footer

### 2. **clients.html** - Client Services
- **Purpose:** Showcase consulting services and past clients
- **Key Elements:**
  - Service descriptions
  - Client company logos/case studies
  - Client testimonials

### 3. **ourteam.html** - Team Members
- **Purpose:** Display team member profiles with headshots
- **Key Elements:**
  - Team member cards with photos
  - Member roles/positions
  - Interactive team gallery

### 4. **exec.html** - Executive Board
- **Purpose:** Leadership team information
- **Key Elements:**
  - Executive leadership profiles
  - Titles and departments

### 5. **join.html** - Get Involved
- **Purpose:** Recruitment and membership information
- **Key Elements:**
  - Why join VCG
  - Application information
  - Requirements/qualifications

### 6. **contact.html** - Contact Form
- **Purpose:** Allow visitors to contact the organization
- **Key Elements:**
  - Contact form with validation
  - Contact information
  - Form submission handling

---

## Common Template Elements

### Navigation Bar (All Pages)
- **Structure:** Fixed top navbar with Bootstrap
- **Logo:** `assets/images/vcg-logo-white-122x122.png`
- **Menu Items:**
  - HOME (index.html)
  - ABOUT US (dropdown)
    - Executive Board (exec.html)
    - Meet our Team (ourteam.html)
  - CLIENT SERVICES (clients.html)
  - GET INVOLVED (join.html)
  - CONTACT (contact.html)
- **Icons:** Mobirise icons (mbri-*)

**Navigation HTML Pattern (All pages):**
```html
<section class="menu" once="menu" id="menu1-[unique-id]">
  <nav class="navbar navbar-dropdown align-items-center navbar-fixed-top">
    <!-- Toggle button for mobile -->
    <!-- Logo section -->
    <!-- Menu items -->
  </nav>
</section>
```

### Footer
- Appears on all pages
- ID: `footer6-4h` (may vary)
- Contains copyright and social links

---

## Assets & Libraries

### CSS Files
| Path | Purpose | Size |
|------|---------|------|
| `assets/bootstrap/css/bootstrap.min.css` | Bootstrap 5 framework | Core layout |
| `assets/bootstrap/css/bootstrap-grid.min.css` | Grid system | Responsive columns |
| `assets/bootstrap/css/bootstrap-reboot.min.css` | CSS reset | Normalize styles |
| `assets/theme/css/style.css` | Custom theme | 1142 lines - Main styling |
| `assets/mobirise/css/mbr-additional.css` | Mobirise additions | Version-controlled |
| `assets/dropdown/css/style.css` | Dropdown styling | Custom menus |
| `assets/socicon/css/styles.css` | Social icons | Brand icons |

### JavaScript Files
| Path | Purpose |
|------|---------|
| `assets/web/assets/jquery/jquery.min.js` | jQuery library |
| `assets/theme/js/script.js` | Main script (see below) |
| `assets/dropdown/js/nav-dropdown.js` | Dropdown menu logic |
| `assets/dropdown/js/navbar-dropdown.js` | Navbar specific |
| `assets/bootstrap/js/bootstrap.min.js` | Bootstrap JS |
| `assets/popper/popper.min.js` | Popper.js (tooltips/dropdowns) |
| `assets/tether/tether.min.js` | Tether (positioning) |
| `assets/smoothscroll/smooth-scroll.js` | Smooth scrolling |
| `assets/parallax/jarallax.min.js` | Parallax backgrounds |
| `assets/formoid/formoid.min.js` | Form handling |

### Images
- **Logo:** `assets/images/vcg-logo-white-122x122.png` (white version for navbar)
- **Logo Alternative:** `assets/images/vcg-logo-black-128x128.png` (favicon)
- **Headshots:** `assets/images/headshots/` - Team member photos
- **Company Logos:** `assets/images/companies/` - Client logos

---

## Styling System

### Theme Structure
- **Primary Colors:** Dark theme with white text on dark backgrounds
- **Font:** Rubik (Google Fonts)
- **Bootstrap Utilities:** Uses Bootstrap classes throughout
- **Custom Classes:** Mobirise-specific classes (mbr-*)

### Key CSS Classes
| Class | Purpose |
|-------|---------|
| `.mbr-section` | Main section container |
| `.mbr-bold` | Bold text |
| `.mbr-fonts-style` | Font styling |
| `.display-1` through `.display-4` | Display heading sizes |
| `.navbar-dropdown` | Dropdown navbar |
| `.mbr-parallax-background` | Parallax effect |
| `.carousel` | Image/content carousel |
| `.col-md-*` | Bootstrap grid columns |

---

## JavaScript Functionality (script.js)

The main `script.js` file includes extensive jQuery plugins and functionality:

### Key Features
1. **Carousel Management**
   - Initializes carousel IDs and controls
   - Handles multi-column carousels

2. **Parallax Effects**
   - Uses Jarallax library for background parallax
   - Mobile device detection to disable on smaller screens

3. **Video Backgrounds**
   - Supports YouTube and Vimeo background videos
   - Generates video thumbnails

4. **Responsive Design**
   - Smart resizing for full-height sections
   - Mobile menu handling
   - Viewport unit handling for mobile browsers

5. **Navigation**
   - Fixed navbar with scroll detection
   - Dropdown menu behavior
   - Smooth anchor scrolling
   - Mobile hamburger menu

6. **Form Handling**
   - Formoid integration for form processing
   - Date/time input styling
   - Number input formatting

7. **Animation Effects**
   - Fade-in animations on scroll
   - easeInOutCubic easing function
   - Animation library integration

8. **Utility Functions**
   - Mobile device detection
   - Window resize event debouncing
   - Smooth scroll to anchor links
   - Footer reveal on short pages

### Important Functions
```javascript
// Carousel setup
p(element)           // Initialize carousel IDs
q(element)           // Setup multi-column carousels

// Navigation
// Handles fixed navbar, dropdowns, smooth scroll

// Video backgrounds
// d(element)         // Process video backgrounds

// Parallax
// c(element)         // Initialize parallax backgrounds

// Animations
// Monitors scroll and applies animations to hidden elements
```

---

## Mobirise-Specific Notes

### Mobirise Project File
- **File:** `project.mobirise` (binary)
- **Purpose:** Stores the Mobirise editor configuration and state
- **Note:** This is generated/maintained by Mobirise builder, don't edit manually

### Mobirise Version
- Built with: Mobirise v5.9.18
- Generator meta tag in all HTML files: `<meta name="generator" content="Mobirise v5.9.18">`

### Mobirise Classes
- `.cid-*` IDs on sections (content ID tracking)
- `.once="menu"` on navbar (prevents duplication)
- `data-app-modern-menu="true"` for modern menu behavior

---

## Development Workflow

### Editing Approach
1. **Primary:** Use Mobirise builder for layout/design changes
2. **Secondary:** Edit HTML directly for minor content updates
3. **CSS:** Modify `assets/theme/css/style.css` for styling
4. **JS:** Modify `assets/theme/js/script.js` for functionality

### Git Workflow
```bash
# Current status: On master, up to date with origin
# Check status
git status

# Make changes, commit
git add .
git commit -m "Description of changes"
git push origin master
```

### Important Files to Modify
- **Content updates:** Edit individual HTML pages (index.html, etc.)
- **Styling:** Modify `assets/theme/css/style.css`
- **Functionality:** Modify `assets/theme/js/script.js`
- **Navigation:** Consistent across all pages (in navbar section)

### Important Files NOT to Touch
- `project.mobirise` - Mobirise project file
- `.git/*` - Git internals
- `hashes.json` - Asset tracking

---

## Common Patterns & How to Make Changes

### Adding a New Page
1. Create new HTML file (e.g., `newpage.html`)
2. Copy navbar section from any existing page
3. Copy footer section from any existing page
4. Add content sections in between
5. Update navigation menu on all pages to link to new page

### Updating Team Members
1. Add headshot to `assets/images/headshots/`
2. Edit `ourteam.html` to add member card with:
   - Photo reference
   - Name
   - Title/role
   - Bio (if applicable)

### Updating Client Companies
1. Add logo to `assets/images/companies/`
2. Edit `clients.html` to reference new logo

### Modifying Colors/Fonts
1. Edit `assets/theme/css/style.css`
2. Look for color definitions (rgb values, hex codes)
3. Font changes in `style.css` or Google Fonts link in HTML head

### Adding Links
- Internal: Use relative paths (e.g., `href="contact.html"`)
- External: Use full URLs (e.g., `href="https://example.com"`)
- Anchors: Use IDs and `href="#id-name"`

---

## Meta Information

### Favicon
- Current: `assets/images/vcg-logo-black-128x128.png`
- Reference in HTML: `<link rel="shortcut icon" href="assets/images/vcg-logo-black-128x128.png">`

### Meta Descriptions
- Each page has a meta description for SEO
- Update in `<meta name="description">` tag

### GitHub Pages
- Domain: Configured via CNAME file
- Hosted on GitHub Pages
- Accessible via GitHub repository

---

## External Links & Forms

### Application Form
- **URL:** `https://forms.gle/LJv3Xh1SJyj2xp3e8`
- **Location:** Home page and Get Involved page
- **Type:** Google Form

### Contact Form
- **Location:** contact.html
- **Backend:** Formoid integration (assets/formoid/formoid.min.js)

---

## Debugging Notes

### Console Log Issues
- Check browser console (F12) for JavaScript errors
- Verify jQuery and other libraries load correctly
- Check network tab for missing assets

### Styling Issues
- Clear browser cache (Ctrl+Shift+Delete)
- Check Bootstrap grid classes (col-md-*, col-lg-*, etc.)
- Verify CSS file paths are correct
- Use Chrome DevTools to inspect elements

### Navigation Issues
- Ensure menu IDs are unique (cid-*)
- Verify navbar section has `once="menu"` attribute
- Check that all pages have consistent navbar code

---

## Technical Debt / Known Items

- Script.js contains minified/obfuscated code at the end (Mobirise licensing enforcement)
- Long inline CSS in some elements (prefer external stylesheet)
- Multiple jQuery plugins loaded (could be optimized)
- Mobirise version could be updated if needed

---

## Quick Reference: File Locations

| Item | Location |
|------|----------|
| Logo (white) | `assets/images/vcg-logo-white-122x122.png` |
| Logo (black/favicon) | `assets/images/vcg-logo-black-128x128.png` |
| Main CSS | `assets/theme/css/style.css` |
| Main JS | `assets/theme/js/script.js` |
| Team photos | `assets/images/headshots/` |
| Client logos | `assets/images/companies/` |
| Google Font | Rubik (loaded from googleapis.com) |
| Bootstrap CSS | `assets/bootstrap/css/` |
| jQuery | `assets/web/assets/jquery/jquery.min.js` |

---

## Getting Started with Changes

1. **For content updates:** Edit the relevant HTML file directly
2. **For styling changes:** Modify `assets/theme/css/style.css`
3. **For JavaScript enhancements:** Modify `assets/theme/js/script.js`
4. **For major layout changes:** Consider using Mobirise builder, or carefully edit HTML structure
5. **Always test** responsive design on mobile/tablet after changes
6. **Use Git** to track all changes with clear commit messages

---

**Last Updated:** January 28, 2026
**Git Status:** Committed and up to date with origin/master
