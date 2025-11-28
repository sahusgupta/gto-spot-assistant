# GTO Hold'em Spot Solver

This project is an easy-to-use, GTO-inspired spot solver for No-Limit Texas Hold’em. The goal is to help players study specific situations (ranges, stacks, board, bet sizes) and get clear, actionable strategy recommendations. It’s designed to be intuitive and educational, not a black-box high-volume solver.

Under the hood, the solver models each spot as a small two-player zero-sum game and uses Counterfactual Regret Minimization (CFR) or similar iterative methods to approximate equilibrium strategies. Hold’em-specific details (ranges, boards, bet trees) are mapped into a simplified abstract game that’s fast enough to experiment with on a single machine. The long-term plan is to layer an AI explainer on top to turn solver output into human-readable coaching.

**v1 Scope & Constraints:**  
v1 is limited to heads-up, single-spot scenarios with a fixed, small betting tree (e.g., river-only or very simple flop trees, predefined bet sizes, and two players). Ranges will be simplified (presets or coarse abstractions) rather than full combo-by-combo inputs, and performance is optimized for clarity and speed over absolute precision. The initial focus is a CLI/tooling interface and a single toy game/spot that can be solved end-to-end and inspected.
