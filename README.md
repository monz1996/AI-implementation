# AI-implementation

Problem

Create a 2d GRID , this GRID has different entities which I will explain in detail in just
a moment, The important part is that the gird will contain the AI AGENT and a number
of HOSTAGES, the objective of this game simulation is for the AGENT to save as
many HOSTAGES as possible and return to a specified coordinates, I was asked to
return a valid series of ACTIONS if exists which must be generated using different AI
search FUNCTIONS.

1- Create all the entities:
- The GRID: Basically a 2D ARRAY in which all the entities of the problem are created.

- The AGENT: the AGENT can perform various ACTIONS, will explain in detail.

- The ENEMIES: the AGENT cannot enter a cell in which an ENEMY exist.

- The SAFE CELL: Hostage can be delivered to the SAFE CELL to be SAVED.

- The HOSTAGES: HOSTAGES start with a random initial health bar, each lose 2 HP
for every ACTION the AGENT takes.

- The PILLS: Increase the AGENT HP and all the Hostages HP by 20 when taken.

- The PADS: PADS come in couples, each pad can be used to teleport the AGENT to
the corresponding PAD.

- AGENT ACTIONS:

• MOVE: move to an adjacent cell, either horizontally or vertically.
• TAKE PILL:
• USE PAD:
• CARRY HOSTAGE: The AGENT can only CARRY one HOSTAGE at a time.
• DROP HOSTAGE: the AGENT can perform this ACTION only when it is in the
SAFE CELL to successfully deliver the HOSTAGE DEAD or ALIVE.
• KILL: killing the adjacent enemies losing 20 HP in the process, adjacent
horizontally or vertically only.

IDEA

The initial idea was to take the dimensions of the GRID from the user, get random
values for all the entities which I mentioned previously and create a class for the agent.
Implement the PATHCOST function and HEURISTIC function and FINALLY
implement the search algorithms to return the required results.

IMPLEMENTATION

- Initialized the GRID.
- Created all the entities and put them in the GRID.
- AGENT CLASS:
• HP
• NO OF PADS USED

• NO OF PILLS TAKEN
• NO OF HOSTAGES SAVED
• BOOLEAN CARRYING HOSTAGES
• NO OF ENEMIES KILLED
• A CLASS FOR EACH ACTION

WHY DO I HAVE NUMBER OF PILLS AS A PARAMETER ?

PATHCOST ِAND HEURISTIC FUNCTION:
- CALCULATES MINIMUM AMOUNT OF HEALTH THE HOSTAGES WILL
LOSE TAKING JUMPING PADS INTO CONSIDERATION AND THE AGENT
LOSE AS A RESULT OF THIS ACTION, I DECIDED TO TAKE PILLS AS
NEGATIVE VALUE.

RESULT

The Search functions where able to find a solution to an overwhelming amount of cases.
The only issue was with extreme edge cases in which the Search Function was not able
to find an existing solution.

Looking Back

This was the biggest project I have ever done in my life it took 2000 lines of codes not
considering the many many lines I have deleted and the other classes that I implemented
to ease the implementation of the project, it was also very convoluted and I am glad that
I had the opportunity of working on it solo and gaining this huge and nourishing
experience.

Challenges

- Project implementation.

- Avoiding Repeated states which can easily result in an infinite loop.

Changes

- Instead of taking into consideration the number of each entity for the state, I will also
consider the positions of each entity, I think that would have solved the edge cases.
- Find the shortest distance in the Heuristic function.
