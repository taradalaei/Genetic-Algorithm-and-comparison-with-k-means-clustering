# Genetic Algorithm for Feature Selection in Clustering

This project demonstrates the use of a genetic algorithm for feature selection in clustering. The genetic algorithm aims to improve the clustering performance by selecting an optimal subset of features from the dataset.

## Project Overview

The project utilizes the Dry Bean Dataset for clustering purposes. It applies a genetic algorithm to select the best subset of features to maximize the clustering performance, which is evaluated using silhouette scores. The results are then compared with the baseline K-means clustering using all features.

## Installation

To run this project, you need to have Python installed along with the following libraries:
- pandas
- numpy
- matplotlib
- scikit-learn

You can install the required libraries using the following command:
```bash
pip install pandas numpy matplotlib scikit-learn
```

## Usage

1. **Load the Dataset**: Ensure that the Dry Bean Dataset is available in the same directory as the script with the filename `Dry_Bean_Dataset.xlsx`.

2. **Run the Script**: Execute the script to perform clustering with both the genetic algorithm selected features and the baseline K-means clustering.

## Project Structure

- `AI_project6_40013015.py`: This is the main script file that contains all the code for loading the dataset, processing it, applying the genetic algorithm, and performing K-means clustering.

## Code Description

1. **Load the Dataset**: The dataset is loaded from an Excel file and checked for missing values, which are then removed.

2. **Label Encoding**: The categorical target variable `Class` is encoded into numerical values.

3. **Outlier Removal**: Outliers are removed using the Interquartile Range (IQR) method.

4. **Feature Selection using Genetic Algorithm**:
    - Initialize a population of chromosomes (feature subsets).
    - Evaluate the fitness of each chromosome using silhouette scores from K-means clustering.
    - Perform selection, crossover, and mutation to create a new generation of chromosomes.
    - Repeat the process for a specified number of generations to find the best chromosome.

5. **Clustering and Evaluation**:
    - Perform K-means clustering on the full feature set and the selected feature set from the genetic algorithm.
    - Evaluate the clustering performance using silhouette scores and Davies-Bouldin Index.
    - Visualize the clustering results.

## Results

The script outputs the best chromosome (feature subset) found by the genetic algorithm along with its fitness score. It also provides silhouette scores and Davies-Bouldin Index for both the baseline K-means clustering and the genetic algorithm-based clustering.

## Visualization

The script generates scatter plots to visualize the clustering results for both the baseline K-means clustering and the genetic algorithm-based clustering.

## Example Output

```
Best Chromosome: [1 1 0 0 1 0 1 1 0 0 1 1 1 0 0 0]
Best Fitness: 0.5456758038287725

Silhouette Score for K-means: 0.492345
Davies-Bouldin Index for K-means: 0.325456

Silhouette Score for GA: 0.567890
Davies-Bouldin Index for GA: 0.289123
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.
