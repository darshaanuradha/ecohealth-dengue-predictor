1. Test Scripts (The Python Files)
You should break your tests down into different files based on what they are checking.

test_risk_engine.py (Unit Tests): This file focuses purely on your math. It will pass dummy numbers (temperature, rainfall, active cases) into your RiskCalculationEngine and check if the math outputs the correct Risk Score (0-100) and Risk Level.

test_integration.py (Integration Tests): This tests how different parts of your system work together. For example, it will test if saving a new HospitalAdmissions record correctly triggers a database update.

test_views_api.py (Endpoint Tests): This file simulates a user or external system trying to load your dashboard or hit your Django REST Framework API endpoints. It checks if the server returns a 200 OK status or a 404 Not Found.


test_edge_cases.py (Invalid/Failure Cases): This is specifically required by the brief. It tests what happens when things go wrong. What if someone enters "-5" for active cases? What if the Weather API is down? Your tests should prove the system handles these errors gracefully instead of crashing.

2. The Folder Structure
Inside your repository, your tests/ folder should look something like this:

Plaintext
ecohealth-dengue-predictor/
│
├── tests/
│   ├── __init__.py                # Tells Python this is a module
│   ├── test_risk_engine.py        # Tests the core math logic
│   ├── test_integration.py        # Tests database interactions
│   ├── test_views_api.py          # Tests web pages and API URLs
│   └── test_edge_cases.py         # Tests bad data and errors
3. A Crucial Grading Reminder: "Test Evidence"
The grading rubric explicitly states that you get 10 marks for your "Test Log and Evidence". This means writing the code isn't enough; you must prove you ran it.

When your QA person runs these tests in the terminal (using python manage.py test or pytest), they need to take screenshots of the terminal showing all the tests passing (or showing how the system handled an error). These screenshots and text logs should be saved in your docs/ folder as part of your final Technical Report.