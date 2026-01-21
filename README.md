# 📊 BMW Sales Interactive Dashboard

This project is an interactive analytics dashboard built with **R**, **Flexdashboard**, and **Plotly**. It visualizes BMW sales data (2010-2024), allowing users to explore market trends, price depreciation, and regional preferences through **brushing and linking**.

## 🚀 Live Demo
*(Once you host it, paste your GitHub Pages link here, e.g., https://yourusername.github.io/bmw-dashboard/)*

---

## 📂 About the Data
The dashboard utilizes a dataset of BMW sales records containing approximately 5,000+ rows (sampled for performance).

| Column | Description |
| :--- | :--- |
| **Model** | BMW Car Model (e.g., i3, M3, X5) |
| **Year** | Manufacturing Year (2010–2024) |
| **Price_USD** | Sale Price in US Dollars |
| **Mileage_KM** | Mileage on the odometer (Kilometers) |
| **Region** | Market Region (Europe, Asia, North America, etc.) |
| **Fuel_Type** | Petrol, Diesel, Hybrid, Electric |
| **Transmission** | Automatic vs. Manual |
| **Sales_Classification** | High vs. Low volume categories |

---

## 🛠️ How It Works (The "Magic")
Unlike traditional dashboards (Tableau/PowerBI) or server-based apps (Shiny), this dashboard is **static HTML** but remains **interactive**.

### Key Technologies
* **[Flexdashboard](https://pkgs.rstudio.com/flexdashboard/):** Defines the layout (rows, columns, sidebars).
* **[Plotly](https://plotly.com/r/):** Renders the charts (Scatter plots, Histograms).
* **[Crosstalk](https://rstudio.github.io/crosstalk/):** The engine behind the interactivity. It creates a `SharedData` object that exists purely in the web browser.
* **[DT (DataTables)](https://rstudio.github.io/DT/):** displays the raw data in a searchable, scrollable table.

### Interactivity Features
1.  **Brushing:** Select a group of points on the "Price vs. Mileage" scatter plot using the Box Select tool.
2.  **Linking:** Automatically filters the "Region" and "Transmission" bar charts to show *only* the data you selected.
3.  **Client-Side Filtering:** All filtering happens instantly in your browser—no server required.

---

## 💻 Installation & Usage

### 1. Prerequisites
You need **R** and **RStudio** installed.

### 2. Install Libraries
Open RStudio and run this command in the console:
```r
install.packages(c("flexdashboard", "tidyverse", "plotly", "crosstalk", "DT"))

```

### 3. Run the Dashboard

1. Open `dashboard.Rmd`.
2. Click the **Knit** button in the toolbar.
3. A file named `dashboard.html` (or `index.html`) will be generated and open in your browser.

---

## 🌐 Hosting on GitHub Pages

This project is designed to be hosted for free on GitHub Pages.

1. **Generate HTML:** Knit your `dashboard.Rmd` file.
2. **Rename:** Rename the output file to `index.html`.
3. **Upload:** Push `index.html` and your csv data file to a GitHub repository.
4. **Activate:** Go to Repo Settings -> Pages -> Select `main` branch -> Save.

---

## 📁 Project Structure

* `dashboard.Rmd`: The main source code for the dashboard.
* `bmw_sales_sampled.csv`: The downsized dataset used for the dashboard (optimized for web performance).
* `BMW sales data (2010-2024).csv`: The original full dataset.
* `index.html`: The compiled website (generated after Knitting).

---

## 📝 License

This project is for educational purposes.

---

## 📝 AI Usage

This README.md file has been created using AI.
