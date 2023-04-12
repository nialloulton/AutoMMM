# AutoMMM.ai An Experimental Open-source Automodeller for Feature Selection in Marketing Mix Models

## _by [1749.io](https://1749.io)_

## Overview

AutoMMM.ai is an experimental open source library designed to automate the process of building base marketing mix models and feature selection methods using Ridge Regression and the GPT-4 AI model. By leveraging AI, AutoMMM.ai assists in variable selection, multicollinearity management, and model performance improvement. Using the automodeller can be useful in identifying potential predictors to use in your Marketing-Mix Model. The library is built on top of widely used libraries like NumPy, pandas, and scikit-learn, and aims to streamline the process of creating high-quality marketing mix models.

Please note that this library is experimental and may produce unexpected results. Users are advised to use this library with caution and always double-check the outcomes to ensure they align with domain expertise and expectations.

**Disclaimer** : AutoMMM.ai, a state-of-the-art application leveraging OpenAI's GPT-4 API, is provided "as-is" without any warranties, expressed or implied. By using this software, you agree to assume all risks associated with its use.

The developers, contributors, and 1749.io disclaim any responsibility or liability for losses, damages, or other consequences that may arise due to the use of AutoMMM.ai. You, as a user, bear sole responsibility for decisions and actions based on the information provided by this software.

Be aware that using the GPT-4 language model may result in substantial expenses due to token usage. By employing AutoMMM.ai, you acknowledge your responsibility for monitoring and managing your own token usage and the associated costs. We strongly recommend regularly reviewing your OpenAI API usage and establishing necessary limits or alerts to prevent unexpected charges.

AutoMMM.ai, designed for assisting in model enhancement and variable selection, may generate content or take actions that deviate from best practices or user expectations. It is your responsibility to ensure that any decisions or actions made based on this software's output are appropriate and in line with your requirements or guidelines. The developers and contributors of this project shall not be held responsible for any consequences arising from the use of this software.

By using AutoMMM.ai, you agree to indemnify, defend, and hold the developers, contributors, and any affiliated parties harmless from and against any and all claims, damages, losses, liabilities, costs, and expenses (including reasonable attorneys' fees) resulting from your use of this software or any violation of these terms

## Usage

**Import the required libraries and dependencies** :
Import necessary libraries such as numpy, pandas, sklearn, statsmodels, matplotlib, and openai.

**Specify your OPENAI Key (Do not publish your presonal Key anywhere)** :
openai.api_key = "your openai key here"

   
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
- As an experimental library, AutoMMM.ai may produce unexpected or suboptimal results.
- There is a risk of misuse through looping a self-prompt, which may lead to unintended consequences. Users should exercise caution and be aware of the risks involved.
- The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

# Contributing to AutoMedia.ai

Thank you for considering contributing to AutoMMM.ai, We appreciate your interest in making this library better for everyone. Before you start working on your contribution, please familiarize yourself with the following guidelines and processes.

## Table of Contents

1. [Getting Started](#getting-started)
2. [Reporting Bugs](#reporting-bugs)
3. [Feature Requests](#feature-requests)
4. [Contributing Code](#contributing-code)
5. [Pull Request Process](#pull-request-process)
6. [Code Review](#code-review)



## Getting Started

To start contributing to AutoMMM.ai, follow these steps:

1. Fork the repository on GitHub.
2. Clone your fork to your local machine.
3. Create a new branch for your changes.
4. Make your changes and commit them.
5. Push your changes to your fork.
6. Create a pull request to the main repository.

## Reporting Bugs

If you encounter a bug or issue with AutoMMM.ai, please report it by opening an issue on the repository's issue tracker. Make sure to include the following information in your report:

1. A clear description of the issue.
2. Steps to reproduce the problem.
3. The expected and actual results.
4. Any relevant error messages or logs.
5. Your system configuration (operating system, Python version, etc.).

## Feature Requests

If you have an idea for a new feature or improvement, please open an issue on the repository's issue tracker. Be sure to include:

1. A clear description of the feature or improvement.
2. A rationale for why it should be added to AutoMMM.ai.
3. Examples of how the feature would be used.

## Contributing Code

When contributing code, please adhere to the following guidelines:

1. Write clear, concise, and well-structured code.
2. Add docstrings and comments to your code, explaining its purpose and functionality.
3. Add tests for your code, ensuring it is reliable and thoroughly tested.
4. Update any relevant documentation.

## Pull Request Process

1. Ensure your changes are on a separate branch from your fork.
2. Create a pull request to the main repository, targeting the `develop` branch.
3. Provide a clear description of the changes in the pull request, including any related issues or feature requests.
4. Request a review from one or more maintainers.
5. Address any feedback or requested changes from the review.
6. Once your pull request has been approved, it will be merged into the `develop` branch.

## Code Review

1. Code reviews are an essential part of the contribution process. They help ensure the quality and maintainability of the codebase.
2. Be respectful and constructive when providing feedback on a pull request.
3. Remember that everyone has different levels of experience and knowledge. Be patient and understanding when reviewing or receiving feedback on your contributions.
4. If you disagree with a reviewer's feedback, discuss it respectfully and try to find a consensus.
5. Once all feedback has been addressed and the maintainers are satisfied with the changes, the pull request will be merged.

Thank you for your interest in contributing to AutoMMM.ai, and we look forward to collaborating with you!


## License
AutoMMM.ai is released under the MIT License.

