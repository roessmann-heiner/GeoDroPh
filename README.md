# GeoDroPh – Direct Georeferencing of Drone Photos

GeoDroPh is a QGIS plugin that performs rapid direct georeferencing of DJI drone photos using onboard GNSS/IMU data.  
It calculates the positions and footprints of aerial images and enables 2D and 3D visualization for a quick review
of the aerial survey. It performs rectification of nadir photos and imports them—along with positions, footprints,
flight path, and user-defined layers—directly into QGIS for further spatial analysis.

GeoDroPh is designed for:
- emergency response teams (fire rescue, disaster response, wildlife conservation)
- drone teams that want to check drone images taken on-site immediately
- users who require fast georeferenced imagery without full photogrammetric processing

---

## 📸 Screenshots

### GeoDroPh

#### XY visualisation of the aerial survey
![GeoDroPh XY Layer](docs/Screenshot_XY_1.png)

Further views:

- 📷 [XZ visualisation of the aerial survey](docs/Screenshot_XZ.png)
- 📷 [3D visualisation of the aerial survey](docs/Screenshot_3D_1.png)

### QGIS

#### Camera positions and orientations
![Camera Positions and Orientations](docs/Screenshot_QGIS_Camera_Positions.png)

Further views:

- 📷 [Nadir Photo and Corresponding Map Section](docs/Screenshot_QGIS_SimultaneousNadirView.png)
- 📷 [Oblique Photo and Corresponding Map Section](docs/Screenshot_QGIS_SimultaneousObliqueView.png)
- 📷 [Rectified Drone Photo](docs/Screenshot_rectification.png)

Image Credits:
The background orthophotos shown in the screenshots are provided by GeoBasis NRW.
© GeoBasis NRW

---

## 🚀 Features

- **Fast direct georeferencing** of nadir as well as oblique drone photos
- **Using EXIF GPS/IMU metadata**
- **Computation of positions, footprints and flight path**
- **2D and 3D visualization** for reviewing the aerial survey   
- **Rapid rectification** of nadir images  
- **Automatic import** of GeoDroPh results into QGIS
- **Optional import** of map layers prepared by the user
- **Simultaneous display** of original drone images and the corresponding map section
- **Display of rectifications** on map layers

---

## 🛠 Requirements

GeoDroPh supports the following QGIS versions:

- **QGIS 3.28 LTR – QGIS 3.40.8 (Qt5)**  
- **QGIS 4.2 and newer (Qt6)**

GeoDroPh does **not** support:

- **QGIS 3.40.9 – QGIS 4.0.3**
  (these versions use early Qt6 bindings and contain breaking API changes)

The plugin will install in these versions, but **it will not start**, because GeoDroPh performs an internal version check to prevent crashes.

---

## 📥 Installation

### 🔹 Still in Progress: Installation from the QGIS Plugin Repository

1. Open **QGIS**
2. Go to **Plugins → Manage and Install Plugins**
3. Search for **GeoDroPh**
4. Click **Install Plugin**

GeoDroPh will appear in the **Plugins** menu.

**Note:**  
The plugin requires Phil Harvey’s ExifTool.
As executables cannot be copied automatically from the QGIS plugin repository as part of the
GeoDroPh installation, a system-wide installation of ExifTool is **required**.

---

### 🔹 Installation from GitHub (ZIP package)
Do not use the automatically generated GitHub "Source code (zip)" or "Source code (tar.gz)".
Download the GeoDroPh release ZIP instead.

1. Download the latest release ZIP from GitHub  
2. In QGIS, open **Plugins → Manage and Install Plugins → Install from ZIP**
3. Select the downloaded ZIP file
4. Click **Install Plugin**

**Note:**  
The GitHub ZIP package includes `exiftool.exe` and `exiftool_files`.  
A system-wide ExifTool installation is **not required**.

---

## 🧩 Troubleshooting

### GeoDroPh does not start
GeoDroPh performs an internal version check.  
The plugin will not start in QGIS versions **3.40.9 – 4.0.3**, because these releases contain unstable Qt6 bindings and breaking API changes.

### ExifTool not found
- If installed from QGIS Repository → install ExifTool system‑wide  
- If installed from GitHub ZIP → ensure `exiftool.exe` and `exiftool_files` are present in the plugin directory

---

## 📦 Downloads

The latest GeoDroPh installation package can be downloaded from the GitHub Releases page.

[Download GeoDroPh Releases](https://github.com/roessmann-heiner/GeoDroPh-Preview/releases)

---

## 🐞 Bug Reports and Feature Requests

Please use the GitHub Issues page to report bugs, suggest improvements or request new features.

[Open an Issue](https://github.com/roessmann-heiner/GeoDroPh-Preview/issues)

---

## 📄 License

GeoDroPh is licensed under the **GNU General Public License v2.0 or later (GPLv2+)**.

See the included `LICENSE` file for details.

---

## ⚠️ Disclaimer
GeoDroPh is provided "as is", without warranty of any kind.
Users are responsible for verifying the correctness of all generated coordinates, 
footprints, orientations and rectified images before using them for operational, legal, surveying or safety-critical purposes.

---

## 🛰 Acknowledgements

- QGIS Plugin Builder  
- ExifTool by Phil Harvey  
- QGIS community and developers
