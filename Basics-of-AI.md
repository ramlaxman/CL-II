Search can be defined as a problem-solving technique that enumerates a problem space from an initial position in search
of a goal position (or solution). 

## Classes of Search

### GENERAL STATE SPACE SEARCH

A search space:  When solving a problem, it’s convenient to think about the solution space:
-	Number of actions 
-	New state of the environment as we perform those actions. 

As we take one of multiple possible actions (each have their own cost), our environment changes and opens up alternatives for new actions. 

As is the case with many kinds of problem solving:
-	Some  paths lead to dead-ends 
-	Others lead to solutions
-	There may also be multiple solutions, some better than others. 
#### Summary: 
The problem of search is to find a sequence of operators that transition from the start to goal state. 
That sequence of operators is the solution.

To avoid dead-ends and then select the best solution available is a product of our particular search strategy which is mentioned as follows:

Search in a Physical Space
Let’s consider a simple search problem in physical space (Figure 2.1). 

=> Our initial position is ‘A’ from which there are three possible actions that lead to
position ‘B,’ ‘C,’ or ‘D.’ 

=> Places, or states, are marked by letters. 

![1](https://user-images.githubusercontent.com/1982225/27367755-4db2cfb6-566c-11e7-8e70-9d697166d430.png)

=> At each place, there’s an opportunity for a decision, or action. The action (also called an operator) is simply a legal move between one place and another. 
Implied in this exercise is a goal state, or a physical location that we’re seeking.

=> This search space (shown in Figure 2.1) can be reduced to a tree structure as illustrated in Figure 2.2. 

=> The search space has been minimized here to the necessary places on the physical map (states) and the transitions
that are possible between the states (application of operators). 

Each node in the tree is a physical location and the arcs between nodes are the legal moves.
The depth of the tree is the distance from the initial position.Uninformed Search 23

