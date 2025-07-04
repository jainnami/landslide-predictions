  <h1>🌍 Landslide Prediction and Analysis</h1>
  <p><strong>Authors:</strong> Theodore Li, Drew Keely, Devanshu Khadka, Nami Jian</p>
  <p><strong>Date:</strong> October 18, 2024</p>

  <h2>📌 Project Overview</h2>
  <p>
    This project analyzes landslide data collected globally to identify temporal and spatial patterns, assess triggers, and develop predictive models. We use unsupervised clustering to group geographic regions and apply supervised learning models, such as Random Forest and XGBoost, to predict landslide-prone regions based on historical data.
  </p>

  <h2>📁 Files</h2>
  <ul>
    <li><code>Landslide_models-2.pdf</code> – Final report and analysis write-up</li>
    <li><code>GLC03122015_20241114.csv</code> – Dataset used for modeling</li>
    <li><code>R scripts and visualizations</code> – Analysis and modeling code (see R Markdown)</li>
  </ul>

  <h2>🔍 Key Steps in Analysis</h2>
  <ol>
    <li><strong>Data Preprocessing:</strong> Cleaned the dataset, extracted date features, and removed missing values.</li>
    <li><strong>Feature Engineering:</strong> Extracted year and month, removed coordinates to prevent data leakage, and encoded categorical variables.</li>
    <li><strong>Clustering:</strong> Applied DBSCAN to identify landslide regions using latitude and longitude.</li>
    <li><strong>Exploratory Data Analysis:</strong> Visualized landslide occurrences by month and year to identify seasonal and temporal trends.</li>
    <li><strong>Train/Test Split:</strong> Used time-based split (2007–2011 for training, 2012+ for testing) to prevent data leakage.</li>
  </ol>

  <h2>📈 Models Used</h2>
  <ul>
    <li><strong>Random Forest:</strong> Baseline accuracy of 54.8%. After hyperparameter tuning using grid search (mtry and ntree), accuracy improved to ~68%.</li>
    <li><strong>XGBoost:</strong> Implemented as an advanced tree-based model. Without tuning, XGBoost achieved even higher accuracy, showing promise for future modeling.</li>
  </ul>

  <h2>🧪 Key Insights</h2>
  <ul>
    <li>Most frequent landslide triggers: heavy rainfall, earthquakes, construction.</li>
    <li>Spatial clustering showed geographic dependencies in landslide occurrences.</li>
    <li>Seasonal trends suggest increased landslides during summer months, especially July and August.</li>
    <li>Temporal trends indicate fluctuating frequency of events, possibly due to climate changes.</li>
  </ul>

  <h2>📊 Visualizations</h2>
  <ul>
    <li>World map with landslide data points</li>
    <li>Bar charts showing landslide frequencies by month</li>
    <li>Line plots of yearly occurrences</li>
  </ul>

  <h2>⚠️ Considerations</h2>
  <ul>
    <li>Coordinates were excluded as predictors to prevent overfitting and data leakage.</li>
    <li>Time-aware train/test split better simulates real-world prediction scenarios.</li>
    <li>Multiclass classification (86+ regions) adds complexity to the model.</li>
  </ul>

  <h2>📦 Requirements</h2>
  <ul>
    <li>R (>= 4.0)</li>
    <li>R packages: <code>ggplot2</code>, <code>randomForest</code>, <code>xgboost</code>, <code>caret</code>, <code>dplyr</code>, <code>kableExtra</code>, <code>dbscan</code>, <code>maps</code></li>
  </ul>

  <h2>📖 How to Run</h2>
  <ol>
    <li>Load the data from <code>GLC03122015_20241114.csv</code>.</li>
    <li>Run the RMarkdown file to generate plots, preprocessing, clustering, and model fitting.</li>
    <li>Review model results and visualizations saved in the output folder or embedded in the final report.</li>
  </ol>

  <h2>📜 License</h2>
  <p>This project is for educational purposes and follows the Virginia Tech data science course guidelines.</p>

</body>
</html>
