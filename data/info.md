According to your module brief, the data/ folder is specifically designated "for datasets or sample inputs".

For your EcoHealth Dengue Outbreak Predictor project, this folder will hold the static files your application needs to process, test, and function before it is connected to a live database or API.

Here is exactly what you should place inside it:

Sample Clinical Data: CSV files containing mock or historical hospital admission records (e.g., hospital_admissions_sample.csv with columns for district, date, active cases, and available beds).

Sample Environmental Data: CSV or JSON files containing historical weather logs (e.g., weather_data_sample.csv detailing temperature, rainfall, and humidity for different Sri Lankan districts over a 28-day period).

Seed Data: Any foundational files used to pre-populate your database when you first initialize it, such as a static list of all the health districts in Sri Lanka.

Keeping these files isolated in the data/ folder ensures your core application logic in the src/ folder remains clean and separated from the raw information it processes.