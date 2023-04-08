# AutoMediaAI: An Open Source Experimental Automodeller for Feature Selection in Marketing Mix Models

## _by [1749.io](https://1749.io)_

## Overview

AutoMediaAI is an experimental open source library designed to automate the process of building base marketing mix models and feature selection methods using Ridge Regression and the GPT-4 AI model. By leveraging AI, AutoMediaAI assists in variable selection, multicollinearity management, and model performance improvement. Using the automodeller can be useful in identifying potential predictors to use in your Marketing-Mix Model. The library is built on top of widely used libraries like NumPy, pandas, and scikit-learn, and aims to streamline the process of creating high-quality marketing mix models.

Please note that this library is experimental and may produce unexpected results. Users are advised to use this library with caution and always double-check the outcomes to ensure they align with domain expertise and expectations.

**Disclaimer:** AutoMediaAI uses OpenAI's GPT-4 API for assisting with variable selection and model improvement. The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

## Usage

**Import the required libraries and dependencies** :
Import necessary libraries such as numpy, pandas, sklearn, statsmodels, matplotlib, and openai.
   
**Load your dataset** :
Load your dataset as a pandas DataFrame, and make sure it contains the dependent variable and all potential independent variables.

**Select the initial independent variables** :
independent_vars = ['media1', 'media2']

**Set the dependent variable** :
dependent_var = 'sales'

**Set the initial alpha value for Ridge Regression** :
initial_alpha = 1.0

**Set the minimum and maximum number of iterations** :
min_iterations = 1
max_iterations = 10

**Create an instance of the AutoModeller class** :
automodeller = AutoModeller(data, dependent_var, independent_vars, initial_alpha, min_iterations, max_iterations)

**Run the automodeller** :
automodeller.run()

**Plot the variable test counts** :
automodeller.plot_variable_test_counts().



## Features
- Automated variable selection combining domain expertise and statistical criterea such as AIC, T-stats, and coefficients sign.
- Assists in handling multicollinearity and model performance improvement.
- Leverages AI to suggest new variables and Ridge Regression alpha parameter for better model performance.
- Allows customization of initial variables, initial alpha, and the number of iterations.
- Provides insights into variable usage, where variables used more than average in the candidate models are identified as key variables
- Returns the average alpha parameter used in the candidate models to help mitigate the issues of multicollinearity.
- Once you have your final variables and alpha, use tools such as [LinReg](https://linreg.tools), to further explore the relationships

## Detailed Description
The automodeller method in this code is an experimental approach to model selection and improvement, particularly for marketing mix models. It uses a combination of domain expertise and a language model (GPT) to iteratively improve the model based on various statistical metrics like AIC, R-squared, T-stats, and more.

Here's a high-level explanation of how the automodeller works:

- The method starts by fitting an initial Ridge Regression model using the given dataset, target variable, and the alpha parameter.
- It calculates various statistical metrics like AIC, R-squared, T-stats, VIF, etc., which are crucial for model evaluation and variable selection.
- A prompt is constructed using these statistical metrics to ask the language model for advice on improving the model. This prompt includes a detailed summary of the current model, its performance, and its variables. It also asks the language model to consider the practical implications of variable selection and the importance of domain knowledge.
- The language model (GPT) processes the prompt and responds with suggestions for new variables to consider and, if appropriate, a new alpha parameter for Ridge Regression.
- The automodeller incorporates the language model's suggestions, updates the variables and alpha parameter, and fits a new Ridge Regression model.
- This iterative process continues until the model converges to a satisfactory solution based on both statistical and practical considerations, or until the maximum number of iterations is reached.
- Throughout this process, the automodeller ensures that it does not overfit the model or select variables that do not make sense in the context of a marketing mix model. The goal is to find a model with the best balance of performance (highest R-squared and lowest AIC) and practical relevance, considering the impact of media channels, price, distribution, and other relevant factors.

## Limitations and Risks
- As an experimental library, AutoMediaAI may produce unexpected or suboptimal results.
- There is a risk of misuse through looping a self-prompt, which may lead to unintended consequences. Users should exercise caution and be aware of the risks involved.
- The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

## Contributing
AutoMediaAI welcomes contributions from the community. If you would like to contribute, please fork the repository, make your changes, and submit a pull request. For any questions or issues, feel free to open an issue on the repository's issue tracker.

## License
AutoMediaAI is released under the MIT License.

