# BATTLESHIP AI

An AI implementation of the game **Battleship**. This project uses Python and the NumPy library to run simulations of each game using different methods. The results of each method are observed later on for analytical purposes.

So far, I was able to implement two different methods...

1. A simple Bayesian method: First, I generate all possible placements of a ship of length 5 on a 10x10 gameboard (this gives a total of 120 different placements). The list is used to generate a separate probability board based on how many times each space may contain a ship. For each guess, this list of possible placements eliminates certain board configurations based on the outcome each guess, and uses the remaining possible candidates to generate new probabilities.

2. Bayesian search based on ship length: This is part of our "prior" information (Bayesian pun intended). When playing **Battleship**, we may not know where each ship is placed, but we do have knowledge of the length of the ships we are looking for... and this strategy uses it! Instead of guessing anywhere on the board, this strategy guesses in places that will guarantee us to hit a ship of a given length at least once, regardless of placement. This saves us a lot of guesses based on probability alone.
