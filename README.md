# Interactive Data Storytelling Lab

Front‑end app that behaves more like an analyst than a static dashboard.  
You upload raw user event logs (CSV) and the UI walks you from **noise → patterns → insights → “what if” decisions**.

---

## Why this project exists

Most dashboards stop at pretty charts. They assume the viewer already knows:

- Which metric actually matters
- Whether a change is “normal” or a problem
- What to do next

This project tries to close that gap from the front‑end side. It takes messy user‑behavior data and turns it into a guided story a product or growth team could actually act on. [web:146][web:149]

---

## What you can do in the app

1. **Stage 1 – Raw data**
   - Upload a CSV of user events: user id, session id, timestamp, page, time spent.
   - See the first 50 rows as‑is, to make it clear how noisy the starting point is.

2. **Stage 2 – Structure & patterns**
   - Aggregate to daily active users, sessions, per‑user time, and top pages.
   - Visualize trends with a Chart.js line chart and a compact “top pages” table.

3. **Stage 3 – Insight engine**
   - Automatically flag spikes and drops in active users using simple rules.
   - Generate an “executive summary” in plain language (strongest page, weakest page, most engaged user, overall trend).
   - Expose the anomaly rules in a small **Insight Rules** panel so you can change thresholds and re‑run the logic.

4. **Stage 4 – Decision simulation**
   - Adjust sliders like “improve onboarding” and “boost engagement”.
   - See a simulated active‑user curve compared with baseline to get an intuitive feel for impact (no ML, just transparent assumptions).

There is also a small **Story Mode** console on the side that updates as you move between stages so viewers understand where they are in the analytical journey. [web:44][web:89]

---

## Tech stack

- **Front end:** HTML, CSS, vanilla JavaScript  
- **Charts:** Chart.js for line charts and simple visuals [web:141]  
- **Data handling:** CSV parsing and aggregation fully in the browser  
- **Architecture:** No backend, no database, no external APIs

---

## How to run locally
clone the repo
git clone https://github.com/kishore0786k/Interactive-data-storytelling-lab.git
cd Interactive-data-storytelling-lab

open in your browser
(on Windows) double‑click index.html
(or) use a simple static server if you prefer

Then:

1. Open `index.html` in your browser.  
2. Upload `data-sample.csv` or your own event log with the same columns.  
3. Walk through the four stages using the buttons at the bottom of each section.

---

## Dataset format

The app expects a CSV with these columns:user_id,session_id,timestamp,page_visited,time_spent_seconds
Example row:U001,S001,2025-11-01 09:15:23,/home,45

You can drop in your own file as long as the headers and order match.

---

## Possible next steps

- Add more segments (e.g., new vs returning users, device types).
- Extend the decision simulation with simple funnels (signup → activation → retention).
- Experiment with different visual encodings and story layouts.

Feel free to open an issue or PR if you have ideas for taking the storytelling further.





