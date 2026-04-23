# CSP Magnet Assignment

A Java-based Constraint Satisfaction Problem (CSP) solver for the **Magnet puzzle**, implementing advanced backtracking algorithms with heuristic optimization.

## 📋 Overview

This project solves the Magnet puzzle, a combinatorial logic puzzle where magnets must be placed on a grid according to specific constraints. The solver uses the **AIMA (Artificial Intelligence: A Modern Approach)** library to implement constraint satisfaction techniques including backtracking with heuristics for efficient puzzle resolution.

## ✨ Features

- **CSP-based solver**: Leverages constraint satisfaction problem techniques for optimal performance
- **Flexible backtracking**: Implements intelligent backtracking with heuristic guidance
- **Performance tracking**: Measures and reports execution time in milliseconds
- **Scalable solution**: Handles variable grid sizes and constraint complexities
- **Grid constraint validation**: Ensures all magnet placements satisfy row and column constraints

## 🛠️ Technology Stack

- **Language**: Java
- **CSP Library**: AIMA (Artificial Intelligence: A Modern Approach)
- **Build Tool**: Standard Java compilation
- **Paradigm**: Object-oriented programming with constraint solving

## 📁 Project Structure

```
CSP-Magnet-Assignment/
├── Main.java                 # Entry point - handles I/O and solver orchestration
├── csp.solver/              # CSP solver implementation
├── models/                  # Domain models and constraint definitions
├── constraints/             # Constraint classes for puzzle rules
└── README.md               # Project documentation
```

## 🚀 Usage

### Input Format

The program accepts input in the following format:

```
<rows> <columns>
<row_positive_constraints>
<row_negative_constraints>
<column_positive_constraints>
<column_negative_constraints>
<magnet_grid>
```

### Example

```
3 3
1 1 1
1 1 1
1 1 1
1 1 1
1 2 1
0 1 2
2 1 0
```

### Running the Program

```bash
javac Main.java
java ir.magnet.Main < input.txt
```

### Output

The program outputs:
- **Execution Time**: Duration in milliseconds to solve the puzzle
- **Solution Grid**: The valid magnet placement satisfying all constraints

```
Execution Time: 45ms
1 2 1
0 1 2
2 1 0
```

## 🧩 How It Works

### Algorithm Overview

1. **Problem Modeling**: Each cell in the grid is represented as a CSP variable with possible values (magnet polarities)
2. **Constraint Definition**: Row and column constraints define valid magnet arrangements
3. **Backtracking Search**: The solver uses depth-first search with backtracking
4. **Heuristic Optimization**: Applies constraint propagation and variable ordering heuristics to prune the search space
5. **Solution Extraction**: Returns the first valid complete assignment or reports unsolvability

### Key Components

- **FlexibleBacktrackingSolver**: Core solving engine from AIMA library
- **CspHeuristics**: Constraint-guided variable and value selection
- **Line**: Represents constraints for rows and columns
- **MagnetVariable**: CSP variable for each grid cell
- **Value**: Represents possible magnet states

## 🎯 Problem Context

The Magnet Puzzle is a constraint satisfaction problem where:
- Each cell contains a magnet with a positive or negative pole (or empty)
- Adjacent magnets cannot have the same polarity (positive next to positive repels)
- Each row and column must satisfy specific counts of positive and negative magnets
- The solver finds a valid configuration satisfying all constraints

## 📊 Performance

The solver efficiently handles puzzles through:
- **Intelligent search space reduction** using heuristics
- **Early constraint violation detection** to minimize backtracking
- **Execution time monitoring** for performance analysis

## 📝 Notes

- This is an educational assignment demonstrating CSP solving techniques
- The AIMA library provides well-tested implementations of search algorithms
- Solution time depends on puzzle complexity and constraint density

## 🔗 References

- AIMA (Artificial Intelligence: A Modern Approach) Library: https://github.com/aimacode/aima-java
- Constraint Satisfaction Problems: https://en.wikipedia.org/wiki/Constraint_satisfaction_problem

## ✍️ Author

Created by hamedgoharshad