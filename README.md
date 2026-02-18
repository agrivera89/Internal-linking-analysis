# Screaming Frog Internal Link Analyzer 🐸🔍

An automated Python utility designed to audit and visualize internal linking structures. This script processes **Screaming Frog "All Inlinks"** bulk exports to isolate broken links, redirects, and non-standard link types that reside within your website's internal architecture.

## 🚀 Key Features

* **Noise Reduction:** Automatically separates outbound links from internal ones so you only audit the link equity you control.
* **Link Type Profiling:** Aggregates and counts link types including JavaScript, Hyperlinks, Images, and Canonical tags.
* **Status Visualization:** Provides a quick summary of page status codes (e.g., Moved Permanently, Not Found, OK).
* **Heatmap Analysis:** A Seaborn-powered heatmap that maps **Link Type** (Y-axis) against **Status Code** (X-axis) to pinpoint precisely where non-200 links live.
* **Batch Export:** Automatically generates individual CSV reports for every non-200 link category in a dedicated folder for easy developer hand-off.



## 🛠️ Getting Started

### 1. Requirements
Ensure you have the following Python libraries installed:
```bash
pip install pandas seaborn matplotlib
