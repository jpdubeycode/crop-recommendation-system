# 🌾 Crop Recommendation System

A Machine Learning web application that recommends the most suitable crop to grow based on soil nutrients and weather conditions.

🔴 **Live Demo:** [https://crop-recommendation-system-7zfu.onrender.com](https://crop-recommendation-system-7zfu.onrender.com)

---

## 📌 Table of Contents
- [About the Project](#about-the-project)
- [Demo](#demo)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Dataset](#dataset)
- [How It Works](#how-it-works)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Deployment](#deployment)
- [Results](#results)
- [Author](#author)

---

## 📖 About the Project

Farmers often struggle to decide which crop to grow based on their soil and local weather conditions. This project solves that problem using **Machine Learning**.

By entering 7 simple parameters — Nitrogen, Phosphorus, Potassium, Temperature, Humidity, pH, and Rainfall — the system predicts the best crop out of **22 possible crops** with **99%+ accuracy**.

---

## 🎥 Demo

| Input Form | Recommendation Result |
|---|---|
| Enter soil & weather values | Get crop recommendation instantly |

👉 Try it live: [https://crop-recommendation-system-7zfu.onrender.com](https://crop-recommendation-system-7zfu.onrender.com)

> ⚠️ The app is hosted on Render's free tier. It may take **30–50 seconds** to load on first visit (server wakes up from sleep).

---

## ✨ Features

- 🌱 Recommends the best crop from 22 crop types
- 📊 Trained on real agricultural dataset (2,200 records)
- 🔢 Takes 7 input parameters: N, P, K, Temperature, Humidity, pH, Rainfall
- 🌐 Responsive web interface built with Bootstrap
- ☁️ Deployed live on Render cloud platform
- 🔄 Auto-redeployment via GitHub CI/CD

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| **Language** | Python 3.14 |
| **ML Framework** | Scikit-learn |
| **Web Framework** | Flask |
| **Frontend** | HTML5, Bootstrap 5 |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Model Saving** | Joblib |
| **Deployment** | Render + Gunicorn |
| **Version Control** | Git, GitHub |

---

## 📊 Dataset

- **Source:** [Kaggle — Crop Recommendation Dataset](https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset)
- **Size:** 2,200 rows × 8 columns
- **Target Classes:** 22 crops

| Feature | Description | Unit |
|---|---|---|
| N | Nitrogen content in soil | mg/kg |
| P | Phosphorus content in soil | mg/kg |
| K | Potassium content in soil | mg/kg |
| temperature | Temperature | °C |
| humidity | Relative humidity | % |
| ph | pH value of soil | — |
| rainfall | Rainfall | mm |
| **label** | **Crop name (target)** | — |

**22 Crop Classes:**
Rice, Maize, Jute, Cotton, Coconut, Papaya, Orange, Apple, Muskmelon, Watermelon, Grapes, Mango, Banana, Pomegranate, Lentil, Blackgram, Mungbean, Mothbeans, Pigeonpeas, Kidneybeans, Chickpea, Coffee

---

## ⚙️ How It Works

```
User Input (7 values)
       ↓
MinMaxScaler  →  scales values to range [0, 1]
       ↓
StandardScaler  →  scales to mean=0, std=1
       ↓
Random Forest Classifier  →  predicts crop number
       ↓
crop_dict  →  converts number to crop name
       ↓
Result displayed on screen 🌱
```

---

## 📁 Project Structure

```
crop-recommendation-system/
│
├── app.py                        ← Flask web application
├── model.pkl                     ← Trained Random Forest model
├── minmaxscaler.pkl              ← Saved MinMaxScaler
├── standscaler.pkl               ← Saved StandardScaler
├── Crop_recommendation.csv       ← Dataset
├── requirements.txt              ← Python dependencies
├── Procfile                      ← Render deployment config
├── Crop_Recommendation_System.ipynb  ← Jupyter notebook (training)
└── templates/
    └── index.html                ← Frontend UI
```

---

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8+
- pip

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/jpdubeycode/crop-recommendation-system.git
cd crop-recommendation-system

# 2. Create virtual environment
python -m venv crop_env
crop_env\Scripts\activate        # Windows
# source crop_env/bin/activate   # Mac/Linux

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
python app.py
```

5. Open your browser and go to: **http://127.0.0.1:5000**

---

## ☁️ Deployment

This app is deployed on **Render** (free tier).

| Field | Value |
|---|---|
| Platform | Render |
| Runtime | Python 3 |
| Build Command | `pip install -r requirements.txt` |
| Start Command | `gunicorn app:app` |

Any push to the `main` branch triggers **automatic redeployment**.

---

## 📈 Results

| Metric | Value |
|---|---|
| **Model** | Random Forest Classifier |
| **Accuracy** | 99%+ |
| **Train/Test Split** | 80% / 20% |
| **Total Records** | 2,200 |
| **Number of Classes** | 22 crops |

---

## 👤 Author

**Jai Prakash Dubey**

- 📧 Email: [jaidubeyiitm@gmail.com](mailto:jaidubeyiitm@gmail.com)
- 🐙 GitHub: [@jpdubeycode](https://github.com/jpdubeycode)
- 💼 LinkedIn: [Jai Prakash Dubey](https://www.linkedin.com/in/jai-prakash-dubey-72b93032a/)

---

## ⭐ Show Your Support

If you found this project helpful, please give it a **⭐ star** on GitHub!

---

*Built with ❤️ by Jai Prakash Dubey*