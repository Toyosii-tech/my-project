# StudentHub — Admin Dashboard

A modern, responsive student management system frontend built with vanilla HTML, CSS, and JavaScript. Designed for administrators to manage students, courses, results, timetables, fees, and settings from a single dashboard.

---

## Features

### Dashboard
- **Statistics overview** — Total students, courses, results, and fees paid at a glance
- **Student management table** — View, search, add, edit, and delete students
- **Real-time search** — Filter students by name, matric number, or course
- **Notifications panel** — Recent activity feed (new students, course updates, payments, results)
- **Quick actions** — One-click access to add students, courses, calculate grades/GPA
- **Today's timetable** — Upcoming classes at a glance

### Pages
| Page | Description | Status |
|------|-------------|--------|
| `index.html` | Main admin dashboard | ✅ Complete |
| `student.htm` | Student management (standalone) | 🚧 Placeholder |
| `courses.html` | Course catalog (student view) | ✅ Complete |
| `results.html` | Results management | 🚧 Placeholder |
| `Fees.html` | Fee management | 🚧 Placeholder |
| `Timetable.html` | Weekly timetable (student view) | ✅ Complete |
| `settings.html` | System settings | 🚧 Placeholder |

### UI/UX
- **Responsive design** — Works on desktop, tablet, and mobile
- **Dark mode support** — CSS variables for easy theming (partial implementation)
- **Modern styling** — Inter font, Font Awesome 6 icons, subtle shadows, smooth transitions
- **Accessible** — Focus-visible outlines, semantic HTML, proper contrast ratios

---

## Tech Stack

- **HTML5** — Semantic markup
- **CSS3** — Custom properties (variables), Grid, Flexbox, media queries
- **Vanilla JavaScript** — DOM manipulation (minimal, extensible)
- **Font Awesome 6** — Icons (via CDN)
- **Google Fonts** — Inter (via CDN)

No build tools, bundlers, or frameworks required.

---

## Project Structure

```
my-project/
├── index.html          # Main admin dashboard (fully styled inline)
├── style.css           # Alternative/legacy stylesheet
├── script.js           # JavaScript (minimal, needs completion)
├── student.htm         # Student management page (placeholder)
├── courses.html        # Course catalog page
├── results.html        # Results page (placeholder)
├── Fees.html           # Fees page (placeholder)
├── Timetable.html      # Weekly timetable page
├── settings.html       # Settings page (placeholder)
└── .kilo/              # Kilo IDE configuration (ignore)
```

---

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Optional: Local server for development (e.g., VS Code Live Server, `npx serve`)

### Installation
```bash
# Clone the repository
git clone https://github.com/Toyosii-tech/my-project.git
cd my-project

# Option 1: Open directly in browser
open index.html        # macOS
start index.html       # Windows

---

## Usage

### Dashboard (`index.html`)
1. Open `index.html` in a browser
2. Use the **sidebar** to navigate between sections
3. Click **"Add student"** to open the add-student modal (UI only — needs JS implementation)
4. Use the **search bars** to filter students
5. Click **edit/delete** icons on any row (UI only — needs JS implementation)
6. Toggle dark mode via the moon icon in the top bar (partial — needs JS implementation)

### Courses (`courses.html`)
- Static course catalog with hover effects and color-coded tags

### Timetable (`Timetable.html`)
- Weekly schedule with color-coded course tags
- Horizontally scrollable on mobile

---

## Customization

### Colors & Theming
All colors are defined as CSS custom properties in `index.html` (lines 21–40):

```css
:root {
  --bg: #f4f6fb;
  --surface: #ffffff;
  --sidebar-bg: #f8f9fc;
  --accent: #2a6df4;
  --accent-soft: #eef4ff;
  --success: #1f9d6e;
  --text-primary: #1e2a3a;
  --text-secondary: #5e6f8d;
  --border-light: #e9edf4;
  /* ... */
}
```

To create a dark theme, override these variables in a `.dark` class (see `style.css` lines 351–393 for reference).

### Adding Pages
1. Create a new `.html` file
2. Add a link in the sidebar navigation (`index.html` lines 680–687)
3. Follow the existing layout patterns (sidebar, top-bar, main-content)

---

## Known Issues / TODOs

- [ ] **JavaScript implementation** — `script.js` is incomplete; needs:
  - Student CRUD operations (add/edit/delete)
  - Search/filter functionality
  - Dark mode toggle
  - Data persistence (localStorage or API integration)
- [ ] **Placeholder pages** — `student.htm`, `results.html`, `Fees.html`, `settings.html` need full implementations
- [ ] **Consolidate styles** — `index.html` has inline styles; `style.css` duplicates some rules. Consider moving all styles to a single external stylesheet
- [ ] **Form validation** — Add client-side validation for student/course forms
- [ ] **API integration** — Connect to a backend for real data persistence
- [ ] **Authentication** — Add login/logout flow

---

## Browser Support

| Browser | Version |
|---------|---------|
| Chrome  | 90+     |
| Firefox | 88+     |
| Safari  | 14+     |
| Edge    | 90+     |

Uses modern CSS (Grid, Flexbox, custom properties) — no polyfills needed for listed versions.

---

## License

MIT License — feel free to use, modify, and distribute.

---

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## Acknowledgments

- [Font Awesome](https://fontawesome.com/) for icons
- [Google Fonts](https://fonts.google.com/) for Inter
- Design inspired by modern admin dashboard patterns