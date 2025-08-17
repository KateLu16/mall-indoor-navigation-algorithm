# Mall Indoor Navigation Algorithm

This project implements an **indoor navigation algorithm** for shopping malls using a combination of **A\*** and **Greedy Search**.  
The system finds the shortest path for the user while considering **crowded areas** (to avoid) and **shops** (that the mall owner wants the user to pass by).

---

## Motivation
When navigating inside large shopping malls, customers not only want to reach their destination efficiently but also:
- **Avoid crowded zones** to save time and increase comfort.
- **Pass by specific shops** that mall owners want to promote (marketing purpose).

This algorithm integrates these factors into the navigation logic.

---

## How It Works
The navigation system is built on **grid-based pathfinding** with the following logic:

1. **Input nodes**
   - `start_node`: User’s current position.
   - `end_node`: Target shop/goal.
   - `crowd_nodes`: Points representing crowded zones (higher penalty).
   - `sell_nodes`: Shops the mall owner wants users to pass by.

2. **Algorithm**
   - **A\***: Ensures the shortest path is computed with heuristic optimization.
   - **Greedy strategy**: Adds extra preference for visiting `sell_nodes`.
   - **Crowd penalty**: `crowd_nodes` increase cost, making the algorithm avoid them.

3. **Output**
   - The optimal path that:
     - Starts at `start_node`
     - Ends at `end_node`
     - Avoids `crowd_nodes`
     - Passes through `sell_nodes` if beneficial

---

## Installation
```bash
git clone https://github.com/KateLu16/mall-indoor-navigation-algorithm.git
cd mall_indoor_navigation_algorithm
pip install -r requirements.tx
```

---

## Usage
Run the visualisation:

```bash
python src/main.py
```
---

## Control

- Press 1 to add/remove the crowd node

- Press 2 to add/remove the sell node

- Press 3 to set the start node

- Press 4 to set the end node

- Press R to Run pathfinding

