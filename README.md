# 🌾 Post-Harvest Loss Reduction Advisor
**Team A15** | Domain 3: Agriculture & Rural AI

| Name | Roll No | USN |
|---|---|---|
| Prasanna Anagal | 120 | 01FE23BCS097 |
| Sahana R | 129 | 01FE23BCS138 |
| Rachana Rane | 130 | 01FE23BCS150 |
| Vindhya Hegde | 131 | 01FE23BCS160 |

---

## 🚀 Setup & Run

```bash
# 1. Activate your venv
venv\Scripts\activate          # Windows
# source venv/bin/activate     # Mac/Linux

# 2. Install dependencies
pip install -r requirements.txt

# 3. Generate all datasets (run once)
python data/download_datasets.py

# 4. Run the app
streamlit run app.py
```

---

## 📁 Project Structure

```
hackathon/
├── app.py                        ← Main Streamlit application
├── requirements.txt
├── README.md
├── .streamlit/
│   └── secrets.toml             ← GROQ_API_KEY goes here
├── data/
│   ├── download_datasets.py     ← Run once to generate all CSVs
│   ├── fao_postharvest_loss.csv ← FAO stage-wise loss data
│   ├── govt_schemes.csv         ← AMIF, WDPSA, PMKSY, Gramin Bhandaran
│   ├── pest_calendar.csv        ← 17 pests, peak seasons, controls
│   ├── imd_storage_risk.csv     ← Month-wise humidity & risk
│   └── icar_storage_standards.csv ← Target MC, bag type, fumigants
└── utils/
    ├── __init__.py
    ├── data_loader.py           ← All dataset query functions
    └── exporter.py              ← DOCX report builder
```

---

## 🗃️ Datasets

| Dataset | Source | Records |
|---|---|---|
| FAO Post-Harvest Loss | fao.org/platform-food-loss-waste | 26 rows (5 crops × stages) |
| Govt Schemes | NABARD, WDRA, MoFPI | 4 schemes |
| Pest Calendar | ICAR / KVK Karnataka | 17 pest records |
| IMD Storage Risk | imd.gov.in | 12 monthly records |
| ICAR Standards | icar.org.in | 5 crop standards |

---

## ✨ Features

- **5-section personalised plan** from Groq LLaMA 3.3 70B
- **FAO data integration** — shows stage-wise loss % and ₹ risk value
- **ICAR standards** — target MC, fumigants, bag types per crop
- **17-pest calendar** with risk badges, controls, peak seasons
- **4 govt schemes** — auto-eligibility check based on crop/quantity/region
- **IMD weather strip** — current month storage risk for Karnataka
- **Bilingual DOCX export** — English + Kannada with tables
- **Premium UI** — DM Serif Display + DM Sans, earthy green palette
