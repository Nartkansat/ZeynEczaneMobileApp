# 📱 Zeyn Pharmacy - Mobile Scanner & Management App

![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)

> **⚠️ Important Note:** Due to security and privacy policies, the source code of this repository is kept closed (Closed-Source).

## ⚙️ Backend & API
This application consumes the ZeynPharmacy RESTful API built with ASP.NET Core and Clean Architecture.
👉 **[Click here to view the ZeynPharmacy Backend Repository](#)** 

---

## 🚀 Core Objectives & Solutions
Zeyn is a smart data scanning and management solution developed to digitalize pharmacy workflows and increase operational efficiency. The application is specifically optimized for bulk data processing and secure document sharing needs of pharmacists.

*   **Multi-QR Management:** Scans multiple QR codes simultaneously, transferring them to a common data pool and allowing seamless sharing with other pharmacies.
*   **Rapid Stock Inventory:** Eliminates manual processes by enabling stock counting within seconds via the device camera.
*   **Secure Document Transfer:** Digitalizes physical documents and ensures their secure transfer over an encrypted infrastructure.

---

## 🏗️ Mobile Architecture & Folder Structure

The application is structured using a feature-based architecture to ensure scalability and ease of maintenance within the Flutter ecosystem:

```text
📂 zeyn_mobile_app
 ┣ 📂 lib
 ┃ ┣ 📂 core               # Constants, Themes, Network Configurations & Utils
 ┃ ┣ 📂 features           # QR Scanner, Auth, Dashboard, Inventory Modules
 ┃ ┣ 📂 shared             # Common Widgets, UI Components & Helpers
 ┃ ┗ 📜 main.dart          # Application Entry Point
 ┣ 📂 assets               # Images, Icons, and Fonts
 ┗ 📜 pubspec.yaml         # Project Dependencies & Configurations

## 🧩 Application Modules

### 1. Authentication
To maintain maximum application security, registration is exclusively handled via the centralized admin panel. Users securely access the system using their pre-registered credentials; direct registration via the mobile app is disabled.

### 2. Dashboard
The centralized management hub to monitor the pharmacy's daily operational status in real-time.
*   **Data Tracking:** Total number of scanned codes and the volume of data transmitted today.
*   **Group Information:** Associated pharmacy group and the number of other pharmacies within the network.
*   **Status Notifications:** Tracking of pending QR codes stored in local memory that have not yet been transmitted to the system.

### 3. Multi-Scan (QR Reader)
Utilizing advanced image processing technology, it simultaneously identifies multiple medications within the camera's field of view and rapidly transfers them to the list.
> **Note:** The application's greatest advantage is its ability to read multiple products simultaneously with a single camera angle.

### 4. QR List
The management panel where scanned medications are detailed (Barcode, Name, etc.).
*   **Editing:** Ability to copy, delete, or perform bulk operations on selected codes.
*   **QR Consolidation:** Converts all data in the list into a single, unified QR code. When this generated QR is scanned, the barcodes of all contained medications are processed in bulk.

### 5. Stock Counting
Optimizes stock counting processes with a rapid scanning mode.
*   **Export Options:** Export counting results directly to the centralized system or export them locally in **Excel** format.

### 6. Document & QR Decoding
*   **Archiving:** Scans physical documents and uploads them to the system via encrypted protocols.
*   **Photo Decoding:** Allows users to decode QR codes from previously taken photos by selecting them directly from the device gallery.

---

## 🛠 Technical Advantages
*   **Speed:** Dozens of data entries in seconds with multi-object detection.
*   **Security:** End-to-end encryption during document transmission.
*   **Flexibility:** Seamless Excel integration and advanced bulk processing capabilities.

---

## 📸 Screenshots

<img src="https://github.com/user-attachments/assets/6cb936ba-8a75-4662-b86b-6d66bbda5a81" alt="Zeyn Mobile App Screenshot" width="300">
