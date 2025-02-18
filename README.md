# 112_2_Operations_Research_Adaptive_Task_Scheduling

## Overview

This project focuses on developing a heuristic algorithm for task scheduling, taking into account human productivity variations, task deadlines, penalties, and efficiency boosts. The goal is to optimize task allocation and minimize the gap between the heuristic approach and the optimal solution obtained via Gurobi.

## Features

- **Task Scheduling Algorithm**: Implements a heuristic method for assigning tasks based on an index function.
- **Optimization with Gurobi**: Provides a benchmark for evaluating the heuristic performance.
- **Parameterized Scenarios**: Analyzes the impact of different factors such as working hours, efficiency boosts, and task complexity on scheduling outcomes.
- **Data Generation**: Simulates task datasets using uniform and discrete uniform distributions.

## Methodology

### Index Calculation

- Computes an index for each task based on its value, required time, due date, penalty, and efficiency considerations.
- Sorts tasks in descending order of index value and assigns them iteratively.
- Handles overdue tasks by prioritizing penalty minimization.

### Data Generation

- Generates synthetic task datasets with varying parameters.
- Uses random distributions for attributes like release time, due date, task duration, value, and penalty.

## Experiments & Analysis

- Compares heuristic scheduling results with optimal solutions from Gurobi.
- Evaluates how parameter variations impact task allocation and objective values.

## Installation

### Prerequisites

- Python 3.x
- Gurobi Optimizer (with a valid license)
- Required Python libraries:

## Results & Insights

- Increasing daily working hours ($H$) improves task completion and reduces the heuristic-optimality gap.
- Efficiency boost ($B$) impacts Gurobi results but is not explicitly considered in the heuristic algorithm.
- Higher efficiency costs ($E_{change}$) reduce total objective value and widen the heuristic-optimality gap.

## Future Improvements

- Implement continuous assignment variables to allow partial task execution over multiple days.
- Incorporate dynamic efficiency modeling based on mood and energy variations.
- Refine heuristic methods to better approximate optimal solutions.
