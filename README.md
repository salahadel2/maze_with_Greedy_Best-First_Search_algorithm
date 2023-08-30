# maze_with_Greedy_Best-First_Search_algorithm
maze-solving algorithm using Greedy Best-First Search algorithm
## Greedy Best-First search is a search algorithm that expands the node that is closest to the goal, as estimated by a heuristic function (explore the node that has the smallest value of h(n)).
### Greedy Best-First search algorithm steps:-
• Start with the initial state as the current state.
• Maintain a priority queue (often implemented using a heap) to store the states yet to be explored, The priority is determined by the heuristic function.
•  While the priority queue is not empty:
   - Remove the state with the highest priority (lowest heuristic value) from the queue.
   - If the removed state is the goal state, a solution has been found. Exit the loop.
•  Generate successor states of the current state, considering all possible actions that can be taken from that state.
• For each successor state, compute its heuristic value using the heuristic function. 
• Add the selected successor state(s) to the priority queue.
• If no successor states can be added to the queue, backtrack to the previous state and continue the search.

### Greedy Best-First search algorithm Pseudocode:-

function greedy_best_first_search(problem):
    Initialize an empty priority queue frontier
    Add the initial state to the frontier with priority based on the heuristic value
    Initialize an empty set explored
    
    while frontier is not empty:
        current_node = remove the node with the highest priority from the frontier
        if current_node is the goal state:
            return the solution

        if current_node is not in explored:
            add current_node to explored

            for each neighbor_node of current_node:
                if neighbor_node is not in explored:
                    add neighbor_node to the frontier with priority based on the heuristic value
                else if neighbor_node is in the frontier with a higher priority:
                    update the priority of neighbor_node in the frontier

    return failure (no solution found)
