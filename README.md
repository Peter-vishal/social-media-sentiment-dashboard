# Social Media Sentiment Dashboard

## Overview
The **Social Media Sentiment Dashboard** is a web application designed to analyze and visualize sentiment trends from social media posts. It leverages **machine learning models** and **natural language processing (NLP)** techniques to classify sentiments and present insights in an interactive dashboard using **Streamlit**.

## Features
- **Real-time Sentiment Analysis**: Classifies tweets or posts as positive, negative, or neutral.
- **Interactive Dashboard**: Displays sentiment trends using **Streamlit**.
- **Data Visualization**: Graphs and charts for sentiment distribution.
- **Flask API**: Backend for managing sentiment analysis and database interactions.
- **Database Integration**: Uses **SQLAlchemy** for data persistence.
- **Docker Support**: Easily deployable with Docker.


---

## Folder Structure
```
📂 social-media-sentiment-dashboard
│── 📂 sentiment-jupyter notebook  # Contains Jupyter notebooks for model training
│── 📂 TW_Sentiment                # Backend (Flask API, database models, routes)
│   │── 📂 application
│   │   │── 📂 Models              # Database models
│   │   │── 📂 Routes              # API endpoints
│   │   │── __init__.py            # App initialization
│   │── config.py                  # Configuration settings
│   │── start.sh                    # Shell script to start the app
│── 📂 tw_sentiment_js              # Frontend (React.js/Streamlit UI)
│   │── public                      # Static files
│   │── src                         # React source code
│── requirements.txt                # Python dependencies
│── wsgi.py                         # WSGI entry point for Flask app
│── NLP report.docx                 # Research paper
```

---

## Installation & Setup

### 1️⃣ Prerequisites
Ensure you have the following installed:
- **Python 3.8+**
- **Node.js & npm** (For frontend development)
- **PostgreSQL** or SQLite (For database storage)
- **Docker** (For containerized deployment)

### 2️⃣ Backend Setup (Flask API)
```sh
cd TW_Sentiment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
flask run  # Runs the Flask API
```

### 3️⃣ Frontend Setup (Streamlit Dashboard)
```sh
cd tw_sentiment_js
npm install
npm start  # Runs the React frontend
```
OR (If using Streamlit)
```sh
streamlit run dashboard.py
```


## Usage
1. Enter a hashtag or keyword to analyze social media sentiment.
2. View the analysis results on the interactive dashboard.
3. Monitor sentiment trends over time.

---

## API Endpoints (Flask Backend)
| Method | Endpoint            | Description                  |
|--------|---------------------|------------------------------|
| `POST` | `/api/analyze`      | Analyze sentiment of tweets  |
| `GET`  | `/api/results`      | Get stored analysis results  |
| `GET`  | `/api/health`       | Check server health status   |

---

## Deployment
- Deploy on **Streamlit Cloud** (Frontend)
- Use **Heroku/Vercel** for backend API
- Deploy using **Docker + AWS/GCP**


