 I built a full-stack application using the Bangalore home prices dataset from Kaggle, taking it from raw data through to a predictive web interface by transforming raw data into actionable insights. It’s designed for real-world use, letting anyone—buyers, analysts, investors—get real-time home price estimates for Bangalore!. Here's a snapshot of what I tackled:
1.Data Cleaning & Feature Engineering
     #Processed ~13,000 records: handled missing values and transformed fields like “2100–2850” sqft into numeric averages.
      #Extracted bedrooms (BHK) from text, calculated price_per_sqft, and aggregated rare locations into an “other” category. Outliers and inconsistent entries—e.g., bathroom count exceeding BHK—were filtered out
2. Exploratory Data Analysis:
       #Visualized distributions and trends to uncover skewed data and location-based price patterns.
       #Used scatter plots and histograms to inform outlier removal and feature scaling.
3. Model Building & Validation
        #Started with Linear Regression as a baseline.
        #Engineered additional features and applied one‑hot encoding to location
        #Tuned hyperparameters via GridSearchCV and evaluated models using K‑Fold cross‑validation (MAE, MSE, R² metrics).
4. API Integration
         #Pickled the best model and exposed it via a lightweight Flask API to serve price predictions.
         #Created endpoints like /get_location_names and /predict_home_price for easy front-end access.
5. Front-End Interface
          #Built a clean HTML/CSS/JavaScript UI that lets users input area, BHK, bathrooms, and location, then fetch predictions from the Flask API in real time.
Tech Stack:
Data & Modeling:  Python, NumPy, Pandas, Matplotlib, Seaborn, Scikit‑Learn
Development:	Jupyter Notebook, VS Code / PyCharm
API: Flask
Frontend: HTML, CSS, JavaScript
