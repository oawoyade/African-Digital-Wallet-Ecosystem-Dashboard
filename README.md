
# 🌍 DataDNA Challenge — African Digital Wallet Ecosystem

## 📌 Project Overview

The **African Digital Wallet Ecosystem Dashboard** was developed as a comprehensive Power BI solution to analyse transaction performance, fraud exposure, gig-worker behaviour, customer risk and operational efficiency across **Nigeria, Kenya, Ghana and South Africa**.

The project transforms **50,000 wallet transactions** into a structured four-page analytical dashboard covering:

- Transaction activity
- Fraud and financial exposure
- Gig-worker and customer risk
- Operational performance
- Payment-channel behaviour
- KYC verification
- Transaction outcomes
- Emerging risk patterns

The dashboard was designed to move beyond basic reporting and provide a clearer understanding of how transaction behaviour, customer characteristics, geography and operational performance interact across the digital-wallet ecosystem.

---

## 🎯 Project Objectives

The dashboard was built to answer key analytical questions such as:

- How much transaction activity and value moves through the ecosystem?
- Which payment channels have the highest fraud exposure?
- How does fraud vary across countries and gig-worker segments?
- Which customer characteristics are associated with higher risk?
- How do KYC tiers compare in terms of fraud exposure?
- Which transaction types experience elevated decline, timeout or pending rates?
- How efficiently are wallet transactions processed?
- Where do operational and emerging risks appear?

---

## 🧱 Data Model

The solution was built using a **star-schema-style data model**.

### Fact Table

`fact_transactions`

Contains the main transaction-level data, including:

- Transaction amount
- Transaction value in USD
- Channel ID
- Market ID
- Date ID
- Fraud loss
- Fraud flag
- Dispute flag
- Reversal flag

### Dimension Tables

`dim_channel`

Contains:

- Channel ID
- Channel type
- Channel subtype
- Digital-channel indicator
- Internet requirement

`dim_market`

Contains:

- Country
- Market ID
- ISO code
- Dominant channel
- Local currency
- Market fraud index
- Regulatory tier

`dim_worker`

Contains:

- Worker characteristics
- Account tenure
- Account tenure band
- Age band
- Gender
- Gig segment
- KYC tier
- Preferred channel
- Risk score
- Active-worker status

`dim_date`

Contains:

- Full date
- Date ID
- Month
- Month number
- Month-year
- Day of week
- Weekend flag
- Month-end flag
- Month-end status

A dedicated **Measures table** was used to organise DAX calculations.

---

## 📊 Dashboard Structure

The project contains four analytical pages.

### 1️⃣ Executive Overview

This page provides a high-level summary of wallet activity and transaction performance.

#### Key KPIs

- **Total Transactions:** 50,000
- **Transaction Value:** $24.98M
- **Average Transaction Value:** $499.51
- **Unique Workers:** 4,999
- **Fraud Rate:** 50.29%

#### Analysis Includes

- Transaction value and fraud rate by month
- Transactions by gig segment
- Transactions by channel type
- Transaction value by country
- Transaction value by transaction type
- Transaction value by channel

### Key Insight

Transaction activity is substantial and geographically distributed, but the overall fraud rate remains very high, making risk analysis essential.

---

### 2️⃣ Fraud & Risk Intelligence

This page focuses on fraud activity, financial loss and reversal exposure.

#### Key KPIs

- **Fraud Rate:** 50.29%
- **Fraud Transactions:** 25,145
- **Fraud Loss:** $12.56M
- **Average Fraud Loss:** $499.47
- **Reversal Rate:** 49.90%

#### Analysis Includes

- Fraud rate by channel
- Fraud rate by KYC tier
- Reversal rate by channel
- Fraud loss by country
- Fraud rate by gig segment
- Average fraud loss by channel

### Key Insight

Fraud is spread across the ecosystem rather than concentrated in one market.

USSD records the highest displayed channel fraud rate at approximately **51.19%**, while Agent transactions record the lowest at approximately **49.33%**.

---

### 3️⃣ Gig Worker & Customer Risk

This page examines worker characteristics and customer risk factors.

#### Key KPIs

- **Active Workers:** 2,441
- **Average Account Tenure:** 906.62 days
- **Average Risk Score:** 50.43
- **Tier 0 Workers:** 1,280
- **Unique Workers:** 4,999

#### Analysis Includes

- Fraud rate by preferred channel
- Fraud rate by age band
- Unique workers by KYC tier
- Fraud loss and worker count by gender
- Unique workers by account-tenure band
- Fraud loss by country

### Key Insight

Fraud risk varies across customer dimensions including:

- Age
- KYC tier
- Account tenure
- Preferred channel
- Gig segment
- Worker risk score

This indicates that customer risk should be evaluated using multiple characteristics rather than a single variable.

---

### 4️⃣ Performance & Emerging Risk

This page evaluates operational efficiency and transaction outcomes.

#### Key KPIs

- **Average Processing Time:** 500.34 ms
- **Completed Rate:** 12.64%
- **Decline Rate:** 12.44%
- **Timeout Rate:** 12.60%
- **Pending Rate:** 12.52%

#### Analysis Includes

- Processing time by preferred channel
- Timeout rate by channel subtype
- Pending rate by transaction type
- Decline rate by transaction type
- Digital Wallet Transaction Funnel
- Average processing time by country

### Key Insight

Operational outcomes are relatively evenly distributed across completion, decline, timeout and pending categories.

Certain transaction types, such as **Agent Withdrawal**, show elevated decline and pending rates and may require further operational investigation.

---

## 🔍 Key Findings

