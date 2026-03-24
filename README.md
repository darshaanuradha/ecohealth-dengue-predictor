
# EcoHealth: Dengue Outbreak Predictor 
**A Climate-Integrated Disease Surveillance System for Sri Lanka**



**Live Deployment URL:** 

---

## 📖 1. Project Overview
**EcoHealth** is a predictive, web-based surveillance system designed to shift dengue control in Sri Lanka from a reactive response to proactive, data-driven planning. By integrating environmental weather patterns (rainfall, temperature, humidity) with clinical hospital records, the system calculates a time-lagged **Dengue Risk Score (0-100)** for specific districts, providing health authorities with a 2–4 week early warning window.

### The Problem & Research Gap
* **The Problem:** Current dengue monitoring systems in Sri Lanka are predominantly reactive, focusing on recording cases only *after* infections occur. This leads to hospital overcrowding, resource shortages, and delayed vector-control interventions.
***The Gap:** There is a distinct absence of integration between environmental climate data and public health surveillance systems at the district level[cite: 34]. Existing tools do not offer a widely deployed 2–4 week predictive window that accounts for the incubation and mosquito breeding cycles.


2. Repository Structure
Following professional modular architecture, the repository is organized as follows:

```text
ecohealth-dengue-predictor/
│
├── src/                # Core Django application code (Interface, Domain, Persistence layers)
├── tests/              # Unit and Integration test scripts
├── data/               # Sample CSV datasets (Historical hospital admissions, weather logs)
├── docs/               # Technical reports, ERDs, Architecture diagrams, Five Whys analysis
├── requirements.txt    # Pinned Python dependencies
├── .gitignore          # Ignored files and environment variables
└── README.md           # Project documentation

3. Setup and Installation Instructions
Follow these steps to run the EcoHealth project locally.

Prerequisites: Python 3.10+ and Git installed on your machine.

1. Clone the repository:

Bash
git clone https://github.com/darshaanuradha/ecohealth-dengue-predictor.git
cd ecohealth-dengue-predictor
2. Create and activate a virtual environment:

Windows:

Bash
python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
4. Run database migrations (SQLite):

cd src
python manage.py makemigrations
python manage.py migrate
5. Start the development server:

python manage.py runserver
The application will now be running locally at http://127.0.0.1:8000/.




