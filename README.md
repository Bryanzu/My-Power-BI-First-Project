# Data Jobs Dashboard — Power BI

![Dashboard_image](images/Dashboard_vid.gif)

A Power BI dashboard built to explore data job trends, salaries, and market insights using a real-world dataset. This is my first Power BI project.

---

## Dataset

**Source:** Data Jobs dataset compiled by Luke Barousse

The dataset covers job postings across various data roles and includes information like job title, company, location, salary (hourly and yearly), job schedule type, posting platform, remote work availability, health insurance, and required skills.

---

## Dashboard Overview

The report has two pages: a main dashboard and a drill-through detail page.

### Page 1 — Data Job Dashboard

![Data Job Dashboard](/images/Dashboard_1.png)

An interactive overview of the data jobs market in 2024. A **Job Title slicer** at the top lets you filter everything on the page, and a **Clear All button** resets the filter. You can also click any job in the visuals and use the **Drill Through to Job Title** button to jump to the detail page.

**KPI Cards**

- **Job Count** — total number of job postings (sourced from the `job_title_short` column)
- **Salary Star Rating** — a custom measure that converts median salary into a 1–5 star rating
- **Median Yearly Salary** — derived from `salary_year_avg` using a median measure
- **Median Hourly Salary** — derived from `salary_hour_avg` using a median measure

**Visuals**

- **Job Trend in 2024** (line chart) — tracks job posting volume month by month. X-axis: `job_posted_date`, Y-axis: `job_title_short` count
- **Hourly vs Yearly Salary** (scatter chart) — plots each job title by its median yearly salary (X) against median hourly salary (Y), showing which roles pay more across both pay structures
- **Highest Paying Jobs in Data** (bar chart) — ranks job titles by median yearly salary. Y-axis: job title, X-axis: median yearly salary
- **Job Summary Table** (matrix) — shows job title and posted date as rows, with job count, yearly salary, hourly salary, and job trends (sparklines) as values

---

### Page 2 — Job Title Drill Through

![Job Title Drill Through](/images/Drill_Through.png)
Accessible from Page 1 by selecting a job title and clicking the drill-through button. Displays a focused breakdown for the selected role.

**Visuals**

- **Salary Gauges** — gauge charts showing median yearly and hourly salary with min/max context
- **Work From Home (WFH) %** (donut chart) — percentage of postings that offer remote work
- **No Degree Mention %** (donut chart) — percentage of postings that don't require a degree
- **Health Insurance %** (donut chart) — percentage of postings that mention health insurance
- **Where Are Jobs Globally?** (map) — geographic distribution of job postings worldwide
- **Top Job Posting Platforms** (bar chart) — which platforms (LinkedIn, BeBee, Indeed, etc.) have the most listings
- **Type of Data Jobs** (treemap) — breakdown of job schedule types (full-time, contract, part-time, etc.)

---

## What I Learned

This project was my introduction to Power BI. Key things I picked up:

- Creating **KPI cards** and usiing **Quick measures** (median salary, star rating)
- Building a **line chart** to track trends over time
- Using a **scatter chart** to compare two salary dimensions at once
- Creating a **matrix table** with sparklines for job trend visualization
- Setting up a **slicer** with a custom **Clear All button**
- Configuring a **drill-through page** with a navigation button
- Using **map visuals** to show geographic data
- Working with **donut charts** and **treemaps**

---

## Tools Used

- Microsoft Power BI Desktop
- Git

---

## Author

Bryan
