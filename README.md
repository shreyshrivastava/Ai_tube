Tube Network Route Finder
This project demonstrates how to use graph traversal algorithms to find optimal routes in a subway (tube) network. With implementations of Depth-First Search (DFS), Breadth-First Search (BFS), and Uniform Cost Search (UCS), it provides insights into pathfinding across a transit network, with an emphasis on efficiency and cost-effectiveness.

Table of Contents
Overview
Data Structure and Setup
Pathfinding Algorithms
Getting Started
Usage
Applications
Future Directions
Contributions
Overview
This project reads station connection and zone data from a CSV file to build a graph representation of a tube network, where each station is a node and each route between stations is an edge. Using various search algorithms, the notebook finds routes between any two stations, providing metrics like path length, travel cost, and node expansion count. Zone information is also included, allowing realistic simulations of zone-based fare calculations.

Data Structure and Setup
Data Import and Graph Creation: The project reads a CSV file (tubedata.csv) with fields for start station, end station, travel cost, and zone information. It then constructs:

station_dict: A dictionary mapping each station to its connected stations and respective travel costs.
zone_dict: A dictionary to map each station to its zone(s), enabling zone-based constraints in UCS.
Library Imports: Essential libraries include pandas, collections, heapq, and queue to manage data processing, graph traversal, and priority queuing.

Pathfinding Algorithms
The project includes implementations of three graph traversal algorithms:

Depth-First Search (DFS): Finds a route by exploring as far as possible along each branch before backtracking. It provides a viable route if one exists but is not necessarily cost-effective.
Breadth-First Search (BFS): Finds the shortest path in terms of station count, helpful in transit networks with uniform travel costs.
Uniform Cost Search (UCS): Identifies the least-cost path, considering variable travel costs and zone constraints, ideal for fare-based route optimization.
Getting Started
Prerequisites
Ensure you have the following libraries installed:

bash
Copy code
pip install pandas
You will also need collections, heapq, and queue, which are part of Python's standard library.
Setup
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/Tube-Network-Route-Finder.git
Add your own tube network data in a CSV file named tubedata.csv with columns for start station, end station, travel cost, and zones.
Run the notebook to build the station graph and execute the algorithms on specified routes.
Usage
To calculate a route between stations, use the function:

python
Copy code
routes(station_dict, 'StartStation', 'EndStation')
This function will output the route found by each algorithm, along with the travel cost and expanded node count.

Applications
Transit System Optimization: Helps in determining efficient routes, valuable for transit route planners.
Fare Calculation: UCS and zone data simulate fare calculations based on routes.
Algorithm Education: Demonstrates graph traversal algorithms on a practical dataset, useful for learning and teaching graph algorithms.
Future Directions
A Search Implementation*: Incorporate heuristic-based A* to combine UCS with estimated costs, improving efficiency.
Dynamic Cost Adjustments: Modify travel costs dynamically to reflect peak and off-peak hours.
Data Visualization: Add visualizations of the tube network and routes using libraries like networkx and matplotlib.
Contributions
Contributions are welcome! Please submit pull requests to add features, enhance documentation, or improve the algorithm implementations.