The analysis revealed several important insights:

- The ecosystem processed **50,000 transactions**
- Total transaction value reached approximately **$24.98M**
- Average transaction value was approximately **$499.51**
- **4,999 unique workers** generated transaction activity
- The overall fraud rate was **50.29%**
- Approximately **25,145 transactions** were fraud-flagged
- Recorded fraud loss totalled approximately **$12.56M**
- Reversal rate was approximately **49.90%**
- USSD recorded the highest displayed fraud rate by channel
- Fraud exposure varies across KYC tiers and gig-worker segments
- Approximately **1,280 workers** were classified as Tier 0 / unverified
- Average processing time was approximately **500.34 ms**
- Completion, decline, timeout and pending rates were each around **12%–13%**
- Agent Withdrawal showed elevated decline and pending rates relative to several other transaction types

---

## 💡 Strategic Recommendations

### Strengthen High-Risk Channel Monitoring

Apply stronger transaction monitoring to channels with elevated fraud rates, especially USSD.

### Improve KYC Verification

Encourage Tier 0 workers to progress through stronger verification levels.

### Use Multi-Dimensional Risk Rules

Combine:

- Country
- Channel
- Gig segment
- KYC tier
- Transaction type
- Account tenure
- Risk score

to develop stronger fraud-monitoring rules.

### Monitor Fraud Loss Alongside Fraud Rate

Fraud frequency should be assessed together with financial loss to identify where risk has the greatest monetary impact.

### Investigate High-Risk Transaction Types

Review transaction types with elevated:

- Decline rates
- Timeout rates
- Pending rates
- Reversal exposure

### Improve Transaction Completion

Investigate why a relatively small proportion of transactions reach full completion.

### Monitor Processing Performance

Use transaction-processing time as an operational KPI to identify slower channels and markets.

---

## 🛠 Tools & Technologies

- **Power BI**
- **Power Query**
- **DAX**
- **HTML**
- **CSS**
- **Star Schema Data Modelling**
- **Data Visualisation**
- **Risk Analytics**
- **Customer Analytics**
- **Operational Analytics**
- **Data Storytelling**

---

## 🎨 Custom Visual Development

In addition to standard Power BI visuals, custom **HTML/CSS visuals** were created to enhance the analytical experience.

Examples include:

- Digital Wallet Transaction Funnel
- Dynamic reference labels
- Heatmap matrices
- Risk-comparison visuals
- Processing-time matrices
- Custom KPI presentation

These visuals were designed to support clearer storytelling while maintaining a consistent blue-themed dashboard design.

---

## 💼 Business Value

The dashboard supports:

### Executive Management

Monitor wallet activity, transaction value and ecosystem-wide risk.

### Fraud & Risk Teams

Identify high-risk channels, customer groups and transaction patterns.

### Operations Teams

Monitor processing performance, pending transactions, declines and timeouts.

### Customer Risk Teams

Analyse worker behaviour by KYC tier, age, account tenure and preferred channel.

### Market Managers

Compare activity and risk across Nigeria, Kenya, Ghana and South Africa.

### Data & BI Teams

Use an integrated analytical model combining transaction, market, worker, channel and date information.

---

## 📈 Skills Demonstrated

This project demonstrates practical capability in:

- Power BI dashboard development
- Data modelling
- DAX development
- Power Query transformation
- Risk analytics
- Fraud analysis
- Customer segmentation
- Operational performance analysis
- Custom HTML/CSS visualisation
- Data storytelling
- Executive reporting
- Business intelligence

---

## 📌 Conclusion

The **African Digital Wallet Ecosystem Dashboard** demonstrates how business intelligence can be used to analyse a complex digital-payment environment.

The dashboard combines transaction, customer, channel, market and operational data to provide an integrated view of performance and risk.

The analysis highlights strong transaction activity alongside significant fraud and reversal exposure.

It also demonstrates that risk is multi-dimensional and varies across payment channels, KYC tiers, customer characteristics and transaction types.

This project showcases my ability to build an end-to-end Power BI analytical solution, from data modelling and DAX development to custom HTML/CSS visualisation, dashboard design and executive data storytelling.

---

## 📷 Dashboard Preview

### Executive Overview
<img width="1285" height="726" alt="gig1" src="https://github.com/user-attachments/assets/00258f8a-db41-410c-bf58-ae870380602f" />


### Fraud & Risk Intelligence

<img width="1281" height="725" alt="gig2" src="https://github.com/user-attachments/assets/9455762c-76ef-4dce-8dd7-541b487bfe4a" />


### Gig Worker & Customer Risk

<img width="1280" height="728" alt="gig3" src="https://github.com/user-attachments/assets/42f223f6-7ee3-4e8f-8e4d-8589880c27f5" />


### Performance & Emerging Risk

<img width="1285" height="727" alt="gig4" src="https://github.com/user-attachments/assets/a9507a46-909f-4cf8-a59a-bdd618694e2a" />


### Data Model
<img width="1485" height="794" alt="gig model" src="https://github.com/user-attachments/assets/f7de65f7-9136-47f6-8e52-899d26462c53" />


---

## 📂 Repository Structure

```text
African-Digital-Wallet-Ecosystem/
│
├── README.md
├── images/
│   ├── executive-overview.png
│   ├── fraud-risk.png
│   ├── gig-worker-risk.png
│   ├── performance-risk.png
│   └── data-model.png
│
├── dashboard/
│   └── African-Digital-Wallet-Ecosystem.pbix
│
├── data/
│   └── dataset.csv
│
└── docs/
    └── project-notes.md
