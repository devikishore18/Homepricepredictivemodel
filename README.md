 ## 🏡 **Bangalore Home Price Prediction**
 
This full-stack machine learning project predicts real estate prices in Bangalore using a dataset from Kaggle. It transforms raw housing data into actionable insights through data preprocessing, model training, API development, and a user-friendly web interface. The application is designed for real-world use, enabling buyers, analysts, and investors to obtain real-time home price estimates.

## 📊 **Dataset Source**: 
Bengaluru House Price Data on Kaggle

- **Size**: ~13,000 records

- **Features**: Location, square footage, number of bedrooms (BHK), bathrooms, price, and more

## 🧠 **Project Workflow**

**1. Data Cleaning & Feature Engineering**
   
- Handled missing values and standardized inconsistent entries.

- Converted range-based square footage entries (e.g., "2100–2850") into numeric averages.

- Extracted BHK from textual data and calculated price_per_sqft.

- Aggregated rare locations into an "other" category to reduce dimensionality.

- Filtered outliers, such as entries where the number of bathrooms exceeds the number of BHKs.

**2. Exploratory Data Analysis (EDA)**

- Visualized data distributions and trends using histograms and scatter plots.

- Identified and addressed skewed data and location-based price patterns.

- Informed outlier removal and feature scaling decisions.

**3. Model Building & Validation**

- Implemented Linear Regression as a baseline model.

- Applied one-hot encoding to categorical features like location.

- Performed hyperparameter tuning using GridSearchCV.

- Evaluated models using K-Fold cross-validation with MAE, MSE, and R² metrics.

**4. API Development**

- Serialized the trained model using pickle.

- Developed a Flask API with endpoints:

- `/get_location_names`: Retrieves available locations.

- `/predict_home_price`: Returns price predictions based on user input.

**5. Front-End Interface**

- Built a responsive UI using HTML, CSS, and JavaScript.

- Enabled users to input area, BHK, bathrooms, and location.

- Integrated the front-end with the Flask API to fetch and display predictions in real-time.

**🛠️ Tech Stack**

- **Data & Modeling**: Python, NumPy, Pandas, Matplotlib, Seaborn, Scikit-Learn

- **Development Tools**: Jupyter Notebook, VS Code / PyCharm

- **API**: Flask

- Front-End: HTML, CSS, JavaScript

**📈 Sample Prediction**

To predict the price of a 2 BHK, 1000 sqft house with 2 bathrooms in "Whitefield":

curl -X POST http://localhost:5000/predict_home_price \
     -H "Content-Type: application/json" \
     -d '{"total_sqft": 1000, "location": "Whitefield", "bhk": 2, "bath": 2}'

Response:

{"estimated_price": 75.0}

## **📞 Contact**
For questions, feedback, or collaboration, feel free to reach out:
Email: devikishore18@gmail.com
LinkedIn: https://www.linkedin.com/in/devikishore18/



