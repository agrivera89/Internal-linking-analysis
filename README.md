Screaming Frog Internal Link Analyzer
An automated Python-based utility to audit and visualize internal linking structures. This script processes Screaming Frog "All Inlinks" bulk exports to quickly isolate broken links, redirects, and non-standard link types (JavaScript, Canonical, etc.) that reside within your website's internal structure.

🚀 The Problem it Solves
Screaming Frog bulk exports often contain hundreds of thousands of rows, mixing internal and external data. Manual filtering is time-consuming. This tool:

Separates Outbound vs. Inbound: Focuses purely on the internal site architecture.

Identifies "Non-200" Placements: Instantly maps where 404s and 301s are triggered (Hyperlinks vs. JavaScript vs. Images).

Automated Segmentation: Exports specific broken link lists into organized CSVs for developer hand-off.

📊 Key Visualizations
Status Code Heatmap
The core of the analysis is a Seaborn heatmap that correlates Link Type (Y-axis) with Status Code (X-axis). This allows you to see, for example, if your 404 errors are coming primarily from hard-coded hyperlinks or dynamically injected JavaScript files.

🛠️ How It Works
Data Ingestion: Load your all_inlinks.csv from Screaming Frog.

Internal Filtering: The script filters the Destination column to match your root domain, stripping away external noise.

Link Type Summary: Aggregates link counts by category (Hyperlink, Image, CSS, JavaScript, etc.).

Health Check: Summarizes status counts (OK, Not Found, Moved Permanently).

Automated Export: Any group containing non-200 status codes is automatically exported to a dedicated CSV file in the /inlink_exports/ folder for easy sharing with dev teams.

💻 Usage
Export the All Inlinks report from Screaming Frog.

Place the CSV in the same directory as the notebook.

Update the file_path and root_domain variables in the second cell.

Run all cells to generate reports and visualizations.

📦 Requirements
Python 3.x

Pandas

Matplotlib

Seaborn
