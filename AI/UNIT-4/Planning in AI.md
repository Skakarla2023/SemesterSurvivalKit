# Planning in AI

- Planning in AI refers to deciding a sequence of actions to reach a goal from the current state.
- Like humans make plans before tasks, computers also makes plan so that it can achieve goals.
- Planning involves asking the following questions:
  1. Where am I now?(current state)
  2. Where I want to go?(Goal state)
  3. How should I reach there?(Action)

## Components of a Planning System

**1. Start state**
- Where the agent starts


**2. Goal state**
- Where the agent needs to reach.

**3. Actions**
- Things that the agent can do.

**4. Plan**
- Final ordered list of items.

**5. Planner**
- (Algorithm) thinks and decides which steps to take.

**6. Execution**
- performs steps in real world.


## Types of Planning in AI
- There are two types of planning in AI. They are:
  1. Goal stack planning
  2. Hierearchical planning


### Goal Stack Planning

- In Goal stack planning, the plan is stored like a stack.
- AI keeps goals on top and expands until goal is reached.
- AI solves by breaking a goal into sub-goals(subtasks).

#### Eg:

- Goal: Making tea.
- Steps involved:
  1. Boil water
  2. Add tea leaves
  3. Add sugar
  4. Add milk
 
### Hierarchical Planning

- In Hierarchical Planning a larger task is broken into smaller tasks and each small task is further broken down.
- It works like a **Tree**.
  - Big Goal(top)
  - Sub-goals(middle)
  - Actions(Bottom)
 
#### Eg:

- Goal: Planning a birthday party.
- Sub-goals:
  - Order food
    → Order pizzas
    → Buy drinks
  - Invite friends
    → call friends
  - Decorate room
    → buy balloons
    → buy decorations

### Difference between goal stack and hierarchical

| Point   | Goal Stack Planning | Hierarchical Planning |
|---------|---------------------|-----------------------|
| struture| Stack/LIFO | tree|
|Works by | Breaking goals into subgoals one at a time|breaking tasks into multiple levels.|
| Best for| small tasks|complex tasks|
|Example| Making Tea|Planning a birthday party|

