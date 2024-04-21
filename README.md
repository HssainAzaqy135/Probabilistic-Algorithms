# Probabilistic-Algorithms

Contains probabilistic algorithms and experiments code

## {Experiment 1}:

    A game is played, where in each game there are a set number of rounds.
    Each round the player tosses a coin with a pre-set succes rate until the coin gives a failure. Proceeding to the next round.
    Each toss costs the player a fixed amount of money.
    When a toss fails, the player gets 2^(successful tosses) money back

    Goal of the experiment:
        To find for varying toss costs, what rate of success is considered "balance point" for said toss cost.
        Meaning for what success rate are we EXPECTED to not lose or gain any money in all of the rounds combined (for large numbers of rounds)
    The algorithm:
        we check for all success rates Si = granularity*i,1 <= i < 1/granularity the average outcome for many simulations of many rounds games.
        we take the Si resulting in the closest outcome to zero in absolute value.
