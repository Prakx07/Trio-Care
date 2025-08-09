# Trio-Care
pip install -r requirements.txt
pandas
numpy
scikit-learn
matplotlib
seaborn
TrioCare/
│
├── data/                     # Dataset files
├── notebook/                 # Jupyter notebooks for experiments
├── src/                      # Python scripts for preprocessing, training, and evaluation
│   ├── preprocess.py
│   ├── train.py
│   ├── evaluate.py
│
├── requirements.txt
├── README.md
└── main.py                    # Entry point to run the model
age,blood_pressure,cholesterol,diabetes
45,130,high,yes
50,120,normal,no
python src/preprocess.py --input data/health_data.csv --output data/processed.csv
python src/train.py --data data/processed.csv --model models/random_forest.pkl
python src/evaluate.py --model models/random_forest.pkl --test data/test.csv
python main.py
Accuracy: 92%
Precision: 90%
Recall: 93%
F1-score: 91.5%
