# This is django project where we buit full-stack application, which will classify radation with svm

# This is django project where we built full-stack application which will classify radiation with svm model and we can download the csv file (Data used for prediction)

# 🌌 Gamma-Hadron Particle Classifier

A Machine Learning web application built with **Django** to classify high-energy particles (Gamma vs. Hadron) using data from the MAGIC Gamma Telescope.

## 🚀 Key Features

* **Real-time Classification:** Integrated ML model for instant prediction.
* **Django Integration:** Logic handled within `views.py` for seamless request processing.
* **Data Persistence:** Automatic logging of inputs and results to the database.

## 🛠️ Tech Stack

* **Backend:** Django (Python)
* **Machine Learning:** Scikit-Learn (SVM)
* **Database:** SQLite
* **Data Source:** MAGIC Gamma Telescope Dataset 

## 🏗️ Implementation Details

### Model Integration (`views.py`)

The application loads a serialized model (`.pkl` or `.joblib`) and processes form data:

```python
def predict_view(request):
    # 1. Capture telescope parameters from form
    # 2. model.predict() determines if it is 'Gamma' or 'Hadron'
    # 3. Results are saved to the database via Django Models
    # 4. Result is rendered to the UI

```

### Database Connection

All prediction history is stored in the database, tracking:

* **Input Features:** fLength, fWidth, fSize, etc.
* **Classification:** Gamma (Signal) or Hadron (Background).
* **Timestamp:** For historical data tracking.

## 📋 Quick Setup

1. **Install:** `pip install -r requirements.txt`
2. **Migrate DB:** `python manage.py migrate`
3. **Run:** `python manage.py runserver`
---

*Developed for high-energy physics data analysis.*
## 📂Project Structure
<img width="464" height="871" alt="Screenshot 2026-02-05 153404" src="https://github.com/user-attachments/assets/e04e0395-8259-49a5-be65-c3e9cb2fa509" />
