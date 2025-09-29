# Smart India Hackathon Workshop
# Date: 29.09.2025
## Register Number:25013553
## Name:SUJAL DAS
## Problem Title
SIH 25010: Smart Crop Advisory System for Small and Marginal Farmers
## Problem Description
A majority of small and marginal farmers in India rely on traditional knowledge, local shopkeepers, or guesswork for crop selection, pest control, and fertilizer use. They lack access to personalized, real-time advisory services that account for soil type, weather conditions, and crop history. This often leads to poor yield, excessive input costs, and environmental degradation due to overuse of chemicals. Language barriers, low digital literacy, and absence of localized tools further limit their access to modern agri-tech resources.

Impact / Why this problem needs to be solved

Helping small farmers make informed decisions can significantly increase productivity, reduce costs, and improve livelihoods. It also contributes to sustainable farming practices, food security, and environmental conservation. A smart advisory solution can empower farmers with scientific insights in their native language and reduce dependency on unreliable third-party advice.

Expected Outcomes

• A multilingual, AI-based mobile app or chatbot that provides real-time, location-specific crop advisory.
• Soil health recommendations and fertilizer guidance.
• Weather-based alerts and predictive insights.
• Pest/disease detection via image uploads.
• Market price tracking.
• Voice support for low-literate users.
• Feedback and usage data collection for continuous improvement.

Relevant Stakeholders / Beneficiaries

• Small and marginal farmers
• Agricultural extension officers
• Government agriculture departments
• NGOs and cooperatives
• Agri-tech startups

Supporting Data

• 86% of Indian farmers are small or marginal (NABARD Report, 2022).
• Studies show ICT-based advisories can increase crop yield by 20–30%.

## Problem Creater's Organization
Government of Punjab

## Theme
Agriculture, FoodTech & Rural Development

## Proposed Solution
1.SOIL & FERTILIZER

AI-powered nutrient gap analysis (rule + ML hybrid).
Crop rotation & intercropping suggestions to restore soil health.
Fertilizer bundles tailored to soil reports (NPK balance with micronutrients).


2.WEATHER & CLIMATE ALERTS

Hyperlocal weather via satellite + IoT sensor integration.
“When NOT to spray/pesticide” → avoid rain wash-off & wasted cost.
Seasonal disease outbreak prediction (e.g., rice blast, cotton bollworm).


3.PEST & DISEASE MANAGEMENT

On-device pest detection (MobileNetV3 in TFLite → works offline).
AI suggests eco-friendly control first (biopesticides, natural methods).
Low-confidence images → automatically sent to extension officer queue.


4.MARKET & FINANCIAL EMPOWERMENT

Real-time mandi price dashboard + nearby buyers.
Marketplace integration for crop selling.
Micro-credit advisory: suggest when to buy inputs / sell produce for max profit.


5.VOICE-FIRST MULTILINGUAL ACCESS

Full IVR + voice bot → works for non-smartphone farmers.
Conversational chatbot in 10+ Indian languages (Hindi, Tamil, Odia, Punjabi…).


6.COMMMUNITY & LEARNING

Short 30-second micro-learning audios (how to spray, how to save water).
Peer farmer leaderboard (“Top Farmer of the Month”).
Farmer storytelling: Success stories shared in audio & text.


7.FEEDBACK & ACTIVE LEARNING

Farmers rate advisories → ML models continuously retrain.
Feedback loop ensures personalization improves season after season.


## Technical Approach

FRONTEND

Flutter mobile app + PWA (Progressive Web App for browsers).
Voice-first UI + offline caching with SQLite.

BACKEND

FastAPI / Node.js for scalable REST/GraphQL APIs.
PostgreSQL + PostGIS → store farm boundaries, soil data, NDVI indices.

AI/ML

1. Pest Detection → MobileNetV3 (quantized for on-device).
2. Soil/Fertilizer Recs → Hybrid Decision Tree + Gradient Boosted Models.
3. Yield Forecasting → Time-series regression (weather + soil + crop stage).
4. Market Forecasting → ARIMA/LSTM for price trends.

INTEGRATION

Weather APIs (IMD/OpenWeather).
Market APIs (Agmarknet).
Satellite NDVI from Sentinel-2 via Google Earth Engine.
Optional IoT: soil moisture & pH sensors.

