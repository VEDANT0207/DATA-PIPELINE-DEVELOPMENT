# DATA-PIPELINE-DEVELOPMENT

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : VEDANT RAMESH KAWARE

*INTERN ID* : CT08DN595

*DOMAIN* : DATA SCIENCE

*DURATION* : 8 WEEKS

*MENTOR* : NEELA SANTOSH

##This project involved designing and implementing a complete ETL (Extract, Transform, Load) pipeline using Python on a real-world health dataset. The primary goal was to automate the process of reading raw medical insurance data, cleaning and transforming it through a structured data preprocessing pipeline, and finally exporting the clean, machine learning–ready data. The entire project was developed using the Jupyter Notebook environment, a popular web-based coding interface ideal for data science workflows. All coding was done in Python, leveraging standard libraries like Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn.

The dataset used in this project is the Medical Insurance dataset, which contains health and demographic data for individuals, including age, sex, BMI, number of children, smoking status, region, and annual insurance charges. The column charges serves as the target variable. This dataset was chosen for its rich combination of both numerical and categorical features, as well as its relevance to real-world problems in healthcare cost prediction and insurance analytics. The raw dataset was loaded from an online GitHub link, extracted into a Pandas DataFrame, and saved locally as insurance.csv.

Once extracted, the transformation phase began with Exploratory Data Analysis (EDA). Visualizations such as histograms, correlation heatmaps, and boxplots were used to explore relationships between features and the target variable. It was observed that smoker status had a significant influence on medical charges, while age and BMI showed moderate correlation. EDA also revealed that the dataset was complete, with no missing values. Numerical columns were identified as age, bmi, children, and charges, while sex, smoker, and region were identified as categorical.

The core of the project was building an automated data preprocessing pipeline using Scikit-learn. Two sub-pipelines were constructed: one for numerical data that handled mean imputation and standard scaling, and another for categorical data that performed mode imputation and OneHotEncoding. These were combined using Scikit-learn’s ColumnTransformer to enable parallel and organized preprocessing of the different data types. This design ensured that any similar dataset could be processed in a reproducible, scalable, and modular way.

Before transformation, the dataset was split into features (X) and target (y). To avoid processing errors, numerical and categorical columns were re-identified after dropping the target column. This correction was necessary because the pipeline would otherwise look for a column (charges) that no longer existed in the feature set. After this, the full pipeline was fitted and applied to X, producing a fully numeric, clean, and transformed dataset.

In the final load step, the transformed dataset was split into training and testing sets in an 80:20 ratio using train_test_split. The resulting X_train and y_train datasets were saved as .csv files, which now serve as the output of the ETL pipeline and are ready for direct input into machine learning models. These files are organized and labeled, making them easy to integrate into any model-building pipeline.

From a learning standpoint, this project offered deep insights into designing reusable data workflows and pipelines. It reinforced the importance of clean data preparation before modeling, helped me develop confidence in handling both numerical and categorical data, and taught me how to debug and resolve real-world errors that occur when working with pipeline components. The use of EDA also helped me discover important feature relationships — particularly the dominant influence of smoking on insurance costs — which are relevant for real-world decision-making in healthcare and insurance industries.

This project is especially useful for anyone who wants to build predictive models related to cost estimation, medical billing, insurance planning, or health analytics. The pipeline structure is flexible and can be adapted for other structured datasets in different industries. By the end of the project, I gained practical skills in modular pipeline design, data transformation logic, and automated preprocessing — all critical components in the data science lifecycle
