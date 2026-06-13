# ATMA_App_V1
the source for ATMA web app
# ATMA Application

The official cross-platform application for the **ATMA (Association of Traditional Martial Arts)**. Built using **Flutter** and powered by a serverless **Firebase** backend, this system is architected to manage student registration, curriculum progression, and an advanced fitness tracking engine with strict data integrity safeguards[cite: 1].

---

## 🚀 Core Project Roadmap

Development is structured into a 6-stage build order to ensure infrastructural stability before adding visual features.

| Stage | Phase Name | Key Focus |
| :---: | :--- | :--- |
| **1** | **The Sovereign Foundation** | Core Infrastructure & Environment Setup (Current Phase) |
| **2** | **The Visual & Identity Layer** | UI/UX, Branding & Custom Belt Widget |
| **3** | **Onboarding & Safeguarding** | User Access, Security, and Age-Based Handover Workflows |
| **4** | **Data Migration & Benchmarking** | The Engine, Historical Schema Validation & Seeding |
| **5** | **Training & Performance** | Student Value-Add Features & Interactive Tracking |
| **6** | **Leadership Handover & Launch** | Production Deployment & Admin Handover |

---

## 🛠️ Architecture & Technical Specifications

### 1. The Dynamic Exercise Engine
The fitness platform is explicitly designed to be **Exercise-Agnostic** using a strategy called **Historical Snapshotted Logging**[cite: 1]. 
* **`exercises`**: Master list with soft delete capabilities and version-aware tracking[cite: 1].
* **`fitness_benchmarks`**: Target rules and goals assigned to ranks[cite: 1].
* **`fitness_logs`**: An immutable historical ledger[cite: 1]. Instead of referencing external benchmarks that might change in the future, each entry saves an immutable snapshot (`snapshotTarget` and `snapshotType`) directly inside the document to preserve historical student accuracy[cite: 1].

### 2. Universal Belt Widget
A highly reusable UI component tracking the traditional ATMA rank structure from **10 Gup (White Belt)** up to **9th Dan (Grand Master)**[cite: 1]. This widget is universally injected into:
* All student registration screens (next to names)[cite: 1].
* Fitness log history entries[cite: 1].
* Curriculum requirement pages[cite: 1].

### 3. Safeguarding & 18th Birthday Handover
To stay fully compliant with safeguarding data standards, the platform runs a specialized transition protocol when a student turns 18:
* Triggers an automated admin dashboard flag for review.
* Prompts the guardian via automated notification to authorize profile handover.
* Issues a secure token to the student to establish an independent adult profile while migrating all historical logs and belt achievements seamlessly.

---

## 💻 Local Development Setup (Windows 11 + VS Code)

### Prerequisites
Ensure your local Windows machine has the required development toolchains installed and configured.

1. **Verify Dependencies**
   Open terminal and check that the core compilers are present:
```powershell
   git --version
   node --version
   flutter doctor
