# 🏔️ Himalayan Climbing Expeditions — Data Cleaning & Visualisation

> A group data analysis project exploring factors that affect expedition success in the Nepal Himalaya.  
> Conducted as part of coursework (DSA2101) at the National University of Singapore (NUS).

---

## 📌 Project Overview

Using data from the [Himalayan Database](https://github.com/rfordatascience/tidytuesday/tree/main/data/2025/2025-01-21) — the most comprehensive record of mountaineering in the Nepal Himalaya — our team of 6 investigated: **what factors affect expedition success?**

Out of 844 expeditions between 2020–2024, the overall summit success rate was approximately **72.5%**, leaving over 230 unsuccessful climbs. We examined variables such as team size, hired personnel, supplemental oxygen use, and peak height to identify what tips the odds toward success or failure.

---

## 👤 My Contribution

I was responsible for **Plot 2: Effect of Peak Height on Death Rate**, which involved:

- Merging `exped_tidy` and `peaks_tidy` datasets by `PEAKID` to obtain peak heights
- Filtering and cleaning the data — removing zero-member expeditions, ambiguous termination codes (12, 13, 14), and deduplicating by expedition ID
- Engineering new features: `PEOPLE` (members + hired staff) and `DEATHS` (member + hired deaths)
- Computing death rates per peak and excluding peaks with fewer than 20 climbers for statistical reliability
- Designing and implementing a **scatter plot with LOESS smoother** using `ggplot2`, annotating key peaks and highlighting the 8,000m "Death Zone" threshold

---

## 📊 Visualisations

### Plot 1 — Expedition Group Size and Success *(teammates)*
A density plot comparing group size distributions for successful vs. failed expeditions, split by whether hired staff were used.

**Key finding:** Without hired staff, failures concentrate in very small teams (~5 members). With hired support, team size becomes far less critical.

---

### Plot 2 — Effect of Peak Height on Death Rate *(my contribution)*
A scatter plot with a LOESS trend line showing how death rates vary across peaks of different heights, for successful climbs only.

**Key finding:** Death rates increase sharply beyond **8,000m** — the "Death Zone" — where reduced atmospheric pressure, extreme cold, unpredictable weather, and intense UV radiation combine to raise fatality risk significantly.

---

### Plot 3 — Oxygen Use and Peak Height *(teammates)*
A grouped bar chart showing success rates across height categories, broken down by whether supplemental oxygen was used.

**Key finding:** Oxygen use is strongly associated with success above 8,000m. Non-oxygen climbers see a steady drop in success rates as altitude increases.

---

## 🧰 Tools & Libraries

- **Language:** R
- **Libraries:** `tidyverse`, `ggplot2`, `ggthemes`, `ggrepel`, `lubridate`, `tidytuesdayR`

---

## 📁 Files

| File | Description |
|------|-------------|
| `Himalayan_Climbing_Expeditions.Rmd` | Full R Markdown source with all code and analysis |
| `Himalayan-Climbing-Expeditions.pdf` | Rendered report with visualisations and writeup |

---

## 📚 Data Source

- **TidyTuesday Week 3, 2025** — [The History of Himalayan Mountaineering Expeditions](https://github.com/rfordatascience/tidytuesday/tree/main/data/2025/2025-01-21)

---

## 👥 Team

Group project (6 members) — NUS DSA2101, April 2025.