INNOVATION LAYER

Blockchain log of every advisory → tamper-proof trust with govt seal.
AI confidence scores visible → farmer sees “High/Medium/Low confidence”.

📊 Architecture (Improved Flow)

[Farmer Inputs]

   ├── Soil Data / IoT Sensor
   
   ├── Crop Image (Camera)
   
   ├── GPS Location & Weather
   
   └── Voice/Text Query
   
        
[Data Integration Layer]

   ├── Soil API | Market API | Weather API
   
   └── Farmer DB (PostgreSQL/PostGIS)
   
        
[AI & Hybrid Processing]

   ├── CNN (Pest Detection, Edge + Cloud)
   
   ├── Decision Trees (Soil/Fertilizer)
   
   ├── LSTM (Yield & Price Prediction)
   
   └── Human-in-Loop (Agronomist review)
   
        
[Advisory Generation]

   ├── Pest/Disease Treatment
   
   ├── Fertilizer Dosage
   
   ├── Crop Selection
   
   ├── Market Alert
   
   └── Voice/TTS Guidance
   
        
[Delivery Layer]

   ├── Mobile App (Flutter + Offline Cache)
   
   ├── IVR/Chatbot (Voice-first)
   
   ├── SMS Alerts
   
   └── Extension Officer Dashboard
   
        
[Impact Tracking]

   ├── Yield Improvement (per farmer)
   
   ├── Input Cost Reduction
   
   ├── Soil Health Index
   
   └── Govt Dashboard (Sustainability KPIs)


   📅 PILOT & ROADMAP:

PHASE 1 (3 MONTHS) → MVP

Soil + Fertilizer advisory
Pest detection (5 major crops)
Weather alerts (rain, heat, pest risk)
Voice chatbot (2 languages)


PHASE 2 (6 MONTHS) → PILOT 500–1000 FARMERS

Market price + sales platform
Satellite NDVI monitoring
Human-in-loop agronomist support
Gamification (farmer points)


PHASE 3 (12 MONTHS) → SCALE

Multilingual expansion (10+ languages)
AI price forecasting + credit linkage
Govt integration (blockchain-backed advisory logs)


## Feasibility and Viability
FEASIBILITY

Technical:

Open-source ML frameworks (TensorFlow, PyTorch) make disease detection viable.
Weather & mandi data APIs are publicly available (IMD, Agmarknet, eNAM).
IoT sensors for soil are now low-cost (₹2000–3000/unit) and scalable.

Operational:

Smartphone penetration in rural India is above 65% (TRAI 2024 report).
Can be deployed via Android app + IVR/SMS for non-smartphone users.


Partnerships:

Collaboration with KVKs, ICAR, IMD, NABARD ensures data reliability.
NGOs/FPOs can assist in farmer onboarding.



VIABILITY

Economic:

Farmers save 20–30% input costs (fertilizer/pesticide optimization).
Yield improvement of 15–25% (as per FAO ICT studies).
Blockchain traceability enables premium pricing for organic/safe produce.


Scalability:

Can start with pilot districts → scale nationwide with multilingual support.
Modular design allows integration with government schemes (PM-Kisan, eNAM).


Sustainability:

Encourages eco-friendly practices (reduced chemical usage).
Strengthens food security and rural income.


Revenue Model (for long-term sustainability):

Freemium app for farmers.
Premium analytics for FPOs, agri-input companies, govt bodies.
Commission from marketplace linkages.


## Impact and Benefits
🎯 IMPACT:

🌱 Farmers: Higher yield, lower input costs, better incomes.

🌍 Environment: Reduced overuse of chemicals, sustainable farming.

🏛 Government: Supports “Digital India” & “Doubling Farmers’ Income” mission.

📊 Economy: Stronger rural supply chain, better market price realization.

BENEFITS:

1. Adds IoT + Blockchain integration (future-ready).
2. Provides clear feasibility & viability analysis (technical + economic).
3. Includes offline access (SMS/IVR) for farmers without internet.
4. Introduces community + expert integration for trust-building.


## Research and Reference

1. http://agriwelfare.gov.in
2. http://enam.gov.in
3. https://www.rishabhsoft.com/blog/iot-in-agriculture-industry
4. https://www.cropin.com/blogs/iot-in-agriculture/



