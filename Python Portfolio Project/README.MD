# US Medical Insurance Costs Analysis

## Project Overview
This project analyzes a dataset containing information about US medical insurance charges.
It provides insights into the relationships between various factors such as age, BMI, smoking habits, and insurance charges.
The analysis is performed using Python and includes a variety of functions to extract meaningful statistics and trends from the data.

## Dataset Description
The dataset contains the following columns:
- **Age**: The age of the insurance policyholder.
- **Sex**: Gender of the policyholder (male/female).
- **BMI**: Body Mass Index, a measure of body fat based on height and weight.
- **Children**: Number of children/dependents covered by the insurance policy.
- **Smoker**: Smoking status of the policyholder (yes/no).
- **Region**: Geographic region of the policyholder in the US (northeast, southeast, southwest, northwest).
- **Charges**: The insurance charges billed to the policyholder.

### Note:
The dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance)
and is licensed under the [Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/1-0/).
A copy of the dataset is included in the `data/` folder of this repository for convenience.

## Features and Functionality
The project includes the following key functionalities:

### 1. **Average Calculations**
- **Average Insurance Charge**: Calculates the average insurance charge across all individuals.
- **Average BMI by Region**: Computes the average BMI for each geographic region.
- **Average Insurance Charges by Gender and Number of Children**: Analyzes how gender and the number of children affect insurance charges.
- **Average Age and Average Age by Number of Children**: Calculates the overall average age and groups it by the number of children.

### 2. **Categorical Comparisons**
- **Charges for Smokers vs. Non-Smokers**: Provides a regional comparison of average charges for smokers and non-smokers.
- **BMI-Smoking Relationship**: Examines the relationship between BMI categories and smoking status.

### 3. **Grouped Data Analysis**
- **Average Insurance Charges and BMI by Age**: Groups data by age ranges and calculates the average insurance charges and BMI for each group.
- **Average Insurance Charges by Number of Children**: Analyzes charges based on the number of children.

### 4. **Highlights**
- **Top 5 Insurance Charges**: Identifies the five highest insurance charges in the dataset.

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/us-medical-insurance-analysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd us-medical-insurance-analysis
   ```
3. Open the notebook in your preferred notebook environment (e.g., Jupyter Notebook, VS Code):
   ```bash
   <notebook_environment> us-medical-insurance-costs.ipynb
   ```

## Usage Examples
- Run individual cells in your notebook to execute specific functions.
- Modify the dataset or parameters in the functions to explore different scenarios.

## Project Structure
```
.
├── data/
│   └── insurance.csv                  # Dataset
├── us-medical-insurance-costs.ipynb  # Main Jupyter Notebook
├── README.md                         # Project README file
├── LICENSE                           # License file for the project
├── ODbL_LICENSE                      # Open Database License file
```

## Future Improvements
- Integrate visualizations to better illustrate data trends.
- Enhance the functionality to include regression models for predicting insurance charges.
- Expand the analysis to consider additional health metrics.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

The dataset is licensed under the [Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/1-0/).
See the [ODbL_LICENSE](ODbL_LICENSE) file for more details.

## Acknowledgments
- The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/mirichoi0218/insurance).
- The project is part of Codecademy's Data and Programming Foundations for AI syllabus: (Portfolio project: U.S Medical Insurance).

---
**Author:** [S19Deen](https://github.com/S19Deen) 

