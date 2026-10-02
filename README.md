# Dynamic Resource Allocation with Markov Decision Processes

A portfolio project that models cloud compute scaling as a **Markov Decision Process (MDP)**. The agent balances service quality against infrastructure cost while deciding whether to scale up, maintain capacity, or scale down.

## Why this project matters

Static autoscaling rules can be brittle. This project turns resource allocation into a sequential decision problem where today's action affects tomorrow's state and cost.

## AI formulation

- **State:** workload level and current capacity
- **Actions:** scale up, maintain, scale down
- **Transition:** probabilistic workload movement plus capacity changes
- **Reward:** low cost when capacity matches demand, penalties for overload and unnecessary capacity
- **Objective:** maximize expected discounted long-term reward

## Algorithms

1. Value Iteration
2. Policy Iteration
3. Convergence and policy comparison

## Example output

The demo prints the learned action policy across workload/capacity states and reports the final value function. This makes the connection between the mathematical MDP and an operational scaling policy explicit.

## Run

```bash
python examples/demo.py
```

## Tests

```bash
pytest -q
```

## Portfolio talking points

- Why sequential decisions are better modeled with an MDP than a one-shot classifier
- How discount factor changes short-term vs. long-term behavior
- How reward design encodes operational tradeoffs
- Why policy iteration and value iteration can converge differently

## CS221 connection

Inspired by classical AI concepts commonly covered in CS221: Markov decision processes, dynamic programming, and sequential decision-making. The application framing, implementation, experiments, and documentation are independently developed.

## GitHub metadata

**Repository name:** `mdp-resource-optimizer`

**Description:** Optimize dynamic compute capacity with Markov Decision Processes, value iteration, and policy iteration.

**Topics:** `artificial-intelligence` `mdp` `markov-decision-processes` `value-iteration` `policy-iteration` `reinforcement-learning` `python` `cs221`
