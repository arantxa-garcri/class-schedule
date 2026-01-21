# Semester Sessions Calculator 📚⏱️

A lightweight, single-file web app to calculate how many class sessions and hours you will have during a semester **per group**, automatically excluding **holidays** and **vacation periods**.  
It also generates a **PDF report** with all sessions, totals, and (optionally) **unit completion milestones** (e.g., _“Se completa Unidad 1”_).

---

## ✨ Features

- ✅ Add **multiple groups** with different weekly schedules (e.g., Mon 2h, Tue 2h, Fri 1h)
- 🗓️ Define a **semester date range**
- 🚫 Exclude:
  - 🎉 **Holidays** (single dates)
  - 🏖️ **Vacations** (date ranges)
- 🧮 Generate a detailed **report per group**:
  - session list with dates
  - total sessions
  - total hours
  - cumulative hours
- 📄 Export a **PDF** (browser-side) with:
  - summary table by group
  - full session tables per group
- 🧩 Optional: **Units plan** per group to compute:
  - **“Se completa Unidad X”** date
  - whether hours **fit**, **fall short**, or **exceed** the unit plan

---

## 🧠 Unit Completion (Curriculum Fit)

Many courses have a curriculum organized into units with assigned hours.  
This app can contrast:

- **Planned calendar hours** (your real sessions after exclusions)
vs
- **Required unit hours** (sum of units)

It then reports:

- 📌 **Se completa Unidad 1 / 2 / 3…** (date when cumulative hours reach each unit threshold)
- ⚠️ **Faltan X horas** (not enough calendar hours to finish all units)
- ✅ **Encaja exacto** (perfect match)
- 🟡 **Sobran X horas fuera del plan** (extra hours you can use for review, exams, projects, contingencies)

---

## 🚀 Quick Start

### Option A: Just open the file (recommended)
1. Download or clone this repo
2. Open `index.html` in your browser (Chrome, Firefox, Edge, Safari)

### Option B: Run a tiny local server (helps with some browser settings)
```bash
# Python 3
python -m http.server 8000
```
Then open:
- http://localhost:8000

---

## 🧭 How to Use (English)

1. **Set semester range**
   - Choose `Start` and `End` dates.
2. **Add exclusions**
   - Add **holidays** (single dates)
   - Add **vacations** (start/end ranges)
3. **Add a group**
   - Name the group (e.g., `1022`)
   - Add weekly schedule rows (weekday + hours)
   - (Optional) Add **units** (name + hours)
   - Click **Save group**
4. **Calculate**
   - Click **🧮 Calculate**
5. **Export PDF**
   - Click **📄 PDF**

---

## 🇲🇽 Instrucciones rápidas (Español) 😄

1) **Define el semestre** 🗓️  
   - Captura la fecha de **inicio** y **fin**.

2) **Agrega exclusiones** 🚫  
   - Festivos 🎉 (fecha suelta)  
   - Vacaciones 🏖️ (rango de fechas)

3) **Registra un grupo** 👩‍🏫  
   - Nombre del grupo (ej. `1042`)  
   - Horario semanal (día + horas) ⏱️  
   - (Opcional) Plan de **unidades** (Unidad 1: 20h, Unidad 2: 24h…) 🧩

4) **Calcula** 🧮  
   - El reporte mostrará sesiones, horas y acumulado.

5) **Revisa “Se completa Unidad X”** ✅  
   - Verás la fecha en que se completa cada unidad (si capturaste unidades).

6) **Exporta el PDF** 📄  
   - Incluye tablas por grupo, resumen y unidades.

---

## 🗂️ Data Model (Conceptual)

Each group is stored roughly as:

- `name`: string  
- `schedule`: list of `{ weekday, hours }`  
- `units` (optional): list of `{ name, hours }`

Session generation is chronological:

- A date becomes a session if:
  1) it matches a scheduled weekday, and  
  2) it is **not** excluded by holidays/vacations.

Unit completion is computed by cumulative hours reaching each unit threshold.

---

## 📄 PDF Export Details

The PDF is generated entirely in the browser using:

- **jsPDF**
- **jsPDF-AutoTable**

No server required ✅

---

## 🤝 Contributing

Forks and contributions are welcome! 🎉

- 🍴 You can freely **fork** this project and build on it.
- ✅ Please **give credit** and reference the original project/repo when you share or publish derivatives.
- 🧪 PRs are encouraged (bug fixes, UX improvements, new features, docs).

---

## 🧾 License (MIT)

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute it, including commercially, under the terms of the license.

---

## 🙌 Credits

Created and maintained by the project authors and community contributors.  
If you build something cool with it, consider sharing it back as a PR. 🚀
