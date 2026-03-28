# Reloop — User Engagement & Retention Analysis

## Overview
SQL-based analysis of user behavior on Reloop, a fictional recommerce app 
selling refurbished electronics. The goal: identify activation gaps, 
retention patterns, and revenue drivers to inform growth decisions.

This project simulates the kind of analysis a Business Operations or 
Growth Operations team would run to understand where users drop off 
and where to focus to drive meaningful impact.

---

## Business Context
Reloop operates in the recommerce space (think Back Market). 
Users sign up, browse, and ideally purchase refurbished electronics. 
The core challenge: converting sign-ups into active buyers — 
and keeping them coming back.

This analysis answers 4 key business questions:
- What % of users actually make a purchase? (Activation)
- Which acquisition channel drives the most valuable users? (Channel quality)
- Do users come back after their first purchase? (Retention)
- Who is churning — and when? (Churn)

---

## Dataset
Fictional dataset generated with Python (pandas, numpy):

| Table | Rows | Description |
|-------|------|-------------|
| users | 800 | Signed-up users with acquisition channel and country |
| orders | 482 | Purchase history with order value and product category |
| sessions | 2324 | App sessions to track engagement behavior |

**Period:** January – March 2026  
**Acquisition channels:** Organic, Paid Social, Referral, Influencer  
**Product categories:** Smartphones, Laptops, Tablets, Audio, Gaming  
**Countries:** France, Germany, Spain, Italy, Belgium

---

## Key Findings

### 1. Activation Rate — 34.3%
Only 1 in 3 users makes a purchase after signing up. 
65.7% of the user base never converts.

→ **Recommendation:** Implement a targeted onboarding sequence 
(push notifications, personalized email) within 48h of sign-up 
to reduce time-to-first-purchase.

### 2. Referral is the highest-quality channel
| Channel | Activation Rate | ARPU |
|---------|----------------|------|
| Referral | 39.2% | €387 |
| Influencer | 41.7% | €221 |
| Paid Social | 36.6% | €227 |
| Organic | 27.5% | €230 |

Referral drives the best users: highest ARPU (€387) 
and strong activation rate (39.2%).

→ **Recommendation:** Invest in a structured referral program 
with incentives — it's the most cost-efficient growth lever.

### 3. Retention D7/D30
- D7 retention: 15% — low but expected for high-consideration purchases
- D30 retention: 39.8% — strong signal of product satisfaction

→ **Recommendation:** Focus retention efforts between D7 and D30 
with targeted campaigns (cross-sell, complementary accessories) 
to accelerate the second purchase cycle.

### 4. Churn Rate — 11.6%
11.6% of users have been inactive for 30+ days. 
206 users (25% of the base) never opened the app after signing up.

→ **Recommendation:** The 206 never-active users represent 
a quick win — a simple re-engagement email sequence 
could recover a meaningful portion of this segment.

---

## Tech Stack
- **Python** — dataset generation (pandas, numpy)
- **SQLite** — database creation and SQL queries
- **Google Colab** — development environment (no installation needed)

---

## How to Run
1. Open the notebook in Google Colab
2. Run all cells in order (Runtime → Run All)
3. CSV outputs will be generated automatically

---

## About
Built as part of a self-directed learning portfolio focused on 
Business Operations and Growth Analytics.

Part of a broader GitHub portfolio:
- Lead Enrichment Pipeline — Python + Clearbit API
- Reloop Retention Analysis — SQL + SQLite (this project)
