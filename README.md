# Post-Harvest Loss Reduction Advisor

**Team A15** | Domain 3: Agriculture & Rural AI

**Members:**

* Prasanna Anagal (120 | 01fe23bcs097)
* Sahana R (129 | 01fe23bcs138)
* Rachana Rane (130 | 01fe23bcs150)
* Vindhya Hegde (131 | 01fe23bcs160)

---

## Problem Statement

India experiences significant post-harvest losses due to improper storage, pest infestation, moisture imbalance, and inefficient handling practices. Farmers often lack access to timely, localized, and actionable advisory services after harvest.

The Post-Harvest Loss Reduction Advisor is designed to assist farmers by generating AI-powered post-harvest management plans tailored to crop type, quantity, storage conditions, and region.

---

## Solution Overview

The system is a Streamlit-based web application that allows farmers to enter:

* Crop type
* Harvest quantity
* Region (District, State)
* Storage method
* Moisture percentage

Using FAO post-harvest loss data and a Groq-powered Large Language Model (Llama 3.3 70B), the application generates a personalized advisory report containing:

1. Storage Recommendations
2. Pest Control Measures
3. Moisture Management
4. Transport & Handling Best Practices
5. Financial Impact & Government Support

The generated report is available in both English and Kannada and can be downloaded as a DOCX document.

---

## Tech Stack

| Component          | Technology                     |
| ------------------ | ------------------------------ |
| Frontend & Backend | Streamlit                      |
| LLM API            | Groq (Llama 3.3 70B Versatile) |
| Translation        | Google Translator              |
| Data Processing    | Pandas                         |
| Document Export    | python-docx                    |
| Data Source        | FAO Food Loss & Waste Database |
| Language           | Python                         |

---

## Features

### 1. Farmer Input Form

The application collects:

* Crop Type

  * Rice
  * Wheat
  * Maize
  * Pulses
  * Groundnut

* Harvest Quantity (kg)

* District and State

* Storage Type

  * Gunny Bags
  * Plastic Silo
  * Metal Bin
  * Open Shed
  * Warehouse

* Moisture Percentage

---

### 2. AI-Powered Management Plan

The system generates a detailed advisory with five structured sections:

#### Storage Recommendations

Safe storage methods and infrastructure recommendations.

#### Pest Control Measures

Identification of likely storage pests and mitigation strategies.

#### Moisture Management

Drying and moisture control recommendations to prevent spoilage.

#### Transport & Handling Best Practices

Methods to reduce losses during movement and handling.

#### Financial Impact & Government Support

Expected loss estimation and relevant support schemes.

---

### 3. FAO-Based Loss Analysis

The application uses official FAO Food Loss and Waste Database records to:

* Estimate post-harvest losses
* Calculate quantity at risk
* Estimate financial loss
* Provide stage-wise loss insights

---

### 4. Pest Risk Calendar

Provides:

* Crop-specific pests
* Peak occurrence seasons
* Risk level classification
* Damage description
* Recommended control measures

---

### 5. Government Scheme Eligibility

Based on farmer inputs, the application displays:

* Available support schemes
* Subsidy information
* Benefit descriptions
* Contact details

---

### 6. Kannada Translation

The generated advisory is translated into Kannada, making recommendations accessible to regional farmers.

---

### 7. DOCX Report Export

Users can download a complete report containing:

* Farmer details
* Loss analysis
* AI-generated advisory
* Pest information
* Scheme recommendations
* English and Kannada content

---

## Data Source

### FAO Food Loss & Waste Database

The application uses official FAO Food Loss and Waste Database records to obtain crop-specific post-harvest loss percentages.

The dataset is used for:

* Loss estimation
* Financial risk calculation
* Context generation for AI recommendations
* Displaying stage-wise loss information

---

## Installation

### Prerequisites

* Python 3.8+
* Groq API Key

### Clone Repository

```bash
git clone https://github.com/Sahana8866/hackathon_ruralAI.git
cd hackathon_ruralAI
```

### Create Virtual Environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

Linux / Mac:

```bash
python -m venv venv
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure API Key

Create:

```text
.streamlit/secrets.toml
```

Add:

```toml
GROQ_API_KEY = "your-groq-api-key"
```

### Run Application

```bash
streamlit run app.py
```

---

## Project Structure

```text
hackathon_ruralAI/
│
├── app.py
├── README.md
├── requirements.txt
│
├── .streamlit/
│   └── secrets.toml
│
├── data/
│   └── Data.csv
│
└── utils/
    ├── __init__.py
    ├── data_loader.py
    └── exporter.py
```

---

## Usage

1. Launch the Streamlit application.
2. Fill the farmer details form.
3. Click **Generate Management Plan**.
4. Review:

   * Management Plan
   * Pest Calendar
   * Government Schemes
   * Kannada Translation
5. Download the generated DOCX report.

---

## Future Enhancements

* Real-time weather integration
* Mobile application support
* Voice-based farmer interaction
* Multilingual support beyond Kannada
* District-specific advisory generation

---

## Acknowledgments

* FAO Food Loss & Waste Database
* Groq Llama 3.3 70B
* Streamlit
* Python Open Source Community

---

### Team A15

**Post-Harvest Loss Reduction Advisor**

Agriculture & Rural AI Hackathon Project
