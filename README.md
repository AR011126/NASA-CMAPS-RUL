============THIS PROJECT IS A WORK IN PROGRESS===============
A production style implementation of an end-to-end Remaining Useful Life (RUL) prediction pipeline using the NASA CMAPSS Turbofan Degredation Dataset (FD001-FD004)
This project includes:
- Data ingestion (raw CMAPSS text files into cleaned SQL tables)
- Data cleaning and processing
- Feature engineering
- Model training 
- Model evaluation
- Feature importance and SHAP explainability


PROJECT STRUCTURE
NASA-DATASET/
├── data/
└── raw/ # Raw CMAPSS text files (ignored by Git)
│
├── notebooks/
│ └── 01_data_preparation.ipynb
│
├── sql/
│ └── create_tables.sql
│ └── load_clean_fd001.sql
│
├── src/
│ ├── data_loader.py # Raw → cleaned dataset logic
│ ├── feature_engineering.py
│ ├── models.py
│ ├── utils.py
│
├── models/ # Saved ML models (ignored by Git)
│
├── .env # MySQL credentials (ignored by Git)
├── .gitignore
└── README.md


DATASET
The project uses NASA CMAPSS Dataset, specifically for the four fault conditions:
- FD001 - single operational condition, single fault
- FD002 - multiple operational conditions
- FD003 - single condition, multiple faults
- FD004 - multiple conditions, multiple faults



SETUP
1) Clone repository

git clone https://github.com/AR011126/NASA-CMAPSS-RUL.git
cd NASA-CMAPSS-RUL

2) Install Dependencies
pip install -r requirements.txt

3) Configure environment variables
Create a .env file and add:
MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=yourpassword
MYSQL_DATABASE=nasa_cmaps
# NASA-CMAPSS-RUL
