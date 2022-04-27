# WindyGridworld

Here is my solution to Exercises 6.9 and 6.10 of the book "Reinforcement Learning: An Introduction (Sutton & Barto)"

## The Problem

**Exemple 6.5: Windy Gridworld** Figure 6.10 shows a standard gridworld,
with start and goal states, but with one difference: there is a crosswind upward
through the middle of the grid. The actions are the standard four—up, down,
right, and left—but in the middle region the resultant next states are shifted
upward by a “wind,” the strength of which varies from column to column. The
strength of the wind is given below each column, in number of cells shifted upward.
For example, if you are one cell to the right of the goal, then the
action left takes you to the cell just above the goal. Let us treat this as an
undiscounted episodic task, with constant rewards of −1 until the goal state
is reached. Figure 6.11 shows the result of applying ε-greedy Sarsa to this
task, with ε = 0.1, α = 0.5, and the initial values Q(s, a) = 0 for all s, a. The
increasing slope of the graph shows that the goal is reached more and more
quickly over time. By 8000 time steps, the greedy policy (shown inset) was
long since optimal; continued ε-greedy exploration kept the average episode
length at about 17 steps, two more than the minimum of 15. Note that Monte
Carlo methods cannot easily be used on this task because termination is not
guaranteed for all policies. If a policy was ever found that caused the agent to
stay in the same state, then the next episode would never end. Step-by-step
learning methods such as Sarsa do not have this problem because they quickly
learn during the episode that such policies are poor, and switch to something
else.

![alt text](https://github.com/LorisGaven/WindyGridworld/blob/main/problem.jpg?raw=true)

## The Exercises

**Exercise 6.9: Windy Gridworld with King's Moves (programming)** Re-solve the windy 
gridworld assuming eight possible actions, including the diagonal moves, rather than four.
How much better can you do with the extra actions?

**Exercise 6.10: Stochastic Wind (programming)** Re-solve the windy gridworld task with
King's moves, assuming that the effect of the wind, if there is any, is stochastic, sometimes
varying by 1 from the mean values given for each column. That is, a third of the time 
you move exactly according to these values, as in the previous exercise, but also a third
of the time you move one cell above that, and another third of the time you move one 
cell below that.
