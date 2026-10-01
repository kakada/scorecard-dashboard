# Scorecard Dashboard – User Manual

This manual explains how to read and use the **Scorecard Dashboard**, which summarises scorecard activity from the CSC web platform: how many scorecards were planned and conducted, where, who took part, which criteria were raised, and how the data is being reviewed.

It is written for program staff, M&E officers and partners who **view** the dashboard. You do not need to know SQL or Grafana.

---

## 1. Quick start

1. Open the dashboard URL given to you by your administrator.
2. Click **Sign in with CSCWEB** and log in with your normal CSC web account.
3. The dashboard opens on the home page, showing **all programs, all provinces, last 12 months**.
4. Use the **filters** at the top to narrow down what you see (Section 4).
5. Change the **time range** at the top right if you need a different period (Section 5).
6. Switch **Language** between ខ្មែរ and English to change panel titles and labels (Section 6).

> New accounts are created automatically on first sign-in with the **Viewer** role. Viewers can filter and explore the data but cannot edit the dashboard.

---

## 2. Screen layout

```
┌──────────────────────────────────────────────────────────────────────┐
│ Filters:  Program │ Year │ Province │ Service │ Type │ NGO │ Inst │ Language │
│                                          Time range ▾   Refresh ⟳    │
├───────────────┬──────────────────────────────────────────────────────┤
│               │  Total scorecards      │  Entered after impl. date   │
│  Map of       ├──────────────────┬─────┴─────────────────────────────┤
│  provinces    │  Completion rate │  Geographic coverage              │
│               ├──────────────────┴───────────────────────────────────┤
│               │  Implementation duration (min / avg / max days)      │
├───────────────┴──────────────────────────────────────────────────────┤
│ Data quality │ Beneficiary reach                                     │
│ FAM reporting views (device pie + detail table)                      │
│ Participants and indicators summary                                  │
│ Charts by service, scorecard type, device                            │
│ Participants by gender / age / profile                               │
│ Top 5 criteria (proposed, prioritised, happy / neutral / angry)      │
│ Activities by waste-management category                              │
└──────────────────────────────────────────────────────────────────────┘
```

Scroll down to see all sections. Everything on the page responds to the same filters and time range, except where noted in Section 7.

---

## 3. Signing in

- The dashboard uses single sign-on through **CSCWEB**. Use the same account you use for the CSC web platform.
- Self-registration is disabled. If you cannot sign in, ask your administrator to make sure your CSC web account exists and has access.
- If you are signed out, your filters are lost. Sign in again, or open a saved link (Section 8.4) to restore them.

---

## 4. Filters

The filters sit in the bar at the top of the page. Every filter is **multi-select** and starts on **All**.

| Filter | What it does |
|---|---|
| **Program** (កម្មវិធី) | Limits everything to one or more programs. |
| **Year** (ឆ្នាំ) | The scorecard year. Only years that exist in the selected program(s) are listed. |
| **Province** (ខេត្ត) | Limits to one or more provinces. |
| **Service** (សេវា) | The service / sector being scored (for example health or education). Only services in the selected program(s) are listed. |
| **Scorecard type** (ប្រភេទប័ណ្ណដាក់ពិន្ទុ) | Self-assessment, community scorecard or combined scorecard. |
| **Local NGO** | Limits to scorecards run by the chosen Local NGO(s). Only NGOs in the selected program(s) are listed. |
| **Institution** | The facility or institution scored, such as a specific health centre or school. Only institutions belonging to the selected service(s) are listed. **មិនកំណត់** (not specified) covers scorecards that have no institution recorded. |
| **Language** | ខ្មែរ or English. See Section 6. |

### How to use a filter

- Click the filter and tick or untick values. Click **All** to select everything again.
- Press **Esc** or click outside the list to apply the change; all panels refresh automatically.
- Type in the filter box to search a long list.

### Filters affect each other

Filters narrow each other from left to right:

- Choosing a **Program** changes the choices in Year, Service, Scorecard type, Local NGO and Institution.
- Choosing a **Service** changes the choices in Institution.

If a filter you expect is missing a value, check that the Program (and Service) selection includes it.

> **Tip:** Set **Program** first, then work your way through the others.

---

## 5. Time range

The time picker is at the top right and defaults to **Last 1 year**.

- Click it to choose a quick range (last 7 days, 30 days, 6 months, 1 year, and so on) or enter an **absolute** From/To date.
- The **refresh** button reloads the data. Use the small arrow beside it to set auto-refresh (5s to 1d), which is normally not needed.

### Which date does the time range use?

