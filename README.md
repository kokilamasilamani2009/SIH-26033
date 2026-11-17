# Smart India Hackathon Workshop
# Date:17-11-2026
## Reference Number:26018359
## Name:M.Kokila

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution
. Detailed Explanation of the Proposed Solution
We propose KrishiSetu, an AI-driven, hyper-local B2B and B2C agricultural marketplace that directly connects Farmer Producer Organizations (FPOs) and individual farmers with bulk buyers (retailers, HoReCa, housing societies) and end consumers. Unlike passive listing portals, KrishiSetu acts as an end-to-end execution engine featuring:
• Direct Farm-to-Fork Listing: Vernacular, voice-assisted onboarding allowing farmers/FPOs to list harvest grades, quantities, and farm-gate prices.
• Dynamic Demand Aggregation: Pools small retail consumer orders within a geographic cluster into bulk orders, making direct farm-to-city transport economically viable.
• Integrated Milk-Run Logistics: Connects local mini-truck/tempo owners (via a partner app) to execute multi-pickup, multi-drop routes with real-time GPS tracking.
2. How It Addresses the Problem
• Eliminates Middlemen Markups: Removes 4–6 layers of commission agents (arhatiyas, local aggregators, and wholesale traders), allowing farmers to retain up to 80–85% of the final retail price while reducing consumer costs by 15–20%.
• Solves Fragmented Supply: Individual smallholders lack the volume to fulfill bulk orders. By routing listings through FPO collection centers and aggregating nearby consumer demand, small harvests are combined into viable truckloads
• Prevents Post-Harvest Spoilage: AI demand forecasting aligns harvest schedules with upcoming regional demand, minimizing distress sales and perishable waste.
3. Innovation and Uniqueness of the Solution
• ONDC-Ready & Vernacular-First Architecture: Designed to interoperate with the Open Network for Digital Commerce (ONDC) while offering an IVR/WhatsApp bot interface for farmers with low digital literacy or 2G/3G connectivity.
• Cold-Start AI Forecasting: Overcomes the lack of initial platform transaction history by training forecasting models on historical Agmarknet mandi arrivals, seasonal weather patterns, and regional festival calendars.
• Perishability-Weighted Vehicle Routing (VRP): Unlike standard delivery algorithms, our route optimizer factors in crop shelf-life and ambient temperature alongside distance and vehicle capacity.
• Prevents Post-Harvest Spoilage: AI demand forecasting aligns harvest schedules with upcoming regional demand, minimizing distress sales and perishable waste.


## Technical Approach
1. Technologies to Be Used
• Frontend (Farmer, Buyer & Driver Apps): React Native / Flutter (cross-platform mobile apps with offline-first SQLite caching) + Next.js (web dashboard for FPOs and bulk buyers).
• Accessibility Layer: Twilio / Gupshup WhatsApp Business API & Bhashini API (for real-time Indian regional language voice-to-text).
• Backend & Database: Node.js (Express/NestJS) or Python (FastAPI) microservices; PostgreSQL with PostGIS (for geospatial clustering and radius queries); Redis (for real-time inventory locking).
• AI/ML & Optimization Engine:
	• Demand Forecasting: Python, Scikit-learn, Prophet / XGBoost (trained on Agmarknet & IMD weather datasets).
	• Route Optimization: Google OR-Tools (Capacitated Vehicle Routing Problem with Time Windows - CVRPTW) integrated with OpenStreetMap / Mappls APIs.
• Payments & Trust: Razorpay Route / UPI Split Payments (automated escrow release upon digital proof-of-delivery).
2. Methodology and Process for Implementation
• Step 1 — Onboarding & Quality Grading: FPOs verify farmer KYC and perform standardized digital quality grading (Grade A/B/C) with geo-tagged photos at the collection center.
• Step 2 — AI Demand & Price Advisory: The ML engine predicts 7-day regional demand and suggests a fair price band based on live mandi rates and transport costs.
• Step 3 — Order Aggregation Window: Consumers and bulk buyers place orders within a daily cut-off window (e.g., before 8:00 PM for next-day morning delivery).
• Step 4 — Route Generation: At cut-off, OR-Tools clusters orders by pin code, assigns available local logistics vehicles, and generates optimized pickup-and-drop sequences.
• Step 5 — Fulfillment & Instant Settlement: QR-code scanning at pickup and delivery triggers automated UPI split settlements directly to the farmer/FPO and driver.
## Feasibility and Viability
1. Analysis of Feasibility
• Technical Feasibility: Built on mature, open-source geospatial and optimization libraries (PostGIS, OR-Tools) and existing Indian Digital Public Infrastructure (UPI, Bhashini, Agmarknet APIs).
• Economic Viability: Asset-light model—no warehouses or trucks are owned. Revenue is generated via a transparent 3–5% platform/logistics facilitation fee paid by bulk buyers and retail consumers, keeping farmer onboarding completely free.
2. Potential Challenges and Risks
• Trust Deficit & Quality Disputes: Buyers fear receiving substandard produce, while farmers fear payment delays.
• Low Digital Literacy & Rural Connectivity: Small farmers may struggle with complex app interfaces or intermittent internet.
• Cold-Start Liquidity: Balancing supply and demand in a new district during initial rollout.
3. Strategies for Overcoming These Challenges
• Escrow + FPO Quality Gatekeeping: Payments are held in UPI escrow until delivery verification; FPOs act as local trust anchors for standardized sorting and grading.
• Offline-First & Assisted Onboarding: Local FPO coordinators ("Krishi Mitras") manage listings on behalf of non-smartphone farmers, backed by WhatsApp/voice prompts.
• Anchor-Buyer Strategy: Onboard bulk institutional buyers (hostels, restaurants, apartment associations) first to guarantee baseline volume before opening retail consumer slots.
## Impact and Benefits
1. Potential Impact on Target Audience
• Farmers & FPOs: Direct market visibility, predictable demand signals before harvest, and faster cash cycles (T+0 / T+1 settlement).
• Consumers & Bulk Buyers: Access to fresher, traceable produce at prices lower than traditional retail markets.
• Rural Transporters: Consistent daily utilization of local mini-trucks and tempos.
2. Multidimensional Benefits
• Economic: Increases net farmer income by 15–30% by eliminating multi-tier commissions while reducing consumer food inflation.
• Social: Empowers FPOs as self-sustaining rural enterprises and creates local gig opportunities in sorting, grading, and last-mile transport.
• Environmental: Reduces food miles and fuel consumption by 12–18% through AI route optimization, while cutting post-harvest perishable waste and landfill methane emissions.

## Research and References
• Government Open Data & Market Portals:
	• Agmarknet (Directorate of Marketing & Inspection, Govt. of India) – Source for historical commodity arrival and modal price datasets used in AI demand forecasting.
	• e-NAM (National Agriculture Market) – Reference model for electronic mandi trade workflows and quality assaying parameters.
	• Open Network for Digital Commerce (ONDC) – Protocol standards for unbundled, interoperable agricultural commerce and logistics.
• Technical Frameworks & Algorithms:
	• Google OR-Tools: Vehicle Routing Problem (VRP) – Open-source optimization suite for multi-stop pickup and delivery routing.
	• Bhashini (National Language Translation Mission) – Speech-to-text and translation APIs for vernacular farmer interfaces.

