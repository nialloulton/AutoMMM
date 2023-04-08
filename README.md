# AutoMediaAI: An Open Source Experimental Automodeller for Marketing Mix Models

## _by [1749.io](https://1749.io)_

## Overview

AutoMediaAI is an experimental open source library designed to automate the process of building base marketing mix models and feature selection methods using Ridge Regression and the GPT-4 AI model. By leveraging AI, AutoMediaAI assists in variable selection, multicollinearity management, and model performance improvement. Using the automodeller can be useful in identifying potential predictors to use in your Marketing-Mix Model. The library is built on top of widely used libraries like NumPy, pandas, and scikit-learn, and aims to streamline the process of creating high-quality marketing mix models.

Please note that this library is experimental and may produce unexpected results. Users are advised to use this library with caution and always double-check the outcomes to ensure they align with domain expertise and expectations.

**Disclaimer:** AutoMediaAI uses OpenAI's GPT-4 API for assisting with variable selection and model improvement. The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

## Usage

**Import the required libraries and dependencies**
Import necessary libraries such as numpy, pandas, sklearn, statsmodels, matplotlib, and openai.
   
**Load your dataset**
Load your dataset as a pandas DataFrame, and make sure it contains the dependent variable and all potential independent variables.

**Select the initial independent variables**
independent_vars = ['media1', 'media2']

**Set the dependent variable**
dependent_var = 'sales'

**Set the initial alpha value for Ridge Regression**
initial_alpha = 1.0

**Set the minimum and maximum number of iterations**
min_iterations = 1
max_iterations = 10

**Create an instance of the AutoModeller class**
automodeller = AutoModeller(data, dependent_var, independent_vars, initial_alpha, min_iterations, max_iterations)

**Run the automodeller**
automodeller.run()

**Plot the variable test counts**
automodeller.plot_variable_test_counts().



## Features
- Automatically selects variables for marketing mix models based on AIC, T-stats, and coefficients.
- Assists in handling multicollinearity and model performance improvement.
- Leverages AI to suggest new variables and Ridge Regression alpha parameter for better model performance.
- Allows customization of initial variables, initial alpha, and the number of iterations.
- Provides insights into variable usage, where variables used more than average in the candidate models are identified as key variables
- Returns the average alpha parameter used in the candidate models to help mitigate the issues of multicollinearity.
- Once you have your final variables and alpha, use tools such as [LinReg](https://linreg.tools), to further explore the relationships


## Limitations and Risks
- As an experimental library, AutoMediaAI may produce unexpected or suboptimal results.
- There is a risk of misuse through looping a self-prompt, which may lead to unintended consequences. Users should exercise caution and be aware of the risks involved.
- The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

## Contributing
AutoMediaAI welcomes contributions from the community. If you would like to contribute, please fork the repository, make your changes, and submit a pull request. For any questions or issues, feel free to open an issue on the repository's issue tracker.

## License
AutoMediaAI is released under the MIT License.

