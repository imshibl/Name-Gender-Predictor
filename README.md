# Name Gender Prediction using Machine Learning

A Python machine learning project to predict the gender of a given name.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Gender prediction based on a person's name is a common natural language processing (NLP) task. This project uses machine learning to predict whether a given name is male or female. It includes a pre-trained model that can be used for predictions and serves as a starting point for similar NLP tasks.

## Features

- Name gender prediction based on machine learning.
- Uses TF-IDF vectorization and a MultinomialNB.
- Pre-trained model for quick predictions.
- Easily customizable for your own dataset.

## Requirements

- Python 3.x
- pandas
- scikit-learn
- joblib (for saving and loading models)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/name-gender-prediction.git
   ```

2. Navigate to the project directory:

   ```bash
   cd name-gender-prediction
   ```

3. Install the required Python packages

## Usage

To predict the gender of a name using the pre-trained model:

```python
import joblib

# Load the pre-trained model
loaded_model = joblib.load('gender_predictor.pkl')

# Example name for prediction
new_name = "Alice"
new_name = [new_name.lower()]

# Use the loaded model for prediction
predicted_gender = loaded_model.predict(new_name)

# Display the predicted gender (0 for male, 1 for female)
if predicted_gender[0] == 0:
    print("Predicted Gender: Male")
else:
    print("Predicted Gender: Female")
```

Replace `"Alice"` with the name you want to predict.

## Model Training

If you want to retrain the model with your own dataset or fine-tune it:

1. Prepare your dataset in CSV format with columns "Name" and "Gender."
2. Replace `'name_dataset.csv'` in the code with the path to your dataset.
3. Run the training code and follow the instructions in the [Model Training](#model-training) section of the README.

## Contributing

Contributions are welcome! If you want to contribute to this project, please follow the guidelines in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
```
