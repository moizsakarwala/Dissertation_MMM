# Marketing Mix Modeling (MMM) with Reinforcement Learning

## Project Overview
This repository contains the code and resources used for my master's dissertation, which focuses on the integration of advanced data science techniques—such as Random Forest (RF) and Reinforcement Learning (RL)—to enhance traditional Marketing Mix Modeling (MMM). The goal of this project is to develop a dynamic budget allocation framework that optimizes marketing spend across multiple channels using machine learning methods, particularly Random Forest and Proximal Policy Optimization (PPO) for reinforcement learning.

The models are tested on a custom dataset that simulates marketing activities for a company selling handsets, with historical data spanning multiple years. The project aims to demonstrate the superiority of advanced machine learning models in improving revenue predictions and providing real-time, adaptive budget allocation recommendations.

## Project Components
This repository contains the following key components:

### 1. **`my_model_mmm.txt`**
- **Description**: This script implements traditional MMM techniques using machine learning models such as Linear Regression, Random Forest, and Gaussian Processes.
- **Purpose**: To evaluate the effectiveness of different models in predicting revenue based on various marketing channels.
- **Main Models**: 
    - Linear Regression (baseline model)
    - Random Forest (core machine learning model)
    - Gaussian Process (alternative advanced model)

### 2. **`rl_model_for_budget_allocation.txt`**
- **Description**: This script implements Reinforcement Learning using Proximal Policy Optimization (PPO) for dynamic marketing budget allocation across different marketing channels.
- **Purpose**: To simulate real-time decision-making in marketing budget allocation based on market conditions, seasonality, and other external factors.
- **Main Algorithms**: 
    - PPO (Proximal Policy Optimization)
    - Custom environment for RL using Gym
    - Budget allocation and revenue prediction using RL

### 3. **Dataset**
- **Description**: The dataset used for this project was sourced from publicly available MMM datasets, enriched with additional features like temperature, holiday indicators, and return on investment (ROI) for each marketing channel.
- **Features**: 
    - Marketing channels such as SMS, Newspaper Ads, Radio, TV, PPC, and more.
    - Temporal features like Day, Month, Year, and Season.
    - External features like Temperature and Is_Holiday.
- **Time Period**: The data spans from 2010 to 2016, with a total of 2,211 rows and 37 columns after data enrichment.

## Setup and Installation
1. **Clone the repository**: 
    ```bash
    git clone https://github.com/moizsakarwala/Dissertation_MMM.git
    cd Dissertation_MMM
    ```

2. **Install dependencies**:
    - You can use a virtual environment to install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. **Running the Models**:
    - **For Traditional MMM models**: 
        Run the `my_model_mmm.txt` script to train Linear Regression, Random Forest, and Gaussian Process models.
    - **For Reinforcement Learning Model**: 
        Run the `rl_model_for_budget_allocation.txt` script to implement the PPO algorithm for budget allocation.

4. **Dataset**: 
    - The dataset should be in `.csv` format and follow the structure defined in the project. Place your dataset in the appropriate folder and modify the path in the script if necessary.

## How It Works
1. **Random Forest Model**:
    - Trains a Random Forest model to predict revenue based on various marketing channels and external factors.
    - Outputs the importance of each marketing channel in influencing revenue.
  
2. **Reinforcement Learning Model**:
    - Uses PPO to allocate a marketing budget dynamically across different channels.
    - Simulates various marketing scenarios and adjusts the allocation based on predicted revenue.

3. **Linking RL to RF**:
    - The RL model allocates the marketing budget, which is then fed into the Random Forest model to predict the corresponding revenue.

## Results and Outputs
- The results for each scenario are displayed, showing the budget allocation across marketing channels and the predicted revenue for each scenario. 
- The `rl_model_for_budget_allocation.txt` script outputs the budget allocation and total predicted revenue for each test scenario.

## Project Goals
- **Primary Goal**: To demonstrate that advanced machine learning techniques like Random Forest and Reinforcement Learning can significantly enhance traditional MMM approaches by capturing non-linear relationships and providing real-time, adaptive decision-making.
- **Future Work**: The framework can be extended to real-world data for further validation, and the RL model can be enhanced to incorporate additional features such as customer experience and multi-touch attribution.

## Appendix
Refer to the appendix section in the dissertation for additional charts, dataset snippets, and system configurations used for training the models.

## Citation
If you use this repository in your research or projects, please cite it as follows:
```plaintext
Moiz Sakarwala. "Dissertation on Marketing Mix Modeling Using Machine Learning and Reinforcement Learning." GitHub, 2024, https://github.com/moizsakarwala/Dissertation_MMM.git
```

