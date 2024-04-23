# Probabilistic-Algorithms

Contains probabilistic algorithms and experiments code writen by Husain Azaqy

## {Experiment 1}:

    Description:

    A game is played, where in each game there are a set number of rounds.
    Each round ,the player tosses a coin with a pre-set success rate until the coin gives a failure. Proceeding to the next round.
    Each toss costs the player a fixed amount of money.
    When a toss fails, the player gets 2^(successful tosses) money back

    Goal of the experiment:
        To find for varying toss costs, what rate of success is considered "balance point" for said toss cost.
        Meaning for what success rate are we EXPECTED to not lose or gain any money in all of the rounds combined (for large numbers of rounds)
    The algorithm:
        we check for all success rates Si = granularity*i,1 <= i < 1/granularity the average outcome for many simulations of many rounds games.
        we take the Si resulting in the closest outcome to zero in absolute value.

//-----------------------------------------------------------------------------

## {Experiment 2}:

    Description:

    This experiment tests the Monte Carlo Method for approximating \pi , the area of a triangle, and intheory the area of any shape that given a 2d point we can decide whether the point is inside the shape or not. given a (0,0) centerd square that contains said shape.

    Goals of the experiment:
        - implementing to approximate \pi
        - implementing for a triangle
        - implementing for a more general shape
    The algorithm:
        - Given a (0,0) centerd square that contains said shape, we uniformly randomize n points inside the box.
        - We count how many of these points are inside our shape, denote k.
        - We compute the ration k/n
        - The estimated area is square_area*(k/n)
