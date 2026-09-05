# Connect Four Algorithms & Performance Optimization

A configurable Connect Four game written in C to explore algorithm design,
game-state evaluation, computer move selection, and performance optimization.

## Overview

This project was developed as part of a C Programming and Data Structures
course. The goal was to implement a functional Connect Four game while
comparing different approaches to game-state evaluation and computer move
selection.

The program supports configurable board sizes and multiple game modes,
including human and computer players. Two different computer strategies were
developed and compared through automated simulations and runtime measurements.

## Features

- Configurable Connect Four board sizes
- Human vs. Human gameplay
- Human vs. Computer gameplay
- Computer vs. Computer simulation
- Multiple computer move-selection algorithms
- Win and block detection
- Directional chain analysis
- Weighted move scoring
- Opponent-threat evaluation
- Automated performance benchmarking
- Runtime and win-rate statistics

## Algorithm Design

### Game-State Evaluation

The initial implementation evaluates the board by searching for winning
conditions throughout the game board.

An optimized approach uses information about the most recent move to limit
the amount of the board that needs to be examined when determining whether
a win has occurred.

This reduced unnecessary board scanning as board size increased.

### Computer Move Selection

The computer player evaluates potential moves using several factors,
including:

- Whether a move immediately wins the game
- Whether a move blocks an opponent's immediate win
- The length and direction of existing piece chains
- The potential value of extending a chain
- Proximity to the center of the board
- Whether a move could create an immediate opportunity for the opponent

During development, improving execution speed alone sometimes resulted in
weaker move selection. Additional threat evaluation and move scoring were
therefore added to balance computational performance with playing strength.

## Performance Testing

The program includes an automated Computer vs. Computer mode that allows
the different implementations to play repeated games against one another.

Execution time for computer turns was measured during these simulations,
allowing the implementations to be compared as board size increased.

Testing showed that optimization had relatively little benefit on small
boards, where the additional decision-making overhead could offset the
runtime savings. The optimized approach became increasingly advantageous
as board size increased.

## What I Learned

This project provided experience with:

- Algorithm design and optimization in C
- Evaluating time-complexity and scalability
- Designing heuristic decision-making logic
- Testing and debugging larger programs
- Measuring program performance
- Comparing computational efficiency with solution quality
- Structuring a program to support multiple implementations of the same
  functionality

One of the most valuable parts of the project was seeing that a faster
algorithm is not necessarily a better algorithm if optimization reduces the
quality of its decisions. Refining the computer player required balancing
runtime performance with effective move selection.

## Technologies

- C
- Command-line / terminal interface
- Runtime performance measurement
- Automated simulation and testing

## Source Code

This project was completed as university coursework. Source code is kept
private to preserve academic integrity and is available upon request for
professional review.
