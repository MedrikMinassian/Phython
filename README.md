# Phython
Simulate Coin Flip
The algorithm will predict a coin flip in the air.

import random

def simulate_coin_flip(num_trials):
    correct_predictions = 0

    for _ in range(num_trials):
        # Simulate a coin flip (0 for heads, 1 for tails)
        actual_result = random.choice([0, 1])

        # Attempt to predict the result (0 for heads, 1 for tails)
        predicted_result = random.choice([0, 1])

        # Check if the prediction is correct
        if predicted_result == actual_result:
            correct_predictions += 1

    # Calculate the average accuracy
    average_accuracy = correct_predictions / num_trials
    return average_accuracy

# Set the number of trials for the simulation
num_trials = 1000

# Run the simulation
average_accuracy = simulate_coin_flip(num_trials)

# Print the results
print(f"Number of trials: {num_trials}")
print(f"Average accuracy: {average_accuracy * 100:.2f}%")
