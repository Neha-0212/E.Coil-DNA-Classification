DNA Promoter Sequence Classifier
A Django-based web application that uses a Multi-Layer Perceptron (MLP) classifier to predict E. coli virus presence from DNA promoter sequences. The model analyzes genomic data (A, C, G, T nucleotides) and provides real-time predictions via a user-friendly interface.

Features
ML Model: Trained on a 106-sample dataset with 92-100% accuracy using one-hot encoding and scikit-learn.
Web Interface: Django app for inputting sequences and viewing predictions.
Preprocessing: Handles sequence cleaning, encoding, and model serialization with Pickle.
Visualization: Includes loss curves and confusion matrices for model evaluation.
Installation
Clone the repository: git clone https://github.com/yourusername/dna-promoter-classifier.git
Navigate to the project: cd dna-promoter-classifier
Create a virtual environment: python -m venv myenv and activate it (myenv\Scripts\activate on Windows or source myenv/bin/activate on macOS/Linux).
Install dependencies: pip install -r requirements.txt (includes Django, scikit-learn, NumPy, Pandas, etc.).
Run migrations: python manage.py migrate
Start the server: python manage.py runserver
Access at http://127.0.0.1:8000/
Usage
Input a DNA sequence (e.g., "ACGT...") in the web form.
The model preprocesses and predicts: "Has E. coli virus" or "Does not have E. coli virus."
For model retraining, use the provided Jupyter notebook (model_training.ipynb) with the dataset.
Model Details
Algorithm: MLP Classifier with hidden layers (150, 50 nodes), ReLU activation, and Adam solver.
Preprocessing: Removes tabs/slashes, one-hot encodes nucleotides.
Evaluation: Confusion matrix, precision/recall, and accuracy metrics.
Files: mlp_model.pkl (trained model), onehot_encoder.pkl (encoder).
Contributing
Feel free to fork and submit pull requests. For issues, open a GitHub issue.

License
MIT License. See LICENSE for details.

Acknowledgments
Inspired by bioinformatics research on DNA promoters and diseases. Dataset sourced from public repositories.



