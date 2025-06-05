# Wine Quality Prediction

This project implements a machine learning model to predict wine quality using decision trees. The model is trained on the Wine Quality dataset and can predict wine quality based on various physicochemical properties.

## Features

- Wine quality prediction using Decision Tree Classifier
- Two different splitting criteria: Gini Index (Possible to use Entropy as well)
- Model evaluation with accuracy metrics and confusion matrix
- Decision tree visualization
- Support for both training and prediction phases

## Prerequisites

Before running this project, make sure you have the following Python packages installed:

```bash
numpy
pandas
scikit-learn
matplotlib
```

You can install these dependencies using pip:

```bash
pip install numpy pandas scikit-learn matplotlib
```

## Dataset

The project uses the Wine Quality dataset (red wine). The dataset should be named `winequality-red.csv` and should be placed in the same directory as the script. The dataset contains the following features:

- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol
- Quality (target variable)

## Usage

1. Clone the repository:

```bash
git clone <your-repository-url>
cd <repository-name>
```

2. Place the `winequality-red.csv` file in the project directory

3. Run the script:

```bash
python wine.py
```

## Project Structure

- `wine.py`: Main script containing the implementation
- `winequality-red.csv`: Dataset file (not included in repository)

## Implementation Details

The project implements the following key functions:

- `import_data()`: Loads and displays basic information about the dataset
- `split_dataset()`: Splits the data into training and testing sets
- `train_decision_tree`: Trains the model using Gini index as the splitting criterion
- `prediction()`: Makes predictions on test data
- `calculate_accuracy()`: Calculates and displays model performance metrics
- `plot_decision_tree()`: Visualizes the decision tree

## Model Performance

The model is evaluated using:

- Confusion Matrix
- Accuracy Score
- Classification Report

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- The Wine Quality dataset
- scikit-learn library
- matplotlib for visualization
