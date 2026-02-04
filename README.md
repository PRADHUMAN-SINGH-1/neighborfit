# 🏙️ NeighborhoodFit

🔴 **Important Note**  
This website uses **free backend hosting on Render**, so the first API request may take **up to 1 minute** when the server wakes up.

🔗 **Live Demo:** https://neighborhoodfit.netlify.app  
🌐 **Backend API:** https://neighborfit-y283.onrender.com/api/neighborhoods  

**NeighborhoodFit** is a full-stack web application that helps users explore suitable neighborhoods in **Bengaluru, India** based on 🛡️ safety, 💰 rent level, 🚇 metro access, and 🌱 lifestyle indicators.

---

## 📡 What does it do?

Whether you're moving to Bengaluru or exploring better places to live, **NeighborhoodFit** lets you:

- 📍 View **relative safety scores** of neighborhoods  
- 💰 Compare **average rent levels**  
- 🚇 Filter areas by **metro station proximity**  
- 🌱 Explore nearby **parks, schools, and lifestyle factors**  
- 🔍 Search and filter neighborhoods easily  
- 🏷️ Understand tags like **Family-Friendly** or **Walkable** using colorful badges  

---

## 📊 Where did the data come from?

The data used in this app was **carefully created**, not randomly downloaded.

### 📥 Base Geo & Place Data
- 🛠️ Tool Used: **Overpass Turbo**
- 🗺️ Map Source: **OpenStreetMap**

Using Overpass queries, the following data was extracted:
- Neighborhood names
- Geographic coordinates
- Nearby metro stations
- Parks and schools
- Roads and points of interest

### 🧾 Dataset Enrichment
The raw data was then **manually processed and enriched** with:
- 🛡️ Relative safety scores  
- 💰 Rent level categories (based on market trends)  
- 🚇 Metro proximity labels  
- 🏷️ Lifestyle tags (walkability, family-friendliness, quiet areas)

📁 **Final Dataset:** `bengaluru_neighborhoods.csv`  
Stored on the backend server and served through an API.

---

## 🔐 How the Safety (Crime) Score was calculated

- Official ward-wise crime data is not fully public.
- A **proxy-based safety score** was created for **relative comparison only**.

### 🧩 Indicators Used
- 🏫 **Amenity Density:** Schools, parks, hospitals, shops  
- 🛣️ **Road Connectivity:** Road network density  
- 🏙️ **Public Activity:** Commercial places and transport stops  

### 🧮 Formula Used
Safety Score =  
(Amenity Density + Road Connectivity + Public Activity) / 3  

- All values were **min–max normalized (0–1)**
- Equal weights were used to avoid bias

### 📈 Interpretation
- Higher score → relatively safer neighborhood  
- Lower score → relatively less safe neighborhood  
- ⚠️ This is **not official crime data**

---

## 🎨 How Lifestyle Badges were calculated

Each neighborhood includes lifestyle tags such as:

- 🧑‍👩‍👧 **Family-Friendly**  
- 💼 **Working Professionals**  
- 🤫 **Quiet Neighborhoods**  
- 🚶 **Walkable & Connected**  

### 🏷️ Tag Logic
- **Family-Friendly:** High number of schools and parks  
- **Working Professionals:** Office and co-working density  
- **Quiet Neighborhoods:** Lower traffic and commercial activity  
- **Walkable & Connected:** Metro proximity, parks, road connectivity  

---

## 🖥️ Project Structure

NeighborFit/
- client/
  - src/
    - App.js
    - App.css
    - NeighborhoodList.js
    - NeighborhoodList.css
- server/
  - data/
    - bengaluru_neighborhoods.csv
  - index.js
- README.md

---

## 🧰 Tech Stack

- 🎨 **Frontend:** React.js, Tailwind CSS  
- ⚙️ **Backend:** Node.js, Express  
- 📊 **Data:** OpenStreetMap (via Overpass Turbo)  
- ☁️ **Hosting:** Netlify (Frontend), Render (Backend)  

---

## 🚀 Key Features

- ✅ Dynamic filtering by safety, rent, and metro access  
- 🏷️ Smart lifestyle badges with animations  
- 📱 Fully responsive UI  
- 🗺️ Google Maps links for neighborhoods  
- 🔄 API-based data fetching  

---

## ⚙️ Backend Overview

- Built using **Node.js + Express**
- CSV parsed using `csv-parser`
- Public API endpoint:
  /api/neighborhoods
- Deployed on **Render** with GitHub auto-deploy

---

## 🌐 Frontend Integration

- React fetches data using `useEffect`
- API base URL stored in environment variables
- Frontend hosted on **Netlify**

---

## 👤 Author

Made by **Pradhuman Singh**  
GitHub: https://github.com/PRADHUMAN-SINGH-1  

Built with 💙 to demonstrate:
- Real-world data handling
- Explainable scoring logic
- Full-stack deployment
- Zero-budget hosting

---

## 📌 Notes for Reviewers / HR

This project highlights my ability to:
- Work with **real geospatial data**
- Design **dataset-driven UI badges**
- Build and deploy **full-stack applications**
- Solve data limitations using practical approaches
