# Fantasy Football Team Optimizer

This project utilizes linear regression and linear programming to suggest an optimized fantasy football team. The approach focuses on maximizing long-term performance by leveraging statistical modeling to select players while adhering to budget constraints.

## Features

- **Linear Regression**: A model is trained on important features to predict player scores based on historical data.
- **Linear Programming**: Pyomo is used to optimize player selection with constraints like budget and team composition.
- **Customizable Settings**: Users can adjust the budget and the number of players based on their league's specific rules.
- **Long-term Focus**: This model emphasizes consistent, long-term performance by not considering short-term variables like match difficulty.

## Workflow

1. **Linear Regression**: 
   - The model uses important features of players to learn the parameters for predicting performance.
   - A new column, 'score', is added to the dataset to represent the predicted points for each player.

2. **Linear Programming (Pyomo)**: 
   - The optimization problem is defined with a budget constraint (initially 83.5 million, after subtracting the value of bench players).
   - The program selects 11 players within the budget that maximize the total score.

3. **Customization**:
   - To adjust the number of players or the budget, simply modify the variables `budget` and `num_players` in the code.
   - For example, if you want to add a bench player, increase the number of players to 12 and adjust the budget accordingly.

## Getting Started

1. **Download the Premier League Dataset**: 
   - Get the dataset from Kaggle: [Fantasy Premier League Dataset 2024-2025](https://www.kaggle.com/datasets/meraxes10/fantasy-premier-league-dataset-2024-2025).
   
2. **Upload the Dataset**:
   - Upload the dataset to your Google Colab environment.
   - Copy the path to the file and paste it into the `read_csv()` function in the notebook.

3. **Run the Notebook**:
   - Open the notebook in Google Colab, execute the cells, and the model will optimize and suggest a team.

## Future Improvements

- **Supervised Captaining**: 
   - Develop a strategy to recommend captains based on fixture difficulty and player consistency over a long period.
  
- **Complex Objective Function**:
   - Replace linear regression with a more sophisticated model (e.g., deep learning) to better capture player performance.

- **Transfers**:
   - Introduce a transfer system where players can be swapped based on performance. Prediciting the players next round points based on several variables. Then they could be replaced with better-performing alternatives.
   - Incorporate injury/red card considerations into the model.

- **Simplified Premier League Formula**: 
   - Implement the official scoring formula provided by the Premier League for a simpler approach instead of Machine Learning.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to Kaggle for providing the dataset.
- Special thanks to the open-source community for Pyomo and the libraries used.
