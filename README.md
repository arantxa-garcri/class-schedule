# Semester Class Sessions Calculator (by Group)

A simple, responsive web app to calculate how many class sessions and total hours you will teach per group during a semester.  
It supports weekly schedules, holidays, vacation periods (date ranges), and exports a detailed PDF report.

## Features

- Add multiple groups (e.g., `1022`, `1041`, etc.)
- Define a weekly schedule per group (e.g., Monday 2h, Friday 1h)
- Exclude:
  - Holidays (single dates)
  - Vacation periods (date ranges)
- Generate an on-screen report:
  - Session list per group (date, weekday, hours)
  - Total sessions and hours per group
  - Grand total hours across all groups
- Export a PDF report (jsPDF + autoTable)
- Light/Dark mode toggle (☀️/🌙) with saved preference
- Responsive layout for small and large screens (I'll try to improve it in later versions, promise!💜)

## Quick Start

### Option A) Run locally (no setup)

1. Download or clone this repository.
2. Open `index.html` in your browser (Chrome/Firefox/Safari).

### Option B) Run with a local server (recommended)

This avoids some browser restrictions and behaves closer to production.

- Using Python:
  ```bash
  python -m http.server 8000
  ```
  Then open `http://localhost:8000`

- Using Node (http-server):
  ```bash
  npx http-server .
  ```
  Then open the provided local URL.

## How to Use

1. **Set the semester range**
   - Choose Start and End dates.

2. **Add exclusions**
   - Add **holidays** as single dates.
   - Add **vacation periods** as date ranges.
   - These dates will be omitted from the final count.

3. **Create groups**
   - Enter a group name.
   - Add one or more weekly schedule rows:
     - Select weekday
     - Enter hours per session
   - Click **Save group**.

4. **Generate report**
   - Click **Calculate report** to view the full breakdown on screen.

5. **Export PDF**
   - Click **Export PDF** to generate a downloadable report including:
     - Semester summary and exclusions
     - Summary table per group
     - Detailed session tables per group

## PDF Export Notes

- PDF generation runs entirely in the browser.
- Powered by:
  - `jsPDF`
  - `jspdf-autotable`

## Tech Stack

- HTML + CSS + Vanilla JavaScript
- jsPDF + autoTable (CDN)

## Contributing

Contributions are welcome! Feel free to:

- Fork the repo
- Create a feature branch
- Submit a Pull Request

If you fork or reuse the project, please provide **credit** by referencing this repository in your fork and/or documentation.  
(And if you improve it, even better: PRs are appreciated. 😄)

## License

MIT License. See `LICENSE` for details.
