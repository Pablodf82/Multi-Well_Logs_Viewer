# 📊 Multi-Well Drilling & Petrophysical Logs Viewer

An open-source, client-side engineering toolkit designed for logs visualization, processing, and seamless benchmarking of Log ASCII Standard (`.LAS`) telemetry datasets.

> 💡 **Live Demo:** [Insert your GitHub Pages link here once active, or delete this line]

---

## 🎯 The "Why" Behind this Project

In drilling operations, legacy enterprise platforms like **Well Advisor** introduce significant friction and complexity when engineering teams need to benchmark and cross-examine multiple wells simultaneously for drilling parameters comparison. 

I designed **Logs Viewer** to eliminate this operational bottleneck. It is a pure, lightweight, client-side application that allows instant drag-and-drop ingestion of multiple `.LAS` datasets, empowering engineers to overlay, align, and compare multi-well physics-based curves very rapidly.

---

## 📸 Interface Preview

![Live Demo](./demo.gif)
*Placeholder: This GIF demonstrates instant multi-well loading, wells selection, interactive tab switching, traces selection and axis tuning.*

---

## 🛠️ Core Architecture & Features

### 1. Mechanical Drilling Parameters (DP Tab)
* **Multi-Well Telemetry Processing:** Dynamic overlay and plotting of ROP, WOB, Torque, RPM, Flow Rate, and Standpipe Pressure (SPP) across multiple datasets.
* **Signal Smoothing:** Integrated client-side moving average filters to clean high-frequency sensor noise and expose true drilling trends.
* **Smart Ingestion Engine:** Automated parsing and unit standardization (e.g., converting GPM to LPM, and PSI to Bar) derived from log mnemonic headers.

### 2. Energy & Mechanical Efficiencies (MSE Tab)
* **Physics-Based Analytics:** Automated computations of Mechanical Specific Energy (**MSE**), Hydraulic Specific Energy (**HSE**), and Total Volumetric Energy (**FMSE**). 
* **Subsurface Geometric Baseline:** Calculations autonomously utilize a standardized 12.25" bit diameter cross-sectional area configuration to compute accurate energy thresholds in real time.
* **Hydraulic Contribution:** Computes the Hydraulic Contribution Ratio (**HCR**) to diagnose and flag under-optimized bit hydraulics.
* **Trajectory Integration:** Incorporates a **Minimum Curvature Engine** mathematical pipeline to accurately project Measured Depth (MD) into True Vertical Depth (TVDRT).

### 3. Logging While Drilling / Petrophysics (LWD Tab)
* **Formation Evaluation:** Multi-well correlation tracks for Gamma Ray (GAPI) and Deep/Shallow Resistivity (Ohm-m).
* **Porosity & Lithology Overlays:** Standardized engineering grids for Bulk Density (RHOB) and Neutron Porosity (NPHI) leveraging inverted scales for standard log analysis.

---

## 🚀 How to Run the Project Locally

Since the application is built entirely on standard client-side web technologies (HTML5, CSS3, vanilla JavaScript, and Plotly.js), **it requires no complex environment installations, no Python dependencies, and no local server overhead.**

### 📋 Prerequisites & Data Format
⚠️ **CRITICAL REQUIREMENT:** This application is strictly designed to parse and process **standard Log ASCII Standard (`.LAS`) files** (the universal format for well logging telemetry data). It will **NOT** accept Excel, PDF, or CSV files. 

---

### 🛠️ Step-by-Step Setup

1. **Clone this repository to your local machine:**
   Run the following command in your terminal:
   git clone [https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git](https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git)

2. **Launch the Interface:**
   Go to your local project folder, locate the index.html file, and open it directly by double-clicking it. It will initialize instantly.
   *(Note: Successfully tested and verified on Microsoft Edge. Compatibility with other browsers has not been tested yet).*

3. **Ingest and Compare .LAS Files:**
   Select your target .LAS telemetry files on your computer, then drag and drop them simultaneously into the web ingestion panel. The pipeline will automatically decode the underlying mnemonics, standardize the engineering metrics, and render the interactive multi-well benchmark plots very rapidly.