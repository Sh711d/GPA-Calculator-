# GPA Calculator

A simple desktop GPA calculator built with PyQt5. Add your courses, credits, and grades to a table, and instantly calculate your semester GPA. Optionally, factor in your previous GPA and credits to get your cumulative GPA.

## Screnshot

https://github.com/user-attachments/assets/be9bd412-f515-459c-8b7a-1702ee3f0c0f


## Features

- Add unlimited course rows to a table
- Select grades from a dropdown (A+ to F)
- Enter credit hours per course
- Calculate semester GPA with one click
- Optional **Cumulative GPA** mode — combine previous GPA/credits with the current semester
- Reset button to clear results and start over
- Clean, styled UI with a purple theme

## Grading Scale

| Grade | Points |
|-------|--------|
| A+    | 4.0    |
| A     | 3.75   |
| B+    | 3.5    |
| B     | 3.0    |
| C+    | 2.5    |
| C     | 2.0    |
| D+    | 1.5    |
| D     | 1.0    |
| F     | 0.0    |

## Project Structure
├── main3.py              # PyQt5 GUI (front-end)

├── gpa_calcBE.py         # GPA class (back-end calculation logic)

└── README.md

## Requirements

- Python 3.7+
- PyQt5

## Installation

```bash
git clone https://github.com/Sh711d/main3.git
cd main3
pip install PyQt5
```

## Usage

Run the application:

```bash
python main3.py
```

1. Click **Add Course** to add a new row.
2. Enter the number of credits for each course.
3. Select the grade you received from the dropdown.
4. Click **Calculate GPA** to see your semester GPA.
5. (Optional) Check **Cumulative GPA Option**, enter your previous GPA and previous attempted credits, then click **Calculate Cumulative** to see your overall GPA.
6. Click **Reset** to clear the GPA and cumulative fields.

## How It Works

The `GPA` class (in `gpa_calcBE.py`) handles the math:

- `calculate_semester_gpa()` — sums grade points × credits across all entered courses and divides by total credit hours.
- `calculate_cumulative_gpa()` — combines previous GPA/credit history with the current semester's totals to compute an overall cumulative GPA.

## License

MIT
