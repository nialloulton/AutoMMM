# AutoMediaAI: An Open Source Experimental Automodeller for Marketing Mix Models

_by [1749.io](https://1749.io)_

## Overview

AutoMediaAI is an experimental open source library designed to automate the process of building marketing mix models using Ridge Regression and the GPT-4 AI model. By leveraging AI, AutoMediaAI assists in variable selection, multicollinearity management, and model performance improvement. The library is built on top of widely used libraries like NumPy, pandas, and scikit-learn, and aims to streamline the process of creating high-quality marketing mix models.

Please note that this library is experimental and may produce unexpected results. Users are advised to use this library with caution and always double-check the outcomes to ensure they align with domain expertise and expectations.

**Disclaimer:** AutoMediaAI uses OpenAI's GPT-4 API for assisting with variable selection and model improvement. The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

## Usage

1. **Import the required libraries and dependencies**
   Import necessary libraries such as numpy, pandas, sklearn, statsmodels, matplotlib, and openai.

2. **Load your dataset**
   Load your dataset as a pandas DataFrame, and make sure it contains the dependent variable and all potential independent variables.

3. **Initialize the AutoModeller class**
   Create an instance of the AutoModeller class by providing the required arguments, such as data, dependent_var, initial_vars, initial_alpha, min_iterations, and max_iterations.

4. **Run the AutoModeller**
   Call the run() method on the instance of the AutoModeller class to start the process of automatic model selection and optimization.

5. **Interpret the results**
   After the run() method is completed, you can access the attributes of the AutoModeller instance, such as best_model_stats, best_r_squared, and best_aic to understand the performance of the final model.

6. **Plot the results (optional)**
   You can call the plot_variable_test_counts() method on the AutoModeller instance to visualize the test counts for each variable.


## Features
- Automatically selects variables for marketing mix models based on AIC, T-stats, and coefficients.
- Assists in handling multicollinearity and model performance improvement.
- Leverages AI to suggest new variables and Ridge Regression alpha parameter for better model performance.
- Allows customization of initial variables, initial alpha, and the number of iterations.
- Provides insights into variable usage and test counts.

## Limitations and Risks
- As an experimental library, AutoMediaAI may produce unexpected or suboptimal results.
- There is a risk of misuse through looping a self-prompt, which may lead to unintended consequences. Users should exercise caution and be aware of the risks involved.
- The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

## Contributing
AutoMediaAI welcomes contributions from the community. If you would like to contribute, please fork the repository, make your changes, and submit a pull request. For any questions or issues, feel free to open an issue on the repository's issue tracker.

## License
AutoMediaAI is released under the MIT License.

