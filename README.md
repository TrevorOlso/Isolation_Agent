Isolation Game Agent (C++) - Center Seeking & Opponent Blocking
This repository contains a C++ implementation of an agent that plays the game of Isolation. The agent employs a strategy that combines center-seeking behavior with opponent blocking to maximize its chances of winning.

Game Description: Isolation
Isolation is a two-player, zero-sum board game played on a rectangular grid. Players take turns moving a single piece, and each player's goal is to maneuver their piece so that the opponent has no legal moves.  With each move, the player eliminates the cell that their piece previously occupied, restricting future movement.

Agent Strategy: Center Seeking & Opponent Blocking
This agent uses a heuristic strategy with two main components:

Center Seeking: In the early game, the agent prioritizes moving its piece towards the center of the board. The center of the board generally offers the greatest number of available moves, increasing the agent's long-term mobility.

Opponent Blocking: As the game progresses, the agent shifts its focus to limiting the opponent's available moves. It evaluates potential moves based on how much they restrict the opponent's future options.  The agent attempts to move to locations that significantly reduce the opponent's legal move count in the following turn.

The agent calculates a score for each possible move based on a combination of these two factors:

A higher score is awarded for moves closer to the center in the early game.

A higher score is awarded for moves that leave the opponent with fewer legal moves.

Implementation Details
Language: C++

Data Structures: The game board is represented using a 2D vector.

Move Generation: The agent efficiently generates all legal moves for both itself and the opponent.

Heuristic Evaluation: The core of the agent is the heuristic function that scores potential moves. This function balances the center-seeking and opponent-blocking strategies.

Search: The agent uses a limited-depth search (likely minimax or a variant) to evaluate moves a few turns ahead.  The depth of the search can be adjusted to balance performance and computational cost.

Authors:  TrevorOlso, Tmdirito
