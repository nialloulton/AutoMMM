# Experience the Future of Marketing Mix Modeling with AutoMMM

## _by [1749.io](https://1749.io)_

---

### 🛠️ **Partner Tools**
- [PyMC-Marketing Documentation](https://www.pymc-marketing.io/en/stable/)
- [PyMC-Marketing on GitHub](https://github.com/pymc-labs/pymc-marketing)
- [Reach Curve](https://www.reachcurve.com)
- [Perceptual Map](https://www.perceptual-map.com/)
- [Linear Regression](https://www.linreg.tools/)

---

### 📚 **Marketing Analytics Resources**
- [Bayesian Marketing Mix Modeling](https://1749.io/resource-center/f/a-comprehensive-guide-to-bayesian-marketing-mix-modeling)
- [Time-Varying Modeling](https://1749.io/resource-center/f/marketing-mix-modeling-in-a-modern-era-time-varying-parameters)
- [Long-Term ROAS](https://1749.io/resource-center/f/measuring-marketing-effectiveness-over-the-long-term)

---

## Overview

AutoMMM is a groundbreaking tool that revolutionizes the process of building and optimizing Marketing Mix Models. Utilizing advanced Ridge Regression and the GPT-4 AI model, AutoMMM offers a seamless and automated approach to feature selection and model creation.

## Take Control of Your Marketing Efforts

AutoMMM empowers marketers by identifying potential predictors in your Marketing-Mix Model. By leveraging the power of AI and domain expertise, it assists with variable selection, multicollinearity management, and model performance improvement, enabling you to optimize your marketing investments for maximum return.

## Innovative Features for Enhanced Performance

AutoMMM combines domain expertise with statistical criteria like AIC, T-stats, and coefficients sign for an effective automated variable selection process. It uses AI to suggest new variables and Ridge Regression alpha parameter, enhancing your model performance.

## Customize and Understand Your Model

With AutoMMM, you have the flexibility to customize initial variables, initial alpha, and the number of iterations. It provides insights into variable usage, identifying key variables used more than average in the candidate models. Plus, it returns the average alpha parameter used in the models to help manage multicollinearity.

## Explore Further with Holiday Extraction and Bayesian VAR

AutoMMM's robust features include holiday extraction and variable creation, processing into any weekly week format, and Bayesian VAR with an exogenous component. It also provides an Impulse Response Function and plotting for the Bayesian VAR class.

Experience the power of AI in Marketing Mix Modeling with AutoMMM, and harness the power of data to drive your marketing success

Please note that this library is experimental and may produce unexpected results. Users are advised to use this library with caution and always double-check the outcomes to ensure they align with domain expertise and expectations.

**Disclaimer** : AutoMMM, a state-of-the-art application leveraging OpenAI's GPT-4 API, is provided "as-is" without any warranties, expressed or implied. By using this software, you agree to assume all risks associated with its use.

The developers, contributors, and 1749.io disclaim any responsibility or liability for losses, damages, or other consequences that may arise due to the use of AutoMMM. You, as a user, bear sole responsibility for decisions and actions based on the information provided by this software.

Be aware that using the GPT-4 language model may result in substantial expenses due to token usage. By employing AutoMMM, you acknowledge your responsibility for monitoring and managing your own token usage and the associated costs. We strongly recommend regularly reviewing your OpenAI API usage and establishing necessary limits or alerts to prevent unexpected charges.

AutoMMM, designed for assisting in model enhancement and variable selection, may generate content or take actions that deviate from best practices or user expectations. It is your responsibility to ensure that any decisions or actions made based on this software's output are appropriate and in line with your requirements or guidelines. The developers and contributors of this project shall not be held responsible for any consequences arising from the use of this software.

By using AutoMMM, you agree to indemnify, defend, and hold the developers, contributors, and any affiliated parties harmless from and against any and all claims, damages, losses, liabilities, costs, and expenses (including reasonable attorneys' fees) resulting from your use of this software or any violation of these terms

## Installation

**pip install autoMMM**: 
[autoMMM 0.1.5](https://pypi.org/project/autoMMM/0.1.5/)


## Usage
- For Automodeller see automodeller demo
- For Holidays Extraction and Processing see Autoholidays demo


## Features
- Automated variable selection combining domain expertise and statistical criterea such as AIC, T-stats, and coefficients sign.
- Assists in handling multicollinearity and model performance improvement.
- Leverages AI to suggest new variables and Ridge Regression alpha parameter for better model performance.
- Allows customization of initial variables, initial alpha, and the number of iterations.
- Provides insights into variable usage, where variables used more than average in the candidate models are identified as key variables
- Returns the average alpha parameter used in the candidate models to help mitigate the issues of multicollinearity.
- Once you have your final variables and alpha, use tools such as [LinReg](https://linreg.tools), to further explore the relationships
- Holidays exctraction and variable creation, processing into any weekly week format
- Bayesian VAR with exogenous component
- Impulse Response Function and plotting for Bayesian VAR class



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

## Holidays Supported
| Country                     | Code | Subdivisions Available                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| American Samoa              | AS   | Can also be loaded as country US, subdivision AS                                                                                                                                                                                                                                                                                                       |
| Andorra                     | AD   | Parishes: 02, 03, 04, 05, 06, 07, 08                                                                                                                                                                                                                                                                                                                   |
| Australia                   | AU   | States and territories: ACT (default), NSW, NT, QLD, SA, TAS, VIC, WA                                                                                                                                                                                                                                                                                 |
| Austria                     | AT   | States: 1, 2, 3, 4, 5, 6, 7, 8, 9 (default)                                                                                                                                                                                                                                                                                                            |
| Bolivia                     | BO   | Departments: B, C, H, L, N, O, P, S, T                                                                                                                                                                                                                                                                                                                 |
| Bosnia and Herzegovina      | BA   | Departments: BD, FBiH, RS                                                                                                                                                                                                                                                                                                                              |
| Brazil                      | BR   | States: AC, AL, AM, AP, BA, CE, DF, ES, GO, MA, MG, MS, MT, PA, PB, PE, PI, PR, RJ, RN, RO, RR, RS, SC, SE, SP, TO                                                                                                                                                                                                                                   |
| Canada                      | CA   | Provinces and territories: AB, BC, MB, NB, NL, NS, NT, NU, ON (default), PE, QC, SK, YT                                                                                                                                                                                                                                                              |
| Chile                       | CL   | Regions: AI, AN, AP, AR, AT, BI, CO, LI, LL, LR, MA, ML, NB, RM, TA, VS                                                                                                                                                                                                                                                                               |
| France                      | FR   | Départements: Alsace-Moselle, Guadeloupe, Guyane, La Réunion, Martinique, Mayotte, Métropole, Nouvelle-Calédonie, Polynésie Française, Saint-Barthélémy, Saint-Martin, Wallis-et-Futuna                                                                                                                                                              |
| Germany                     | DE   | States: BB, BE, BW, BY, BYP, HB, HE, HH, MV, NI, NW, RP, SH, SL, SN, ST, TH                                                                                                                                                                                                                                                                            |
| Guam                        | GU   | Can also be loaded as country US, subdivision GU                                                                                                                                                                                                                                                                                                       |
| India                       | IN   | States: AN, AP, AR, AS, BR, CG, CH, DD, DH, DL, GA, GJ, HP, HR, JH, JK, KA, KL, LA, LD, MH, ML, MN, MP, MZ, NL, OR, PB, PY, RJ, SK, TN, TR, TS, UK, UP, WB                                                                                                                                                                                           |
| Italy                       | IT   | Provinces: AG, AL, AN, AO, AP, AQ, AR, AT, AV, BA, BG, BI, BL, BN, BO, BR, BS, BT, BZ, CA, CB, CE, CH, CL, CN, CO, CR, CS, CT, CZ, EN, FC, FE, FG, FI, FM, FR, GE, GO, GR, IM, IS, KR, LC, LE, LI, LO, LT, LU, MB, MC, ME, MI, MN, MO, MS, MT, NA, NO, NU, OR, PA, PC, PD, PE, PG, PI, PN, PO, PR, PT, PU
| Puerto Rico                 | PR   | Can also be loaded as country US, subdivision PR                                                                                                                                                                                                                                                                                                     |
| Nicaragua                   | NI   | Departments: AN, AS, BO, CA, CI, CO, ES, GR, JI, LE, MD, MN (default), MS, MT, NS, RI, SJ                                                                                                                                                                                                                                                            |
| Portugal                    | PT   | Districts: 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 14, 15, 16, 17, 18, 20, 30, Ext; Use subdiv=’Ext’ to include holidays most people have off                                                                                                                                                                                            |
| Spain                       | ES   | Autonomous communities: AN, AR, AS, CB, CE, CL, CM, CN, CT, EX, GA, IB, MC, MD, ML, NC, PV, RI, VC                                                                                                                                                                                                                                                   |
| United Kingdom              | GB   | Subdivisions: England, Northern Ireland, Scotland, UK (default), Wales; For Isle of Man use country code IM                                                                                                                                                                                                                                          |
| United States of America     | US   | States and territories: AL, AK, AS, AZ, AR, CA, CO, CT, DE, DC, FL, GA, GU, HI, ID, IL, IN, IA, KS, KY, LA, ME, MD, MH, MA, MI, FM, MN, MS, MO, MT, NE, NV, NH, NJ, NM, NY, NC, ND, MP, OH, OK, OR, PW, PA, PR, RI, SC, SD, TN, TX, UM, UT, VT, VA, VI, WA, WV, WI, WY                     |
| United States Minor Outlying Islands | UM   | Can also be loaded as country US, subdivision UM                                                                                                                                                                                                                                                                                                     |
| Virgin Islands (U.S.)       | VI   | Can also be loaded as country US, subdivision VI                                                                                                                                                                                                                                                                                         

## Limitations and Risks
- As an experimental library, AutoMMM.ai may produce unexpected or suboptimal results.
- There is a risk of misuse through looping a self-prompt, which may lead to unintended consequences. Users should exercise caution and be aware of the risks involved.
- The open source software and 1749.io are not responsible for any misuse of the OpenAI API or any consequences resulting from looping a self-prompt.

# Contributing to AutoMMM

As an experimental library, contributions and improvements are thoroughly encouraged. We appreciate your interest in making this library better for everyone. Before you start working on your contribution, please familiarize yourself with the following guidelines and processes.

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
AutoMMM is released under the MIT License.

