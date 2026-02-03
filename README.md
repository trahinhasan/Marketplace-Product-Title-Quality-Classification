# Marketplace-Product-Title-Quality-Classification
Built a Random Forest–based ML system to classify marketplace product titles into Good, Mediocre, and Bad categories using real Walmart product listing data.

I built an end-to-end machine learning system to classify marketplace product titles into Good, Mediocre, and Bad quality categories. The goal was to automatically identify poorly constructed titles that negatively affect search relevance and user experience. I used a Random Forest classifier trained on real Walmart product listing data, where I engineered features directly from the product titles such as brand presence, color keywords, material indicators, numeric information, and title length.

Product titles play a critical role in e-commerce platforms. Poorly written titles reduce discoverability and hurt conversion rates. I chose this problem because it has a direct business impact and allowed me to work on real-world, noisy text data rather than clean benchmark datasets.

I used Random Forest because this problem relies heavily on interpretable, rule-based features such as the presence of measurements, brand names, and descriptive attributes. Random Forest handles non-linear feature interactions well, works effectively on structured features extracted from text, and provides feature importance for explainability, which is important for production systems.

The dataset did not contain predefined quality labels, so I created labels using business-driven rules. Titles containing multiple informative elements such as brand names, attributes, measurements, and sufficient length were labeled as Good. Titles with partial information were labeled as Mediocre, and vague or very short titles were labeled as Bad. This approach simulates how marketplace quality teams manually evaluate titles.

I extracted multiple structured features from unstructured text, including title length, count of numeric characters, presence of brand keywords, color descriptors, material indicators, and measurement-related tokens. These features help quantify how informative a product title is.

I evaluated the model using precision, recall, and F1-score instead of relying solely on accuracy. Since the dataset contains class imbalance between Good, Mediocre, and Bad titles, F1-score provided a more balanced evaluation of performance across classes.

Based on feature importance from the Random Forest model, numeric information such as size and capacity, title length, and brand presence were the most influential features in determining title quality. This aligns well with how humans assess product titles.

The biggest challenge was working with noisy, real-world product titles that lacked consistent structure. Additionally, creating reliable labels without ground truth required careful rule design to avoid bias while still reflecting business realities.

I would improve this system by incorporating semantic embeddings using transformer models for deeper contextual understanding, introducing human-in-the-loop validation for labeling, and extending the model to support multilingual product titles.

I built a Random Forest–based ML system using real marketplace data to automatically assess product title quality and improve e-commerce listing standards.