Different panels count different events, so the time range is applied to different dates:

| Panels | Time range applies to |
|---|---|
| Planned counts (total planned, completion-rate denominator, geographic target, the "planned" bars, map planned/in-review/rejected figures) | The date the scorecard was **created / planned**. |
| Conducted counts, participants, criteria, waste-management activities, coverage "covered" figures, implementation duration | The date the scorecard was **conducted**. |
| FAM reporting views | The date of each **view event**. |

### Time range and Year work together

The **Year** filter and the **time range** are both applied, and only data matching **both** is shown. If you select Year = 2024 but leave the time range on "Last 1 year", you may see less than you expect. When you want a whole calendar year, set the time range to cover that year (for example 1 Jan 2024 to 31 Dec 2024).

---

## 6. Language

Use the **Language** filter to switch between **ខ្មែរ** (Khmer) and **English**.

It changes:

- Panel titles and their help text (the **i** icon)
- Chart and table labels
- Province, service and category names

It does not change the labels on the filters themselves, criteria names entered by users, or Local NGO names.

---

## 7. Reading the panels

Hover over the **i** icon in the top-left corner of a panel to read its built-in description.

### 7.1 Scorecard status – key terms

| Term | Meaning |
|---|---|
| **Planned** | A scorecard that has been created or scheduled. |
| **In review** | Submitted for review but not yet approved or rejected. |
| **Conducted / Implemented** | Submitted **and approved** (completed). |
| **Rejected** | Sent back or rejected during review. Rejected scorecards are excluded from most participant, criteria and chart figures. |

Deleted scorecards are never counted.

### 7.2 Map of provinces (top left)

Each marker is a province with planned scorecards.

- **Hover** to see a tooltip: *conducted / planned*.
- **Click** for a popup with the province's Local NGOs (links open their websites) and the counts for **Planned, In review, Implemented** and **Rejected**.
- Zooming with the mouse wheel and double-click is turned off so the page scrolls smoothly. Use the **+ / –** buttons on the map and drag to pan.

### 7.3 Summary figures (top right)

| Panel | Shows | How to read it |
|---|---|---|
| **Total scorecards** | Three numbers separated by " / ": **Planned / In review / Conducted** | For example `120 / 8 / 95`. Here "Conducted" means scorecards whose review is finished (approved or rejected). |
| **Entered after the actual implementation date** | Count of completed scorecards whose data was finished on a later day than the day they were conducted | A measure of late data entry. Lower is better. |
| **Completion rate** | Approved conducted scorecards ÷ planned scorecards, as a percentage | Shows a bare `%` (no number) when nothing is planned. |
| **Geographic coverage** | A small table with three rows: **Provinces, Districts, Communes**. Columns are **Covered / Target** and **Coverage rate** | *Covered* = places with at least one approved scorecard. *Target* = places with at least one planned, non-rejected scorecard. |
| **Implementation duration** | **Min / Average / Max** number of days from the conducted date to approval | Rounded to whole days. |

### 7.4 Data quality and beneficiary reach

| Panel | Shows |
|---|---|
| **Data quality** | Total **submitted**, **approved** and **rejected** scorecards, and the number of **custom indicators that were corrected** after they were first entered. A high rejected or correction count suggests a need for follow-up training or supervision. |
| **Beneficiary reach** | Total **participants** from approved scorecards, with counts and percentages of **female, youth, people with disabilities** and **minority** participants. |

### 7.5 FAM reporting views

These two panels track how often the FAM reporting page is opened.

- **Pie chart** – views by device type (mobile, desktop, tablet).
- **Table** – views broken down by device type, operating system and browser, most viewed first.

They follow the **time range only**. The Program, Province and other filters do not apply.

### 7.6 Participants and indicators summary

| Panel | Shows (in order, separated by " / ") |
|---|---|
| **Participants** | Number of **Local NGOs** / number of **CAFs** (community facilitators) / total **participants** / **average participants per scorecard** |
| **Total indicators** | Total indicators **raised** / of which **custom** (added by participants) / of which **selected** for scoring |
| **Average indicators per scorecard** | Same three measures, averaged per approved scorecard and rounded up |

### 7.7 Scorecards by service, type and device

| Panel | Type | Shows |
|---|---|---|
| **Scorecards by service** | Bar chart | **Planned** vs **implemented** for each service. |
| **Implemented by scorecard type and service** | Bar chart | Implemented scorecards for each service, with one bar each for self-assessment, community scorecard and combined. |
| **Implemented by scorecard type** | Pie chart | Share of each scorecard type. |
| **Implemented by service** | Pie chart | Share of each service. |
| **Implemented by device type** | Pie chart | Whether scorecards were run on a **tablet** or a **mobile** phone. |

