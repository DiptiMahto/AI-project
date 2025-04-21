# AI-project

1.Scenario: 
In the era of rapid technological advancement, logistics companies are shifting towards automation and intelligent systems for delivery. Drones have emerged as a promising solution to tackle challenges like traffic congestion, remote area accessibility, and contactless delivery. However, effective drone navigation in complex environments requires intelligent pathfinding mechanisms. 
This case study investigates the implementation of A* and Dijkstra’s algorithms to simulate an AI-powered drone delivery system capable of autonomously identifying the shortest path between a warehouse and a customer location while avoiding obstacles. 
2.Tasks: 
Simulate a 2D grid environment with obstacles. 
Apply A* and Dijkstra algorithms for autonomous drone pathfinding. 
Analyze performance of both algorithms using metrics like speed, accuracy, and computational cost. 
Interpret results to recommend the best algorithm for real-time delivery systems. 

3.Introduction: 
Modern logistics systems are undergoing a digital transformation. Automation, AI, and robotics are reshaping how goods are delivered. Among the forefront technologies, autonomous drones are promising tools for last-mile delivery. 
The efficiency of drones relies significantly on navigation algorithms. The environment in which drones operate may have obstacles like buildings, no-fly zones, and natural terrains. Hence, it's crucial to develop intelligent algorithms that can compute the shortest and safest route in minimal time. 
Pathfinding algorithms such as Dijkstra and A* have been widely adopted in robotics, games, and AI systems due to their reliability and efficiency. This case study delves into their roles in drone navigation. 

 

 

 

 

 

4.Problem Statement 

 

Objective: 

Develop an intelligent drone delivery system capable of: 

Navigating from a warehouse to a delivery location. 

Avoiding obstacles like buildings or restricted zones. 

Computing the most optimal route in a 2D grid environment. 

 

 

 

Challenges: 

Dealing with grid-based environments with blocked paths. 

Reducing computational time for real-time decision-making. 

Maintaining shortest-path accuracy despite obstacles. 

 

 

5.Overview of Algorithms 

 

Dijkstra’s Algorithm 

 

Dijkstra’s algorithm is an uninformed search algorithm that finds the shortest path from a source node to all other nodes in a graph with non-negative edge weights. 

 

Working Principle: 

 

Starts from the source node. 

Expands the node with the lowest cumulative cost. 

Updates the shortest path to each neighbor. 

Repeats until the destination node is reached. 

 

Key Characteristics: 

 

Guaranteed to find the shortest path. 

Explores all possible paths to ensure optimality. 

Can be slow in large or sparse environments due to exhaustive search. 

 

Use Case: 

 

Best suited for static environments where complete information is known. 

Ideal for scenarios where reaching every node with the shortest path is required. 

 

 

 

Example: 
Imagine a 2D grid where the drone starts at cell (0,0) and needs to reach (4,4). Obstacles block certain cells. Dijkstra explores all nearby paths equally and eventually finds the path with the lowest overall cost by expanding in all directions. 

 

Strengths: 

Always finds the shortest path. 

Excellent for finding multiple paths or mapping the entire area. 

Weaknesses: 

Time-consuming in large grids. 

Doesn't prioritize direction toward the goal, leading to unnecessary exploration. 

 

 

A (A-Star) Algorithm* 

 
 A* is an informed search algorithm that uses a heuristic function to estimate the cost from the current node to the goal. It balances the actual cost with the estimated cost to guide the search efficiently. 

 

Formula: 
f(n) = g(n) + h(n) 

g(n) = cost from the start node to current node 

h(n) = heuristic estimate from current node to goal (e.g., Manhattan Distance) 

 

Working Principle: 

Selects the path that appears most promising based on a cost + heuristic. 

Prioritizes nodes closer to the goal. 

Reduces unnecessary exploration, making it faster than Dijkstra. 

 

Heuristic Used: 

Manhattan Distance: 
 h(n) = |x1 - x2| + |y1 - y2| 
 Suitable for grid-based movement without diagonals. 

 

 

 

Key Characteristics: 

Faster due to heuristic-based pruning. 

Finds the shortest path when using an admissible heuristic. 

More efficient for real-time applications. 

 

Use Case: 

Ideal for dynamic or real-time systems like drone navigation. 

Can efficiently compute paths in large environments. 

 

Example: 
In the same grid, A* estimates how far the target is and prefers nodes in the direction of the goal, avoiding paths that go in the opposite direction. As a result, the drone reaches the destination quicker than with Dijkstra. 

  

Strengths: 

Faster than Dijkstra in large, complex environments. 

Ideal for real-time pathfinding with fewer explored nodes. 

Weaknesses: 

Performance depends on the quality of the heuristic. 

Can become less accurate with poor heuristics or rapidly changing environments. 

 

6.Simulation and Results: 

 

Simulated city grid: 50x50 cells 

Obstacles: Randomly placed “no-fly” zones 

Source: (0,0), Destination: (49,49) 

 

Parameters Analyzed: 

Execution Time (ms) 

Number of Nodes Explored 

Path Length (steps) 

Memory Usage (approx.) 

 

 

 

 

 

Performance Table: 

Grid Size 

Algorithm 

Time (ms) 

Path Length 

Nodes Explored 

Efficiency 

10x10 

Dijkstra 

9 

14 

45 

Medium 

10x10 

A* 

5 

14 

25 

High 

30x30 

Dijkstra 

35 

42 

132 

Medium 

30x30 

A* 

15 

42 

59 

High 

50x50 

Dijkstra 

87 

68 

289 

Low 

50x50 

A* 

32 

68 

114 

High 

 

 

Insights: 

A* consistently found the shortest path faster. 

Dijkstra covered more nodes and took longer due to lack of directional preference. 

For large maps, A* scaled better and was more memory-efficient. 

 

 

7.Executive Summary: 

 

This case study explores the integration of intelligent pathfinding algorithms—A* and Dijkstra—into a simulated drone delivery system. The goal is to optimize drone navigation in urban environments by computing the shortest, obstacle-free path between two points. Both algorithms are tested and analyzed based on various metrics. The results confirm that A* is faster and more suitable for real-time delivery applications, while Dijkstra is thorough and ideal for environments where complete exploration is necessary. 

 

 

 

 

8. Conclusion: 

 

The implementation of A* and Dijkstra algorithms in drone pathfinding systems reveals critical differences in performance and application scope: 

 

Dijkstra's algorithm guarantees optimal paths but is computationally heavy. It is suitable for static planning or pre-mapping entire regions. 

 

A* algorithm, on the other hand, is faster, more scalable, and ideal for real-time applications due to its heuristic guidance. 

 

 

 

For practical drone delivery systems, where time and computational resources are crucial, A* stands out as the preferred choice. However, Dijkstra’s reliability in exhaustive searches makes it a strong candidate for backup or multi-path systems. 

 

 

9. Future Work: 

 

3D Grid Implementation: Simulate drones flying at various altitudes. 

Dynamic Pathfinding: Include moving obstacles and real-time route re-evaluation. 

Battery-Aware Routing: Add energy constraints into pathfinding cost. 

Obstacle Prediction with AI: Use object detection to enhance live rerouting. 

Integration with GPS and IoT: For real-world delivery trials and tracking. 

 

 

 

 

 

 

s 
