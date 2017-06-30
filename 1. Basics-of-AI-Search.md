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
##### Summary: 
The problem of search is to find a sequence of operators that transition from the start to goal state. 
That sequence of operators is the solution.

To avoid dead-ends and then select the best solution available is a product of our particular search strategy which is mentioned as follows:

#### Search in a Physical Space

Let’s consider a simple search problem in physical space (Figure 2.1). 

- Our initial position is ‘A’ from which there are three possible actions that lead to position ‘B,’ ‘C,’ or ‘D.’ 

- Places, or states, are marked by letters.

- At each place, there’s an opportunity for a decision, or action. The action (also called an operator) is simply a legal move between one place and another. Implied in this exercise is a goal state, or a physical location that we’re seeking.

- This search space (shown in Figure 2.1) can be reduced to a tree structure as illustrated in Figure 2.2. 

- The search space has been minimized here to the necessary places on the physical map (states) and the transitions
that are possible between the states (application of operators). 

- Each node in the tree is a physical location and the arcs between nodes are the legal moves. The depth of the tree is the distance from the initial position.

![1](https://user-images.githubusercontent.com/1982225/27413682-89681788-571a-11e7-8dbe-d7a3e7d1faa1.png)


![2](https://user-images.githubusercontent.com/1982225/27403190-2e069672-56e7-11e7-8f0b-b09934e59da6.png)

#### Search in a Puzzle Space

The “Towers of Hanoi” puzzle: 
The object of this puzzle is to move a number of disks from one peg to another (one at a time), with a number of constraints
that must be met. 

![3](https://user-images.githubusercontent.com/1982225/27381273-cfeb0268-569f-11e7-964f-f41ca6eb554c.png)


The only disk that may move is the small disk at the top of Peg A. For this disk, only two legal moves
are possible, from Peg A to Peg B or C. From this state, there are three potential moves:

1. Move the small disk from Peg C to Peg B.
2. Move the small disk from Peg C to Peg A.
3. Move the medium disk from Peg A to Peg B.

The first move (small disk from Peg C to Peg B), while valid is not a potential move, as we just moved this disk to Peg C (an empty peg). Moving it a second time serves no purpose (as this move could have been done during the prior transition), so there’s no value in doing this now (a heuristic)<sup>[1](#myfootnote1)</sup>. The second move is also not useful (another heuristic), because it’s the reverse of the previous move.

Purpose: When our sequence of moves brings us from the initial position to the goal, we have a solution. The goal state in itself is not interesting, but instead what’s interesting is the sequence of moves that brought us to the goal state. The collection of moves (or solution), done in the proper order, is in essence a plan for reaching the goal. The plan for this configuration of the puzzle can be identified by starting from the goal position and backtracking to the initial position

#### Search in a Adversarial Space

Also known as game trees, these structures enumerate the possible moves by each player allowing the search algorithm to find an effective strategy for playing and winning the game.

![image](https://user-images.githubusercontent.com/1982225/27416693-9e372020-572c-11e7-9a6b-a46dbb0cb61e.png)

Note that the depth of the tree determines the length of the game (number of moves). It’s implied in the tree that the shaded node is the final move to be made, and the player that makes this move loses the game. Also note the size of the tree. In this example, using six objects, a total of 28 nodes is required. If we increase our tree to illustrate a pile of seven objects, the
tree increases to 42 nodes.



-----------------------
<a name="myfootnote1">[1]</a>: A heuristic is a simple or efficient rule for solving a given problem or making a decision.
