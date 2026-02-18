📦 OTTO Session Pattern Mining – Frequent Itemsets vs Sequential Patterns
📌 Project Overview

This project explores behavioral pattern mining in large-scale e-commerce session data using the OTTO Recommender Systems Dataset.

The goal is to compare:

Unordered frequent itemsets and association rules (course technique)

Sequential pattern mining (beyond-course technique)

The analysis investigates whether incorporating temporal ordering reveals behavioral structures that unordered co-occurrence patterns may miss.

📊 Dataset

Source:
https://www.kaggle.com/datasets/otto/recsys-dataset

Structure:

Session-based interaction logs (JSONL format)

Each session contains time-ordered events:

aid (item ID)

ts (timestamp)

type (clicks, carts, orders)

Scale:

~12 million sessions

~220+ million interaction events

For exploratory analysis, a 20,000-session sample was used to maintain computational feasibility while preserving distributional properties.

🔍 Exploratory Findings

Initial analysis revealed:

Heavy-tailed session length distribution

Strong interaction imbalance (91% clicks, <2% orders)

Long-tail item popularity (Top 1% items account for ~19% of events)

These structural characteristics motivate comparison between static co-occurrence mining and temporal sequence mining.

🧠 Research Questions

How does varying support thresholds affect association rule quality?

Do sequential patterns reveal behavioral structure missed by frequent itemsets?

Does temporal ordering better capture high-intent session behavior?

⚙️ Methods
Course Technique

Frequent Itemset Mining

Association Rule Mining

Beyond-Course Technique

Sequential Pattern Mining

🗂 Repository Structure
.
├── notebooks/
│   └── checkpoint1_eda.ipynb
├── data/                # Not included in repo (large Kaggle dataset)
├── README.md
└── requirements.txt

🚀 How to Run

Download the OTTO dataset from Kaggle.

Place otto-recsys-train.jsonl inside a local data folder.

Update the file path in the notebook if necessary.

Run the notebook cells sequentially.

🛠 Requirements

Python 3.9+

pandas

matplotlib

numpy

mlxtend (for association rules)

prefixspan or similar library (for sequential mining)

You can install dependencies with:

pip install pandas matplotlib numpy mlxtend

📚 Academic Context

This project was developed as part of a data mining course requirement. It demonstrates:

Structured dataset evaluation

Professional exploratory data analysis

Bias-aware interpretation

Comparative methodological reasoning

📄 Collaboration Declaration

All analysis was conducted independently. AI assistance (ChatGPT) was used for structuring documentation and refining explanations. All code was verified and executed locally.

👤 Author

Bhaumik Patel
MS in Management Information Systems
Texas A&M University
