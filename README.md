# Class Schedule Generator

A simple web application that generates a PDF class schedule from user input.

## Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/class-schedule-generator.git
   cd class-schedule-generator
   ```

2. **Open the app**
   - Simply double-click `index.html` to open it in your default browser.  
   - _Or_ serve it locally:
     ```bash
     npx serve .
     ```

3. **Enter schedule data**
   1. Select **Semester Start** and **Semester End** dates.
   2. List **Holidays** in `YYYY-MM-DD` format, separated by commas.
   3. Fill in **Group** code (e.g., `1022`) and **Class Name** (e.g., `Calculus I`).
   4. Click **+ Add day** to define weekly meetings:
      - Choose **Day of week**.
      - Enter **Hours** for that day.
      - Repeat for each meeting day.

4. **Generate PDF**
   - Click **Generate PDF**.  
   - Download will start automatically with your schedule.

## What’s Included

- `index.html`: Main application file.
- `LICENSE`: MIT License granting permission with credit requirement.
- **No build steps** or dependencies beyond a modern browser.

## Contributing

- Feel free to fork and submit pull requests.  
- Keep credit in header and LICENSE intact.

## License

Distributed under the MIT License.  
See `LICENSE` for details.

---

*Developed by ArantxaGC © 2025*