### 7.8 Participants by gender, age and profile

| Panel | Shows |
|---|---|
| **By gender** | Male, Female, Other. |
| **By age** | Age bands: under 15, 15–30, 31–45, over 45. |
| **By profile** | Participants who are **ID Poor, Disability, Minority** or **Youth**, stacked by gender. One person can belong to more than one profile group, so the bars are not expected to add up to the total number of participants. |

Only participants marked as *countable* on approved scorecards are included.

### 7.9 Top 5 criteria

| Panel | Shows |
|---|---|
| **Top 5 proposed criteria** | The five criteria most often **proposed** (raised) by participants. |
| **Top 5 prioritised criteria** | The five criteria most often **selected** for scoring, counted by the number of scorecards. |
| **Top 5 – happy face** | Criteria receiving the most **positive** votes (score above 3). |
| **Top 5 – neutral face** | Criteria receiving the most **neutral** votes (score equal to 3). |
| **Top 5 – angry face** | Criteria receiving the most **negative** votes (score below 3). |

### 7.10 Waste management categories

A bar chart of the **number of activities** recorded under each waste-management category, taken from approved scorecards. Categories are shown from the most to the least common.

### 7.11 Footer

The bottom of the page shows credits for the co-producers and funders of this version of the dashboard.

---

## 8. Working with panels

### 8.1 Chart interaction

- **Hover** over a bar, slice or table row to see exact values.
- **Click a legend item** to hide or show that series. **Ctrl/Cmd-click** to show only that series.
- **Click a column header** in a table to sort it.

### 8.2 View a panel full-screen

Hover over a panel, click the small menu (⋮) at the top right and choose **View**, or hover and press **v**. Press **Esc** to go back.

### 8.3 See the underlying numbers and download them

1. Open the panel menu (⋮) and choose **Inspect → Data**.
2. Review the table, or click **Download CSV** to open it in Excel or Google Sheets.

The download reflects your current filters and time range.

### 8.4 Share or bookmark a view

Your current filters, language and time range are stored in the web address. Copy it from the browser and send it to a colleague to open the same view. Bookmark it to return to the same view later.

---

## 9. Troubleshooting and FAQ

**A panel says "No data".**
No scorecards match your current filters and time range. Widen the time range, set the filters back to **All**, and check that Year and time range agree (Section 5).

**A filter list is empty or is missing a value I expect.**
Filters depend on Program (and Service). Make sure the correct Program is selected. Filters refresh when the page is reloaded.

**The total on one panel is different from another.**
This is often expected:

- Panels use different dates (planned date vs conducted date, Section 5).
- "Total scorecards" counts a scorecard as *conducted* once its review is finished (approved **or** rejected), while most other panels count **approved** scorecards only.
- Rejected scorecards are left out of participant, criteria and chart figures.
- Participant totals count only *countable* participants.

**A percentage shows only `%`, or the number is missing.**
The panel divides by a total that is zero, for example a completion rate when nothing is planned.

**A panel title shows text like `$scorecard_total_panel_title`, or labels are missing.**
The translation for the selected language could not be loaded. Switch Language and switch back, refresh the page, and report the issue to your administrator if it persists.

**The map is blank or the province shapes are missing.**
Reload the page. If it continues, report it to your administrator, because the map depends on a separate map service that may be unavailable.

**I changed a filter but nothing happened.**
Filters apply after you close the drop-down list. Press **Esc** or click outside the list.

**The page is slow.**
A very wide time range with All filters is the heaviest query. Narrow it to a Program or a shorter period.

**Can I change or add panels?**
Not as a Viewer. Ask your administrator for a new panel or a different breakdown.

---

## 10. Glossary

| Term | Meaning |
|---|---|
| **CSC** | Community Scorecard. |
| **CAF** | Community facilitator attached to a Local NGO who helps run scorecards. |
| **Local NGO** | The local organisation that runs scorecards in a province. |
| **Service / Sector** | The public service being assessed (for example health or education). |
| **Institution / Facility** | The specific site being assessed, such as a health centre or school. |
| **Scorecard type** | Self-assessment, community scorecard, or combined scorecard. |
| **Criteria / Indicator** | A topic raised by participants that is later voted on. |
| **Custom indicator** | A criterion written by the participants rather than chosen from a standard list. |
| **Countable participant** | A participant included in official counts. |
| **FAM** | The reporting page whose views are tracked in the FAM reporting panels. |
