SPY Data Visualizer

Overview

SPY Data Visualizer is a single-page web application that displays intraday 30-second interval SPY data using Lightweight Charts. The data is stored in .xlsx files, with each file containing data for a single trading day. The goal is to provide a sleek, minimal, and mobile-friendly visualization of historical SPY price movements.

Features

Displays SPY intraday data using Lightweight Charts

Minimal and responsive UI optimized for desktop and mobile

Read-only historical data (no real-time updates for now)

Uses Python backend (FastAPI or Flask) to serve .xlsx data as JSON

Version control with GitHub

Data Structure

Each .xlsx file contains the following columns:

open

high

low

close

18-EMA

34-EMA

VWAP

400-EMA

200-EMA

Volume

open_price

high_price_body

low_price_body

Project Structure

spy-data-visualizer/
├── backend/  (Handles reading .xlsx files)
│   ├── app.py  (Python API for serving data)
│   ├── data/   (Folder where .xlsx files are stored)
├── frontend/  (The website UI)
│   ├── index.html
│   ├── styles.css
│   ├── script.js  (Handles chart logic)
├── README.md
├── .gitignore

Setup Instructions

1. Clone the Repository

git clone https://github.com/YOUR_USERNAME/spy-data-visualizer.git
cd spy-data-visualizer

2. Backend Setup

Install Python dependencies:

pip install fastapi uvicorn pandas openpyxl

Run the backend:

cd backend
uvicorn app:app --reload

This will start the API at http://127.0.0.1:8000

3. Frontend Setup

Simply open frontend/index.html in a web browser to view the charts.

Next Steps

Build the backend to parse .xlsx files and return JSON data

Develop the frontend to fetch and display this data using Lightweight Charts

Improve UI design and mobile responsiveness

Contributing

If you’re new to GitHub, here are the basic steps to contribute:

Pull the latest changes

git pull origin main

Create a new branch for changes

git checkout -b feature-branch-name

Make changes and commit

git add .
git commit -m "Added feature XYZ"

Push changes to GitHub

git push origin feature-branch-name

Open a pull request (PR) on GitHub



